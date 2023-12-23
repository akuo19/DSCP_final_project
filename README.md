# DSCP final Project

## Objective:
With the upcoming presidential election, this time featuring not only the traditional competition between the two major parties but also the candidacy of Ko Wen-je from the Taiwan People's Party, both the Kuomintang (KMT) and the Democratic Progressive Party (DPP) have cultivated their supporter bases over decades in Taiwan. What piques my curiosity is how the public perceives the candidate Ko Wen-je. Therefore, I aim to collect public opinions, process the data, and visualize keywords related to Ko Wen-je.

## Dataset:
For this project, I opted to create my own dataset using Google's YouTube Data API v3. I used "柯文哲" (Ko Wen-je) as the keyword to search for relevant videos and scraped all the comments from these videos to create a dataset of public opinions. In total, I collected data from 20 videos, comprising 17,869 comments.

## Data Processing:
1. Data Collection:
    1. Utilized the YouTube API to search for the 20 most relevant videos related to Ko Wen-je.
    2. Used the YouTube API to gather comments from these 20 videos.
    3. Saved the comments in an Excel file for future use without the need to re-query the API.

2. Data Pre-processing:

    1. Converted all comments into strings.
    2. Removed duplicate comments from the same individual, retaining only one instance.
    3. Removed newline characters and spaces from the comments.
    4. Excluded comments written in simplified Chinese characters.
    5. Employed regular expressions for fuzzy searching to filter out comments related to Ko Wen-je.
    6. Formatted the timestamp of the comments to the desired format (2023-0x-xx).
3. Data Processing:

    1. Used the Jieba library for word segmentation.
    2. Added a list of "stop words" to enhance the precision of Chinese word segmentation.
    3. Calculated word frequencies to identify the most frequently occurring words in comments related to Ko Wen-je.
## Data Visualization:
1. Employed Matplotlib and Seaborn to create bar charts.
![image](https://github.com/akuo19/DSCP_final_project/assets/154663804/b5022270-ca99-45bb-9ada-c41df0aab5d3)

2. Utilized Matplotlib and Wordcloud to generate word clouds.
![image](https://github.com/akuo19/DSCP_final_project/assets/154663804/f1729791-a55c-4f4f-829f-902a5435c1b9)


# How to use this ipynb
1. Clone this repository
2. Replace the api_key with your own YouTube Data API v3 key and you are ready to go.
