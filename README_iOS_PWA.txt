CREMERCE – iOS-PWA
==================

Inhalt
------
- index.html: CREMERCE-App
- manifest.webmanifest: App-Name, Farben und Icons
- service-worker.js: Offline-Cache und Aktualisierung
- offline.html: verständliche Offline-Seite
- icons/: Icons für iPhone, iPad und andere Geräte
- docs/: Importvorlage und direkt nutzbare Beispieldaten

Beim Hochladen bitte die vorhandenen Dateien auf dem Webspace durch den gesamten
neuen Inhalt des ZIPs ersetzen. Einzelne Icon-Dateien allein reichen nicht,
weil HTML, Manifest und Offline-Cache gemeinsam aktualisiert wurden.

Wichtig
-------
Eine PWA benötigt HTTPS. Das direkte Öffnen der index.html aus dem ZIP-Ordner
reicht für Service Worker und iOS-Installation nicht. Den vollständigen Inhalt
des ZIPs auf dem HTTPS-Webspace veröffentlichen.

Installation auf iPhone oder iPad
---------------------------------
1. Falls CREMERCE bereits auf dem Home-Bildschirm liegt: das alte Symbol zuerst
   vom Home-Bildschirm entfernen. iOS speichert Home-Screen-Icons sehr lange.
2. Den vollständigen Inhalt des ZIPs im Repository-Hauptverzeichnis veröffentlichen.
3. Die veröffentlichte CREMERCE-Adresse in Safari öffnen und einmal neu laden.
4. Auf "Teilen" tippen.
5. "Zum Home-Bildschirm" auswählen.
6. Mit "Hinzufügen" bestätigen.

Falls weiterhin das alte Symbol erscheint
------------------------------------------
- Prüfen, ob wirklich die neue Datei apple-touch-icon.png direkt im
  Hauptverzeichnis unter /CREMERCE2/apple-touch-icon.png erreichbar ist.
- Den alten Home-Bildschirm-Eintrag erneut löschen, Safari schließen, die Seite
  wieder in Safari öffnen und neu hinzufügen.
- Notfalls nur die Websitedaten der veröffentlichten Domain in den iOS-
  Einstellungen löschen und anschließend erneut hinzufügen.

Enthaltene Apple-Icons
----------------------
- 120 x 120 px: ältere/kleinere iPhones
- 152 x 152 px: iPad
- 167 x 167 px: iPad Pro
- 180 x 180 px: aktuelle iPhones

Alle Apple-Icons sind quadratisch, vollflächig und ohne transparente Ecken.
Die Versionskennung "v20" verhindert, dass Safari die frühere Icon-Datei
weiterverwendet. Das iPhone rundet die Ecken beim Hinzufügen automatisch ab.

Browser und Desktop
-------------------
- favicon.ico enthält die Standardgrößen für Browser und Windows.
- PNG-Varianten in 16, 32 und 48 px versorgen Browser-Tabs und Lesezeichen.
- Das sichtbare Logo ist direkt in index.html eingebettet; logo.png liegt
  zusätzlich als separat verwendbare Datei bei.
- icon-192.png, icon-512.png und icon-maskable-512.png versorgen die PWA.
- icon-1024.png ist die hochauflösende App-Icon-Version.
- Nach dem Veröffentlichen alte Browser-Lesezeichen oder Desktop-Verknüpfungen
  einmal löschen und neu anlegen, damit deren alter Icon-Cache ersetzt wird.

Datenübernahme
--------------
Die Datei docs/CREMERCE_Importvorlage.csv kann in Excel bearbeitet werden.
Sie verwendet dieselben Feldnamen wie der Export in CREMERCE. Deshalb kann
eine exportierte CSV später ohne Spaltenumbau wieder importiert werden.

Beim Import gilt Marke + Asset-ID als eindeutige Kombination:
- bereits vorhanden: Datensatz wird aktualisiert
- noch nicht vorhanden: Datensatz wird ergänzt

Der HTML-Prototyp speichert Datensätze lokal auf dem jeweiligen Gerät.
Für einen gemeinsamen Echtbetrieb werden Backend, Anmeldung, Rollen,
zentrale Datenbank, Backups und serverseitige TikTok-Verbindungen benötigt.

Finales Oberflächendesign
-------------------------
- Vollständig umschaltbarer Light- und Dark-Mode
- Kombinierte Balken-/Liniendiagramme mit sichtbaren Datenpunkten
- Leuchtendere Analysefarben im Dark-Mode
- Kategorienbasierte Creator-Farben für skalierbare Listen
- Responsive Darstellung für Desktop, Tablet und Smartphone
