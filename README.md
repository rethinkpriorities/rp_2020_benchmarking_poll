## RP 2020 Benchmarking Poll

Open data and code behind [Rethink Priorities](https://www.rethinkpriorities.org/)'s analysis of its 2020 Benchmarking Poll.


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

* **[(3) Analysis - CA Propositions](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(3)%20Analysis%20-%20CA%20Propositions.ipynb)** - Model California state propositions

