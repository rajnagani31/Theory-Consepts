<h1> What is Middleware</h1>

ANS:
They work before view and after work views.
Middleware is a way to process requests and responses globally before they reach the views or after views return a response.


<h3>>>> Two Type Middleware </h3>
<hr>
1.Function based middleware

2.Class based middleware

<h3>>>> Use Case </h3>
<hr>
You can use middleware for:

Logging

Security

Authentication

Exception handling

Modifying request/response

<h3>>>> Fix meddileware Expales for specific work:</h3>
<hr>

1.process templates middleware:

      any cheakin and test befor view
2.Exception middlewares:

    first cheak Exception and after work view

<h2> Type of middleware </h2>

### 1.Built-in Middleware:
 they avilabel in seetings.py file

 ### 2.Custom Middleware:

 Developers can create their own middleware classes to implement specific logic or functionalities not covered by the built-in middleware. This allows for tailored modifications to the request/response cycle, such as logging, performance monitoring, or custom authentication schemes.

