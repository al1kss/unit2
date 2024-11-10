# Quiz 017

## Code
```.py
def get_truth(num:int):
    bit0, bit1, bit2 = 1, 1, 1
    output = "| A | B | C |"
    for i in range(2*2**(num-1)):
        output += "\n"
        if i%4 == 0:
            bit2 = not bit2
        if i%2==0:
            bit1 = not bit1
        if i%1==0:
            bit0 = not bit0
        output +=  f"| {bit2*1} | {bit1*1} | {bit0*1} |"

    return output
num = int(input())
print(get_truth(num))
```

## Proof of work
<img width="134" alt="Screenshot 2024-11-09 at 19 32 33" src="https://github.com/user-attachments/assets/100e61c6-8a90-47a4-a3ab-f3d8b383826b">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 02](https://github.com/user-attachments/assets/0ce2bdfc-f9c4-4bfe-8225-e89dddbca74f)
![WhatsApp Image 2024-11-11 at 00 37 01](https://github.com/user-attachments/assets/169f1464-4d18-4f92-91ec-1f723822a766)

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz017
