# Quiz 028

## Code
```.py

import matplotlib
import numpy as np
import requests
from matplotlib import pyplot as plt

def moving_average(windowSize:int, x:list)->list:
    x_smoothed = []
    for i in range(0, len(x)-1-windowSize):
        x_section = x[i:i+windowSize]
        x_average = sum(x_section)/windowSize

        x_smoothed.append(x_average)

    return x_smoothed


server_ip = "192.168.4.137"

r = requests.get(f"http://{server_ip}/readings")
data = r.json()
readings = data.get("readings", [])
values = []
for k in readings:
    for v in k:
        if v["sensor_id"] == 11:
            values.append(v["value"])

plt.style.use("ggplot")
matplotlib.use("MacOSX")

def model(x, m, b):
    return m*x+b

fig = plt.figure(figsize=(10,8))
plt.subplot(3, 1, 1)
plt.xlim(600, 1600)

smoothed = moving_average(windowSize=50, x=values)
plt.plot(smoothed)
plt.title("Smoothed graph")

x1 = list(range(0, 7000))

plt.subplot(3, 1, 2)
plt.xlim(600, 1600)
a,b,c = np.polyfit(x1[600:1600], smoothed[600:1600], deg=2)
models = []
for x in x1:
    models += [a*x**2 + b*x + c]
plt.plot(models, color="black")
plt.title("Quadtratic model")

plt.subplot(3, 1, 3)
plt.xlim(600, 1600)

m,b = np.polyfit(x1[600:1600], smoothed[600:1600], deg=1)

x_model = [min(x1), max(x1)]
y_model = [model(min(x1), m, b), model(max(x1), m, b)]
plt.plot(x_model, y_model, color="blue")
plt.title("Linear model")


plt.show()

```

## Proof of work
<img width="894" alt="Screenshot 2024-12-04 at 6 43 59" src="https://github.com/user-attachments/assets/17b2bc8b-1401-4dbc-913a-1251bd97829a">

## Part B

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz028
