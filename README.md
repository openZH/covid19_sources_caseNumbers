# Sources of the [SARS-CoV-2 Cases communicated by Swiss Cantons and Principality of Liechtenstein (FL)](https://github.com/openZH/covid_19)
We are providing a common official OGD dataset of SARS-CoV-2 case numbers, which are communicated by official Swiss canton's (26 cantons, abbreviations see below) and Principality of Liechtenstein's (abbreviation: FL) sources. In this repository, we provide additional information about the sources of the data. The data shown here is provided by the cantons and shows their most recent answer to a weekly poll.

We are available to advise and support interested authorities, how to easily complete both historized data, and missing columns. You can reach us:
- https://twitter.com/OpenDataZH (follow us, we send you a private Direct Message, thanks!)
- mailto:info@open.zh.ch

# Data structure

## Data Sources of the Cantonal Case Numbers
The dataset containing the sources of the cantonal case numbers is structured as follows:

| Field Name                 | Description                                                           | Format     | Note                                                                                                      |
|----------------------------|-----------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------|
| abbreviation_canton_and_fl | Abbreviation of the reporting canton and Fürstentum Liechtenstein     | Text       | Accessible via https://www.parlament.ch/de/%C3%BCber-das-parlament/parlamentsw%C3%B6rterbuch/abkuerzungen |
| ncumul_tested_src          | Source of ncumul_tested, as stated by the respective canton           | Text       | see source descriptions for further information                                                           |
| ncumul_tested_def          | Definition of ncumul_tested, as stated by the respective canton       | Text       | see source descriptions for further information                                                           |
| ncumul_conf_src            | Source of ncumul_conf, as stated by the respective canton             | Text       | see source descriptions for further information                                                           |
| ncumul_conf_def            | Definition of ncumul_conf, as stated by the respective canton         | Text       | see source descriptions for further information                                                           |
| new_hosp_src               | Source of new_hosp, as stated by the respective canton                | Text       | see source descriptions for further information                                                           |
| new_hosp_def               | Definition of new_hosp, as stated by the respective canton            | Text       | see source descriptions for further information                                                           |
| current_hosp_src           | Source of current_hosp, as stated by the respective canton            | Text       | see source descriptions for further information                                                           |
| current_hosp_def           | Definition of current_hosp, as stated by the respective canton        | Text       | see source descriptions for further information                                                           |
| current_icu_src            | Source of current_icu, as stated by the respective canton             | Text       | see source descriptions for further information                                                           |
| current_icu_def            | Definition of current_icu, as stated by the respective canton         | Text       | see source descriptions for further information                                                           |
| current_vent_src           | Source of current_vent, as stated by the respective canton            | Text       | see source descriptions for further information                                                           |
| current_vent_def           | Definition of current_vent, as stated by the respective canton        | Text       | see source descriptions for further information                                                           |
| ncumul_released_src        | Source of ncumul_released, as stated by the respective canton         | Text       | see source descriptions for further information                                                           |
| ncumul_released_def        | Definition of ncumul_released, as stated by the respective canton     | Text       | see source descriptions for further information                                                           |
| ncumul_deceased_src        | Source of ncumul_deceased, as stated by the respective canton         | Text       | see source descriptions for further information                                                           |
| ncumul_deceased_def        | Definition of ncumul_deceased, as stated by the respective canton     | Text       | see source descriptions for further information                                                           |
| current_isolated_src       | Source of current_isolated, as stated by the respective canton        | Text       | see source descriptions for further information                                                           |
| current_isolated_def       | Definition of current_isolated, as stated by the respective canton    | Text       | see source descriptions for further information                                                           |
| current_quarantined_src    | Source of current_quarantined, as stated by the respective canton     | Text       | see source descriptions for further information                                                           |
| current_quarantined_def    | Definition of current_quarantined, as stated by the respective canton | Text       | see source descriptions for further information                                                           |
| from                       | First date, on which the given sources are known                      | YYYY-MM-DD | If 1970-01-01, the given sources have been known since the first publication of the respective variable   |
| until                      | Last date, on which the given sources are known                       | YYYY-MM-DD | If empty, the given sources are known to this date                                                        |
| active                     | Dummy, indicating if the given sources are currently in use.          | Number     | The last survey was answered by the cantons between 2020-07-07 and 2020-07-17.                            |
