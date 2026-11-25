# IIIF research workflow — local JupyterLab with `uv`

## Collaborative document 

[https://edu.nl/68cfc](https://edu.nl/68cfc)

## Slides

Slides are found [here](https://4turesearchdata-carpentries.github.io/IIIF_hands_on_session_AMOLF_2026/slides/iiif-4tu-introduction.html#/make-your-image-datasets-easier-to-view-and-reuse)  

## Hands-on session

Launch the interactive JupyterLab environment.
No local installation is required.

[![Launch Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/4TUResearchData-Carpentries/IIIF_hands_on_session_AMOLF_2026/main?urlpath=lab)

## Local setup (Windows PowerShell, macOS Terminal, or Linux shell)

### Project and Environment Setup

Create a course working directory somewhere convenient, for example your home directory, and then download the course environment file.

```bash
mkdir  ~/IIIF4Research
cd ~/IIIF4Research
curl -o pyproject.toml \
https://raw.githubusercontent.com/4TUResearchData-Carpentries/IIIF_hands_on_session_AMOLF_2026/refs/heads/main/iiif_uv_workshop/pyproject.toml
```

The `pyproject.toml` file defines the Python dependencies required for this course.

Verify that the file was downloaded successfully:

```bash
ls
```

Expected output:

```bash 
pyproject.toml
```
### Create and Synchronise the Environment

**Prerequisite:** install `uv` from the [official installation guide](https://docs.astral.sh/uv/getting-started/installation/). Verify with `uv --version`.

Run:

```bash
uv sync
```

This command will:

- create a local `.venv` folder if it does not exist;
- install all packages listed in `pyproject.toml`;
- create or update the `uv.lock` file.

### Register the Environment in Jupyter

Register the course environment as a Jupyter kernel:

```bash
uv run python -m ipykernel install --sys-prefix --name iiif-4tu --display-name "Python (4TU IIIF)"

```

This makes the environment available inside JupyterLab as:

```text
Python (4TU IIIF)
```


### Launch JupyterLab

Launch JupyterLab with:

```bash
uv run jupyter lab
```

In JupyterLab, click on the button **Python (4TU IIIF)** under Notebook.


