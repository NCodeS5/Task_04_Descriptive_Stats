# Task_04_Descriptive_Stats

Introduction
This report summarizes the findings from our exploratory data analysis conducted on a dataset of Facebook posts. The analysis was performed using three different approaches: pure Python, pandas, and polars, to ensure consistency and validate results across tools.

Data Overview
The dataset consists of 19,009 records, each representing a Facebook post along with various engagement and content-related metrics.

Key fields include Facebook_Id, post_id, Page Category, Post Created Date, Total Interactions, and detailed engagement metrics such as Likes, Comments, Shares, and reactions (Love, Wow, Haha, Sad, Angry, Care).

Findings
Completeness of Data:

Core columns like Facebook_Id, post_id, Total Interactions, Likes, Comments, and Shares were fully populated, each having 19,009 non-empty entries.

Other columns such as Page Category and Is Video Owner? had slightly fewer entries, indicating some missing data.

Sparse or Missing Data:

Fields related to sponsorship (Sponsor Id, Sponsor Name, Sponsor Category) contained no data, with counts of zero across all records.

Columns representing nuanced content classifications and message topics (e.g., covid_topic_illuminating, environment_topic_illuminating, womens_issue_topic_illuminating) also showed extremely low or zero counts, suggesting limited tagging or availability of such metadata.

Descriptive Statistics:

We calculated various statistics, including counts, means, minimums, maximums, and standard deviations, to summarize numeric engagement features.

The data distributions showed reasonable engagement variations, supporting the dataset's potential for insights on user interactions.

Conclusion
Our analysis demonstrates that while the dataset provides a robust foundation of core engagement metrics, it suffers from sparsity in specialized features such as sponsorship details and topical tags. This points to the need for targeted data enrichment or imputation strategies if these features are to be leveraged in subsequent modeling or reporting. Nonetheless, the well-populated engagement metrics position this dataset as a strong candidate for analyses focused on post performance and audience interaction trends.
