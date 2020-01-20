# BeCode - Workshop
- Thème : Regular Expression (RegEx)
- Objectif : découvrir et apprendre à utiliser les `Expressions Régulières`
- Sources principales : [Sololearn](https://www.sololearn.com/), [Expreg.com](http://www.expreg.com), [Regular-Expressions.info](https://www.regular-expressions.info)
- Infos complémentaires : [Expression régulière](https://fr.wikipedia.org/wiki/Expression_r%C3%A9guli%C3%A8re), [Hiérarchie de Chomsky](https://fr.wikipedia.org/wiki/Hi%C3%A9rarchie_de_Chomsky), [Langage naturel](https://fr.wikipedia.org/wiki/Langage_naturel), [Langage formel](https://fr.wikipedia.org/wiki/Langage_formel)
- Doc Python 3 : [module 're'](https://docs.python.org/3/library/re.html)

## Pourquoi les RegEx ?
Comme l'empereur romain Marcus Aurelius disait :

> Dura RegEx Sed RegEx

Traduction :

> Les RegEx sont dures, mais ce sont des RegEx

Ce qui signifie :

> Les expressions régulières sont dures à aborder, mais ce sont des expressions régulières (et PAF dans ta face !)

![mème de Gladiator avec Maximus hurlant à la foule : are you not entertained](https://i.kym-cdn.com/photos/images/original/000/615/056/23c.gif)

Si vous n'avez rien compris à cette signification, c'est normal, c'était le but (de ma blague pourrie)! Par contre, plus sérieusement, vous serez normalement amené à rencontrer et utiliser des RegEx (peu importe le langage de programmation) et il est, selon moi, utile de savoir comment et quand bien les utiliser.

## Qu'est-ce qu'une RegEx ?

Une `Expression Régulière` est une séquence de caractères qui décrit, selon une syntaxe précise, un ensemble de chaînes de caractères possibles. En gros, c'est un filtre qui peut être utilisé pour rechercher/valider/modifier des chaînes de caractères.

## Exemples d'utilisation

- Remplacer par des '**X**' tous les numéros de téléphone d'une liste clients pour en garder la confidentialité lors d'une publication **0123/456 78 90 > 01XX/XXX XX XX**
- Vérifier le contenu de certains champs de formulaire avant envoi (**email, numéro de téléphone, adresse IP**...)

## Et maintenant ?
Il est temps de se lancer et découvrir les différents éléments qui constituent la syntaxe des `Expressions Régulières`. Afin de pouvoir s'exercer de manière interactive et le plus simplement possible, j'ai décidé de vous faire coder en Python utiliser le [Code Playground](https://code.sololearn.com/#py) de Sololearn
<br><br>
Les `Expressions Régulières` en Python sont disponibles via le module **re** qui fait parti de la bibliothèque standard.
<br><br>
Après avoir défini une `Expression Régulière`, il suffit d'utiliser la fonction **re.match**
<br><br>
Cette fonction retournera un object qui correspond au modèle de l'expression sinon elle retournera `None`
<br><br>
**EXEMPLE** : *valeur littérale (=exacte)*
```python
import re

pattern = r"spam"

if re.match(pattern, "spamspamspam"):
  print("Match")
else:
  print("No Match")
```
> SOLOLEARN : [Code Playground](https://code.sololearn.com/#py)

<br><br>
## Liste des étapes
### [1) Trois petites fonctions](regex-py-01.md)
### [2) Métacaractères](regex-py-02.md)
### [3) Classes de caractères](regex-py-03.md)
### [4) Encore plus de métacaractères](regex-py-04.md)
### [5) Groupes](regex-py-05.md)
### [6) Séquences spéciales](regex-py-06.md)
### [7) Exercice : Email](regex-py-07.md)
### [8) Vers l'infini et au-delà](regex-py-08.md)
### [Récapitulatif](regex-py-recap.md)
