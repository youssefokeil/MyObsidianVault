Created on: 31-08-2025 11:04, note by Youssef Okeil
Status: #idea
Tags: #BaRead 
# Book APIs
## ISBNdb \[paid]
pros:
- ~91 million unique books
- "The world's largest book database"
- gathers data from various public sources like libraries, merchants.
- great for non-EN books, local editions and rare books.

cons:
- pricing:
![[Pasted image 20250831111445.png]]
![[Pasted image 20250831111500.png]]

--------------
## OpenLibrary API \[free]
pros:
- completely free and open source
- has work, edition and author specific APIs
	work is a logical collection of similar editions, a work can be something like "Crime and Punishment", an edition can have everything from different translations or just different editions. Work can be thought of the umbrella under which all editions reside. 

cons:
- only 30million books
- may not be so good in specifying edition format (paperback, hardcover etc)
----------------
## Google Books API \[free with rate limits]
pros:
- (may) be more reliable than OpenLibrary
- provides additional information as we can make the user log in & find favorites and book-shelved on his google play books account.

cons:
- has a rate limit of 1000 queries per day
- may not be so good in specifying edition format (paperback, hardcover etc)
-------------
## Hardcover API \[free with rate limits]
pros:
- uses GraphQL, more flexible than REST
- gathers edition format data

cons:
- rate limit of 60 queries per minute
-----------------
# References