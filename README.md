#Capstone

Preliminary Project Proposal


1. Name, Date.

Nauman Malik, 11/3/2016

2.  High level description of the project: what question or problem are you addressing?

I’m working with a Palo Alto tech consulting startup, Convetit (www.convetit.com).  They are in the business of identifying SMEs (subject matter experts) and connecting them to C-suite executives of mid-to-large companies (P&G, Bayer, etc.).  The executives receive a “data dump” of relevant knowledge from these SMEs over a 4-day moderated engagement (which Convetit arranges and charges fees for).

Convetit is basically in the business of curating and amassing knowledge related to various technical  subject areas; and identifying SMEs related to those subject areas.  They have scraped “tags” (these can be thought of ’n-grams’ in NLP parlance) from tens of thousands of webpages (but primarily from Linkedin).  They have additionally identified SMEs affiliated with these tags.  I have been provided these two datasets and asked to “make sense of them” and “see what data science can reveal”.  It’s not a particularly specific request so far.  

3. How are you presenting your work? (web app, visualization, presentation/slides, etc.)

I’m thinking about applying NLP techniques to this data to “bucketize” the tags into topics; I’m also thinking about finding associations between tags and SMEs.  This is my initial idea.  PPT slides make sense to present the data at this point.  
However, if I end up using graph theory techniques (as suggested by Chris O.), perhaps a more intricate visualization will make sense.  

4. Whats your next step?

I have installed MySQL on my computer (since Convetit provided me the data as MySQL scripts.  
I have successfully loaded the scripts in MySQL, created tables, and uploaded the data.
I have successfully transferred the data into Pandas data frames.  
I now plan to clean the data and stem it.  I then plan to tokenize it.
I’m considering using LDA and Naive Bayes for my analysis.  

5. Data

The company provided me with data last week (after I signed an NDA). 

****************************
mysql> select count(*) from tags;
+----------+
| count(*) |
+----------+
|   107327 |
+----------+
1 row in set (0.01 sec)

mysql> select * from tags limit 5;
+--------+----------------------------------------------------------------------------------+
| tag_id | name                                                                             |
+--------+----------------------------------------------------------------------------------+
|  41953 |                                                                                  |
|  98049 | " Audio Editing, Broadcast Engineering, Client Relationship Management, Contract |
|  87866 | " Strategic Sales Planning Executive Sales Management Sales Process & Exe        |
|  58106 | "A" licensed Skydiver                                                            |
|  81241 | "Irrevocable Funeral Expense Trusts"                                             |
+--------+----------------------------------------------------------------------------------+
5 rows in set (0.00 sec)

mysql> select count(*) from prospecttags;
+----------+
| count(*) |
+----------+
|  2802783 |
+----------+
1 row in set (1.17 sec)

mysql> select * from prospecttags limit 5;
+-----------------+-------------+--------+---------------------+
| prospect_tag_id | prospect_id | tag_id | created_at          |
+-----------------+-------------+--------+---------------------+
|               1 |         387 |     37 | 2016-09-30 02:36:59 |
|               2 |         387 |   2217 | 2016-09-30 02:36:59 |
|               3 |         387 |    232 | 2016-09-30 02:36:59 |
|               4 |         387 |    224 | 2016-09-30 02:36:59 |
|               5 |         387 |    209 | 2016-09-30 02:36:59 |
+-----------------+-------------+--------+---------------------+
5 rows in set (0.01 sec)

****************************
‘tags’ table contains 107327 rows of data
‘prospecttags’ table contains 2,802,783 rows of data 
(a many-to-1 relationship exists between tags and prospects)
