# MVC (Model-View-Controller)

A software design pattern usually used when designing user interfaces.

Model

The central component of the pattern. It is the application's dynamic data structure, independent of the user interface.[\[10\]](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller#cite\_note-10) It directly manages the data, logic and rules of the application.

View

Any representation of information such as a chart, diagram or table. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.

Controller

Accepts input and converts it to commands for the model or view.[\[11\]](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller#cite\_note-11)

In addition to dividing the application into these components, the model–view–controller design defines the interactions between them.[\[12\]](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller#cite\_note-posa-12)

* The model is responsible for managing the data of the application. It receives user input from the controller.
* The view renders presentation of the model in a particular format.
* The controller responds to the user input and performs interactions on the data model objects. The controller receives the input, optionally validates it and then passes the input to the model.

As with other software patterns, MVC expresses the "core of the solution" to a problem while allowing it to be adapted for each system.[\[13\]](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller#cite\_note-gof-13) Particular MVC designs can vary significantly from the traditional description here.[\[14\]](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller#cite\_note-14)



![](<../.gitbook/assets/image (1).png>)
