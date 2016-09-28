Privacy policy
==============

This is the privacy policy for the kontalk.net network (the default network clients will connect to).

Phone numbers
=============
The real phone number of the user must be provided during the registration phase because it needs to be verified through a SMS or a phone call by providing some challenge code (e.g. a PIN) that the user must supply back to the server. We don't store the phone number in any way, however our verification providers (namely Nexmo and CheckMobi) do keep a record of all verified phone numbers for some time. We access those logs only when supporting users having issues during registration.

Phone numbers in the messaging protocol itself are exchanged in an irreversible hashed form (SHA-1), hiding the real phone number from the most basic attack. However, recent technological development made possible brute-force attacks that can be used to reverse a hash in a matter of hours.

Contacts matching
=================
When a contact refresh is triggered, all phone numbers stored in the user's address book are hashed and sent to the server. The hashed phone numbers are used to look for other registered users in the network and then discarded.

Buddy list
==========
Chat invitation and blocked status lists are stored on the user's server roster.

Encryption keys
===============
Public keys are stored on the servers. Public key access is allowed to a user if the requested user has accepted the chat invitation.

Private keys are stored in the client device and in the device only. You can choose to export it to a zip file that can be moved to another device for backup or import. Although the keys in the zip file are encrypted, we recommend to minimize movements through the wire at the minimum possible.

Crash reporting/Analytics
=========================
The Google Play version of the Android app uses Fabric ([Crashlytics](https://try.crashlytics.com/terms/)+[Answers](https://answers.io/privacy)) to collect statistical data from the app usage and automatic reports of crashes. Information sent with crash reports includes:

* Exception stacktrace
* App version
* Device brand and model
* Android version

A user preference in the app will allow the user to opt-out.
