Secondary Table:-
-----------------
-> Generally, one entity class is connected to one table(called the primary table).
-> Sometimes we can convert and store data in multiple tables of one class. 
-> For this, along with the primary table, another table(s) are created, which are known as Secondary table(s). 

Notes:-
-----
1. Every Secondary table gets a primary key column automatically.
2. We can create multiple Secondary Tables for one class.
3. @Table indicates Primary Table.
   @SecondaryTable indicates Sec. table
4. For more than in sec. tab(s) format is
   @SecondaryTables({
             @SecondaryTable(name="..."),
             @SecondaryTable(name="...")
     })   
5. At the column level, provide sec. table name using @Column(name="",table="")
   . If the table name is not provided for the column, then it will be stored in PrimaryTab
     (that is, @Table(name="..."))
6. To change the Primary key column name in the Sec. table, use code:
   pkJoinCoulmns=@PrimarykeyJoinColumn(name="colName")
   **** It is  optional ****
