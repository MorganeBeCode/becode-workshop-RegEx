## 3) Classes de caractères
Les classes de caractères permettent de créer des modèles définis par un **ensemble de caractères** délimité par des "**[]**".

Un tiret "**-**" représente une intervalle à l'intérieur de la classe. Il s'agit d'un métacaractère s'il est placé dans cette position. Pour permettre sa lecture en tant que caractère "tiret" il convient de le placer en début de la classe comme ceci "**[-....]**"

Le premier exemple met en application une classe de caractères qui permet de vérifier si **au moins un des caractères** est présent.

**EXEMPLE 1** : *classe de caractères*

```python
import re

pattern = r"[aeiouy]"

if re.search(pattern, "this"):
  print("Match 1")

if re.search(pattern, "is"):
  print("Match 2")

if re.search(pattern, "SPARTAAAAAAA"):
  print("Match 3")
```
<br>

L'exemple suivant met en application une classe de caractères constituée de plusieurs **ensembles de caractères** afin de vérifier si **au moins deux lettres majuscules et un chiffre** se suivent.

<br>

**EXEMPLE 2** : *ensembles de caractère*

```python
import re

pattern = r"[A-Z][A-Z][0-9]"

if re.match(pattern, "LS8"):
  print("Match 1")

if re.match(pattern, "Ec3"):
  print("Match 2")

if re.match(pattern, "10AB3"):
  print("Match 3")
```
<br>

*Passer à l'étape suivante...*
## [3) Classes de caractères](./regex-py-03.md)
