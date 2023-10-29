--Basic understanding of the dataset for analysis
SELECT title,score
FROM hacker_news
ORDER BY score DESC
LIMIT 5;

SELECT SUM(score)
FROM hacker_news;

SELECT user, SUM(score)
FROM hacker_news
GROUP BY user
HAVING SUM(score) > 200
ORDER BY 2 DESC;

SELECT (517 + 309 + 304 + 282) / 6366.0;

SELECT user, COUNT(URL)
FROM hacker_news
WHERE url = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ'
GROUP BY 1
ORDER BY 2 DESC;

SELECT CASE
   WHEN url LIKE '%github.com%' THEN 'GitHub'
   WHEN url LIKE '%medium.com%' THEN 'Medium'
   WHEN url LIKE '%nytimes.com%' THEN 'New York Times'
   ELSE 'Other'
  END AS 'Source',
  COUNT(*)
FROM hacker_news
GROUP BY 1;

SELECT strftime('%H', timestamp) AS 'Hour', 
   ROUND(AVG(score), 1) AS 'Average Score', 
   COUNT(*) AS 'Number of Stories'
FROM hacker_news
WHERE timestamp IS NOT NULL
GROUP BY 1
ORDER BY 2 DESC;


/* Final comments 
The top 5 stories are
1. Penny Arcade – Surface Pro 3 update	517
2. Hacking The Status Game	309
3. Postgres CLI with autocompletion and syntax highlighting	304
4.Stephen Fry hits out at ‘infantile’ culture of trigger words and safe spaces	282
5.Reversal: Australian Govt picks ODF doc standard over Microsoft	191

The total score of all the stories is 6366

There are 4 individual users who have a combined scored of more than 200 and have a combined 22% of the total scores in the table.  
The highest score belongs to user vxNsr with a score of 517

The user named @sonnynomnom has posted the most number of links to trick readers into clicking on a link that is fake. This user has to be banned and it is recommended to issue a warning to @scorpiosister

The number of times stories are linked to Github, Medium and NewYorkTimes are 23,12 and 13 respectively.

The best hours to post a story is arounf 7 am in the morning and 6-8 pm in the evening
*/
