---
title: Example Book
sub_title: Example sub-title
date: 2024-02-25
authors:
  - Tom
categories:
  - Book
tags:
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
book_authors:
  - Author Name
book_rating: 5
cover:
  image: images/book-cover.webp
draft: true
---

{{< book
  title="Example title"
  subTitle="Example sub-title"
  author="Example Author, Example Second Author"
  cover=images/book-cover.webp
  link1="https://www.amazon.pl/link-to-example-book"
  link2="https://link-to-the-review.page"
  link3=""
  link4=""
>}}


<!--
To generate covers, I use imagemagick's `convert` command:
```bash
convert book-orig.jpg -resize 625x625^ -gravity Center book-cover.webp
```
-->
