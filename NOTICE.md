# Sources, droits et mentions

Ce projet reconstruit l'argument d'un livre sous droits. Il n'en reproduit pas le texte : il le **reformule**, en renvoyant à chaque passage, et n'en **cite** que de courts extraits. **Pour lire Lordon, lisez Lordon.**

## Le livre

- Frédéric Lordon, *Capitalisme, désir et servitude. Marx et Spinoza*, Paris, La Fabrique, 2010. © Frédéric Lordon et La Fabrique éditions.
- Traduction anglaise : *Willing Slaves of Capital. Spinoza and Marx on Desire*, trad. Gabriel Ash, Londres, Verso, 2014.
- Ce que le dépôt contient du livre : de courtes citations (433 passages, presque tous de quelques mots ; au plus 29 mots consécutifs pour Lordon), chacune avec son repère (section et paragraphe), et les titres de ses sections, utilisés comme repères. Le texte lui-même n'est pas distribué : le dossier `source/` est exclu du dépôt, et `outils/check.py` vérifie qu'il le reste.
- Ces citations relèvent du droit de courte citation (Code de la propriété intellectuelle, art. L122-5, 3°) : elles sont incorporées à un travail d'analyse et leur source est indiquée. Elles ne sont **pas** couvertes par les licences du dépôt (voir `LICENSE`).

## Les versions anglaise et allemande

- Les versions anglaise et allemande traduisent la reconstruction (titres, énoncés, démonstrations, commentaires). Elles sont faites sur la reconstruction française, non sur une traduction publiée du livre (en anglais, celle de Verso), qui n'est ni utilisée ni citée.
- Dans les corps anglais et allemands, les mots de Lordon, quand ils sont cités, sont rendus brièvement par nous, avec les mêmes repères ; le champ `citation` garde l'original français.
- Les titres de section et les repères (§ 08.4) renvoient à l'édition française.

## Spinoza

- Les liens vers l'*Éthique* renvoient à [SpinozaGraph](https://github.com/mqtin/SpinozaGraph) (en ligne : <https://treillis.qpetit.com/spinoza/>), qui publie le texte latin et des traductions du domaine public. Rien de SpinozaGraph n'est copié ici.
- Les énoncés des prémisses S sont des reformulations de Spinoza. Les citations de Spinoza sont celles que fait Lordon, dans les traductions qu'il emploie : Robert Misrahi pour l'*Éthique* (traduction protégée), Charles Ramond pour le *Traité politique* (traduction protégée), Charles Appuhn pour quelques lettres et passages (domaine public). Elles sont courtes et sourcées.

## Autres auteurs

Les citations de Marx et Engels, Kant, Pascal, Camus, Bourdieu, Deleuze, Balibar et d'autres sont celles que rapporte Lordon, avec la référence qu'il donne en note.

## Le projet

- Reconstruction, traductions anglaise et allemande, outils et explorateur : auteur du dépôt [mqtin](https://github.com/mqtin), 2026, avec l'aide de Claude (Anthropic).
- L'explorateur est adapté de celui d'Homo Status, autre projet du même auteur (<https://treillis.qpetit.com/status>).
- Licences : code sous GPL-3.0, travail de reconstruction (et ses traductions) sous CC BY-SA 4.0, citations exclues (voir `LICENSE`).

**Ces mentions doivent être conservées** dans toute redistribution du dépôt ou d'`explorer.html`.
