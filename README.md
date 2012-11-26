## Heroku buildpack: Erlang Dialyzer

This is a Heroku buildpack for Erlang apps. It uses [Rebar](https://github.com/basho/rebar).


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
