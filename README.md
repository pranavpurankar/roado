### A site is live at [https://pranavpurankar.github.io/roado]

## a) Mention the logic to figure out monthly logged in and active users for an year

### Algorithm:

1. Loop through each 'session' object once to process it.

2. Find relevant month for every session

3. The "logged_in" and "logged_out" time is used to check which month the date falls into.

4. Marking user as 'logged_in' for particular month, adding "user_id" to the respective set of month.

5. Create a set to store the logged in user. This set will contains all users logged in in a particular month

6. Checking the last logged in timestamp to make sure that user is active for a respective month.

7. Assuming whenever new entry is made; instead of checking every session against every month, only update relevant month directly

8. Two sets will find the active user count and logged in user counts in time complexity of O(N)


## b) List down the assumptions made in the logic

### Assumptions:
1. User logged in on multiple devices and they had mutiplee sessions => must have unique "user_id"

2. Complexity involved in handling overlapping, tried the same approach with segment trees but failed to achieve fair TC. So in-depth overlap analysis in a single month not considered.

3. Most important thing is data format, hard coded the data in UTC format.

4. Assumed that user logged in and logged out only once per device within the time range. Multiple login within the same month not considered.

5. Strategy is good for single year only.

## d) Given an option to get more data regarding the same, what would be the fields / key values that would help to get better accurate values for the same and how would it help the time complexity of the operation.

### Useful metric here could be:

* Sessio Duration :- 

Total session duration; this will reduce the operation of calulating the user was logged in for entire month or not. This metric can also reduce the calculation of date overlaps.
