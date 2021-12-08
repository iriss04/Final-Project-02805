---
title: "The Network and basic stats"
date: 2021-11-29T23:45:51+01:00
---

In this post you will see the network of Greek mythology we created. How the information from the [Fandom wiki](https://mythus.fandom.com/wiki/Category:Greek_mythology) was extracted is detailed in [the dataset](https://iriss04.github.io/posts/data/) post.

## The network
After getting all the characters, their texts and their links the Giant Connected Component (GCC) was plotted. The characters, nodes, is given different colours to make it more visually pretty and there is added edges in between to see which characters has links to which.

- Number of isolated nodes (degree zero):  23
- Number of nodes:  523
- Number of links:  3708

Following is the visualisation of the dataset. 

![alt text for screen readers](/images/greek_network.png "Greek network")

Not to our surprise, Zeus is the biggest node. 

The ForceAtlas2 algorithm was also used when plotting the GCC to make positions of the nodes and links more understandable.

![alt text for screen readers](/images/force_atlas.png "force atlas greek network")

## Basic statistics of the network
### In and out degrees
We calculated the in and out degrees for the network and the results did not surprise us. Here you can see a bar plot of the top 15 most connected characters in our network. Zeus has the top in and out degree, which is not surprising since he is the biggest name in Greek Mythology. 

![alt text for screen readers](/images/top15_in_degree.png "in degree top 15")
The in-degree tells us the frequency that other character pages mention the character. 

![alt text for screen readers](/images/top15_out_degree.png "out degree top 15")
The out-degree tells us the frequency that a character mention other characters. 


![alt text for screen readers](/images/dist.png "distributions")
* Inward degree distribution
    * This distribution follows a power-law-like pattern. There is a significant number of characters with none-to-small amount of inward links. This means that there are a few distinct characters pointed by many, and many much less relevant characters pointed by very few.  Similar to a videogame, but not as extreme, there is a character (or a set of characters, depending on where we set the degree limit) there are a few central nodes that interact with many at some point.
* Outward degree distribution
    * Unlike the inwards degree distribution, here the most common number of degrees is  "spread" among more values. It is closer to a Poisson distribution. 


### Powerlaw
![alt text for screen readers](/images/powerlaw.jpg "powerlaw")

The powerlaw exponent $\gamma$ (alpha in our output), is $\gamma \approx 2.6$ for the in-degree network and $\gamma \approx 3.6$ for the out-degree. According to Barbasi (Barabasi, 4.7), this would put the in-degree network in the scale free regime, and the out-degree in the random network regime. 

This was expected, as multiple hubs were noticed in the in-degree network, opposed to none in the out-degree network, as is common in these networks:
In a random network most nodes have comparable degrees and hence hubs are forbidden. Hubs are not only tolerated, but are expected in scale-free networks. Furthermore, the more nodes a scalefree network has, the larger are its hubs. Indeed, the size of the hubs grows polynomially with network size, hence they can grow quite large in scalefree networks. In contrast in a random network the size of the largest node grows logarithmically or slower with N, implying that hubs will be tiny even in a very large random network. (Barbasi, 4.3)




