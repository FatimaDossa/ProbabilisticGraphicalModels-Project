# ProbabilisticGraphicalModels-Project
## Overview

This project addresses the significant public health challenge of waterborne diseases in Sindh, Pakistan, where communities heavily rely on often contaminated hand-pump water sources [1]. We developed a **predictive model using Bayesian Networks** to assess the likelihood of disease occurrences based on water quality data collected from three districts in Sindh: **Badin, Sanghar, and Sukkur** [1, 2]. The dataset, comprising contamination metrics from **90 water samples**, was collected under the "Assessment of Water Quality of Hand Pumps from Lower, Middle and Upper Districts of Sindh, Pakistan" study [1, 2].

The Bayesian Network model represents villages, water quality parameters, and diseases as interconnected nodes, modeling causal relationships [1]. Probabilities within the network are derived from primary data collected during the aforementioned study [1]. By integrating probabilistic graphical models with localized data, our aim is to provide information on disease prevention and inform policy interventions to improve public health in vulnerable communities [1].

**Key contributions of this project include:**

*   Development of a **localized disease risk prediction model** specifically for Sindh, Pakistan [2].
*   Utilization of **Bayesian Networks** to map causal relationships between water quality parameters and disease occurrences [2].
*   Integration of **firsthand data** collected within Sindh [2, 3].
*   Providing a tool for the **visualization and analysis of causal relationships**, valuable for policymakers and health practitioners [2].

## Key Features

*   **Predictive Modeling:** Uses Bayesian Networks to predict the likelihood of waterborne diseases based on water quality data [1].
*   **Localized Data:** Based on data collected from 90 water samples across three districts of Sindh (Badin, Sanghar, Sukkur) [1, 2].
*   **Causal Relationship Mapping:** Models the intricate causal links between water quality metrics and their potential health impacts [2].
*   **Risk Assessment:** Provides risk assessments across different districts based on water quality parameters [4].
*   **Identification of Prevalent Issues:** Highlights commonly found water impurities like E.Coli, Coliform, and Hardness in the studied districts [5].
*   **Disease Likelihood Prediction:** Predicts the prevalence of diseases such as Dysentery, Cholera, Cancer, and Kidney and Urinary Diseases based on water quality [6].
*   **District-Specific Analysis:** Allows for the analysis of water quality parameters and disease risks specific to Badin, Sanghar, and Sukkur [7-11].

## Methodology

1.  **Data Collection:** Utilized water quality data from 90 samples collected from Badin, Sanghar, and Sukkur [1, 2, 12]. Each district had 30 samples from six different villages, with five samples per village [12].
2.  **Water Quality Parameter Analysis:** The samples were tested for 19 water quality parameters, including Total Alkalinity, pH, Hardness, Chlorine levels, Nitrate, Nitrite, Iron, Chromium, Lead, Copper, Mercury, Fluoride, E.Coli, and Coliforms [13, 14].
3.  **Bayesian Network Model Construction:** A Bayesian Network model was developed with three levels of nodes:
    *   **Level 0:** Districts of Sindh (Sukkur, Sanghar, Badin) [14].
    *   **Level 1:** Shortlisted water quality parameters that can lead to diseases [14].
    *   **Level 2:** Diseases caused by the parameters in Level 1 [14].
4.  **Probability Assignment:**
    *   Prior probability for each district was set to 1/3 [15].
    *   Conditional probabilities for water quality parameters being high in each district were calculated based on the collected data, using a threshold-based binary classification (high/optimum) according to WHO and testing kit standards [15, 16]. **Laplacian smoothing** was applied to address zero probability instances [15, 17].
    *   Conditional probabilities for diseases given high or optimum levels of water quality parameters were determined through a **qualitative approach and consultation with domain experts** due to the unavailability of a combined dataset [17].
5.  **Model Analysis and Validation:** The model was analyzed by instantiating evidence on different nodes to observe changes in probabilities and predict disease likelihoods in specific district contexts [5, 7, 9]. The model's general observations were found to be in sync with the data from the STRP research [6].

## Results

The Bayesian Network model revealed significant relationships between water quality and disease prevalence:

*   **High prevalence of E.Coli (97%) and Coliform (97%)** across all districts leads to a high likelihood of Diarrhea (76%) and Cholera (39%) [5, 6, 18].
*   **High Hardness (86%)** increases the probability of Arthropathies (36%) and Kidney and Urinary Diseases (50%) [5, 6, 11].
*   District-specific analysis showed:
    *   In **Sanghar**, high Hardness, Nitrate, Nitrite, E.Coli, and Coliform levels were observed [7]. Evidence instantiation predicted increased chances of Cancer, Blue Baby Syndrome, Thyroid Dysfunction, Methemoglobinemia, Dysentery, Cholera, Typhoid, HUS, Diarrhea, and Gastroenteritis [10].
    *   In **Sukkur**, relatively high levels of Hardness, Nitrite, Nitrate, and Arsenic were found [8]. Evidence predicted increased risks of Cancer, Cardiovascular Diseases, Dysentery, Cholera, Typhoid, HUS, Diarrhea, Gastroenteritis, Blue Baby Syndrome, and Methemoglobinemia [10].
    *   In **Badin**, E.Coli and Coliform remained very high, while Nitrate and Nitrite levels decreased. High Arsenic and Hardness were also noted [8, 9]. Predictions indicated increased risks of Cancer, Cardiovascular Diseases, Dysentery, Cholera, Typhoid, HUS, Diarrhea, and Gastroenteritis [11].
*   Arsenic levels in Sukkur and Badin showed a significant increase in the likelihood of Cancer (34%) and Cardiovascular Diseases (24%) [19].

## Limitations

*   The model assumes **Noisy OR structures** for nodes with multiple parents, which might oversimplify complex real-world dependencies [20, 21].
*   Expert validation was limited to one district-specific and one general advisor, potentially creating gaps in context-specific validation for other districts [21].
*   Disease probability data was derived **manually from literature** due to the unavailability of prior datasets, introducing a potential for human error [21].
*   Limited sample size for Arsenic testing in the original research might affect the accuracy of probabilities related to Arsenic [4].

## Conclusion and Recommendations

This project demonstrates the effectiveness of **Bayesian Network models** for locally predicting water quality and disease outbreaks in Sindh, Pakistan [4]. The model highlights the urgent need for interventions to improve water quality, particularly addressing microbial contamination and reducing Arsenic levels [18, 19]. Based on the model's results, we recommend immediate safety measures such as **cost-efficient water treatment methods, like boiling water before consumption**, to evaluate and improve water quality in rural areas [4, 22]. This study contributes to a better understanding of disease causality in environmental contexts and provides actionable insights for public health interventions [20].

## Acknowledgments

This research was completed as a final project for the Probabilistic Graphical Models course at Habib University [22]. We acknowledge the significant assistance of our domain experts, including local and district-level advisors, as well as contacts in the Public Health sector. We are also grateful for the motivating research conducted by Dr. Humaira Qureshi on local areas of Sindh [22].

## References

[1] J. Ahmed, et al., “Quantitative Microbial Risk Assessment of Drinking Water Quality to Predict the Risk of Waterborne Diseases in Primary-School Children,” *International Journal of Environmental Research and Public Health*, vol. 17, no. 8, pp. xx-yy, Apr. 2020, doi: https://doi.org/10.3390/ijerph17082774 [23, 24].
[25] A. Nayan, J. Saha, A. Mozumder, K. Mahmud, A. Azad, and M. Kibria, “A machine learning approach for early detection of fish diseases by analyzing water quality,” *Trends in Sciences*, vol. 18, no. 21, p. 351, 2021, doi: https://doi.org/10.48048/tis.2021.351 [24, 26].
[2] D. H. Hall and Q.-T. Le, “Use of Bayesian networks in predicting con-tamination of drinking water with E. coli in rural Vietnam,” *Transactions of The Royal Society of Tropical Medicine and Hygiene*, vol. 111, no. 6, pp. 270–277, Jun. 2017, doi: https://doi.org/10.1093/trstmh/trx043 [27, 28].
[23] A. Ali, S. Javed, S. Ullah, S. H. Fatima, F. Zaidi, and M. S. Khan, “Bayesian spatial analysis and prediction of groundwater contamination in Jhelum city (Pakistan),” *Environmental Earth Sciences*, vol. 77, no. 3, Jan. 2018, doi: https://doi.org/10.1007/s12665-018-7253-5 [28, 29].
[30] A. M. Nangraj, E. Fatima, U. Aftab, H. Qureshi, “Assessment of Water Quality of Hand Pumps from Lower, Middle and Upper Districts of Sindh, Pakistan” [12, 31].

## Code

The Python code used for calculating probabilities with Laplace smoothing can be found in the [Appendix](PGM_report_group5%20(1)%20(2).pdf) of the full report [31, 32]. An example snippet for the Sanghar district is provided below:

```python
import pandas as pd

# Load the Excel file to inspect the data structure
file_path = ’D:\\MARIA\\PGM\\project\\Analysis\\sanghar water parameter results.xlsx’
data = pd.read_excel(file_path)

thresholds = {
    ’Hardness mg/L’: 100,
    ’Nitrate mg/L’: 10,
    ’Nitrite mg/L’: 1,
    ’Iron mg/L’: 10,
    ’Chromium/Cr (VI) mg/L’: 2,
    ’Lead ppb’: 15,
    ’Copper mg/L’: 1,
    ’Mercury mg/L’: 0.002,
    ’Fluoride mg/L’: 4,
    ’Coliforms MPN’: 1,
    ’E.Coli MPN’: 1,
}

# Create a new DataFrame to store binary classifications
binary_data = data.copy()

# Apply thresholds to classify parameters
for param, limit in thresholds.items():
    if param in binary_data.columns:
        binary_data[param] = binary_data[param].apply(lambda x: 1 if x > limit else (0 if x <= limit else None))

# Drop rows with missing data for simplicity
binary_data_clean = binary_data.dropna()
total_entries = len(binary_data_clean) # Total rows after cleaning

# Apply Laplace smoothing to the probabilities
k = 1 # Smoothing factor
smoothed_probabilities = {}
for param in thresholds.keys():
    if param in binary_data_clean.columns:
        num_impermissible = binary_data_clean[binary_data_clean[param] == 1].shape
        smoothed_probabilities[param] = (num_impermissible + k)/(total_entries + 2 * k)

# Print the smoothed probabilities
print("\nConditional Probabilities (Laplace Smoothing):")
for param, prob in smoothed_probabilities.items():
    print(f"{param}: {prob:.4f}")
Similar code was used for the other two districts. The Bayesian Network model itself was likely constructed and analyzed using software such as Netica.
