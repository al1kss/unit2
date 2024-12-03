# Quiz 026

## Code
```.py
def flip(in_dict: dict):
    out = {}
    for k, v in in_dict.items():
        if v in out:
            out[v] = [out[v], k]
        else:
            out[v] = k
    return out

a = eval(input())
print(flip(a))

```

## Proof of work
<img width="277" alt="Screenshot 2024-12-04 at 6 40 11" src="https://github.com/user-attachments/assets/40aadbcc-0808-447b-9819-be8b3ca1697a">

## Part B
<img width="895" alt="Screenshot 2024-12-04 at 7 04 45" src="https://github.com/user-attachments/assets/554823fe-1d8e-4b85-b5c8-d6064f2091bc">

### For my info
Where is it on PC
>Documents/Coding/CS Lessons/Quizzes/Unit 2/quiz026
