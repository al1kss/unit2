# Quiz 022

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
    x.append(start + step * i)
    y.append(abs(x[-1]))

plt.plot(x, y, linewidth=2, color="#fb8500")
plt.xlabel("x")
plt.ylabel("$y = |x|$")
plt.title("Graph for the $y = |x|$")
plt.legend(["$y = |x|$"])

plt.show()
```

## Proof of work
<img width="635" alt="Screenshot 2024-11-11 at 0 49 32" src="https://github.com/user-attachments/assets/2cf4af97-9536-4275-a1b2-bf3a67c21638">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 08](https://github.com/user-attachments/assets/a173a265-0839-47cd-8010-1af1b2eb137b)

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz022
