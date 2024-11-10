# Quiz 018

## Code
```.py
def get_truth():
    bit0, bit1, bit2 = True, True, True
    output = "| A | B | C | AB+(not B)+not(CB) |"
    for i in range(8):
        output += "\n"
        if i%4 == 0:
            bit2 = not bit2
        if i%2==0:
            bit1 = not bit1
        if i%1==0:
            bit0 = not bit0
        result = (bit2 and bit1) + (not bit1) + (not (bit1 and bit0))
        output +=  f"| {bit2*1} | {bit1*1} | {bit0*1} |         {result-1 if result > 0 else result}          |"
    return output

print(get_truth())
```

## Proof of work
<img width="284" alt="Screenshot 2024-11-11 at 0 40 33" src="https://github.com/user-attachments/assets/c64f24a5-b3d0-4362-9be7-93c045b98a23">

## Part B
![WhatsApp Image 2024-11-11 at 00 37 03 (1)](https://github.com/user-attachments/assets/c8dabd87-f068-4544-97e0-f000fe55dcf6)
![WhatsApp Image 2024-11-11 at 00 37 03](https://github.com/user-attachments/assets/7f258b9c-8470-4085-8c6b-837e9df57872)

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz018
