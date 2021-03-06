{% include online-assignment/intro.md %}

# Problem

We are given advertising metrics for two companies. We want to calculate **if there is a discrepancy/difference** between the two datasets.

# Dataset format

The data is in JSON files and the two companies use the exact same JSON format.

The advertising metrics are aggregated on an hourly basis.

Each JSON file contains a list of objects (one for each hour) and each object has the following properties:

| Field | Type | Description |
|---|---|---|
| timestamp | string | The timestamp of the hour that this object is representing (in ISO 8601 format) |
| spend | decimal | The total spend/revenue generated in this hour |
| impressions | integer | The total impressions (ad views) generated in this hour |

You can view a sample [here](/test-cases/companyA.json).

# Objective

We want to create a system which will take as input the two datasets (one for Company A and one for Company B) and will return a list of the hours for which we detected a discrepancy higher than 5% in any of the two metrics (spend and impressions). 

{% include online-assignment/deliverables.md %}

{% include online-assignment/test-cases-intro.md %}

| Description | Expected input | Expected output |
|---|---|---|
| No discrepancies detected | [Company A dataset](/test-cases/companyA.json) and [Company B dataset](/test-cases/companyB-no-discrepancies.json) | Empty list |
| Discrepancies detected | [Company A dataset](/test-cases/companyA.json) and [Company B dataset](/test-cases/companyB-discrepancies.json) | [Expected output](/test-cases/expected-discrepancies.json) |

{% include online-assignment/assessment-criteria.md %}