# temporal

1. [Getting Started](https://learn.temporal.io/getting_started/python/first_program_in_python/)
2. Install Temporal server https://learn.temporal.io/getting_started/python/dev_environment/?os=linux
3. Once installed, start the temporal server
4. Temporal uses in memory database, for persistence use this `temporal server start-dev --db-filename your_temporal.db`
   
```bash
temporal server start-dev

CLI 1.5.1 (Server 1.29.1, UI 2.42.1)

Server:  localhost:7233
UI:      http://localhost:8233
Metrics: http://localhost:32859/metrics
```

The Temporal Application will consist of the following pieces:

1. A **Workflow** written in your programming language of choice using the Python SDK. A Workflow defines the overall flow of the application.
2. An **Activity** is a method that encapsulates business logic prone to failure (e.g., calling a service that may go down). These Activities can be automatically retried upon some failure.
3. A **Worker**, provided by the Temporal SDK, which runs your Workflow and Activities reliably and consistently.