# NYC Parking Violations — dbt project

A small dbt pipeline and workspace for exploring and transforming NYC parking violations data using DuckDB and dbt.

## 🔎 Project overview

- **Purpose:** Transform and model NYC parking violations sample data into clean, testable tables and reports using dbt.
- **Main tech:** dbt (dbt-core, dbt-duckdb), DuckDB, Python (for utilities/notebooks).

## 📁 Repository structure (high level)

- `nyc_parking_violations_md/` — main dbt project (models, macros, seeds, tests, docs, target/ artifacts).
- `data/` — raw CSVs used for local exploration and seeding.
- `run_sql_queries.ipynb` — sample Jupyter notebook for running queries against transformed models.
- `env/` — Python virtual environment used for local development.
- `requirements.txt` — Python dependencies for the environment.

## ⚙️ Prerequisites

- Python 3.10+ (recommended)
- Git (optional)
- dbt (installed via pip in the project venv)

## 🚀 Quick setup (Windows)

1. Activate the virtual environment (PowerShell):

```powershell
# PowerShell
.\env\Scripts\Activate.ps1
# or (cmd)
.\env\Scripts\activate.bat
```

2. Install Python dependencies:

```bash
pip install -r requirements.txt
```

3. Ensure `profiles.yml` is configured where dbt expects it (see `nyc_parking_violations_md/profiles.yml`). This project is configured to use DuckDB by default.

## ▶️ Common dbt commands

Run seeds (if any):

```bash
dbt --project-dir nyc_parking_violations_md seed
```

Run models:

```bash
dbt --project-dir nyc_parking_violations_md run
```

Run tests:

```bash
dbt --project-dir nyc_parking_violations_md test
```

Generate and serve docs:

```bash
dbt --project-dir nyc_parking_violations_md docs generate
# then
dbt --project-dir nyc_parking_violations_md docs serve
```

## 🧪 Notebooks & local exploration

Open `run_sql_queries.ipynb` with Jupyter or VS Code to run SQL queries directly against DuckDB and the dbt artifacts.

## 📌 Notes

- Artifacts and run results are stored under `nyc_parking_violations_md/target/` (catalog, manifest, run_results, compiled SQL, etc.).
- Seed and sample CSV files are in `data/` (and `nyc_parking_violations_md/seeds/` if you add them there).

## 📄 License

This project is licensed under the MIT License — see `LICENSE` for details.

For questions, message the repo owner.

