# What is Celery?

```bash
Celery is a powerful, open-source distributed task queue system written in Python.It allows you to run time-consuming or asynchronous tasks outside the main request-response cycle of your Django app.


Celery uses a message broker to pass task between your app to worker.comman brokers are redia and RabbitMQ.It can also use a backend (like Redis or a database) to store task results.
```

Key components:

* Broker — Queue storage (e.g., Redis)
- Worker — Process that runs the tasks
* Result backend — Stores task status/results (optional, often Redis)
* Tasks — Python functions decorated with @app.task

