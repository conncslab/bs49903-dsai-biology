# BS49903 Data Science and AI for Biology

[![Python 3.12](https://img.shields.io/badge/python-3.12-blue.svg)](https://www.python.org/downloads/release/python-3120/)
![Last commit](https://img.shields.io/github/last-commit/conncslab/bs49903-dsai-biology)

**Lecturer:** Alex Bae<br>
**Contact:** jalexbae@kaist.ac.kr<br>
**Term / Institution:** Fall 2026, Department of Biological Sciences, KAIST

Course materials for BS49903 Data Science and AI for Biology (DS/AI for Biology).

All code in this course is written for **Python 3.12**.

**Questions?** Post them in
[Discussions](https://github.com/conncslab/bs49903-dsai-biology/discussions) so the whole
class can see the answer, or email me. See [Asking questions](#asking-questions).

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

The full list, with exact version requirements, is in
[`requirements.txt`](requirements.txt).

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

## Asking questions

Course questions go to
[**Discussions**](https://github.com/conncslab/bs49903-dsai-biology/discussions).

| Category | Use it for |
| --- | --- |
| **General Q&A** | Lectures, setup problems, anything about the course |
| **Assignment Q&A** | Assignments — describe what you tried; don't post full solutions |
| **Final project Q&A** | Project scope, data, and methods |

Search the existing threads first — someone has usually hit the same error. When you
post, paste code and error messages as text rather than screenshots, so that others
can search and copy them.

You are also welcome to email me at [jalexbae@kaist.ac.kr](mailto:jalexbae@kaist.ac.kr).
Discussions is the better place for anything the rest of the class might also be
wondering about, since everyone can read the answer.

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
jupyter kernelspec uninstall dsai-bio
```

The last line removes the Jupyter kernel entry. Without it, **Python 3.12 (dsai-bio)**
keeps appearing in the kernel menu even though the environment it points to is gone.

---

## License

MIT for code, CC BY 4.0 for course materials.
