# GraphQL / Apollo

GraphQL was developed by Facebook as an alternative to the standard REST API architectural style. It was designed to be faster and more flexible/efficient. GraphQL lets developers construct requests that can pull data from multiple data sources in a single API call.



API developers use GraphQL to create a **schema** to describe all the possible data that clients can query through that service.&#x20;

A GraphQL schema is made up of object types, which define which kind of object you can request and what fields it has.&#x20;

As **queries** come in, GraphQL validates the queries against the schema. GraphQL then executes the validated queries.

The API developer attaches each field in a schema to a function called a **resolver**. During execution, the resolver is called to produce the value.
