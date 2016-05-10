Alpine Edge with:

* Basic gcc development tools
* Alpine main, community and testing repositories for apk

Intended use is as a base for other images that need to build things
as part of their construction.  This is common in ruby and python
situations where the gcc tools are needed to build native
versions of gems or eggs.
