---
title: "MEDIA FRAMING : THE BIAS IN INTERNATIONAL NEWS COVERAGE"
date: 2018-10-12 11:11:11 +0100
---

With the development of new technologies, people have access to tremendous amounts of sources to keep up with the events of the world. This increase of sources made it nearly impossible for people to get a sense of how biased the media are in transferring the facts and events. With an increasing number of sources, there is increasing risks of misinformation. The goal of our project is to raise awareness of the potential bias of news sources in each country and develop a visual representation to demonstrate it. To that aim, we used the dataset provided by the GDELT project which contains the key information needed to investigate international news coverage. The idea is to offer textual analysis and graphical content to present the results. We will include node graphs linking sources to one another and maps that will indicate the different characteristics of media coverage in different countries.


## Website lookup


In this section we will display a code sniplet to show how awesome this blog is

{% highlight ruby %}

def src_to_country_v2(web_data): # Look at extension if fail go for ip alpha 3 
    def extension_lookup(website):
        site, _ = get_map_site() # Get dictionary Extensions to County code
        try:
            return site[str('.') + website.split('.')[-1]]
        except:
            return None
        
    def ip_lookup(website):
        try:
            obj = IPWhois(socket.gethostbyname(website))
            results = obj.lookup_rdap(obj)
            country = pycountry.countries.get(alpha_2=results['asn_country_code'])
            return country.alpha_3
        except:
            return None
        
    def two_way_lookup(website):
        ret = extension_lookup(website)
        if ret == None:
            ret = ip_lookup(website)
            return ret
        return ret
        
    return web_data.map(lambda x: two_way_lookup(x))

{% endhighlight %}

## Map

Here is an awesome map

<figure>
	<img src="{{ site.baseurl }}/assets/plot_03.png" alt="image">
	<figcaption>
		There is the information concentration or something like that
	</figcaption>
</figure>

Pretty amazing right ?

<figure>
	<img src="{{ site.baseurl }}/assets/plot_04.png" alt="image">
	<figcaption>
		Spaaace
	</figcaption>
</figure>

The end
