# Chinese Pandoc Docker Image
## Contains
- Ubuntu:18.04 base
- Latest TeX Live
    - Japanese packages
    - LuaTeX
    - latexmk etc...
- Japanese Fonts (Noto)
- [jgm/pandoc](https://github.com/jgm/pandoc)
- [lierdakil/pandoc-crossref](https://github.com/lierdakil/pandoc-crossref)
- [jgm/pandocfilters](https://github.com/jgm/pandocfilters) 

## How to build
```
$ docker build -t shanghaikid/pandoc .
```

## Built image
```
$ docker pull shanghaikid/pandoc
```

## Publish
$ docker login
$ docker push shanghaikid/pandoc

## How To Use
```
$ docker run -it --rm -v `pwd`:/workspace shanghaikid/pandoc pandoc yourfile.md -o output.pdf --pdf-engine=luatex
```

# Thanks
- https://github.com/aruneko/texlive
- https://github.com/k1LoW/docker-alpine-pandoc-ja