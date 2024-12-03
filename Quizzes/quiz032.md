# Quiz032

## Code
```.py
def mystery(a:list, b:list)->list:
    out = []
    for i in a:
        for k in b:
            if i==k:
                out.append(i)
    return out

print(mystery(a=[2,5,3, "hello"],b=[4,1,2,6,2, "hello"]))
```

## Proof of work
<img width="144" alt="Screenshot 2024-12-04 at 8 07 23" src="https://github.com/user-attachments/assets/ec5f2fb0-fcc3-485c-844e-628b1bcaf310">
