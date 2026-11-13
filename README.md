# *Capitalisme, désir et servitude* en treillis

L'argument de Frédéric Lordon, *Capitalisme, désir et servitude. Marx et Spinoza* (La Fabrique, 2010), reconstruit dans l'ordre géométrique et rendu explorable comme un graphe. Les prémisses que Lordon prend à Spinoza renvoient à l'*Éthique* de [SpinozaGraph](https://github.com/mqtin/SpinozaGraph) ; celles qu'il prend à Marx, ses concepts et ses thèses s'enchaînent chapitre par chapitre ; les positions qu'il réfute sont reliées aux thèses qui les réfutent.

C'est une reconstruction, pas une critique ni une reproduction : les énoncés reformulent le livre, avec leurs repères dans le livre, et les citations sont courtes. Pour lire Lordon, lisez Lordon.

**Terminé, en relecture.** Le livre est entièrement reconstruit (137 éléments vérifiés contre le texte). En ligne : <https://treillis.qpetit.com/lordon>.

## Utilisation

Ouvrir `explorer.html` dans un navigateur : le fichier est autonome et fonctionne hors ligne. Il est **trilingue** : un bouton FR / EN / DE en haut à droite (ou `?lang=en`, `?lang=de` dans l'adresse) bascule toute l'interface et tous les textes en anglais ou en allemand.

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
| `PARCOURS.md` | parcours de lecture en seize étapes (`PARCOURS.en.md` : en anglais) |
| `INDEX.md` | table des éléments, plan, journal |
| `AGENT.md` | méthode, conventions et règles de fidélité |
| `LICENSE`, `NOTICE.md`, `LICENSES/` | licences, sources et mentions de droits (`NOTICE.en.md` : en anglais) |

---

## Droits et licences

Le livre est sous droits (© Frédéric Lordon et La Fabrique, 2010) : le dépôt n'en contient pas le texte, seulement de courtes citations référencées, qui restent à leurs ayants droit. Le code est sous GPL-3.0, le travail de reconstruction sous CC BY-SA 4.0. Voir [LICENSE](LICENSE) et [NOTICE.md](NOTICE.md), à conserver dans toute redistribution.

---

**English.** Frédéric Lordon's *Capitalisme, désir et servitude* (2010; English translation *Willing Slaves of Capital*, Verso, 2014) reconstructed in geometrical order as an explorable graph, linked to Spinoza's *Ethics* in SpinozaGraph. The explorer is bilingual: use the FR / EN switch, or open <https://treillis.qpetit.com/lordon/?lang=en>. Every element, part, the reading path (`PARCOURS.en.md`) and the notice (`NOTICE.en.md`) have an English version, translated from the French reconstruction, not from the published translation. Statements are paraphrases with section and paragraph references to the French edition; quotations are kept short and remain the property of their rights holders. The book's text is not included. Code under GPL-3.0, reconstruction under CC BY-SA 4.0; see LICENSE and NOTICE.en.md.

**Deutsch.** Frédéric Lordons *Capitalisme, désir et servitude* (2010) als erkundbarer Graph in geometrischer Ordnung rekonstruiert, mit Verweisen auf Spinozas *Ethik*. Auf Französisch verfasst, mit englischer und deutscher Fassung: `explorer.html` öffnen und DE anklicken oder `?lang=de` anhängen. Nur Paraphrasen und kurze Zitate; der Text des Buches wird nicht verbreitet. Wer Lordon lesen will, lese Lordon.
