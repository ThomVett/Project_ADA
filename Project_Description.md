
---------------------------------------------------------------------------------------------------------------------------
PROJECT PROPOSAL.
---------------------------------------------------------------------------------------------------------------------------

	Project Title: 			Data Challenge - Frequencies Prediction
	Project Team: 			Thomas Vetterli(SV) ,Axel De la Harpe (SV),Olagoke Lukman Olabisi (Sys Com)
	Collaborator: 			Digital  Learning Group, EPFL.
	Project Due Date :	 	December 2016
	Project Supervisor:		Michaele Casata


---------------------------------------------------------------------------------------------------------------------------
Background
-----------------------------------------------------------------------------------------------------------------------------
This project is about data analytics. At the end of the course Applied Data Analytics at EPFL students are required to complete a project on data analytics where they try to apply the tools they have learnt in class to a real world data analytics problem. The team will build the data analytics pipeline and present the results. Usually, there are many projects that are presented to the class. Then it is up to each group to select which of the projects they should work on.

This project counts towards a successful completion of the course Applied Data Analysis.

---------------------------------------------------------------------------------------------------------------------------
Introduction
---------------------------------------------------------------------------------------------------------------------------
This work is part of the project requirement for the class Applied Data Analysis at EPFL. It aims to use various Machine Learning Algorithm to predict the observed word frequency patterns in obtained data sets. In addition to this, this project will be accompanied by various result/data visualisation  tasks to provide synopsis of our results and findings.
It uses the available datasets provided by the Digital Learning Group at  EPFL. Usually such data sets always requires a lot of cleaning/ preprocessing before they can be used for prediction. After such preprocessing we apply machine learning algorithm for predictions and thereafter provide good visualisation for any observed trend.

Below, We provide aims and objectives, a brief abstract about the project, Data description, Feasibility and risk, Deliverables and Time plan of the project. 

---------------------------------------------------------------------------------------------------------------------------
Aims And Objectives
---------------------------------------------------------------------------------------------------------------------------

	1) Perform the data preprocessing
	2) Use various Machine Learning tools to predict word frequencies
	3) Provide good visualisation of the results
	4) Master the art of working on big data and machine learning
	5) Learn how to solve various problems associated with working on big data

---------------------------------------------------------------------------------------------------------------------------
Abstract
---------------------------------------------------------------------------------------------------------------------------

In this project, we want to predict word frequencies in Le Temps data from 2000-2015 based on the data we have until 1999. 

We will start with tokenisation of the data into unique words. At this step we will have to decide how much data cleaning we want to do (NLP for word matching, spelling mistakes etc..). We will also have to filter the words and choose words that are relevant for predictions. We are thinking of looking at the number of appearances of one word in the whole dataset, and if the number is too low then we will not predict his occurence. But we still want to look at words that do not appear often to check if perhaps they are words that were only used during a specific period of time, for example only between 1850 and 1870, which would be an interesting information to highlight.

Then we will generate a time series of the frequency of each word selected previously. The occurences of words in the form of frequencies, will be plotted for a selected time bin. We could plot the frequency in a time bin of a day, a week or a month. We need to keep in mind that we have a huge amount of data (more than 250 years of newspaper parution) and that a small time bin might be irrelevant. We will then do some research on which machine learning methods is best suited for the task of predicting the frequencies of words in subsequent parution. For now a time series prediction seems to fit well with regression or a recurrent neural network but we will have to do a lot of research (Machine learning papers). We will have to think about the way to partition the data into test and training sets. We think that we will need a model per word (which means one regression per word), but this will mean having 1000 models (there are on average 1000 words that people use in the french language). As explained before, choosing only the words that are the most frequent in the whole corpus can help us reduce drastically the number of models. It could also be possible to begin by creating classes of words with unsupervised learning and then creating models for the sub classes, which will result in fewer computations. This will be done by word clustering perhaps (methods that Prof. Jaggi presented in his talk).

For the programming part, we will begin by searching the available machine learning functions in the scikit learn libraries, and once we have a basic approach with theses libraries that is valid, we will go deeper and find more advanced methods. For the NLP we will start with using the natural langage toolkit and see if it matches our needs. We are also going to learn the Spark library to implement the algorithms on the cluster.

The final part of the project will be the visualisation of the data we have predicted. We want to do a semi interactive visualisation where you can choose a word and it will show you it’s predicted time frame.

We will also be collaborating with other people as this project is of great interest, and we will get insight and help from them. 

-----------------------------------------------------------------------------------------------------------------------------
Data Description
-----------------------------------------------------------------------------------------------------------------------------

The data consists of the scanned newspapers of "*La Gazette De Lausanne*"  (1804-1997) and "*Le Journal De Genève*" (1826-1997). We have at our disposition the word content in each edition of both journals. We have 4 million press articles, and this means that we have about 20 Gb of text data. As our data consists of OCR scanning, we will have errors that will come from the scanning methods, that we will have to correct, or erase. We will also have to deal with spelling mistakes made by the journalism. One other thing that is possible is that the language will have evolved over the 200 years and the orthography of certain words will have changed. There will also be maybe abnormal characters (due to the scanning or even to the printing press). We will also deal with missing data, it is possible that some scanning entries will be missing for certain period, but we don’t know yet the structure of the data so we will find out.

As the newspapers come from two different sources we also have to pay attention to the fact that these sources can have common differences, a bias in writing style due to regional culture difference for example.

-----------------------------------------------------------------------------------------------------------------------------
Feasibility and Risks
-----------------------------------------------------------------------------------------------------------------------------
Basic word frequencies predictions using simple statistical models should be attainable with this data. Once we have that we will look for more specific insights in the data set. But we have to pay attention to set a goal that will not be too difficult to achieve. We will focus on a simple result before trying to dwell on more exotic and complicated methods. One of the risks is also that we focus on cool niche results and we don’t have time to go on to the final expected result. For example, one idea that we wanna look into is to find out if the length of the sentences used in the newspaper change over time, getting longer or shorter. But in order to be done, it is necessary to be able to separates the corpus in sentences, a task that might be hard. We could also try to plot the words that only occur in certain time periods. This would be a very interesting result but potentially time consuming and we only have to do it if the principal objective is attained and the results polished.

As machine learning has a lot of different methods and libraries it is important for us that we do not get lost when we are searching for methods and focus quite quickly on one, without loosing to much time by testing each one, as all of them have their pros and cons. Furthermore the time to learn the new libraries will start to add up.

One risk is the bias we will enter in our data during the cleaning. As we will develop a particular pipeline to clean the data (for example by matching misspelled words) we will surely not include some parts and we have to pay attention to the pipeline we create and it’s implication on our results.

As we are working with collaborators we also have to pay attention with our interactions with them. For example our timeframe has to match theirs.

One of the risks that we also have is the change in semantics of a word, but this is over the scope of this project and we will not be able to address it.

In our opinion, word usage also depends on culture and could be affected by factors that are not in our dataset, and therefore we miss some input for our predictions.

-----------------------------------------------------------------------------------------------------------------------------
Deliverables
-----------------------------------------------------------------------------------------------------------------------------
Our final result will be the predictions models of the word frequencies as well as the interactive visualisation of the time series of the most frequent words form 2000 to 2015.

We also want to be able to precisely define the accuracy of our model and highlight it with graphs illustrating the accuracy of each tested model.

We will also write a report that covers precisely our method for data extraction, data cleaning and model building. As the project involves other people we would like to produce an open algorithm so that the collaborators can iterate on our work and understand easily what we have done.

---------------------------------------------------------------------------------------------------------------------------
Projec Impact
---------------------------------------------------------------------------------------------------------------------------

	1)On completion of projects we should be able to predict patterns in word frequencies over time which 
	might be useful for pedagogical research.
	2)Project will also help to give insight into the  disappearance patterns of words over time. This might be useful 
	as a basis for linguistic research
	3)Project will enable prediction of frequencies in new class of words.
	4)It will also help reveal writing style during the various time series considered.

-----------------------------------------------------------------------------------------------------------------------------
Timeplan
-----------------------------------------------------------------------------------------------------------------------------

Until the submission of the project we have about 7 semester weeks and 5 during the winter break, so we have in total 12 weeks. There are two main parts of the project, on the one hand applying nice machine learning techniques and on the other hand providing nice insights on the data (by doing interesting visualisations for example). The breakdown of the time plan / miles stone is given below:

|WEEKS 	|TASK 	|  COMMENTS 	|  
|---	|---|---|---|---|
|1-2   	| <ul><li>Understanding Data</li><li>Cleaning data</li><li>Small Visualisation for certain time series for certain words</li></ul> | We aim to understand the data in details at this stage   	|   	  	
| 3  	|  Research of the Algorithms that are consistent with our data (time series data and prediction )	| Having understood the data, we start trying out Algorithms and fine tuning parameters 	|   	
|  4-7 	|  <ul><li>Implementation of Algorithms (*coding,testing and debugging*)</li><li>Beginnning of results visualisation </li></ul>  	|   	|   
|   8-12 | <ul><li>Result Visualisation</li><li> Report Submission </li></ul>  	|   	|   

-----------------------------------------------------------------------------------------------------------------------------
Summary of Task Flow
-----------------------------------------------------------------------------------------------------------------------------
Below we provide a graphical representation of the task flow. 

![Alt text](http://g.gravizo.com/svg?
  digraph G {
   aize ="4,4";
   node [shape=box,style=filled,color=".7 .3 1.0"];
   Data [shape=box];
   Data -> Data_preprocess [weight=8];
   Data_preprocess -> {cleaning;Analysis;Visualization} [style=bold,label="Do this on raw data.[1]"];
   cleaning -> Analysis; [style=bold,label=" 3 Actions in pipeline.From cleaning to Visualisation. [2].compare [1] and [2] "];
   Analysis -> Visualization;
   Visualization -> Extract;
   Extract -> ML;
   ML -> ML ;[style=dotted,label=" Iterate through this step for Models Selection"]
   node [shape=box,style=filled,color="gray"];
   ML -> Parameter;
   node [shape=box,style=filled,color=".7 .3 1.0"];
   Parameter -> Testing_Validation;
   Testing_Validation->Prediction
   Prediction -> Parameter
   Prediction -> Visualization1
   Visualization -> Visualization1
   {Data_preprocess;Visualization1;ML} -> Report;
   Visualization1 [label = "Trends Visualiser"]
   Testing_Validation[label = "Testing and Validation"]
   Parameter [label = "Parameter tuning and optimization of Models"]
   ML [label = "Do Machine Learning Algorithm"]
   Extract [label = "Extract clean Data"];
   Data_preprocess [label="Data Preprocessing"];
   Data [label="Data Collection"];
  }
)




-----------------------------------------------------------------------------------------------------------------------------
Conclusion
-----------------------------------------------------------------------------------------------------------------------------

In conclusion, we will start with data cleaning and data preprocessing (*Tokenization*). Then machine learning algorithms will be tested in order to come up with the optimized algorithmic solution for predicting the word frequencies. If the timeplan is respected, we will look for more specific insight in the data set. In addition to this, we will work on the interactive visualisation of the results so that they can be communicated easily. Finally we will write a report that will explain each step of our work, the methods used and the results we have been able to achieve.


