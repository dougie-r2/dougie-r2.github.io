---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
draft: true
{{ $path := .File.Dir }}
{{ $sections := split (trim $path "/") "/" }}
{{ if and (gt (len $sections) 1) (eq (index $sections 0) "posts") }}
{{ $category := index $sections 1 }}
categories: 
  - "{{ $category }}"
{{ if in (slice "math" "ML" "science" "programming" "physics" "statistics" "engineering") $category }}
math: true
toc: true
{{ else }}
math: false
toc: false
{{ end }}
{{ else }}
categories: []
math: false
toc: false
{{ end }}
tags: 
  - "untagged"
description: ""
---