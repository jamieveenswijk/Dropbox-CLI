# Dropbox-CLI
Documentation about the Dropbox CLI for Linux Servers

# Dutch

### Documentatie Dropbox CLI


Nadat je bent ingelogd ga je naar /var/dropbox/Dropbox en typ je eerst "dropbox.py status"
om te checken of Dropbox up-to-date is. Voor een lijst met alle info over de beschikbare commands
typ je "dropbox.py ?"

Hier een lijst met de commands en hun waarden:


|Command       | Uitleg                                                                         |
|--------------|:------------------------------------------------------------------------------:|
|status        |  Verkrijg de huidige staat van Dropbox                                         |
|filestatus    |  Verkrijg de huidige synchronisatie status van de bestanden en mappen          |
|throttle      |  Zet een bandbreedte limiet                                                    |
|help          |   Zet dit voor een command en krijg uitgebreid uitleg                          |
|puburl        |   Verkrijg de publieke URL van een bestand in de public folder van Dropbox     |
|start         | Start het Dropbox proces                                                       |
|stop          |  Stopt het Dropbox proces                                                      |
|update        |  Werkt de huidige Dropbox bij naar een (eventuele) nieuwere versie             |
|proxy         |  Zie proxy instellingen                                                        |
|autostart     |  Start automatisch Dropbox met login, dit wordt alleen ondersteunt bij Ubuntu distro's momenteel |
|exclude       |  Ignores / excludes mappen van synchronisatie                                  |
|lansync       |  Enables LAN sync (staat op enabled by default)                                |
|sharelink     | Krijg een gedeelde link van een bestand in Dropbox                             |
|ls            |  Weergeeft alle mappen en bestanden met hun huidige synchronisatie status      |

// Extra note

Elke command is best straightforward behalve de "exclude" command. Met de "exclude" command
kun je mappen toevoegen of verwijderen van de exclude list.


dropbox exclude add [DIRECTORY] [DIRECTORY] ... : Voegt een map toe aan de exclude list

dropbox exclude remove [DIRECTORY] [DIRECTORY] ... : Verwijderd een map uit de exclude list


Voordat je de exclude command gebruikt is het verstandig om eerst "dropbox.py exclude list" te
gebruiken om te zien welke mappen al aanwezig zijn in de lijst.


als je alles wilt verwijderen van de huidige synchronisatie dan kun je de
"dropbox.py exclude add *" command gebruiken. Doormiddel van het gebruik van een Wildcard (*)
kun je alles selecteren. Dit kun je ook toepassen bij andere commands.

