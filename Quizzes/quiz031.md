# Quiz 031

## Code
```.py
import matplotlib
from matplotlib import pyplot as plt

plt.style.use("ggplot")
matplotlib.use("MacOSX")

x = [i/10 for i in range(-20,21)]
y = [i**2 for i in x]
y1 = [-i for i in y]

plt.plot(x, y, label = ' Parabola 1 (x-axis)')
plt.plot(x, y1, label="Parabola 2 (x-axis)")
plt.plot(y,x, label="Parabola 3 (y-axis)")
plt.plot(y1,x, label="Parabola 4 (y-axis)")
plt.legend()

plt.show()
```

## Proof of work
<img width="574" alt="Screenshot 2024-12-04 at 6 49 33" src="https://github.com/user-attachments/assets/95134570-f475-45f5-bfb4-8d46cbae9918">

## Part B

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz031
