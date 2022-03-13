# Databases

{% tabs %}
{% tab title="Relational" %}
![](<../.gitbook/assets/image (1) (1).png>)

* MySQL
* PostgreSQL
* MariaDB
* Oracle DB
* SQL Server (Microsoft)
* SQLite
* Amazon RDS

SQL (**S**tructured **Q**uery **L**anguage) is a programming language used to communicate with data stored in a relational database management system. SQL syntax is similar to the English language, which makes it relatively easy to write, read, and interpret.
{% endtab %}

{% tab title="Document Store" %}
![](<../.gitbook/assets/image (1) (1) (1).png>)

* Amazon DynamoDB
* MongoDB
* Couchbase
* Google Cloud Firestore
* Redis

The term document in NoSQL databases refers to a set of key-value pairs, typically represented in JSON, XML, or a binary form of JSON.
{% endtab %}
{% endtabs %}





## Goals

* to design a performant and future-proof database
* eliminate redundant data
* maintain accuracy and integrity
* provide quick access

steps:

1. identify the purpose of the database
   * how do clients want to access the data?
   * gather structure of data included, and list types
   * break down information into smallest useful pieces
   * avoid including the same data point in more than one table
2. organize data into tables
   * each row in the table is a record
   * assign the appropriate data type to each column
     * char - specific length of text
     * varchar - texxt of variable lengths
     * text - large amount of texts
     * int - positive or negative whole number
     * float, double - stores floating point numbers
     * blob - binary data
     * auto-number (automatically generates unique number in each row, can be used as a key)
3. determine keys + relationships
   * primary key - a unique id for an entry, one of a kind, used for identifying and querying a specific record
   * primary keys cannot be null nor empty
   * composite key - primary key that is multiple fields
4. normalize databases
   1.

**Types of Database Relationships**

{% tabs %}
{% tab title="One to One" %}
![one to one relationship](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/seo/database/discovery/un-representative1.svg)
{% endtab %}

{% tab title="One to Many" %}
![one to many relationship](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/seo/database/discovery/presidential-candidate.svg)
{% endtab %}

{% tab title="Many to Many" %}

{% endtab %}
{% endtabs %}



### Terms:&#x20;

data definition language

database management system

database performance level

storage space

cardinality - quantify of elements that interact between two related tables

one to one relationship - there's only one instance of A for every instance of B

## Further Resources

* [https://www.lucidchart.com/pages/database-diagram/database-design](https://www.lucidchart.com/pages/database-diagram/database-design)
