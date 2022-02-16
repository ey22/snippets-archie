---
title: JSONL
description: Newline Delimited JSON
date: 2022/02/15
tldr: How to create a JSONL module, similar to the JSON global, that stringifies and parses newline delimited JSON.
tags: [JavaScript, JSON]
---

You can create a global `JSONL` module using the folloiwng code:

```js
const JSONL = {
  stringify: array => array.map(JSON.stringify).join('\n'),
  parse: string => string.split('\n').map(JSON.parse)
}
```

This should achieve parsing strings of ND-JSON to JavaScript objects, and stringifying arrays into ND-JSON.
