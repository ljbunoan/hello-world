# Question 3: There was a severe security vulnerability discovered yesterday in versions 3.12.x.x ofour Ruby agent! How many customer accounts are affected? Create a list of email addresses of primary account admins that we can use to send notifications to affected customers.


# Approach

- Use of joining Users and Cluster_Agents Tables
- Use primary key of default_account_id in Users connecting to account_id in Cluster_Agents
- Limit results so that agent_version from Cluster_Agents starts with (is like) "3.12.%"
- Also limit agent language to Ruby.
- In the results, I will pull a distinct list of emails from the Users table.

# Result
106010, 986214, 1047875 are 3 distinct account ids that are affected by it. However, only account 106010 has an account email tied to the account id, which is pughashley@mendez-freeman.info 
