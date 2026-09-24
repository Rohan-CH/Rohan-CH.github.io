# Rohan-CH.github.io

## How to Build This Site

### 1. Restore the Python Environment
This project uses `uv` for Python dependency management. To restore the environment and install packages from the lockfile, run:
`uv sync`

### 2. Restore the R Environment
This project uses `renv` for R dependency management. Open an R console in the project root and run:
`renv::restore()`

### 3. Render the Website
To compile the Quarto website while forcing it to use the isolated Python virtual environment, run the following command in your terminal from the project root:
`QUARTO_PYTHON=".venv/bin/python" quarto render`