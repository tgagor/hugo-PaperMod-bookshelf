# hugo-PaperMod-bookshelf
Set of shortcodes and templates extending original PaperMod theme, with a page dedicated to listing the books I've read

# Installation

1. It requires original [PaperMod theme](https://github.com/adityatelange/hugo-PaperMod), [install it first](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation).

2. Clone repo to your project

- as submodule (recommended)
    ```bash
    cd your-site-location

    git submodule add --depth=1 https://github.com/tgagor/hugo-PaperMod-bookshelf.git themes/PaperMod-bookshelf

    # fetch submodule for the first time
    git submodule update --init --recursive
    ```
- or by just cloning
    ```bash
    cd your-site-location

    git clone https://github.com/tgagor/hugo-PaperMod-bookshelf.git themes/PaperMod-bookshelf --depth=1
    ```

# Adding books

Theme rely on posts in the `content/books` directory.

To add new book, just use `book` archetype:

```bash
hugo new -k book books/2024/lotr
```

It will generate "a blog post" describing the book, with additional fields which are required to make the mechanism work. They are:

```yaml
title: Book's title
sub_title: Book's sub title
date: Date when you read the book
book_authors:
  - A list of
  - All the authors
categories: # used for finding the books among other posts
  - Book
tags:       # categories of books, use/extend as you want
  - Biography
  - Business
  - Fantasy
  - Finance
  - Graphic Novel
  - Leadership
  - Management
  - Mystery
  - Politics
  - Pop-sci
  - Psychology
  - Security
  - Sci-fi
  - Science
  - Sociology
  - Technology
  - Trading
book_rating: 5  # your raging 1-5 stars
```

Archetype adds a shortcode `book` call, which add's a nice header with book's cover and can link to few websites (reviews, affiliate links, whatever).

Full structure should look like below

```bash
$ tree your-site-location
.
├── archetypes/
│   ├── book/
│   │   ├── images/
│   │   ├── index.md
├── assets/css/extended/
├── content/
│   ├── posts/
│   │   ├── your-posts-here
│   ├── books/
│   │   ├── 2024/
│   │   |   ├── my-first-book/
│   ├── bookshelf.md
│   ├── .../
├── themes/
│   ├── PaperMod/
│   ├── PaperMod-bookshelf/
├── config.yaml
├── ...
```

# Extend Hugo's blog config

```yaml
theme:
  - PaperMod
  - PaperMod-bookshelf

params:
  cover:
    responsiveImages: true
    hidden: false # hide everywhere but not in structured data
    hiddenInList: false # hide on list pages and home
    # setting to true will show potentially huge cover image, I prefer to disable it
    # hiddenInSingle: false
```
