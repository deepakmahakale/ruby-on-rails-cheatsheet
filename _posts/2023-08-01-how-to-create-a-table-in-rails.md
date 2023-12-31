---
date: 2023-08-01
title: How to create a table in rails?
categories:
  - migration
description: >
  Need to create a table in rails?
  Let's see how to do it.
type: Document
image: /images/og/how-to-create-a-table-in-rails.jpg
---


## Table

Create an articles table

```bash
$ bin/rails generate migration CreateArticles
```

Generates the following migration:

```bash
# db/migrate/20230803041631_create_articles.rb
class CreateArticles < ActiveRecord::Migration[7.1]
  def change
    create_table :articles do |t|

      t.timestamps
    end
  end
end
```

## Table with fields

Create an articles table with title and content fields

```bash
$ bin/rails generate migration CreateArticles title content:text
```

Generates the following migration:

```bash
# db/migrate/20230803042216_create_articles.rb
class CreateArticles < ActiveRecord::Migration[7.1]
  def change
    create_table :articles do |t|
      t.string :title
      t.text :content

      t.timestamps
    end
  end
end
```

## Table with references

Create an articles table with references

```bash
$ bin/rails generate migration CreateArticles title content:text user:references
```

Generates the following migration:

```bash
# db/migrate/20230803042543_create_articles.rb
class CreateArticles < ActiveRecord::Migration[7.1]
  def change
    create_table :articles do |t|
      t.string :title
      t.text :content
      t.references :user, null: false, foreign_key: true

      t.timestamps
    end
  end
end
```

## Table with indexes
## Table with additional indexes
## Table with polymorphic associations

## References
- [https://guides.rubyonrails.org/active_record_migrations.html](https://guides.rubyonrails.org/active_record_migrations.html)

## Note
All the commands have been tested with rails 7.1 and the result may differ with prior versions
