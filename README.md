# CriticalityScoreAnalysis
Analysis and Improvement of the Criticality Score Algorithm

Research I conducted over Purdue Summer Internship

Open source software (OSS) projects are third-party resources increasingly targeted by software supply chain attacks. To counteract this, a criticality score algorithm identifies the most important OSS projects to prioritize their security. The algorithm uses $10$ features extracted from GitHub projects in a deterministic calculation to measure their criticality. However, the current criticality score algorithm suffers from inconsistent and redundant features. In this work, we examine the weaknesses of these features through statistical analysis and identify the most important features to create a more consistent, precise criticality score. First, we randomly selected $100$K from $900$K GitHub projects to visualize the high-dimensional data using t-SNE. Then, we calculate each feature’s correlation and display the results in a heat map. Furthermore, we model the data using Linear, Lasso, and ElasticNet regression to help with feature selection. The best regression had a test $R^2$ value of $0.71$. Lastly, we use Recursive Feature Extraction, SelectFromModel, Sequential Forward Floating Selection, and Sequential Backward Floating Selection to determine the $5$ most essential signals. The resulting regression from these $5$ features has a test $R^2$ value of $0.70$, indicating that only these features are necessary to calculate the criticality score. The criticality algorithm using these consistent features paves the way for better identifying important OSS projects. Future work will create a non-deterministic criticality score with machine learning algorithms or Graphs for Understanding Artifact Composition (GUAC).

See the Criticality Score Paper document.


