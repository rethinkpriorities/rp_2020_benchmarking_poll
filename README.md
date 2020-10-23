## RP 2020 Benchmarking Poll

Open data and code behind [Rethink Priorities](https://www.rethinkpriorities.org/)'s analysis of its 2020 Benchmarking Poll.

This poll was run via the [Prolific](https://www.prolific.co/) platform. After dropping for data quality checks, it includes 4944 people. People from California were upsampled on Prolific, so the raw data includes 1024 people from California and 3920 people from other US states. Analyses are done on weighted data that corrects this upsampling and corrects other ways that Prolific may not be representative.


### Topline Results

* Turnout is estimated to be 68.3% of the voting population (80% CI: 61.0% to 72.6%).
* 87.6% of eligible voters are estimated to be registered (80% CI: 80.6% to 91.5%).
* Biden at +10.0 support nationally (80% CI: Biden +3.6 to Biden +16.4), suggesting a 90.6% chance Biden wins the Presidency.
* Dems are at +5.4 nationally in the Generic Congressional Ballot (80% CI: Reps +3.4 to Dems +14.0), suggesting a 69.8% chance that Dems keep the House.
* Trump is at +4.7 in Texas (80% CI: Trump +15.2 to Biden +5.9), suggesting a 64.5% chance that Trump wins Texas.
* Biden is at +44.6 in California (80% CI: Biden +36.4 to Biden +52.8), suggesting a >99.9% chance that Biden wins California.
* Cornyn (R) is at +6.3 in the Texas Senate race (80% CI: Cornyn +18.8 to Hegar (D) +6.2), suggesting a 66.7% chance that Cornyn keeps his Texas Senate seat.
* CA Prop 14 (Stem Cell) is at 54.0% support (80% CI: 31.7 to 72.6), suggesting a 57.7% chance of passing.
* CA Prop 15 (Property Tax) is at 59.3% support (80% CI: 36.2 to 78.9), suggesting a 68.0% chance of passing.
* CA Prop 16 (Affirmative Action) is at 45.1% support (80% CI: 22.0 to 64.9), suggesting a 41.4% chance of passing.
* CA Prop 17 (Felon Voting) is at 59.3% support (80% CI: 37.1 to 78.0), suggesting a 68.7% chance of passing.
* CA Prop 18 (17yo Voting) is at 73.8% support (80% CI: 43.7 to 100.0), suggesting a 75.2% chance of passing.
* CA Prop 20 (Parole) is at 52.9% support (80% CI: 29.4 to 73.1), suggesting a 56.1% chance of passing.
* CA Prop 21 (Rent Control) is at 47.7% support (80% CI: 22.6 to 69.5), suggesting a 46.7% chance of passing.
* CA Prop 22 (Rideshare) is at 54.1% support (80% CI: 35.9 to 71.7), suggesting a 58.5% chance of passing.
* CA Prop 23 (Dialysis) is at 52.4% support (80% CI: 28.3 to 72.9), suggesting a 55.1% chance of passing.
* CA Prop 25 (Bail) is at 58.8% support (80% CI: 37.7 to 76.3), suggesting a 67.8% chance of passing.

See [this sheet](https://docs.google.com/spreadsheets/d/1yuEruo1z4sQ9IIqVMGba1-fumtmypbjZk_2tOZgVhkk/edit#gid=0) for all results and predictions.
 
 
### Install Prerequisites

`pip install -r requirements.txt` to install the pre-requisite packages.


### Raw Data

Raw data is in `repsonses_processed_national_weighted.csv`.

This data was produced with the following two scripts:

* **[(1) Process Data.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(1)%20Process%20Data.ipynb)** - Load the data from Surveymonkey Raw CSV into processed CSVs. Use [survey_dud_detector](https://github.com/rethinkpriorities/survey_dud_detector) and other quality checks to remove bad data.
* **[(2) Weighting.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(2)%20Weighting.ipynb)** - Use [surveyweights](https://github.com/rethinkpriorities/surveyweights) package to apply US Census weighting


### Models

See [this sheet](https://docs.google.com/spreadsheets/d/1yuEruo1z4sQ9IIqVMGba1-fumtmypbjZk_2tOZgVhkk/edit#gid=0) for results and predictions.

This data was produced with the following scripts:

* **[(3) Analysis - Trump-Biden](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(3)%20Analysis%20-%20Trump-Biden.ipynb)** - Model Trump vs. Biden. Also include estimates of turnout.
* **[(4) Analysis - Generic Congressional Ballot](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(4)%20Analysis%20-%20Generic%20Congressional%20Ballot.ipynb)** - Model the Generic Congressional Ballot
* **[(5) Analysis - Texas Biden + Senate](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Texas%20Biden%20%2B%20Senate.ipynb)** - Model Trump vs. Biden presidential race and Cornyn (R) vs. Hegar (D) senate race in Texas
* **[(6) Analysis - CA Propositions](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Analysis%20-%20CA%20Propositions.ipynb)** - Model California state propositions. Also model Trump-Biden in CA.

