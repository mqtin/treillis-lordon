# AGENT.md : *Capitalisme, désir et servitude* en treillis

Ce fichier définit l'objectif, la méthode et les conventions du projet. Il s'adresse à l'agent (Claude) et à l'auteur. Tout travail dans ce dépôt doit s'y conformer. Il évolue avec le projet, et toute modification est discutée avec l'auteur.

Projets voisins : [SpinozaGraph](https://github.com/mqtin/SpinozaGraph) (l'*Éthique*, `/spinoza`) et Homo Status (`/status`, dépôt `status-and-politics`), dont ce projet reprend l'outillage et une partie des conventions.

## 1. Objectif

Reconstruire **fidèlement** l'argument de Frédéric Lordon, *Capitalisme, désir et servitude. Marx et Spinoza* (La Fabrique, 2010), dans l'ordre géométrique, et le rendre explorable comme un graphe. Depuis une thèse, on doit pouvoir voir le chemin qui y mène, jusqu'aux prémisses spinozistes et marxiennes, et ce qui en découle.

C'est une **reconstruction, non une critique**. On ne juge pas les thèses, on ne cherche pas de rivales et on ne dit pas ce qui les réfuterait : ce travail-là appartient à Homo Status (`status-and-politics/references/lordon.md`). Ici, la seule question est : *qu'est-ce que Lordon dit, et comment est-ce que cela s'enchaîne ?*

## 2. Fidélité

1. **Rien qui ne soit dans le livre.** Chaque élément reformule un passage du livre. Si un pas manque pour relier deux thèses, on le signale (§ 2.4) ; on n'ajoute pas de contenu.
2. **Toute affirmation a son repère** (champ `loc`, § 6). Dans une démonstration, chaque étape porte son repère entre parenthèses : « (08.4) ».
3. **Les renvois à Spinoza sont ceux de Lordon.** Quand Lordon cite l'*Éthique*, on note le renvoi tel quel (champ `ethique`). Quand on identifie soi-même la proposition qu'il utilise sans la citer, on l'écrit dans le corps, marqué *[renvoi reconstruit]*.
4. **Explicite ou reconstruit.** Le champ `lien_explicite` d'une thèse dit si Lordon fait lui-même les liens déclarés dans `depends_on` (`true`) ou si on les a reconstruits pour relier son argument (`false`). Dans le corps, un pas que Lordon ne fait pas est marqué *[reconstruit]*.
5. **Démonstration ou argumentation.** Une thèse a une section `## Démonstration` quand Lordon déduit, et une `## Argumentation` quand il établit par exemples, analogies ou réfutation. On ne fabrique pas de déduction absente du livre.
6. **Le vocabulaire de Lordon** est conservé (enrôlement, désir-maître, colinéarisation, épithumè…). On ne le traduit pas dans celui d'Homo Status.

## 3. Types d'éléments

| type | préfixe | dossier | rôle |
|---|---|---|---|
| `definition` | `D` | `definitions/` | un concept que Lordon définit ou forge (enrôlement, désir-maître, angle α…) |
| `spinoza` | `S` | `premisses/` | une thèse de Spinoza que Lordon prend comme prémisse ; renvoie à l'*Éthique* (`ethique`) sans en recopier le texte, qui est dans SpinozaGraph, ou, pour une autre œuvre (*Traité politique*, lettres), la cite dans `ref` (ex. « Traité politique, III, 8 ») |
| `marx` | `M` | `premisses/` | une thèse de Marx que Lordon prend comme prémisse (rapport salarial, double séparation, argent…) |
| `these` | `T` | `theses/` | une thèse de Lordon, avec sa démonstration ou son argumentation |
| `refutee` | `R` | `refutees/` | une position que Lordon réfute (servitude volontaire, consentement, intériorité…), énoncée telle qu'il la présente |

- Concepts, prémisses et positions réfutées ne s'appuient que sur des concepts et des prémisses. Seules les thèses s'appuient sur des thèses.
- Le champ `contre` d'une thèse liste les positions `R` qu'elle réfute. Ces arêtes « contre » sont distinctes des appuis : elles n'entrent ni dans le chemin ni dans les conséquences.
- Un **corollaire** se rédige dans le fichier de sa thèse et porte l'identifiant `T012-C1`. Une **scolie** (exemples, digressions, résumés) est un commentaire et n'est pas porteuse logiquement.
- Les identifiants sont globaux (`T012`, et non « chap. 1, thèse 12 »). Ils sont numérotés dans l'ordre d'apparition dans le livre et peuvent être renumérotés tant que le pilote n'est pas validé (§ 7) ; toute renumérotation est répercutée partout.

## 4. Structure du dépôt

```
AGENT.md          ce fichier
sections.yaml     titres des sections du livre, pour les repères (§ 6)
README.md
PARCOURS.md       parcours de lecture : un fil d'une quinzaine d'éléments, de la question du livre à sa conclusion
PARCOURS.en.md    sa version anglaise ; de même NOTICE.en.md (§ 5 bis) ; PARCOURS.de.md, NOTICE.de.md en allemand (§ 5 ter)
INDEX.md          table de tous les éléments, plan par chapitre, journal
parties/          P (prémisses), 0 (avant-propos), 1, 2, 3 (chapitres) : titre de Lordon, sections, résumé
definitions/      D01.md …
premisses/        S01.md …, M01.md …
theses/           T001.md …
refutees/         R01.md …
outils/           build_explorer.py, explorer_template.html, check.py, extract_epub.py
source/           NON VERSIONNÉ : le fichier du livre et le texte extrait (§ 6)
explorer.html     généré
```

Chaque élément porte un champ `partie` : `P` pour les prémisses S et M, sinon le chapitre où il apparaît (`0` pour l'avant-propos). `INDEX.md` est mis à jour à chaque ajout, modification ou retrait.

## 5. Format d'un fichier

```markdown
---
id: T012
type: these                 # definition | spinoza | marx | these | refutee
partie: "1"                 # P | 0 | 1 | 2 | 3
titre: Titre court
enonce: >
  Reformulation de la thèse, en une ou deux phrases.
loc: ["08.2", "08.4"]        # repères section.paragraphe (§ 6)
citation: "« … »"           # facultative ; une ou deux phrases au plus (§ 6)
depends_on: [D03, S02, T009]
contre: [R02]               # thèses seulement
ethique: [3p6, 3p9sc]       # identifiants de SpinozaGraph (obligatoire pour S)
lien_explicite: true        # thèses seulement (§ 2.4)
statut_revision: brouillon  # brouillon | verifie-texte
---

## Énoncé
…

## Démonstration            (ou ## Argumentation)
1. Par S02, … (08.3).
2. Par D03 et T009, … (08.4). ∎

## Scolie
Exemples et digressions du livre, résumés.
```

**§ 5 bis. Version anglaise.** Chaque élément et chaque partie a sa version anglaise dans le même fichier : `titre_en`, `enonce_en` (ou `resume_en`) dans le front-matter, et, après une ligne `<!-- en -->`, le corps anglais, avec les sections `## Demonstration` (ou `## Argument`), `## Scholium`, `## In Lordon`, `## As Lordon presents it`. Le corps anglais garde les mêmes étapes, les mêmes identifiants et les mêmes repères que le français, ce que `check.py` vérifie. Il traduit la reconstruction, jamais la traduction anglaise publiée (Verso, 2014) ; les mots de Lordon y sont rendus brièvement entre guillemets anglais, et le champ `citation` reste en français. Un document `NOM.md` a sa version dans `NOM.en.md`. Toute correction du français se reporte dans l'anglais.

**§ 5 ter. Version allemande.** Sur le même modèle, chaque élément et chaque partie a sa version allemande : `titre_de`, `enonce_de` (ou `resume_de`), et, après une ligne `<!-- de -->` placée après le corps anglais, le corps allemand, avec les sections `## Beweis` (ou `## Argumentation`), `## Anmerkung`, `## Bei Lordon`, `## Wie Lordon sie darstellt`. Il garde les mêmes étapes, les mêmes identifiants et les mêmes repères, ce que `check.py` vérifie. Il traduit la reconstruction, sans recourir à une traduction publiée du livre ; les mots de Lordon y sont rendus brièvement par nous entre guillemets allemands („…“). Un document `NOM.md` a sa version dans `NOM.de.md`. Toute correction du français se reporte dans l'anglais et dans l'allemand.

`depends_on` correspond exactement aux identifiants invoqués dans la démonstration ou l'argumentation. Les identifiants de l'*Éthique* suivent SpinozaGraph : `1def3`, `1ax4`, `3p6`, `3p9sc`, `3p13csc`, `3ad1` (définitions des affects), `3agd` (définition générale des affects), `4pr` (préface), `4appc28` (appendice de la partie IV, chapitre 28). Une démonstration est citée par sa proposition (`3p37` pour « III, 37, démonstration »).

## 6. Droits et texte source

Le livre est sous droits.

- Le fichier du livre et le texte extrait vivent dans `source/`, **exclu de Git** (`.gitignore`). On ne les publie jamais, ni en tout ni en partie. `outils/check.py` signale une erreur si un fichier de `source/` est suivi par Git ou si une citation du corps dépasse 300 caractères.
- Les citations ne sont pas couvertes par les licences du dépôt (CC BY-SA 4.0 pour la reconstruction, GPL-3.0 pour le code) : voir `LICENSE` et `NOTICE.md`, à tenir à jour.
- Les éléments **reformulent**. Une citation (champ `citation` ou dans le corps) tient en une ou deux phrases, au plus 300 caractères, entre guillemets, avec son repère, et seulement quand la formule compte (une formule célèbre, un concept). C'est l'usage du droit de citation : courte, justifiée par l'analyse, sourcée.
- **Repères.** Le fichier de travail est un EPUB sans pagination. Un passage est donc repéré par **section et paragraphe** : `08.4` est le 4e paragraphe de la section 08, « La servitude volontaire n'existe pas ». Les sections sont celles de la table des matières de Lordon (`sections.yaml`, qui ne contient que les titres) ; les paragraphes sont numérotés par `outils/extract_epub.py`, qui produit `source/texte/` à partir de l'EPUB. Un lecteur de l'édition papier retrouve le passage par le titre de section. Si l'auteur fournit plus tard la pagination papier, on l'ajoutera à côté.

## 7. Méthode de travail

1. **Pilote** : l'avant-propos et le chapitre 1. L'auteur valide le découpage et le format avant qu'on poursuive.
2. **Un chapitre à la fois** : lecture → éléments → `INDEX.md` → `python outils/check.py` → `python outils/build_explorer.py` → relecture par l'auteur → commit.
3. **Audit de fidélité** : chaque élément est relu contre le passage cité (reformulation exacte, repère juste, liens explicites ou reconstruits bien marqués), puis passe à `verifie-texte`.

   **Ce que `verifie-texte` garantit** : l'énoncé a été relu contre les passages cités et ne dit ni plus ni moins que Lordon (ou, pour une prémisse S, que Spinoza) ; tout passage entre guillemets est dans le livre mot pour mot ; repères et notes existent et sont à leur place (`audit_forme.py`) ; aucune étape ne renvoie à un passage manifestement moins pertinent qu'un autre (`audit_reperes.py`). Le corps des thèses, des concepts et des positions réfutées a en outre été relu phrase à phrase contre le texte par l'agent (13 novembre 2026) ; celui des prémisses S et M l'a été lors de leur rédaction et par les contrôles. **Relecture par l'auteur** : faite et terminée le 14 novembre 2026 ; toute correction ultérieure est consignée dans le journal d'`INDEX.md`.
4. Les commits et les push se font seulement à la demande de l'auteur.

## 8. Contrôles

`python outils/check.py` vérifie : identifiants et types, repères présents et bien formés, longueur des citations, existence des dépendances, absence de cycle, concordance entre `depends_on` et la démonstration, arêtes `contre` vers des `R`, renvois à l'*Éthique* existants dans SpinozaGraph (si le dépôt est à côté), cohérence avec `INDEX.md`, exclusion de `source/`, complétude et concordance des versions anglaise et allemande (§ 5 bis et 5 ter). L'onglet « Audit » de l'explorateur affiche les mêmes contrôles.

`python outils/audit_forme.py` fait l'audit de forme, sans juger l'argument : ponctuation et guillemets, structure des fichiers (sections attendues, étapes numérotées, chacune avec son repère, ∎ final), accord entre les repères du corps et le champ `loc`, existence des paragraphes cités, présence des notes citées dans les sections citées, et présence mot pour mot dans le livre de tout passage entre guillemets. Les contrôles qui lisent le livre demandent `source/texte/`.

Aucun de ces contrôles ne remplace l'audit de fidélité.

## 9. Style

Le style est celui des projets voisins : phrases courtes, vocabulaire précis, pas de jargon ajouté. Le texte est écrit en français, et un résumé en anglais n'est donné que dans le README.
