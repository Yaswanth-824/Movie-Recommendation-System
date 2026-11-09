# Movie Recommendation Experiments

Jupyter notebooks that explore recommendations from movie metadata and user ratings. The repository contains individual experiments and a [project report](Report.pdf).

| Folder | Experiments |
| --- | --- |
| `Content_Based_Filtering/` | Bag of words, TF-IDF, BM25 and BERT |
| `Collaborative_Filtering/` | Singular value decomposition and neural collaborative filtering |

## Run locally

Use Python 3.11 and install the notebook dependencies in a virtual environment.

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter notebook
```

Open a notebook and run its cells in order. The content-based notebooks read the CSV files in their folder and may download NLTK resources or a pretrained model. The collaborative notebooks expect `ratings.dat` and `movies.dat` in their working directory. Those files are absent from the repository. The SVD notebook also references `normalized_matrix.csv`; follow its preprocessing cells before loading that matrix.

This repository is organized as notebooks and data. See [LICENSE](LICENSE) for license terms.
