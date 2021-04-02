---
layout: post
title: Seeking Asylum
tags:
- project, lambda, Human, Rights, First, Asylum
description: 'Project for Human Rights First'
categories:
- Λ Lambda Projects
---

<img src="https://i.imgur.com/jYHNXAa.png">


<h2>Who and What?</h2>


This past month I have been working with the Human Rights First, a 501(c)3 organization to develop an application that uses optical character recognition to scan input court decisions for important values and inserts them into a database. The application is to assist immigration attorneys and refugee representatives in advocating for clients in asylum cases by identifying patterns in judicial decisions, and by predicting possible outcomes.


Going into this project I was afraid that I wouldn’t be of much use to the team and the company. I wasn’t very confident in my abilities, and felt woefully unprepared for what I faced. I could only hope that I would be able to rise to the occasion and create something wonderful.

<h2>Contributing to the Cause</h2>

Two weeks into the project, over my fears and smashing through hurdles, I had made significant progress on my addition to the cause.
 Due to the nature of the project the first thing I had done was take an in-depth look at data ethics, something I, and the rest of the team, was rather unfamiliar with. I devoted almost a full day towards this, as this would have a big impact on the stakeholders. Afterwards I researched my topic, looking at various other sites that visualized court data.


This is where I came face to face with one of the biggest challenges. Anything I made now would look drastically different and possibly unusable in the future as more data was added to the project. I needed to come up with something that would allow me to have a usable visualization both now, and in the future.


My solution was to make a visual that had a baseline that wouldn’t change, and the baseline that I chose was the world. Countries are immovable objects that have stayed the same for centuries now, and by using the world as a baseline, the visual itself will maintain its ease of use, requiring very little maintenance.
Having ensured the data was ethical, I then transformed the given data into something more useful and created two world maps. One, a choropleth map, took a look at all the countries that had asylum seekers and displayed their protected grounds.


<p align="center" style="font-size:11px"><iframe width="1200" height="350" src="https://jace-hambrick.github.io/space-jekyll-template/assets/asylum_choropleth.html" title="Choropleth Map"></iframe>
 <i>Choropleth Map showing country colored by Protected Grounds.</i></p>


The other world map was a scatterplot map that showed more in depth information. It plotted each case so far by its country of origin and allowed a user to hover over the dot in order to read more about the case. Though the issue with dots overlapping has yet to be fixed.


<p align="center" style="font-size:11px"><iframe width="1200" height="350" src="https://jace-hambrick.github.io/space-jekyll-template/assets/asylum_scatter.html" title="Choropleth Map"></iframe>
 <i>Scatterplot Map showing individual cases.</i></p>


My goal was more or less to provide a skeleton for the rest of the team, so that they would have a starting point for any visuals they needed to create, as well as for anyone who worked on it in the future. To ensure that this was possible, I maintained a documentation file in the background, containing the basics on everything I had created. Knowing full well that at a later point it could be that my visuals were scrapped in favor of a different one, I found it prudent to provide links to numerous different python graphing programs and a few that specifically worked with those programs to draw world maps.


In the end my contribution was a massive jumpstart on visualizations. CSV files containing data were ready to go. Two different styles of scalable visuals that would grow with the data, and documentation to help anyone wanting to adjust or continue my work.


<h2>Passing on the Torch</h2>


<p align="center" style="font-size:11px"><img src="https://i.imgur.com/kU7d1q9.png" />
<i>The login site for FE's website</i></p>





Now at the end of a full month, me and my team have pushed forward and together with the Front and Back End teams we have added a number of features.


<ul>
<li>Aligned our endpoints to throughout the three teams code bases.</li>
<li>Further refined the dockerfile for AWS Elastic Beanstalk</li>
<li>Deployed the functional Scraper application to AWS EB</li>
<li>The code now reads files from BE connected S3 bucket</li>
<li>Various visualizations awaiting Front End implementation.</li>
</ul>

<p align="center" style="font-size:11px"><img src="https://i.imgur.com/ZKDmPg1.png">
<i>Docker deployment code</i></p>

<p align="center" style="font-size:11px"><img src="https://github.com/Jace-Hambrick/space-jekyll-template/blob/master/assets/DockerDeployed.gif?raw=true" />
<i>Local deployment of the Docker API application</i></p>

<p align="center" style="font-size:11px"><img src="https://i.imgur.com/nR8EmMJ.png">
<i>Front Ends advanced search application</i></p>

Future features will most likely include many more visualizations, more fields added to the data, a number of new search features on the website, improved scrappers, and a revamped website allowing for detailed viewing of information and data. Though the process of getting all of this done will be a challenge for the next team. As the data grows, creating visualization is going to get more challenging and harder to maintain, in conjunction with applying data ethics it will be no easy task. As for the rest, making sure that proper documentation is in the records, and that it seamlessly merges with the existing code bases should allow for future teams to move forward with ease. The only real technical problem that occurs to me is how to increase the efficiency of the scrapper, which at this point has some troubles with the court documents.


A month later and looking back on it, I could have done better, and it always hurts to know that one could have done better. I ran into communication problems early on with the rest of the team, and was only later able to amend them and really connect with the rest of the team. I received some feedback in regards to this and in regards to my tardiness at the start of the project. It took some personal changes to my habits and an extra cup of coffee in the morning. But I was able to get on track and move forward with my team.


I’m looking forward to seeing what the future offers me now. Having completed this project and refined my skills more, the future looks brighter. My visualizations and coding expertise will only continue to grow from here on out.

