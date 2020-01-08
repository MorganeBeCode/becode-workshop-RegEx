## 8) Vers l'infini et au-delà
Dans l'exercice précédent nous avions un texte avec une adresse e-mail connue que nous voulions extraire. Mais lorsque vous voulez valider ou vérifier des adresses e-mail inconnue, ne vous cassez pas la tête à vouloir utiliser une `Expression Régulière` car vous risqueriez de sérieusement vous prendre la tête pour rien.

En effet, l'exemple ci-dessous peut convenir à 99,9% de la syntaxe autorisée pour une adresse e-mail et vous pouvez tout de même être sûr de tôt ou tard tomber sur la personne qui fait parti des 0,1%

```
(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])
```

Franchement, pour valider un e-mail lors d'une inscription sur un site web ou vérifier l'envoi d'un message par formulaire, il suffit juste d'envoyer un e-mail de confirmation en retour à l'utilisateur.

C'est bien plus simple et au moins, vous êtes sûr que l'utilisateur va faire attention à vérifier lui-même que son adresse e-mail soit correcte s'il souhaite valider son inscription ou obtenir une réponse à son message !

Tout ça pour vous dire que les `Expressions Régulières` sont comparables à une boîte à outils. Connaître chaque outil et savoir s'en servir c'est très bien mais savoir à quel moment s'en servir c'est encore mieux.

En plus des ressources citées dans le README, vous pouvez continuer à découvrir, manipuler et tester des `Expressions Régulières` sur :

- [RegEx Testing](https://www.regextester.com/)
- [regexr](https://regexr.com/)
- [regular expressions 101](https://regex101.com/)
