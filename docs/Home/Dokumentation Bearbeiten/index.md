# Dokumentation Bearbeiten

Diese Dokumentation basiert auf [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Auf dieser Website gibt es auch eine Umfangreiche Dokumentation.

### Setup
Um die Dokumentation selbst zu bearbeiten, muss man sich das [Repository](https://github.com/PandorasBoxStudios/Documentation) klonen.
Wenn man das Repository geklont hat, kann man die Umgebung am besten in VS Code öffnen.


Sobald man das Repository geklont hat, sollte man mit hilfe des Terminals (Windows Power Shell) ein virtuelles environment für python erstellen.

Ich empfehle diese Videos: 
[:simple-youtube: Mac](https://www.youtube.com/watch?v=xlABhbnNrfI)
[:simple-youtube: Windows](https://www.youtube.com/watch?v=NY7DHvo1XVM&t=386s)

Folgende Plugins sollte man außerdem noch mit Hilfe von pip installieren:

!!! note warning "Wichtig!"
    Plugins sollte man in der Virtuellen Maschine installieren, also erst .venv\Scripts\activate.ps1 starten, dann die pip installs machen

``` py
pip install mkdocs-git-revision-date-localized-plugin
pip install mkdocs-git-authors-plugin
```


Möchte man eine neue Seite erstellen, einfach in den entsprechenden Ordner gehen und eine neue `.md` Datei erstellen. Möchte man Seiten verschachteln, einfach neue Ordner erstellen und entsprechend benennen. Möchte man, dass man auf den Parent (Also Ordner) auch eine Seite hat, dann in dem Ordner eine `Index.md` Seite erstellen

``` sh title="Beispiel, wie eine Seite aufgebaut ist"
docs
| Folder
| | index.md #(1)
| page.md #(2)
```

1.  Das ist die Page, die erscheint, wenn man auf 'Folder' klickt
2.  Das ist eine normale Page

### Reihenfolge der Seiten verändern
Für das ändern der Reihenfolge von Seiten wird das Plugin [mkdocs-awesome-pages](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin) verwendet.
Möchte man die Reigenholge der Seiten verändern, legt man sich im übergeordneten Order eine `.pages` File an. Das die `.pages` Datei gilt nur für den Scope, in der diese Datei angelegt wurde.

``` sh title="Beispiel Aufbau einer .pages Datei"
nav:
    - Seite 1
    - Seite 2
```