Space with Rooms about Matrix which are not in [#community:matrix.org](https://matrix.to/#/#community:matrix.org):  
[![#free-messengers:matrix.org](https://img.shields.io/matrix/free-messengers:matrix.org.svg?label=%23free-messengers:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#free-messengers:matrix.org) 
## Send custom reactions in Element to messages 
1. Chat /devtools
2. Send Custom Event
3. 
Event Type: `m.reaction`
Event Content: 
```{
    "m.relates_to": {
        "rel_type": "m.annotation",
        "event_id": "$164569109460761pvPSY:matrix.org",
        "key": "BOMP!"
    }
}
```
[Source](https://www.natrius.eu/dokuwiki/doku.php?id=digital:server:matrixsynapsemisc&s%5B%5D=reaction#send_custom_reactions_to_messages)

## Tombstone
1. Chat /devtools
2. Explore room state
2. Send custom state event
3. 
Event Type: `m.room.tombstone`  
State Key: let it empty  
Event Content: 
```
{
    "body": "This room has been replaced",
    "replacement_room": "!ERZvriGbDxJDxaCBxX:matrix.org"
}
```
[Source](https://www.natrius.eu/dokuwiki/doku.php?id=digital:server:matrixsynapsemisc&s%5B%5D=reaction#tombstone_event)


## Add Jitsi Widget with a custom url to the room
1. Chat /devtools
2. Click on explore room status (german: "Roomstatus erkunden")
3. Send Custom Event (german: "Benutzerdefiniertes Status-Event senden")
4. In the “Event Type” text field, write this: im.vector.modular.widgets
5. In the “State Key” text field, write this: dimension-jitsi-1622722886114
6. In Event Content (German: Event Inhalt) insert the following:
```
{
 "type": "jitsi",
 "url": "https://dimension.opensuse.org/widgets/jitsi?conferenceId=$conferenceId&domain=$domain&isAudioOnly=$isAudioOnly&displayName=$matrix_display_name&avatarUrl=$matrix_avatar_url&userId=$matrix_user_id",
 "name": "Jitsi Video Conference",
 "data": {
     "conferenceUrl": "<jitsi instance>/<jitsi room>",
     "domain": "<jitsi instance>",
     "conferenceId": "<jitsi room>",
     "isAudioOnly": false,
     "url": "https://dimension.opensuse.org/widgets/jitsi?conferenceId=$conferenceId&domain=$domain&isAudioOnly=$isAudioOnly&displayName=$matrix_display_name&avatarUrl=$matrix_avatar_url&userId=$matrix_user_id",
     "dimension:app:metadata": {
         "wrapperUrlBase": "",
         "wrapperId": "",
         "scalarWrapperId": null,
         "integration": {
             "category": "widget",
             "type": "jitsi"
         }
     }
 },
 "id": "dimension-jitsi-1622722886114"
}
```
> Replace <jitsi instance> with the URL of the Jitsi Server, e.g. https://meet.opensuse.org and replace <jitsi room> with the name of the Jitsi room, e.g. bar A working example looks like this (it links to the openSUSE Bar):
```
{
 "type": "jitsi",
 "url": "https://dimension.opensuse.org/widgets/jitsi?conferenceId=$conferenceId&domain=$domain&isAudioOnly=$isAudioOnly&displayName=$matrix_display_name&avatarUrl=$matrix_avatar_url&userId=$matrix_user_id",
 "name": "Jitsi Video Conference",
 "data": {
     "conferenceUrl": "https://meet.opensuse.org/bar",
     "domain": "meet.opensuse.org",
     "conferenceId": "bar",
     "isAudioOnly": false,
     "url": "https://dimension.opensuse.org/widgets/jitsi?conferenceId=$conferenceId&domain=$domain&isAudioOnly=$isAudioOnly&displayName=$matrix_display_name&avatarUrl=$matrix_avatar_url&userId=$matrix_user_id",
     "dimension:app:metadata": {
         "wrapperUrlBase": "",
         "wrapperId": "",
         "scalarWrapperId": null,
         "integration": {
             "category": "widget",
             "type": "jitsi"
         }
     }
 },
 "id": "dimension-jitsi-1622722886114"
}
```
[Source](https://blog.karatek.net/2021/06/09/jitsi-bar-magic/)

## How to react on Threads?
If your Matrix Client don't support Threads, use the Answer function. Then your messages will appear in the threads, too.

## How to activate Labs on Element
Certain options in labor didn't show up when certain config files aren't edited.  
You have to edit the config.json   
-    `%APPDATA%\$NAME\config.json` on Windows  
-    `$XDG_CONFIG_HOME\$NAME\config.json` or `~/.config/$NAME/config.json` or Flatpak: `~/.var/app/im.riot.Riot/config/$NAME/config.json` on Linux  
-    `~/Library/Application Support/$NAME/config.json` on macOS  
$Name is `Element`, if you use a profilename its `Element-<$Profilename>`

Insert this in the file:
```
{
	"show_labs_settings": true
}
```
(If the file don't exists, create it)
## How to join a Room with a room alias
If you have a Room alias and want to join this room, you have to insert it in the public room search.
![JoinRoom1](img/EN-JoinRoom1.png)  
If the Room was found in the Room directory the search result states as following:  
![JoinRoom2](img/EN-JoinRoom2.png)  
If the Room was not found in the Room directory the search result states as following:  
![JoinRoom3](img/EN-JoinRoom3.png)  
In both cases you can join the Room.

## Sliding Sync Urls
matrix.org: https://slidingsync.lab.matrix.org  
tchncs.de: https://syncv3.matrix.tchncs.de

## Deutsch
Matrix Raum für "einfache" Fragen:  
[![Matrix Raum für "einfache" Fragen: #matrix-support-de:matrix.org](https://img.shields.io/matrix/matrix-support-de:matrix.org.svg?label=%23matrix-support-de:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#matrix-support-de:matrix.org)  
Matrix Raum für fortgeschrittene Fragen:  
[![Matrix Raum für fortgeschrittene Fragen: #matrixgeeks:matrix.org](https://img.shields.io/matrix/matrixgeeks:matrix.org.svg?label=%23matrixgeeks:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#matrixgeeks:matrix.org)  
Matrix Raum über Messenger Allgemein:  
[![Matrix Raum über Messenger Allgemein: #messenger-de:matrix.org](https://img.shields.io/matrix/messenger-de:matrix.org.svg?label=%23messenger-de:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#messenger-de:matrix.org)  
Space wo die genannten Räume enthalten sind:  
[![#freie-messenger-space:matrix.org](https://img.shields.io/matrix/freie-messenger-space:matrix.org.svg?label=%23freie-messenger-space:matrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#freie-messenger-space:matrix.org) 
### Wie reagiere ich auf Threads
Wenn dein Matrix-Client Threads nicht unterstützt, nutze die Antwort funktion auf die Beiträge, damit deine Nachrichten auch in den Threads erscheinen.

### Wie man Labor in Element freischaltet:
Viele Optionen tauchen im Labor Menü nicht auf, wenn man sie nicht freischaltet.
Es muss die config. json bearbeitet werden
-    `%APPDATA%\$NAME\config.json` unter Windows  
-    `$XDG_CONFIG_HOME\$NAME\config.json` oder `~/.config/$NAME/config.json` oder Flatpak: `~/.var/app/im.riot.Riot/config/$NAME/config.json` unter Linux  
-    `~/Library/Application Support/$NAME/config.json` unter macOS  
$Name sollte in der Regel `Element` sein. Wird ein Profilname genutzt ist es `Element-<$Profilename>`

In die Datei folgendes einfügen:
```
{
	"show_labs_settings": true
}
```
(Ist die Datei nicht vorhanden, einfach erstellen.)

### Wie man einen Raum mithilfe des Raum Alias beitritt
Wenn man den Raum Alias weiß, dann kann man dem Raum beitreten indem man den Raum alias in der Raum suche eingibt.
![JoinRoom1](img/DE-JoinRoom1.png)  
Wenn der Raum in der Raumsuche gefunden wurde, sieht es so aus:  
![JoinRoom2](img/DE-JoinRoom2.png)  
Wenn der Raum nicht in der Raumsuche gefunden wurde, sieht es so aus:__
![JoinRoom3](img/DE-JoinRoom3.png)  
In beiden Fällen kann man dem Raum beitreten!

### Draupnir/mjolnir die korrekten Rechte geben
Es gibt zwei verschiedene Möglichkeiten wie vorgegangen werden kann:  
1. Dem Bot Admin Rechte geben.  
Vorgehensweise hierbei ist einfach:  
Draupnir/Mjolnir einladen und Admin Rechte geben.  
Nachteil ist, dass dem Bot die dadurch die höchstmöglichen Berechtigungen gegeben werden und somit kein anderer Mjolnir/Draupnir herabstufen oder kicken kann.

2. Dem Bot Moderator Rechte geben.

Vorgehensweise:  
1. Die Raumberechtigung für *Server-ACLs bearbeiten* auf Moderator stellen
<details>
  <summary>Element Web/Desktop</summary>
  
![](https://user-images.githubusercontent.com/30293477/233482127-c8ce7797-48a8-43a8-8746-386928bab39a.png)
  
</details>
<details>
  <summary>Schildichat Android</summary>
  
![ModBot1](https://user-images.githubusercontent.com/30293477/233576913-745e914b-291d-4e0e-a4fe-35fb6216de7a.png)


![Modbot2](https://user-images.githubusercontent.com/30293477/233576937-13e0467f-7dda-4c7e-a11e-c9ecb8225768.png)


![Modbot3](https://user-images.githubusercontent.com/30293477/233576952-b1907f2c-38a9-458f-90c4-4a5e551b6a7a.png)

</details>
2. mjolnir/draupnir einladen
3. mjolnir/draupnir Moderator Rechte geben.
