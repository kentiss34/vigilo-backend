### Upgrade
Before upgrading you should disable INNODB STRICT MODE by launching in MySQL CLI:

```
SET SESSION innodb_strict_mode=OFF;
```

#### For all upgrades

##### Update source code

###### For versions < 0.0.17

* Update source code from last version branch (replace X.X.X by the latest release)
```
$ git fetch origin
$ git checkout X.X.X
```

###### For versions >= 0.0.17

* Update source code from last version branch (replace X.X.X by the latest release)

```
$ git fetch --all --tags --prune
$ git checkout v0.0.17
```

##### Update database

* Launch in MySQL the SQL scripts in mysql/init/ corresponding to the superior versions order by the version number.

Example :
  If your current version is 0.0.12, launch init-0.0.13.sql then init-0.0.14.sql then init-0.0.15.sql then ...

* Execute if needed the specific actions below 

#### Specific actions

#### 0.0.11/0.0.12 to 0.0.13

* Go the page https://URL/admin/ and go to the "Observations" pages and follow the instructions

