---
title: Snippets
weight: 1
hidden: true
chapter: false
disableToc: false
---

<!-- A document to collect useful snippets of code (handy for students and for copying and pasting during live demos). Delete menu params entry on `config.toml` if not required --!>



## Setup chunk

````markdown
```{r setup, include=FALSE}
knitr::opts_chunk$set(
  echo = TRUE,
  warning = TRUE,
  message = TRUE,
  comment = ""
)
```
````

