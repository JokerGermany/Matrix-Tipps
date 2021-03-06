# Matrix-Tipps
This file will provide Tips for End-Users, if you want to use your own server, [i suppose this.](server-tips.md) 

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
3. In the “Event Type” text field, write this: im.vector.modular.widgets
4. In the “State Key” text field, write this: dimension-jitsi-1622722886114
5. In Event Content (German: Event Inhalt) insert the following:
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


## Deutsch
### Wie reagiere ich auf Threads
1. Aktiviere Threads ([e.g in Element](https://user-images.githubusercontent.com/30293477/169691217-7be8bd74-e9c1-4c9c-9ee4-7e2f838f162d.png))   
oder
2. Nutze die Antwort funktion auf die Beiträge, damit deine Nachrichten auch in den Threads erscheinen.

### Wie man Threads in Element aktiviert
![grafik](https://user-images.githubusercontent.com/30293477/169691217-7be8bd74-e9c1-4c9c-9ee4-7e2f838f162d.png)
