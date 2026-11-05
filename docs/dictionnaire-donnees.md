# Dictionnaire des données

> Un champ par ligne, d'après `SUJET.md` et le fichier de `donnees/`. La première ligne sert de modèle.

| Champ | Signification | Type | Règle de validation | Unité | Exemple |
| --- | --- | --- | --- | --- | --- |
| `id` | Identifiant unique | texte | non vide, absent des données | — | S01 |
|`date`  | Date de l'operation | texte|  existente au format AAAA-MM-JJ |—| 2026-12-03|
|`parcelle` | Parcelle de l'operation  |texte |non vide |—|P1|
|`culture`|culture concernée |texte |non vide |—|tomate|
|`operation`|type d'opération |texte | appartient à la liste fermée ci-dessous |—|arrosage|
|`coutFCFA` | cout de l'opération |texte | nombre nul ou positif |—|2000|
**Listes de valeurs autorisées** : 
istes de valeurs autorisées : OPERATIONS = ['semis', 'arrosage', 'désherbage', 'repiquage', 'récolte']
**Sources** : `SUJET.md` et `donnees/operations.json`
