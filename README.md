# Git Bisect Demo

Dies ist eine Demo zur Verwendung von git bisect, um einen Fehler in einem Projekt zu finden. Es handelt sich hierbei um eine Angular App, die in der Mitte vom Bildschirm eine Animation ausführen soll. In der aktuellen Version, funktioniert es nicht mehr. Finde den Fehler und behebe ihn!

## Schritt-für-Schritt-Anleitung für Git Bisect

1. Clone das Repository auf den Computer.

2. Starte den Git Bisect-Prozess mit dem Befehl `git bisect start`.

3. Markiere einen Commit, bei dem das Problem noch nicht vorhanden war, mit `git bisect good [commit-hash]`.

4. Markiere einen Commit, bei dem das Problem bereits vorhanden war, mit `git bisect bad [commit-hash]`.

5. Git wird automatisch zu einem Commit in der Mitte beider Commits gebracht. Überprüfe das Verhalten der Anwendung und markiere es als "good" oder "bad" mit `git bisect good` oder `git bisect bad`.

6. Git wird zu einem neuen Commit gebracht und wiederholt den Prozess, bis es den Commit gefunden hat, bei dem das Problem begonnen hat.

7. Sobald Git den Commit gefunden hat, beende den Bisect-Prozess mit `git bisect reset`.

8. Überprüfe den Commit, um den Ursprung des Fehlers zu identifizieren und behebe ihn.

Das war's! Mit Git Bisect kann man den Ursprung eines Fehlers im Code schnell und effizient finden, indem man den Code automatisch bis zum fehlerhaften Commit durchsucht. Überprüfe jeden Commit gründlich, um sicherzustellen, dass das Problem tatsächlich gefunden wurde.