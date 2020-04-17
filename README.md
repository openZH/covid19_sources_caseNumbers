# Sources of the [SARS-CoV-2 Cases communicated by Swiss Cantons and Principality of Liechtenstein (FL)](https://github.com/openZH/covid_19)
We are providing a common official OGD dataset of SARS-CoV-2 case numbers, which are communicated by official Swiss canton's (26 cantons, abbreviations see below) and Principality of Liechtenstein's (abbreviation: FL) sources. In this repository, we provide additional information about the sources of the data. The data shown here is provided by the cantons and shows their most recent answer to a weekly poll.

We are available to advise and support interested authorities, how to easily complete both historized data, and missing columns. You can reach us:
- https://twitter.com/OpenDataZH (follow us, we send you a private Direct Message, thanks!)
- mailto:info@open.zh.ch

# Data structure

## Data Sources of the Cantonal Case Numbers
The dataset containing the sources of the cantonal case numbers is structured as follows:

| Field Name                 | Description                                                       | Format     | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------|-------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abbreviation_canton_and_fl | Abbreviation of the reporting canton and Fürstentum Liechtenstein | Text       | Accessible via https://www.parlament.ch/de/%C3%BCber-das-parlament/parlamentsw%C3%B6rterbuch/abkuerzungen                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ncumul_tested_src          | Source of ncumul_tested, as stated by respective canton           | Text       | canton_result: data collected by the canton, the date indicates the positive result of the test; canton_sampling: data collected by canton, the date indicates the extraction of the sample; ism_result: data collected out of the Information System Meldungen (ISM) of the Bundesamt für Gesundheit (BAG), the date indicates the positive result of the test; ism_sampling: data collected out of the Information System Meldungen (ISM) of the Bundesamt für Gesundheit (BAG), the date indicates the date indicates the extraction of the sample |
| ncumul_conf_src            | Source of ncumul_conf                                             | Text       | canton_result: data collected by the canton, the date indicates the positive result of the test; canton_sampling: data collected by canton, the date indicates the extraction of the sample; ism_result: data collected out of the Information System Meldungen (ISM) of the Bundesamt für Gesundheit (BAG), the date indicates the positive result of the test; ism_sampling: data collected out of the Information System Meldungen (ISM) of the Bundesamt für Gesundheit (BAG), the date indicates the date indicates the extraction of the sample |
| new_hosp_src               | Source of new_hosp                                                | Text       | canton: data collected by the canton; ies: data read out of the Informationserfassungssysten (IES) of the Koordinierte Sanitätsdienste (KSD)                                                                                                                                                                                                                                                                                                      |
| current_hosp_src           | Source of current_hosp                                            | Text       | canton: data collected by the canton; ies: data read out of the Informationserfassungssysten (IES) of the Koordinierte Sanitätsdienste (KSD)                                                                                                                                                                                                                                                                                                      |
| current_icu_src            | Source of current_icu                                             | Text       | canton: data collected by the canton; ies: data read out of the Informationserfassungssysten (IES) of the Koordinierte Sanitätsdienste (KSD)                                                                                                                                                                                                                                                                                                      |
| current_vent_src           | Source of current_vent                                            | Text       | canton: data collected by the canton; ies: data read out of the Informationserfassungssysten (IES) of the Koordinierte Sanitätsdienste (KSD)                                                                                                                                                                                                                                                                                                      |
| ncumul_released_src        | Source of ncumul_released                                         | Text       | canton: data collected by the canton; ies: data read out of the Informationserfassungssysten (IES) of the Koordinierte Sanitätsdienste (KSD)                                                                                                                                                                                                                                                                                                      |
| ncumul_deceased_src        | Source of ncumul_deceased                                         | Text       | canton: data collected by the canton; ism: data read out of the Information System Meldungen (ISM) of the Bundesamt für Gesundheit (BAG)                                                                                                                                                                                                                                                                                                      |
| from                       | First date, on which the given sources are known without a doubt  | YYYY-MM-DD | If empty, the given sources have been known since the first publication of the respective variable                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| until                      | Last date, on which the given sources are known without a doubt   | YYYY-MM-DD | If empty, the given sources are known to this date                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| active                     | Dummy, indicating if the given sources are currently in use.      | Number     | This will be updated once a week according to feedback of the cantons to a questionaire. Therefore the sources given can be indicated as being active, despite having changed already.                                                                                                                                                                                                                                                                                                                                                                |
