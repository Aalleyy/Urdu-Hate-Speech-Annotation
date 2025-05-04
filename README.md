# Urdu Sentence Annotation for Hate Speech Detection

## **Objective**
The objective of this assignment was to scrape Urdu comments from YouTube videos and label them as offensive, hateful, or neutral to build a dataset for hate speech detection. The dataset is meant to aid in training machine learning models for detecting hate speech in the Urdu language. The assignment involved several pipelining phases, including data collection, preprocessing, and labeling.

The key objective of this assignment was to:

- Collect 300 Urdu comments (100 from each category: offensive, hateful, and neutral).

- Clean the collected text to remove irrelevant characters.

- Label the comments based on their content into three categories: offensive, hateful, or neutral.

- Validate the annotation with the help of a peer

## **Data Collection**

The data collection was carried out by scraping YouTube comments using the YouTube Data API. Several YouTube video URLs were chosen from Urdu news, political, and cultural discussions, where comments might include offensive or hateful content. The process used in this project was:

**API Setup:** The `googleapiclient.discovery` module was used to interact with the YouTube Data API. The API key was obtained via the Google Developer Console.

**Video Selection:** Few YouTube videos were chosen based on their relevance to topics that could include hate speech or offensive language.

**Comment Extraction:** The comments were extracted from each video by making API calls for each video ID. The API retrieves comments, and the script ensures that it collects a sufficient number of comments by handling pagination (nextPageToken).

**Keeping only Nastaliq Urdu:** A cleaning function was applied to each comment, keeping only the relevant Urdu characters and removing non-Urdu characters.

**Sampling:** 300 comments (100 per category) were sampled randomly and saved for labeling.


## **Data Preprocessing**
The preprocessing of comments included:

**Text Cleaning:** Using regular expressions, all non-relevant characters were removed, leaving only the Urdu characters.

- Emojis were removed

- Non-Urdu text and numbers were removed

- Excess spaces were removed

- Empty rows were dropped

**Unicode Handling:** The text was cleaned to ensure that the dataset contains only valid Urdu characters.


## **Annotation**

The manual annotation through this script was based on the following categories:

**Offensive (o):** Comments that use profane language or derogatory remarks aimed at individuals or groups.

**Hate Speech (h):** Comments that promote hatred or violence towards specific groups, often based on religion, ethnicity, or nationality.

**Neutral (n):** Comments that do not contain harmful language, hate speech, or offensive content. These are simply informational or neutral statements.


## **Validation**

The annotated dataset was validated with the help of a peer and the final dataset file `annotated_data_validated.csv` was created


## **Results**

The final dataset contains 300 comments, distributed as follows:

- 100 Offensive Comments

- 100 Hate Speech Comments

- 100 Neutral Comments

Each comment was carefully reviewed and assigned the appropriate label. The comments were saved in a `annotated_data_validated.csv` CSV file, with each comment paired with its corresponding label.
