# LaTeX-Master-Vorlage

Die Latex-Master-Vorlage kann für Forschungsprojekte, Bachelor- und Masterarbeiten optimal genutzt werden. Notwendige
Pakete sind bereits eingebunden und Einstellungen vorgenommen. 

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

* ```git``` (zum Clonen und Contributen)
* ```perl``` (für ```latexmk```)
* ```latexmk``` (über MikTex)

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

* ```git``` (zum Clonen und Contributen)
* ```perl``` (für ```latexmk```)
* ```latexmk``` (über MikTex)

## Runterladen der LaTeX Dateien
Die Vorlage kann entweder mit ```git clone https://github.com/a-czyrny/LaTeX-Master-Vorlage.git``` (siehe optionale Software) oder mit über die GitHub Seite als *.zip Datei runtergeladen werden.


## Bearbeiten und Compilieren der LaTeX Dateien
### Windows
Unter **Windows** ist [TexStudio](http://www.texstudio.org/) als Editor empfohlen.

Wenn die Standardeinstellungen von TexStudio genutzt werden, müssen noch zwei manuelle Schritte durchgeführt werden:
1. Die Referenzen für das Glossar und das Abkürzungsverzeichnis müssen erstellt werden. In der Kommandozeile in dem Ordner der Vorlage:

```
makeindex -s main.ist -t main.alg -o main.acr main.acn
makeindex -s main.ist -t main.glg -o main.gls main.glo 
```

2. Das LaTeX Dokument muss zwei mal compiliert werden (```F5```) damit alle Referenzen aufgelöst werden.

**Alternative** 

Wenn ```latexmk``` installiert wurde (siehe optionale Software) kann im TexStudio unter "Optionen / TexStudio konfigurieren / Erzeugen" auch ```latexmk```als Standardkompiler angegeben werden.
```latexmk```funktioniert dann auch von der Kommandozeile aus
 
### Linux
Unter **Linux** kann die Vorlage mit dem Texteditor der Wahl editiert werden. Zum compilieren kann ```lualatex``` genutzt werden:

    lualatex -synctex=1 -interaction=nonstopmode main
    biber main
    makeindex main
    makeindex -s main.ist -t main.alg -o main.acr main.acn
    makeindex -s main.ist -t main.glg -o main.gls main.glo
    lualatex -synctex=1 -interaction=nonstopmode main
    lualatex -synctex=1 -interaction=nonstopmode main
    
**Alternative**
Wenn ```latexmk``` installiert wurde (siehe optionale Software) kann in dem Verzeichnis auch ```latexmk```angegeben werden. Dies führt die oben genannten Schritte aus.
    

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

# Lizenz
<p xmlns:dct="http://purl.org/dc/terms/" xmlns:cc="http://creativecommons.org/ns#"><a rel="cc:attributionURL" property="dct:title" href="https://github.com/a-czyrny/LaTeX-Master-Vorlage">LaTeX Master Vorlage</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/a-czyrny">Alexander Czyrny</a> is licensed under <a href="https://creativecommons.org/licenses/by-nc-sa/4.0?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution-NonCommercial-ShareAlike 4.0 International</a></p>
