## 4) Encore plus de métacaractères
Les métacaractères **\*, +, ?, { }** permettent de spécifier le nombre de répétitions de l'élément qui précède.

Le premier exemple met en application **\*** qui signifie **zéro ou plusieurs répétitions** de l'élément qui précède.

**EXEMPLE 1** : *métacaractère \**

```python
import re

pattern = r"egg(spam)*"

if re.match(pattern, "egg"):
  print("Match 1")

if re.match(pattern, "eggspamspamspamegg"):
  print("Match 2")

if re.match(pattern, "spam"):
  print("Match 3")
```
<br>

L'exemple suivant met en application **+** qui signifie **une ou plusieurs répétitions** de l'élément qui précède.

<br>

**EXEMPLE 2** : *métacaractère +*

```python
import re

pattern = r"g+"

if re.match(pattern, "g"):
  print("Match 1")

if re.match(pattern, "ggggggggggggg"):
  print("Match 2")

if re.match(pattern, "abc"):
  print("Match 3")
```
<br>

L'exemple suivant met en application **?** qui signifie **zéro ou une répétition** de l'élément qui précède.

<br>

**EXEMPLE 3** : *métacaractère ?*

```python
import re

pattern = r"ice(-)?cream"

if re.match(pattern, "ice-cream"):
  print("Match 1")

if re.match(pattern, "icecream"):
  print("Match 2")

if re.match(pattern, "lasagne"):
  print("Match 3")

if re.match(pattern, "ice--ice"):
  print("Match 4")
```
<br>

Le dernier exemple met en application **{x,y}** qui permet de définir une **intervalle de répétitions comprise entre x et y** de l'élément qui précède.

Du coup, **{0,1}** est similaire à **?**.

Si la première ou la seconde valeur n'est pas spécifiée, elle vaudra 0 par défaut.

<br>

**EXEMPLE 4** : *métacaractère { }*

```python
import re

pattern = r"9{1,3}"

if re.match(pattern, "9"):
  print("Match 1")

if re.match(pattern, "999"):
  print("Match 2")

if re.match(pattern, "9999"):
  print("Match 3")
```
<br>

*Passer à l'étape suivante...*
## [5) Groupes](./regex-py-05.md)
