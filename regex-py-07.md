## 7) Exercice : Email
Dans cet exercice nous allons mettre en application ce que nous avons découvert jusqu'à présent à propos des `Expressions Régulières` et ainsi pouvoir extraire une adresse e-mail depuis un texte.

```python
str = "Please contact info@becode.org for assistance"
```

L'objectif est de récupérer **info@becode.org**.

Une adresse email simple est formée d'un ou plusieurs mots séparés éventuellement par des points ou des tirets, suivis d'un "**@**" puis du nom de domaine de l'adresse (nom + point + extension).

Cela sera la base de notre `Expression Régulière`.

```python
pattern = r"([\w\.-]+)@([\w\.-]+)(\.[\w]+)"
```

Cette `Expression Régulière` comporte 3 groupes:
- 1 - première partie de l'adresse e-mail
- 2 - le nom de domaine
- 3 - l'extension

Que pouvez-vous en dire de plus ?

Ensuite il ne reste plus qu'à rassembler le tout et tester !

**EXERCICE** : *extraire une adresse e-mail*

```python
import re

pattern = r"([\w\.-]+)@([\w\.-]+)(\.[\w]+)"

str = "Please contact info@becode.org for assistance"

match = re.search(pattern, str)
if match:
    print(match.group())
```

<br>

*Passer à l'étape suivante...*
## [8) Vers l'infini et au-delà](./regex-py-08.md)
