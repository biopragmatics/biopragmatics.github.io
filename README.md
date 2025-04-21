# Biopragmatics Stack

## Serve Locally

```console
$ docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:4.2.0 jekyll serve
```

Note that the 4.2.0 tag is important - 4.2.2 (latest, released ~2022) does not
work.

This is using an old version of Jekyll Minima:
https://github.com/jekyll/minima/tree/v2.5.1

## Lint

```console
$ npx prettier --prose-wrap always --check "**/*.md" --write
$ npx prettier --prose-wrap always --check "**/*.yml" --write
```
