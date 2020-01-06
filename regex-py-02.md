## 2) Métacaractères
En plus de la fonction **re.match**, il existe **re.search** et **re.findall**

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
## [3) Métacaractères](./regex-py-03.md)
