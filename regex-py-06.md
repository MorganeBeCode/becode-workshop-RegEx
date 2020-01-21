## 6) Séquences spéciales
Bien qu'il en existe de plusieurs sortes, toutes les séquences spéciales débutent par un **\** suivies d'un autre caractère.

Le premier exemple met en application une séquence spéciale qui, suivie d'un nombre entre 1 et 99, indique **le nombre de fois que l'élément doit apparaître**.

**EXEMPLE 1** : *séquence spéciale à répétition*

```python
import re

pattern = r"(.+) \1"

if re.match(pattern, "word word"):
  print("Match 1")

if re.match(pattern, "?! ?!"):
  print("Match 2")

if re.match(pattern, "abc cba"):
  print("Match 3")
```
<br>

Les séquences spéciales **\d**, **\s** et **\w** correspondent respectivement aux **chiffres** (digits), **espaces blancs** (spaces) et aux **mots** (word characters).

En mode ASCII, ce serait équivalent à **[0-9]**, **[\t\n\r\f\v]** et **[a-ZA-Z0-9_]**

En mode Unicode, ça suit le même principe de base avec plus de précisions. Par exemple **\w** englobe également les caractères accentués.

La valeur d'une séquence spéciale s'inverse lorsque le caractère qui suit **\** est une lettre majuscule. Si **\d** équivaut à **n'importe quel chiffre** alors **\D** vaudra **tout sauf un chiffre**.

<br>

**EXEMPLE 2** : *séquences spéciales alphanumériques*

```python
import re

pattern = r"(\D+\d)"

match = re.match(pattern, "Hi 999!")
if match:
  print("Match 1")

match = re.match(pattern, "1, 23, 456!")
if match:
    print("Match 2")

match = re.match(pattern, " ! $?")
if match:
    print("Match 3")
```
<br>

On va maintenant compliquer un peu plus les choses avec les séquences spéciales **\A**, **\Z** et **\b**. Les séquences **\A** et **\Z** annoncent respectivement le **début** et la **fin** d'une chaîne de caractères.

Quand à la séquence **\b**, elle correspond à la frontière entre des caractères **\w** et **\W** (espace entre des mots) mais également à la frontière entre un caractère **\w** et le début ou la fin de la chaîne de caractères (début ou fin d'une phrase).

<br>

**EXEMPLE 3** : *séquence spéciale aux frontières du réel*

```python
import re

pattern = r"\b(cat)\b"

match = re.search(pattern, "The cat sat!")
if match:
  print("Match 1")

match = re.search(pattern, "We s>cat<tered?")
if match:
    print("Match 2")

match = re.search(pattern, "We scattered.")
  if match:
      print("Match 3")
```
<br>

Et pour terminer, la séquence spéciale **\B** correspond à une absence de frontière.

Le dernier exemple illustre très bien la différence entre **\b** et **\B**.

<br>

**EXEMPLE 4** : *séquence spéciale Space Jam*

```python
import re

pattern = r".+\b-\b.+"

match = re.match(pattern, "grille-pain")
if match:
  print("Match 1")

match = re.match(pattern, "hauteur - largeur")
if match:
    print("Match 2")

pattern = r".+\B-\B.+"

match = re.match(pattern, "grille-pain")
if match:
  print("Match 3")

match = re.match(pattern, "hauteur - largeur")
if match:
    print("Match 4")
```
<br>

*Passer à l'étape suivante...*
## [7) Exercice : Email ](./regex-py-07.md)
