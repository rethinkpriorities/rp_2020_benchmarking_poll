## RP 2020 Benchmarking Poll

Open data and code behind [Rethink Priorities](https://www.rethinkpriorities.org/)'s analysis of its 2020 Benchmarking Poll.

This poll was run via the [Prolific](https://www.prolific.co/) platform. After dropping for data quality checks, it includes 4944 people. People from California were upsampled on Prolific, so the raw data includes 1024 people from California and 3920 people from other US states. Analyses are done on weighted data that corrects this upsampling and corrects other ways that Prolific may not be representative.


### Install Prerequisites

`pip install -r requirements.txt` to install the pre-requisite packages.


### Raw Data

Raw data is in `repsonses_processed_national_weighted.csv`.

This data was produced with the following two scripts.

* **[(1) Process Data.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(1)%20Process%20Data.ipynb)** - Load the data from Surveymonkey Raw CSV into processed CSVs. Use [survey_dud_detector](https://github.com/rethinkpriorities/survey_dud_detector) and other quality checks to remove bad data.
* **[(2) Weighting.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(2)%20Weighting.ipynb)** - Use [surveyweights](https://github.com/rethinkpriorities/surveyweights) package to apply US Census weighting


### Models

See [this sheet](https://docs.google.com/spreadsheets/d/1yuEruo1z4sQ9IIqVMGba1-fumtmypbjZk_2tOZgVhkk/edit#gid=0) for results and predictions.

This data was produced with the following scripts:

* **[(3) Analysis - Trump-Biden](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(3)%20Analysis%20-%20Trump-Biden.ipynb)** - Model Trump vs. Biden
* **[(4) Analysis - Generic Congressional Ballot](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(4)%20Analysis%20-%20Generic%20Congressional%20Ballot.ipynb)** - Model the Generic Congressional Ballot
* **[(5) Analysis - Texas Biden + Senate](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Texas%20Biden%20%2B%20Senate.ipynb)** - Model Trump vs. Biden presidential race and Cornyn (R) vs. Hegar (D) senate race in Texas
* **[(6) Analysis - CA Propositions](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Analysis%20-%20CA%20Propositions.ipynb)** - Model California state propositions. Also model Trump-Biden in CA.

