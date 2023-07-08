# AGES und EMS-Daten

[`ages_all.tar.xz`](../data/ages_all.tar.xz.md) enthält Dateien von
<https://covid19-dashboard.ages.at/data/data.zip> (via https://covid19-dashboard.ages.at/).
Diese ZIPs enthielten jeweils alle CSV-Dateien mit Datenstand des aktuellsten
Tages. Die CSV-Dateien waren auch einzeln über
<https://www.data.gv.at/daten/covid-19/> verfügbar.

Noch ältere Datenstände sind über <https://github.com/statistikat/coronaDAT/>
(halboffizielle Quelle) zu beziehen.

Falls nicht der Zeitverlauf der Meldungen sondern nur der letzte Stand des
Zeitverlaufs der Epidemie benötigt wird, sollte stattdessen einfach
[`ages_last.zip`](../data/ages_last.zip)
verwendet werden (entspricht `20230630/20230630_140201_orig_csv_ages` in `ages-all.tar.xz`).
Die Informationen aus dem Abschnitt [Lizenz](#lizenz) und
[Haupt-CSV-Dateien](#haupt-csv-dateien) gelten auch für diese Datei.

## Lizenz

Aus <https://www.data.gv.at/daten/covid-19/>:

> Die statistischen Informationen des Bundesministeriums für Soziales, Gesundheit, Pflege und Konsumentenschutz (BMSGPK) zur Ausbreitung des neuartigen Coronavirus (COVID-19, SARS-CoV-2) sind als Open Government Data (OGD) unter der offenen Creative Commons (CC) Lizenz verfügbar ([CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.de)). Die Daten sind für die Allgemeinheit unter der Bedingung der Namensnennung (d.h. der Nennung der Quelle BMSGPK) in maschinenlesbarem Format zusammen mit den zugehörigen Metadaten weiterverwendbar.
>
> Dies entspricht den Vorgaben des [Informationsweiterverwendungsgesetzes (IWG)](https://www.ris.bka.gv.at/GeltendeFassung.wxe?Abfrage=Bundesnormen&Gesetzesnummer=20004375) und der [Open Data und Public Sector Information (PSI) Richtlinie 2019/1024 der EU](https://eur-lex.europa.eu/eli/dir/2019/1024/oj?eliuri=eli:dir:2019:1024:oj).

## Struktur und Inhalt von `ages_all.tar.xz`

`ages_all.tar.xz` enthält ein Verzeichnis pro Kalendertag `%Y%m%d` mit einem oder selten mehreren Unterverzeichnissen `%Y%m%d_%H%M%S_orig_csv_ages`
die jeweils die Haupt-CSVs enthalten.

Daneben gibt es fast immer eine Datei mit dem selben Namen wie das Unterverzeichnis und dem Suffix `_hdr.txt` mit den HTTP Response Headern
zur Datei.

Die Ordner sind großteils die entpackten Original-ZIPs. Da die Original-ZIPs deflate-Kompression verwenden konnte durch das Entpacken eine drastische
Reduktion der finalen Archivgröße erreicht werden. Zum Zeitpunkt des Verfassens dieses Textes wären die Original-ZIPs aber ggf. auf Nachfrage
verfügbar.

### Nicht-originale Daten in `ages_all.tar.xz`

Daten die Original-ZIPs entstammen haben einen Zeitstempel der weder auf `_000000` noch `_235959` endet, und haben eine `_hdr.txt` beiliegen.

Alle anderen Daten sind nicht original:

* Wenn der letzte Teil des Zeitstempel `_00000` ist, fehlten üblicherweise die Datei an diesem Tag. Die Daten sind dann meist die des Folgetages mit dem
  letzten Berichtstag aus der CSV-Datei entfernt.
* Wenn keine `_hdr.txt` beiliegt aber der Zeitstempel "normal" ist, dann wurde üblicherweise kein oder ein kaputtes `data.zip` ausgeliefert, aber die
  Einzel-Dateien waren als CSV verfügbar und wurden einzeln heruntergeladen & in den Ordner kombiniert.

Zweck dieser Modifikationen war es, eine lückenlose Zeitreihe der Meldedaten zu haben um zB eine durchgehende Inzidenz nach Meldedatum berechnen zu können.

### Haupt-CSV-Dateien

Bezeichnungen von <https://www.data.gv.at/daten/covid-19/> übernehmend, sind dies "Datensätze zu Fahlzahlen \[sic!] und Hospitalisierung":

* [COVID-19: Daten Covid19-Fälle je Altergruppe](https://www.data.gv.at/katalog/dataset/3765ed62-0f9d-49ad-83b0-1405ed833108): `CovidFaelle_Altersgruppe.csv`
* [COVID-19: Daten Covid19-Fälle je GKZ](https://www.data.gv.at/katalog/dataset/2f6649b6-2b2d-49a9-ab31-6c7e43728001), nur je Bezirk nicht Gemeinde, nur Werte des letzten Tages: `CovidFaelle_GKZ.csv`
* [COVID-19: Zeitliche Darstellung von Daten zu Covid19-Fällen je Bundesland](https://www.data.gv.at/katalog/dataset/ef8e980b-9644-45d8-b0e9-c6aaf0eff0c0): `CovidFaelle_Timeline.csv`
* [COVID-19: Zeitliche Darstellung von Daten zu Covid19-Fällen je Bezirk](https://www.data.gv.at/katalog/dataset/4b71eb3d-7d55-4967-b80d-91a3f220b60c): `CovidFaelle_Timeline_GKZ.csv`
* [COVID-19: Daten zur Auslastung in Spitälern und Testergebnissen](https://www.data.gv.at/katalog/dataset/846448a5-a26e-4297-ac08-ad7040af20f1): `Hospitalisierung.csv`

Weiters, nicht bei der data.gv.at-Übersicht gelistet:

* [COVID-19: Daten zur Auslastung in Spitälern und Testergebnissen "bis 30.5.2021 verlinkt"](https://www.data.gv.at/katalog/dataset/846448a5-a26e-4297-ac08-ad7040af20f1): `CovidFallzahlen.csv` enthält Informationen die mit `Hospitalisierung.csv` überlappende, enthält aber als einzige Datei die "freien" Betten (siehe z.B. https://woswasi.at/2021/04/07/die-auslastung-der-intensivstationen-und-das-ages-dashboard-teil-2/).
  Übrigens gar nicht in dieser Datei sind Fallzahlen.
* `CovidFaelleDelta.csv`: Legacy-Datei, redundant, bei data.gv.at gar nicht auffindbar
* `Version.csv`: Versionsinformationen und Zeitstempel
