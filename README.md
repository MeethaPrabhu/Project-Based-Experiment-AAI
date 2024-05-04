<H3>MEETHA PRABHU</H3>
<H3>212222240065</H3>
<H3>DATE: 04.05.2024</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
To perform sentiment analysis using your Facebook data and count the number of Occurrences of <Your Name> 
<H3>Program:</H3>

```python
import pandas as pd
from textblob import TextBlob

# Read data from Excel file
data = pd.read_excel("/content/facebookcomments.xlsx")  # Replace "facebook_data.xlsx" with your file path

# Given name to count occurrences
given_name = "Meetha"

# Initialize counters for sentiment analysis and name occurrences
sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}
name_occurrences = 0

# Perform sentiment analysis and count occurrences of the given name
for index, row in data.iterrows():
    # Perform sentiment analysis
    blob = TextBlob(row['FBPost'])
    polarity = blob.sentiment.polarity
    if polarity > 0:
        sentiment_counts['positive'] += 1
    elif polarity < 0:
        sentiment_counts['negative'] += 1
    else:
        sentiment_counts['neutral'] += 1
    
    # Count occurrences of the given name
    name_occurrences += row['FBPost'].lower().count(given_name.lower())

# Print sentiment analysis results
print("Sentiment Analysis Results:")


# Print occurrences of the given name
print(f"Occurrences of '{given_name}': {name_occurrences}")
```
<H3>Output:</H3>

![image](https://github.com/Lavanyajoyce/Project-Based-Experiment-AAI/assets/119401038/4eafdfbb-6e23-4419-80de-e426016f95d9)

Show your execution results here

https://colab.research.google.com/drive/1cPrUz29_iheCRic21hyv-VCu5nQWQupQ#scrollTo=2L58Yz8tPHe5

<H3>Inference:</H3>
I have learned about the extensive usage of SENTIMENT ANLYSYS, as its not only for finding the occurance of a given word, but can also be used to 
find the positive and negative comments or Facebook posts. This can be used well in social media network to balance the usage and limit of it.
