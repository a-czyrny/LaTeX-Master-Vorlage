# LaTeX-Master-Vorlage
Die Funktionskommentare sind innerhalb der *.tex Dateien auf Deutsch.

## Anmerkungen
### Stichwortverzeichnis
Zum Erzeugen vom Stichwortverzeichnis, Glossar und Abkürzungsverzeichnis muss "makeinxed" wie folgt aufgerufen werden:

*makeindex -s indexstyle.ist main.idx*
*makeindex -s main.ist -t main.glg -o main.gls main.glo*
*makeindex -s main.ist -t main.alg -o main.acr main.acn*

### biber downgrade
Sollte das Erstellen der Literaturverzeichnisse nicht funktionieren, ist es in einigen Fällen notwendig "biber" zu downgraden. Als vollständig kompatibel hat sich Version 1.9 (http://sourceforge.net/projects/biblatex-biber/files/biblatex-biber/1.9/) herausgestellt.
