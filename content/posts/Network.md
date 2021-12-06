---
title: "The Network"
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
We calculated the in and out degrees for the network and the results did not surprise us. Here you can see a bar plot of the top 15 most connected characters. Zeus has the top in and out degree, which is not surprising since he is the biggest name in Greek Mythology. 

![alt text for screen readers](/images/top15_in_degree.png "in degree top 15")
The in-degree tells us the frequency that other character pages mention the character. 

![alt text for screen readers](/images/top15_out_degree.png "out degree top 15")
The out-degree tells us the frequency that a character mention other characters. 


![alt text for screen readers](/images/dist.png "distributions")

![alt text for screen readers](/images/powerlaw.png "powerlaw")





