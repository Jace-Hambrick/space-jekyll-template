---
layout: post
title: Have movies gone downhill?
tags:
- project, lambda, movie, movies
description: ''
categories:
- Λ Lambda Projects
---

<img src="https://i.imgur.com/a79WjUN.jpg" alt="movie theater">

As a movie lover, it's been a Question of some concern to me. It seems to me that while special effects and technology have advanced, movies have gotten worse. The Question, have movies gotten worse in recent years? Why? Are larger movie companies simply not making the cut anymore?
<br>
<br>
So let's keep that Question nice and close:
<br>
<b>Have Movies Gotten Worse In Recent Years?</b>
<br>
<br>
Using a <a href="https://www.kaggle.com/danielgrijalvas/movies/data">Dataset</a> pulled from Kaggle, I took a deeper look at the Question. Ironically, the creator of said dataset made it for simallar reasons. I started by importing the dataset and taking a good look at what was contained, specifically at what I would need in order to find my Answer.


<img src="https://i.imgur.com/rTHZ9cY.png" alt="dataset">
<p>Contains the columns <q><i>Budget, Company, Country,	Director, Genre, Gross Name, Rating, Released, Runtime, Score, Star, Votes, Writer, and Year</i></q></p>
<br>
<br>
After sifting through the data it became apparent that it was pretty useable with only a few tweaks. To start I had to fix a rather simple problem that would affect my data at a later time. Inside the dataset there were two duplicate companies with the same names, <i>Paramount Pictures</i>. After that I needed to slim down the dataset to have only what I needed to find my Answer.


<img src="https://i.imgur.com/wXJmpTL.png" alt="slim_set">


With this new information I can get closer to the Answer, but with so many companies I would need to slim it down a bit more. After running a value count on company names it was easy to see which companies had been the most active. No suprise, I recognized all of them by name. The next step was to pull each individual year used in the data and save them to use at a later date.


<img src="https://i.imgur.com/2IMu3jP.png" alt="top10">


After that I needed to slim the data frame down to these top 10 companies, as looking at a larger number would have been hard to decypher, and then average the scores of each company by year. A quick pivot so that the columns are the companies, the index is the years, and the average ratings are the values, and the resulting dataframe is a easily readable set of average scores with a few NaN values. A feature of the dataset is its sample of 220 movies per year, and so not all companies had movies pulled from a specific year. 

And then I graphed it for your viewing pleasure.

<b>Warning:</b><i> The following graph may incite madness in mathmaticians.</i>

<div>
<iframe style="display: block; margin: auto;" height="600" width="800" src="https://jace-hambrick.github.io/space-jekyll-template/assets/plotfig.html" frameborder="0" allowfullscreen>
  </iframe>
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
