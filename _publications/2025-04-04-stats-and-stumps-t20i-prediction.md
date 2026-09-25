---
title: "Stats & Stumps: Using Machine Learning to Predict T20I Matches with Player and Venue Data"
collection: publications
permalink: /publication/2025-04-04-stats-and-stumps-t20i-prediction
excerpt: 'Predicts Twenty20 International outcomes from venue-adjusted, player-level impact metrics. Regularized logistic regression reached 70.24% test accuracy on 1,029 matches.'
date: 2025-04-04
venue: 'Wharton Sports Analytics Journal'
paperurl: '/files/stats-and-stumps-t20i-prediction.pdf'
citation: 'Sharma, A. (2025). &quot;Stats &amp; Stumps: Using Machine Learning to Predict T20I Matches with Player and Venue Data.&quot; <i>Wharton Sports Analytics Journal</i>.'
---

**Abstract.** Cricket is gaining popularity worldwide rapidly, and at the front is the newest format of the game, Twenty20 Internationals (T20I), and big data. This project attempts to predict cricket match outcomes using player-level performance metrics and machine learning models. A dataset of 1,029 T20I matches was analyzed, with player-level features engineered from batting and bowling statistics such as runs, strike rate, boundaries, wickets, economy rate, and maiden overs. These features were normalized by ground-specific scoring rates to account for venue effects.

Four modeling approaches were compared: a simple heuristic based on total player impact, logistic regression with regularization, random forests, and support vector machines (SVMs). Logistic regression achieved the highest test accuracy of 70.24%, balancing predictive performance with model interpretability. The final model was used to generate win probabilities for both past and unseen matches, including the 2024 T20 World Cup Final (India vs South Africa) and a March 2025 match between New Zealand and Pakistan.

**Code:** [github.com/ArchithSharma/CricketPredictions](https://github.com/ArchithSharma/CricketPredictions)
