# NIP'AJIN Shots

[Deutsch](README.md) | [English](README.en.md).

Bitte beachte die Lizenzinformationen im Hauptverzeichnis.

## Einleitung

Diese Flyer sind komplette, eigenständig spielbare Mini-Rollenspiele auf 2 A6 Seiten: eine Seite Regeln, eine Seite Szenario.

## Schnellanleitung

In jedem Unterverzeichnis finden sich alle nötigen Dateien für jeweils einen Flyer. Wenn alle Voraussetzungen erfüllt sind, generiert

```
flyer-name$ make de
```

das deutsche PDF in einen `out` Ordner.

Welche anderen Sprachen bereits verfügbar sind, ist im `Makefile` ersichtlich.

## Flyer übersetzen

Wenn du einen Flyer übersetzen möchtest, befolge diese Schritte:

* Kopiere die `content.xx.tex` deiner Ausgangsprache nach `content.yy.tex`. Dabei ist yy das ISO 639-1 Kürzel deiner Zielsprache.
* Editiere die neue `content.yy.tex` und übersetze alle Texte. Achte darauf, einen UTF-8 Editor zu benutzen, die Einrückungen nicht zu ändern und die Makro-Namen nicht zu ändern.
* Editiere das `Makefile`. Füge am Anfang der Datei ein `VERSION_yy = ...` für deine Sprache hinzu. Kopiere dann den Block einer bestehenden Sprache und ändere ihn auf deine Sprache yy ab.
* Wenn du fertig bist, kannst du mit `make yy` dein Szenario in ein PDF verwandeln.
