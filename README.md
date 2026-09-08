# Retail Promotions Visualization

An exploratory retail analytics project that measures how promotional campaigns affected store-level sales volume and revenue across cities, product categories, and promotion types.

The project combines a reproducible Jupyter analysis with a client-facing presentation. The source datasets are intentionally excluded because they are confidential.

## Project highlights

- Converts promotional sales data into business-focused insights across stores, cities, categories, and campaign types.
- Uses reproducible analysis to compare incremental sold units and incremental revenue rather than relying on raw sales totals alone.
- Includes a client-facing presentation alongside the notebook so findings can be communicated to non-technical stakeholders.
- Keeps confidential source data out of version control while retaining executed notebook outputs for review.

## Analysis approach

The workflow follows a simple business-analysis pipeline:

1. Load and validate campaign, product, store, and transaction-level data.
2. Join the source tables into an analysis-ready dataset.
3. Calculate pre- and post-promotion revenue and unit metrics.
4. Aggregate results by city, category, store, and promotion type.
5. Compare incremental sold units and incremental revenue to identify where promotions created value.
6. Visualize the findings and translate them into client-facing recommendations.

This structure keeps the analysis reproducible while separating raw calculations from the final business interpretation.

## Business questions

The analysis answers seven questions:

1. How are stores distributed across cities?
2. Which product categories contributed most to Sankranti sales?
3. How strongly are post-promotion price and quantity related?
4. How does baseline demand vary by product category?
5. Which cities achieved the highest and lowest incremental sold units percentage?
6. Which promotions produced the most incremental units and revenue in Hyderabad?
7. How did promotions affect category revenue in Bengaluru?

## Key findings

- Bengaluru has the largest store network with 10 stores, followed by Chennai with 8 and Hyderabad with 7.
- Grocery & Staples contributed 70.51% of all post-promotion units during Sankranti.
- Post-promotion price and quantity have a weak positive Pearson correlation of 0.269. This association does not establish causation.
- Madurai recorded the highest city-level ISU% at 121.28%, while Visakhapatnam had the smallest increase at 99.07%.
- In Hyderabad, BOGOF produced the most incremental units at 24,168.
- In Hyderabad, 500 Cashback generated the most incremental revenue at 12,866,500.
- Bengaluru's overall revenue increased by 81.34%, with Combo1 contributing the largest absolute gain.
- Bengaluru Personal Care revenue declined by 32.39%, showing that sales volume and revenue should be evaluated separately.

## Metrics

```text
Revenue before = base price before promotion * quantity sold before promotion

Revenue after = base price after promotion * quantity sold after promotion

ISU% = (units after - units before) / units before * 100

IR% = (revenue after - revenue before) / revenue before * 100
```

Percentages are calculated from aggregated totals instead of averaging row-level percentages.

## Repository structure

```text
retail-promotions-visualization/
├── notebooks/
│   └── retail_promotions_analysis.ipynb
├── presentation/
│   └── retail_promotions_client_presentation.pptx
├── .gitignore
├── README.md
└── requirements.txt
```

## Tools

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook
- PowerPoint

## Running the notebook

1. Create a virtual environment and install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Create a local `datasets` directory beside the notebook.

3. Add the following source files to that directory:

   ```text
   dim_campaigns.csv
   dim_products.csv
   dim_stores.csv
   fact_events.csv
   ```

4. Open `notebooks/retail_promotions_analysis.ipynb` and run all cells.

The repository includes previously executed notebook outputs so the analysis can be reviewed without access to the confidential data.

## Data privacy

No raw dataset, source assignment document, credentials, or personally identifiable information is included in this repository. The `.gitignore` rules prevent common dataset formats and local notebook artifacts from being committed accidentally.
