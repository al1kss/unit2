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

## Part B

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz025
