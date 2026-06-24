# Freshers Training Materials

## 1. Prerequisites

- **Python 3.10 – 3.12** (tested on 3.12). Check with `python --version`.
- **Git** to clone the repository.
- A notebook environment: **VS Code** with the Jupyter extension, or
  classic **Jupyter Notebook / JupyterLab** (installed via `requirements.txt`).

Optional, only needed for specific notebooks:

- **Java 8/11/17** (with `JAVA_HOME` set) — required by `pyspark.ipynb`.
- A running **PostgreSQL** and/or **MySQL** server — required to fully run
  `database_integartion.ipynb` and the live database parts of `sqlalchemy_orm.ipynb`.

## 2. Clone the repository

```bash
git clone <your-repo-url>
cd freshers_training_materials
```

## 3. Create and activate a virtual environment

**Windows (PowerShell):**

```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```

**macOS / Linux (bash/zsh):**

```bash
python3 -m venv venv
source venv/bin/activate
```

## 4. Install the dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

## 5. Register the virtual environment as a Jupyter kernel

```bash
python -m ipykernel install --user --name freshers-training --display-name "Python (freshers-training)"
```

## 6. Open and run the notebooks

- **VS Code:** open a `.ipynb` file, then pick the
  `Python (freshers-training)` kernel in the top-right kernel selector.
- **JupyterLab / Notebook:**

  ```bash
  jupyter lab        # or: jupyter notebook
  ```

Run cells top-to-bottom (Run All), and make sure the selected kernel is the one
created in step 5.

## 7. Notebook-specific notes

- **`10.django_rest_framework.ipynb`** is fully self-contained: it configures
  Django in-memory with `settings.configure()` and uses an in-memory SQLite
  database, so every example runs without creating a Django project. Just run the
  cells from top to bottom.
- **`FastAPI.ipynb`** writes a `main.py` file and shows `uvicorn main:app --reload`.
  Run that command in a terminal (not inside the notebook) to start the server.
- **`pyspark.ipynb`** needs Java installed and on the `PATH`.
- **`database_integartion.ipynb`** needs a real PostgreSQL/MySQL server and valid
  connection credentials.

## 8. Troubleshooting

- **"Kernel not found" / wrong Python:** ensure the virtual environment is
  activated and you selected the `Python (freshers-training)` kernel (step 5).
- **`ModuleNotFoundError`:** the kernel is not using the venv. Re-run steps 3–6.
- **PySpark errors about Java:** install a JDK and set `JAVA_HOME`.
- **Database connection errors:** confirm the DB server is running and the host,
  port, user, and password in the notebook match your local setup.
