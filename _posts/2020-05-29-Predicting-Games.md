---
layout: post
title: Predicting Games
tags:
- project, lambda, steam, games
description: ''
categories:
- Λ Lambda Projects
---

<img src="https://i.imgur.com/5YBERI3.jpg">
<br>
<br>
<b>I am a gamer, as are most of us.</b> So for my project I decided to try and see if I could accurately predict how many people owned a specific game.


Using a <a href="https://www.kaggle.com/tamber/steam-video-games">Dataset</a> pulled from Kaggle, I explored the data and slowly figured out what it was I would be looking for. But first the data needed to be cleaned. The main issues being (1) the column for Owners being a string instead of integer, (2) the NaNs floating throughout the data, (3) a number of columns that had been set with a delimiter which blurred the data, and (4) columns with to much Cardinality and No Variation.


<img src="https://i.imgur.com/32lozNA.png">


The next step was to clean the data by removing the columns with high cardinality and the 'name' column, which had a specific value for each row. Taking apart the columns with multiple tags in each was an issue of sperating the tags by the given delimiter (;) and turning them into features by assigning them to (1) if the feature was contained and (0) if it was not.

Once this was all done I made a visualization based on games that had more than 50,000 positive ratings so that I could get a better idea of what I was working with.

<div>
<iframe style="display: block; margin: auto;" height="600" width="800" src="https://jace-hambrick.github.io/space-jekyll-template/assets/numberofownerstest.html" frameborder="0" allowfullscreen></iframe>
</div>
<br>
<br>
<br>

I wanted to see if I could accurately predict how many owners each game had. The following graph shows what the mean (blue) and median (red) are for the dataset, with mean being 184,360. And after calculating the MAE (mean absolute error) I learned that if we just guessed every game had 184,361 owners, we would be off by 266,700 on average. Keep in mind that far to the right there are a few games with around 10,000,000 owners.


<img src="https://i.imgur.com/bBdwcpj.png">

I decided that the best way to go about solving my problem was with a classification method. So I fit the data to a Linear Regression model to start and see what my Validation Score would be with no feature selection. My model returned a score of 0.6876958141426244. Not the greatest score, but a good starting point.

Next was to fit my data to a Random Forest Classifier and see if I couldn't tune my model to get a higher accuracy. After a bit of fiddling with my classifiers settings I settled for <i>n_estimators=100, random_state=42, n_jobs=-1</i> and ran it to see what I would get. My Validation Accuracy was now 0.8029547553093259, a sizeable improvement.


Finally to make sure that I was reaching the highest score that I could I experiemented with feature testing, seeing what my score would be with, and without specific columns. However every column seemed to carry some importance to the model and I kept it the way it was. To try and see if there was a different way to improve my model I ran it through an XGboost, but kept my previous model as my final.

<img src="https://i.imgur.com/kubsInh.png">

And lastly, I wanted to see which features held the most importance in the model, as well as see how my accuracy changed with those features removed as that information could could be knowledgeable later on. However even after changing them, I was still stuck with a score that barely flucuated from my 0.80295.

<img src="https://i.imgur.com/CC7RE5N.png">

Thank you for reading along!
If you were interested in seeing how this was accomplished please check out my Projects tab!
