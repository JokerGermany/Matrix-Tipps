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
1. Activate Threads ([e.g in Element](https://user-images.githubusercontent.com/30293477/169691217-7be8bd74-e9c1-4c9c-9ee4-7e2f838f162d.png))   
or
2. Use the Answer function. Then your messages will appear in the threads, too.

## How to activate Labor in Element.
Certain options in labor didn't show up when certain config files aren't edited.  
You have to edit the config.json   
-    %APPDATA%\$NAME\config.json on Windows  
-    $XDG_CONFIG_HOME\$NAME\config.json or ~/.config/$NAME/config.json or Flatpak: ~/.var/app/im.riot.Riot/config/$NAME/config.json on Linux  
-    ~/Library/Application Support/$NAME/config.json on macOS  
$Name is Element, if you use a profilename its Element-<$Profilename>

Insert this in the file:
```
{
	"showLabsSettings": true
}
```
(If the file don't exists, create it)

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
1. Aktiviere Threads ([e.g in Element](https://user-images.githubusercontent.com/30293477/169691217-7be8bd74-e9c1-4c9c-9ee4-7e2f838f162d.png))   
oder
2. Nutze die Antwort funktion auf die Beiträge, damit deine Nachrichten auch in den Threads erscheinen.

### Wie man Threads in Element aktiviert
![grafik](https://user-images.githubusercontent.com/30293477/169691217-7be8bd74-e9c1-4c9c-9ee4-7e2f838f162d.png)

## Wie man Labor in Element freischaltet:
Viele Optionen tauchen im Labor Menü nicht auf, wenn man sie nicht freischaltet.
Es muss die config. json bearbeitet werden
-    %APPDATA%\$NAME\config.json unter Windows  
-    $XDG_CONFIG_HOME\$NAME\config.json oder ~/.config/$NAME/config.json oder Flatpak: ~/.var/app/im.riot.Riot/config/$NAME/config.json unter Linux  
-    ~/Library/Application Support/$NAME/config.json unter macOS  
$Name sollte in der Regel Element sein. Wird ein Profilname genutzt ist es Element-<$Profilename>

In die Datei folgendes einfügen:
```
{
	"showLabsSettings": true
}
```
(Ist die Datei nicht vorhanden, einfach erstellen.)
