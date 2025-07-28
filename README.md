# 620-mod6-web-scraping

### Student Name: Matthew Block
[Web Scraping Repository](https://github.com/matthewpblock/620-mod6-web-scraping/)  

See [BeautifulSoup Quickstart Guide](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#quick-start)

Choose a BeautifulSoup parser:

- 'html.parser' (default, you get this with BeautifulSoup)
- 'html5lib' (install separately if desired)

## Getting Started
Fork (copy into your GitHub account) and clone down (to your machine) this repo to get started with web scraping.

## Setup Notes
1. Setup a virtual environment:  
`py -m venv .venv`  
2. Activate the virtual environment:  
`.venv\Scripts\activate`  
3. Update pip & install requirements
`py -m pip install --upgrade pip setuptools wheel`  
`py -m pip install -r requirements.txt`
4. Set correct interpreter & kernel
5. `python -m spacy download en_core_web_sm` to install english language model


## Web Mining and Applied NLP: Web Scraping and Analysis

This project demonstrates a complete pipeline for web scraping, natural language processing (NLP), and data analysis. The primary goal is to extract an article from a web page, perform various linguistic analyses on its content using `spaCy`, and visualize the findings.

## Project Overview

The notebook `P6-web-scraping.ipynb` executes the following steps:
1.  **Web Scraping**: Fetches the HTML content of a Hackaday article about laser headlights using the `requests` library.
2.  **HTML Parsing**: Extracts the main article content from the raw HTML using `BeautifulSoup` and saves it to a local file.
3.  **Text Extraction**: Reads the saved HTML and extracts the clean, human-readable text.
4.  **Token & Lemma Analysis**:
    *   Uses the `spaCy` library to process the article text.
    *   Identifies and counts the 5 most frequent tokens and lemmas, after filtering out stopwords and punctuation.
5.  **Sentence Scoring**:
    *   Implements functions to score sentences based on the density of "interesting" tokens and lemmas.
    *   Applies these scoring functions to every sentence in the article.
6.  **Data Visualization**:
    *   Generates histograms using `matplotlib` to visualize the distribution of sentence scores.
7.  **Part-of-Speech (POS) Filtering**:
    *   Demonstrates how to refine the analysis by considering only nouns, using `spaCy`'s POS tagging capabilities.

## Getting Started

### Prerequisites
- Python 3.x
- `pip` package manager

### Setup
1.  Fork this repository to your GitHub account and clone it to your local machine.
2.  Navigate to the project directory and create a virtual environment:
    ```bash
    python -m venv .venv
    ```
3.  Activate the virtual environment:
    *   On Windows:
        ```bash
        .venv\Scripts\activate
        ```
    *   On macOS/Linux:
        ```bash
        source .venv/bin/activate
        ```
4.  Install the required packages:
    ```bash
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
5.  Download the necessary `spaCy` language model:
    ```bash
    python -m spacy download en_core_web_sm
    ```

### Usage
1.  Ensure your virtual environment is activated.
2.  Start Jupyter Notebook or JupyterLab (`jupyter notebook`).
3.  Open the `P6-web-scraping.ipynb` file and run the cells sequentially.

