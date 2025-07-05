# Oleg Kachurin #
## Contact information ##
**Discord:** BrainsBreaker(@BrainsBreaker)
## About me ##
*Bla bla bla*
## Skills ##
- C/C++
- Python
## Code Example ##
```
import requests
import re

def find_link(A, B, k):
    res = requests.get(A)
    if res.status_code != 200:
        return False
    else:
        for serch in re.finditer(r'<a.*href=\"', res.text):
            C1 = ''
            i = serch.span()[1]
            while res.text[i] != '\"':
                C1 += res.text[i]
                i += 1
            B2 = B.replace('stepik.org', 'stepic.org')
            C2 = C1.replace('stepik.org', 'stepic.org')
            if C2 == B2 and k == 1:
                return True
            elif k<1:
                if find_link(C1, B, k+1) or find_link(C2, B, k+1):
                    return True


A = input()
B = input()
if find_link(A, B, 0):
    print('Yes')
else:
    print('No')
```
## Experience ##

## Education ##
Saint Petersburg Lyceum 30

[Stepick phyton courses №1](https://stepik.org/course/67/syllabus)

[Stepick phyton courses №2](https://stepik.org/course/512/syllabus)

## English:

**English** - A2