# Quiz 027

## Code
```.py
import matplotlib
import numpy as np
import matplotlib.pyplot as plt

def sort_dict(in_dict:dict):
    l = []
    out = {}
    for k,v in in_dict.items():
        l.append(v)
    l.sort(key=str) #convert all elements to str for sorting
    for j in l:
        for i in in_dict:
            if in_dict[i] == j:
                out[i] = j
    return out

a = eval(input())
print(sort_dict(a))

## PART B

plt.style.use("ggplot")
matplotlib.use("MacOSX")

x = np.linspace(0, 1, 500)  # 500 points between 0 and 1
y = np.sin(2 * np.pi * x)

plt.figure(figsize=(8, 4))
plt.plot(x, y, color='blue')
plt.title("Graph of $y = \sin(2\pi x)$")
plt.xlabel("x")
plt.ylabel("y")
plt.show()

```

## Proof of work
<img width="724" alt="Screenshot 2024-12-04 at 6 41 23" src="https://github.com/user-attachments/assets/e230ea06-91ae-4c24-94e6-9b78f08428dc">

## Part B
<img width="748" alt="Screenshot 2024-12-04 at 7 11 34" src="https://github.com/user-attachments/assets/fb380f13-f8ee-4231-8304-b30fe21ef1a8">

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz027
