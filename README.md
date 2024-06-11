# Python-Basics-Date-and-Time-Mastery
Handling Dates &amp; Times in Python


1
from tests import tests


Store a Specific Date (and Time)


import datetime

# Store the current date and time
dt = datetime.datetime.now()

dt # Output example: "datetime.datetime(2024, 3, 12, 11, 50, 49, 521069)"
datetime.datetime(2024, 6, 10, 21, 15, 36, 330619)

1
tests.ch1()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+



# Store a specific date and time
dt = datetime.datetime(2024, 6, 6, 12, 0, 0)

dt # Output example: "datetime.datetime(2024, 1, 1, 12, 0)"
datetime.datetime(2024, 6, 6, 12, 0)






Use the Strftime Method to Format Dates and Times as Strings

# Create a datetime object
dt = datetime.datetime.now()

# Use strftime to convert the datetime object to a string in the format "YYYY-MM-DD HH:MM:SS"
dt_string = dt.strftime("%Y-%m-%d")

print(dt_string) # Output example: 2024-03-11
print(type(dt_string)) # Output example: <class 'str'>
2024-06-10
<class 'str'>

1
tests.ch4()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+






Parse Strings into Datetime Objects

string_date = "2024-01-01 12:00:00"

# Parse the string_date into a datetime object
dt = datetime.datetime.strptime(string_date, "%Y-%m-%d %H:%M:%S")

print(dt) # Output example: 2024-01-01 12:00:00

string_date1 = "21 June, 2023"
date_object1 = datetime.datetime.strptime(string_date1, "%d %B, %Y")

print(date_object1) # Output example: 2023-06-21 00:00:00

2024-01-01 12:00:00
2023-06-21 00:00:00

1
tests.ch6()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+





Operations with Dates

from datetime import datetime, timedelta

date1 = datetime(2023, 12, 30)
date2 = datetime(2024, 1, 4)
difference = date1 - date2
print(difference) # Output example: -5 days, 0:00:00

date1 += timedelta(days = 30) 
print(date1) # Output example: 2024-01-29 00:00:00
-5 days, 0:00:00
2024-01-29 00:00:00

1
tests.ch8()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+





Access the Datetime Object Properties


from datetime import datetime

date = datetime(2023, 12, 28, 23, 55, 59)

print("Year =", date.year) # Output example: Year = 2023
print("Month =", date.month) # Output example: Month = 12
print("Hour =", date.hour) # Output example: Hour = 23
print("Minute =", date.minute) # Output example: Minute = 55
Year = 2023
Month = 12
Hour = 23
Minute = 55

1
tests.ch10()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+



Other Datetime Methods


import datetime
import pytz

# Create a timezone object for the Eastern Time zone
et = pytz.timezone("US/Eastern")

# Create a datetime object representing the current date and time in the Eastern Time zone
dt = datetime.datetime.now(et)

# Convert the datetime object to the Pacific Time zone
pt = pytz.timezone("US/Pacific")
dt_pt = dt.astimezone(pt)

print(dt) # Output example: 2024-03-12 06:01:52.114071-04:00 
print(dt_pt) # Output example: 2024-03-12 03:01:52.114071-07:00

timestamp = dt_pt.timestamp()
print(timestamp) # Output example: 1710237712.114071
2024-06-10 17:21:01.057916-04:00
2024-06-10 14:21:01.057916-07:00
1718054461.057916

1
tests.ch12()
+----------------------------------------------------------+
Test Passed!
+----------------------------------------------------------+

Start writing or add content...


text
Text

Python
Python
