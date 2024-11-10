# Quiz 020

## Code
```.py
from matplotlib import pyplot as plt
import matplotlib
import random

random.seed(1234)
matplotlib.use('MacOSX')
plt.style.use('ggplot')

def produce(n=5, m=3, s=2):
    x, y = [],[]
    for _ in range(n):
        r = random.randint(0,100)
        x.append(r)
        e = r ** (0.5 * (m/s) ** 2)
        y.append(e)
    return x, y

ax, ay = produce(n=10)
plt.plot(ax, ay, 'xr') #'or' marker is a circle, color red, no line
plt.show()

```

## Proof of work
<img width="644" alt="Screenshot 2024-11-11 at 0 45 21" src="https://github.com/user-attachments/assets/6f7bb3dc-893d-45b0-9b81-01442b22089c">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 06](https://github.com/user-attachments/assets/26dc2b3c-2554-41a0-b1a6-b2e976c1d5a1)


### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz020
