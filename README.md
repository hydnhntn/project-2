# Project-2

Best Elden Ring Weapons

Where original data was stored, how it was formatted, how we extracted it:
After dying an embarrassing number of times while playing the new open world action RPG Elden Ring we set out to create databases that could be used to determine the best starting classess and weapon choices. We turned to our trust advisor, Google, and discovered the following sources:
https://eldenring.wiki.fextralife.com/Weapons
https://www.pcgamer.com/all-elden-ring-classes-origins/
The sites above contained tables of all the unique classes and weapons options, along with the corresponding stats. The tables were formatted in HTML. Using the Python library Beautiful Soup, we extracted the data from these tables.

Types of data wrangling required before that data was usable:
Several of the cells in the weapons tables listed both the base damage done, along with a modifier. Since these two values were listed in the same cell, we had to split these up so that we could convert this data into integers. We needed to perform integer operations so these cells, coded initially as string, had to be split and converted into floats. Some cells had non-integer values, such as question marks and other symbols. Those we replaced with null values. We did not have to do any data cleaning of the classes table prior to transformation into the schemata chosen below.

What schemata we used in the final database and why we chose it:
Once this was all cleaned up, we used Pandas to convert to data frames and used MongoDB to convert to databases. We used Pandas so we could more easily manipulate the data as data frames. We used Mongo so we could create databases.  We ended up with four distinct schemata.
