# GartnerTest
# 1. 
SELECT
  id
  ,first_name
  ,last_name
  ,email
  ,status
  ,created
FROM users
WHERE id in(2,3,4)
# 2.
SELECT
first_name
,last_name
,COUNT(listing.status)
FROM
  listings ls
INNER JOIN
  Users us
ON
  ls.user_id=us.id
 GROUP BY 
  first_name
  ,last_name
 HAVNG
  us.status=2
   
