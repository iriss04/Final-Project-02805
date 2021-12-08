---
title: "Analysis"
date: 2021-11-29T22:46:41+01:00
---

For this part of the project we go in deeper analysis of the dataset. Here we will not go deep into how the analysis was performed, that information is available in our explainer notebook, which can be downloaded [here](https://github.com/iriss04/Final-Project-02805/blob/main/Explainer%20Notebook%20-%20Greek%20Mythology.ipynb). Here you will see the word clouds we created. Finding communities and calculate their TF-IDF. Then finally sentiment of the created communities. 

## Word clouds
Word Clouds are a very fun way to get to know your dataset better. Word clouds are a visualisation that highlights the frequency of words within a text, in our case, words within categories. The word cloud picks out the most used words and ranks them by size in an image. For our word clouds we decided to only create them for the six biggest categories. 

Those are:
- Gods
- Goddesses
- Peoples
- Creatures
- Mortals
- Titans

The six different WordClouds provides a good overview of what the gods, goddesses, peoples, creatures, mortals and titans have in their text files. 

![alt text for screen readers](/images/gods_wc.png "Gods Word Cloud")

![alt text for screen readers](/images/goddess_wc.png "Goddess Word Cloud")

![alt text for screen readers](/images/people_wc.png "People Word Cloud")

![alt text for screen readers](/images/creatures_wc.png "Creatures Word Cloud")

![alt text for screen readers](/images/mortal_wc.png "Mortals Word Cloud")

![alt text for screen readers](/images/titan_wc.png "Titans Word Cloud")

Here's an overview of what can be learned about the categories from the word clouds: 
- The gods clearly have one word in common - son. 
- The goddesses wordcloud has words as daughter and Zeus as the most mentioned ones. In greek mythology Zeus is one the main gods and is said to have a lot of lovers which probably are goddesses. 
- The people text have many familiar expressions as son, family and father. This gives an indication that the peoples text includes many family relations. - The creatures text includes words as horse, bull, monster, centaur and sphinx which is not surprising since the text most likely describe what kind of species the creatuers are.  
- In the WordCloud for the mortals three words stand out - son, king and troy. The Trojan war is a big event in the greek mythology which reflects the texts of the mortals. 
- Zeus, goddess, god and son are the most repeated words for the titans.


## Communities
For our network we identified communities with the Louvain algorithm. With this algorithm we detected 12 communities in our network, ranging from 0 to 11. The smallest community has 2 characters and the largest has 79 characters. 

Here you can see a histogram of the community size distribution. 

![alt text for screen readers](/images/community_dist.png "Distribution of communities")

From the distribution we can see how all of the communities have a distinct number of characters. The largest community has 87 characters and the second largest has 70 characters. It's interesting to see how different categories distribute down to the largest communities. Here below is a list of the number of different characters in the five largest communities.

Largest community: 
- Creature    35
- God         35
- Goddess     25
- Cyclope      2

Second largest community:
- Creature    35
- God         35
- Goddess     10
- Cyclope      2

Third largest community:
- Creature    35
- God         34
- Cyclope      2

Fourth largest community
- Creature    35
- God         27
- Cyclope      2

Fourth largest community
- Creature    35
- God         20
- Cyclope      2

All of the five largest communities include creatures, gods and cyclope. The two largest ones include goddesses as well. But none of the biggest ones include peoples or mortals for example. That means that they don't make large communities with creatures, gods and cyclopes, which is not unusual. 

## TF-IDF of communities
TF-IDF stands for term frequency-inverse document frequency and it is widely used, for example by Google search engine. This tool is a statistical measure that evaluates how relevant a word is in a document, compared to a collection of documents. To get the TF-IDF score two values are multiplied: how many times a word appears in a document and the invers document frequency of the word in a collection of documents. 

Let's look at our results:

TF for the largest communities are interesting to see but it is only showing us the most frequent words in the communities. So all of the communities could have the same words as the most frequent ones. 

The five most frequent words for each of the five largest communities are the following:
  - Largest: 'son', 'heracles', 'king', 'father', 'theseus'
  - Second largest: 'zeus', 'poseidon', 'demeter', 'hades', 'goddess'
  - Third largest: 'son', 'king', 'jason', 'bull', 'mythology'
  - Fourth largest: 'artemis', 'goddess', 'zeus', 'mythology', 'also'
  - Fifth largest: 'son', 'troy', 'achilles', 'war', 'king'

The term frequency is not as descriptive as TF-IDF, since it's only giving us the frequency of a word. TF-IDF is a very useful tool when extracting keywords from a text. The highest scoring words in the five largest communities are the most relevant to that specific community. TF-IDF gives us words that are most descriptive to that specific document, so for the largest communities, none of them get the same words. 

Five of the highest scoring words in terms of TF-IDF for the largest communities are the following: 
  - Largest: 'amphitryon', 'cetus', 'atreus', 'acrisius', 'anaxagoras'
  - Second largest: 'udc', 'amun', 'hestia', 'consort', 'persephone'
  - Third largest: 'fleece', 'talos', 'ino', 'circe', 'hnir'
  - Fourth largest: 'nike', 'arete', 'dike', 'aether', 'clotho'
  - Fifth largest: 'priam', 'patroclus', 'hector', 'neoptolemus', 'ascanius'


## Sentiment of communities
A sentiment analysis was performed using two different methods: labMT (language assessment by Mechanical Turk) and VADER.

We did the sentiment analysis on two levels, character levels and community level. With this analysis we are able to identify which are the happiest and saddest characters and also find which communities are the happiest and saddest. 

But in doing this we realised that not much sentiment can be extracted from the Fandom page, so we went out on the Internet to find an extra source that would provide us with more information about the characters.

We found [Theoi](https://www.theoi.com/), an encyclopedia-like free reference guide for greek mythology. An example of one of its pages can be found [here](https://www.theoi.com/Olympios/Zeus.html). All (or most) pages contain a section called CLASSICAL LITERATURE QUOTES, which provide a more "sentimental" description than the wiki entries.

#### Character level - LabMT

![alt text for screen readers](/images/char_labmt.png "Distribution of sentiments")
Here you can see the distribution of all characters associated sentiments.

We detected the happiest and saddest characters of the greek mythology network:

Happiest characters LabMT:
- Helios
- Selene
- Aegle
- Leto
- Persephone
- Asteria
- Eos
- Aceso
- Ariadne
- Atlas

Saddest characters LabMT:
- Eris
- Hypnos
- Ares
- Sphinx
- Cerberus
- Charybdis
- Penthesilea
- Ate
- Achlys
- Aetna


#### Character level - Vader

![alt text for screen readers](/images/char_vader.png "VADER")

Happiest characters Vader:
- Psyche
- Arete
- Artemis
- Pygmalion
- Leda
- Hermes
- Apollo
- Phoenix
- Demeter
- Aphrodite

Saddest characters Vader:
- Cerberus
- Phaethon
- Sphinx
- Ate
- Penthesilea
- Charybdis
- Dionysus
- Hypnos
- Eris
- Pelos


#### Community level 

The happiest communities for LabMT are: 
- Atlas - Maia - Pleiades 
- Apollo - Helios - Horae 
- Poseidon - Gaia - Aphrodite

The happiest communities for Vader are: 
- Thetis - Peleus - Amphitrite
- Atlas - Maia - Pleiades 
- Poseidon - Gaia - Aphrodite

The saddest communities for LabMT are: 
- Athena - Scylla - Medusa
- Muses - Hercules (1997 film) - Adonis
- Troy - Ares - Agamemnon

The saddest communities for Vader are: 
- Troy - Ares - Agamemnon 
- Athena - Scylla - Medusa 
- Muses - Hercules (1997 film) - Adonis

The above happiest communities shows that the happiest community for LabMT is actually the second happiest community of Vader. The third happiest community are equal for the two analysis methods. Both approaches have the same three communities as the saddest one but not in the same order.

Helios is the god of sun, Poseidon is the god of water, Aphrodite is the goddess of love and Gaia is the god of earth. These themes are often thought of as calm and positive.

Medusa is a monster, Heracles is god of sports and Troy is a city which is known for the big Trojan war. Not surprisingly, these characters are among the saddest communities.

![alt text for screen readers](/images/labmt_average_with_error_bars.png "LabMT error bar")

![alt text for screen readers](/images/vader_average_with_error_bars.png "VADER error bar")

In the LabMt plot the average sentiments lays between 5 to 7 for the different communities. The variation is not that wide which leads to a smaller standard devation, as showed as error bars, compared to the ones in the Vader plot. As seen in the Vader plot the range in average sentiments are broad. This is because the different sentiments for the different communitites and characters vary. This leads to greater standard deviations, hence the long error bars.

The conclusion of this is that the dictionary-based method makes the communities more positive compared to the rule-based method that overall has lesser positivity in the different communities.


