---
title: "Stock News Sentiment Analysis Tool"
excerpt: "Calculating the sentiment based on recent company news.<br/>"
collection: portfolio
---

This project involved the development of a **Flask** web application designed to analyze the sentiment of financial news articles related to specific stock tickers. By integrating **NLTK's VADER sentiment analysis model**, the application processes news content to determine its sentiment, providing valuable insights for users to assess market trends and make informed investment decisions.

The application also pulls real-time news data using the **News.org API**, which ensures that the articles analyzed are relevant to the user's stock ticker of interest. To improve the accuracy of sentiment classification, a few preprocessing techniques were employed, such as case normalization and punctuation handling. These steps were crucial in ensuring that the sentiment results were reliable and insightful.

In addition to the sentiment analysis, the web app presents the results in a structured and interactive table format, allowing users to easily browse and interpret sentiment trends over time. This intuitive display aids in visualizing the relationship between news sentiment and potential stock market movements, enhancing decision-making capabilities for investors.

For a closer look at the project, you can view the full code on [GitHub](https://github.com/wesleymeredith/Financial-News-Sentiment-Analysis).

Here's a screenshot from the tool, here I entered in NVIDIA's stock ticker NVDA:
<img src='/images/senti2.png'>
<img src='/images/senti1.png'>

There might be some future plans to integrate a paid API if I were to seriously market this because on further inspection this News.org api can be too general when it comes to web scraping.