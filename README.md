## RP 2020 Benchmarking Poll

Open data and code behind [Rethink Priorities](https://www.rethinkpriorities.org/)'s analysis of its 2020 Benchmarking Poll.

This poll was run on Rethink Priorities via the [Prolific](https://www.prolific.co/) platform on 20 October 2020. After dropping for data quality checks, it includes 4933 people. People from California were intentionally upsampled, so the raw data includes 1022 people from California and 3911 people from other US states.

Analyses are done on weighted data that corrects this upsampling and corrects other ways that Prolific may not be representative. The weighted N is 1867, suggesting a raw margin of error of +/-2pts at 95% confidence.


### Topline Results

* US national turnout is estimated to be 62.7% of the voting eligible population (80% NMCI: 57.4% to 67.0%). (Note that NMCIs are _naive modeled confidence intervals_ that project actual election results using this poll alone and historical information about polling accuracy, but not other polls or other non-polling informaiton like fundamentals. Thus NMCI are not just the CIs implied by the raw polling margin of error. This is meant to imply that there is an 80% chance that the true value as observed on election day will fall between the two 80% NMCI values.)
* 80.4% of eligible US voters are estimated to be registered (80% NMCI: 75.5% to 85.3%).
* Biden at +9.8 support nationally (80% NMCI: Biden +5.3 to Biden +14.4). These naive modeled NMCIs alone suggest a 86.1% chance Biden wins the Presidency (again, taking into account this poll alone and information about historical accuracy, not taking into account any other polls or any non-polling fundamentals).
* Dems are at +5.3 nationally in the Generic Congressional Ballot (80% NMCI: Reps +2.6 to Dems +13.1), suggesting a 71.7% chance that Dems keep the House.
* Biden is at +2.3 in Texas (80% NMCI: Trump +4.0 to Biden +8.7), suggesting a 62.1% chance that Biden wins Texas.
* Biden is at +28.9 in California (80% NMCI: Biden +22.5 to Biden +35.3), suggesting a >99.9% chance that Biden wins California.
* Cornyn (R) is at +2.5 in the Texas Senate race (80% NMCI: Cornyn +11.3 to Hegar (D) +6.3), suggesting a 59.5% chance that Cornyn keeps his Texas Senate seat.
* CA Prop 14 (Stem Cell) is at 55.6% support (80% NMCI: 43.9 to 67.4), suggesting a 65.7% chance of passing.
* CA Prop 15 (Property Tax) is at 56.5% support (80% NMCI: 45.4 to 67.6), suggesting a 68.8% chance of passing.
* CA Prop 16 (Affirmative Action) is at 39.6% support (80% NMCI: 28.8 to 50.5), suggesting a 21.0% chance of passing.
* CA Prop 17 (Felon Voting) is at 61.2% support (80% NMCI: 52.3 to 70.0), suggesting a 85.7% chance of passing.
* CA Prop 18 (17yo Voting) is at 47.6% support (80% NMCI: 37.2 to 57.9), suggesting a 42.1% chance of passing.
* CA Prop 20 (Parole) is at 45.4% support (80% NMCI: 34.0 to 56.7), suggesting a 36.6% chance of passing.
* CA Prop 21 (Rent Control) is at 46.8% support (80% NMCI: 33.2 to 60.5), suggesting a 42.3% chance of passing.
* CA Prop 22 (Rideshare) is at 50.2% support (80% NMCI: 39.8 to 60.6), suggesting a 50.7% chance of passing.
* CA Prop 23 (Dialysis) is at 55.4% support (80% NMCI: 43.9 to 66.8), suggesting a 65.4% chance of passing.
* CA Prop 25 (Bail) is at 59.0% support (80% NMCI: 49.3 to 68.8), suggesting a 78.2% chance of passing.

See [this sheet](https://docs.google.com/spreadsheets/d/1yuEruo1z4sQ9IIqVMGba1-fumtmypbjZk_2tOZgVhkk/edit#gid=0) for all results and predictions.
 
 
### Install Prerequisites

`pip install -r requirements.txt` to install the pre-requisite packages.


### Raw Data

Raw data is in `repsonses_processed_national_weighted.csv`.

This data was produced with the following two scripts:

* **[(1) Process Data.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(1)%20Process%20Data.ipynb)** - Load the data from Surveymonkey Raw CSV into processed CSVs. Use [survey_dud_detector](https://github.com/rethinkpriorities/survey_dud_detector) and other quality checks to remove bad data.
* **[(2) Weighting.ipynb](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(2)%20Weighting.ipynb)** - Use [surveyweights](https://github.com/rethinkpriorities/surveyweights) package to apply US Census weighting

Note that running these two scripts on your own is unnecessary as the generated data is already included in the repo. Further note that running the first script is not possible publicly as the raw CSVs expose internal Prolific information that cannot be disclosed publicly.


### Models

See [this sheet](https://docs.google.com/spreadsheets/d/1yuEruo1z4sQ9IIqVMGba1-fumtmypbjZk_2tOZgVhkk/edit#gid=0) for results and predictions.

This data was produced with the following scripts:

* **[(3) Analysis - Trump-Biden](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(3)%20Analysis%20-%20Trump-Biden.ipynb)** - Model Trump vs. Biden. Also include estimates of turnout.
* **[(4) Analysis - Generic Congressional Ballot](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(4)%20Analysis%20-%20Generic%20Congressional%20Ballot.ipynb)** - Model the Generic Congressional Ballot
* **[(5) Analysis - Texas Biden + Senate](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Texas%20Biden%20%2B%20Senate.ipynb)** - Model Trump vs. Biden presidential race and Cornyn (R) vs. Hegar (D) senate race in Texas
* **[(6) Analysis - CA Propositions](https://github.com/rethinkpriorities/rp_2020_benchmarking_poll/blob/master/(5)%20Analysis%20-%20CA%20Propositions.ipynb)** - Model California state propositions. Also model Trump-Biden in CA.

