This file is work in progress

Datenschutz-Bestimmungen
==============

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

Phone numbers in the messaging protocol itself are exchanged in an irreversible
hashed form (SHA-1), hiding the real phone number from the most basic attack.
However, recent technological development made possible brute-force attacks that
can be used to reverse a hash in a matter of hours.

Telefonnummern im Messaging-Protokoll selbst werden ausschließsich in gehashter Form (SHA-1) verwendet
Die echte Telefonnummer wird vor den meisten grundlegenden Angriffen versteckt.
Allerdings ist es beim aktuellen technischen Stand möglich mittels Brute-Force-Angriffen den 
originalen Wert (Telefonnumer) innerhalb von Stunden aus dem Hash-Wert zu errechnen.

Contacts matching
=================
When a contact refresh is triggered, all phone numbers stored in the user's
address book are hashed and sent to the server. The hashed phone numbers are
used to look for other registered users in the network and then discarded.

Buddy list
==========
Chat invitation and blocked status lists are stored on the user's server roster.

Encryption keys
===============
Public keys are stored on the servers. Public key access is allowed to a user if
the requested user has accepted the chat invitation.

Private keys are stored in the client device and in the device only. You can
choose to export it to a zip file that can be moved to another device for backup
or import. Although the keys in the zip file are encrypted, we recommend to
minimize movements through the wire at the minimum possible.

Messages
========
Messages are stored on the recipient's server until they are delivered and
acknowledged by the recipient's client. After correct delivery, messages are
deleted immediately and permanently.

User data removal
==================
All user data will be automatically deleted from the server if the user doesn't
access the service for 30 days.

Server logs
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
