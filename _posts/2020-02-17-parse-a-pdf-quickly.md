---
title: "Parse a pdf, quickly"
date: "2020-02-17"
tags: 
  - "pdf"
  - "tabula"
---

1. You have docker installed.
2. You don't have time to futz around with PDFs

If you have a PDF you'd like to get tables out of, tabula works a dream. When last I used it successfully, I was on my mac. I jumped on to a windows machine, and I just couldn't get it to run.

\*a few googles later\*

I found a docker command that hosts a web API that gives access to tabula:

**docker run -p 8080:8080 -e HOST=0.0.0.0 gavinkflam/tabula-api:1.0.0**

At the [readme](https://github.com/gavinkflam/tabula-api) for this container, the example was this:

curl -X POST -H 'Content-Type: multipart/form-data' \\
  -F 'file=@my-pdf-file.pdf' -F 'guess=true' -F 'pages=all' \\
  http://localhost:8080/api/extract

Thankfully, because of WSL, I just popped over into bash and I had tables in a flash 😎
