## 1) Les trois petites fonctions
En Python, en plus de la fonction **re.match**, il existe les fonctions **re.search** et **re.findall**

Selon vous, que retourneront ces fonctions lors de l'exécution du code ci-dessous ?

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
<br>

*Passer à l'étape suivante...*
## [2) Métacaractères](./regex-py-02.md)
