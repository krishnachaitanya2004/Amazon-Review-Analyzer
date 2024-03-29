# Amazon Review Analyzer

Welcome to the Amazon Review Analyzer, a Python program designed to help you make informed decisions about purchasing products on Amazon.

## Overview

This program takes an Amazon product link as input and analyzes the reviews, providing insights into whether the product is a good buy. However, the ultimate decision to purchase rests entirely with you.

## How It Works

1. **Input the Product Link:** When you provide the Amazon product link, the program initiates a web scraping process to extract reviews.

2. **Scraping and Data Storage:** The scrapper extracts reviews from the [amazon.in/product-reviews/asin](amazon.in/product-reviews/asin) page. The unique ASIN (Amazon Standard Identification Number) is extracted from the link using Python's regular expressions. Due to pagination, the program iterates through the pages, storing the reviews in a CSV file named `reviews.csv`.

3. **User Agent:** Replace **headers** variable  in  `scrapper.py` with your user agent to know what is your user agent simply google **my user agent**

4. **Sentiment Analysis:** The program uses the `vaderSentiment` Python package to analyze the tone of the reviews. Additionally, the `demoji` package is employed to handle emojis present in the reviews.

## Running the Program

To run the analyzer, follow these simple steps:

```bash
python3 analyzer.py
