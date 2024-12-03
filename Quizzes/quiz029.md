# Quiz 029

## Code
```.py
import requests
from matplotlib import pyplot as plt
import matplotlib

plt.style.use("ggplot")
matplotlib.use("MacOSX")

server_ip = "192.168.4.137"

# Fetch data from the server
r = requests.get(f"http://{server_ip}/readings")
data = r.json()
readings = data.get("readings", [])

temp = []
hum = []

for k in readings:
    for v in k:
        if v["sensor_id"] == 11:
            temp.append(v["value"])
        if v["sensor_id"] == 10:
            hum.append(v["value"])

fig = plt.figure(figsize=(10, 8))

plt.subplot(4, 1, 1)
plt.plot(temp[0:801], color="red")
plt.title("Temperature")

plt.subplot(4, 1, 2)
plt.plot(hum[0:801], color="yellow")
plt.title("Pressure")

sum = []
for i in range(801):
    sum.append(temp[i]+hum[i])
plt.subplot(4, 1, 3)
plt.plot(sum, color="blue")
plt.title("Sum of Temp and Pressure")

avg = []
for i in range(801):
    avg.append((temp[i]+hum[i])/2)
plt.subplot(4, 1, 4)
plt.plot(avg, color="black")
plt.title("Average of Temp and Pressure")

plt.show()
```

## Proof of work
<img width="876" alt="Screenshot 2024-12-04 at 6 45 30" src="https://github.com/user-attachments/assets/217a141b-b024-4fe1-9381-ff4ddb0f6202">


### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz029
