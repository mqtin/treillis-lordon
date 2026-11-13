# *Capitalisme, désir et servitude* en treillis

L'argument de Frédéric Lordon, *Capitalisme, désir et servitude. Marx et Spinoza* (La Fabrique, 2010), reconstruit dans l'ordre géométrique et rendu explorable comme un graphe. Les prémisses que Lordon prend à Spinoza renvoient à l'*Éthique* de [SpinozaGraph](https://github.com/mqtin/SpinozaGraph) ; celles qu'il prend à Marx, ses concepts et ses thèses s'enchaînent chapitre par chapitre ; les positions qu'il réfute sont reliées aux thèses qui les réfutent.

C'est une reconstruction, pas une critique ni une reproduction : les énoncés reformulent le livre, avec leurs repères dans le livre, et les citations sont courtes. Pour lire Lordon, lisez Lordon.

**En construction.** Le projet fera partie de [treillis.qpetit.com](https://treillis.qpetit.com).

## Utilisation

Ouvrir `explorer.html` dans un navigateur : le fichier est autonome et fonctionne hors ligne.

Pour entrer dans le livre : un **parcours de lecture** en seize étapes (`PARCOURS.md`), une **figure interactive de l'angle α** (le modèle vectoriel du livre : le désir-maître, le conatus enrôlé, et la part de son effort que capte le désir-maître selon leur angle) et une vue des **régimes d'affects** (intrinsèques ou extrinsèques, tristes ou joyeux).

Pour le régénérer (Python 3 et PyYAML) :

```
python outils/check.py            # contrôles de cohérence
python outils/audit_forme.py      # audit de forme (demande source/texte/)
python outils/audit_reperes.py    # aide à l'audit de fidélité : repères douteux
python outils/build_explorer.py   # -> explorer.html
```

## Organisation

| dossier ou fichier | contenu |
|---|---|
| `parties/` | prémisses, avant-propos et chapitres : titre, sections, résumé |
| `definitions/` | concepts de Lordon (D) |
| `premisses/` | prémisses de Spinoza (S) et de Marx (M) |
| `theses/` | thèses de Lordon (T), avec démonstration ou argumentation |
| `refutees/` | positions réfutées (R) |
| `PARCOURS.md` | parcours de lecture en seize étapes |
| `INDEX.md` | table des éléments, plan, journal |
| `AGENT.md` | méthode, conventions et règles de fidélité |

---

**English.** Frédéric Lordon's *Capitalisme, désir et servitude* (2010; English translation *Willing Slaves of Capital*, Verso, 2014) reconstructed in geometrical order as an explorable graph, linked to Spinoza's *Ethics* in SpinozaGraph. Statements are paraphrases with section and paragraph references, in French; quotations are kept short.
