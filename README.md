# Challenge Week 12 Submission Template

# Name: Chris Wittenberg

Points Earned: 98

# Reddit Data Challenges

## Challenge 1

![screenshot](RCheckpoint1.png?raw=true)

## Challenge 2

There are subreddits for EVERYTHING!

![screenshot](RCheckpoint2.png?raw=true)

Also, people really like to Ask Reddit, find something humorous, and look at Advice for Animals.

![screenshot](RCheckpoint4.png?raw=true)

## Challenge 3

You can find out what are the most popular subreddits based on this data by aggregating the number of posts based on subreddits. 

![screenshot](RCheckpoint4.png?raw=true)

## Challenge 4

It would tell us about the real interests of the Reddit Community.

![screenshot](RCheckpoint4.png?raw=true)

## Challenge 5

These are MongoDB Querries

Query1 = db.reddit.aggregate([ {$group: { _id: "$subreddit", count: {$sum: 1}}},{$sort: {"count": -1}}]), array = [];

for (i = 0; i < 50; i++) array.push(Query1[i]["_id"]);

Query2 = db.reddit.find({"subreddit": {$in: array}}, {"_id" : 0, "name": 1 }), array2 = [], num = db.reddit.count({"subreddit": {$in: array}});

for (i = 0; i < num; i++) array.push(Query1[i]["name"]);

Query1 = db.reddit.aggregate([ $match: {"name": {$in: array2}}, {$group: { _id: "$subreddit", count: {$sum: 1}}},{$sort: {"count": -1}}]), array = [];

[Answer]

I could not get this working with MongoDB. It does not support relational calculations very well, and the dataset was so monstrously huge that queries took forever to run. Also, I could not get the python code to work because my python interpreter did not recognize the libraries. 

## Challenge 6

The data is biased toward incumbent subreddits because these subreddits are the ones getting visited, and therefore upvoted. However, newer subreddits will not get as much traffic and nearly as many upvotes. This would change my conclusion because it would change the subredits that would be analyzed, and therefore the users we would look at. 

## Challenge 7

The data is also biased based on positivity. Reddit is very well-know for being laden with users known as "trolls". Comments of trolls are extremely deragatory in nature and will not be upvoted, but due to Reddit's reputation for trolls I am sure there are a lot of trollish comments that are not getting looked at, not to mention users with tendency to leave deragatory comments all over Reddit that would be ignored.

## Challenge 8

I would query the top 50 subreddits based on total comments using MongoDB and compare them to what the python code decided what the top 50 subreddits are. 

# Yelp and Weather 

## Challenge 1

![screenshot](YCheckpoint1.png?raw=true)

62

## Challenge 2

![screenshot](YCheckpoint2.png?raw=true)

Answer: 110.08333 mph

## Challenge 3

[![screenshot](YCheckpoint3.png?raw=true)

Answer: 31305

## Challenge 4

![screenshot](YCheckpoint4.png?raw=true)

Answer: 522104

## Challenge 5

![screenshot](YCheckpoint5.png?raw=true)

Answer: 185907

## Challenge 6

[Query snippet]
[Answer]

## Challenge 7 [BONUS]

[Code]
[Answer]



