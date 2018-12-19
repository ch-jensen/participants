# Participants
Semantic mapping of literary participants is a linguistic endavour that includes several task. The underlying question is "who are doing what to whom?" And further "what does this interaction entail in terms of the relationship among the characters in questions?"

The present work investigates network analysis on a corpus from the Hebrew Bible. The text is from Leviticus 17-26, a legal text with a number of participants, including the Lord, Moses, Aaron, the sons of Aaron, the sons of Israel, foreigners, the brother, the neighbor, the priests, the family of the priest, and so forth. This group of characters constitute a network of relationships and interactions but traditional, non-digital approaches struggle to cope with the relative high amount of data needed for a consistent mapping. For a digital approach, the amount of data is not an issue. Rather, the more data we have, the more precise can we model the networks of the participants.

### The ETCBC database and the incorporation of participant references
The corpus for the present network analysis is derived from the ETCBC database in its [BHSA representation](https://github.com/ETCBC/bhsa). The ETCBC database contains the Hebrew text and is augmented with many linguistic annotations, such as part of speech, gender, number, object type (clause, phrase, word etc.). The database can be downloaded and accessed with the Python package [text-fabric](https://dans-labs.github.io/text-fabric/) that also comes with a catalog of functions to navigate the database and even add more features.

The notebooks in this repo present the procedure from importing a [dataset with participant reference tracking](https://github.com/ch-jensen/Talstra-participant-tracking) to adding the participant as new text-fabric features and using the features to map the networks between the participants of Lev 17-26. The original dataset used for the participant analysis is created by Eep Talstra, founder of the Eep Talstra Centre for Bible and Computer at Vrije Universiteit, Amsterdam.

### New TF features
So far, three new features have been added as extra modules to the TF-represenation of the ETCBC database. The features are available in this repo.
* *actor*: Actor references assigned to nodes of different object types (phrase atom, subphrase, and word)
* *prs_actor*: Actor references assigned to pronominal suffixes. NB: The distinction between *actor* and *prs_actor* is due to the fact that suffixes do not occupy their own slot in the database.
* *coref*: An edge feature where each referring node is linked to all the co-referring nodes in the same chapter.

## Contents
The repo contains datasets, notebooks and feature-sets for my ongoing work on participant tracking and network analysis of the literary characters of Leviticus 17-26

## Licence
This work is licensed under a Attribution-NonCommercial 4.0 International (CC BY-NC 4.0). That means:

* You may download the data and use it: process, copy, modify;
* You may use the data to create new software applications;
* You may use the data for research and publish any amount of results;
* When you publish this data or results you obtained from them, you have to comply with the following: [![DOI](https://zenodo.org/badge/156556830.svg)](https://zenodo.org/badge/latestdoi/156556830)
  * give proper attribution to the data when you use it in new applications, by citing this persistent identifier:
  * do not use the data for commercial applications without consent.
