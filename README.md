# working-with-Databases

# 1. I had a brief challenge accessing mysql due to system failure in creating a port connection,however this was easily corrected by re-launching mysql and everything run smoothly.

# 2. In importing the netflix_titles.csv data into the database, it was pretty easy and straightforward.  

# 3. One interesting thing is the fact that a database had to be created first, an indication that when dealing with databases, there is some sort of order that must be adhered to for it to actually function.

# 4. Filtering data in the database is quite simple especially for single command logical operators and slowly increases in "complexity" where more that one logical operator commands have to be used together. 

# 5. In grouping data in sql, it's amazing and astonishing to see how vast amounts of data can be manipulated to create meaningful outputs.

# 6. sql conditional expressions are easy to use for evaluating conditions.

# 7.Another interesting thing when joining multiple tables is the fact that aliases more commonly referred to as nick-names in lay mans terms can be used to simplify a query, by shortening it while still maintaining it's readbility and functionality.

# 8. Aggregate functions are the easiest functions to use, with most from observation, capitalises more on integer type of data.

# 9.-- SELECT * FROM netflix_csv_db.netflix_titles;
# /* wanted to find out a director who has directed more tv/movie title and which titles and year was this were these*/
# SELECT show_id,director, release_year, COUNT(*) AS title_count, GROUP_CONCAT(title ORDER BY title ASC SEPARATOR ', ') AS directed_titles
# FROM netflix_titles
# WHERE release_year >2000
# GROUP BY show_id, director,release_year
# ORDER BY title_count DESC
# LIMIT 1;


# /*the highest number of cast produced by a given country*/
# -- SELECT IFNULL(country, 'Unknown') AS country_name, COUNT(*) AS cast_count
# -- FROM netflix_titles
# -- GROUP BY country
# -- ORDER BY cast_count DESC
# -- LIMIT 1;

# from trying to gain insight into the netflix dataset there was need to find out which director actually directed more movies, and this was to be movies direted after the year 2000.One director whose name popped up was Kirsten Johnson with the movie titled Dick Johnson is Dead. 
