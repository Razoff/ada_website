
<h1> The bias in international news coverage </h1>

<p> In Januaryi 2018, the Knight Foundation issued a new report on “trust, media, and democracy.” It was a long document—71 pages, with eight headings atop 28 bullet points in the “Key Findings” section alone—and took a detailed look at why modern news organizations struggle to “fulfill their democratic responsibilities of informing the public and holding government leaders accountable.”</p>

<p> The report identified many contributing factors, but none more than the perception among the public that the nation’s news organizations weren’t being objective. According to a Gallup-Knight survey conducted for the report, fewer than half of all Americans could think of a news source that “reports the news objectively.” Political partisanship had, apparently, so eroded trust that respondents to a “media trust scale” rated their belief in the news at an abysmal 37 out of 100.</p>

<h2> Introduction </h2>

<p>Nowadays, people have an easy access to information. There are many explanation to this phenomena but the main reason is the worldwide connection between people via technology, in particular social media.</p>

<p>Today any event in the world can be cover and presented to a global audience in less than a couple of hours. This led to an increase of popularity for international news outlet. Those companies can reach to million of people in no time.</p> 

<p>The quickness of information sharing is thrilling but it raises question. We all  have all been guilty at least onece to be a little bit too quick on jugement whether on someone or something. Making mistake is part of the human nature, but in an era of international coverage where international journalism covers domestic events the question of impartility is even more actual.</p> 

<p>The goal of this blog is to highlight the notion of bias in today's journalism. The tool we have to work on this is the GDELT Project database. For more than two months, we worked investigating on this question using the freely provided GDELT project database, Our intention is to demonstrate that we can answer deep questions in society using no more than a computer.</p>

<h3> GDELT Project </h3> 

<p>Since the GDELT dataset will be our main analyse tool let's have a quick look at it. It is a project maintained by google. A huge database that is refreshed every fifteen minutes with input of events all around the world.</p>

<p>To keep it simple every quarter of an hour three new files are uploaded on the server.</p> 

<li> <b>Export :</b> This file holds all the individual event and their geographical informations. Essentially these files contains the information to answers the questions: Where? Who? What? </li>

<li> <b>Mentions :</b> Each entry in this file is recorded anytime when a news outlet mention one event. It also holds some semantic information about the article such as its tone. </li>

<li> <b>GkG :</b> It is a knowledge graph of the GDELT project which connects every trait of all organisation and event across the planet into a single massive network that captures what’s happening around the world </li>

<p>With these informations available the possibilities are endless.</p> 

<h2> Let's talk about news </h2>

<p>The first thing we wanted to confirm was the hypothesys. Is there a recurrent lack of objectivity from news outlet ?</p>

<p>We started our investigation using tools gathered during the ADA course. We noticed that on every knowledge graph sources are matched with the themes addressed in each of their article. Inspired by the <i>bag of words</i> approach we managed to aggregate enough data to do a <i>bag of themes</i> matrix. This matrix matches all the media source to all themes detected in the knowledge graph throughout time. The matrix contains counts which correspond to the occurence of each theme for a specicific media source</p>

<p>From this bag of word we appllied the PCA decomposition. And by using a eigenvector factorisation with an unsupervised machine learning algorithm (Kmeans) for clustering we managed to plot a map of the proximity between the 5000 news outlet according to their themes. </p>

<figure>
 	<img src="{{ site.baseurl }}/assets/clusters.png" alt="image">
</figure>

<p>From the results it seems fairly obvious that theme-wise news outlet are polarized. The next field we investigated was the following. We tried to find waht the underlying themes were reguarding the clustering algorithm. By diving into the decomposition we managed to output the underlying features of the themes regarding to the sources. Each of the following graph shows the representation of themes in an underlying feature.</p>

<figure>
	<img src="{{ site.baseurl }}/assets/theme01.png" alt="image">
</figure>

<p>Now that is something interesting! Each graph indicates that connoted themes are a very good separator between news sources. For example the first underlying feature shows that are linked to goverment oriented articles the terms looks like it might be domestic news. The second one is more oriented to the quality of life in a country. The third one is more into the reformation aspect of the society and the fourth one clearly covers conflictual news.</p>

<p>This first analyse confirm our doubts concerning the information is in fact heavily polarised. Now that the hypothesis is confirmed what does it mean for the globality of people.</p>

<h2>Who talks ?</h2>

<p>Once we figured out that the media were polarized one of the question we asked ourselves was: Is the information evenly distributed ? This question is important since that it would show if the bias is local or global. And if it is global how can one country's belief influence the others.</p> 

<p>To highlight this matter we took advantages of the geographical informations provided by the dataset. The following interactive map is showing how the information is unevenly distributed. </p>

<iframe src="./assets/plot_high_2.html" frameborder="0" scrolling="no" height="500" width="960"></iframe>

<p>The representation emphasize clearly that the ditribution of event is centered on the USA the western Europe and the some of the middle east countries. Even if there are many event in other country as well all bubbles that really stands out of the rest is for one of the region mentioned before. In the end it seems like the news selections revovles a lot around who the G8 leaders are intereted in.</p>

<p> This phenomena can be explained in different ways. First, many of the international news outlets (we are talking about the really big ones that covers everythin 24/7) are based either in the United State or in Europe (mostly England). It seems that the anglo-saxon countries holds a lot of power influence wise. Their articles are the most represented over the planet which makes at the same time very interesting and very dangerous.</p>

<!--<figure>
	<img src="{{ site.baseurl }}/assets/coverage_animation.gif" alt="image">
</figure> -->

<h2> The measure and visualisation of bias </h2>

<p>From the beginning we went through different question and analysis but we left the biggest question on hold. We found that the news were polarised and unevenly distributed but does this really mean that there is a consistant bias in the related informations ?</p>

<p>To emphasize both the polarity and the uneven ditribution and see what can be the impact for the public on the long run we focus our anlysis on the way american news sources report events all around the world.</p>

<iframe src="./assets/Bias_plot_US_news_media.html" frameborder="0" scrolling="no" height="500" width="960"></iframe>

<p>We can see that the US ar </p>

<h2> Conclusion </h2>


<p>In the end this data story proved that it in general the respresentation of the news is not neutral </p>
