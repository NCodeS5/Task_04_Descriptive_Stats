# Task_04_Descriptive_Stats

<h1 style="color:red;">Facebook Posts Data Analysis Report</h1>

<h2 style="color:red;">Introduction</h2>
<p>
This report summarizes the findings from our exploratory data analysis conducted on a dataset of Facebook posts. 
The analysis was performed using three different approaches — <strong>pure Python</strong>, <strong>pandas</strong>, and <strong>polars</strong> — to ensure consistency and validate results across tools.
</p>

<h2 style="color:red;">Data Overview</h2>
<p>
The dataset consists of <strong>19,009 records</strong>, each representing a Facebook post along with various engagement and content-related metrics.
</p>

<strong>Key fields include:</strong>
<ul>
  <li>Facebook_Id</li>
  <li>post_id</li>
  <li>Page Category</li>
  <li>Post Created Date</li>
  <li>Total Interactions</li>
  <li>Detailed engagement metrics such as Likes, Comments, Shares, and reactions (Love, Wow, Haha, Sad, Angry, Care)</li>
</ul>

<h2 style="color:red;">Findings</h2>

<h3>Completeness of Data</h3>
<ul>
  <li>Core columns like <code>Facebook_Id</code>, <code>post_id</code>, <code>Total Interactions</code>, <code>Likes</code>, <code>Comments</code>, and <code>Shares</code> were <strong>fully populated</strong>, each having <strong>19,009 non-empty entries</strong>.</li>
  <li>Other columns such as <code>Page Category</code> and <code>Is Video Owner?</code> had slightly fewer entries, indicating <strong>some missing data</strong>.</li>
</ul>

<h3>Sparse or Missing Data</h3>
<ul>
  <li>Fields related to sponsorship (<code>Sponsor Id</code>, <code>Sponsor Name</code>, <code>Sponsor Category</code>) contained <strong>no data</strong>, with counts of zero across all records.</li>
  <li>Columns representing nuanced content classifications and message topics (e.g., <code>covid_topic_illuminating</code>, <code>environment_topic_illuminating</code>, <code>womens_issue_topic_illuminating</code>) also showed <strong>extremely low or zero counts</strong>, suggesting limited tagging or availability of such metadata.</li>
</ul>

<h3>Descriptive Statistics</h3>
<ul>
  <li>We calculated various statistics including <strong>counts</strong>, <strong>means</strong>, <strong>minimums</strong>, <strong>maximums</strong>, and <strong>standard deviations</strong> to summarize numeric engagement features.</li>
  <li>The data distributions revealed <strong>reasonable engagement variations</strong>, supporting the dataset's potential for insights on user interactions.</li>
</ul>

<h2 style="color:red;">Conclusion</h2>
<p>
Our analysis demonstrates that while the dataset provides a <strong>robust foundation of core engagement metrics</strong>, it suffers from <strong>sparsity in specialized features</strong> such as sponsorship details and topical tags. 
This indicates a need for <strong>targeted data enrichment or imputation strategies</strong> if these features are to be leveraged in subsequent modeling or reporting.
</p>
<p>
Nonetheless, the <strong>well-populated engagement metrics position this dataset as a strong candidate for analyses focused on post performance and audience interaction trends</strong>.
</p>
