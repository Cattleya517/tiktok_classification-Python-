
# TikTok Video Classification: Predictive Modeling for Claim vs. Opinion Content

## Project Overview
This project developed a machine learning model to classify TikTok videos as either containing claims or expressing opinions. Using a dataset of 19,084 TikTok videos, we analyzed various attributes including view count, like count, and transcription text length. Our Random Forest model achieved a 99.2% recall score and a 99.6% accuracy score on the test data, demonstrating high effectiveness in distinguishing between claim and opinion videos.

## Business Understanding

Stakeholder: TikTok's content moderation team
Business Problem: Efficiently identify and mitigate potential misinformation on the TikTok platform. Claim videos are more likely to contain content that violates the platform's terms of service, making their accurate identification crucial for maintaining platform integrity and user trust.

## Data Understanding

The analysis utilized a dataset from Kaggle containing information on 19,084 TikTok videos. Key features included:

Video attributes: duration, transcription text
Author information: verification status, author status
Engagement metrics: view count, like count, share count, download count, comment count
Classification label: claim or opinion

### Exploratory Data Analysis (EDA) revealed:

Uneven distribution of engagement metrics across videos
Similar proportions of claim (9,608) and opinion (9,476) videos
Higher engagement rates for claim videos
Longer transcriptions in claim videos compared to opinion videos
Strong correlations among engagement metrics

## Modeling and Evaluation
We employed a Random Forest model, which outperformed XGBoost in our evaluation:

Data split: 60% training, 20% validation, 20% test

Hyperparameter tuning using grid search
Model selection based on recall score
Final model performance on test set:

Recall score: 99.2%
Accuracy score: 99.6%



The most predictive feature was found to be view count, suggesting that engagement metrics are effective predictors of a video's claim status.

## Conclusion
Recommendations:
Implement the Random Forest model to assist in identifying claim videos for priority review.
Increase moderation efforts on high-view-count videos, as they are more likely to contain claims.
Utilize the model to improve the efficiency of the content moderation workflow.

## Future steps:

1. Incorporate more features, such as video content analysis or user behavior patterns.
2. Regularly retrain the model with new data to maintain its accuracy over time.
3. Develop a real-time classification system for immediate content flagging.
4. Explore the potential for multi-class classification to further categorize video content.