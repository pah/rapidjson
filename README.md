RapidJSON -- svn-authors information
====================================

The branch `svn/authors` contains an `svn-authors` file to hold the
SVN <-> Git author mappings.

In order to follow the SVN updates in your local fork as well, configure the
`git svn` authorsfile after cloning this repository:

````
  SVN_AUTHORS=`git rev-parse --git-dir`/svn-authors
  git config svn.authorsfile $SVNAUTHORS
  git show origin/svn/authors:svn-authors > $SVNAUTHORS
````

Afterwards, you can initialize the `svn.remote` for this repository and update
to the latest revision:

````
  git svn init http://rapidjson.googlecode.com/svn/trunk/
  git svn fetch fetch --use-log-author
````

The branch `svn/trunk` strictly follows the `git-svn` remote.

-- 
Philipp A. Hartmann (@pah), 2014-02-01
