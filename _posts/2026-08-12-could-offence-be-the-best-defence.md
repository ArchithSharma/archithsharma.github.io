---
title: 'Could offence be the best defence in football?'
date: 2026-08-12
permalink: /posts/2026/08/could-offence-be-the-best-defence/
excerpt: 'A review of "parking the bus" at the 2026 World Cup, combined with data on whether attacking teams are better at protecting a lead.'
tags:
  - football
  - sports analytics
  - World Cup
---

<div class="notice--info" markdown="1">
Originally published on [Beyond the Box Score](https://archithsharma.substack.com/p/could-offence-be-the-best-defence) on Substack.
</div>

90 minutes into the match, Japan are desperately trying to keep the Brazilians out. After Japan stole an opening goal, Casemiro pulled the Selecao level. Hajime Moriyasu has made his decision on how to keep it that way - everyone’s at the back. In the 90+6th minute, Gabriel Martinelli then sends a dagger into the heart of the Japanese fans before they can settle the affair in extra time.

About a week after this happened, Thomas Tuchel was down a man, but up a goal against the co-host nation in their fortress, the Azteca. For 30 minutes, Mexico sent cross after cross into the English box, while Dan Burn, John Stones, and Jordan Pickford cleared the ball as quickly as it came in. They escaped the Round of 16 before getting past Erling Haaland and company in the quarters. The introduction of Dan Burn forced Ståle Solbakken to take off his superstar #9 and try to beat England a different way, which they couldn’t.

Then came the game against Argentina. After Anthony Gordon’s strike early in the second half, England remarkably had 12% possession for the rest of the match. This wasn’t the most damning statistic, however.

[![England's 2026 World Cup squad announcement](https://substackcdn.com/image/fetch/$s_!A7xq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb85a460-8bbb-482a-87e8-e08582f6f82a_399x501.jpeg)](https://substackcdn.com/image/fetch/$s_!A7xq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb85a460-8bbb-482a-87e8-e08582f6f82a_399x501.jpeg)

Reece James was positioned behind the keeper for an average of over 20 minutes, and Declan Rice was the furthest player up the pitch. While parking the bus suffocated Norway and Mexico, it was the perfect environment for Lionel Messi, and why wouldn’t it be for a passer of his caliber? Just look at the [picture-perfect weak-footed cross to Lautaro Martinez to go out in front.](https://youtu.be/y-4saPWrPt0?si=nn12AWEpeZLaVF9d&t=708)

If you ask me, it’s wrong to say Tuchel was at fault for the strategy. Look at the full second-half match momentum chart.

[![Second-half match momentum chart, England vs Argentina](https://substackcdn.com/image/fetch/$s_!jVOR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc01c2a18-3d32-4814-9d31-7e1f4aa9a0d1_770x478.png)](https://substackcdn.com/image/fetch/$s_!jVOR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc01c2a18-3d32-4814-9d31-7e1f4aa9a0d1_770x478.png)

Even before England’s first substitution, Argentina were pummeling the English, starting at the point Djed Spence unleashed a Maldini-esque tackle on Giuliano Simeone to turn a clear equalizer into a corner. It’s also easy to say that the strategy was wrong after the fact, as hindsight is 20/20. In fact, Argentina’s momentum was significantly reduced over the next few minutes when Dan Burn and Nico O’Reilly were introduced. Then came the Fernandez wonderstrike, and the rest was history.

The question that we should be asking is not whether England should have hunted for a second, but **whether the threat of attacking does a good job of defending.**

Thanks for reading! [Subscribe for free on Substack](https://archithsharma.substack.com/subscribe) for more data-related insights :)

I know this piece isn’t as detail-oriented as my first one (check it out below!) but I thought it was a question worth exploring given what happened at the World Cup and its ramifications.

> Earlier post: [“For 60 overs, they should feel like hell out there”](/posts/2026/05/for-60-overs-they-should-feel-like/) — how much of India’s 2021 Lord’s turnaround can be credited to Kohli’s captaincy?

I conducted a quick analysis of games with [Gökhan Ergül's Kaggle Football dataset](https://www.kaggle.com/datasets/gokhanergul/football-match-statistics/data), although it was not a robust analysis. The general finding is that, on average, teams that play more attacking football tend to preserve leads in club football. 

## (Brief) Method Description

The way that I went about it with this data was to calculate a “defensive” statistic for every team, scaling 4 attributes: the share that the opponent had of possession, SOG, shots, and amount of corners. This isn’t a very robust analysis, but it’s kind of just an exposure to the problem statement anyway so be on the lookout for a better version of this with event data that I’ll be doing later and uploading here!

Note: share is, for any of the four attributes:

$$\text{share} = -\frac{x_{team}}{x_{team} + x_{opp}}$$

Each of these attributes are then added, with no weighting on them. For each statistic, a higher opponent share corresponds to a higher defensive profile. I standardized the four measures and averaged them with equal weights. Then, I looked at specifically the games with a one-goal halftime differential (or more), to see how this defensive statistic was associated with the probability of preserving a lead conditional on the halftime score.

## Results

[![Win probability by halftime lead, split by defensive profile](https://substackcdn.com/image/fetch/$s_!k8ts!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b17981f-b3d2-44d4-831c-88a8f4ee1f5b_960x594.png)](https://substackcdn.com/image/fetch/$s_!k8ts!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b17981f-b3d2-44d4-831c-88a8f4ee1f5b_960x594.png)

As you’d expect, win probability increases with the lead regardless of strategy. It’s much easier to give up a one goal lead than a two-goal lead, as Tuchel’s men showed us against Argentina and Mexico. In addition, playing more defensive was mostly correlated to a lower probability of winning, however! This doesn't necessarily mean that playing defensively makes you more likely to lose; the relationship could instead reflect differences in team quality and other match-level factors. 

Possession is such a weird statistic in this sense, because most great teams have it, but at the same time, it kind of doesn’t matter. You can pass the ball a thousand times, but be so dull in the final third that 4 minutes is all it takes for your opponent to beat you - just look at the wild momentum sheets from Japan’s match against Spain in 2022, and their momentum sheet from Spain’s opening game against Cabo Verde (via SofaScore). Neither match yielded a favorable result for La Roja.

[![Match momentum chart, Japan vs Spain, 2022 World Cup](https://substackcdn.com/image/fetch/$s_!BZa0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ec163ff-9f14-499f-82ea-6449341e373c_1604x546.png)](https://substackcdn.com/image/fetch/$s_!BZa0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ec163ff-9f14-499f-82ea-6449341e373c_1604x546.png)

[![Match momentum chart, Spain vs Cabo Verde, 2026 World Cup](https://substackcdn.com/image/fetch/$s_!ukdv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a01d4a5-842d-4c76-9bbe-8cea2540b3b8_2052x566.png)](https://substackcdn.com/image/fetch/$s_!ukdv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a01d4a5-842d-4c76-9bbe-8cea2540b3b8_2052x566.png)

However, with a very similar style of play, Spain dominated the 2026 World Cup, even though they had an early exit in the 2022 World Cup and had a slow start to the most recent one. 

[![Second-half goal differential against defensive profile](https://substackcdn.com/image/fetch/$s_!5wfu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1610077c-11c4-4e68-a50f-7cab9633506f_960x594.png)](https://substackcdn.com/image/fetch/$s_!5wfu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1610077c-11c4-4e68-a50f-7cab9633506f_960x594.png)

> By itself, playing defensively isn’t the reason teams win or lose matches.

## Takeaways I think are important

Take a look at this chart. The defensive profile is the x-axis, while the response is goal-differential in the second half. Playing more defensively is correlated with giving up the lead, but part of the reason is simple: when you generate fewer chances yourself, there are fewer opportunities to extend your advantage. The outcome becomes increasingly binary: if the opponent doesn't score, you survive; if they do, you're in a real pickle. By itself, playing defensively isn’t the reason teams win or lose matches. The defensive profile explains some variation, but it doesn’t determine the outcome.

There’s obviously comparing execution - Argentina executed very well, England didn’t and there’s luck that plays into that as well. Before Messi’s go-ahead cross, Spence was limping, making Messi’s job of getting the ball to Martinez’s head much easier.

Feel free to share with friends who would also enjoy this content!

The point is, there are plenty of teams that played defensively and came out on top, and plenty of teams that didn’t play defensively and paid for that decision. It just goes to show how difficult the job of a coach is, and how they balance what they can and can’t do while literally the whole world is watching. 

Team quality, opponent pressure, execution, and luck all matter. With that being said, there is still merit to the idea that sitting deep can invite pressure, drain energy, and create the conditions for the opponent to eventually find a breakthrough. 

> Perhaps attacking isn't the opposite of defending. Perhaps threatening the opponent is itself a defensive mechanism.

Maybe the best way to defend a lead isn’t to stop attacking at all. **Maybe the threat of attacking really is a form of defence.**

Hi, I’m Archith! If you love sports and math, you’re in the right place - [subscribe on Substack](https://archithsharma.substack.com/subscribe) for more :)
