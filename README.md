# covidat-data

This repository aims to contain as-raw-as-sensible Austrian data from these areas:

1. COVID-19 / SARS-CoV-2 (cases, tests, deaths, wastewater, etc.)
2. Mortality (weekly deaths, cause of death, etc.)
3. Health system & Health
4. Related relevant data such as job market data, etc.

Data generally was available to the public from official sources but is no
longer (easily), or is anticipated to become unavailable.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for more general details.

Sorry fürs Denglisch!

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
    [2020](https://web.archive.org/web/20211025205450/https://www.statistik.at/web_de/presse/125475.html))
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
* [Vertriebeinschränkungen bei Medikamenten](docs/basg-medicineshortage.md)
* [Monatsberichte der österr. Sozialversicherung](docs/sozialversicherung-monatsberichte.md)
* [Grippe und ILI-Daten](data/grippe/) von <https://www.ages.at/mensch/krankheit/krankheitserreger-von-a-bis-z/grippe>.
  Die Daten-Tabellen sind beim Öffnen im Browser nicht direkt sichtbar aber im HTML enthalten
  (mit Inspektor im Browser spielen oder Source ansehen).
* Und einiges mehr, derzeit noch nicht dokumentiert (TODO 🚧)

Daten für die keine weitere Aktualisierung der Quelle erwartet wird sind mit 📕
markiert. Eine Aktualisierung bzw. Vervollständigung hier im Repository ist
trotzdem möglich.
