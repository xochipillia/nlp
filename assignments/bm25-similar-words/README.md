# BM25 Similar Words

This notebook uses distributional context vectors to find words used similarly
to `time` in a sample of the Corpus of Contemporary American English (COCA)
news corpus.

It implements and compares:

- normalized BM25 with IDF and cosine similarity;
- relative frequency with cosine similarity;
- dot product and Euclidean distance;
- lemmatized and unlemmatized text;
- context windows of two and eight words;
- minimum-frequency and noun filters.

The weighting and similarity formulas are shown directly in the notebook.

## Dataset

The COCA sample is not distributed in this repository.

Place an authorized copy at:

```text
data/text_news.txt
```

See [data/README.md](data/README.md) for details.

## Environment

From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

Then start Jupyter from the assignment directory:

```bash
cd assignments/bm25-similar-words
jupyter lab
```

Run `bm25-similar-words.ipynb` from top to bottom.

## Generated Results

The notebook writes the normalized corpus and complete result tables under:

```text
results/generated/
```

That directory is ignored because it contains full-corpus derivatives and
large generated tables. The notebook retains aggregate statistics and the
most relevant result tables for inspection on GitHub.
