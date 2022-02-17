# VirtualSpace

Das Chaosdorf existiert auch im virtuellen Raum!

Damit unsere Treffen auch während einer Corona Pandemie stattfinden können, treffen wir uns online. Um die verschiedenen Räume des Hackspaces abzubilden, gibt es ebenso mehrere Räume virtuell (als Video-Meetings).

Wir nutzen dazu die Plattform Jitsi. Klicke auf einen der Links, um den jeweiligen Raum zu betreten. Du gelangst dann zu einer Seite mit weiteren Anweisungen.

Bitte beachte unsere Jitsiquette! Nach dem Lesen wird dir unser geheimes Passwort bekannt sein. Es lautet raumstation.

## Räume

### Lounge

Die Lounge ist der allgemeine Treffpunkt zum Ankommen, Quatschen und Kennenlernen. Wenn du Jitsi ausprobieren willst, komm hier rein!

- [Virtual Lounge](https://virtual.chaosdorf.space/Lounge)
- [Virtual Lounge](https://meet.ffmuc.net/Lounge) - Backup bei Freifunk Server Ausfall

### Hackcenter

Im Hackcenter finden die Gruppentreffen statt, also alle Veranstaltungen wie sie im Kalender stehen. Darauf gibt es keine Garantie, also frage bitte in deiner Gruppe nach.

- [Virtual Hackcenter](https://virtual.chaosdorf.space/Hackcenter)
- [Virtual Hackcenter](https://meet.ffmuc.net/Hackcenter) - Backup bei Freifunk Server Ausfall

### Cave

Die Cave ist das Hinterzimmer für ausgelagerte Gespräche. Hier ist meistens nix los; aber wenn in den anderen Räumen zu viel los ist, verlagert euer Gespräch doch einfach mal hier hin.

- [Virtual Cave](https://virtual.chaosdorf.space/Cave)
- [Virtual Cave](https://meet.ffmuc.net/Cave) - Backup bei Freifunk Server Ausfall

### Backup

Falls mal der Jitsi-Server ausfällt, finden wir uns manchmal in [diesem Raum](https://meet.ffmuc.net/Freitagsfoo), [diesem](https://meet.ffmuc.net/Lounge) oder [diesem](https://meet.ffmuc.net/Hackcenter) auf einem anderen Server wieder. Aktuelle Infos gibt es ggf. auch in unserem Telegram-Channel.

## Wie ihr euren eigenen Jitsi Server aufsetzen könnt

In Zeiten wie diesen kann es nicht genug (dezentrale) Videochat-Infrastruktur geben, um trotz Corona ungefährdet soziale Kontakte pflegen zu können. Wenn ihr also evtl. noch ungenutze Serverkapazitäten rumstehen habt, könnt ihr relativ leicht eigene Jitsi Server aufsetzen.

Das Jitsi Projekt empfiehlt zwar nach der [Quick-Install](https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-quickstart) Anleitung vorzugehen, einzelne Konfigurationsaspekte sind dort allerdings zu ungenau oder missverständlich beschrieben. So hatten wir z.B. das Problem, dass zwei Prozesse den gleichen Port nutzten. Hier lohnt sich ein Blick in die [Manual-Install](https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-manual) Anleitung. Dort findet ihr eine Übersichtsgrafik, mit welchem Port-Setup die einzelnen Komponenten am besten miteinander kommunizieren.

Ein weitere Ansatz ist die Installation mittels Docker. Eine Anleitung hierfür findet ihr z.B. auf [golem.de](https://www.golem.de/news/homeoffice-videokonferenzen-auf-eigenen-servern-mit-jitsi-meet-2003-147239.html).
