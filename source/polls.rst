Poll Data Collection
=========================================================================


We wrote a Python program that gathers all of the polls that the Huffington Post Pollster API releases. The format of the data that the API returned was extremely overly verbose and nested in an unintuitive structure of lists within dictionaries within lists and so on, so we had to write another program that parsed each poll and converted it into a more readable format that reduced the amount of unnecessary data we were collecting. Once the poll was in the correct format, it was then stored in the poll table within our database. The file where this is accomplished is PollPopulateDatabase.py which is run by a cronjob daily.
