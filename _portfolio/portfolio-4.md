---
title: "Stock News Sentiment Analysis Tool"
excerpt: "Calculating the sentiment based on recent company news using BERT.<br/>"
collection: portfolio
---

This project involved the development of a **Flask** web application designed to analyze the sentiment of financial news articles related to specific stock tickers. Instead of traditional rule-based methods, this application uses **BERT (Bidirectional Encoder Representations from Transformers)** for sentiment analysis, enabling it to better understand the context and nuances in news headlines and summaries.

The application pulls real-time news data using the **News.org API**, ensuring that the articles analyzed are relevant to the user's stock ticker of interest. To prepare the text for BERT input, preprocessing steps like case normalization, tokenization, and punctuation handling were applied.

By leveraging the power of BERT, the tool can offer deeper insights into the sentiment behind news articles—whether positive, negative, or neutral—even when the sentiment is subtle or implied through context.

The results are displayed in an interactive table format, making it easy for users to browse sentiment trends and relate them to potential stock market movements. This clean and intuitive interface supports smarter, data-driven investment decisions.

For a closer look at the project, you can view the full code on [GitHub](https://github.com/wesleymeredith/Financial-News-Sentiment-Analysis).

Here's a screenshot from the tool, here I entered in NVIDIA's stock ticker NVDA:
<img src='/images/senti2.png'>
<img src='/images/senti1.png'>

There might be some future plans to integrate a paid API if I were to seriously market this because on further inspection this News.org API can be too general when it comes to web scraping.
