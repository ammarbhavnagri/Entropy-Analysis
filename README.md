# Language Entropy

This folder contains materials for the **entropy analysis** component of the **Heritage Phonology and Syntax** project (Jazmin’s Honors Capstone). The goal is to compute **language entropy** from our **Bilingual Language Profile (BLP)** language background questionnaire data.

### What the analysis materials include

The core analysis is implemented in an R Markdown file:

`BLP_language_entropy_protocol.Rmd`

This `.Rmd` walks through:

1. What **language entropy** is and how it is calculated.
2. Loading the BLP Excel data.
3. Extracting the relevant BLP responses about language use with:
   - Friends
   - Family
   - School/work
4. Converting self-reported percentages into **proportions**.
5. Reshaping the data and running the `languageEntropy` R package.
6. Summarizing and plotting the resulting entropy scores.
7. Creating a **global entropy score per participant** and saving outputs to CSV.

---

## Software requirements

This analysis is written in **R**, and all work should be done in **RStudio**.

You need both of the following installed on your machine:

1. **R** (base language)
   Download from:
   https://cran.r-project.org/

2. **RStudio Desktop** (IDE for R, free version)
   Download from:
   https://posit.co/download/rstudio-desktop/

You only need to run R directly once to confirm the installation; after that, you will work entirely in **RStudio**, opening and running the `.Rmd` file there.

---

## Quick start: running the R Markdown

If you have not used R/RStudio before, here is the short version of what to do:

1. Open **RStudio**.
2. In RStudio, go to `File → Open File...` and open:
   `BLP_language_entropy_protocol.Rmd`
   from the `Entropy analysis` folder.
3. Set the working directory so R can see the BLP Excel file in the same folder:
   `Session → Set Working Directory → To Source File Location`
4. To run the analysis:
   - Either click the green `Run` button at the top of each code chunk to step through the script, **or**
   - Click `Knit` (at the top of the editor window) to run the entire document and generate an HTML report.
5. If anything errors out, note:
   - Which chunk it happened in.
   - The error message text.

---

## Folder location and contents

All files for this piece of the project live in:

`/UIC Multilingual Phonology Lab Team Folder/Projects/PROJECT Heritage Phonology and Syntax/Data analysis/Entropy analysis/`

You should see at least the following key files:

`BLP data - PROJECT Heritage phonology and syntax.xlsx`
The BLP Excel file for this project (participant responses).

`BLP_language_entropy_protocol.Rmd`
The R Markdown file that documents and implements the entropy workflow.

`languageEntropy-1.0.1c`
The folder that houses the languageEntropy R package in case there are issues calling it from within the .Rmd

Please keep all **new CSV outputs** and any **updated scripts** in this same `Entropy analysis` folder to maintain a clean, versioned workflow for the lab.

---

## Expected deliverables

For the first full pass of this analysis, the expected outputs are:

1. A **debugged, reproducible** R Markdown file:
   - `BLP_language_entropy_protocol.Rmd` (or a copy/updated version)
   - Runs start-to-finish without errors on the current lab data.

2. **CSV output files** including:
   - Entropy by **participant** and **context**
     (friends, family, school/work).
   - A **global entropy score per participant**, averaged or otherwise summarized across contexts (as specified in the `.Rmd`).

3. A **knitted report** from the `.Rmd`:
   - HTML (preferred) or PDF.
   - Contains basic summaries of entropy values by context.
   - Includes at least one plot visualizing the distribution of entropy across contexts (e.g., boxplots or density plots).

---

## Notes on data quality and documentation

While running the analysis, keep an eye out for potential data issues, such as:

- Participants whose reported percentages do **not** sum close to 100 within a context.
- Extremely unusual entropy values that may indicate input or coding errors.

When you find issues:

- Add a brief note either in:
  - A small `README_issues.md` (or similar) in this folder, **or**
  - Comments inside the `.Rmd` near where the issue is detected.
- Include participant IDs and a short description of the problem.

This documentation will help the rest of the lab quickly understand any limitations or corrections that were made.

---

## Timeline and workflow expectations

The initial task is to:

1. Confirm that you can run the existing `.Rmd` on your machine (knit once or step through all chunks).
2. Debug and update the `.Rmd` so it runs cleanly.
3. Produce the CSV outputs and knitted report described above.

A rough target is a **one-week turnaround** for this first complete run-through, *after* confirming that R/RStudio are installed and you can open the `.Rmd`. If additional time is needed due to installation issues, package problems, or unexpected data quirks, document the blockers and communicate that to the project lead.
