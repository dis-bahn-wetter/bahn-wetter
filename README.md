# Bahn & Wetter

Ist die Bahn bei Regen, Sturm, Schnee oder Hitze unpünktlicher?

## Team

| Name | GitHub | Zuständig für |
| --- | --- | --- |
| Thomas Trinh | [@trinhthomas](https://github.com/trinhthomas) | DB-Verspätungen |
| Paul Ewers | [@paulews](https://github.com/paulews) | DWD-Wetter |
| Lennart Merschel | [@lenmer100](https://github.com/lenmer100) | Feiertage/Events (Scraping) |
| Robel Mihretab | [@robelmihretab](https://github.com/robelmihretab) | NRW-Schulferien (Scraping) |

## Thema

Verspätungen gehören für viele Pendlerinnen und Pendler in Köln zum Alltag. Wir untersuchen, ob die Bahn bei schlechtem Wetter unpünktlicher ist. Dafür verbinden wir die Verspätungsdaten der Deutschen Bahn für Köln Hbf mit stündlichen Wetterdaten des Deutschen Wetterdienstes und reichern sie mit gescrapten Daten zu Schulferien und Feiertagen an.

Grenzen: Die DB-Daten reichen erst ab Juli 2024 zurück und stammen aus einer gesammelten Kopie der DB-Schnittstelle. Streiks und Baustellen können den Einfluss des Wetters überlagern.

## Daten

| Datensatz | Herausgeber | Lizenz | Formate | Profiliert von |
| --- | --- | --- | --- | --- |
| DB-Verspätungen (Deutsche Bahn Train Data) | Deutsche Bahn AG (Timetables API), gesammelt von piebro auf [Hugging Face](https://huggingface.co/datasets/piebro/deutsche-bahn-data) | CC BY 4.0 | Parquet | Thomas Trinh |
| Stündliche Wetterdaten, Station 02667 Köln/Bonn: [Niederschlag](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/hourly/precipitation/), [Wind](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/hourly/wind/), [Lufttemperatur](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/hourly/air_temperature/) | Deutscher Wetterdienst (DWD) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | ZIP mit TXT (`;`-getrennt, Latin-1, Zeit in UTC) | Paul Ewers (Niederschlag) |
| Gesetzliche Feiertage in Deutschland und daraus abgeleitete Kölner Karnevalstage, [Feiertag (Deutschland)](https://de.wikipedia.org/w/index.php?oldid=271794065) (Version 271794065 vom 01.11.2026) | Autor:innen der deutschsprachigen Wikipedia | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.de) | HTML, JSON über die MediaWiki-API; aufbereitet als CSV (ein Eintrag pro Tag) | Lennart Merschel |

Sobald die Feiertagsspalten (CC BY-SA 4.0) in den gemeinsamen Datensatz einfließen, muss dieser selbst unter [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.de) stehen.

## Forschungsfragen

1. Sind Züge in Köln Hbf bei Starkregen, Sturm, Schnee oder Hitze (≥ 30 °C) stärker verspätet als bei normalem Wetter?
2. Ist die Bahn in den NRW-Schulferien und an Feiertagen pünktlicher als an normalen Werktagen?
3. Trifft schlechtes Wetter den Fernverkehr (ICE/IC) stärker als den Regionalverkehr (RE/RB/S)?

Als pünktlich gilt ein Zug mit weniger als 6 Minuten Verspätung (Definition der DB).

## Plan

| Bis | Schritt | Wer |
| --- | --- | --- |
| 13.11.26 | Milestone 1: Roadmap in dieser README | alle |
| 27.11.26 | Scraper für Schulferien und Feiertage | Lennart, Robel |
| 04.12.26 | DB-Daten auf Köln Hbf filtern, DWD-Daten laden | Thomas, Paul |
| 11.12.26 | Bereinigung (Ausfälle, negative Verspätungen, Zeitzonen – DWD in UTC); Join auf Datum und Stunde | alle |
| 18.12.26 | Milestone 2: Datensatz online, Notebook, Datenwörterbuch, World Café | alle |
| 08.01.27 | Hypothesentests und Grafiken | alle |
| 22.01.27 | Repo-Stand final (23:59) | alle |
| 25.01.27 | Milestone 3: Präsentation | alle |
