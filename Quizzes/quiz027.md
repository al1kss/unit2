# Quiz 027

## Code
```.py
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

```

## Proof of work
<img width="724" alt="Screenshot 2024-12-04 at 6 41 23" src="https://github.com/user-attachments/assets/e230ea06-91ae-4c24-94e6-9b78f08428dc">

## Part B

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz027
