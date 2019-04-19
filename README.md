# wkhtmltopdf Buildpack

This is a [Heroku buildpack][0] for bundling a compatible [wkhtmltopdf][1] binary with your environment.

`wkhtmltoimage` binary is not included in this buildpack.

## Versions

* Buildpack:   `0.2`
* wkhtmltopdf: `0.12.5`

## Usage

This buildpack only installs wkhtmltopdf, it isn't very useful by itself. You'll probably want to use add it to you current buildpacks config.

```bash
$ heroku buildpacks:add https://github.com/notvad/wkhtmltopdf-buildpack
```

### Clearing Repo Cache

Remember to clean your repository cache if you are updating the version of buildpack. To do that, run:

```bash
$ heroku plugins:install https://github.com/heroku/heroku-repo.git
$ heroku repo:purge_cache -a appname
```

## Troubleshooting

If you run into issues when trying to deploy with this buildpack, make sure your app is running on Cedar with Ubuntu 14.04 (`cedar-14`, heroku-16, or heroku-18). You can check this with:

```bash
$ heroku stack
```

[0]: http://devcenter.heroku.com/articles/buildpacks
[1]: http://wkhtmltopdf.org/
