# LaTeX-Master-Vorlage

Die Latex-Master-Vorlage kann für Forschungsprojekte, Bachelor- und Masterarbeiten optimal genutzt werden. Notwendigen Pakete sind bereits eingebunden und Einstellungen vorgenommen. 

Diese LaTeX Vorlage wurde bereits für Masterarbeiten an der Hochschule für Technik und Wirtschaft Berlin (HTW Berlin), Fachbereich 4 genutzt.

Wenn diese Vorlage für deine Arbeit (oder Forschungsprojekt) genutzt wurde, schreibe bitte den Professor/Prüfer unten an die Liste. 

# Beispiel-PDF

[PDF Ansehen](main.pdf)

# Benutzung

Um diese Vorlage nutzen zu können muss die benötigte Software installiert werden. Sobald dies der Fall ist, kann die Vorlage runtergeladen und angepasst werden.

## Empfohlene Umgebung
Die Vorlage wurde erfolgreich unter der [TEX Live](http://tug.org/texlive/) Umgebung mit folgenden Programmen kompiliert.

- **Compiler**: lualatex
- **Bibliographie**: biber
- **Index**: makeindex (Ergänzungen unter Anmerkungen beachten)
- **Glossar**: makeglossaries

## Installieren der benötigten Software
### Windows
**Benötigte Software:**

* MikTex
* TexStudio

**Optionale Software:**

* git (zum Clonen und Contributen)
* perl (für ```Latexmk```)

### Linux (getestet mit Debian Jessie)
**Benötigte Software:**

* wget (```apt-get -y install wget```)
* texlive (```apt-get -y install texlive```)
* texlive Pakete:
        wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz &&\
        tar -xzvf install-tl-unx.tar.gz &&\
        rm install-tl-unx.tar.gz
        echo I | install-tl*/install-tl
* Pakete zu Path hinzufügen
        PATH=/usr/local/texlive/2015/bin/x86_64-linux:$PATH    
* Noch mehr settings:
        tlmgr conf texmf TEXMFHOME "/usr/local/texlive/2015/bin/x86_64-linux"

**Optionale Software:**

* git (zum Clonen und Contributen)
* perl (für ```Latexmk```)

## Runterladen der LaTeX Dateien
Die Vorlage kann entweder mit ```git clone https://github.com/a-czyrny/LaTeX-Master-Vorlage.git``` (siehe optionale Software) oder mit über die GitHub Seite als *.zip Datei runtergeladen werden.


## Bearbeiten und Compilieren der LaTeX Dateien
Unter **Windows** kann TexStudio genutzt werden, die Vorlage den eigenen Bedürfnissen anzupassen und zu compilieren.
Um die Vorlage mit TexStudio zu bearbeiten, muss die main.tex mit TexStudio geöffnet werden.
Mit ```F5``` wird dann das PDF erstellt.

**Achtung**

Um Referenzen korrekt aufzulösen, muss das Dokument mehrfach compiliert werden. Zweimal hintereinander ```F5``` löst dieses Problem.

Unter **Linux** kann die Vorlage mit dem Texteditor der Wahl editiert werden. Zum compilieren kann ```lualatex``` genutzt werden:

    lualatex -synctex=1 -interaction=nonstopmode main
    biber main
    makeindex main
    makeindex -s main.ist -t main.alg -o main.acr main.acn
    makeindex -s main.ist -t main.glg -o main.gls main.glo
    lualatex -synctex=1 -interaction=nonstopmode main
    lualatex -synctex=1 -interaction=nonstopmode main

# Contributing 
Die Funktionskommentare innerhalb der *.tex Dateien sind größtenteils auf Deutsch. 
Ergänzungen Anderer können jedoch in englischer Sprache ausfallen. Diese werden, wenn notwendig, zeitnah übersetzt.
  
# Anmerkungen
## Stichwortverzeichnis
Zum Erzeugen des Glossar und Abkürzungsverzeichnis muss "makeinxed" wie folgt aufgerufen werden:

*makeindex -s main.ist -t main.glg -o main.gls main.glo*

*makeindex -s main.ist -t main.alg -o main.acr main.acn*

Der Titel im Header der Seite muss zusätzlich in der Style-Datei "[indexstyle.ist](indexstyle.ist)" angepasst werden:

siehe: preamble "\\\markboth{**STICHWORTVERZEICHNIS**}{}\n\n\\begin{theindex}\n"

# Welcher Professororen/ Prüfer haben Arbeiten mit dieser Vorlage bereits zugestimmt?
* Prof. Dr. Fortenbacher, Masterarbeit
