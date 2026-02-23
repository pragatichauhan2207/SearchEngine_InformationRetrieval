# SearchEngine_&_InformationRetrieval
## Topic -- Web Page Analyzer with Simhash
This project analyzes web pages using web scraping techniques and computes document similarity using Simhash.

The program:
- Extracts body text from two given URLs
- Counts word frequency (case-insensitive, alphanumeric words)
- Computes a 64-bit polynomial rolling hash for each word
- Generates a 64-bit Simhash fingerprint
- Compares similarity using Hamming distance

  ## Concepts Used

- Web Scraping (BeautifulSoup, requests)
- Regular Expressions (word extraction)
- Polynomial Rolling Hash (p = 53, mod 2^64)
- Simhash Algorithm
- Bitwise Operations (XOR, shift, OR)

## How to Run

```bash
python3 Scrapping2.py <URL1> <URL2>   #(for HashVal Script)
python3 Scrapping2.py https://example.com https://example.com  #Eg
```

## Output Explanation

## Output

- Simhash value of both URLs
- Number of common bits
- Similarity percentage

```bash
python3 Scrapping2.py <URL1>   #(for Scrapping Script)
python3 Scrapping2.py https://example.com #Eg
```

## Assumptions

- Only body text is used for similarity computation.
- Words are defined as sequences of alphanumeric characters.
- Case is ignored.
- Similarity is based on 64-bit Simhash comparison.
- bits = 64

## Time Complexity

Let:
- N = number of words in document
- U = number of unique words

Word counting: O(N)  
Simhash computation: O(U × bits)  
Hamming distance: O(bits)
