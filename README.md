# Análisis de Supervivencia en EPCM Usando R

This repository contains training materials for a 1-day workshop on Survival Analysis offered by the Mexico City Prospective Study team at the Nuffield Department of Population Health, University of Oxford.

The project is set up as an **RStudio Project** with **renv** for reproducible package management.

## Getting Started

To work with this project on your machine:

### 1. Clone the repository

Use Git to clone the repository to your computer:

```bash
git clone https://github.com/diegojehu/2025-supervivencia-epcm.git
```

Then open the project in RStudio by double-clicking the `manual-de-ejercicios.Rproj` file.

---

### 2. Install `renv`

Make sure you have the {renv} package installed in your global R library:

```r
install.packages("renv")
```

---

### 3. Restore the environment

Once the project is open in RStudio, run:

```r
renv::restore()
```

This will:

* Create a project-local library under `renv/library/`
* Install the exact package versions listed in `renv.lock`

This ensures your setup matches the environment in which the training materials were developed.

---

### 4. Explore the materials

* The training manual is organized into sections, each with an `.Rmd` source file and a rendered `.html` file:

  * `01_precourse-material-spa.Rmd` / `01_precourse-material-spa.html`
  * `02_survival-analysis-spa.Rmd` / `02_survival-analysis-spa.html`
  * `03_cox-ph-models-spa.Rmd` / `03_cox-ph-models-spa.html`
  * `04_age-at-risk-spa.Rmd` / `04_age-at-risk-spa.html`
  * `05_epi-data-vis-spa.Rmd` / `05_epi-data-vis-spa.html`
* The `index.Rmd` / `index.html` contain the preface and table of contents.
* Additional resources are in the `data/` and `img/` folders.

You can knit the `.Rmd` files in RStudio to regenerate the corresponding `.html` outputs.

---

### 5. Keeping your environment in sync

* When you install new packages inside the project, run:

  ```r
  renv::snapshot()
  ```

  This updates `renv.lock` so your collaborator can reproduce the same environment.
* When your collaborator pulls updates from GitHub, they should run:

  ```r
  renv::restore()
  ```

  to install any new or updated packages.

---

### 6. Version control notes

* Commit these files:

  * `*.R`, `*.Rmd`, `*.html`
  * `manual-de-ejercicios.Rproj`
  * `README.md`, `custom.css`, `data/`, `img/`
  * `renv.lock`, `renv/activate.R`, `renv/settings.json`, and `renv/.gitignore`
* Do **not** commit the local package library or temporary files. Add this to `.gitignore`:

```
# R + RStudio
.Rhistory
.Rapp.history
.RData
.Ruserdata
.Rproj.user/

# renv local libs and staging
renv/library/
renv/staging/

# OS-specific cruft
.DS_Store
Thumbs.db
```

---

## Questions

If you run into issues setting up the environment or knitting the documents, please open an issue or reach out.

## Recommended advanced additional material:

1.  [Survival Analysis Part I: Basic concepts and first analyses](https://www.nature.com/articles/6601118)
2.  [Survival Analysis Part II: Multivariate data analysis – an introduction to concepts and methods](https://www.nature.com/articles/6601119)
3.  [Survival Analysis Part III: Multivariate data analysis – choosing a model and assessing its adequacy and fit](https://www.nature.com/articles/6601120)
4.  [Survival Analysis Part IV: Further concepts and methods in survival analysis](https://www.nature.com/articles/6601117)

