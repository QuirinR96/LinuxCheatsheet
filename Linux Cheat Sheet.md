## Dateisystem
In jedem Linux-Dateisystem gibt es eine bemerkenswerte Eigenschaft: Alles wird als Datei behandelt.
+ Ordnertrenner: / ('/home/user/Documents/file.txt')
### Ordnerstruktur
+ **/** : Root - Oberstes Verzeichnis, beinhaltet alle Ordner und Dateien
	+ **bin** : Binaries - Essentielle ausführbare Terminal-Binärdateien
	+ **boot** : Boot - Statische Dateien des Bootloaders
	+ **dev** : Devices - Gerätedateien
	+ **etc** : Et-Cetera - Systemweite Konfigurationsdateien
	+ **lib** : Libraries - Essentielle geteilte Bibliotheken und Kernel-Module
	+ **media** : Media - Automatischer Einhängepunkt für Massenspeicher
	+ **mnt** : Mount - Manueller Einhängepunkt
	+ **opt** : Optional - Optionale Softwarepakete und Anwendungsprogramme
	+ **run** : Running - Relevante Daten für laufende Prozesse
	+ **sbin** : System Bin. - Essentielle System-Binärdateien
	+ **srv** : Services - Daten für Dienste, die vom System bereitgestellt werden
	+ **tmp** : Temporary - Temporäre Dateien
	+ **usr** : Benutzerprogramme, -bibliotheken und -dokumentationen sowie systemweite ausführbare Dateien und Hilfsprogramme
	+ **var** : Variable - Dateien, die sich häufig ändern (Logs, ...)
  + **home/[user]** : Home - Benutzerverzeichnisse

+ **/home/[user]**
	+ **Documents, Downloads, Music, Pictures, Videos** : frei verwendbare Benutzerordner
	+ **Desktop** : auf Dektop angezeigte Daten
	+ **Public** : Daten, die konstant mit anderen geteilt werden sollen
	+ **Templates** : Vorlagen
	+ **.config** : Benutzerspezifische Konfiguration
	+ **.local/share** : Benutzerspezifische Daten und Programmeinstellungen
	+ **.cache** : Zwischenspeicher für Programmdaten

(# => {Nummer}, ? => {Buchstabe})
+ **/dev**
	+ **null** : Verwirft alle hierher geschriebenen Daten
	+ **zero** : Liefert beim Lesen unendlich viele Nullen
	+ **full** : Liefert beim Schreiben immer eine Fehlermeldung „Kein Speicherplatz mehr verfügbar“
	+ **random** : Erzeugt zufällige Daten
	+ **urandom** : Erzeugt pseudozufällige Daten
	+ **tty** : repräsentiert das aktuelle Terminal
	+ **tty#** : repräsentiert jeweiliges Terminal
	+ **/ttyS#** : serielle Schnittstelle
	+ **ttyUSB#** : USB-zu-Seriell-Schnittstelle
	+ **sd?** : Massenspeicher-Gerät
	+ **sd?#** : Partition eines Massenspeichergeräts
	+ **cdrom** : Link zum 1. CD-ROM-Laufwerk (sr0)
	+ **sr#**: CD-ROM-Laufwerk
  + **rtc** : Echtzeituhr (Real-Time Clock)
  + ...

## Terminal
### Datei- und Verzeichnisverwaltung
+ **ls** : list - Verzeichnisinhalt anzeigen
+ **cd** : change directory - Verzeichnis wechseln
+ **cp** : copy - Dateien/Verzeichnisse kopieren
+ **mv** : move - Dateien/Verzeichnisse verschieben/umbenennen
+ **rm** : remove - Dateien/Verzeichnisse löschen
+ **mkdir** : make directory - Verzeichnis erstellen
+ **rmdir** : remove directory - Leeres Verzeichnis löschen
+ **touch** : touch - Leere Datei erstellen/Zeitstempel ändern
+ **pwd** : print working directory - Aktuelles Verzeichnis anzeigen
+ **find** : find - Dateien/Verzeichnisse suchen
+ **ln** : link - Symbolischen/Hardlink erstellen
+ **stat** : stat - Datei-/Verzeichnisdetails anzeigen
+ **file** : file - Dateityp erkennen

### Benutzerverwaltung
+ **who** : who - Angemeldete Benutzer anzeigen
+ **w** : w - Angemeldete Benutzer und deren Aktivitäten anzeigen
+ **whoami** : whoami - Aktuellen Benutzer anzeigen
+ **id** : id - Benutzer- und Gruppeninformationen anzeigen
+ **useradd** : add user - Benutzer hinzufügen
+ **userdel** : delete user - Benutzer löschen
+ **usermod** : user modify - Benutzerkonto ändern
+ **passwd** : password - Benutzerpasswort ändern
+ **chage** : change age - Passwort- und Kontoalter ändern
+ **last** : last - Letzte Anmeldezeiten anzeigen
+ **su** : substitute user - Benutzer wechseln
+ **sudo** : superuser do - Befehle als anderer Benutzer ausführen

### Rechteverwaltung
+ **chmod** : change mode - Zugriffsrechte ändern
+ **chown** : change owner - Besitzer ändern
+ **chgrp** : change group - Gruppe ändern
+ **umask** : user mask - Standardrechte festlegen
+ **setfacl** : set file access control list - ACL setzen
+ **getfacl** : get file access control list - ACL anzeigen
+ **lsattr** : list attributes - Dateiattribute anzeigen
+ **chattr** : change attributes - Dateiattribute ändern

### Textmanipulierung
+ **nano** : nano - interaktive Textbearbeitung
+ **cat** : concatenate - Dateiinhalte anzeigen
+ **echo** : echo - Text ausgeben
+ **head** : head - Anfang einer Datei anzeigen
+ **tail** : tail - Ende einer Datei anzeigen
+ **grep** : grep - Muster in Dateien suchen
+ **sed** : stream editor - Text in Dateien bearbeiten
+ **awk** : awk - Textverarbeitung und Musterabgleich
+ **cut** : cut - Textspalten ausschneiden
+ **sort** : sort - Text sortieren
+ **uniq** : unique - Doppelte Zeilen entfernen
+ **tr** : translate - Zeichen übersetzen oder löschen
+ **wc** : word count - Zeilen, Wörter und Zeichen zählen
+ **diff** : difference - Unterschiede zwischen Dateien anzeigen
+ **patch** : patch - Unterschiede anwenden
+ **nl** : number lines - Zeilen nummerieren
+ **fmt** : format - Text formatieren
+ **pr** : print - Textdateien für Druck aufbereiten
+ **fold** : fold - Lange Zeilen umbrechen
+ **join** : join - Dateien zeilenweise verbinden
+ **paste** : paste - Dateien nebeneinander ausgeben

### Dateisystem- und Datenträgerverwaltung+ **mount** : mount - Dateisystem einhängen
+ **umount** : unmount - Dateisystem aushängen
+ **df** : disk free - Freien Speicherplatz anzeigen
+ **du** : disk usage - Speicherplatznutzung anzeigen
+ **fsck** : file system check - Dateisystemprüfung durchführen
+ **mkfs** : make filesystem - Dateisystem erstellen
+ **blkid** : block id - Blockgeräte und Dateisysteme anzeigen
+ **lsblk** : list block - Blockgeräte anzeigen
+ **parted** : partition editor - Partitionen verwalten
+ **fdisk** : format disk - Partitionstabelle bearbeiten
+ **mkpart** : make partition - Partition erstellen
+ **resize2fs** : resize ext2 filesystem - Dateisystemgröße ändern (ext2/ext3/ext4)
+ **tune2fs** : tune ext2 filesystem - Dateisystemparameter ändern (ext2/ext3/ext4)
+ **mkswap** : make swap - Swap-Partition erstellen
+ **swapon** : swap on - Swap-Partition aktivieren
+ **swapoff** : swap off - Swap-Partition deaktivieren
+ **cryptsetup** : crypt setup - Datenträgerverschlüsselung einrichten
+ **mount.cifs** : mount cifs - CIFS-Netzwerkdateisystem einhängen
+ **mount.nfs** : mount nfs - NFS-Netzwerkdateisystem einhängen

### Prozessverwaltung
+ **ps** : process status - Laufende Prozesse anzeigen
+ **top** : top - Dynamische Prozessanzeige
+ **htop** : htop - Interaktive Prozessanzeige
+ **kill** : kill - Prozess beenden
+ **killall** : kill all - Alle Prozesse mit bestimmten Namen beenden
+ **pkill** : process kill - Prozesse anhand von Kriterien beenden
+ **pgrep** : process grep - Prozesse anhand von Kriterien suchen
+ **nice** : nice - Prozesspriorität festlegen
+ **renice** : renice - Prozesspriorität ändern
+ **bg** : background - Prozess im Hintergrund weiterführen
+ **fg** : foreground - Hintergrundprozess in den Vordergrund holen
+ **jobs** : jobs - Aktuelle Hintergrundprozesse anzeigen
+ **nohup** : no hangup - Prozess gegen Abmelden schützen
+ **at** : at - Einmalige Aufgaben zu bestimmter Zeit planen
+ **cron** : cron - Wiederkehrende Aufgaben planen
+ **crontab** : cron table - Cron-Tabellen bearbeiten
+ **pstree** : process tree - Baumstruktur der Prozesse anzeigen
+ **systemctl** : system control - System- und Dienstverwaltung

### Hilfsprogramme
+ **man** : manual - Handbuchseiten anzeigen
+ **info** : info - Detailinformationen zu Befehlen anzeigen
+ **which** : which - Pfad zu einem Befehl anzeigen
+ **whereis** : where is - Speicherorte von Befehlen und deren Dateien anzeigen
+ **alias** : alias - Alias für Befehle erstellen
+ **unalias** : unalias - Alias entfernen
+ **clear** : clear - Terminalbildschirm löschen
+ **date** : date - Aktuelles Datum und Uhrzeit anzeigen
+ **cal** : calendar - Kalender anzeigen
+ **bc** : basic calculator - Rechner im Terminal
+ **printf** : print formatted - Formatierten Text ausgeben
+ **yes** : yes - Text wiederholt ausgeben
+ **sleep** : sleep - Verzögerung einfügen
+ **time** : time - Ausführungszeit eines Befehls messen
+ **watch** : watch - Befehl in regelmäßigen Abständen ausführen
+ **tee** : tee - Ausgabe in Datei und an Terminal senden
+ **xargs** : x arguments - Argumente aus Standardausgabe lesen und als Befehlsparameter verwenden
+ **basename** : basename - Dateiname ohne Pfad anzeigen
+ **dirname** : dirname - Pfad ohne Dateiname anzeigen
+ **env** : environment - Umgebungsvariablen anzeigen/anpassen
+ **export** : export - Umgebungsvariablen setzen
+ **echo** : echo - Text oder Variableninhalt ausgeben
+ **uname** : unix name - Systeminformationen anzeigen
+ **uptime** : uptime - Systemlaufzeit und Auslastung anzeigen
+ **dmesg** : diagnostic message - Kernel- und Systemmeldungen anzeigen  

### Datenübergabe
+ **|** :  Pipe - Ausgabe von Befehl 1 --> Eingabe in Befehl 2
+ **>** :  Redirect - Ausgabe in Datei (überschreiben)
+ **>>** :  Append - Ausgabe in Datei (anhängen)
+ **<** :  Input Redirection - Eingabe aus Datei
+ **<<** :  Here-Document - Textblock als Eingabe bis Marker
+ **2>** :  Error Redirection - Fehlerausgabe in Datei (überschreiben)
+ **2>>** :  Error Append - Fehlerausgabe in Datei (anhängen)
+ **&>** :  Output and Error Redirection - Ausgabe + Fehler in Datei (überschreiben)
+ **&>>** :  Output and Error Append - Ausgabe + Fehler in Datei (anhängen)

## Linux Geschichte
+ **1991**: Linus Torvalds startet das Linux-Projekt und veröffentlicht die erste Version des Linux-Kernels.
+ **1992**: Linux wird unter der GNU General Public License (GPL) veröffentlicht.
+ **1993**: Die erste Slackware-Distribution wird veröffentlicht, gefolgt von Debian.
+ **1994**: Linux Kernel Version 1.0 wird veröffentlicht.
+ **1996**: Linux Kernel Version 2.0 kommt mit Unterstützung für Symmetrisches Multiprocessing (SMP).
+ **1998**: IBM und andere große Firmen beginnen, Linux zu unterstützen.
+ **2001**: Linux Kernel Version 2.4 wird veröffentlicht, verbessert Netzwerksupport und USB-Unterstützung.
+ **2003**: Red Hat wechselt von Red Hat Linux zu Red Hat Enterprise Linux (RHEL).
+ **2005**: Linus Torvalds entwickelt das Versionskontrollsystem Git.
+ **2006**: Ubuntu wird immer beliebter als benutzerfreundliche Distribution.
+ **2011**: Linux Kernel Version 3.0 wird veröffentlicht.
+ **2015**: Linux Kernel Version 4.0 erscheint mit Live-Patching-Fähigkeiten.
+ **2020**: Linux Kernel Version 5.0 bringt zahlreiche Leistungs- und Sicherheitsverbesserungen.
+ **2021**: 30-jähriges Jubiläum von Linux.

### Technische Details
+ **Geräte:** Programm -> Gerätedatei -> Kernel -> Hardwareabstraktionsschicht (HAL) -> Treiber -> Gerät
+ **Systemaufrufe:** Programm -> Bibliotheken -> Systemaufrufe (Syscalls) -> Kernel (System Calls Interface) -> {Prozessverwaltung, Speicherverwaltung, Dateisystemverwaltung, Netzwerkverwaltung}
+ **Netzwerk:** Anwendung (z.B. Webbrowser) -> Socket API -> Netzwerkprotokolle (TCP/IP) -> Netzwerk-Treiber -> Netzwerkgerät
