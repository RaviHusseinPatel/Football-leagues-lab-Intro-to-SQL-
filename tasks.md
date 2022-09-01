# Football Matches - Tasks

Each of the questions/tasks below can be answered using a `SELECT` query. When you find a solution copy it into the code block under the question before pushing your solution to GitHub.

1) Find all the matches from 2017.

```sql
<!-- 123404 -->
SELECT COUNT (*) FROM matches WHERE season=2017;
```

2) Find all the matches featuring Barcelona.

```sql
<!-- 608 -->

SELECT COUNT (*) FROM matches WHERE awayteam ='Barcelona' OR hometeam = 'Barcelona' ;
608

```

3) What are the names of the Scottish divisions included?

```sql
<!-- 3-->
SELECT name (*) FROM divisions WHERE country ='Scotland' ;



```

4) Find the division code for the Bundesliga. Use that code to find out how many matches Freiburg have played in the Bundesliga since the data started being collected.

```sql
<!-- 374 -->
SELECT COUNT (*) FROM matches WHERE division_code= 'D1' AND (hometeam= 'Freiburg' OR awayteam= 'Freiburg') ;

```

5) Find the unique names of the teams which include the word "City" in their name (as entered in the database)

```sql
<!-- 4 -->
select count (DISTINCT hometeam) FROM matches WHERE hometeam LIKE '%City'
```

6) How many different teams have played in matches recorded in a French division?

```sql
<!-- 61 -->
select count (DISTINCT hometeam) FROM matches WHERE (division_code = 'F1' OR division_code= 'F2');


```

7) Have Huddersfield played Swansea in the period covered?

```sql
<!-- 12-->
select COUNT (*) FROM matches WHERE (hometeam = 'Huddersfield' AND awayteam='Swansea') OR (hometeam = 'Swansea' AND awayteam='Huddersfield');

```

8) How many draws were there in the Eredivisie between 2010 and 2015?

```sql
<!-- 431 -->
select COUNT (*) FROM matches WHERE (ftr= 'D' AND division_code = 'N1' AND (season=2010 or season=2011 or season=2012 or season=2013 or season=2014 or season=2015));

```

9) Select the matches played in the Premier League in order of total goals scored from highest to lowest. Where there is a tie the match with more home goals should come first.

```sql
<!-- PL games in order from highest to lowest scoring draws -->
select * FROM matches WHERE (division_code='E0' AND ftr='D') ORDER BY fthg DESC;

```

10) In which division and which season were the most goals scored?

```sql
<!-- Copy solution here -->


```

### Useful Resources

- [Filtering results](https://www.w3schools.com/sql/sql_where.asp)
- [Ordering results](https://www.w3schools.com/sql/sql_orderby.asp)
- [Grouping results](https://www.w3schools.com/sql/sql_groupby.asp)