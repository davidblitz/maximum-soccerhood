soccer-pred
===========

The soccer-pred project consists mainly of four files - one .txt file and three .ipynb files:

1. preprocess.ipynb

   This ipython-notebook-file preprocesses the input .txt-file and outputs bundesliga_15_16.csv
   as well as bundesliga_15_16_teams.csv which store the home-team/away-team pairings and results
   as well as the teams of the current Bundesliga season respectively.

  A. 1-bundesliga-i.txt

     This is a rather unstructured list of the games of the current season which has to be processed.
     It is taken from [this](https://github.com/openfootball/de-deutschland/tree/master/2015-16) github page.

2. train-scipy.ipynb

   This ipython-notebook-file takes bundesliga_15_16.csv as input and uses (still) a simplified version of
   the Dixon-Coles predictor described in [this](http://www.math.ku.dk/~rolf/teaching/thesis/DixonColes.pdf) paper from 1997.
   It outputs dc_model_params.csv which stores all the parameters of the (simplified) Dixon-Coles model.
   In our model we have an attack and a defense strengths for each team, as well as an overall home-advantage parameter.

3. pred.ipynb

   This ipython-notebook-file takes dc_model_params.csv as input and in the last cell you can designate a home team and
   an away team in order to simulate a match based on the data from the first half of the current Bundesliga season.

Happy simulating!
