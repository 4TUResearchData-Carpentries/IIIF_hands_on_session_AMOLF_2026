# IIIF research workflow — local JupyterLab with `uv`





## Setup (Windows PowerShell, macOS Terminal, or Linux shell)

### . Project and Environment Setup

Create a course working directory somewhere convenient, for example your home directory, and then download the course environment file.

```bash
mkdir  ~/IIIF4Research
cd ~/IIIF4Research
curl -o pyproject.toml \
https://raw.githubusercontent.com/4TUResearchData-Carpentries/interoperability-climate-sciences/main/learners/files/pyproject.toml
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


