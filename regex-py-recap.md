# RegEx syntaxe

## Récapitulatif pour Python

### Lib/re.py

#### Métacaractères

- \ : permet de transformer un métacaractère en caractère simple
- . (dot) : n'importe quel caractère excepté 'nouvelle ligne' (\n)
- \d : caractère numérique [0-9]
- \D : caractère non-numérique [^0-9]
- \w : caractère alphanumérique [a-zA-Z0-9]
- \W : caractère non-alphanumérique [^a-zA-Z0-9]

#### Quantifieurs
- \* : correspondre 0 ou plusieurs fois (greedy)
- *? : comme \* et le moins de fois possible
- + : correspondre 1 ou plusieurs fois (greedy)
- +? : comme + et le moins de fois possible
- ? : correspondre 0 ou 1 fois (greedy)
- ?? : comme ? et le moins de fois possible
- {m} : correspondre exactement m fois
- {m,n} : correspondre minimum m fois et maximum n fois (greedy)
- {m, n}? : comme {m,n} et le moins de fois possible

#### Classes / Ensembles de caractères
- [...] : n'importe quel caractère qui se trouve dans l'ensemble
- [^...] : aucun caractère qui se trouve dans l'ensemble

#### Groupes de caractères
- (...) : correspondre exactement au groupe de caractères
- (..|.) : comme (...) ou juste à ce qui se trouve avant |
- \numéro :

#### Ancres et espaces-vides
- ^ (caret) : indique le début d'une chaîne ou ligne (similaire à \A)
- $ : indique la fin d'une chaîne ou ligne (similaire à \Z)
- \b : frontière d'un mot
- \B : n'est pas une frontière d'un mot
- \s : espace-blanc
- \S : n'est pas un espace-blanc
