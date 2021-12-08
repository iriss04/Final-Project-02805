---
title: "Dataset"
date: 2021-11-29T23:46:33+01:00
---

## About the dataset
The dataset we're exploring is from Greek mythology. The data used in this project was extracted from a [Fandom wiki](https://mythus.fandom.com/wiki/Category:Greek_mythology) containing all kinds of information about characters of Greek mythology. 

The dataset we extracted includes information about many categories of greek mythology. To name a few we have for example Gods, Heroes, Creatures and Peoples. The dataset includes which characters belong to which categories and text about each of them. With that we analyse each text and get a lot of information about the data. 

We chose the relevant categories:
- Gods
- Goddesses
- Creatures
- Figures
- Heroes
- Peoples
- Personifications
- Cyclopes
- Mortals
- Stubs
- Titans

After looking into greek mythology we learned that there is more to the greek gods and goddesses than we first thought. Greek mythology has shaped today's culture and traditions, directed political systems, encouraged problem solving as well as taught valuable lessens through stories and highly influenced today's literature.

Nowadays we can see greek mythology in brands, movies, culture, art and more. For example:
- Nike is amed after the Greek goddess of victory.
- Amazon is named after fierce warrior women.
- Ajax was a greek hero in the trojan war.
- Zodiac signs are named after greek mythology characters.
- Movies like "Percy Jackson and the lightning thief" and "Clash of the titans" are inspired by greek mythology.
- References like "Achilles' heel", "Pandora's box" and "Trojan horse" are known to many.

With this website we want to show you the world of greek mythology. We want to figure out if the pages of the greek characters describe them as happy/sad/violent/romantic and if this is related to a certain attribute, that is species, habitat, etc.. 

If you want to play around you can access the whole data set [here](https://github.com/iriss04/Final-Project-02805/blob/main/characters.zip).

## Data extraction
Here are the initial steps we took to extract the data. 
1) Data is extracted by generation several URL queries and issuing them to the Fandom wiki.
2) For each category (god, goddesses,..), a JSON file is downloaded.
3) Each character's info is extracted from the JSON files in a string and saved in a text file. 
4) A data frame is created with an entry (row) for each character. 
5) Further processing retrieves the connections between characters that allows us to generate a network. You can see the network and find more information on it on [the network](https://iriss04.github.io/posts/network/) post.

## Size of the dataset
- Size of dataset: 4 MB
- Number of pages: 547

