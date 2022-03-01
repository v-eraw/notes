# HTTP

### [Web servers and HTTP (a primer)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First\_steps/Client-Server\_overview#web\_servers\_and\_http\_a\_primer) <a href="#web_servers_and_http_a_primer" id="web_servers_and_http_a_primer"></a>

Web browsers communicate with [web servers](https://developer.mozilla.org/en-US/docs/Learn/Common\_questions/What\_is\_a\_web\_server) using the **H**yper**T**ext **T**ransfer **P**rotocol ([HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)). When you click a link on a web page, submit a form, or run a search, the browser sends an _HTTP Request_ to the server.

This request includes:

* A URL identifying the target server and resource (e.g. an HTML file, a particular data point on the server, or a tool to run).
* A method that defines the required action (for example, to get a file or to save or update some data). The different methods/verbs and their associated actions are listed below:
  * `GET`: Get a specific resource (e.g. an HTML file containing information about a product, or a list of products).
  * `POST`: Create a new resource (e.g. add a new article to a wiki, add a new contact to a database).
  * `HEAD`: Get the metadata information about a specific resource without getting the body like `GET` would. You might for example use a `HEAD` request to find out the last time a resource was updated, and then only use the (more "expensive") `GET` request to download the resource if it has changed.
  * `PUT`: Update an existing resource (or create a new one if it doesn't exist).
  * `DELETE`: Delete the specified resource.
  * `TRACE`, `OPTIONS`, `CONNECT`, `PATCH`: These verbs are for less common/advanced tasks, so we won't cover them here.
* Additional information can be encoded with the request (for example, HTML form data). Information can be encoded as:
  * URL parameters: `GET` requests encode data in the URL sent to the server by adding name/value pairs onto the end of it — for example `http://mysite.com?name=Fred&age=11`. You always have a question mark (`?`) separating the rest of the URL from the URL parameters, an equals sign (`=`) separating each name from its associated value, and an ampersand (`&`) separating each pair. URL parameters are inherently "insecure" as they can be changed by users and then resubmitted. As a result URL parameters/`GET` requests are not used for requests that update data on the server.
  * `POST` data. `POST` requests add new resources, the data for which is encoded within the request body.
  * Client-side cookies. Cookies contain session data about the client, including keys that the server can use to determine their login status and permissions/accesses to resources.

Web servers wait for client request messages, process them when they arrive, and reply to the web browser with an HTTP Response message. The response contains an [HTTP Response status code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) indicating whether or not the request succeeded (e.g. "`200 OK`" for success, "`404 Not Found`" if the resource cannot be found, "`403 Forbidden`" if the user isn't authorized to see the resource, etc). The body of a successful response to a `GET` request would contain the requested resource.

When an HTML page is returned it is rendered by the web browser. As part of processing the browser may discover links to other resources (e.g. an HTML page usually references JavaScript and CSS pages), and will send separate HTTP Requests to download these files.

Both static and dynamic websites (discussed in the following sections) use exactly the same communication protocol/patterns.

\
