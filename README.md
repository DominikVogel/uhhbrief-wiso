# LaTeX-Briefvorlage für die WiSo-Fakultät der Uni Hamburg

[Reinhard Zierke](https://www2.informatik.uni-hamburg.de/~zierke/) hat ein wunderbares LaTeX-Paket geschrieben, das es ermöglicht, LaTeX-Briefe im Corporate Design der Universität Hamburg zu verfassen. Für meine Zwecke hat das Paket jedoch zwei Nachteile:

1. Es nutzt das veraltete Logo der WiSo-Fakultät
2. Die Installationsanleitung klammert Windows aus.

Ich habe daher die Briefvorlage angepasst und untenstehend eine Installationsanleitung für Windows geschrieben.

# Installation von ``uhhbrief`` in Windows (mit MiKTeX)

Die Anleitung basiert auf der Anleitung, die ich unter https://www.tug.org/fonts/fontinstall.html gefunden habe.

1. ``uhhbrief.zip`` und die dazugehörige LaTeX-Unterstützung für die Hausschrift ``thesansuhh.zip`` von https://www2.informatik.uni-hamburg.de/universitaet/uhhbrief.php herunterladen.
2. Die beiden zip-Dateien nach ``%USERPROFILE%\Roaming\MiKTeX\2.9\`` entpacken (z. B. ``C:\Users\Vogel\AppData\Roaming\MiKTex\2.9\``).
3. Eingabeaufforderung öffnen und ``initexmf --edit-config-file updmap`` eingeben. Es öffnet sich ein Texteditor. Dort folgendes eintragen, speichern und schließen: ``Map thesansuhh.map``
4. In der Eingabeaufforderung ``initexmf --mkmaps`` eingeben und Fehlermeldungen ignorieren.
5. Die erfolgreiche Installation der Schrift kann mithilfe der Eingabeaufforderung getestet werden:
    1. ``pdftex testfont`` eingeben
    2. ``ftsb7t`` eingeben
    3. ``\table`` eingeben
    4. ``\bye`` eingeben
    5. MiKTeX erstellt eine PDF im aktuellen Verzeichnis
    
    
## Problemlösung
 
Sollte es zu Problemen kommen, kann es helfen, die MiKTeX Console zu öffnen und die unter "Task" aufgeführten Aufgaben anzustoßen.
    
# Neues Fakultätslogo nutzen
 
Um das aktuelle Logo der WiSo-Fakultät nutzen zu können, muss die Datei ``UHH_Plakat_DINlang_Wortmarken_WiSo.pdf`` im selben Verzeichnis wie die tex-Datei liegen. Zusätzlich muss die Präambel die Zeile ``\fakultaetslogo{UHH_Plakat_DINlang_Wortmarken_WiSo}{46.9truemm}{-0.5truemm}{3truemm}`` enthalten. 
 
``Beispiel-Brief.tex`` enthält den LaTeX-Code für einen vollständigen Brief. Das Ergebnis ist in ``Beispiel-Brief.pdf`` dokumentiert.
 
 
