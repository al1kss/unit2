# Quiz 025

## Code
```.py
def count_letters(my_dict:dict, msg:str):
    for k,v in my_dict.items():
        for i in msg:
            if k == i:
                v += 1
                my_dict[k] = v
    return my_dict

a, b = input().split(', ', 1)
a = eval(a)
b = b.strip('"')

print(count_letters(a, b))

```

## Proof of work
<img width="447" alt="Screenshot 2024-12-04 at 6 58 35" src="https://github.com/user-attachments/assets/d8698932-37bc-448c-86d1-d326f1b84b3f">

## Part B
<img width="667" alt="Screenshot 2024-12-04 at 6 56 56" src="https://github.com/user-attachments/assets/67ad1d5f-06ba-420d-8e82-6200c9b30255">

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz025
