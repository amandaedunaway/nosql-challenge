# nosql-challenge
## Module 12 Challenge

### Outline
The challenge consists of two .ipynb files.

The first file, "NOSQL_setup," imports the establishments.json file into a MongoDB database. The database is then updated with a new restaurant, and missing entries in the new document are updated using existing documents in the database as a reference. A location of no interest to the client is then removed. Finally, data types are converted as needed to perform operations in the analysis.

The second file, "NoSQL_analysis," answers four questions for the client:
- Which establishments have a hygiene score equal to 20?
- Which establishments in London have a RatingValue greater than or equal to 4?
- What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to Penang Flavours?
- How many establishments in each Local Authority area have a hygience score of 0, sorted from highest to lowest?

Additional comments are provided in "No_SQL_anlysis" cells that were not explained by the starter file.


### Resources
To complete this challenge, I used class activity solution files and notes that I took from the instructor during class for this module. I also referred to my .ipynb file from Project 1 for additional refreshing on checking data types. Finally, in a conversation with [ChatGPT](https://chat.openai.com/) about the differences between data types, I realized that I needed to revisit my data type conversion for latitude and longitude in part 5 of the set-up file. I had converted to Decimal128, which is not compatible with the nececssary addition operator in part 3 of the analysis file. Changing this to "toDouble" in my code gave the compatibility I needed and eliminated the error.