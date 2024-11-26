# DDX3X Stress Granules Analysis

This repository contains the analysis pipeline for investigating stress granules in DDX3X variants using microscopy data. The analysis includes cell segmentation, stress granule detection, and statistical analysis of granule properties.

## Prerequisites

1. Install [uv](https://github.com/astral-sh/uv) for Python package management
2. Install [Quarto](https://quarto.org/docs/get-started/) for report generation

## Setup

1. Clone this repository:
```bash
git clone https://github.com/username/ddx3x-stress-granules-analyses.git
cd ddx3x-stress-granules-analyses
```

2. Use `uv sync` to create a virtual environment and install depedencies:
```bash
uv sync
```

3. Activate the virtual environment:
```bash
source .venv/bin/activate
```

## Data

The microscopy data is not included in this repository due to size constraints but is available on Zenodo (link to be added). Download and place the data in the `data/` directory.

## Running the Analysis

Generate the analysis report using Quarto:
```bash
quarto render . --output-dir report
```

This will create a `report` directory containing the complete analysis. Open `report/index.html` in your web browser to view the results.

## Directory Structure

- `data/`: Raw microscopy images (not included in repository)
- `figures/`: Generated images showing three processing stages for each analyzed image:
  1. Maximum intensity projection
  2. Filtered channel
  3. Cell and granule detection results
- `output/`: CSV files containing:
  - `granule_area.csv`: Measurements of individual stress granules
  - `granules_per_cell.csv`: Cell-level granule counts and metrics
- `plots/`: Generated plots and visualizations including:
  - Violin plots comparing granule areas across conditions
  - Violin plots showing granule count distributions
  - Bar plots of cell percentages with different granule counts
- `report/`: Generated analysis report (after running Quarto)
