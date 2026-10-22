# Healthcare Analytics for Doctor Visits

Analysis of 5,190 people to find which health, financial, demographic and coverage factors are associated with the number of doctor visits.

Submitted for the TIRTC programme (AICTE 4-week programme extended to 8 weeks), project P2.

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels, Jupyter Notebook

## Dataset
- 5,190 records, 13 columns (one is a record number). No missing values, no duplicates.
- Supplied by the TIRTC programme with a dataset understanding guide.
- Two details come from the data, not the guide: `age` has only 12 distinct values (assumed years / 100), and `nchronic` and `lchronic` never occur together.

## Key findings
| # | Finding | Label |
|---|---|---|
| 1 | 79.8% had no visit; 93 people (1.8%) with 3+ visits account for 27.8% of all visits | Fact |
| 2 | Share visiting rises from 6.8% (0 illnesses) to 41.9% (5 illnesses); illness, reduced-activity days and health score stay significant after adjustment | Strong evidence |
| 3 | Women visit more (24.4% vs 15.6%); persists after adjustment (male OR 0.77) | Strong evidence |
| 4 | Free-repatriation cover goes with more visits (31.6% vs 17.2%; adjusted OR 1.52); this group is older and lower income | Correlation |
| 5 | The raw chronic-limitation gap (35.0% vs 18.3%) shrinks to OR 1.27 (p = 0.059) after adjusting for illness | Hypothesis: works through illness |
| 6 | Private cover shows no raw difference (20.0% vs 20.4%) | Fact |

The adjusted model explains little (pseudo R-squared 0.13). All results are associations from a single snapshot, not causes.

## Limitations
- Observational snapshot; the period behind `visits` and the units of age and income are not stated.
- Small groups (free-poor, n = 222) give wide uncertainty; visit counts are mostly zero.

## Files
| File | Description |
|---|---|
| `Healthcare_Analytics_Doctor_Visits.ipynb` | Full analysis with code, outputs and written interpretation |
| `doctor_visits.csv` | Dataset |
| `TIRTC_P2_Healthcare_Analytics_Doctor_Visits.pptx` | Project presentation |
| `figures/` | Charts saved by the notebook |

## How to run
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
jupyter notebook Healthcare_Analytics_Doctor_Visits.ipynb
```
Keep the CSV in the same folder as the notebook.

## Author
Om Bagal, B.E. Metallurgy and Materials Engineering, COEP Technological University, Pune
[GitHub](https://github.com/Om777-Stack)
