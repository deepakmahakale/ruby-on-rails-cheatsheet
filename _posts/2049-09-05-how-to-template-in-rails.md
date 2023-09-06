---
date: 2049-09-06
title: How to do something?
categories:
  - migration
description: >
  Need to do something?
  Let's see how to do it.
type: Document
---

## rename_column

Syntax:

```ruby
rename_column(table_name, column_name, new_column_name)
```

Example:

rename_column(:users, :email_id, :email)

Rails Command:

```bash
$ rails generate migration rename_email_id_to_email email
```
