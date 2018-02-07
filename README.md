# hello-world

 This is for answering questions for the New Relic Take Home Exercises.
 

# Analysis Tool(s) Used
 
 MYSQL and Microsoft Excel
 
 Downloaded MYSQL Community Suite for MAC. All datasets and tables were placed under the default "World" Schema upon installation.
 
# Challenges and Workarounds 

After running the Schema-creating queries, loading the .CSV files via Import Wizard led to errors from nulls (\N), formatting of dates/timestamps, and integers.

To work around these issues:

NULLS

- For integers and booleans: change values in csv file to 0.
- For dates: change format in csv file to "1900-1-0".
- For varchars and text: change "\N" to "null".

TIMESTAMPS
- Convert values in all csv files into format "yyyy-mm-dd".
Anything defined as TIMESTAMP in schema query changed to DATETIME.
