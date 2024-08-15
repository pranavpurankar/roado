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
