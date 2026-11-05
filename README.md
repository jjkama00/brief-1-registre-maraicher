# Registre des opérations maraîchères

> Projet individuel du SAS DFS, brief 1 (sujet : [SUJET.md](SUJET.md)). Remplacez chaque ✏️ par votre texte, puis supprimez cette ligne.

## Contexte
Une responsable d'une exploitation maraîchère pédagogique suit au jour le jour les opérations réalisées sur ses parcelles, telles que le semis, l'arrosage, le désherbage, le repiquage et la récolte. Son besoin est de conserver une trace écrite et fiable de ces gestes ainsi que de leurs coûts en FCFA, en remplaçant les notes volantes sur papier. Pour chaque intervention, elle saisit un identifiant, une date, une parcelle, une culture, le type d'opération (sélectionné dans une liste fermée) et un coût. Le programme contrôle rigoureusement la saisie et rejette les données invalides en expliquant chaque erreur avant d'enregistrer l'opération. Ensuite, l'outil lui permet d'afficher la liste des opérations, de les rechercher, de les trier par coût ou par date, et d'obtenir des synthèses détaillées des dépenses. Enfin, l'application se limite à décrire et additionner les dépenses enregistrées : elle ne fournit aucun conseil agronomique et ne mesure pas la rentabilité financière, ignorant tout des revenus et des quantités récoltées.  

## Prérequis et lancement

- Node.js 20 ou plus récent, Git ; aucune bibliothèque à installer.

```bash
git clone https://github.com/VOTRE-COMPTE/brief-1-registre-maraicher.git
cd brief-1-registre-maraicher
node app.js
npm test
```

Sous PowerShell, si `npm` est bloqué : `npm.cmd test`.

## Fonctionnalités

*Cochez seulement ce qui marche : `- [x]`.*

- [x] Données lues et enregistrées dans `donnees/operations.json`
- [x] Ajouter une opération, saisies invalides refusées sans arrêter le programme
- [x] Lister les opérations, message si le registre est vide
- [x] Rechercher par identifiant ou par parcelle ; filtrer par culture
- [x] Trier par coût ou par date
- [x] Synthèse : total, nombre et total par parcelle, coût minimum et maximum
- [x] Bonus : supprimer et modifier une opération (choix 6 et 7)
- [x] Bonus : tri par coût décroissant, parcelle la plus coûteuse

## Données
Les informations sont centralisées dans le fichier donnees/operations.json.  Le registre recense des opérations (10 opérations sur une période du 20 au 26 octobre 2026) réparties à travers trois parcelles (P1, P2, P3) et trois cultures (tomate, gombo, aubergine). Chaque opération comprend exactement six champs : id, date, parcelle, culture, operation et coutFCFA (conformément au dictionnaire des données). Les coûts sont comptabilisés en FCFA et les dates sont rédigées au format standard AAAA-MM-JJ. Ces données ont un caractère purement fictif et servent exclusivement à tester le bon fonctionnement du programme.   


## Limites
Manque de cohérence logique des saisies : Le programme effectue une vérification basique des formats (validité de la date, positivité du coût, présence de l'opération dans la liste autorisée), mais ne vérifie pas la logique métier (il accepterait par exemple une date de récolte antérieure au semis, ou une parcelle inexistante). Absence de conseils agronomiques : L'outil a un rôle strictement descriptif des actions passées et ne constitue en aucun cas un guide pour planifier les cultures (quand semer, arroser ou récolter).  Impossibilité de mesurer la rentabilité financière : Le registre trace uniquement les dépenses et ignore totalement les revenus issus des ventes. Le total des coûts ne permet donc pas de déterminer si l'exploitation gagne ou perd de l'argent.

## Documents
Dictionnaire des données - Tâches - Relevé des tests - Journal de recherche - Fiche agronomique - Fiche individuelle
## Auteur

Auteur: KAMAGATE JUNIOR

 Entraide : SOUMAHORO HAMED CHEICK TIDIANE, MARC BOTI, ABO JOSUE dans src/registre.js et app.js pour mieux comprendre la fonction verifierOperation et autre. Aussi claude IA pour relire mon code et comprendre des erreurs dans quasiment toutes les parties de mon code et plusieurs fonctions.   

