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
  # 3.
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
  ls.status=2 AND COUNT(ls.status)>0
  AND us.status=2
# 5.
   INSERT INTO `clicks` VALUES (33,3,4.00,'USD','2019-12-12 16:18:43');
   SELECT Max(id) FROM clicks
# 6.
SELECT
ls.name
FROM
Listings ls
WHERE ls.id
NOT IN( SELECT id FROM
clicks cl
WHERE YEAR(cl.created)='2013')
