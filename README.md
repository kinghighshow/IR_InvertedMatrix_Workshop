# IR-invertedmatrix-workshop

PROG8245 – Inverted Matrix Workshop, Team 1

## Team members

| Name | Student ID | Part of the notebook |
|---|---|---|
| Sultan Akinola Atanda | 9114837 | Biword and positional indexes, phrase queries, merging and submission |
| John Buni | 9115726 | Document collection and tokenizer |
| Echezona (Eche) Oji | 9078881 | Normalization pipeline and Boolean retrieval (AND, AND NOT) |
| Antonio Sainz | 9072844 | TF-IDF ranking, RAG and AI agents |

## What's in the notebook

`IR_InvertedMatrix_Workshop.ipynb` keeps all of the professor's cells and adds our own cells (marked 🧩 with the author's name) after each step:

1. **Document collection:** 20 PSF blog posts, HTML stripped, loaded in a fixed order, vocabulary checked (2,473 unique tokens)
2. **Tokenizer:** keeps contractions and version numbers like `3.13.1` as single tokens, tested against the original
3. **Normalization:** lowercasing, NLTK stop words and Porter stemming, shown step by step on one sentence
4. **Inverted index and Boolean search:** posting lists, AND and AND NOT using sorted merges, checked against a full scan
5. **Biword and positional indexes:** two phrase queries (`board of directors`, `board election candidate`) checked against the raw text
6. **TF-IDF, RAG and agents:** ranked search, a `retrieve()` function, a RAG prompt and a simulated agent tool call

There are 6 talking points in total, one or two per section.

## Dataset

- **Source:** Python Software Foundation News blog: https://pyfound.blogspot.com
- **Feed used:** https://pyfound.blogspot.com/feeds/posts/default?alt=rss
- **Size:** the 20 most recent posts at the time we collected them (November 2026), saved as `sample_docs/blog_1.txt` to `blog_20.txt`, each with the post title and body
- **Content:** PSF news such as board elections, grants, security staffing, the strategic plan and community awards
- **License:** the posts belong to the Python Software Foundation. We use them only for this non-commercial class exercise and credit the PSF as the source.

The download cell refreshes `sample_docs` from the live feed. The feed changes over time, so a later run may pick up newer posts and give slightly different results from the saved outputs.

## How to run

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate    macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

Open the notebook in VS Code, select the `.venv` kernel and use **Run All**. The NLTK stop words download inside the notebook.
