# Using Scattertext on BlackLab search results

We analyze how gendered verbs are within the [Brown Corpus](http://korpus.uib.no/icame/manuals/BROWN/INDEX.HTM) hosted at https://blacklab.impfic-knaw.src.surf-hosted.nl/blacklab-server/brown_corpus to show how to combine the corpus search engine [BlackLab](http://inl.github.io/BlackLab/) and the visualization tool [scattertext](https://github.com/JasonKessler/scattertext).

## Installation
Dependencies can be either installed via [pipenv](https://pipenv.pypa.io/en/latest/) or [pdm](https://pdm.fming.dev/latest/). Both will version-pin dependencies and create a virtual environment in which they are installed. This keeps the host system clean and aids reproducability.

### Pipenv
A common, mature system to create virtual Python environments.

```
pipenv shell    # create a new environment
pipenv install  # install dependencies listed in `Pipfile`
jupyter lab     # start jupyter
```

### PDM
A newer package manager system with, among other features, [improved reproducability](https://frostming.com/2021/03-26/pm-review-2021/). Not as widespread as Pipenv yet. Unlike Pipenv, PDM does not spawn a sub-shell by default and you need to prepend `pdm run` to your commands. If that mode of operation does not suit you, feel free to [activate your environment](https://pdm.fming.dev/latest/usage/venv/) instead.

```
pdm install          # install dependencies listed in `pyproject.toml` into a virtual environment
pdm run jupyter lab  # start jupyter
```

## Notebooks

> :warning: The BlackLab server at https://blacklab.impfic-knaw.src.surf-hosted.nl/blacklab-server might not be available. The quickest way to create your own is via [Docker](https://www.docker.com/), as described in this [README](https://github.com/INL/BlackLab/tree/dev/docker).

### `Blacklab_queries.ipynb`

This notebook shows how to use the [BlackLab](http://inl.github.io/BlackLab/) corpus search engine hosted at https://blacklab.impfic-knaw.src.surf-hosted.nl/blacklab-server . It shows how to conduct a basic search and browse the results.

### `verbs-detailed.ipynb`

This notebook shows how to use [BlackLab](http://inl.github.io/BlackLab/) search results as input for the [scattertext visualization](https://github.com/JasonKessler/scattertext). Here we conduct two queries, searching for words following "she" or "he". Then we compile the list of words that occurs in both search results. This list of words in transformed into a format that scattertext can understand and we create an interactive dashboard, either within Jupyter itself or as an exported HTML file.

## Results

An example of this dashboard created by the `verbs-detailed.ipynb` notebook is hosted at https://ole.mn/impfic_blacklab-and-scattertext/ .
