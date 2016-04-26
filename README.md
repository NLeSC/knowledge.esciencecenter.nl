# knowledge.esciencecenter.nl
NLeSC knowledge website

## Adding a Book

1. Create new Markdown file (.md) in `_books/` directory.
2. Fill following FrontMatter properties

    * title: Human readable name of book.
    * url: Url of book (e.g. pdf or GitBook).
    * cover: Url of cover image

3. Fill main body with short description of book.

## Generating cover image

If you have a pdf of a book you can create an cover by coverting the first page using imagemagick:

```
convert book.pdf[0] book-cover.png
```

## Preview website

The website uses Jekyll powered Github pages.

To preview locally use docker:
```
docker run --rm --volume=$(pwd):/srv/jekyll -i -t -p 127.0.0.1:8080:80 jekyll/jekyll:pages
```
The website can be viewed on http://localhost:8080
