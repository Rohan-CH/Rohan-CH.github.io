# Rohan-CH.github.io

## How to Build This Site

**Prerequisites:** Ensure you have [Quarto](https://quarto.org/), R, and [`uv`](https://docs.astral.sh/uv/) installed on your system.

### 1. Clone the Repository
```bash
git clone [https://github.com/Rohan-CH/Rohan-CH.github.io.git](https://github.com/Rohan-CH/Rohan-CH.github.io.git)
cd Rohan-CH.github.io
```

### 2. Restore the Python Environment
This project uses `uv` for Python dependency management. To restore the environment and install packages from the lockfile, run:
```bash
uv sync
```

### 3. Restore the R Environment
This project uses `renv` for R dependency management. Open an R console in the project root and run:
```r
renv::restore()
```

### 4. Render the Website
To compile the Quarto website while forcing it to use the isolated Python virtual environment, run the following command in your terminal from the project root:
```bash
QUARTO_PYTHON=".venv/bin/python" quarto render
```