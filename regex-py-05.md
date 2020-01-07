## 5) Groupes
Les groupes sont délimités par des **( )** ce qui permet, par exemple, d'isoler une partie précise d'une `Expression Régulière` et de lui appliquer un métacaractère.

Vous l'avez sûrement déjà remarqué dans le premier exemple à l'étape précédente...

```python
pattern = r"egg(spam)*"
```

L'exemple suivant met en application "**|**" qui signifie **soit ce qui précède OU soit ce qui suit** le métacaractère "|".

**EXEMPLE 1** : *métacaractère ` | `*

```python
import re

pattern = r"gr(a|o)s"

if re.match(pattern, "gras"):
  print("Match 1")

if re.match(pattern, "gros"):
  print("Match 2")

if re.match(pattern, "gris"):
  print("Match 3")
```
<br>

L'avantage des groupes dans les `Expressions Régulières` c'est que l'on peut en définir plusieurs et accéder aux résultats correspondant à leur position.

En Python, la fonction **group(n)** peut recevoir en paramètre la position du groupe que l'on souhaite atteindre (aucune valeur ou la valeur 0 retourneront tous les groupes qui correspondent à l'`Expression Régulière`)

<br>

**EXEMPLE 2** : *group(n)*

```python
import re

pattern = r"a(bc)(de)(f(g)h)i"

match = re.match(pattern, "abcdefghijklmnop")
if match:
  print(match.group())
  print(match.group(0))
  print(match.group(1))
  print(match.group(2))
```
<br>

L'exemple suivant met en application les groupes nominatifs **(?P<name>...)** qui deviennent donc accessible par leurs labels respectifs et les groupes non-capturables **(?:...)** qui peuvent être ajouté à n'importe quel moment et n'importe quelle position sans casser l'ordre actuel des autres groupes.

<br>

**EXEMPLE 3** : *groupes nominatifs et non-capturables*

```python
import re

pattern = r"(?P<first>abc)(?:def)(ghi)"

match = re.match(pattern, "abcdefghi")
if match:
  print(match.group("first"))
  print(match.group(0))
  print(match.group(1))
  print(match.group(2))
```
<br>

*Passer à l'étape suivante...*
## [6) Séquences spéciales](./regex-py-06.md)
