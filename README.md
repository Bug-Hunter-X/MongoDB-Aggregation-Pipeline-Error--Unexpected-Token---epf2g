# MongoDB Aggregation Pipeline Bug
This repository demonstrates a common error in MongoDB aggregation pipelines and provides a solution.

## Bug Description
The provided MongoDB aggregation pipeline is designed to group users by city, calculate the average age within each city, and count the total number of users in each city. However, it throws an error due to incorrect use of the '$' symbol in the $group stage. 

## Solution
The solution involves correctly referencing fields within the $group stage.  The $avg operator should reference the 'age' field directly without the additional '$' prefix. The '1' in $sum is correct as it's a constant for counting users.

## How to Reproduce the Bug
1. Clone the repository.
2. Connect to your MongoDB instance.
3. Create a 'users' collection and insert sample data containing fields 'age' and 'city'.
4. Run the script 'bug.js'.
5. Observe the error.

## How to Run the Solution
1. Run the script 'bugSolution.js'.
2. Observe the correct aggregation result.

## Note
Ensure you have MongoDB installed and properly configured before running either script.