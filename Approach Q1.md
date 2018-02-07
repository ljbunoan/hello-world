# Approach with queries (New Relic Question 1 query SQL code)

Revenue is calculated using MRR. Since it is broken out daily, 
we need to calculate the number of months the subcriptions has been active, and multiply it by the MRR for each account. 
We also need to take into account 2 separate type of accounts: currently active (to-date), and ended.

We will pull the account IDs and the difference between subscription start date and end date (or through 6/1/17 as the latest day avialable)
in months. We then multiply the MRR for each respective account times those number of months.These come from the customer_history
tables. We then join the Accounts table on account_ids being the primary keys. We define the application type to be limited to 
limited to those consumers who are using Ruby.

We write 2 separate queries: to calculate revevenue from accounts with current active subscriptions as of June 2017 (i.e. null or '1900-0-1'
and revenuefrom accounts that had defined plan start and end dates. To address plan starts with null starts, we specify that those
records not be included.

# Results
Overall total for Ruby customers is: $2,476.
For accounts to-date: total is $1,791 (from account 1549877). 
For accounts with start and end plan dates: total is $685 ($447 from 917573,	$238 from 1574191).


