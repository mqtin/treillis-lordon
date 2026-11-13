# Quellen, Rechte und Angaben

Dieses Projekt rekonstruiert die Argumentation eines urheberrechtlich geschützten Buches. Es gibt seinen Text nicht wieder: Es **paraphrasiert** ihn, mit Verweis auf jede Stelle, und **zitiert** nur kurze Auszüge. **Wer Lordon lesen will, lese Lordon.**

## Das Buch

- Frédéric Lordon, *Capitalisme, désir et servitude. Marx et Spinoza*, Paris, La Fabrique, 2010. © Frédéric Lordon und La Fabrique éditions.
- Englische Übersetzung: *Willing Slaves of Capital. Spinoza and Marx on Desire*, übers. von Gabriel Ash, London, Verso, 2014.
- Was das Repository vom Buch enthält: kurze Zitate (433 Stellen, fast alle wenige Wörter lang; höchstens 29 aufeinanderfolgende Wörter von Lordon), jeweils mit Fundstelle (Abschnitt und Absatz), und die Titel seiner Abschnitte, die als Fundstellen dienen. Der Text selbst wird nicht verbreitet: Der Ordner `source/` ist aus dem Repository ausgeschlossen, und `outils/check.py` prüft, dass es so bleibt.
- Diese Zitate fallen unter das Recht des kurzen Zitats (französisches Gesetzbuch über geistiges Eigentum, Art. L122-5, 3°): Sie sind in eine analytische Arbeit eingebunden, und ihre Quelle ist angegeben. Sie fallen **nicht** unter die Lizenzen des Repositorys (siehe `LICENSE`).

## Die übersetzten Fassungen

- Die englische und die deutsche Fassung übersetzen die Rekonstruktion (Titel, Aussagen, Beweise, Kommentare). Sie beruhen auf der französischen Rekonstruktion, nicht auf einer veröffentlichten Übersetzung des Buches, die weder benutzt noch zitiert wird.
- In den englischen und deutschen Texten sind Lordons Worte, wo sie zitiert werden, unsere eigenen kurzen Übertragungen aus dem Französischen, mit denselben Fundstellen; das Feld `citation` bewahrt das französische Original.
- Abschnittstitel und Fundstellen (§ 08.4) beziehen sich auf die französische Ausgabe.

## Spinoza

- Die Verweise auf die *Ethik* führen zu [SpinozaGraph](https://github.com/mqtin/SpinozaGraph) (online: <https://treillis.qpetit.com/spinoza/>), das den lateinischen Text und gemeinfreie Übersetzungen veröffentlicht. Nichts aus SpinozaGraph wird hier kopiert.
- Die Aussagen der S-Prämissen sind Paraphrasen Spinozas. Die Spinoza-Zitate sind die, die Lordon anführt, in den Übersetzungen, die er verwendet: Robert Misrahi für die *Ethik* (geschützte Übersetzung), Charles Ramond für den *Politischen Traktat* (geschützte Übersetzung), Charles Appuhn für einige Briefe und Stellen (gemeinfrei). Sie sind kurz und belegt; in der deutschen Fassung sind sie von uns übertragen.

## Andere Autoren

Die Zitate von Marx und Engels, Kant, Pascal, Camus, Bourdieu, Deleuze, Balibar und anderen sind die, die Lordon anführt, mit der Referenz, die er in seinen Anmerkungen angibt.

## Das Projekt

- Rekonstruktion, Übersetzungen, Werkzeuge und Explorer: Autor des Repositorys [mqtin](https://github.com/mqtin), 2026, mit Hilfe von Claude (Anthropic).
- Der Explorer ist von dem von Homo Status übernommen, einem anderen Projekt desselben Autors (<https://treillis.qpetit.com/status>).
- Lizenzen: Code unter GPL-3.0, Rekonstruktionsarbeit (und ihre Übersetzungen) unter CC BY-SA 4.0, Zitate ausgenommen (siehe `LICENSE`).

**Diese Angaben müssen** bei jeder Weitergabe des Repositorys oder von `explorer.html` **erhalten bleiben**.
