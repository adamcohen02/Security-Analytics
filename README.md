**Security Analytics Risk Scoring Project**

**Introduction**:
This repository contains the documentation and analysis of a comprehensive security analytics project aimed at categorizing individual users with a risk score. 
This score reflects their activity based on collected security data, focusing on Data Loss Prevention (DLP) incidents.

**Project Description**:
The project's core objective was to develop a risk scoring system that could categorize users into risk categories based on their behavior and interaction with security protocols. 
The focus was on DLP incidents, including print control, data transfer via plugins, device monitoring, and control, as well as upload and post activities. 
Each incident was evaluated and marked by a severity level relative to the organization's preset standards.

**Methodology**:
Data was aggregated and analyzed using unsupervised learning modules from sklearn. The analysis involved clustering techniques that categorized users into risk categories: low, medium, high, higher, and highest. This stratification allows for a nuanced understanding of user behavior and risk potential within the organization's security framework.

**Findings**:

_Cluster_ 0 - Lowest Risk: This cluster is characterized by values close to zero across all features, indicating minimal deviations from the norm. The low count of unique violation days, rule violations, and total violations, coupled with negligible file sizes across all severities, suggests that the activities within this cluster are within expected security parameters. Therefore, it is reasonable to assign the 'Lowest risk' label to this cluster, as it represents the baseline or control group against which other clusters are compared. 

_Cluster_ 1 - Moderate Risk: Although this cluster has a higher count of unique rule violations, the unique violation days and total violations are still below average. The significant increase in severity_2 violations and corresponding file size indicates a potential for moderate impact breaches. However, the lack of high severity across other categories justifies a 'Moderate risk' classification, as the cluster does not exhibit the highest levels of risk factors. 

_Cluster_ 2 - High Risk: This cluster stands out with the highest values in total violations and severity_1 violations, along with a substantial file size for severity_3 violations. The combination of frequent and severe violations, especially with large file sizes, points to a pattern of high-risk security incidents. Assigning this cluster to 'High risk' reflects the serious nature of the violations and the potential for significant impact on the company. 

_Cluster_ 3 - Higher Risk: With values that are generally high across several features, including the highest file sizes for severity_4 violations and significant counts in Device Monitoring and Control, this cluster indicates a heightened level of risk. The presence of the highest severity violations and large file sizes associated with them suggests that incidents within this cluster could have a more severe impact than those in Cluster 2, justifying the 'Higher risk' designation. 

_Cluster_ 4 - Highest Risk: This cluster exhibits the highest count of total violations and a very high count of unique rule violations. The extremely high file size for severity_3 violations, coupled with the highest values in Uncategorized and Upload file sizes, indicates a pattern of severe security breaches with extensive data involved. Such a pattern represents the most critical risk to the company, warranting the 'Highest risk' classification.


**Acknowledgments**
Gratitude to the security analytics team for their continuous support and collaboration.



