# IR-invertedmatrix-workshop

PROG8245 – Inverted Matrix Workshop, Team #___

## Team members
- Sultan Akinola Atanda
- ________
- ________

## What's inside
`IR_InvertedMatrix_Workshop.ipynb` builds an information-retrieval pipeline end to end:

1. **Document collection**: 20 posts from an RSS feed, HTML stripped, files loaded in a fixed order, vocabulary checked against the 2000-word target
2. **Tokenizer**: keeps contractions and version numbers (`3.13`) as single tokens
3. **Normalization**: NLTK stop words + Porter stemming, with positions taken from the original token stream
4. **Inverted & positional index**: Boolean AND, exact phrase queries checked against a regex ground truth, and TF-IDF ranking

Our own work is marked **🧩 Team Talking Point** in the notebook (7 talking points plus 2 phrase query tests).

## Dataset
- **Source:** Python Software Foundation News blog, RSS feed `https://pyfound.blogspot.com/feeds/posts/default?alt=rss`
- **Size:** 20 posts (titles + post bodies), saved as `sample_docs/blog_N.txt`
- **License:** blog content © Python Software Foundation, used here for non-commercial educational purposes only. The text is fetched at run time and is not redistributed in this repo.

## Run it
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate   |   macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
python -m nltk.downloader stopwords
```
Open the notebook in VS Code, select the `.venv` kernel, and click **Run All**.
