+++
title = "The Math behind a Calendar"
date = "2020-04-5"
math = true
+++

### Backstory

We all know that the earth takes 365 days to complete one revolution around the sun...or does it? Well, not quite. It takes approximately 365.2422 days. The early Julian Calendar (introduced by Julius Caesar) rounded off the decimal to one-fourths which accumulated to a day once every four years. Hence a day was added to every year (in Febuary as I'm sure you know) once in four years. This year was termed a leap year.

However this was still not accurate enough. The minor approximation meant that every 128 years, we lost a day. By the 16th century, 10 days were lost which meant that the Easter festival was celebrated at the wrong astronomical time. Pope Gregory XIII rectified this by introducing a new calendar and having 10 days omitted in the year 1582 - October 5 - October 15. For the coming years, the inaccuracy was fixed by the following scheme : Only the century years (years ending with 00) which are divisible by 400 are considered leap years.

### The Math Part

(Note \\(a \equiv b \\ (mod \\ n)\\) implies \\(b\\) is the remainder when \\(a\\) is divided by \\(n\\))

Our goal is to determine which day a particular date after 16th century falls on the Gregorian Calendar. For convenience we assign numbers to the days of the week. Sun - 0, Mon - 1 and so on till Sat - 6. \
Once again for convenience's sake, we first find what day the first of March falls on. Let our year be \\(Y\\). Number of days between March 1 of year \\(Y\\) and year of \\(Y+1\\) is \\(365\\) (assuming no leap years were involved). Since \\(365 \equiv 1 \\ (mod \\ 7)\\), the weekday of March of \\(Y+1\\) is one more than that of March 1 of the previous year \\(Y\\). If the year \\(Y+1\\) is a leap year, then we have \\(366\\) days and since \\(366 \equiv 2 \\ (mod \\ 7)\\), we add two days to the previous years March 1. 

For instance, if \\(D_{1600}\\) is the weekday number of March 1,1600, then March 1 in the years 1601, 1602, 1603 and 1604 are \\(D_{1600} + 1\\), \\(D_{1600} + 2\\), \\(D_{1600} + 3\\) and \\(D_{1600} + 5\\) (Since 1604 is a leap year). Now we devise a simple formula. 

\\(D_Y \equiv D_{1600} + (Y-1600) + L \\ (mod \\ 7) \equiv 3 + (Y-1600) + L \\ (mod \\ 7)\\) (\\(D_{1600}\\) was found to be a Wednesday = 3.)) \
Where \\(L\\) is the number of leap year days between March 1, 1600 and March 1 of the year \\(Y\\). 

First we find \\(L\\). For this we count the number of non-century years divisible by four and the number of century years divisible by 400. (Here we use the property \\([x-a] = [x]-a\\) where \\(a\\) is an integer). 

Number of elapsed years divisible by 4 = \\([\frac{Y-1600}{4}] = [\frac{Y}{4}-400] = [\frac{Y}{4}] - 400\\) 

Number of elapsed years divisible by 100 = \\([\frac{Y-1600}{100}] = [\frac{Y}{100}-16] = [\frac{Y}{100}] - 16\\)

Number of elapsed years divisible by 400 = \\([\frac{Y-1600}{400}] = [\frac{Y}{400}-4] = [\frac{Y}{400}] - 4\\) 

Now we get \\(L\\) by adding all the years divisible by 4, subtracting the ones divisible by 100 and adding back the ones divisible by 400 as only those are leap years. 

Now we get \\(L = ([\frac{Y}{4}] -400) - ([\frac{Y}{100}] - 16) +  ([\frac{Y}{400}] - 4) = [\frac{Y}{4}] - [\frac{Y}{100}] +  [\frac{Y}{400}] - 388\\) \
We substitute this back into \\(D_Y\\). 

Now we move to finding the days for other dates in the year. This is quite a simple task after we've established it for a single day. For example, April 1 is after 31 days from March 1. \\(31 \equiv 3 \\ (mod \\ 7)\\) so we add 3 days to March 1. Similarly we can determine the first days of the all months. The table of values to add to March 1 is given below. 

![table](/calendar_table.jpg#center)

Finally we move on to finding the day of a specific date, lets say the 17th of March. There are 16 days between March 1 and March 17th so we simply add \\(16 \equiv 2 \\ (mod \\ 7)\\), that is, 2 days to March 1. Indeed, March 15th falls on the same day as March 1 so March 17th is a further 2 away from it. Bringing all this together, we achieve our final desired formula : 

\\(D_Y \equiv (d-1) + 3 + i + [\frac{Y}{4}] - [\frac{Y}{100}] +  [\frac{Y}{400}] - 388 \\ (mod \\ 7)\\) \
where \\(d\\) is the date, \\(i\\) is the incremental value, \\(Y\\) is the year.
