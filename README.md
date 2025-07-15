# Descriptive Statistics Analysis Report
## Task 04: Comparing Pure Python, Pandas, and Polars

---

## Introduction
This project explores building a data summarization system that computes descriptive statistics on real-world datasets — specifically social media activity data related to the 2024 U.S. Presidential elections.  
The analysis was performed using three different approaches:
- Pure Python (no third-party libraries)
- Pandas
- Polars

This allowed for a direct comparison of functionality, ease of use, performance, and suitability for general data analysis tasks.

---

## Data Overview
The primary dataset analyzed consisted of 19,009 Facebook posts, each record containing engagement metrics (Likes, Comments, Shares, reactions) along with metadata such as post creation dates, page categories, and topical tags.

Key columns included:
- Identifiers: `Facebook_Id`, `post_id`
- Engagement metrics: `Total Interactions`, `Likes`, `Comments`, `Shares`, `Love`, `Wow`, `Haha`, `Sad`, `Angry`, `Care`
- Contextual fields: `Page Category`, `Is Video Owner?`, sponsorship columns, topic classification columns

---

## Summary of Findings
- Core engagement columns (Likes, Comments, Shares) were fully populated, each with 19,009 non-empty entries.
- Sponsorship-related fields (`Sponsor Id`, `Sponsor Name`, `Sponsor Category`) and many topic tagging columns (like `covid_topic_illuminating`, `environment_topic_illuminating`) had zero or near-zero data, limiting their immediate analytical use.
- Despite this, the dataset showed meaningful variation in interaction metrics, making it suitable for studying post performance and audience engagement.

---

## Comparison: Pure Python vs Pandas vs Polars

| Feature / Aspect       | Pure Python                       | Pandas                             | Polars                             |
|-------------------------|----------------------------------|------------------------------------|------------------------------------|
| Ease of Use             | Requires manual loops, explicit type checks, and custom calculations. More verbose and error-prone. | Very concise; single-line `describe()`, `value_counts()`, and robust `groupby` make exploration fast. | Similar to pandas but cleaner for lazy or parallel operations. Supports easy method chaining. |
| Performance             | Slow on large datasets due to single-threaded native structures. | Optimized C-based backend; handles typical data well but can slow on very large files. | Extremely fast, built for multi-threading and Arrow-based processing. Excellent for big data. |
| Memory Efficiency       | Minimal overhead but inefficient on large datasets since all data is stored in Python lists and dictionaries. | Loads entire DataFrame into memory, can become memory-heavy. | More memory-friendly, processes in chunks, optimized for large-scale analytics. |
| Feature Set             | Very basic. Everything from groupings to unique counts must be coded manually. | Rich ecosystem with `describe()`, `groupby()`, `value_counts()`, `isna()` and more. | Similar robust tools, plus advanced lazy execution and streaming. |
| Readability & Maintenance | Verbose and harder to maintain due to manual logic. | Highly readable and intuitive for standard data analysis workflows. | Similarly readable, well-suited for building efficient pipelines. |
| Recommendation          | Best for educational exercises or when external packages are not allowed. | Ideal general-purpose tool with massive ecosystem and strong community support. | Excellent for large-scale, high-performance data analysis.

---

## Personal Reflections
### Challenges
It was time-consuming to replicate standard summary statistics in pure Python, especially when handling missing values and computing grouped statistics (such as by `Facebook_Id` or `post_id`).  
Ensuring identical results across all three approaches also required extra care to clean and cast data consistently.

### Performance and Ease of Use
Pandas was the easiest to use, offering one-liners to get most summary statistics.  
Polars performed exceptionally well on larger datasets, offering significant speed advantages and more memory-efficient processing.  
Pure Python, while educational, was not practical for datasets of this size.

### Recommendation for Junior Analysts
For general data exploration and reporting, pandas is the best starting point due to its extensive capabilities and intuitive design.  
For larger datasets or when performance is critical, Polars provides a modern alternative.  
Pure Python is useful for understanding how calculations work under the hood or when no external libraries are permitted.

---

## Observations on AI Tools
When using coding AI tools like ChatGPT to generate template code, they typically default to pandas.  
This recommendation makes sense because pandas is the most mature and widely adopted library for data analysis in Python, offering a balance of simplicity and power that suits most needs.

---

## Next Steps and Visualizations
As an extension, visualizations such as histograms, bar plots, and boxplots can be created to explore the distributions of likes, shares, and other engagement metrics.  
Popular tools include matplotlib, seaborn, and plotly in Python.

---

## Conclusion
This comparative exercise demonstrated:
- The foundational understanding gained from using pure Python,
- The powerful, well-balanced capabilities of pandas,
- And the impressive performance and scalability of Polars.

