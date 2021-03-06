# A Game of Faces

A RESTful Web API for implementing a game of matching names and faces. Includes a simple MVC client.

## How to Run

### To Creat DB

Use Tools > Connect to Database to create Data.mdf in App_Data. Make sure SQL Server specified in connection string in web.config ((LocalDB)\MSSQLLocalDB) is correct.

Then run the following script in the context of the database.

```SQL
CREATE TABLE [dbo].[Statistics] (
    [Id]              INT IDENTITY(1,1) NOT NULL,
    [User]            NVARCHAR (50)     NOT NULL,
    [Total_Guesses]   INT               NOT NULL,
    [Correct_Guesses] INT               NOT NULL,
    PRIMARY KEY CLUSTERED ([Id] ASC)
);
```

### Specify a Profile Source in Application Settings

Add a profile source to web config and the test project's App.config. It must be a valid URI.

### Use IIS

You can simply use IIS Express and browse to the start page defined in project properties > Web to use the client, or use Postman etc. Turn Windows Authentication on in IIS.