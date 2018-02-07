
# Approach with queries (New Relic Question 2 query SQL code)

Revenue is calculated using APM_MRR, which is a monthly value. Since it is broken out daily, 
we need to calculate the number of months the subcriptions has been active, and multiply it by the APM_MRR for each account. 
We also need to take into account 2 separate type of accounts: active all through 2016, and started or ended in 2016.

We will pull the agent languages and the difference between subscription start date and end date (or through 12/31/16) as the latest day avialable)
in months. We then multiply the APM_MRR for each respective account times those number of months the plan was active. These come from the customer_history
tables. We then join the Cluster_Agents table on account_ids being the primary keys. We need to call on the agent_lanugages to determine apm_mrr by language.

We write 2 separate queries: to calculate revevenue from accounts with active subscriptions through 2016 (i.e. null or '1900-0-1'
and revenue from accounts that had plans that ended in 2016. In cases where plans have been active prior to 2016, we choose the greater between 1/1/16 and customer_history.plan_start date so that we do not calculate other months prior to 2016. To address plan starts with null starts, we specify that those
records not be included.

# Results

TOTAL:
- PHP: $5,771.
- DOTNET: $119.
- RUBY: 0. 
- Python: 0.
- nodejs: 0.
- PHP: 0. 
- Java: 0. 

Query 1 (active through 2016 results):
php	$3,582
php	$1,791

Query 2 (with plans ending or starting in 2016:
php	$398
dotnet	$119

PHP was utilized by 2 account ids: 683694 and 966979. DOTNET was utilized by 1 account: 1160071.


