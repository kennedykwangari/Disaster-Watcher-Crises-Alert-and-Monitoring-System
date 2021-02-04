# Disaster Watcher Crises Alert, and Monitoring System. 

This is a crisis mapping platform that collects data from twitter, extracts disaster-related information from tweets, and visualizes the results on a map. It enables users to quickly locate information in different geographic areas at a glance, and to determine physical constraints caused by the disaster, such as non-accessible bridges or roads, and take an informed action. Such information helps both public officials and disaster responders (e.g., humanitarian organizations, disaster relief agencies, or local actors) answer the following questions:

When did the disaster happen?
Where are the affected areas?
What are the impacts of the disaster?

The answers to these questions provide spatial (where), temporal (when), and thematic (what) information about an event. The insights gained from real-time information analysis is valuable to decision-makers throughout each phase of a disaster, from preparedness to response and recovery.


## Assessing the implementation of Deep Learning in Humanitarian Assistance and Disaster Recovery: A case study of Integrating Twitter for crises, and disaster relief

This repository contains the code for automatically identifying and classifying the disaster/ crises related tweets. 

This project aims to convert tweets into a reliable source of information and, therefore, enable an effective use of social media messages in disaster response and recovery. It uses machine learning to identify disaster-related tweets, extract place names, and map the results. The following section presents the technical architecture and describes how the system works

## 1. Introduction
Social media is increasingly being used to broadcast useful information during local crisis situations(e.g. hurricanes, earthquakes, explosions, bombings,etc).Identifying disaster related information in social media is challenging due to the low signal-to-noise ratio.In this work we will use NLP to address this challenge.

Some of the tweets sent from mobile devices can be geotagged containing the precise location coordinates. However, only about 1% to 3% of all tweets are geotagged.Identifying the disaster related tweets along with their is highly valuable to for the first responders in the disaster and crisis situations. In this project we fist. identify the disaster related tweets from a deep learning model and then use Named Entity Recognition library to identify and map the location of the data.

## 2. Data
The natural disaster events generally generate a massive and disperse reaction in social media channels.Users usually express their thoughts and actions taken before, during, and after the storm. We used the classified crisis related tweets collection from the CrisisLex.org which is a repository of crisis-related social media data. We used the CrisisLexT6 dataset which includes Tweets from 6 crises, labeled by relatedness.

Contents: ~60K tweets posted during 6 crisis events in 2012 and 2013.
Labels: ~60,000 tweets (10,000 in each collection) were labeled by crowdsourcing workers according to relatedness (as "on-topic", or "off-topic").
The data from the following crisis events were used in this analysis :

- Flood
- Earthquake
- Hurricane
- Tornado
- Explosion
- Bombing
- Wildfire

## 3. Application
The workflow starts with the data collection process. The backend API uses a keyword-based sampling approach to collect tweets using Twitter’s streaming API. In this context, a reference dictionary of disaster-related terms, developed by CrisisLex.org, was used as keywords. CrisisLex is a lexicon of 380 disaster-related terms that frequently appeared in relevant tweets during different types of disasters between October 2012 and July 2013 in the US, Canada, and Australia.

The API then sends the tweet to the deep learning model built using TensorFlow 2.0 for Python and exposed as a Flask app. The model analyzes textual content of tweets to evaluate their relevance to floods, earthquakes, hurricanes, tornadoes, explosions, and bombings. The relevant tweets are then sent to the geoparser, which extracts place names from the text and geocodes them. Finally, the results are sent to the frontend for visualization.



![image](https://user-images.githubusercontent.com/32692718/78304887-e6bdcb00-74fc-11ea-939d-19b6334edd5e.png)

# KENNEDY KAMANDE WANGARI   :: SCT221-0147/2016

