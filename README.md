# App-Reviews_Sentiments-Analaysis

This project analyzes user reviews of the LinkedIn app to classify them as **Positive**, **Negative**, or **Neutral** based on sentiment polarity using the TextBlob library.

## Project Overview

- Load and explore LinkedIn app reviews dataset.
- Visualize distribution of ratings and sentiments.
- Perform sentiment analysis with TextBlob.
- Visualize results using pie charts, bar plots, and word clouds.
- Export the analyzed data for further use.

## Project Structure

```
linkedin-sentiment-analysis/
│
├── data/
│   └── linkedin-reviews.csv        # Dataset file
├── notebook/
│   └── sentiment_analysis.ipynb    # Jupyter/Colab notebook
├── requirements.txt                # Project dependencies
└── README.md                      # Project documentation
```

## How to Run

1. Clone this repo.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook (`Sentiment_Analysis.ipynb`) in Jupyter or Google Colab.
4. Alternatively, run the script if you have a Python script version.

## Dependencies

- pandas
- matplotlib
- seaborn
- textblob
- wordcloud
- nltk

## Sample Sentiment Analysis Code Snippet

```python
from textblob import TextBlob

def textblob_sentiment_analysis(review):
    sentiment = TextBlob(review).sentiment
    if sentiment.polarity > 0.1:
        return "Positive"
    elif sentiment.polarity < -0.1:
        return "Negative"
    else:
        return "Neutral"
```

## Future Improvements

- Use advanced NLP models like VADER or BERT.
- Build an interactive web app using Streamlit.
- Include time-series analysis if review timestamps are available.

---

Made with ❤️ by [Saril Pandey]

Feel free to contribute or raise issues!
