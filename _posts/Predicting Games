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

I am a gamer, as are most of us. So for my project I decided to try and see if I could accurately predict how many people owned a specific game.
<br>
<b>So let's predict some games.</b>
<br>
<br>
Using a <a href="https://www.kaggle.com/tamber/steam-video-games">Dataset</a> pulled from Kaggle, I explored the data and slowly figured out what it was I would be looking for. But first I needed to clean up the data. The main issues being (1) the column for Owners being a string instead of integer, (2) the NaNs floating throughout the data, and (3) a number of columns that had been set with a delimiter which blurred the data.

<img src="https://i.imgur.com/32lozNA.png">

I wanted to see if I could accurately predict how many owners each game had. The following graph shows what the mean (blue) and median (red) are for the dataset, with mean being 184,360. And after calculating the MAE (mean absolute error) I learned that if we just guessed every game had 184,361 owners, we would be off by 266,700 on average.


<img src="https://i.imgur.com/bBdwcpj.png">


With this baseline in hand I could start to 


<img src="https://i.imgur.com/2IMu3jP.png" alt="top10">


After that I needed to slim the data frame down to these top 10 companies, as looking at a larger number would have been hard to decypher, and then average the scores of each company by year. A quick pivot so that the columns are the companies, the index is the years, and the average ratings are the values, and the resulting dataframe is a easily readable set of average scores with a few NaN values. A feature of the dataset is its sample of 220 movies per year, and so not all companies had movies pulled from a specific year. 

And then I graphed it for your viewing pleasure.

<b>Warning:</b><i> The following graph may incite madness in mathmaticians.</i>

<div>
<iframe style="display: block; margin: auto;" height="600" width="800" src="https://jace-hambrick.github.io/space-jekyll-template/assets/plotfig.html" frameborder="0" allowfullscreen></iframe>
</div>


While not the most comprehensive graph. You can take one major thing away from it. Over the past thirty years, with some minor exceptions, the top ten movie companies have stayed almost consistently at 6 or just slightly above. This got me curious, so I slimmed it down to only the top three to get a better view, as shown in the graph below.

<img src="https://i.imgur.com/5eh6sP0.png" alt="top10graph">

The result is rather conclusive. The top 3 movie companies have gotten more consistent, but are still stuck at just about 6. So let's look at our question.

<b>Have Movies Gotten Worse In Recent Years?</b>


Well we can now say that no, they have not gotten worse, at least not for the top movie studios. But that doesn't really answer my question. So the next thing to look at is every company, and to do so I look back at the Graph_Data dataset. Everything I need is here but I not exclusive from the rest of the data. To fix this I need to make another funtion, this time to find out the average ratings of every movie provided, by the year it was released.

Taking a crosstab, or comparing two seperate columns of the dataset against eachother, of the Scores and Years. Using this new dataset I was able to look at the average ratings of every year. And the result was rather interesting. Over a span of thirty years (1986-2016) there was about a .5 rise in the average rating of movies as seen in the two charts below.


<img src="https://i.imgur.com/69k3YW4.png" alt="Average Movies Bar">

Well that answers the Question. But <b>who</b> is making the better movies, and what movies <i>are</i> the better movies. Another question for us to answer, and a rather simple one at that. With a quick bit of exploring I was able to put together a new chart for your enjoyment.

<div>
<iframe style="display: block; margin: auto;" height="600" width="800" src="https://jace-hambrick.github.io/space-jekyll-template/assets/plotfig2.html" frameborder="0" allowfullscreen></iframe>
</div>

<br>
<br>

Thank you for reading along!
If you were interested in seeing how this was accomplished please check out my Projects tab!
