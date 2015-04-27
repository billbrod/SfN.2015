---
geometry: margin=2cm
tags: [+PenaltyKick, +Behavioral, +MVPA, +Abstract]
date: 2015-04-26
title: Figures 

---

Discuss with everyone:

* We should do subject-level cross-validation for all of the contrasts
  right? Even human-cpu, which we could do at run-level, but then it
  wouldn't be as good of a control (results are similar, but not as
  extreme). Actually, may want to use them together. The fact that
  run-level, some subjects have very low errors that they don't have
  when used as the test dataset suggests that there's something
  particular in their brain being used that is not found in
  others'. Makes sense, but it's not just a stronger version of
  something found in others'.
* Probably want to include univariate for these contrasts as
  well. Will be hard to tell what exactly that is telling us, but
  still useful. I read a paper which had the suggestion to classify on
  the univariate means instead of just using GLM, what do people think
  about that? More directly comparable then. -- Stick with GLM for now
* Do we want to do anatomical ROIs vs. searchlights? Not sure how to
  implement ROIs, quick search doesn't turn up much. Appears I would
  need to define ROIs elsewhere (via
  [Nipype?](http://miykael.github.io/nipype-beginner-s-guide/regionOfInterest.html)),
  and mask the datasets, presenting them individually to
  classifiers...not sure there's a simpler way. -- Anatomical, McKell
  will send something
* Still don't have any sort of statistical significance testing for
  MVPA, which we'll need, and should do permutation testing.
* If we decide to do regression instead of classification, or change
  SVM so we get rankings out of it - does that change any other part
  of analysis much? How does that interact with sig testing? -- do
  classification for now, then see.
* How many figures for an abstract? How long does that have to be? (No
  more than 2300 characters including punctuation but not spaces) What
  theme/subtheme would this be under? (Probably Cognition and Behavior
  -> Human, but then, Decision making and reasoning?) -- no figures,
  just writing for now
  

#Task#

* Figure showing task

#Behavioral Analyses#

* Figure showing how we transformed task data to the form used for the
  behavioral analysis and k-means (y-difference, interpolation,
  standardization, combined with trial length)

* Human opponent 4-cluster group figure

* Maybe: time (both the time of the path\_trial clustering and the
  group for the trial\_length\_std clustering), win/loss figures as
  well to show that info isn't being used

* PCA 1,2,4,6 cluster plots

* Cost vs. number of clusters plots? (probably not)

* Transition probabilities, grouped (non-grouped too?)

* Symmetry plots?

* Breakdown by subject somehow (either the PCA 2-dim plots or the
heatmaps - probably heatmaps)

# MVPA #

* Following is for each analysis run: human-computer, early-late, up-down, change-repeat

* Violin plots (probably not showing label balance)

* Searchlights in brain: by subject or just overall? Don't want to show all searchlight results, so how do we pick most significant?
