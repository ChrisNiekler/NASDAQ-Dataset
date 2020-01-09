# NASDAQ Twitter Feed Dataset
Streaming and domain adaptation datasets based on twitter feed 
with hashtags related to NASDAQ and represents new challenges in the domains.

The dataset contains tweets from twitter crawled from 10.02.2019 til 3.12.2019.
The tweets from streaming and domain adaptation are choosen with respect to the tasks and can be found below.
All tweets are crawled that no user information is passed to us and only the tweet itself is processed. 

This repository offers two datasets.
* The prefix `nsdqs_` includes files for stream dataset
* The prefix `sentqs_` includes files for domain adaptation dataset

## NSDQ Dataset for Stream Analysis 
The main dataset file can be found in `data/nsdqs_skipgram_embedding.npy`. 
Hastags crawled: ADBE', 'GOOGL', 'AMZN', 'AAPL', 'ADSK', 'BKNG',
'EXPE', 'INTC', 'MSFT', 'NFLX', 'NVDA', 'PYPL', 'SBUX', 'TSLA' and 'XEL'.
There are number of tweets with 1000 data dimensions.

### Scenario

### Challanges
* High feature dimension compared compared to existing dataset
* High number of classes with large imbalances compared to existing dataset

### Usage
* Download data from: 
* Copy it to data/ 
* (Optional) Preprocess on your on:
- Raw tweets are at `Tweets.csv`
- Run `nsdqs_processing.py`
- This creates a basic statistical dataset description,trains the embedding and plots tsne embedding and eigenspectra which needs some time. 
- Afterwards the dataset is in `data/nsdqs_skipgram_embedding.npy` ready for usage.
  
* Demo 
Run `nsqds_demo.py` for a stream machine learning demonstration using SamKNN and RSVLQ. 
  
## SentQS Dataset for Domain Adaptation 
The main dataset file can be found in `data/sentqs_skipgram_embedding.npy`. 
Hastags crawled: 'ADBE', 'GOOGL', 'AMZN', 'AAPL', 'ADSK', 'BKNG',
'EXPE', 'INTC', 'MSFT', 'NFLX', 'NVDA', 'PYPL', 'SBUX', 'TSLA', 'XEL', __'positive', 'bad' and 'sad'__.
There are tweets encoded with 200 data dimensions 

### Scenario

### Challanges
* Real-world scenario not relying on standard image or text datafield undergoing large preprossing. 
* High number of samples compared to existing datasets
* Highly unbalanced Classes
* Domain adaptation problem implicity by using tweets from varying hashtags.

### Usage
* Download data from: 
* Copy it to data/ 
* (Optional) Preprocess on your on:
- Raw tweets are at `Tweets.csv`
- Run `sentqs_processing.py`
- This creates a basic statistical dataset description, trains the embedding and plots tsne embedding and eigenspectra which needs some time. 
- Afterward the dataset is ready for usage in `data/sentqs_skipgram_embedding.npy` for usage.
  
* Demo 
  Run `sentqs_demo.py` for a stream machine learning demonstration using SamKNN and RSVLQ. 
