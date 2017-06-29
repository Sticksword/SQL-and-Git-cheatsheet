# SQL-and-Git-cheatsheet

## Git stuff

#### Updating the branch you are in with the `master` branch
* `git checkout master`
* `git pull`
* `git checkout branch-to-update`
* `git merge master`

#### Removing files
* `git clean -f` removes files that are not tracked
* `git checkout .` removes files that are tracked
* `git reset --hard` removes staged and unstaged tracked files

#### Make new branch from `master`
* `git checkout -b <new-branch-name>`

#### Deleting branches
* `git branch -d <branch_name>` deletes local branch
* for deleting a branch remotely, see this for further info:
 * http://stackoverflow.com/questions/2003505/how-to-delete-a-git-branch-both-locally-and-remotely
 
#### Squashing / cleaning commits
* `git rebase -i origin/master`
* follow on screen instructions to mark stuff as `squash` or not
* `git push -f` after with new singular and cleaned commit message

## DB/SQL stuff

* consider read/write ratio
* http://dba.stackexchange.com/questions/31260/consistency-in-acid-and-cap-theorem-are-they-the-same
* https://docs.microsoft.com/en-us/azure/documentdb/documentdb-nosql-vs-sql
* Good explanation of SQL joins: http://stackoverflow.com/questions/406294/left-join-vs-left-outer-join-in-sql-server
* Constraints limit the columns
* Indexes can also limit columns (eg. unique index) but also make things faster
* `GROUP BY` info (see bottom answer) http://stackoverflow.com/questions/2421388/using-group-by-on-multiple-columns
* `EXPLAIN` is a great tool to analyze queries
* can kill long processes via `show full processlist` and then `kill <process-id>`
* SQL index DOs and DONTs: https://stackoverflow.com/questions/6098616/dos-and-donts-for-indexes

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

```
ALTER TABLE <table-name> [ADD|DROP|RENAME] [COLUMN|CONSTRAINT] <column-name|constraint-name>;
```

