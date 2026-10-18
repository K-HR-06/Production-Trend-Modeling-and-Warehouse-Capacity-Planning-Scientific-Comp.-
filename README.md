# Production Trend Modeling and Warehouse Capacity Planning

A Scientific Computing coursework project that models monthly bag production and estimates when additional warehouse capacity will be needed.

The project fits a cubic polynomial to production data, then estimates when production reaches **25,000 bags per month**. It also calculates when construction should begin, allowing **13 months** to build the new warehouse.

## Dataset

The supplied dataset contains **144 production values**, labeled `M1` to `M144`.

The notebook represents these observations using time indices from `0` to `143`.

## Methods

- Load production data using pandas.
- Fit a degree-three polynomial using NumPy's `polyfit`.
- Visualize the production history and fitted curve with Matplotlib.
- Use SciPy's `fsolve` to find when the model reaches the capacity threshold.
- Subtract 13 months to estimate the construction start time.

## Tools

Python, NumPy, pandas, Matplotlib, and SciPy.

## Recorded Results

The notebook contains the following outputs:

| Estimate | Time index |
| --- | --- |
| Production reaches 25,000 bags per month | 169.374 |
| Construction start, 13 months earlier | 156.374 |

These values use the notebook's zero-based time scale, where `0` corresponds to `M1`. They are model estimates beyond the observed data, not actual production outcomes.

## Project Files

| File | Description |
| --- | --- |
| `aol_data.xlsx - in.csv` | Monthly production data |
| `ScientifcComputingAOL.ipynb` | Modeling, visualization, and capacity calculations |
| `AOL_ScientificComputing.pdf` | Project report in PDF format |
| `Case Study.pdf` | Assignment background and requirements |

## How to Run

Open the notebook in Jupyter Notebook or Google Colab with the required Python libraries installed. Place the dataset in the same working directory.

The supplied CSV uses semicolons, so update the loading line to:

```python
data = pd.read_csv("aol_data.xlsx - in.csv", sep=";")
```

Run the notebook cells in order to generate the plots and estimates.

## Authors

**Computer Science and Statistics — BINUS University**

Marcell Prasetyo

