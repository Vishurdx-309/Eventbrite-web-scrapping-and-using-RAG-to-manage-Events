# Los Angeles Event Scraper and Query System

This project is a Python-based solution designed to scrape event data for Los Angeles from Eventbrite and build a query system leveraging Retrieval-Augmented Generation (RAG). Additionally, an evaluation pipeline is included to assess the performance of the system.Wrote a python script to scrape the events for the city: Los Angeles - from eventbrite.com. The URL is: https://www.eventbrite.com/d/ca--los-angeles/all-events/ Then used RAG to ingest the events and query the events Finally, created an evaluation pipeline evaluating 10 queries on this pipeline.

## Overview

The project comprises three main components:
1. **Web Scraping**: 
   - Scrapes event details from Eventbrite's Los Angeles events page:  
     [Eventbrite Los Angeles Events](https://www.eventbrite.com/d/ca--los-angeles/all-events/).
   - Extracted data includes event names, dates, times, locations, and other relevant details.

2. **RAG Integration**:
   - Ingests the scraped event data into a RAG pipeline.
   - Enables querying event information using a natural language interface.

3. **Evaluation Pipeline**:
   - A set of 10 pre-defined queries to evaluate the performance of the RAG pipeline.
   - Measures response accuracy and relevance to ensure the system's robustness.

## How It Works

### 1. Web Scraping
- A Python script uses web scraping libraries (e.g., BeautifulSoup, Selenium) to collect event data from the Eventbrite page.
- The scraped data is stored in a structured format for ingestion into the RAG system.

### 2. Retrieval-Augmented Generation (RAG)
- The scraped data is indexed using a document store (e.g., Elasticsearch or FAISS).
- A question-answering pipeline built with RAG retrieves relevant event details and generates user-friendly responses.
- The pipeline combines a retriever for fetching data and a generator for formulating answers.

### 3. Evaluation Pipeline
- Evaluates the RAG system's performance by executing 10 test queries.
- Queries are designed to assess various aspects, such as event relevance, detail completeness, and response accuracy.

## Key Features
- **Dynamic Event Updates**: Automatically fetches the latest event details from Eventbrite.
- **Intelligent Querying**: Supports natural language queries like "What are the best concerts this weekend in Los Angeles?".
- **Evaluation and Metrics**: Provides insights into the pipeline's accuracy and areas for improvement.

## Prerequisites
- Python 3.7 or later
- Required Python libraries:
  - `beautifulsoup4`
  - `selenium`
  - `langchain` or similar library for RAG
  - `elasticsearch` or `faiss`
