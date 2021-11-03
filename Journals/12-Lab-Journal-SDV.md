# SDV601 - Week 12 Blog

------

#### <u>How to read a CSV file from a URL with Python?</u>

------

What have I learned?

This week I learned about reading a CSV file from a URL using Python. This was a pretty straight forward task.

There are a few different methods that we can achieve this, as shown by ExceptionsHub (2018), but the most concise method I found is as follows:

```python
import pandas as pd
data = pd.read_csv('http://winterolympicsmedals.com/medals.csv')
print(data)

Returns:
      Year      City       Sport      Discipline  NOC            Event Event gender   Medal
0     1924  Chamonix     Skating  Figure skating  AUT       individual            M  Silver
1     1924  Chamonix     Skating  Figure skating  AUT       individual            W    Gold
2     1924  Chamonix     Skating  Figure skating  AUT            pairs            X    Gold
3     1924  Chamonix   Bobsleigh       Bobsleigh  BEL         four-man            M  Bronze
4     1924  Chamonix  Ice Hockey      Ice Hockey  CAN       ice hockey            M    Gold
...    ...       ...         ...             ...  ...              ...          ...     ...
2306  2006     Turin      Skiing       Snowboard  USA        Half-pipe            M  Silver
2307  2006     Turin      Skiing       Snowboard  USA        Half-pipe            W    Gold
2308  2006     Turin      Skiing       Snowboard  USA        Half-pipe            W  Silver
2309  2006     Turin      Skiing       Snowboard  USA  Snowboard Cross            M    Gold
2310  2006     Turin      Skiing       Snowboard  USA  Snowboard Cross            W  Silver
```


------

How have I learned this?

I have learned this by looking at tutorials online and following the steps to execute methods that read CSV files from a URL. I have practiced using the different types and how to implement them. 


------

Why have I learned this?

Python is a well used language when it comes to data analysis. Being able to read a CSV file from a URL rather than requiring the user to download the file or for us to create our own data source such as JSON drop removes the repetition of data. By doing this, we can eliminate the middleman and read directly from the sources. Another benefit is if the data source is added to or updated, we do not need to redownload the data or update the data in our remote storage.


------

What will I do to remember this learning?
I will continue to practice these techniques and find areas where I can implement this knowledge.

------

What is the point?

As stated before, we can pull the data directly from its source rather than using up unnecessary space in our own remote storage. This data will always remain up to date when the source is updated. This is a useful alternative to downloading the CSV and reading it from there.

------

What do I know now, that I did not know before?

- How to read a CSV file from a URL
- That the pandas library can use the `read_csv()` method to read from a URL, not just a local file
