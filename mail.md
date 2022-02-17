# Mail

## Mail-Programme einrichten

Am besten einen IMAP-Account einrichten und als Eingangs- und Versand-/SMTP-Server **intern.chaosdorf.de** eingeben.
Alternativ zu IMAP geht auch Mail-Abholung via POP3 über den gleichen Server.

In jedem Fall wird Verschlüsselung vorausgesetzt. Einzelheiten:

- Der Username muss ohne Domain angegeben werden.
- Für IMAP nutzen wir SSL/TLS über Port 993. Authentifizierung ist PLAIN bzw. Einfach (heißt je nach Client ggf. etwas anders).
- Zum Versand via SMTP muss man sich mit Nutzernamen und Kennwort authentifizieren (wieder PLAIN bzw. Einfach). Als Verschlüsselungstyp (Start-)TLS über Port 587.
- Bei POP3 nimmt man SSL-Verschlüsselung über Port 995.

## Details zum Mail-Empfang

- der Server akzeptiert ankommende Mails an user@chaosdorf.de und user@duesseldorf.ccc.de
- wenn der einliefernde Client '[postscreen](http://www.postfix.org/POSTSCREEN_README.html)', diverse DNS-Blacklists und einige Konformitätschecks überlebt hat, wird die Mail ins Maildir von Dovecot einsortiert (und evtl. vorher noch vom SpamAssassin als Spam markiert; einen Virenfilter gibt es nicht)
- Zugriff von außen und von shells ist nur verschlüsselt via IMAPS (Port 993) und POP3S (995) möglich
- unsere lokalen [Mailinglisten](https://intern.chaosdorf.de/sympa/) kann man über den "List-Id"-Header filtern
- eigene [Sieve](http://de.wikipedia.org/wiki/Sieve)-Filter kann man mittels ManageSieve bearbeiten:
  - A) `sieve-connect -s intern.chaosdorf.de`, eigenes Passwort eingeben, `help`
  - B) "Einstellungen > Filter" im Roundcube
  - C) einige GUI-Mailclients unterstützen ebenfalls ManageSieve, z.B. KMail oder Claws (Plugin)
Falls ihr im LDAP eine externe Mail-Adresse eingetragen habt (s.u.), werden alle eingehenden Mails (auch die an intern@ und andere Mailinglisten) an diese weitergeleitet.

## Details zum Mail-Versand

- der Server führt auch beim Versenden ein paar grundlegende Tests durch (z.B. dass Empfänger- und Absenderdomain existieren), der Spam-Filter wird aber umgangen
- von shells aus muss man sich nicht authentifizieren, von außerhalb ist SMTP-AUTH aber Pflicht; es wird AUTH PLAIN auf Port 465 (SSL) und 587 (STARTTLS) unterstützt
- es darf mit beliebigen (vorzugsweise eigenen) Adressen relayt werden
- Bei Speedport Routern kann es zu Problemen im Versand kommen, auf Grund von einer "Liste der sicheren E-Mail-Server", Lösung: einfach intern.chaosdorf.de whitelisten.

## Mail-Weiterleitung

Falls im LDAP ('ldapme' auf shells ausführen) das Attribut "mailRoutingAddress" eingetragen ist, werden Mails an diese Adresse weitergeleitet. Andernfalls landen sie lokal auf dem Server und können per IMAP/POP3 gelesen werden, siehe oben.

Wenn ihr keine Weiterleitung wollt, muss die Zeile entfernt werden.

Wer keinen Shellzugang hat oder möchte, kann für Änderungswünsche auch einfach nachfragen (admin@, byte@, postmaster@ ... sucht euch was aus).

## Mailinglisten

- werden mit [Sympa](http://www.sympa.org/) verwaltet
- [https://intern.chaosdorf.de/sympa](https://intern.chaosdorf.de/sympa) bietet eine Übersicht aller lokalen Listen
- oben rechts kann man sich mit seinem üblichen LDAP-User einloggen
- für angemeldete User sind von den jeweils abonnierten Listen auch deren Archive zugänglich, also mindestens intern@, außerdem ist das mail@-Archiv für jedes Mitglied lesbar
- aktuell sind die Listen gamedev@ und pythonfoo@ auch für Externe nutzbar, der Rest ist auf Mitglieder beschränkt (und teilweise selbst abonnierbar)
- das Standard-Setup setzt Reply-To: Sender (falls nicht anders vom Absender festgelegt) und List-Post-Header, also sollte Reply-To-List in den gängigen Mailclients problemlos funktionieren (und im Regelfall benutzt werden)