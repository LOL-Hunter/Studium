# GIT-Cheat-Sheet

---
**Git-Config**

Um das version-control korrekt durchf�hren zu k�nnen, muss GIT den Namen und die Email-Adresse wissen.

````shell
git config user.name "<name>"
git config user.email "<email>"
````
Dieser Befehl setzt name bzw Email.
````shell
git config --global user.name "<name>"
git config --global user.email "<email>"
````
Um name und Email global, also in allen GIT-Projekten festzuegen verwendet man das Schl�sselwort global.

OPTIONAL: Es k�nnen Alias von GIT Commands erstellt werden um diese zu vereinfachen.
````shell
git config alias.c commit
````
Hier kann der Commit �ber ``git c`` ausgef�hrt werden.

---
**Init**

Um ein neues GIT-Projekt zu initialisieren, verwendet man:
````shell
git init
````
Wichtig: Das Projekt wird am AKTUELLEN Terminal-Pfad erstellt.

---
**Modified**

Wenn eine Datei ge�ndert wurde, ist sie Modified.

---
**Stage**

Der Stage einer Modified Datei f�gt diese ins Staging Environment hinzu. Diese Datei is nun bereit Committet zu werden.
Alle Dateien die im Staging Environment vorgemerkt sind, werden im n�chsten Commit in die Datenbank gespeichert.
Die Datei ist jetzt nicht mehr Modified.

````shell
git add index.html
````
````shell
git add --all
````

---
**Commit**

�ber den Commit werden alle Stage �nderungen als Snapshot in die Lokale Datenbank �bernommen.

````shell
git commit -m "<message>"
````

````shell
git commit -a -m "<message>"
````
Hier wird automatisch vor dem Commit ein Stage auf alle Dateien ausgef�hrt.

---
**Stash**

Dies wird ben�tigt, wenn ein Commit noch nicht fertig (programmiert) ist und es muss aber etwas anderes gemacht werden.
Dann k�nnen die Stages tempor�r gespeichert werden.
Und sp�ter kann auf die �nderungen wieder zugegriffen werden.

````shell
git stash
````
Speichert die nicht Comitteten Stages.

````shell
git stash pop
````
Wendet den Stash auf den Branch an und der Stash wird gel�scht.

---
**Repository**

Das Lokale Repository ist der Ordner in dem sich das Projekt bzw die GIT-Datenbank (.git) befindet.

---
**Clone**

Hierbei wird die GIT-Datenbank (.git) von einem anderen Projekt oder Ordner in diesen kopiert.

````shell
git clone <url>
````

---
**Branch**

Ein Branch ist eine neue oder separate Version des Main-Repository. 
Dieser erlaubt an verschiedenen Teilen des Projekts zu arbeiten, ohne den Main-Teil zu beeinflussen.

````shell
git branch <name>
````
Erstellt ein neuen Branch vom aktuellen Stand des Projekts.

````shell
git branch
````
Listet alle verf�gbaren Branches auf. Der Branch auf dem sich git gerade befindet ist mit einem Stern Markiert.

````shell
git branch -d <name>
````
L�scht den angegebenen Branch.

---
**Checkout**
Der Branch wird auf den angegebenen Branch ge�ndert.
Es werden auch alle Dateien ersetzt.

````shell
git checkout <name> 
````

---
**Merge**

F�hrt den Aktuellen Branch mit dem angegebenen Branch zusammen.

Wenn der angegebene Branch eine Weiterentwicklung des aktuellen Branches ist, kann dieser einfach gemerged werden.
Wenn sich die Branches jedoch unterscheiden, dann wird �ber den ausgef�hrten merge Befehl eine Fehlermeldung ausgegeben. 
````shell
git merge <name>
````

Wenn der Merge fehlgeschlagen ist:
Wenn man die Datei, wegen der der Merge fehlgeschlagen ist, �ffnet, dann sieht es ungef�hr so aus:

````html
<<<<<<< HEAD
<p>This line is here to show how merging works.</p>
=======
<p>A new line in our file!</p>
>>>>>>> hello-world-images
````
Hier kann frei entschieden werden ob beide oder nur eine �nderung �bernommen werden soll.
Dazu einfach �ndern, die Zeilen "HEAD", ">>>>>>" und "=====" entfernen, speichern, add, commit.
Nun ist der Merge abgeschlossen und der Branch <name> kann gel�scht werden da er gleich zu dem aktuellen Branch ist.

---
**Diff**

Zeigt die Unterschiede zwischen dem letzten Commit und dem Aktuellen stand der Dateien.
````shell
git diff
````

---
**Pull**

Bei einem Pull wird das Repository von einem anderen meist Externen Repository heruntergeladen.
Es wird das lokale Repository �berschrieben.
Und direkt ein Merge eingeleitet.

````shell
git pull <remote>
````

---
**Fetch**
Bei einem Fetch wird das Repository von einem anderen meist Externen Repository heruntergeladen.
Es wird jedoch kein Merge eingeleitet.
Und es wird auch nicht das lokale Repository �berschrieben.

````shell
git fetch <remote> [<branch>]
````

---
**Push**

Hochladen der Lokalen Commits ins remote Repository.
````shell
git push <remote> [<branch>]
````

## Weiter Begriffe:

**Rebase**
**Reflog**

**Tag**
**Blame**

**Clean**
**Reset**
**Rm**
**Revert**



**Contribute**