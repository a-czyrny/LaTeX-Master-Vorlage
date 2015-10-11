# LaTeX-Master-Vorlage
Die Funktionskommentare sind innerhalb der *.tex Dateien auf Deutsch.

## Anmerkungen
### Stichwortverzeichnis
Zum Erzeugen des Stichwortverzeichnisses muss "makeinxed" wie folgt aufgerufen werden:

*makeindex  -s indexstyle.ist main.idx*

### biber downgrade
Sollte das Erstellen der Literaturverzeichnisse nicht funktionieren, ist es in einigen Fällen notwendig "biber" zu downgraden. Als vollständig kompatibel hat sich Version 1.9 (http://sourceforge.net/projects/biblatex-biber/files/biblatex-biber/1.9/) herausgestellt.
