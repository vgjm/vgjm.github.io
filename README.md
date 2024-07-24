# vgjm.github.io

### Develop on Windows

The _Newline_ is stored as `CRLF` on Windows but `LF` on MacOS and Linux, which may lead to CSS integrity check problems. Since most CI/CD runs on Linux, do the following change on Windows to adopt the `LF` _Newline_ character.

```
git config --global core.autocrlf input
```

### Deploy to github pages

I have set github pages to read this repo's `/docs` directory of `main` branch as the source of [https://vgjm.github.io]. Run

```
hugo
```

then hugo will generate static files into `/docs` directory. This is controlled by `publishDir` setting of `/hugo.toml`.

### favicon files

These files under /static are favicons.

- favicon-16x16.png
- favicon-32x32.png
- favicon.ico
