## Economic Impact Analysis of the 2014 Russian Invasion of Ukraine

This project analyzes the economic consequences of the 2014 Russian invasion of Ukraine using causal inference methods, specifically the Synthetic Control Method (SCM). Our analysis builds on and extends the findings of the paper by Bluszcz and Valente (2020) on the economic costs of hybrid wars. Through replication and extension of their approach, this project aims to deepen understanding of the invasion's impact on Ukraine’s GDP per capita (GDPpc) over an extended period.

### Project Summary

This repository contains the data and code used to:
1. **Replicate** the findings in Bluszcz and Valente’s study, specifically focusing on the GDPpc loss for Ukraine and war-affected regions like Donetsk and Luhansk.
2. **Extend** the study by:
   - Analyzing post-treatment effects from 2013 to 2021, beyond the original 2013-2017 timeline.
   - Implementing a more rigorous donor pool selection by removing countries affected by conflicts from 1990 to 2012.
   - Adjusting the weights of predictors to achieve better balance, thus improving the robustness of synthetic control results.

### Methodology

- **Synthetic Control Method (SCM):** SCM is a statistical method that estimates causal effects by comparing treated units with a weighted combination of control units (donor pool). Here, we create a synthetic version of Ukraine using countries with similar pre-intervention characteristics.
- **Donor Pool Selection:** Countries from the Post-Soviet and Eastern Bloc regions were carefully selected to construct a control group unaffected by similar shocks.
- **Extensions in Analysis:** 
  - **Extended Post-Treatment Period:** Evaluating the long-term impact of the invasion through 2021.
  - **Donor Pool Adjustments:** Excluding additional countries with prolonged conflicts to reduce bias.
  - **Predictor Balance Improvement:** Adjusted weights to improve alignment on key predictors like inflation and human development indices.

### Repository Structure

- **`/data`**: Contains the data files used in the analysis, including GDP per capita data for Ukraine and selected donor pool countries.
- **`/code`**: Includes Python scripts and Jupyter Notebooks for replicating and extending the analysis.
  - `replication.py`: Code for replicating Bluszcz and Valente’s original analysis.
  - `extension.py`: Code implementing the extensions, such as new donor pool criteria and extended post-treatment period.
- **`/results`**: Generated figures and tables comparing Ukraine’s actual and synthetic GDPpc.

### Results

The findings indicate a sustained economic impact of the invasion, with a greater divergence in Ukraine’s GDPpc compared to the synthetic control when extending the analysis to 2021. Adjusting the donor pool and rebalancing predictors further reinforces the robustness of these results.

### How to Run

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/yourusername/economic-impact-ukraine.git
   cd economic-impact-ukraine
   ```
2. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the analysis by executing the scripts in the `/code` directory.

## References

- Bluszcz, J., & Valente, M. (2020). The Economic Costs of Hybrid Wars: The Case of Ukraine. *Defence and Peace Economics*. [DOI link](https://doi.org/10.1080/10242694.2020.1791616)

For a deeper understanding, refer to the full report [here](https://drive.google.com/drive/folders/1MJfuSINd1vk-pb18GFRzgZlrxbg84XHK?usp=sharing).
