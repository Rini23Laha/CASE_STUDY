#  Data Engineer Case Study


# Task 1 - Joining Data Sets
For the task, assume that we have a database with the following schema:

SELECT
t.transaction_category_id,
SUM(t.transaction_amount) AS sum_amount,
COUNT(DISTINCT t.user_id) AS num_users
FROM transactions t
JOIN users u USING (user_id)
WHERE t.is_blocked = False
AND u.is_active = 1
GROUP BY t.transaction_category_id
ORDER BY sum_amount DESC;

## Task 2: who traveled with their parents?

Given a list of travelers and a guest list of hotels the travelers stayed at, identify the set of travelers that may have stayed in the same hotel as one of their parents (ordered by name). Assume that there must be an age difference of at least 16 years between a child and their parents. 


## Task 3: help the hotel manager

You are asked to support the management of a hotel, more specifically **how many rooms** should be prepared and opened for each given week. We want to minimize the number of served rooms so that we also minimize maintenance costs. Assume that the number of guests is always 2 per room and that a room can always be made available the same day as the check-out date.

As input you are given a list of the reservations with the check-in and check-out dates.
