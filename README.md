# Bahn & Wetter

Ist die Bahn bei Regen, Sturm, Schnee oder Hitze unpünktlicher?

## Team

## Thema

## Daten

| Datensatz | Herausgeber | Lizenz | Formate | Profiliert von |
| --- | --- | --- | --- | --- |
| DB-Verspätungen (Deutsche Bahn Train Data) | Deutsche Bahn AG (Timetables API), gesammelt von piebro auf [Hugging Face](https://huggingface.co/datasets/piebro/deutsche-bahn-data) | CC BY 4.0 | Parquet | Thomas Trinh |
| [Stündlicher Niederschlag, Station 02667 Köln/Bonn](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/hourly/precipitation/) | Deutscher Wetterdienst (DWD) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | ZIP mit TXT (`;`-getrennt, Latin-1) | @paulews |

## Forschungsfragen

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