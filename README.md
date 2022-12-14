# ExchangeRateSolution
Is a Backend 
Fixer.io API deserialize Data from the rate and currency and save to database.
Read the data from the database to a console log prosject.


## API Setup

First create a account in Fixer.io <br />
https://apilayer.com/marketplace/fixer-api#pricing 
<br />
get your API key from the website account page.
<br />
https://apilayer.com/account 

![key](https://user-images.githubusercontent.com/86916224/192824173-45005ac9-2d69-4fb0-b33c-d4833d4d8cc4.png)

Go to the Controller class 
and set the API key in the String apiKey

![key](https://user-images.githubusercontent.com/86916224/192825106-31dfd07b-6337-43bf-9517-00842da1aaab.png)


## Database Setup

Entity core will provide the tools needed to create the database through the model class.
We can access the data through the context object allowing us to query and save data.

To save the data from Fixer.io we need to create a database.
Go to SQL server Management studio and get the Server name

see documentation for setup. <br />
https://learn.microsoft.com/en-us/ef/core/miscellaneous/connection-strings

Add the server name inside  the connection string in the appsettings.json
Copy the connectionString name and write it in the GetConnectionString in the Program class inside the Web Api.
![connectionString](https://user-images.githubusercontent.com/86916224/192825313-e5059c27-16a2-4061-99f2-6596dc44af23.png)

Add image her getConnetionString

## Run Project 

Add the start project to ExchangeRate.
Inside the Package manager Console check that the Default project is Infrastructure.

Add the migration and  configure the database by following the documentation <br />
https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=vs

We can run the project by setting the startup project as multiple and starting the Web API without the debugging. 


We can run the project by adding the currency that for the conversion.
see all currency and currency code in documentation. <br />
https://fixer.io/symbols 



Console App

The Console App start to ask you for the base currency. 
Thereafter you can choice to look for a specific currency conversion or get the list of all conversions.

![console](https://user-images.githubusercontent.com/86916224/192825509-422ec2f5-c35a-452c-ab49-cf705c94eda3.png)



