This file is work in progress

Datenschutz-Bestimmungen
========================

Dies ist die Datenschutzrichtlinie für das öffentliche Kotalk-Netzwerk 
(das Standardnetzwerk mit dem sich die Clients verbinden).

Telefonnummern
==============
Die echte Telefonnummer des Benutzers muss während der Registrierungsphase angegeben werden
da sie verifiziert werden muss. Dies geschiet mittels eines Verifizierungs-Codes 
(z. B. eine PIN) der durch eine SMS oder einen Telefonanruf übermittelt wird und durch den Nutzer an 
den Server zurückgegeben wird.
Wir speichern Sie die Telefonnummer in keiner Weise (außer in Protokollen, siehe weiter unten).
Unsere Verifizierungsanbieter ([Nexmo] (https://www.nexmo.com/) und
[JMP.Chat] (https://jmp.chat/) lesen sie deren Datenschutzrichtlinien auf den
jeweiligen Webseiten), speichern aller verifizierten Telefonnummern für einige
Zeit. 
Wir greifen auf diese Protokolle nur zu, wenn bei der Registrierung von Benutzern Probleme auftreten.

Telefonnummern im Messaging-Protokoll selbst werden ausschließsich in gehashter Form (SHA-1) verwendet.
Die echte Telefonnummer wird vor den meisten grundlegenden Angriffen versteckt.
Allerdings ist es beim aktuellen technischen Stand möglich mittels eines Brute-Force-Angriffs den 
originalen Wert (Telefonnumer) innerhalb von Stunden aus dem Hash-Wert zu errechnen.

Kontakt-Abgleich
================
Wenn eine Kontaktaktualisierung ausgelöst wird, werden alle Telefonnummern im lokalen Adressnbuch gehasht und
an den Server gesendet. Die Hash-Werte der Telefonnummern werden verwendet um registrierte Kontalk-Nutzer zu finden
und werden anschließend wieder vom Server gelöscht.

Freunde-Liste
=============
Chat Einladungen und der Sperrstatus wird in einer Nutzerliste des Servers gespeichert.

Kryptologische Schlüssel
========================
Öffentliche Schlüssel werden auf dem Server gespeichert. Der Zugriff auf den öffentlichen Schlüssel ist
erst dann möglich wenn der angefragte Nutzer die Einladung angenommen hat.

Private Schlüssel werden ausschließlich auf dem Endgerät gespeichert.
Sie können mit der Exportfunktion ein Backup (zip-Datei) des Schlüssels erstellen welches auch auf einem
anderen Gerät importiert werden kann.
Obwohl die Schlüssel in der zip-Datei verschlüsselt sind empfehlen wir sehr vorsichtig damit zu sein.

Nachrichten
===========
Nachrichten werden auf dem Server des Empfängers gespeichert bis sie ausgeliefert und vom Client des
Empfängers bestätigt wurden. Nach der korrekten Übermittlung werden die Nachrichten sofort und entgültig
vom Server gelöscht.

Benutzerdaten entfernen
=======================
Alle Benutzerdaten werden automatisch gelöscht wenn der Nutzer seit 30 Tagen keinen Serverzugang hatte.
Z.B. nachdem die Kontalk App vom Gerät gelöscht wurde.

Server Logs
===========
Server instances keep a log of various operations happening inside the server,
including: IP addresses, phone number registration requests (including the phone
number itself), metadata of messages being exchanged (but not their content,
that is only from-to information and timestamps).

Logs are rotated every few hours and any information stored in the logs usually
goes away (rotated out, thus deleted) in a couple of days.

Crash reporting/Analytics (Android only)
========================================
The Google Play version of the Android app uses Fabric
([Crashlytics](https://try.crashlytics.com/terms/)+[Answers](https://answers.io/privacy))
to collect statistical data from the app usage and automatic reports of crashes.
Information sent with crash reports includes:

* Exception stacktrace
* App version
* Device brand and model
* Android version

A user preference in the app will allow the user to opt-out.
