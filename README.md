# SQL-and-Git-cheatsheet

## Git stuff

#### Updating the branch you are in with the master branch
* `git checkout master`
* `git pull`
* `git checkout branch-to-update`
* `git merge master`

#### Removing files
* `git clean -f` removes files that are not tracked
* `git checkout .` removes files that are tracked
* `git reset --hard` removes staged and unstaged tracked files

## SQL stuff

Good explanation of SQL joins: http://stackoverflow.com/questions/406294/left-join-vs-left-outer-join-in-sql-server

```
CREATE TABLE <table-name> (
  column_a NUMBER(10,0),
  column_b NUMBER(10,0)   NOT NULL,
  column_c VARCHAR2(200)  NOT NULL
);
```

```
INSERT INTO <table-name>
(column_a, column_b, column_c)
VALUES
('value-a', 'value-b', 'value-c');
```

```
UPDATE <table-name>
SET column_a='value-b'
where id_column = 2;
```

```
CREATE SEQUENCE column_1_seq
START WITH 1
MAXVALUE 9999999999
MINVALUE 1
INCREMENT BY 2
NOCYCLE
CACHE 500
NOORDER;
```

