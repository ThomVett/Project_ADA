# Projet in Applied Data Analysis

This repository contains the project that was done for the course [Applied Data Analysis](http://edu.epfl.ch/coursebook/en/applied-data-analysis-CS-401) at [EPFL](www.epfl.ch).

The aim of this project is to predict frequencies of word appearance in le journal [Le Temps](https://www.letemps.ch/) based on their archives from 1800 to 1998.

###Description of the file in the repository

What follows can serve as a short report to understand the thought process that went into the realization of this project. These notebooks are a cleaned up version of the code that was used to produce and find all the folloeing results.
- **Project_Description.md** : A detailed description of the project that was done as an introductory work to understand what had to be done over the course of the semester.
#### Exploration and extraction of the data
- **1_Exploring the Data.ipynb** : We do a first exploratory analysis of the dataset using [Spark](http://spark.apache.org/) library. We describe how the dataset and show why we choose not to use Spark because we encountered some issues that would have taken too much time to solve.
- **2_Filtering the data.ipynb** : As each file contained a lot of information a short pipeline had to be implemented to extract the raw word count of each word during each month. Here we compare a few methods on speed and qualitfy of results. 
- **3_Extracting the Data & Cleaning.ipynb** : In this notebook we apply the extraction method defined in the previous one on each month (stored on our private computers). We then desrcribe the cleaning methods that are applied to the data. We implement here custom NLP rules that can be used for the french language are we are not convinced by NLTK library toolkit. The output of this notebook is the cleaned version of the data that can be used for subsequent analysis.
- **4_First Visualisations .ipynb** : In this notebook we show a few exploratory analysis of the dataset to understand a little how it looks like!
- **5_Word Distribution.ipynb** : As in step 2 we only extract the 3000+ most frequent words we miss a part of the long tail distribution of the words. In this notebook we compute theoretically the percentage of the distribution that was missed.
- **6_Finding Patterns in the Data.ipynb** : In this notebook we describe methods that were used to find words with time series that were interesting to look at (periodic words, appearing words, disappearing words etc...)
- **7_Word Clouds..ipynb** : In this notebook we propose to implement a wordcloud gif over the year (one wordcloud per year). Unfortunately due to the noisiness of the data the result is not very nice, but it's fun to look at.
- **8_Analyzing Word Ranks.ipynb** : In this notebook we analytze the evolution of the word set over time and we find that as expected this journal uses a large wordset!
#### Predicitons
- **9_LSTM_prediction.ipynb** : Here we implement an LSTM model to try and predict a time series. The problem is framed as a regression model. The network is given previous time value and has to output the correct future value.
- **10_sarimax_model.ipynb** : Here we try to understand and implement the Sarimax model to predict word frequency. The time serie is made stationary and parameters are extracted. The model is implemented for the word "politique".
- **11_sarimax_model_for_seasonal_words.ipynb** : Here we implement the SARIMAX model to word with a seasonality and assess its viability.
- **Visualizations.ipynb** : Notebook that was used to produce the plots in the presentation.
- **Interactive_Vizualizations.ipynb** : In this notebook we provide a short overview of the two interactive visualisation plots that were implemented : Evolution of the rank of the most frequent words over time and interactive tree graph of the most frequent words, with one main node per year.

- **Images** : Images associated with the word cloud video
- **movie.gif** : Gif of the word cloud over time
- **Plots** : Plots for the visualisation
- **Data** : Cleaned data that was small enough to put on GitHub.
-**Presentation** : PDF and PPT files for the Poster Session.

###Dependencies
The project was done in Python code with the following main libraries: 

- [Numpy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [Scikit-Learn](http://scikit-learn.org/stable/)
- [Wordcloud](https://github.com/amueller/word_cloud)
- [Keras](https://keras.io/)
- [https://www.crummy.com/software/BeautifulSoup/bs4/doc/](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [http://www.statsmodels.org/dev/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html]
(http://www.statsmodels.org/dev/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html)
