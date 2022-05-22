# Matrix-Tipps
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

## [Matrix Server](server-tips.md) 
