# Trame de rapport d'audit — eRezo

> **Modèle à remplir par votre groupe.** Remplacez chaque bloc _en italique_ par votre analyse.
> Le rapport final est rendu en PDF à **J+7**. Soyez concis et factuel : un bon audit tient en 6 à 10 pages.

---

## Page de garde

- **Projet audité :** eRezo — SaaS de gestion de contacts et d'événements
- **Équipe (groupe) :** _noms des membres_
- **Date de l'audit :** _date_
- **Périmètre :** code source (lecture) + production https://erezo.fr (lecture seule)
- **Autorisation de test signée :** _oui / n° annexe_

---

## 1. Résumé exécutif

_En 5-8 lignes, pour un lecteur non technique (le client) :_
- _État général de l'application (sain / à surveiller / à risque)_
- _Les 2-3 points les plus importants_
- _Verdict de reprenabilité (reprenable en < 30 min ? oui/non/sous conditions)_

**Score de risque global (sécurité) :** _X / 10_

| Sévérité | Nombre de failles |
|---|---|
| Critique | _n_ |
| Haute | _n_ |
| Moyenne | _n_ |
| Basse / Info | _n_ |

---

## 2. Architecture & conception

**Domaines métier identifiés (bounded contexts) :**
_Listez les grands domaines (ex : gestion de contacts, événements, messagerie, comptes…) et dites s'ils sont bien délimités._

**Style d'architecture observé :**
_Monolithe ? Modulaire ? Trace d'architecture hexagonale (séparation domaine / infrastructure, ports & adapters) ? Justifiez avec des exemples de dossiers/fichiers._

**Ubiquitous language :**
_Le code emploie-t-il les termes du métier ? Exemples._

**Points de couplage / dette technique :**
_Où est-ce rigide ? Qu'est-ce qui serait risqué à faire évoluer ?_

**Verdict architecture :** _/ points forts / points faibles / recommandations_

---

## 3. Tests & qualité

**Tests présents :**
_Types (unitaires / intégration / E2E), où ils se trouvent, ce qu'ils couvrent._

**Pyramide des tests :**
_Respectée ? Inversée ? Absente ?_

**Traces de TDD :**
_Voit-on des tests écrits avant le code ? Le cœur métier est-il testé ?_

**Outillage qualité :**
_CI, linters, conventions, hooks…_

**Verdict tests :** _/ recommandations_

---

## 4. Stack technique

_Décrivez la stack que vous avez identifiée :_

| Couche | Technologie identifiée | Comment vous l'avez découverte |
|---|---|---|
| Langage / runtime | _ex : ..._ | _headers HTTP, code, ..._ |
| Framework backend | _..._ | _..._ |
| Base de données | _..._ | _..._ |
| Frontend / templating | _..._ | _..._ |
| Hébergement / infra / CDN | _..._ | _..._ |
| Services externes | _..._ | _..._ |

**Analyse des choix :** _cohérents avec un SaaS de ce type ? Ce que vous feriez autrement._

---

## 5. Audit de sécurité (pentest IA — OWASP Top 10)

> Rappel : **lecture seule, non destructif.** Aucune donnée personnelle réelle ne doit apparaître dans ce rapport (anonymisez).

**Méthodologie :** _outils / agents IA utilisés, phases (reco → tests → vérification)._

### Findings

Pour **chaque faille** trouvée, remplissez :

#### [FIND-00X] _Titre_
- **Sévérité :** _Critique / Haute / Moyenne / Basse_ · **Priorité :** _P0 / P1 / P2_
- **Endpoint / zone concernée :** _..._
- **Description :** _..._
- **Preuve :** _requête, capture anonymisée, comportement observé_
- **Impact :** _ce que ça permet à un attaquant_
- **Correction recommandée :** _..._

_(Dupliquez ce bloc pour chaque finding.)_

### Points positifs (ce qui est bien sécurisé)
_Listez ce qui résiste (ex : CSRF, cookies, échappement XSS…). Un bon auditeur note aussi ce qui va bien._

### Plan de remédiation priorisé

| Priorité | Finding | Effort estimé | Impact |
|---|---|---|---|
| P0 | _..._ | _faible/moyen/élevé_ | _..._ |
| P1 | _..._ | _..._ | _..._ |
| P2 | _..._ | _..._ | _..._ |

---

## 6. Reprenabilité (« test du freelance »)

- **Documentation présente :** _CLAUDE.md ? README ? doc d'onboarding ?_
- **Temps estimé pour comprendre + lancer le projet :** _< 30 min ? plus ?_
- **Ce qui manque pour rendre le projet reprenable :** _..._
- **Verdict :** _reprenable / partiellement / non — argumenté_

---

## 7. Synthèse des recommandations

_Top 5 des actions prioritaires, tous axes confondus, dans l'ordre où vous conseillez au client de les traiter._

1. _..._
2. _..._
3. _..._
4. _..._
5. _..._

---

## Annexe — Audit croisé

_Commentaires reçus d'un autre groupe sur votre rapport (séance 5) et comment vous les intégrez._
