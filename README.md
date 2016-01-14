# LaTeX-Master-Vorlage

Die Latex-Master-Vorlage kann für Forschungsprojekte, Bachelor- und Masterarbeiten optimal genutzt werden. Notwendigen Pakete sind bereits eingebunden und Einstellungen vorgenommen. Die Funktionskommentare innerhalb der *.tex Dateien sind größtenteils auf Deutsch. Ergänzungen Anderer können jedoch in englischer Sprache ausfallen. Diese werden, wenn notwendig, zeitnah übersetzt.

# Empfohlene Umgebung

Die Vorlage wurde erfolgreich unter der [TEX Live](http://tug.org/texlive/) Umgebung mit folgenden Programmen kompiliert.

- **Compiler**: lualatex
- **Bibliographie**: biber
- **Index**: makeindex (Ergänzungen unter Anmerkungen beachten)
- **Glossar**: makeglossaries

# Beispiel-PDF

[PDF Ansehen](main.pdf)

# Anmerkungen
## Stichwortverzeichnis
Zum Erzeugen des Glossar und Abkürzungsverzeichnis muss "makeinxed" wie folgt aufgerufen werden:

*makeindex -s main.ist -t main.glg -o main.gls main.glo*

*makeindex -s main.ist -t main.alg -o main.acr main.acn*

Der Titel im Header der Seite muss zusätzlich in der Style-Datei "[indexstyle.ist](indexstyle.ist)" angepasst werden:

siehe: preamble "\\\markboth{**STICHWORTVERZEICHNIS**}{}\n\n\\begin{theindex}\n"