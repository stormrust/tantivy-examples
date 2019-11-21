
This file is all about the **schema** directory

##### This example is located in schema.rs

```
use tantivy::schema::*;

let mut schema_builder = Schema::builder();
let id_field = schema_builder.add_text_field("id", STRING);
let title_field = schema_builder.add_text_field("title", TEXT);
let body_field = schema_builder.add_text_field("body", TEXT);
let schema = schema_builder.build();
```
