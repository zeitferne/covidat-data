# Morgenmeldung

Die Morgenmeldung, 9:30-Meldung, Ländermeldung, Bundesländermeldung, Meldung
des Innenministeriums.

Diese Daten sind nah verwandt mit den [AGES und EMS-Daten](ages-und-ems.md) und
stehen unter der selben Lizenz.

## Lizenz

Aus <https://www.data.gv.at/daten/covid-19/>:

> Die statistischen Informationen des Bundesministeriums für Soziales, Gesundheit, Pflege und Konsumentenschutz (BMSGPK) zur Ausbreitung des neuartigen Coronavirus (COVID-19, SARS-CoV-2) sind als Open Government Data (OGD) unter der offenen Creative Commons (CC) Lizenz verfügbar ([CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.de)). Die Daten sind für die Allgemeinheit unter der Bedingung der Namensnennung (d.h. der Nennung der Quelle BMSGPK) in maschinenlesbarem Format zusammen mit den zugehörigen Metadaten weiterverwendbar.
>
> Dies entspricht den Vorgaben des [Informationsweiterverwendungsgesetzes (IWG)](https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=20004375) und der [Open Data und Public Sector Information (PSI) Richtlinie 2019/1024 der EU](https://eur-lex.europa.eu/eli/dir/2019/1024/oj?eliuri=eli:dir:2019:1024:oj).

## Inhalte

Bezeichnungen von <https://www.data.gv.at/> übernehmend:

* [`timeline-testungen-apotheken-betriebe.csv`](/data/covid/morgenmeldung/timeline-testungen-apotheken-betriebe.csv):
  [COVID-19: Zeitreihe der gemeldeten COVID-19 Apotheken- und Betriebstestungen](https://www.data.gv.at/katalog/dataset/76a266e7-752e-4979-a415-78a663c9cf53):
  Diese Datei ist als einziges über <https://www.data.gv.at/daten/covid-19/> in der Kategorie "Datensätze zu Fahlzahlen \[sic!] und Hospitalisierung" verlinkt.
  Die letzte URL war <https://www.ages.at/fileadmin/Corona/Wochenbericht/timeline-testungen-apotheken-betriebe.csv> (via <https://www.ages.at/mensch/krankheit/krankheitserreger-von-a-bis-z/coronavirus>), zuvor war sie unter <https://info.gesundheitsministerium.gv.at/data/timeline-testungen-apotheken-betriebe.csv>
  verfügbar (via <https://info.gesundheitsministerium.at/opendata/>)
* [`timeline-testungen-bundeslaender.csv`](/data/covid/morgenmeldung/timeline-testungen-bundeslaender.csv):
  [COVID-19: Zeitverlauf der gemeldeten COVID-19 Testungszahlen der Bundesländer (Morgenmeldung)](https://www.data.gv.at/katalog/dataset/ca7c9b6f-ac7d-4918-8804-edd0942c5dd2).
  Letzte URL <https://www.ages.at/fileadmin/Corona/Wochenbericht/timeline-testungen-bundeslaender.csv>
  via <https://www.ages.at/mensch/krankheit/krankheitserreger-von-a-bis-z/coronavirus>,
  vorher <https://info.gesundheitsministerium.gv.at/data/timeline-testungen-bundeslaender.csv>
  via <https://info.gesundheitsministerium.at/opendata/>.
* [`timeline-faelle-bundeslaender.csv`](/data/covid/morgenmeldung/timeline-faelle-bundeslaender.csv):
  [COVID-19: Zeitverlauf der gemeldeten COVID-19 Zahlen der Bundesländer (Morgenmeldung) (gültig bis 12.09.2022)](https://www.data.gv.at/katalog/dataset/covid-19-zeitverlauf-der-gemeldeten-covid-19-zahlen-der-bundeslander-morgenmeldung):
  Das waren die "echten" Morgenmeldungen.

  Letzte URL <https://info.gesundheitsministerium.gv.at/data/timeline-faelle-bundeslaender.csv>
  via <https://info.gesundheitsministerium.at/opendata/>
  oder <https://www.sozialministerium.at/Informationen-zum-Coronavirus/Neuartiges-Coronavirus-(2019-nCov).html>
  oder in Teilen, dafür mit älteren Zahlen als OTS
  <https://www.ots.at/suche?query=Aktuelle+Zahlen+zum+Corona-Virus&from=01.01.2020&to=01.01.2023&filter=&emittentid=54&searchinpm=on>
  oder früher täglich überschrieben bei <https://bmi.gv.at/news.aspx?id=4A7171477A51625143334D3D>.

  Auch bei <https://just-the-covid-facts.neuwirth.priv.at/download_data/>
  (via https://just-the-covid-facts.neuwirth.priv.at/) gibt es ein Archiv mit
  älteren Daten als in der CSV enthalten sind.
* [`timeline-faelle-ems.csv`](/data/covid/morgenmeldung/timeline-faelle-ems.csv):
  [COVID-19: Zeitverlauf der gemeldeten COVID-19 Fälle im EMS (Morgenmeldung) (gültig bis 12.09.2022)](https://www.data.gv.at/katalog/dataset/9723b0c6-48f4-418a-b301-e717b6d98c92):
  Letzte URL <https://info.gesundheitsministerium.gv.at/data/morgenmeldung/timeline-faelle-ems.csv>
  via <https://info.gesundheitsministerium.at/opendata/>
  oder <https://www.sozialministerium.at/Informationen-zum-Coronavirus/Neuartiges-Coronavirus-(2019-nCov).html>
* [`timeline-testungen-schulen.csv`](/data/covid/morgenmeldung/timeline-testungen-schulen.csv):
  [COVID-19: Zeitreihe der gemeldeten COVID-19 Schultestungen](https://www.data.gv.at/katalog/dataset/01e8bfdf-9688-44eb-b851-40b61c4785bd)
  Letzte URL <https://info.gesundheitsministerium.at/data/timeline-testungen-schulen.csv>
  via <https://www.sozialministerium.at/Informationen-zum-Coronavirus/Neuartiges-Coronavirus-(2019-nCov).html>.
  Die Zeitreihe war aus den kumulativen Summen jederzeit selbst mitschreibbar,
  der Link auf die CSV-Datei wurde jedoch irgendwann von der Webseite entfernt
  und der Datensatz auf data.gv.at offiziell als "eingestellt" deklariert,
  obwohl die Datei hinter der URL weiterhin wöchentlich aktualisiert wurde.

  Kein eigentlicher Teil der Morgenmeldung aber auf der selben Webseite
  und mit ähnlicher Struktur, und passt sonst nirgendwo dazu.

All diese Dateien wurden nur im letztgültigen Datenstand archiviert, da es sich
um Daten nach Meldedatum handelt in denen, bis auf wenige Ausnahmefälle bei
groben und früh erkannten Eintragefehlern, nie rückwirkend korrigiert wurde.
Teilweise (immer?) hat der Twitter-Account
[@medienkontrolle](https://twitter.com/medienkontrolle) einen kleinen
Auszug der ursprünglicheren Zahlen aus der "echten" Morgenmeldung vertwittert.
