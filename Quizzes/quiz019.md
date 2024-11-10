# Quiz 019

## Code
```.py
import random
random.seed(1234)

def produce(n=5, m=3, s=2):
    output = "|   x   |    y    |"
    for i in range(n):
        output += "\n"
        r = random.randint(0,100)
        e = r ** (0.5 * (m / s) ** 2)
        output += f"|  {r:<5}|  {e:<7.2f}|"
    return output

print(produce())
```

## Proof of work
<img width="163" alt="Screenshot 2024-11-11 at 0 43 24" src="https://github.com/user-attachments/assets/bb486da9-c057-4be3-8eb9-5bc7c407efab">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 06 (1)](https://github.com/user-attachments/assets/409b9413-19bc-4442-9bf9-f0246b34efdb)


### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz019
