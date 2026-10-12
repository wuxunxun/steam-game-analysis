# Steam Game Analysis

A Python final project for **CP388001 — Computer Programming for Data Science and Artificial Intelligence**.

This project explores associations between Steam game attributes and popularity through research-inspired data preparation, aggregation, and visualization. The planned study focuses on games released from **2020 to 2025**, using a fixed snapshot of a public dataset. The final scope and popularity measures will be confirmed after inspecting the data.

**Status:** Project setup. Data acquisition and analysis have not started.

## Quick links

| Location | Contents |
| --- | --- |
| [Code](code/) | Analysis notebooks and Python scripts |
| [Data](data/) | Downloaded source data and prepared analysis data |
| [Documents](docs/) | Research paper, references, report, and presentation materials |
| [Resources](resources/) | Figures, summary statistics, tables, and exported reports |
| [Dependencies](requirements.txt) | Python packages needed to run the project |

- [Main notebook](code/final_run.ipynb)
- [Reports](docs/report/), [research papers](docs/paper/), and [references](docs/reference/)
- [Project requirements](docs/reference/project%20requirement.docx)
- [Images](resources/images/) and [charts](resources/charts/)

## Research foundation

De Luisa, A., Hartman, J., Nabergoj, D., Pahor, S., Rus, M., Stevanoski, B., Demšar, J., & Štrumbelj, E. (2021). *Predicting the Popularity of Games on Steam*. Elektrotehniški vestnik, 88(4), 151–162.

- [Published paper](https://ev.fe.uni-lj.si/4-2021/Luisa.pdf)
- [Local paper PDF](docs/paper/Predicting%20the%20Popularity%20of%20Games%20on%20Steam.pdf)
- [Proposed dataset: FronkonGames/steam-games-dataset](https://huggingface.co/datasets/FronkonGames/steam-games-dataset)
- [Dataset files and versions](https://huggingface.co/datasets/FronkonGames/steam-games-dataset/tree/main)
- [Dataset collection code](https://github.com/FronkonGames/Steam-Games-Scraper)

The proposed dataset is an alternative to the original paper's data. Estimated owners, review counts, and concurrent players represent different measures. A dataset snapshot does not provide the paper's monthly player history by default. This project will document its chosen measures and differences from the paper.

The release period and data collection date are different: a game released in 2020 may have price and review statistics observed at the later snapshot date. Record the dataset revision and retrieval date when downloading it. Do not describe repository update dates as the collection dates of every record.

## Project structure

```text
Steam Game Analysis/
├── code/
│   └── final_run.ipynb
├── data/
├── docs/
│   ├── report/
│   ├── paper/
│   └── reference/
│       └── project requirement.docx
├── resources/
│   ├── images/
│   └── charts/
├── .venv/               # Local Python environment; excluded from Git
├── .gitignore
├── README.md
└── requirements.txt
```

Empty content folders contain `.gitkeep` so they remain visible in GitHub.

## Run locally in VS Code

Open **Steam Game Analysis** itself as the VS Code project folder. Use Python 3.14 (the initial setup version), with the Python and Jupyter extensions for notebook work.

From the terminal in the project folder, create the environment if it does not already exist:

```bash
python3 -m venv .venv
```

Activate the environment on macOS/Linux and install the dependencies:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```

For Windows PowerShell, activate it with `.venv\Scripts\Activate.ps1` instead.

In VS Code, choose **Python: Select Interpreter**, then select this project's `.venv/bin/python` (Windows: `.venv\Scripts\python.exe`). For a notebook, choose the same environment using **Select Kernel**.

To use JupyterLab:

```bash
python -m jupyterlab
```

Open [code/final_run.ipynb](code/final_run.ipynb) to begin. It currently contains the project outline and path setup; data acquisition and analysis will be added step by step after the dataset version and research questions are confirmed.

## Data and public repository

The `data/` folder is retained in Git, while its contents are excluded by default. Large downloaded datasets should stay local; this keeps the public repository practical to clone. Data acquisition instructions and source/version information will be added when the data workflow is implemented.

Python code, documents, and exported resources can be tracked. Before publishing, confirm redistribution rights for any paper PDF or third-party material; references can link to the publisher's public copy. Credentials, environment files, and local caches are excluded.

The planned public GitHub repository has not been created yet. Once published, this README's relative links will navigate to the repository folders.

## Planned workflow

1. Confirm research questions and dataset snapshot.
2. Summarize the paper and identify its data preparation methods.
3. Inspect data quality and choose a justified study subset.
4. Implement loading, cleaning, transformation, filtering, and aggregation.
5. Produce at least three visualizations and interpret the findings.
6. Prepare a 5–8 page report and a 5–8 minute presentation.
7. Run the complete analysis and check the submission materials.

## Author

XUN WU — Student ID: 695380025-4
