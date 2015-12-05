#Eric Young
#Homework #1
#12.7.15

1. Using chipotle.tsv in the data subdirectory:
	i. Look at the head and the tail, and think for a minute about how the data is structured. What do you think each column means? What do you think each row means?

	   Column names are order_id, quantity, item_name, choice_description, and item_price. Each row represents a specific item as part of an order (i.e. multiple rows can belong to the same order_id).

	   Code used: head chipotle.tsv
	   Code used: tail chipotle.tsv

   ii. How many orders do there appear to be?

       There appear to be 1834 orders, assuming orders are sorted .

       Code used: tail chipotle.tsv

  iii. How many lines are in the file?

       There are 4623 lines in the file.

       Code used: wc -l chipotle.tsv

   iv. Which burrito is more popular, steak or chicken?

       There were 553 chicken burritos ordered and 368 steak burritos ordered, so chicken burritos are more popular.

       Code used: grep -i "chicken burrito" chipotle.tsv | wc -l
       Code used: grep -i "steak burrito" chipotle.tsv | wc -l

    v. Do chicken burritos more often have black beans or pinto beans?

       Chicken burritos more often come with black beans. There were 282 chicken burritos that came with black beans and 105 that came with pinto beans.

       Code used: grep -i "chicken burrito" chipotle.tsv | grep -i "black beans" | wc -l
       Code used: grep -i "chicken burrito" chipotle.tsv | grep -i "pinto beans" | wc -l

2. Make a list of all of the CSV or TSV files in the DAT19 repo (using a single command). Think about how wildcard characters can help you with this task.

   -airlines.csv
   -chipotle.tsv
   -drinks.csv
   -hitters.csv
   -housing-data.csv
   -imdb_1000.csv
   -titanic.csv
   -ufo.csv
   -vehicles_test.csv
   -vehicles_train.csv
   -yelp.csv

   Code used: find . -name *.*sv

3. Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT19 repo.

   There were 121 occurrences of the word 'dictionary' across all files in the repo.

   Code used: grep -r -i "dictionary" . | wc -w 

**Optional:**Use the the command line to discover something "interesting" about the Chipotle data.

   There were 4589 unique records and 4623 total records, so there are duplicate records in this dataset.

   Code used: uniq chipotle.tsv | wc -l
   Code used: wc -l chipotle.tsv 




