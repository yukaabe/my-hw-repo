### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Awesome job on this assignment! You did some serious processing in this assignment, and took advantage of many of the tools that Pandas has to offer with skew, boolean indexing, and more! Moving forward, I definitely recommend that you try re-writing some of those big code blocks in shorter code that is in a method. For example, you could write a method like, `find_outliers(df, column_name)` that takes in a dataframe and the column that you want to investigate and it would do the calculations of 1.5 standard deviations, find if there are values that are outside of the range, and report the index! Take a stab at it! This logic also follows for imputing the mean. Also, as I mentioned in class, you can easily use some pandas methods to impute the mean/median rather than just selecting specific indexes! Take a look at these links below:
https://chrisalbon.com/python/pandas_missing_data.html
http://www.dummies.com/programming/big-data/data-science/data-science-how-to-deal-with-missing-data-in-python/

Also, when you write those functions/methods, take a look at using the `.apply()` method for dataframes! You will definitely want to take advantage of this. Look at this [walkthrough for more info!](https://chrisalbon.com/python/pandas_apply_operations_to_dataframes.html)

**Some Notes**

* Regarding correlation matrices, you can use the numpy correlation method, but you can also just use `DataFrame.corr()` as a method that will output something much more readable and clean.
* Regarding your analysis plan, you should probably include what models/modeling techniques you think you should use. Considering we haven't gotten into it yet, this is more than okay to not include. However, typically when you write out your analysis plan, you include data cleaning, data manipulation, some analysis, and then modeling techniques to find, in this case, the relationship between Admission and Prestige!
