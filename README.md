# auditrail_in_mssql_server

Hi guys,

I was struggling to create sql code which automatically makes a audit (shadow) table for chosen tables in a database. I figured it out 
and put an example in this repo. 

Advantages of the code are:
- applicable on every table in a ms sql database
- will track all DML changes in the database for the given tables
- only saves updated/deleted/inserted values
- saves all the changes of the different tables into one big audit table

Disadvantages of the code:
- it contains dynamic query
- it take to much of your memory if you put it on too many tables for too long (which is the case with all audit tables)

Still needs work on:
- optimizing the code
- I've written the code for one table in one database but if you only change these names it should work if you've created the sc_audit
schema and audit table it will try and write up to the point where you only need to change one or two variables

