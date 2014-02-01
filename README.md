RapidJSON -- svn-authors information
====================================

The branch `svn/authors` contains an `svn-authors` file to hold the
SVN <-> Git author mappings.

In order to follow the SVN updates in your local fork as well, configure the
`git svn` authors file after cloning this repository:

````
  SVN_AUTHORS=`git rev-parse --git-dir`/svn-authors
  git config svn.authorsfile $SVN_AUTHORS
  git show origin/svn/authors:svn-authors > $SVN_AUTHORS
````

Afterwards, you can initialize the `svn.remote` for this repository and update
to the latest revision:

````
  git svn init http://rapidjson.googlecode.com/svn/trunk/
  git svn fetch --use-log-author
````

The branch `svn/trunk` strictly follows the `git-svn` remote.

-- 
Philipp A. Hartmann <pah@qo.cx>, 2014-02-01
