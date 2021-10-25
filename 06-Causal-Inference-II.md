# Causal Inference I

## Topics

* Introduction to Causal Inference.
* Finishing up "stop rates" description.
* Implementing the Veil of Darkness.

## Reading and Analyses
  
* Read [Mostly Harmless
  Econometrics](https://www.researchgate.net/publication/51992844_Mostly_Harmless_Econometrics_An_Empiricist's_Companion/link/00b4953344a9a0cb13000000/download)
  (sections 2.1, 2.2, 3.2 (you can skip 3.2.2), 5.1, 5.2). While
  reading the book, carefully understand how it relates to the
  [notebook](material/Simulation.ipynb) from section last week.
  
* Recreate the analyses in the Simulation notebook on the SD stops
  data using the naive approximation for stops rates we have been
  using (you have already computed the necessary tables in previous
  work!). How do you think the data generating process for the SD data
  compares to the data generating processes defined in the notebook? 

* Recreate the Veil of Darkness study on SD data. You may find the
  OpenPolicing tutorial useful. Note, this study doesn't use
  stop-rate, but a different measurement! (When doing this, flexibly
  structure your code; you will be expected to compute these results
  across years/places for assignment-2).

## Discussion questions from reading and analysis

* What might be captured in the selection bias portion of the observed
  difference in stop rates? What is the sign of this bias? (Give
  examples from suspect citizens).
  
* Suspect citizens suggests that past police interactions may affect
  current behavior.  Then we can represent the DGP as where <img
  src="https://render.githubusercontent.com/render/math?math=D_{it}">
  is driver behavior in *t*. Can we still causally estimate the effect
  of observed race? How would this change the interpretation of our
  estimates?
  
  <img
  src="https://render.githubusercontent.com/render/math?math=Y_{it}=f(M_i,D_{it}(Y_{it-1}),\varepsilon_{it})">
  
* (Related to previous) In medical trials, [double blind
  experiments](https://link.springer.com/referenceworkentry/10.1007%2F978-3-540-68706-1_1425)
  are the gold standard.  If you could design an experiment to test
  for racial bias in police behavior, how could you attempt to meet
  this standard? Note that this may not be an experiment that is
  feasible or ethical, and if what you create fails either of those
  standards, explain why. What do you sacrifice in generalizability?
  
* From 3.2: what is the conditional expectation function assumed in
  the veil of darkness study.  What assumptions are required?
  
* From 5: What fixed effect does the intertwilight period allow us to
  use? What treatment intensity variables could you construct? (Think
  about natural and unnatural light sources to get started).
  
