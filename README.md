# SimWeave — Blog Notebooks

Companion notebooks for the [SimWeave blog](https://notabot123.github.io/simweave/blog/).
Each notebook is a runnable, visual version of its corresponding post.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/notabot123/simweave-notebooks/HEAD)

---

## Notebooks

| Notebook | Blog post |
|---|---|
| `01_suspension_dynamics.ipynb` | Suspension Dynamics: From Quarter Car to Full Vehicle |
| `02_des_vs_simpy.ipynb` | Discrete-Event Simulation: SimWeave vs SimPy |
| `03_road_traffic.ipynb` | Urban Traffic Simulation and Decision Support |
| `04_predictive_maintenance.ipynb` | Synthetic Datasets for Predictive Maintenance |
| `05_Agent_Economic_Sim.ipynb` | Agent Based Simulation |
| `06_quadcopter_flight.ipynb` | Flying a Quadcopter in Simulation |
| `07_copulas_dependence.ipynb` | When Arrivals Aren't Independent: Copulas in SimWeave |

---

## Quickstart (local)

**1. Create and activate a virtual environment**

```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS / Linux
python -m venv .venv
source .venv/bin/activate
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Launch Jupyter**

```bash
jupyter notebook
```

Then open any notebook from the file browser.

---

## Exporting plots

Each notebook includes a final cell that exports key figures as PNGs using
[Kaleido](https://github.com/plotly/Kaleido) (already in `requirements.txt`):

```python
fig.write_image('img/my_plot.png', width=1200, height=600, scale=2)
```

Run all cells top-to-bottom to populate the `img/` folder, then use those
PNGs in your Medium article.

---

## Requirements

- Python 3.10 or later
- See `requirements.txt` for all dependencies

The `simweave[viz,optim,ml]` extra pulls in Plotly, SciPy, and pandas.
`kaleido` enables static PNG export from Plotly figures.
