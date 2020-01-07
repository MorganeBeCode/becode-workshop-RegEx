## 2) Métacaractères
Les métacaractères représentent toute la puissance des `Expressions Régulières`. Ils permettent de créer facilement des modèles capables, par exemple, de trouver *"une ou plusieurs répétitions de voyelles"*

Le premier exemple met en application l'utilisation du "." (point) qui correspond à **n'importe quel caractère** autre qu'un retour à la ligne.

**EXEMPLE 1** : *métacaractère* ` . `

```python
import re

pattern = r"gr.y"

if re.match(pattern, "grey"):
  print("Match 1")

if re.search(pattern, "gray"):
  print("Match 2")

if re.search(pattern, "blue"):
  print("Match 3")
```
<br>

L'exemple suivant met en application l'utilisation des métacaractères **^** et **$** qui correspondent aux **début** et **fin** de la chaîne de caractère.

<br>

**EXEMPLE 2** : *métacaractères* ` ^ ` *et* ` $ `

```python
import re

pattern = r"^gr.y$"

if re.match(pattern, "grey"):
  print("Match 1")

if re.match(pattern, "gray"):
  print("Match 2")

if re.match(pattern, "gray sky"):
  print("Match 3")
```
<br>

*Passer à l'étape suivante...*
## [3) Classes de caractères](./regex-py-03.md)
