# cascading-avro

Cascading scheme for reading and writing data serialized using Apache Avro. This project provides several
schemes that work off an Avro record schema.

- AvroScheme - sources and sinks tuples with fields named and ordered according to a given Avro schema.
- TextScheme - A variant of of standard Cascading TextDelimited scheme that uses an Avro schema to infer
field names and types.
- RenamerScheme - used to coerce field names (mostly for using with Cascalog)

The current implementation supports all primitive types, byte arrays (including fixed), as well as, union of null
and another supported type.

# cascading-avro-maven-plugin

An Apache Maven plugin that generates classes with field name constants based on Avro record schema. This plugin
is similar to standard Avro schema plugin used to generate specific objects for Avro records. For The plugin names
generated classes by appending the word "Fields" to the record name. The generated class will have constant fields
for all record fields, as well as, a field named ALL that lists all fields in the expected order.

## License

Copyright (c) 2012 MaxPoint Interactive, Inc. All Rights Reserved.
Distributed under Apache License, Version 2.0
