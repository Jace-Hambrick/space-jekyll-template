---
layout: post
title: Have movies gone downhill?
tags:
- mongodb
description: ''
categories:
- Learn Jekyll 
---

## Are Movies Going Downhill?

<img src="https://i.imgur.com/BiD8eV2.jpg" alt="movie theater">

As a movie lover, it's been a Question of some concern to me. It seems to me that while special effects and technology have advanced, movies have gotten worse. The Question, have movies gotten worse in recent years? Why? Are larger movie companies simply not making the cut anymore?
<br>
<br>
So let's keep that Question nice and close:
<br>
<b>Have Movies Gotten Worse In Recent Years?</b>
<br>
<br>
Using a <a href="https://www.kaggle.com/danielgrijalvas/movies/data">Dataset</a> pulled from Kaggle, I took a deeper look at the Question. Ironically, the creator of said dataset made it for simallar reasons. I started by importing the dataset and taking a good look at what was contained, specifically at what I would need in order to find my Answer.


<img src="https://i.imgur.com/wts70E8.png" alt="dataset">
<p>Contains the columns <q><i>Budget, Company, Country,	Director, Genre, Gross Name, Rating, Released, Runtime, Score, Star, Votes, Writer, and Year</i></q></p>
<br>
<br>
After sifting through the data it became apparent that it was pretty useable with only a few tweaks. To start I had to fix a rather simple problem that would affect my data at a later time. Inside the dataset there were two duplicate companies but with different names, <i>Columbia Pictures Corporation</i> and <i>Columbia Pictures</i>. After that I needed to slim down the dataset to have only what I needed to find my Answer.


<img src="https://i.imgur.com/tS0uitC.png" alt="slim_set">


With this new information I can get closer to the Answer, but with so many companies I would need to slim it down a bit more. After running a value count on company names it was easy to see which companies had been the most active. No suprise, I recognized all of them by name.



<img src="https://i.imgur.com/rMfj8oy.png" alt="top10">





After some data manipulation I was able to find something rather interesting. Over a span of thirty years (1986-2016) there was about a .5 rise in the average rating of movies.


<img src="https://i.imgur.com/XMJibY9.png" alt="Average Movies Bar">


