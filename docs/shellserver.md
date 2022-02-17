# Shellserver

Sobald ihr einen SSH-Key im LDAP habt, könnt ihr euch damit auf **shells.chaosdorf.de** ([Hostkey](https://www.chaosdorf.de/chaosdorf-keys.asc)) einloggen.

Falls euer Account noch frisch ist und keinen SSH-Key eingetragen hat, schickt einfach eine Mail mit eurem Publickey an <admin@chaosdorf.de> und wir kümmern uns drum.


## Usage Policy

Nichts illegales tun, ansonsten im Zweifelsfall den Admin fragen.

Für Netzwerkdienste können die TCP-Ports 50000 bis 51000 verwendet werden, andere Ports sind extern nicht erreichbar. Für [mosh](http://mosh.mit.edu/) werden zusätzlich die UDP-Ports 60000 bis 61000 durchgelassen.

## Software

Falls welche fehlt: Admins kontaktieren; die Chancen, daß sie installiert wird, sind sehr hoch.

## Quotas

Es gelten Disk-Quotas, d.h. es kann nur eine bestimmte Menge Festplattenspeicherplatz verbraucht werden.

Das Soft-Quota liegt bei 512MB und produziert bei Überschreiten eine Mail an die Admins sowie folgende Warnung: "warning, user block quota exceeded". Der Shellaccount kann dabei ganz normal weiter benutzt werden, wird jedoch das Hard-Quota von 768MB erreicht, sind keinerlei Schreiboperationen mehr möglich (das merkt man an Meldungen wie "write failed, user block limit reached").

## Limits

In /etc/security/limits.conf sind diverse Limits für Speichernutzung, Anzahl der Prozesse etc. festgelegt. Diese lassen sich mit Shell-spezifischen Builtins (zsh: 'limit', bash: 'ulimit') anschauen und im vom Administrator vorgesehenen Rahmen erhöhen; siehe auch 'man 5 limits.conf'.