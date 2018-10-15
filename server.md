# Sautogen Server
* Written in Microsoft .NET Core C#  
* IDE used: Visual Studio   
* Protocols used: HTTPS, SSL (currently self-signed)  

The Salutogen server is implemented using .NET Core C#. The server consists of two parts: 
1.	Web application
2.	Web API

## Web application
The web application provides an interface for the end-user to apply CRUD (Create Read Update Delete) operations with an intuitive and simple user interface.  Authorization is implemented using Identity User, while the database operations are implemented with Entity Framework Core which in turn is using the Code first approach to design the database. 
The current database provider used is Microsoft SQL Server. However, this can easily be changed to other database providers supported by .NET Core.

## Web API
The main purpose of the web API is to provide database read and write operations for external application such as the Salutogen android application. 
To increase the security, the WEB API supports a very limited subset of CURD operation. For example, it is not possible for a third-party application to delete data. Please refer to the Appendix – section API to get an overview of the tested API functionalities. 
