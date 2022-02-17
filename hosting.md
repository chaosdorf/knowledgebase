# Hosting

Ihr könnt unter `chaosdorf.de/~username` eure eigene Website betreiben.

Der Inhalt kann per SFTP auf extern.chaosdorf.de hochgeladen werden, z.B. mit

```
lftp sftp://extern.chaosdorf.de/
```

Für die Anmeldung ist genau wie bei shells.chaosdorf.de dein SSH-Key erforderlich, siehe [Auth](./auth.md).

Im Vezeichnis /public_html/ kannst Du dann Deine Seite anlegen.

Falls es Zugriffsprobleme gibt liegt es meist an den Dateiberechtigungen, siehe auch chmod.

Wie auf dem Shellserver gelten hier Quotas, 512MB Soft und 768MB Hard.

## Kleines Howto zu lftp

so meldet man sich an:

```
lftp sftp://extern.chaosdorf.de/
```

(meist kommt noch eine Passwortabfrage, die man getrost mit Enter übergehen kann.)

der Login sieht dann z.B. so aus:

```
lftp oerb@extern.chaosdorf.de:/>
```

mit ls kann man sich den Inhalt des Verzeichnisses angeben lassen.

Beispiel:

```
drwxr-xr-x    3 0        1028         4096 Oct  1  2009 .
drwxr-xr-x    3 0        1028         4096 Oct  1  2009 ..
drwxr-xr-x    3 1026     1028         4096 Dec 11 16:12 public_html
```

mit cd wechselt man in das Hauptverzeichnis der Seite:

```
lftp oerb@extern.chaosdorf.de:/>cd public_html/
```

mit put kann man dann z.B. Dateien hochladen:

```
lftp oerb@extern.chaosdorf.de:/>put index.html
```

## Alternativen zu lftp

- [Filezilla](http://www.filezilla.de/)
- sftp
