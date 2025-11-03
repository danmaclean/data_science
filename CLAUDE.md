# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Quarto book project for a Data Science and Bioinformatics course, part of The Sainsbury Laboratory MSc in Global Plant Health. The book covers topics including genomics, data visualization, statistics, machine learning, Python programming, and literate computation.

## Build and Development Commands

### Building the Book

```bash
# Render the entire book (outputs to docs/)
quarto render

# Preview the book with live reload
quarto preview

# Render a single chapter
quarto render chapter_name.qmd
```

### Output Formats

The book is configured to produce multiple formats:
- HTML (theme: cosmo, outputs to `docs/`)
- PDF (document class: scrreprt)
- EPUB

All rendered outputs are placed in the `docs/` directory.

## Project Structure

### Quarto Configuration

The project is configured in `_quarto.yml`:
- Project type: book
- Output directory: `docs/`
- Bibliography: `references.bib`
- Comments enabled via Hypothesis

### Chapter Organization

Chapters are organized in `_quarto.yml` in this order:
1. `index.qmd` - Course introduction and schedule
2. `intro.qmd` - Introduction
3. `flippedclass.qmd` - Flipped classroom methodology
4. `howtosucceed.qmd` - Student guidance
5. Main topics section (`topics.qmd`):
   - `genomics.qmd` - Introduction to Genomics
   - `dataviz.qmd` - Data Exploration and Visualisation
   - `stats.qmd` - Understanding Statistics with Linear Models
   - `nonfreq.qmd` - Introduction to Non-Frequentist Statistics
   - `ml.qmd` - Introduction to Machine Learning
   - `python.qmd` - Beginning Programming
   - `literacy.qmd` - Literate Computation

### R Environment

The project uses `renv` for R package management:
- R version: 4.4.1
- Key packages: knitr, rmarkdown, bslib, htmltools
- Lock file: `renv.lock`

To restore the R environment:
```bash
# In R console
renv::restore()
```

### External Resources

The book links to four external chatbot applications hosted on shinyapps.io:
- Introduction to Genomics Chatbot
- Data Exploration and Visualisation Chatbot
- Understanding Statistics with Linear models Chatbot
- Introduction to Non-Frequentist Statistics Chatbot

These are configured in `_quarto.yml` under `format.html.other-links`.

## Content Guidelines

This is an educational resource for MSc students. The course follows a "flipped classroom" model where students read materials before contact sessions, then practice and discuss in class.

Course topics are divided into:
- Core parts: Sections 1, 2, 3, and 7
- Extension parts: Sections 4, 5, and 6