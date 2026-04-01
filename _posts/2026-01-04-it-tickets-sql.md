---
layout: post
title: IT Tickets Sql
date: 2026-01-04
description:
repo:
category: Data
permalink: /posts/2026-01-04-it-tickets-sql/
---
Sqlite Python Setup
- Use an sqlite database in python with basic SQL operations.

```python
# Import sqlite libraries
import sqlite3
import pandas as pd

# Create a new sqlite database in memory
conn = sqlite3.connect(":memory:")
cursor = conn.cursor()
```

[View Github](https://github.com/shiyunx/it-tickets-sql)