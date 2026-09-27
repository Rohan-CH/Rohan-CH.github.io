# Rohan-CH.github.io

## 1. What This Repository Is
This repository contains the source code for a Quarto-based data science portfolio and blog. It features statistical analyses of the Gapminder dataset, demonstrating global life expectancy trends using both R and Python environments, as well as an interoperability demonstration.

## 2. What to Install First
Before building the site, ensure you have the following installed on your system:
*   **Quarto** (v1.3 or higher)
*   **R** (v4.1 or higher) - *Note: The `renv` package manager will bootstrap itself.*
*   **uv** (latest version) - For Python dependency management.

## 3. Build Instructions (Exact Commands)

**Step A: Clone the repository**
Run this in your shell to clone the project and navigate into the directory:
```bash
git clone [https://github.com/Rohan-CH/Rohan-CH.github.io.git](https://github.com/Rohan-CH/Rohan-CH.github.io.git)
cd Rohan-CH.github.io
```

**Step B: Restore the Python Environment**
Run this in your shell to use `uv` to install the Python dependencies from the lockfile:
```bash
uv sync
```

**Step C: Restore the R Environment**
Open an R console from the root of the project directory and run:
```r
renv::restore()
```
*(Type `y` if prompted to proceed).*

**Step D: Render the Website**
Run this in your shell to compile the Quarto website while forcing it to use the isolated Python virtual environment:
```bash
QUARTO_PYTHON=".venv/bin/python" quarto render
```

## 4. Where the Built Site Lands
Once the render command completes, the built HTML files will be deposited into the `docs/` folder at the root of the project. To view the site locally, simply open `docs/index.html` in any web browser.

## 5. Where the Data Comes From
The data for these posts originates from the Gapminder dataset. The data files are not committed directly to this repository; instead, they are dynamically loaded via the `gapminder` R package and `gapminder` Python library during the render step. Because the environment restoration commands (`uv sync` and `renv::restore()`) must fetch these packages from external repositories, **an active internet connection is required** to build the site from a fresh clone.