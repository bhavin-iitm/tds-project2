# Dataset Narrative

## Dataset Overview
The dataset under analysis consists of various attributes related to reviews, presumably of films or media content. It contains the following columns:
- **date**: The date on which the review was posted.
- **language**: The language in which the review is written.
- **type**: The type of the reviewed content (e.g., movie, series).
- **title**: The title of the content being reviewed.
- **by**: The reviewer or entity that submitted the review.
- **overall**: The overall rating given by the reviewer, on a scale (likely from 1 to 5).
- **quality**: The quality rating assigned to the content, also on a scale from 1 to 5.
- **repeatability**: The repeatability score, which might indicate how often the reviewer would recommend the content.

The dataset has a total of **2,652 entries** and originates from an unspecified source that aggregates reviews, possibly from a film review website or application. Its primary purpose is to analyze user feedback on various media types, providing insights into overall viewer satisfaction and content quality.

## Data Cleaning and Preprocessing
The initial data cleaning and preprocessing steps included:
1. **Handling Missing Values**: 
   - The `date` column had **99 missing values** which were handled by removing those entries, as they may not contribute to meaningful analysis.
   - The `by` column had **262 missing values**; similar treatment was applied, with these entries also excluded.

2. **Outlier Detection**: 
   - Outliers were detected in the `overall` and `quality` columns using statistical methods such as IQR (Interquartile Range).
   - No outliers were found in the `repeatability` column.

3. **Data Type Conversion**: 
   - The `date` column was converted from object to datetime format for better time-series analysis.
   - Other columns were confirmed to be in their appropriate types (e.g., integers for ratings).

4. **Normalization**: 
   - Ratings were normalized on a scale of 0 to 1 to facilitate comparisons across different metrics.

## Outlier Analysis
Outliers were detected predominantly in the `overall` ratings, with **1,216 instances** flagged. These outliers could potentially skew the analysis and are likely indicative of either extreme opinions or errors in rating. The `quality` ratings had **24 outliers**. It is crucial to analyze these outliers further to determine if they represent genuine user sentiments or if they should be excluded from the dataset for a more accurate representation of average ratings.

## Exploratory Data Analysis (EDA)
During the exploratory data analysis, several key insights and trends emerged:
- The **majority language** used in reviews was **English**, accounting for **1,306 entries**, indicating a possible bias towards English-speaking audiences.
- The **most reviewed content type** was movies, with **2,211 entries** classified as such.
- The **average overall rating** was approximately **3.05**, suggesting a generally positive but not overwhelmingly favorable reception.
- The **average quality rating** of **3.21** indicated that users perceive quality positively but with room for improvement.
- **Review patterns** indicated that certain titles such as "Kanda Naal Mudhal" received significantly more reviews (9 entries), showing popularity.

## Visualizations
1. **Bar Chart of Reviews by Language**: 
   - This chart highlights the distribution of reviews across different languages. The dominance of English suggests targeting strategies for content in other languages may be needed.

2. **Box Plot of Overall Ratings**: 
   - The box plot reveals the median ratings and the spread of ratings, showing a concentration around the average with visible outliers. This visualization emphasizes the need to understand user sentiment better.

3. **Heatmap of Quality vs. Overall Ratings**: 
   - This heatmap illustrates the correlation between overall ratings and quality ratings, reinforcing the notion that higher quality ratings tend to correspond with higher overall ratings.

## Clustering and Segmentation
Using clustering algorithms, the dataset was segmented into **10 distinct clusters**. The cluster sizes varied significantly, with the largest cluster containing **592 entries** and the smallest containing **50**. The characteristics of these clusters suggest differing user groups with varying preferences and reviews of content. For example, users in the largest cluster may have a more favorable bias toward certain genres or content types.

## Implications and Recommendations
The analysis suggests several actionable recommendations:
1. **Targeted Marketing Campaigns**: Given the dominance of English reviews, stakeholders might consider focusing on marketing for non-English content in regions with high potential viewership.
2. **Quality Improvement Initiatives**: The quality ratings suggest a need for content improvement; stakeholders should explore user feedback to enhance content quality further.
3. **Enhanced User Engagement**: Identifying popular titles can lead to targeted campaigns or discussions to engage viewers and encourage more reviews.

## Future Work
To enhance the understanding of the dataset, the following analyses or visualizations could be performed:
1. **Time-Series Analysis**: Analyzing trends in reviews over time to identify peak periods for content reception.
2. **Sentiment Analysis**: Utilizing text analysis on review content to gauge sentiment and correlate it with numerical ratings.
3. **Comparative Analysis**: Comparing user ratings across different types of media to draw insights into user preferences.

## Vision Agentic Enhancements
Incorporating advanced visual analysis techniques could provide deeper insights:
1. **Interactive Dashboards**: Building dashboards that allow stakeholders to filter and visualize data dynamically based on various attributes (e.g., language, type).
2. **Image-Based Analysis**: Utilizing machine learning to analyze images related to content (like posters) to see if visual appeal correlates with higher ratings.
3. **Augmented Reality Visualizations**: Using AR to visualize data trends and patterns in a spatial context, making it easier for stakeholders to interpret complex data relationships.

This comprehensive analysis provides a solid foundation from which to draw actionable insights and strategic recommendations for stakeholders in the media and entertainment industry.

## Interactive Visualizations
[overall_vs_quality_interactive.html](overall_vs_quality_interactive.html)
