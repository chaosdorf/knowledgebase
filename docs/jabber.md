# Jabber

Auf extern läuft ein prosody. Registrierung ist aus Ressourcengründen aus, Accounts für Mitglieder werden auf Anfrage angelegt. Im Gegensatz zu anderen Diensten ist der Jabberserver derzeit nicht an unser LDAP angebunden.

## Für User

### Account anlegen

- Mail mit "Ohai, ich hätte gerne nen Account" an [admin@chaosdorf.de](mailto:admin@chaosdorf.de) (wir verwenden standardmäßig den im LDAP eingetragenen Nickname, d.h. **Mail-Adresse und Jabber-ID sind gleich**)
- Der Account wird mit einem temporären Passwort angelegt, das per Mail zurückkommt (hier ist es hilfreich, wenn wir wissen, mit welchen PGP-Key die Mail verschlüsselt werden soll)
- Mit einem Jabberclient der Wahl verbinden und das Passwort auf ein eigenes ändern

## Administration

### Account anlegen

```
fab jabber-adduser nickname
```

Das dort angegebene generierte Passwort in die zwei Passwort-Abfragen von prosody pasten und der zugehörigen Person mitteilen.