# Trame de rapport d'audit — Infrastructure & Sécurité d'eRezo

> **Modèle à remplir par votre société de conseil.** Remplacez chaque bloc _en italique_ par votre analyse.
> Le rapport final est rendu en PDF le **vendredi 17 juillet 2026**, à partir du travail réalisé **en séance**. Soyez concis et factuel : un bon rapport tient en 5 à 8 pages.

---

## Page de garde

- **Rapport d'audit :** Infrastructure & Sécurité — eRezo
- **Réalisé par (votre société de conseil) :** _nom de votre société_
- **Consultant(s) :** _vous, seul ou avec votre associé_
- **Client :** KodeSaaS — Maxime Nicole (propriétaire d'eRezo)
- **Date de l'audit :** _date_
- **Périmètre :** production https://erezo.fr (lecture seule) — infrastructure & sécurité, hors code source
- **Autorisation de test signée :** _oui / n° annexe_

---

## 1. Résumé exécutif

_En 5-8 lignes, pour votre client :_
- _État général côté infrastructure et sécurité (sain / à surveiller / à risque)_
- _Les 2-3 points les plus importants_
- _Votre recommandation principale pour la V2_

**Score de risque global (sécurité) :** _X / 10_

| Sévérité | Nombre de failles |
|---|---|
| Critique (P0) | _n_ |
| Haute (P1) | _n_ |
| Moyenne / Basse (P2) | _n_ |

---

## 2. Audit de l'infrastructure

_Tout ce que vous avez pu observer de l'extérieur. Pour chaque point : ce que vous constatez, et pourquoi c'est un problème (ou pas)._

**Hébergement :**
_Où et comment l'application semble hébergée (serveur, hébergeur, CDN…), et comment vous l'avez identifié (DNS, en-têtes…). Écrivez « non confirmé » si vous n'êtes pas sûr._

**HTTPS / certificat :**
_Le site est-il en HTTPS ? Le certificat est-il valide et correctement configuré ?_

**En-têtes HTTP & configuration :**
_En-têtes de sécurité présents ou absents, messages d'erreur trop bavards, pages ou fichiers exposés qui ne devraient pas l'être, robots.txt, etc._

**Traces de « fait vite » :**
_Environnement de dev visible en prod, informations techniques qui fuient, incohérences…_

**Verdict infrastructure :** _points forts / points faibles / recommandations._

---

## 3. Audit de sécurité (pentest — OWASP)

> Rappel : **lecture seule, non destructif.** Aucune donnée personnelle réelle ne doit apparaître dans ce rapport (anonymisez).

**Méthodologie :** _outils / agents IA utilisés, phases (reconnaissance → tests → vérification)._

### Findings

Pour **chaque faille** trouvée, remplissez :

#### [FIND-00X] _Titre_
- **Sévérité :** _Critique / Haute / Moyenne / Basse_ · **Priorité :** _P0 / P1 / P2_
- **Zone concernée :** _page, endpoint, fonctionnalité…_
- **Description :** _en quoi consiste la faille._
- **Preuve :** _comportement observé, capture anonymisée._
- **Impact :** _ce que ça permet à un attaquant._
- **Correction recommandée :** _..._

_(Dupliquez ce bloc pour chaque finding.)_

### Points positifs (ce qui est bien sécurisé)
_Listez ce qui résiste. Un bon auditeur note aussi ce qui va bien._

### Plan de remédiation priorisé

| Priorité | Faille | Effort estimé | Impact |
|---|---|---|---|
| P0 | _..._ | _faible/moyen/élevé_ | _..._ |
| P1 | _..._ | _..._ | _..._ |
| P2 | _..._ | _..._ | _..._ |

---

## 4. Recommandations pour la V2

_Comment reconstruire eRezo, bien hébergé et sécurisé. Pour chaque thème : la bonne pratique et ce que vous recommandez concrètement au client. Vous n'êtes pas obligés d'employer le vocabulaire technique exact._

**Une infrastructure propre et fiable :**
_Hébergement, HTTPS partout, séparation dev / production, sauvegardes._

**Une application sécurisée :**
_Les règles pour éviter précisément les failles trouvées (contrôle des accès, en-têtes de sécurité, configuration, données exposées)._

**Une mise en ligne maîtrisée :**
_Un déploiement propre, ce qui se passe entre « ça marche sur mon poste » et « c'est en production »._

**Le respect des données des utilisateurs :**
_Les règles de base sur les données personnelles._

**Un socle fait pour durer _(pour aller plus loin)_ :**
_Ce qui rend le projet solide et reprenable (organisation, tests, documentation)._

---

## 5. Synthèse des recommandations

_Top 5 des actions à conseiller au client, dans l'ordre où vous lui conseillez de les traiter._

1. _..._
2. _..._
3. _..._
4. _..._
5. _..._

---

## Annexe — Audit croisé

_Commentaires reçus d'une autre société (autre groupe) sur votre rapport (séance 5) et comment vous les intégrez._
