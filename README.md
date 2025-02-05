 ETL Pipeline for Web Text Analysis

This project demonstrates an **ETL (Extract, Transform, Load) pipeline** that extracts text data from a webpage, processes it to remove noise and stopwords, and then analyzes the word frequency. The results are presented in a structured format using **Python**.

---

## 🛠️ Features

1. **Extract:** Scrapes textual content from a specified webpage using `requests` and `BeautifulSoup`.
2. **Transform:** Cleans the text by:
   - Removing non-alphabetic characters.
   - Tokenizing and filtering out stopwords using `nltk`.
3. **Load:** Generates a word-frequency table in the form of a Pandas DataFrame for analysis.

---

## 📦 Requirements

To run the project, ensure the following Python libraries are installed:

- **BeautifulSoup4** (for web scraping)
- **nltk** (for text processing)
- **pandas** (for tabular data manipulation)
- **requests** (for HTTP requests)

Install the required libraries using pip:

```bash
pip install beautifulsoup4 nltk pandas requests
```

---

## 🚀 How to Run

1. Clone the repository or copy the code to your local machine.
2. Install the required dependencies using the above pip command.
3. Run the Python script:

```bash
python etl_pipeline.py
```

---

## 📋 Code Workflow

### **1. Web Scraper Class**
- **Purpose:** Extracts raw text content from the webpage.
- **Key Method:** 
  - `extract_text()`: Fetches the HTML content and parses it to retrieve the text.

### **2. Test Processor Class**
- **Purpose:** Transforms raw text into cleaned, tokenized data.
- **Key Methods:**
  - `tokenize_text(text)`: Converts text into lowercase, removes stopwords, and keeps only alphabetic words.

### **3. ETL Pipeline Class**
- **Purpose:** Integrates the scraper and processor, then loads the transformed data into a Pandas DataFrame.
- **Key Method:**
  - `run()`: Executes the ETL process and outputs a sorted word-frequency table.

---

## 📊 Example Output

For the webpage `https://timesofindia.indiatimes.com/india`, the pipeline generates a word frequency table similar to:

| Word       | Count |
|------------|-------|
| modi       | 10    |
| india      | 9     |
| pm         | 9     |
| rs         | 8     |
| kumbh      | 8     |

---

## 🧪 Testing the Code

1. Modify the `url` variable in the `__main__` section to scrape any webpage of your choice:
   ```python
   url = 'https://example.com'
   ```
2. Run the script and check the word frequency output.

---

## 📖 Dependencies Overview

- **BeautifulSoup4**: Parses HTML content and extracts text.
- **nltk**: Provides tools for stopword removal and text processing.
- **requests**: Fetches the webpage's HTML content.
- **pandas**: Creates a structured DataFrame for analysis.

---

## 📝 Notes

- Ensure the target webpage allows scraping and does not block requests.
- Some websites may require additional headers (like User-Agent) for successful HTTP requests.

---

## 👨‍💻 Author

This ETL pipeline is designed to facilitate quick text analysis from online sources. Feel free to contribute and improve!
