# Statistical Inference on Air Pollution Data

Class project for DSCI 431 at Lehigh University (Fall 2026).

Does rush hour make the air measurably worse? This project analyzes a year of
hourly air-quality readings (March 2004 – April 2005) from a heavily polluted
Italian city, focusing on carbon monoxide (CO) and nitrogen oxides (NOx).

## What I did
- **Cleaned the data**: removed empty rows and columns and replaced the dataset's
  `-200` placeholder values with missing values (9,357 hourly readings).
- **Explored the distributions**: histograms, ECDFs and percentiles. Both pollutants
  are right-skewed, with occasional very high spikes.
- **Hypothesis testing**: one-sided Welch's t-tests comparing 8 AM (rush hour)
  with 2 PM.
- **Bootstrap simulation**: 10,000 resamples to build 95% confidence intervals
  for the average level of each pollutant.

## Key findings
- Both pollutants are significantly higher at 8 AM than at 2 PM
  (CO: t = 6.47, p ≈ 1e-10; NOx: t = 6.24, p ≈ 4e-10).
- 95% bootstrap confidence intervals for the mean: CO 2.12–2.19 mg/m³,
  NOx 242–252 ppb.

## Tech
Python · pandas · NumPy · SciPy · seaborn · Matplotlib · Jupyter

## Data
[UCI Air Quality dataset](https://archive.ics.uci.edu/dataset/360/air+quality)
(De Vito et al.), included as `AirQualityUCI.csv`.

## Run it
pip install pandas numpy scipy seaborn matplotlib
Then open `Arnold_Aidan_Chemical_Emissions.ipynb` in Jupyter or Colab.
