# Auth

Diese Merkmale sind für sämtliche Chaosdorf-Dienste gleich (sie liegen im LDAP auf backend.chaosdorf.de).

## Username[edit | edit source]

Überall gleich

## Passwort

Für Webmail, Wiki, Website etc.

Ändern: Entweder auf shells.chaosdorf.de per SSH einloggen und **passwd** ausführen oder das [changeme](https://intern.chaosdorf.de/cgi-bin/changeme.cgi) benutzen

## SSH-Keys

Für shells.chaosdorf.de, SFTP auf extern.chaosdorf.de und Zugriff auf git@intern.chaosdorf.de.

Ändern: shells.chaosdorf.de: `ldapme` ausführen. Es können beliebig viele SSH-Keys eingetragen werden, sie müssen nur jeweils `sshPublickey:` als Prefix haben.

Bitte beachten: Es kann bis zu 5 Minuten dauern, bis diese Änderungen auf den Hosts angekommen sind.

Falls du Neumitglied bist (d.h. noch keinen SSH-Key auf shells eingetragen hast): Mail an [admin@chaosdorf.de](mailto:admin@chaosdorf.de) und/oder byte / derf im Clubraum ansprechen.

## Mail-Adresse

Siehe Mail

Ändern: auf shells.chaosdorf.de `ldapme` ausführen und das Feld `mailRoutingAddress` entsprechend setzen.

## LoginShell

Um deine loginshell zu ändern musst du auf shells.chaosdorf.de "ldapme" ausführen und den entsprechenden Eintrag anpassen.

Anmerkung: Ein Ändern über chsh scheint nicht möglich.