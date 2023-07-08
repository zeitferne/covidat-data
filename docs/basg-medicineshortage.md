# Vertriebseinschränkungen von Medikamenten (BASG)

Daten: [`data/basg-medicineshortage`](../data/basg-medicineshortage/)


Übersicht bei <https://www.basg.gv.at/marktbeobachtung/meldewesen/vertriebseinschraenkungen>.

Die `Vertriebseinschraenkungen_*.xlsx`-Dateien stammen von
<https://medicineshortage.basg.gv.at/vertriebseinschraenkungen>, die xml-Dateien
von <https://www.basg.gv.at/fileadmin/uploadVERE/VertriebseinschraenkungenASP.xml>
(via https://www.basg.gv.at/fuer-unternehmen/datenbereitstellung-vertriebseinschraenkungen).
Die URL <https://webservices.basg.gv.at/medicineshortage/export/v1/download>
wurde nicht verwendet da sie die selbe Datei wie die vorherige URL auszuliefern
scheint aber die HTTP Header Last-Modified/If-Modified-Since nicht unterstützt.

Die xlsx-Dateien sind teilweise mit unterschiedliche Verfügbarkeitsfiltern und
Spalten heruntergeladen. Weitere Aktualisierung ist nicht geplant, obwohl die
xslsx-Daten die Spalte "Verwendung" (Human/Veterinär) haben die in den
xml-Dateien fehlt. Diese Information ist jedoch über Verknüpfung mit dem
[Arzneispezialitätenregister](https://aspregister.basg.gv.at/) über die
Zulassungsnummer verfügbar. Zu beachten ist dabei:

* Die `EU/*`-Zulassungsnummern sind häufig keine Einzelnummern sondern
  Bereichsangaben, insbesondere wenn `-` oder `,` vorkommt. Die Bereichsangaben
  unterscheiden sich zwischen Vertriebseinschränkungsregister und ASP-Register
  manchmal leicht. Bei nicht auffindbare Medikamenten kann z.B. mit der
  Regular Expression `[-,][^/]+$` die Bereichsangabe aus der Zulassungsnummer
  entfernt bzw. auf den Bereichsanfang normalisiert werden.
* Vereinzelt fehlen Medikamente im ASP-Register, vermutlich großteils weil sie
  aus der aktuellen Version herausgefallen sind. Das Medikament muss dann
  händisch recherchiert werden, aber bisher waren es immer Human-Medikamente
  sofern nicht schon aus der Bezeichnung offensichtlich ist dass es sich um
  ein veterinär-Medikament handelt.

  `ASP-Missing.csv` enthält nicht-originale Daten mit der Verwendung dieser
  fehlenden Medikamente. Alle Angaben natürlich völlig ohne Gewähr.

Snapshots des [Arzneispezialitätenregisters](https://aspregister.basg.gv.at/)
(derzeit ein einziger) sind in `ASP-Register_*.xlsx` enthalten.
