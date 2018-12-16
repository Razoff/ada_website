
<h1> The bias in international news coverage </h1>

<p> In January, the Knight Foundation issued a new report on “trust, media, and democracy.” It was a long document—71 pages, with eight headings atop 28 bullet points in the “Key Findings” section alone—and took a detailed look at why modern news organizations struggle to “fulfill their democratic responsibilities of informing the public and holding government leaders accountable.” The report identified many contributing factors, but none more than the perception among the public that the nation’s news organizations weren’t being objective. According to a Gallup-Knight survey conducted for the report, fewer than half of all Americans could think of a news source that “reports the news objectively.” Political partisanship had, apparently, so eroded trust that respondents to a “media trust scale” rated their belief in the news at an abysmal 37 out of 100.</p>

<h2> Introduction </h2>

<p>Today, people have access to more and more information. This increase in information comes in different aspect but in the end the main cause of this phenomena is the worldwide connection between people.</p>

<p>Now every event in the world can be cover and present to a global audiance in less than a couple of hours. This led to an increase of popularity for international news outlet. Those company can reach to million of people in no time.</p> 

<p>The quickness of the information highway is thrilling but it raises question. We as people have all been guilty at least onece to be a little bit too quick on jugement be it on someone or something and in an era of international coverage where international journalist are covering domestic event the question of impartility is even more actual.</p> 

<p>The goal of this blog is to highlight the notion of bias in todays jounalism. The tool we have to work on this are a the GDELT Project database and a computer.</p>

<h3> GDELT Project </h3> 

<p>Since the GDELT dataset will be our main analyse tool let's have a quick look at it. It is a project maintained by google. A huge database that is acualized every fifteen minutes with input of event all around the world.</p>

<p>To keep it simple every quarter of an hour three new files are uploaded on the server.</p> 

<li> <b>Export :</b> This file holds all the individual event and their geographical informations. It basically answers the questions: Where? Who? What? </li>

<li> <b>Mentions :</b> Each entry in this file is when a news outlet mention one event. It also holds some semantic information about the article like its tone. </li>

<li> <b>GkG :</b> It is a knowledge graph of the GDELT project  it connects every trait of all organisation and event across the planet into a single massive network that captures what’s happening around the world </li>

<p>With these informations available we could not go wrong so lets look at what we managed to get out of it.</p> 

<h2> Let's talk about news </h2>

<p>The first thing we wanted to confirm the hypothesys. Is constant lack of objectivity from news outlet ?</p>

<p>We started our investigation using tools gathered during the lecture. We noticed that on every knowledge graph sources are matched with the themes addressed in each of their article. By taking inspiration of the <i>bag of words</i> approach we managed to aggregate enough data to do a <i>bag of themes</i> matrix.</p>

<p>From this bag of word we appllied the PCA decomposition. And by using a eigenvector factorisation with some unsupervised machine learning algorithm (Kmeans) for clustering we managed to plot a map of the proximity between the 5000 news outlet with the most themes cited. </p>

<figure>
 	<img src="{{ site.baseurl }}/assets/clusters.png" alt="image">
</figure>

<p>From the results it seems fairly obvious that theme-wise news outlet are polarized. The next field we investigated was the following. We tried to find waht the underlying themes were reguarding the clustering algorithm. By diving into the decomposition we managed to output the underlying features of the themes regarding to the sources. </p>

<figure>
	<img src="{{ site.baseurl }}/assets/theme01.png" alt="image">
</figure>

<a href=http://www.google.ch/> lol </a>

<iframe src="./assets/plot_high.html" frameborder="0" scrolling="no" height="720" width="960"></iframe>

