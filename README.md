# covidat-data Datensammlung

Dieses Repository soll Rohdaten (so unbearbeitet wie sinnvoll) mit
Österreich-Bezug zu folgenden Gebieten sammeln:

1. COVID-19 / SARS-CoV-2 (Fälle, Tests, Verstorbene, Abwasser, etc.; dies ist
   das Kerngebiet des Repositories)
2. Sterbefälle allgemein (Wöchentliche Todesfälle, Todesursachenstatistik, etc.)
3. Gesundheitssystem & Gesundheit
4. Related relevant data such as job market data, etc.

Daten sollten generell aus öffentlichen und offiziellen Quellen stammen die
nicht länger abrufbar sind oder von denen anzunehmen ist, dass sie in Zukunft
nicht mehr länger (einfach) abrufbar sein werden (der Klassiker: Nur der
Datensatz des je aktuellsten Tages/Monats/Jahres steht zur Verfügung).

Siehe [CONTRIBUTING.md](./CONTRIBUTING.md) für mehr generelle Details die v.a.
interessant sind für die die beitragen (contributen) möchten.

Dieses Repository hat ein Schwester-Repository
[covidat-tools](https://github.com/zeitferne/covidat-tools)
das Werkzeuge, einen täglich ausgeführten Auto-Updater und
auch regelmäßig aktualisierte
[📊 Auswertungen](https://zeitferne.github.io/covidat-tools/export/monitoring.html)
enthält.

## Übersicht über enthaltene Daten

* COVID-19
  * [COVID-19 AGES und EMS-Daten](docs/covid/ages-und-ems.md): 📕 Fallzahlen, EMS-erfasste Todesfälle, Hospitalisierungen, Daten zu Tests
  * [Diverse weitere EMS-basierte AGES-Auswertungen](data/covid/ages-ems-extra/): 📕
    Reinfektionen (<https://www.ages.at/fileadmin/Corona/Reinfektionen/Reinfektionen.csv>),
    Inzidenz je Immunstatus (sehr unvollständiges Archiv, Original-URL TODO),
    R-Werte (<https://www.ages.at/fileadmin/Corona/Epidemiologische-Parameter/R_eff.csv>,
    bzw. früher <https://wissenaktuell.ages.at/fileadmin/AGES2015/Wissen-Aktuell/COVID19/R_eff.csv>).
  * [COVID-19 Morgenmeldungen](docs/covid/morgenmeldung.md): 📕 Erweiterte Daten zu Tests, alternative Facts zu Fallzahlen und Todesfällen
  * [Statistik Austria Covid-Tote lt. Pressemitteilung (immer vorl. Zahlen)](data/covid/statat_yearly_covid_deaths_pr.csv) (Aus:
    [2022](https://www.statistik.at/fileadmin/announcement/2023/03/20230315Todesursachen2022vorl.pdf),
    [2021](https://www.statistik.at/fileadmin/announcement/2022/05/20220303Todesursachen2021.pdf),
    [2020](https://www.statistik.at/web_de/presse/125475.html) (Web Archive!))
  * [Abwassermonitoring](data/covid/abwassermonitoring/): Archivierte Daten von
    <https://abwassermonitoring.at/dashboard/> bzw. früher <https://corona.hydro-it.com/dashboard/>.
  * ["Corona-Virus: Aktuelle Kennzahlen der Stadt Wien" Presseaussendungen](data/covid/wien-kennzahlen.tar.xz)
    via <https://presse.wien.gv.at/presse/>.
    HTML-only-Archiv, zus. Snapshots von <https://coronavirus.wien.gv.at/aktuelle-kennzahlen-aus-wien/>
    (offline, großteils redundant, enthält aber vereinzelt Tage für die es keine eigene Presseaussendungen gab)
  * ["Aktuelle Situation Covid-19 in OÖ" Landeskorrespondenzen](data/covid/ooe-landeskorrespondenz-cov-situation.tar.xz),
    via <https://www.land-oberoesterreich.gv.at/lksuche.htm>, zus. vereinzelt andere Landeskorrespondenzen mit CoV-Bezug.
  * [SARS-CoV-2-Variantenberichte der AGES](data/covid/ages-varianten/) via <https://www.ages.at/mensch/krankheit/krankheitserreger-von-a-bis-z/coronavirus>
    (im speziellen <https://www.ages.at/fileadmin/Corona/Wochenbericht/Varianten_Verteilung.csv> und <https://www.ages.at/fileadmin/Corona/Wochenbericht/Varianten_gesamt_KW.csv>)
  * [Sehr unvollständige Abschrift der Konsortiums-Prognosen für die KH-Normalstation](data/covid/cov-prognose-nst.csv);
    Format so gewählt dass man es durchs Kopieren vom PDF ins Excel erzeugen kann.
    Zuletzt via <https://datenplattform-covid.goeg.at/prognosen> davor <https://www.sozialministerium.at/Corona/zahlen-daten/COVID-Prognose-Konsortium-2022.html>,
    davor <https://www.sozialministerium.at/Corona/Coronavirus/COVID-Prognose-Konsortium-2022.html>, davor <https://www.sozialministerium.at/Informationen-zum-Coronavirus/COVID-Prognose-Konsortium.html>, davor <https://www.sozialministerium.at/Informationen-zum-Coronavirus/Neuartiges-Coronavirus-(2019-nCov)/COVID-Prognose-Konsortium.html> (jeweils ohne Redirect; Reihenfolge nach neuesten 2 ev. nicht akkurat)
* [Vertriebeinschränkungen bei Medikamenten](docs/basg-medicineshortage.md)
* [Monatsberichte der österr. Sozialversicherung](docs/sozialversicherung-monatsberichte.md)
* [Sterbefälle nach Todesursache, Kalenderjahre, Alter und tw. Bundesland](data/statat-todesursachen/).
  Aktuellste jeweils bei <https://www.statistik.at/statistiken/bevoelkerung-und-soziales/bevoelkerung/gestorbene/todesursachen>,
  früher bei <http://www.statistik.at/web_de/statistiken/menschen_und_gesellschaft/gesundheit/todesursachen/index.html> (Web Archive!)
* [Grippe, ILI und Meldepflichtiges via AGES](data/ages-epi-misc/) von <https://www.ages.at/mensch/krankheit/krankheitserreger-von-a-bis-z/grippe> usw.
  Die Daten-Tabellen sind beim Öffnen im Browser nicht direkt sichtbar aber im HTML enthalten
  (mit Inspektor im Browser spielen oder Source ansehen).
  Die `Masern_Tabelle.csv` kommt direkt so von der AGES, bei anderen Krankheiten
  steht so ein Download nicht zur Verfügung.

Daten für die keine weitere Aktualisierung der Quelle erwartet wird sind mit 📕
markiert. Eine Aktualisierung bzw. Vervollständigung hier im Repository ist
trotzdem möglich.

## Hinweis zu tar.xz-Dateien

Bei diesen Dateien handelt es sich um komprimierte Archive, also konzeptionell
das selbe wie ZIP-Dateien. Allerdings können tar.xz-Dateien viel kleiner werden
als entsprechende ZIPs. Zum Entpacken unter Windows kann z.B.
[7-Zip](https://www.7-zip.org/download.html) verwendet werden.

Unter Linux sind diese Dateien mit Standard-Bordmitteln verarbeitbar.
