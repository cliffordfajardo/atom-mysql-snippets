# MySQL-snippets

> A collection of MySQL commands for optimizing modern MySQL development productivity.

![](https://raw.githubusercontent.com/cliffordfajardo/mysql-snippets/master/mysql-snippets-demo.gif)
![The MIT License](https://img.shields.io/npm/l/express.svg)


## Install

```shell
$ apm install mysql-snippets
```










### Contributing/Suggestions

Feel free to let me know ([link](https://github.com/cliffordfajardo/mysql-snippets/issues)) what else can be improved/added or you can also submit a PR.










## Snippets Overview
- [Database](#database)
- [Table](#table)
- [Table components](#create-table-components)
- [Insert](#insert)
- [Select](#select)
- [Query options](#query-options)
- [Update](#update)
- [Delete](#delete)
- [Alter](#alter---modify-anything)
- [Trigger](#trigger)
- [Procedure](#procedure)
- [Function](#function)
- [Constructions](#constructions)
- [Show](#show)
- [User](#user)
- [Privileges](#privileges)
- [Other](#other)










### Database
| Snippet Code     | Description    |
| -----------------|----------------|
| s-db             | create a new database |
| s-db-drop        | delete the database |










### Table
| Snippet Code     | Description    |
| -----------------|----------------|
| s-table | create simple table with INT primary key |
| s--table | create simple table with INT primary key, but first remove the old table |
| s-table-tmp | create simple temporary table with engine=memory |
| s--table-tmp | the same, but first remove the old table |

**s-many-many** - Very powerful snippet! Make table for relation *many-to-many*, make two foreign key constrain, and two indexes in it and make two indexes in corresponding tables










### Create Table components
| Snippet Code     | Description    |
| -----------------|----------------|
| s-fk | make foreign key constrain for table creation |
| s--fk | make foreign key constrain for table creation with corresponding indexes |
| s-idx | make default index for table creation |
| s-idx-txt | make `FULLTEXT` index for table creation |
| s-pk | make primary key |
| s-uk | make unique key |










### Insert
| Snippet Code     | Description    |
| -----------------|----------------|
| s-i | insert multirow |
| s-ione | insert one row |
| s-ifrom | isert data from a sample(other table or database)|










### Select
| Snippet Code     | Description    |
| -----------------|----------------|
| s-s       | default *select* for extending with help *query-options* |
| s-sone    | *select* one row by *where* condition |
| s-sinline | inline *select* for simple a sample |
| s-smin    | inline *select* for search *min* value |
| s-smax    | inline *select* for search *max* value |
| s-scount  | inline *select* for count rows in the table |
| s-ss      | select a value `SELECT '...';` |
| s-sv      | select a variable `SELECT `...`;` |










### Query options

**Expressions**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-| the entity. Like `` `table`.`column` ``|
| s--| the entity with a comma. Like ``, `table`.`column` ``|
| s-alias | the entity with alias. Like `` `table`.`column` AS `my_col` ``|
| s--alias | the same with comma. Like ``, `table`.`column` AS `my_col` ``|
| s-and | a part of conditions `` AND ( ... ) `` |
| s-or | a part of conditions `` OR ( ... ) `` |
| s--and | a part of conditions with expression `` AND ( `col` = `col2` ) `` |
| s--or | a part of conditions with expression `` OR ( `col` = `col2` ) `` |
| s-e | an expression ``( `col` = `col2` )``|

**Statements**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-f |`from` statement like `` FROM `table` AS `alias` ``|
| s-j |`inner join` statement |
| s-jleft |`left join` statement |
| s-jright |`right join` statement |
| s-w |`where` statement |
| s-o |`order by` statement |
| s-l |`limi` statement |
| s-g |`group by` statement |
| s-h |`having` statement |
| s-u |`union` statement |










### Update
| Snippet Code     | Description    |
| -----------------|----------------|
| s-u | default `update` snippet with `where` condition |










### Delete
| Snippet Code     | Description    |
| -----------------|----------------|
| s-d | default `delete` snippet with `where` condition |










### Alter - modify structure
All `alter` snippets begining from ``s-alter-*`` prefix, like `s-alter-add`.

**Columns**

| Snippet Code     | Description    |
| -----------------|----------------|
| add | add a column to table at the last column |
| add-first | add a column to table at the first column |
| add-after | add a column to table after someone column |
| auto-increment | change `auto_increment` counter value |
| change |`change` the column(rename or change type)|
| modify |`modify` the column(change type and column order)|
| drop | drop the column from the table |

**Other**

| Snippet Code     | Description    |
| -----------------|----------------|
| idx           | add an index to the table |
| idx-drop      | drop the index from the table |
| order         | sort the table by column(yes it indeed possible!) |
| table-rename  | rename the table |
| table-charset | change table charset and collate |
| db-charset    | change database charset and collate |
| fk            | add foreign key to the table |
| -fk           | add foreign key to the table with index |
| fk-drop       | drop the foreign key from the table |
| uk            | add unique key to exists table |










### Trigger

| Snippet Code     | Description    |
| -----------------|----------------|
| s-trig | create new trigger |
| s--trig | replace trigger(drop and create new)|
| s-trig-list | list triggers for table |
| s--trig-list | list triggers for table(also specify DB)|
| s-trig-drop | drop the trigger |










### Procedure

| Snippet Code     | Description    |
| -----------------|----------------|
| s-proc | create new storage procedure |
| s--proc | replace procedure(drop and create new)|
| s-proc-drop | drop the storage procedure |
| s-proc-list | show stored procedures list(only current database)|










### Function

| Snippet Code     | Description    |
| -----------------|----------------|
| s-func | create new function |
| s--func | replace function(drop and create new)|
| s-func-drop | drop the function |
| s-func-list | show list of user-defined functions(only current database)|










### Show

| Snippet Code     | Description    |
| -----------------|----------------|
| s-hcols   | details of the table (`SHOW FULL COLUMNS FROM ...`) |
| s-hcreate | show command for creating the table |
| s-hidx    | show indexes for the table |
| s-hrel    | show relations of a table (using `information_schema`) |










### Constructions

**Declare**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-dec     | declare a variable |
| s--dec    | declare a variable with default value |
| s-dec-s   | declare a *string*(`VARCHAR`) variable |
| s--dec-s  | declare a *string*(`VARCHAR`) variable with default value |
| s-dec-h   | declare a `CONTINUE `*`HANDLER`*` FOR SQLSTATE`|
| s-dec-cur | declare a cursor |


**Condition**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-if  | create `if`  statement |
| s--if | create `if else` statement |


**Case**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-case     | `CASE var_name WHEN 'value' THEN ... END CASE` - value based |
| s-case-w   | `WHEN 'value' THEN ... ;` - value based |
| s-case-wb  | `WHEN 'value' THEN BEGIN ... END;` - value based |
| s--case    | `CASE WHEN var_name = 'value' THEN ... END CASE` - condition based |
| s--case-w  | `WHEN var_name = 'value' THEN ... ;` - condition based |
| s--case-wb | `WHEN var_name = 'value' THEN BEGIN ... END;` - condition based |


**Loops**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-loop    | `LOOP ... END LOOP` - Complex snippet. With additional logic! |
| s-repeat  | `REPEAT ... UNTIL ... END REPEAT` construct |
| s--repeat | `REPEAT BEGIN ... END; UNTIL ... END REPEAT` construct |


**Other**

| Snippet Code     | Description    |
| -----------------|----------------|
| s-cur | powerful complex snippet! Makes ready to use cursor |










### User

| Snippet Code     | Description    |
| -----------------|----------------|
| s-user-list | list all users |
| s-user-add | create a new user |
| s--user-add | create a new user with a password (short access `s--u`)|
| s-user-add-hash | create new user with a password by hash |
| s-user-drop | remove user |
| s-user-pwd | change user password |










### Privileges

| Snippet Code     | Description    |
| -----------------|----------------|
| s-priv-refresh | command `flush priveleges`|
| s-priv-add | add some privileges to user |
| s-priv-add-all | add _all_ privileges to user |
| s-priv-drop | remove some privileges from user |
| s-priv-drop-all | remove _all_ privileges from user |
| s-priv-list | show list of user privileges |










### Other

| Snippet Code     | Description    |
| -----------------|----------------|
| s-delim | make `delimiter $$` statement and at the end `delimiter ;`
| s-utc | select current `timestamp`|










### Contact Me
- [@github/cliffordfajardo](https://github.com/cliffordfajardo/)
- [@twitter/cliffordfajard0](https://twitter.com/cliffordfajard0)










### Credits
- [Idleberg](https://atom.io/users/idleberg/) for his [Atomizer](https://atom.io/packages/atomizr) package that helped me convert Sublime snippets into Atom's format.
- [ancor-dev](https://github.com/ancor-dev) for his [sublime-sql-snippets package](https://github.com/ancor-dev/sublime-sql-snippets), which I used for the snippets in this package.
