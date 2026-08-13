# 🇮🇳 India Measles Vaccination & Monte Carlo Transmission Model

## Integrated Epidemiological, Deterministic, Age-Structured and Monte Carlo Modelling Study

---

## 📌 Project Overview

Measles is one of the most highly transmissible vaccine-preventable diseases and requires very high population immunity to interrupt sustained transmission.

This project evaluates the relationship between **Measles-Containing Vaccine second-dose (MCV2) coverage and measles transmission in India** using an integrated modelling framework.

The project combines:

- Observational epidemiological analysis
- Deterministic SIR transmission modelling
- Age-structured transmission modelling
- Monte Carlo uncertainty analysis
- Sensitivity analysis
- Vaccination coverage and vaccine-effectiveness scenario analysis

The analysis uses Indian vaccination, measles surveillance and population data from **2014–2025**, together with a detailed age-structured model based on the **2025 Indian population**.

The central research question is:

> **What level of vaccination coverage and population protection is required to reduce measles transmission below the epidemic threshold, and how does uncertainty in vaccine effectiveness and transmission parameters affect this conclusion?**

---

# 🎯 Research Objectives

### Primary Objective

To evaluate the effect of MCV2 vaccination coverage on measles transmission dynamics and epidemic burden in India using mathematical and probabilistic modelling.

### Specific Objectives

1. Examine trends in MCV2 coverage and reported measles incidence in India from 2014–2025.
2. Quantify the association between MCV2 coverage and measles incidence.
3. Develop a deterministic SIR model to evaluate the effect of vaccination coverage on the effective reproduction number (\(R_e\)).
4. Estimate epidemic burden under different vaccination coverage scenarios.
5. Develop an age-structured transmission model using the 2025 Indian population.
6. Evaluate how vaccination distributed across age groups affects population-level protection.
7. Incorporate uncertainty in \(R_0\), vaccine effectiveness, infectious period and initial infections using Monte Carlo simulation.
8. Estimate the probability that \(R_e > 1\) under different vaccination coverage scenarios.
9. Identify the most influential parameters driving epidemic burden.
10. Evaluate the interaction between vaccine effectiveness and vaccination coverage.

---

# 🔬 Research Questions

### RQ1
How did MCV2 vaccination coverage and reported measles incidence change in India between 2014 and 2025?

### RQ2
Is higher MCV2 coverage associated with lower reported measles incidence?

### RQ3
How does increasing vaccination coverage affect \(R_e\) and epidemic burden?

### RQ4
What vaccination coverage is required to reduce \(R_e\) below 1 under deterministic assumptions?

### RQ5
How does age structure affect effective population protection?

### RQ6
How does uncertainty in epidemiological parameters affect the probability of sustained measles transmission?

### RQ7
How does vaccine effectiveness interact with vaccination coverage?

### RQ8
Which model parameters contribute most strongly to variation in epidemic burden?

---

# 🧠 Conceptual Framework

The project follows a progressive modelling framework:

```text
                 INDIAN DATA
                     │
                     ▼
        ┌─────────────────────────┐
        │ Model 2A                │
        │ Observational Analysis  │
        └────────────┬────────────┘
                     │
                     ▼
        MCV2 Coverage vs
        Measles Incidence
                     │
                     ▼
        ┌─────────────────────────┐
        │ Model 2B                │
        │ Deterministic SIR       │
        └────────────┬────────────┘
                     │
                     ▼
             R₀ → β → γ → Re
                     │
                     ▼
        Epidemic Burden Scenarios
                     │
                     ▼
        ┌─────────────────────────┐
        │ Model 2C                │
        │ Age-Structured Model    │
        └────────────┬────────────┘
                     │
                     ▼
        Age-Specific Susceptibility
        + Contact Matrix
                     │
                     ▼
        ┌─────────────────────────┐
        │ Monte Carlo Simulation  │
        │ 10,000 simulations      │
        └────────────┬────────────┘
                     │
                     ▼
        Probabilistic Re + Burden
                     │
                     ▼
        Sensitivity & Scenario
             Analysis
📊 Data
Study Period
2014–2025
Geographic Scope
India
Main Data Components
The analysis incorporated:
MCV1 vaccination coverage
MCV2 vaccination coverage
Reported measles cases
Population estimates
Measles incidence
Population age structure
💉 MCV2 Coverage Trend
MCV2 coverage increased substantially during the study period:
Year	MCV2 Coverage
2014	60%
2015	69%
2016	76%
2017	80%
2018	82%
2019	84%
2020	81%
2021	82%
2022	90%
2023	90%
2024	92%
2025	95%


Overall:
MCV2 coverage increased from 60% to 95%.
🦠 Observed Measles Incidence
Reported measles incidence changed from:
6.17 per 100,000 in 2014
to:
1.28 per 100,000 in 2025.
The relationship was not monotonic, particularly during and after the COVID-19 period.
📈 Model 2A — Observational Epidemiological Analysis
Objective
To quantify the observed association between MCV2 coverage and measles epidemiology.
Two primary relationships were examined:
MCV2 Coverage
      ↓
Reported Measles Cases
and
MCV2 Coverage
      ↓
Reported Measles Incidence
Results
MCV2 vs Reported Measles Cases
Pearson correlation:
r = -0.575
MCV2 vs Measles Incidence
Pearson correlation:
r = -0.615
This indicates a moderate inverse association between MCV2 coverage and measles incidence.
Interpretation
Higher MCV2 coverage was generally associated with lower reported measles incidence.
However, this is an observational association and does not establish causality.
Potential confounding factors include:
surveillance intensity
healthcare-seeking behaviour
COVID-19-related disruptions
population mobility
supplementary immunization activities
geographic heterogeneity
reporting completeness
🧮 Model 2B — Deterministic SIR Transmission Model
Model Structure
The classical SIR framework was used:
\[
S \rightarrow I \rightarrow R
\]where:
\(S\) = susceptible population
\(I\) = infectious population
\(R\) = recovered/immune population
The model equations were:
\[
\frac{dS}{dt}
=
-\beta\frac{SI}{N}
\]\[
\frac{dI}{dt}
=
\beta\frac{SI}{N}
-\gamma I
\]\[
\frac{dR}{dt}
=
\gamma I
\]⚙️ Model Parameters
Baseline assumptions included:
Parameter	Value
\(R_0\)	15
Infectious period	7 days
\(\gamma\)	0.142857
\(\beta\)	2.142857
Initial infections	Model scenario dependent


The basic reproduction number was:
\[
R_0=\frac{\beta}{\gamma}
\]📉 Model 2B Results
Coverage	\(R_e\)	Peak Day	Peak Infections	Total Infections	Attack Rate
60%	6.450	14	271,405	624,290	62.43%
70%	5.025	18	193,033	529,211	52.92%
80%	3.600	26	115,907	412,397	41.24%
85%	2.888	33	78,620	340,820	34.08%
90%	2.175	49	42,915	253,876	25.39%
92%	1.890	61	29,522	211,682	21.17%
94%	1.605	81	17,153	162,633	16.26%
95%	1.463	99	11,599	134,624	13.46%
96%	1.320	129	6,561	102,495	10.25%
97%	1.178	186	2,526	62,417	6.24%
98%	1.035	290	215	9,482	0.95%
99%	0.893	0	100	904	0.09%


🎯 Deterministic Transmission Threshold
The final Model 2B scenario results showed:
98% coverage → Re = 1.035
99% coverage → Re = 0.893
The interpolated threshold was approximately:
98.3% coverage
for:
\[
R_e<1
\]under the final deterministic scenario assumptions.
👥 Model 2C — Age-Structured Transmission Model
Model 2C extended the deterministic model by incorporating population age structure.
The 2025 Indian population used in the model was:
\[
N=1,463,865,525
\]The population was divided into seven age groups:
Age Group	Population	Proportion
0–11 months	32,205,042	2.2%
1–4 years	128,820,166	8.8%
5–9 years	134,675,628	9.2%
10–14 years	137,603,359	9.4%
15–24 years	248,857,139	17.0%
25–44 years	439,159,658	30.0%
45+ years	342,544,533	23.4%


The age-specific populations summed exactly to the national population.
🔗 Age-Specific Contact Matrix
A 7 × 7 age-specific contact matrix was incorporated into Model 2C.
The model was calibrated so that:
\[
R_0 \approx 15
\]under the no-vaccination scenario.
The calibrated model produced:
\[
R_0=15.0
\]💉 Routine MCV2 Vaccination Scenario
Routine vaccination was applied to:
1–4 years
5–9 years
10–14 years
At:
\[
MCV2=95\%
\]and:
\[
VE=97\%
\]effective protection among vaccinated individuals was:
\[
0.95\times0.97=0.9215
\]or:
92.15%
However, because vaccination was concentrated in specific childhood age groups, whole-population effective protection was only:
25.25%
The resulting age-structured reproduction number was:
\[
\boxed{R_e=7.409}
\]📊 Age-Structured Vaccination Scenarios
Scenario	Effective Protection	\(R_e\)
Routine MCV2 only	25.25%	7.409
Routine + 15–24	40.92%	5.835
Routine + 15–44	68.56%	4.426
Routine + all adults	90.12%	4.375
All age groups	92.15%	1.178


Key Insight
High vaccination coverage within the routine target age groups does not necessarily produce equivalent population-level protection.
🎲 Monte Carlo Simulation
Monte Carlo simulation was used to propagate uncertainty in:
vaccine effectiveness
\(R_0\)
infectious period
initial infections
A total of:
10,000 simulations per scenario
were performed.
📌 Parameter Distributions
Vaccine Effectiveness
\[
VE\sim Beta(84.269,4.766)
\]Mean:
94.65%
Median:
94.97%
95% uncertainty interval:
89.13%–98.22%
Basic Reproduction Number
\[
R_0\sim Uniform(12,18)
\]Mean simulated \(R_0\):
14.96
95% uncertainty interval:
12.15–17.83
Infectious Period
\[
D\sim Uniform(6,8)
\]days.
Initial Infections
Initial infections were sampled from a specified uncertainty range around the baseline infection seed.
📊 Monte Carlo Results
Coverage	Median \(R_e\)	95% UI	P(\(R_e>1\))
95%	1.450	0.932–2.398	94.43%
96%	1.307	0.799–2.251	84.91%
97%	1.168	0.669–2.097	70.02%
98%	1.026	0.533–1.950	52.78%
99%	0.883	0.398–1.804	38.01%
100%	0.743	0.258–1.663	25.64%


🎯 Probabilistic Transmission Threshold
The approximate coverage at which:
\[
P(R_e>1)=50\%
\]was:
\[
\boxed{98.23\%}
\]This is a probabilistic threshold and should not be interpreted as an official vaccination target.
🦠 Monte Carlo Epidemic Burden
Coverage	Median Infections	Lower 95% UI	Upper 95% UI	Median Attack Rate
95%	52.37 M	15,878	159.37 M	3.58%
96%	35.06 M	4,136	142.68 M	2.40%
97%	13.22 M	1,617	125.94 M	0.90%
98%	141,410	754	109.19 M	0.01%
99%	11,385	397	92.50 M	~0%
100%	4,166	205	75.59 M	~0%


🚨 Probability of Large Outbreaks
At 95% coverage:
Probability of >1 million infections = 89.50%
Probability of >10 million infections = 83.54%
Probability of >100 million infections = 16.42%
At 100% coverage:
Probability of >1 million infections = 19.90%
Probability of >10 million infections = 15.93%
Probability of >100 million infections = 1.07%
🔬 Sensitivity Analysis
Sensitivity analysis examined the influence of:
vaccine effectiveness
\(R_0\)
infectious period
initial infections
Pearson Correlations
Parameter	Correlation
VE	-0.743
\(R_0\)	+0.154
\(I_0\)	+0.014
Infectious period	-0.005


Standardized Regression Coefficients
Parameter	Standardized β
VE	-0.745
\(R_0\)	+0.161
Infectious period	-0.006
\(I_0\)	+0.003


Key Finding
Vaccine effectiveness was the strongest determinant of epidemic burden.
🧪 Vaccine Effectiveness × Coverage Analysis
The interaction between VE and coverage was explored using deterministic scenarios.
VE	95% Coverage	97% Coverage	99% Coverage	100% Coverage
90%	2.175	1.905	1.635	1.500
92%	1.890	1.614	1.338	1.200
94%	1.605	1.323	1.041	0.900
96%	1.320	1.032	0.744	0.600
98%	1.035	0.741	0.447	0.300
99%	0.892	0.596	0.299	0.150


Values below 1 indicate transmission control under the deterministic assumptions.
🏆 Key Findings
1. MCV2 coverage increased substantially
2014 → 60%
2025 → 95%
2. MCV2 coverage was inversely associated with measles incidence
\[
r=-0.615
\]3. Increasing vaccination coverage reduced transmission
The deterministic model showed a progressive decline in \(R_e\) with increasing coverage.
4. Age structure substantially changes population protection
At 95% routine MCV2 coverage:
Nominal coverage = 95%
Effective population protection = 25.25%
under the routine childhood vaccination scenario.
5. Deterministic age-structured threshold
Approximately:
\[
96.3\%
\]coverage was required for:
\[
R_e<1
\]under the fixed Model 2C assumptions.
6. Probabilistic threshold
Approximately:
\[
98.23\%
\]coverage corresponded to:
\[
P(R_e>1)\approx50\%.
\]7. Residual transmission risk remains under uncertainty
At 100% hypothetical all-age coverage:
\[
P(R_e>1)=25.64\%.
\]8. Epidemic burden falls dramatically
Median infections decreased from:
52.37 million at 95%
to:
4,166 at 100%
9. Vaccine effectiveness was the dominant uncertainty driver
\[
Standardized\ \beta=-0.745
\]📌 Main Interpretation
The study demonstrates:
\[
\boxed{
Higher\ vaccination\ coverage
\rightarrow
Lower\ R_e
\rightarrow
Lower\ epidemic\ burden
}
\]However:
\[
\boxed{
Nominal\ vaccination\ coverage
\neq
effective\ population\ immunity
}
\]and:
\[
\boxed{
Median\ R_e<1
\neq
zero\ probability\ of\ transmission
}
\]Therefore, measles elimination requires consideration of:
vaccination coverage
vaccine effectiveness
age-specific immunity
geographic susceptibility
contact patterns
surveillance
parameter uncertainty
💡 Public Health Implications
The findings support several broad implications for measles elimination strategies.
Maintain very high vaccination coverage
High coverage remains fundamental to reducing transmission.
Identify immunity gaps
National averages may conceal susceptible populations.
Monitor age-specific coverage
Age structure can substantially influence population-level immunity.
Consider targeted supplementary vaccination
Catch-up or supplementary vaccination may be useful where immunity gaps are identified.
Maintain high vaccine effectiveness
VE was the strongest determinant of epidemic burden in the sensitivity analysis.
Strengthen surveillance
Reported cases do not necessarily represent all infections.
Incorporate uncertainty
Probabilistic estimates can provide a more realistic assessment of residual transmission risk.
⚠️ Limitations
Important limitations include:
Observational correlations cannot establish causality.
Reported measles cases may underestimate true infections.
COVID-19 disrupted vaccination and surveillance.
The deterministic model assumes simplified population mixing.
Contact matrix assumptions affect age-structured results.
The age-structured model uses a static 2025 population.
Geographic heterogeneity is not explicitly modelled.
Vaccine effectiveness is represented using a population-level distribution.
\(R_0\) was represented using an assumed uncertainty distribution.
Initial infections and infectious period were simplified.
Waning immunity was not explicitly modelled.
Maternal immunity was not explicitly modelled.
Supplementary immunization activities were not explicitly represented.
Modelled infections should not be interpreted as reported cases.
🛠️ Technologies and Tools
The project was developed using Python and Jupyter/Anaconda.
Programming
Python
Jupyter Notebook
Data Analysis
Pandas
NumPy
Statistical Analysis
SciPy
scikit-learn
Mathematical Modelling
Ordinary differential equations
SIR compartmental modelling
Age-structured transmission modelling
Next-generation matrix methods
Eigenvalue-based \(R_e\) estimation
Monte Carlo simulation
Visualization
Matplotlib
Seaborn
Data Sources / File Formats
Excel
CSV
📁 Repository Structure
India_Measles_Vaccination_Monte_Carlo/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_Data_Preparation.ipynb
│   ├── 02_Model_2A_Observational_Analysis.ipynb
│   ├── 03_Model_2B_Deterministic_SIR.ipynb
│   ├── 04_Model_2C_Age_Structured_Model.ipynb
│   ├── 05_Monte_Carlo_Analysis.ipynb
│   └── 06_Sensitivity_and_Scenario_Analysis.ipynb
│
├── src/
│   ├── data_preparation.py
│   ├── sir_model.py
│   ├── age_structured_model.py
│   ├── monte_carlo.py
│   └── sensitivity_analysis.py
│
├── results/
│   ├── figures/
│   └── tables/
│
└── report/
    ├── India_Measles_Vaccination_Monte_Carlo_Report.docx
    └── India_Measles_Vaccination_Monte_Carlo_Report.pdf
📊 Planned Visualizations
The repository will include visualizations such as:
Figure 1
MCV2 vaccination coverage in India, 2014–2025
Figure 2
Reported measles incidence in India, 2014–2025
Figure 3
MCV2 coverage versus measles incidence
Figure 4
Deterministic \(R_e\) versus vaccination coverage
Figure 5
Deterministic epidemic curves under different coverage scenarios
Figure 6
2025 Indian population age structure
Figure 7
Age-specific susceptibility under routine vaccination
Figure 8
Monte Carlo distribution of \(R_e\)
Figure 9
Probability of \(R_e>1\) versus vaccination coverage
Figure 10
Median epidemic burden versus vaccination coverage
Figure 11
Sensitivity analysis of model parameters
Figure 12
Vaccine effectiveness × vaccination coverage scenario analysis
📑 Planned Outputs
The project produces:
Cleaned epidemiological dataset
Observational analysis
Deterministic SIR model
Age-structured transmission model
Monte Carlo simulations
Sensitivity analysis
Vaccination scenario analysis
Epidemic burden estimates
Transmission thresholds
Research report
🔁 Reproducibility
To reproduce the analysis:
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/India_Measles_Vaccination_Monte_Carlo.git
2. Navigate to the project
cd India_Measles_Vaccination_Monte_Carlo
3. Create a virtual environment
python -m venv venv
4. Activate the environment
macOS/Linux
source venv/bin/activate
Windows
venv\Scripts\activate
5. Install dependencies
pip install -r requirements.txt
6. Launch Jupyter
jupyter notebook
7. Run the notebooks sequentially
01 → 02 → 03 → 04 → 05 → 06
📚 Report
The complete academic report is available in:
report/
The report includes:
Introduction
Data and Methodology
Results
Discussion
Limitations and Policy Implications
Conclusion and Recommendations
🔮 Future Research
Future extensions could include:
State- and district-level modelling
Geographic heterogeneity
Dynamic demographic modelling
Time-varying vaccination coverage
Bayesian parameter estimation
Stochastic transmission modelling
Individual-based modelling
Explicit waning immunity
Maternal immunity
Supplementary immunization activities
Dynamic reporting fractions
Calibration against observed measles incidence
Cost-effectiveness analysis of alternative vaccination strategies
⚠️ Interpretation Note
This project is a research and modelling exercise and should not be interpreted as an official estimate of India's measles elimination threshold.
Model outputs are conditional on the assumptions, parameter distributions and population structure specified in the analysis.
The vaccination thresholds reported here are therefore model-derived scenario estimates, not official policy recommendations.
📖 References and Data Sources
The project uses publicly available vaccination, epidemiological and population data.
The repository should include the full source citations and data-access information used to construct the analysis.
Where redistribution of original source datasets is restricted, the repository will provide:
Dataset name
Original source
Data-access instructions
Processing methodology
rather than redistributing the original file.
👩‍🔬 Project Author
Leena Gaikwad
Public Health | Epidemiology | Health Economics & Outcomes Research | Evidence Synthesis | Data Science | Mathematical Modelling
⭐ Key Takeaway
High MCV2 coverage substantially reduces measles transmission and epidemic burden, but vaccination coverage alone does not guarantee elimination. Population-level immunity, age-specific susceptibility, vaccine effectiveness and uncertainty in transmission dynamics must all be considered when evaluating measles elimination strategies.

Project Status
Status: Completed modelling analysis / documentation and visualization finalization