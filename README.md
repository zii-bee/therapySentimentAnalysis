# TherapySentimentAI

## Overview  
**TherapySentimentAI** is a sentiment analysis tool that evaluates the emotional tone of responses in therapy-related datasets. The analysis compares real and AI-generated datasets to assess AI's effectiveness in therapeutic communication.

## Features  
- Uses **VADER Sentiment Analysis** to compute polarity scores.  
- Identifies **key therapeutic categories** (Validation, Encouragement, Reassurance, Supportive).  
- Normalizes sentiment scores for better comparison.  
- Supports **CSV datasets** as input.  

## Usage  
1. Provide a CSV file containing a `Response` column.  
2. Run the `sentiment_analysis(input_url)` function with the file URL.  
3. The function returns a DataFrame with computed sentiment scores.  

## Dependencies  
- `pandas`  
- `nltk` (WordNet & VADER)  

## Example  
```python
import pandas as pd
import nltk
from nltk.sentiment.vader import SentimentIntensityAnalyzer
from nltk.corpus import wordnet as wn

nltk.download('vader_lexicon')
nltk.download('wordnet')

sid = SentimentIntensityAnalyzer()

df = sentiment_analysis("data.csv")
print(df.head())
```
