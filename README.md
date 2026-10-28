# Social Media Engagement Analysis

**Author:** Risty Anugrah Dwi Septiana

## Project Overview

This project analyzes social media content performance to understand engagement patterns, audience reach, content effectiveness, and click-through behavior.

Using Python and Pandas, the analysis evaluates engagement rates across platforms and content types, compares promoted and organic content, identifies top- and low-performing posts, and explores relationships between social media performance metrics.

The goal is to generate data-driven insights that can help improve content strategy and social media performance.

## Business Objectives

- Evaluate engagement performance across social media platforms.
- Identify the highest- and lowest-performing content based on engagement rate.
- Compare engagement across different content types.
- Analyze reach, impressions, interactions, and click-through rate (CTR).
- Compare promoted and organic content performance.
- Explore correlations among key social media metrics.
- Develop recommendations for improving content engagement and audience interaction.

## Dataset Overview

The dataset contains **100 content records and 23 columns**.

Key attributes include:

| Category | Columns |
|---|---|
| Content information | `Content_ID`, `Platform`, `Content_Type` |
| Audience exposure | `Reach`, `Impressions`, `Follower_Count` |
| Engagement metrics | `Likes`, `Comments`, `Shares`, `Saves` |
| Click performance | `Clicks`, `CTR` |
| Content characteristics | `Upload_Time`, `Day_of_Week`, `Hashtags_Count`, `Caption_Length`, `Video_Duration_Sec` |
| Promotion | `Ad_Spend_USD`, `Is_Promoted` |
| Performance rates | `Completion_Rate`, `View_Through_Rate`, `Engagement_Rate_Reach`, `Engagement_Rate_Impressions` |

## Tools & Technologies

- **Python** — Data analysis and processing
- **Pandas** — Data manipulation and aggregation
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Google Colab / Jupyter Notebook** — Interactive analysis

## Data Cleaning & Preparation

The notebook performs the following preparation steps:

1. Inspects dataset dimensions, column names, data types, and missing values.
2. Replaces missing values in `Saves` with zero.
3. Filters out records with `Reach` less than or equal to zero.
4. Creates additional interaction and performance metrics.
5. Prepares a final metrics table for ranking, comparison, and export.

After filtering, **93 content records remain** from the original 100 records.

Missing `Video_Duration_Sec` values are retained because video duration may not apply to every content type. However, this assumption should be verified against the dataset's content definitions.

## Key Metrics

### 1. Total Interactions

Measures the total number of recorded interactions with a content item.

`Total Interactions = Likes + Comments + Shares + Saves`

### 2. Engagement Rate by Reach

Measures interactions relative to the number of people reached.

`Engagement Rate (%) = Total Interactions / Reach × 100`

### 3. Interaction per Impression (IPI)

Measures interactions relative to total impressions.

`IPI = Total Interactions / Impressions`

The notebook also calculates `IPI_Percent` by multiplying IPI by 100.

### 4. Click-Through Rate (CTR)

Calculates the percentage of impressions that resulted in clicks.

`CTR (%) = Clicks / Impressions × 100`

The notebook recalculates CTR using the raw click and impression counts as `CTR_Calc`.

## Analysis Performed

### 1. Content Performance Ranking

- Ranks content by engagement rate.
- Identifies the top 10 content items.
- Identifies the 10 lowest-performing content items.
- Compares reach and total interactions across content.

### 2. Platform Performance Analysis

Compares social media platforms using:
- Average reach
- Average impressions
- Average interactions
- Average engagement rate
- Average IPI
- Average CTR

This analysis helps identify differences in performance across platforms.

### 3. Content Type Analysis

Evaluates engagement performance across content types to understand which formats generate stronger audience interactions.

### 4. Promoted vs. Organic Content

Compares promoted and organic content based on:
- Number of content items
- Average reach
- Average interactions
- Average engagement rate
- Average CTR

The results can help assess whether paid promotion is associated with differences in content performance.

### 5. Correlation Analysis

Examines relationships among numeric metrics, including reach, impressions, likes, comments, shares, saves, clicks, engagement rate, IPI, and CTR.

Correlation can reveal patterns between variables, but it does not establish causation.

### 6. Data Visualization

The notebook creates horizontal bar charts to visualize:
- Top 10 content items by engagement rate
- Average engagement rate by platform
- Average engagement rate by content type

## Key Findings

The notebook establishes the following descriptive results:

- The original dataset contains 100 content records.
- Seven records are excluded because their reach is not greater than zero.
- The cleaned dataset contains 93 records.
- Engagement rates are calculated to rank individual content items.
- Platform and content type comparisons are prepared to identify differences in average engagement.
- Promoted and organic content are compared using reach, interactions, engagement rate, and CTR.

**Note:** The final numerical rankings, best-performing platform, best-performing content type, and promoted-versus-organic comparison are not included in the supplied notebook output. These findings should be populated using the actual results generated by the analysis.

## Business Recommendations

The following are potential actions to evaluate after reviewing the final analytical results:

1. **Prioritize high-performing content:** Investigate the characteristics of content with consistently strong engagement rates.
2. **Optimize platform strategy:** Allocate content production resources based on platform-specific engagement and click performance.
3. **Refine content formats:** Test different content types and compare their engagement, reach, and CTR.
4. **Evaluate paid promotion:** Compare promoted and organic content while accounting for differences in reach, content type, and advertising spend.
5. **Improve measurement:** Monitor engagement rate, CTR, reach, and impressions together instead of relying on a single metric.
6. **Run controlled experiments:** Test posting schedules, content formats, captions, and promotional strategies to assess their effects more reliably.

These recommendations are hypotheses for further investigation, not confirmed causal conclusions from the current analysis.

## Limitations

- The dataset contains only 100 original content records, with 93 retained after filtering.
- The dataset's time period and representativeness are not specified in the supplied notebook.
- Missing `Saves` values are treated as zero, which may underestimate engagement if the values represent unrecorded data rather than true zero saves.
- Engagement rate by reach can be sensitive to very small reach values.
- Promoted and organic content may differ in other characteristics, so their performance comparison does not establish the impact of advertising.
- The notebook calculates new CTR and engagement metrics; these should be compared with the existing dataset metrics to check consistency.
- Correlation results should not be interpreted as proof of causation.

## Repository Structure

```text
social-media-engagement-analysis/
├── social_media_engagement_analysis.ipynb
├── README.md
└── data/
    └── README.md
```

The `data/` directory is optional. If the original dataset cannot be shared, document the required filename and column structure in `data/README.md` instead of uploading restricted data.

## How to Run

1. Clone or download this repository.
2. Open `social_media_engagement_analysis.ipynb` in Google Colab or Jupyter Notebook.
3. Upload the original dataset.
4. Update the dataset path in the notebook.
5. Execute the notebook cells in order.
6. Review the generated rankings, summary tables, and visualizations.
7. Export the cleaned metrics table for further analysis.

## Author

**Risty Anugrah Dwi Septiana**

- GitHub: [Ristyanugrah](https://github.com/Ristyanugrah)
- Data Analytics Portfolio: [data-analytics-portfolio](https://github.com/Ristyanugrah/data-analytics-portfolio)
- Portfolio Website: [risty-portfolio.vercel.app](https://risty-portfolio.vercel.app/)

---

*This project was developed for data analytics practice and portfolio development, focusing on social media performance, content engagement, and data-driven content strategy.*
