# Quiz 023

## Code
```.py
from matplotlib import pyplot as plt
import matplotlib
import numpy as np

plt.style.use('ggplot')
matplotlib.use("MacOSX")

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
x = []

for i in range(0, 320, 10):
    x.append(i)

m, b = np.polyfit(x,h,1)
print(f"The linear model for the data is y={m:.2f}x+({b:.2f})")
def model(x, m, b):
    return m*x+b

x_model = [min(x), max(x)]
y_model = [model(min(x), m, b), model(max(x), m, b)]

plt.plot(x_model, y_model, color="green")

plt.scatter(x,h)

plt.ylabel("Humidity (%)")
plt.xlabel("Time (min)")

plt.show()
```

## Proof of work
<img width="639" alt="Screenshot 2024-11-11 at 0 51 48" src="https://github.com/user-attachments/assets/26119a07-5970-430b-8363-953f3ab9701d">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 05](https://github.com/user-attachments/assets/9c639871-b56b-4f77-abc4-372b658deb19)

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz023
