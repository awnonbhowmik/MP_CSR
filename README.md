# MP_CSR — Comprehensive Systematic Review of Microplastics

A data analysis and visualization project supporting a systematic literature review on microplastics research. The notebook processes keyword and abstract data from reviewed papers to produce publication-quality figures.

## Figures generated

| Figure | Output |
|---|---|
| Geographic distribution of study origins | `images/world_map.png` |
| Keyword word cloud | `images/wordcloud.png` |
| Top contributing journals (donut chart) | `images/journal_distribution.png` |
| Sample type distribution map | `images/sample_type_map.png` |

## Requirements

- Python 3.13+
- See [requirements.txt](requirements.txt) for all dependencies

## Setup

```bash
# 1. Clone the repository
git clone <repo-url>
cd MP_CSR

# 2. Create and activate a virtual environment
python3.13 -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Register the kernel with Jupyter
python -m ipykernel install --user --name mp_csr --display-name "MP_CSR (Python 3.13)"
```

## Usage

Open `main.ipynb` in Jupyter (or VS Code) and run all cells. NLTK resources are downloaded automatically on first run. All figures are saved to `images/` at 300 DPI.

```bash
jupyter notebook main.ipynb
```

## Repository structure

```
MP_CSR/
├── main.ipynb          # Analysis and visualization notebook
├── keywords.txt        # Keywords extracted from reviewed papers
├── abstracts.txt       # Abstracts of reviewed papers
├── data/
│   └── naturalearth_lowres.geojson   # World map base layer
├── requirements.txt
└── images/             # Generated figures (git-ignored)
```

## Data

- **keywords.txt** — 185 keyword entries collected from the reviewed papers
- **abstracts.txt** — 80 abstracts from papers included in the review
- **data/naturalearth_lowres.geojson** — Natural Earth 1:110m countries layer (bundled to avoid a runtime download dependency)
