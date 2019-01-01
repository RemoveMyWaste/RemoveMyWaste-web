# Overview

This is a hostable web version of RemoveMyWaste.

# Find something wrong in the database or want to add a new center?

If you have a github account, you can submit issues [here](https://github.com/cs361-group24/database/issues).

Otherwise, you can (anonymously!) submit corrections or updates [here](https://removemywaste.liambeckman.com/issues).

# Development

Pull requests and forks welcome.

# Hosting

This version of the app depends on [this database](https://github.com/cs361-group24/database) submodule. Information on working with submodules can be found [here](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

## To clone the project and intialize database submodule

```sh
git clone --recurse-submodules https://github.com/cs361-group24/RemoveMyWaste-web/
```

## To update the database submodule

```sh
git submodule update --remote DbConnector
```

## To run the node server

```sh
cp dbcon-example.js dbcon.js
nano dbcon.js 
# add username and password info
# add database name 

# only if you want a portal for anonymous users to submit issues like
# https://removemywaste.liambeckman.com/issues
cp issue-auth-example.js issue-auth.js
nano issue-auth.js
# add OAUTH key

npm install
node database.js PORT
```
