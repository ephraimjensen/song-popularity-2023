# Overview

The dataset I am analyzing is a list of the 953 most popular songs of 2023 according to Spotify. Far beyond a simple list of songs, this dataset provided useful information for each song including: how many streams it has, what its peak on Spotify Charts was, the number of playlists it was included in, and more. [Link to Dataset](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)

I wanted more practice with data analytics and to explore using predictive machine learning models. 

{Provide a link to your YouTube demonstration.  It should be a 4-5 minute demo of the data set, the questions and answers, the code running and a walkthrough of the code.}

[Software Demo Video](https://www.loom.com/share/f0f1880df02c4d3ebb02106f86ca8599?sid=86e9b137-e627-4a1a-b5a7-9c32be28be3a)

# Data Analysis Results

The first question I wanted to answer was if the number of artists that worked on a song have an effect on spotify chart rankings. 
The answer that I found was that within this dataset there was not a significant difference. In the dataset 61.6% of songs were made by a single artist and 38.4% of songs were made by two or more artist. This is very close to the percentage of solo/collaborative songs for songs that reached top 50 on the Spotify Charts (59.4% solo, 40.6% collaborative) and the songs that reached top 1 on Spotify Charts (62.5% solo, 37.5% collaborative). Because the ratio of solo songs and collaborative songs did not change significantly as I filtered the dataset to only include songs that placed higher on the charts, I feel confident in asserting that having more artists on a song does not necessarily improve how far up on the Spotify Charts it reaches.

The second question I wanted to answer was if I could build a model to predict if a song has more than 500 million streams on Spotify. 
The answer was yes! I built a Random Forest Classifier model using the sklearn python module that reached 91% accuracy for classifying a song as having more than 500 million streams on Spotify. The model was very good at identifying true negatives (95.6%), but struggled a little to identify True Positives (81.8%). This model determined if a song had more than 500 million streams based on how many Spotify playlists it was in, how high it peaked on the Spotify charts, what year it was released in, how high it reached on the Apple Music charts, and the presence of live performance elements (given by a liveness_% feature).

# Development Environment

I used Visual Studio Code as my IDE and used Quarto to create notebooks that I wrote my code in.  

I wrote this program in Python using the Pandas and Scikit-Learn (Sklearn) module heavily. Pandas was core as it provided most of my data analytics and manipulation tools. Scikit-Learn provided an array of machine learning tools and was how I could build my module so easily. I also used the Plotly and Plotly Express modules to create my graphs.

# Useful Websites

{Make a list of websites that you found helpful in this project}
* [Pandas Documentation](https://pandas.pydata.org/docs/user_guide/index.html)
* [Scikit-Learn Documentation](https://scikit-learn.org/stable/)
* [I/O FLOOD](https://ioflood.com/blog/python-pandas/)

# Future Work

* Clean spotify charts dataframe column to increase accuracy
* Explore data more and answer a third question
* Try to decrease False Negatives in my model
