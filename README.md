## Heroku buildpack: Erlang Dialyzer

This is a Heroku buildpack for producing Dialyzer results of an Erlang app.

### Configure your app

```shell
$ heroku create --buildpack "https://github.com/tsloughter/heroku-buildpack-erlang-dialyzer.git"
```

### Add post-commit hook

Create  .git/hooks/post-commit:

```shell
#!/bin/sh

git push heroku master > /dev/null 2>&1 &
```

Make executable:

```shell
$ chmod a+x .git/hooks/post-commit
```

### View output

```shell
$ heroku open
```
