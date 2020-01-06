## 1) Les trois petites fonctions
En plus de la fonction **re.match**, il existe **re.search** et **re.findall**

Selon vous, que retourneront ces fonctions ?

```python
import re

pattern = r"spam"

if re.match(pattern, "eggspamsausagespam"):
  print("Match")
else:
  print("No match")

if re.search(pattern, "eggspamsausagespam"):
  print("Match")
else:
  print("No match")

print(re.findall(pattern, "eggspamsausagespam"))
```
