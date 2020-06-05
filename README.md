heroku-buildpack-statsite
=================================

A [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for compiling statsite.

You can set the statsite version via an ENV variable.

```bash
heroku config:set STATSITE_VERSION=8dd7750
```

STATSITE_VERSION can be any reference supported by git, such as a SHA or branch name.

After the first compile the build is cached. If you change the version you need to force a rebuild:

```bash
heroku config:set STATSITE_REBUILD=true
```

After it's been rebuilt you should unset it.

```bash
heroku config:unset FREETDS_REBUILD
```

