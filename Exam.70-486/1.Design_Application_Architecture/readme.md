## Material by topic

### Plan the application layers
    - Plan data access
	- plan for separation of concerns, appropriate use of models, views, controllers, components, and service dependency injection
	- choose between client-side and server-side processing
	- design for scalability
	- choose between ASP.NET Core and ASP.NET
	- choose when to use .NET standard libraries

### Design a distributed application
    - Design a hybrid application
	- plan for session management in a distributed environment
	- plan web farms
	- run Microsoft Azure services on-premises with Azure Pack
	- enable deferred processing through Azure features including queues, scheduled and on-demand jobs, Azure Functions, and Azure Web Jobs

### Design and implement the Azure Web Apps life cycle
    - Identify and implement Start, Run, and Stop events
	- code against application events in applications
	- configure startup tasks, including IIS, app pool configuration, and third-party tools

### Configure state management
    - Choose a state management mechanism including in-process, out of process, and Redis-based state management
	- plan for scalability
	- use cookies or local storage to maintain state
	- apply configuration settings in web.config files
	- implement sessionless state including query strings
	- configure middleware to enable session and application state in ASP.NET Core

### Design a caching strategy
    - Implement page output caching and data caching
	- create cache profiles
	- implement HTTP caching
	- implement Azure Redis caching
	- plan a content delivery network (CDN) strategy, for example, Azure CDN

### Design and implement a Web Socket strategy
    - Read and write string and binary data asynchronously
	- choose a connection loss strategy
	- decide when to use Web Sockets
	- implement SignalR
	- enable web socket features in an Azure Web App instance

### Design a configuration management solution
    - Manage configuration sources, including XML, JSON, and INI files
	- manage environment variables
	- implement Option objects
	- implement multiple environments using files and hierarchical structure
	- manage sensitive configuration
	- react to runtime configuration changes
	- implement a custom configuration source
	- secure configuration by using Azure Key Vault
	- use the Secret Manager tool in development to keep secrets out of your code for configuration values

### Interact with the host environment
    - Work with file system using file providers
	- work with environment variables
	- determine hosting environment capabilities
	- implement native components, including PInvoke and native dependencies for hosts including Linux and Windows
	- use ASP.NET hosting on an Open Web Interface for .NET (OWIN)-based server

### Compose an application by using the framework pipeline
    - Add custom request processing modules to the pipeline
	- add, remove, and configure services used in the application
	- design and implement middleware
	- design for kestrel, Http.sys web server and IIS
	- design and implement startup filters

## Microsoft preparation resources
- [Entity Framework Development workflows](http://msdn.microsoft.com/en-US/data/jj590134)
- [DataAdapters and DataReaders](http://msdn.microsoft.com/en-us/library/ms254931(v=vs.110).aspx)
- [ASP.NET State Management overview](http://msdn.microsoft.com/en-us/library/75x4ha6s(v=vs.100).aspx)