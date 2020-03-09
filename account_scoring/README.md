# Account Scoring

## Optimizing B2B Accounts Distribution & Prioritization - Outbound Accounts Scoring Model

### Introduction

### Goal

The goal of the following project is to create an account scoring model for Outbound accounts. The main motivation for such a model is to to aid in the distribution of accounts from managers to the SDR's(Sales Development Representatives) and ultimately help them lift their conversion rates(account to qualified lead) and consequently increase sales and revenue for the company.

To better understand what Outbound marketing is and the challenges it poses, as well as the difference with Inbound marketing, this article by Hubspot is very helpful.

### Challenges/Approach

The dataset we are dealing with is heavily imbalanced, which means that the positive examples are much fewer than the negative ones. Based on this observation, we decided to approach this as an anomaly detection problem and used techniques to combat the imbalanced classes.

| Field | Description |
|-------|-------------|
|region |The region where the account is located|
|billing_country|The country of the account|
|city|The city of the account|
|gtm_segment__c|Small Business, Mid-Sized or Enterprise|
|abm_group__c|The abm_group of the account|
|industry|The industry of the account(Clearbit)|
|ICP_tier|Account Tier, based on  Sub-Industry(Clearbit)|
|persona__c|Account persona|
|currently_using_group|What tech/ATS the account is using(if any)|
|received_funding|If the account received funding or not(from researcher_notes__c field in sfcd)|
received_series_a|If the account received series A funding or not(from researcher_notes__c field in sfcd)|
|received_series_b|If the account received series B funding or not(from researcher_notes__c field in sfcd)|
|received_series_c|If the account received series C funding or not(from researcher_notes__c field in sfcd)|
|hiring_multiple_locations|If the account is hiring on multiple locations or not(from researcher_notes__c field in sfcd)|
|growth_turnover|If the account has growth turnover or not|
|hiring|If the account is hiring or not|
|new_manager|If the account has a new manager or not|
|annual_revenue|Annual Revenue of the account(Clearbit)|
|has_at_least_one_non_company_email|If the account has generic email or not(from sfcd email)|
|has_atl_contact|If the account has above-the-line contacts or not|
|num_of_atl_contacts|The number of above-the-line contacts the account has|
|has_btl_contact|If the account has below-the-line contacts or not|
|num_of_btl_contacts|The number of below-the-line contacts the account has|
|num_contacts|The total num of contacts at the time of MQL datestamp|
