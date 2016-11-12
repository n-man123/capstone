#Capstone

Preliminary Project Proposal


Q.  High level description of the project: what question or problem are you addressing?

I’m working with a Palo Alto tech consulting startup, Convetit (www.convetit.com).  They are in the business of identifying SMEs (subject matter experts) and connecting them to C-suite executives of mid-to-large companies (P&G, Bayer, etc.).  The executives receive a “data dump” of relevant knowledge from these SMEs over a 4-day moderated engagement (which Convetit arranges and charges fees for).

Convetit is basically in the business of curating and amassing knowledge related to various technical  subject areas; and identifying SMEs related to those subject areas.  They have scraped “tags” (these can be thought of ’n-grams’ in NLP parlance) from tens of thousands of webpages (but primarily from Linkedin).  They have additionally identified SMEs affiliated with these tags.  I have been provided these two datasets and asked to “make sense of them” and “see what ML can reveal”.  It’s not a particularly specific request so far.  

I’m exploring NLP techniques to apply to this data to “bucketize” the tags into topics; I’m also thinking about finding associations between tags and SMEs.  This is my initial idea.  

Q. How are you presenting your work? (web app, visualization, presentation/slides, etc.)

I plan to explore how to serve web pages from Domino to present my findings.  I'll be using Flask.

Q. What ML models are you planning to use?

I'm using Gensim's LDA library to do my initial analysis.  I will also explore Google's word2vec soon.

To-Do:
Describe your techniques: break the data pipeline into portions and describe each one.
Can you anticipate problems, what are they, do you need to overcome them now? How do you overcome them?
How far do you anticipate to take the project in the allotted time frame?
Any other repos, libraries and other tools that you're considering using? Are you citing them? Are you acknowledging them for their contribution?
Data
should be a CSV or something similar representing a feature matrix
if the data requires specialized processing (e.g. MIDI files converted to feature matrix), you should provide the processed data
if the data is not tabular (i.e. can't be represented in CSV), it should should otherwise be fully processed so that it's immediately consumable by your ML algorithms
you don't have to include all your data, but you must include at least a few rows
if you're scraping, do not provide only a link to a website; provide the data already scraped.

