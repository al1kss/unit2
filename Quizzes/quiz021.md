# Quiz 021

## Code
```.py
from matplotlib import pyplot as plt
import matplotlib

plt.style.use('ggplot')
matplotlib.use("MacOSX")

start = -10
step = 0.01
x, y = [], []

for i in range(int(20/step)):
    x.append(start+step*i)
    y.append(2 * (x[-1] + 5) ** 2)

plt.plot(x, y, linewidth=2, color="#fb8500")
plt.xlabel("x")
plt.ylabel("$y = 2(x+5)^2$")
plt.title("Graph for the parabola $y = 2(x+5)^2$")
plt.legend(["$y = 2(x+5)^2$"])

ax, ay = [-5, -5], [0, 450]
plt.plot(ax,ay, "--", color="blue")

plt.show()
```

## Proof of work
<img width="637" alt="Screenshot 2024-11-11 at 0 47 11" src="https://github.com/user-attachments/assets/edb030d3-d3b5-4993-a6f2-16063323cca2">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 08 (1)](https://github.com/user-attachments/assets/67b3657d-3041-4ad7-a79b-0a74d3dba1cc)

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz021
