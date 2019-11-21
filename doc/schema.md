
This file is all about the **schema** directory

**schema_builder** is mission critical to the whole tantivy ecosystem
and to better understand it you can search across either the src
directory or the examples directory.

##### This example is located in schema.rs

```
use tantivy::schema::*;

let mut schema_builder = Schema::builder();
let id_field = schema_builder.add_text_field("id", STRING);
let title_field = schema_builder.add_text_field("title", TEXT);
let body_field = schema_builder.add_text_field("body", TEXT);
let schema = schema_builder.build();
```


[On integer types in Rust](https://medium.com/@marcinbaraniecki/on-integer-types-in-rust-b3dc1b0a23d3) shows why for Hackernews ID's we want to use

```
pub fn add_u64_field
```

Unsigned integer types are those, that cannot hold negative values. Simply put — they cannot go below zero (think of unsigned as those, that can’t have a minus sign in front), and zero is exactly what is returned by their min_value() method..
