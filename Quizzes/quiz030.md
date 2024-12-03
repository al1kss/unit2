# Quiz 030

## Code
```.py
import requests
from matplotlib import pyplot as plt
import matplotlib
from matplotlib.gridspec import GridSpec
from matplotlib.pyplot import figure

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

fig = plt.figure(figsize=(10, 5))

grid = GridSpec(nrows=3, ncols=4, figure=fig)
plt.subplots_adjust(hspace=0.5)

box1 = fig.add_subplot(grid[1, 0]) #row 1, column 0
plt.plot(temp[0:801], color="red")
plt.title("Sensor ID: 11")


dif = []
for i in range(801):
    dif.append(temp[i]-hum[i])
box2 = fig.add_subplot(grid[0:3, 1:3]) #row 0, 1, 2, column 1,2
plt.plot(dif, color="blue")
plt.title("Sensor #11 - #10")

box3 = fig.add_subplot(grid[1, 3])
plt.plot(hum[0:801], color="yellow")
plt.title("Sensor ID: 10")

plt.show()


```

## Proof of work
<img width="891" alt="Screenshot 2024-12-04 at 6 46 58" src="https://github.com/user-attachments/assets/064f9d3c-be0d-426b-b424-88b4f740995a">


### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz030
