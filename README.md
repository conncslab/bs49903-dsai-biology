# BS49903 — Data Science and AI for Biology

**Lecturer:** [Lecturer name, affiliation]
**Contact:** [email]
**Term / Institution:** [e.g. Fall 2026, Department of ...]

Course materials for BS49903, *Data Science and AI for Biology* (DSAI for Biology):
[one or two sentences describing what the course covers and who it is for].

All code in this course is written for **Python 3.12**.

---

## Setup

The instructions below use **Miniconda** to create an isolated virtual environment so
that the packages for this course don't interfere with anything else on your system.

If you don't have Miniconda yet, download and install it first:
https://www.anaconda.com/docs/getting-started/miniconda/install

### 1. Clone the repository

```bash
git clone https://github.com/conncslab/bs49903-dsai-biology.git
cd bs49903-dsai-biology
```

### 2. Create and activate the virtual environment

Pick the section for your operating system.

<details open>
<summary><b>Windows</b></summary>

Open the **Anaconda Prompt** from the Start menu (not the regular Command Prompt —
`conda` is only on the PATH there by default), then run:

```bat
conda create -n dsai-bio python=3.12
conda activate dsai-bio
```

</details>

<details open>
<summary><b>macOS</b></summary>

Open **Terminal** and run:

```bash
conda create -n dsai-bio python=3.12
conda activate dsai-bio
```

If `conda` is not found, initialize your shell once with `conda init zsh`
(or `conda init bash`), then close and reopen the Terminal.

</details>

Once the environment is active, your prompt will be prefixed with `(dsai-bio)`.

### 3. Install the required packages

Same command on both platforms:

```bash
pip install -r requirements.txt
```

### 4. Register the environment as a Jupyter kernel

```bash
python -m ipykernel install --user --name dsai-bio --display-name "Python 3.12 (dsai-bio)"
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

This opens Jupyter in your browser. Open any notebook from this repository and make
sure the kernel in the top-right corner is set to **Python 3.12 (dsai-bio)**.

---

## Required packages

| Package | Purpose |
| --- | --- |
| numpy | Array and matrix computation |
| scipy | Scientific computing, signal processing, statistics |
| pandas | Tabular data handling |
| tifffile | Reading and writing TIFF images and image stacks |
| scikit-learn | Machine learning |
| matplotlib | Plotting |
| seaborn | Statistical plotting |
| notebook | Jupyter Notebook interface |

Exact version requirements are listed in [`requirements.txt`](requirements.txt).

---

## Every session after the first

You only need to create the environment once. To resume work later:

```bash
cd bs49903-dsai-biology
conda activate dsai-bio
jupyter notebook
```

To get the latest course materials:

```bash
git pull
```

---

## Repository structure

```
bs49903-dsai-biology/
├── README.md
├── requirements.txt
├── notebooks/        # Lecture notebooks
├── data/             # Example datasets
└── solutions/        # Exercise solutions
```

---

## Troubleshooting

**`conda: command not found`** — On Windows, use the Anaconda Prompt. On macOS, run
`conda init zsh` and restart the Terminal.

**`git: command not found`** — Install Git from https://git-scm.com/downloads
(macOS users can also run `xcode-select --install`).

**Notebook can't import a package** — Check that the kernel is set to
**Python 3.12 (dsai-bio)** and that `conda activate dsai-bio` was run before
launching Jupyter.

**Removing the environment and starting over:**

```bash
conda deactivate
conda env remove -n dsai-bio
```

---

## License

[e.g. MIT for code, CC BY 4.0 for course materials]
