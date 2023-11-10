<h1>Konfiguration des Ersatzvmhosts</h1>
Da für der Rechner mehrere Festplatten und SSDs hat, müssen für die Installation des Betriebssystem alle Blockgeräte ausser dem für das OS vorgesehenen abgeklemmt werden.

**Vorher muss, im Falle einer Neuinstallation des Systems, dafür gesorgt werden, daß alle LVs und VGs auf allen Datenträgern des Rechners gelöscht sind**

Sonst kann das Ansiblescript für die Initiale Installation das neue VG nicht korrekt umbenennen, das Resultat ist ein nicht bootbares System.

**Die Installation findet daher in zwei Schritten statt.**

<h2>Installation</h2>

1. Abklemmen aller Blockgeräte, ausser demjenigen für das OS.
1. Installation des OS via PXE mit dem beiliegenden Preseed-File.
1. Starten des Rezeptes ``pbkvmhost01-initial.yml``.
1. Stoppen des Rechners und Anschliessen aller übrigen Blockgeräte.
1. Starten des Rezeptes ``pbkvmhost01.yml``.