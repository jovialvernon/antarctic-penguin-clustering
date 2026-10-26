# Clustering Antarctic Penguin Species

An unsupervised learning project exploring groups in 332 Antarctic penguin records with K-means clustering.

Completed as a [DataCamp project](https://app.datacamp.com/learn/projects/1809). The notebook contains my implementation of the guided challenge. The supplied project credits Dr. Kristen Gorman and Palmer Station, Antarctica LTER as the original data source.

## Objective

Identify and describe groups of penguins using physical measurements and sex, without species labels.

## Workflow

- Inspect the five-column dataset and encode sex with dummy variables.
- Standardize the four physical measurements and encoded sex using `StandardScaler`.
- Compare K-means inertia for 1–9 clusters using an elbow plot.
- Fit a six-cluster model and visualize the groups by culmen length and depth.
- Summarize mean culmen length, culmen depth, flipper length, and body mass for each cluster in `stat_penguins`.

## Results

The selected six-cluster model has inertia of approximately **216.00**. Cluster sizes range from **29 to 78 penguins**, and mean body mass ranges from approximately **3,363 g to 5,485 g**.

The elbow method is a heuristic, and these six groups are not six confirmed species. Sex contributes to the clustering alongside the physical measurements. Species labels and external validation would be needed to assess biological correspondence.

## Files and tools

- `antarctic_penguin_clustering.ipynb`: executed notebook with the elbow plot, cluster visualization, and summary table.
- `penguins.csv`: supplied dataset with 332 rows and five columns.
- `requirements.txt`: pinned analysis dependencies.
- Tools: Python, pandas, scikit-learn, Matplotlib, and Jupyter.

## How to run

Download or clone this repository and create a Python 3.12 environment, then run:

```bash
pip install -r requirements.txt
jupyter notebook antarctic_penguin_clustering.ipynb
```

Keep the CSV alongside the notebook and run all cells in order. `random_state=42` and `n_init=10` make the initialization explicit; cluster numbers are arbitrary identifiers. The notebook was rerun successfully before publication.
