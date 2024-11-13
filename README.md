# My approach

Standard repo - service layer pattern for development. I started with the models as I knew it would be required to adjust the model for Plate with status after reading through all the user stories. I also added a model for PromoDetails. 

My repo layer is fairly simple, the service layer is then more complex. Ideally, if I had more time I would have split this up further - a PromoService class, a ReservationStatus class and a Filtering/Sorting class. All would have been implemented in the same way. 

I tried to get to all the user stories, skipped the Sale one as it required more Frontend work which is more time consuming for me. I would have approached this in the same way as the others, a sold button next to the item. If I had implemented this I would have changed status to be an enum with Availebl, Reserved and Sold as the options but the time limit made this too long. 




# Monolithic Application Template

If you have found your way here, you have more than likely been asked by Regtransfers Ltd to complete a Coding Exercise as a part of your interview process. 

It’s great that you are eager to join our team. To make your life a bit easier we have provided you with a basic boilerplate project. 

This is the Monolithic style application, you can find a Microservices based boilerplate here: https://github.com/Regtransfers/RTCodingExercise.Microservices

## Forking
Please fork this project into your own github repository, this repository has been locked and cannot be committed to.

## MVC Application
ASP.NET Core 6.0.1 Web App (Model-View-Controller) with a seeded database.

- ApplicationDbContext inside the data folder is your Entity Framework Code First DatabaseContext.
- CodeFirst Migrations are enabled, any changes you make to the database can be implemented with 
  `Add-Migration` or `dotnet ef migrations add`
- ApplicationDbContextFactory enables these migrations to work
- ApplicationDbContextSeed seeds the DbContext with sample data, if you wish you can update this with more
- WebHostExtention in the extensions folder enables code first migrations to be run when the project starts
- Models contains the Plate model for the DbContext

For ease of use, Startup.cs has been created and initiated in the Program.cs.

## Database
The database requires that you have SQL Server Express LocalDb installed (usually installed with VisualStudio), if you don't you can grab it from here
https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/sql-server-express-localdb?view=sql-server-ver15

The database should automatically create and seed itself thanks to some fancy boilerplate code.
Database: RTCodingExercise
Connection: (localdb)\mssqllocaldb

you can connect to it via VisualStudio by adding it under the ServerExplorer DataConnections referencing `(localdb)\mssqllocaldb` as the server and choosing RTCodingExercise from the Database dropdown list, connecting with Windows Authentication or the same way through SQLServerManagementStudio

## Unit Tests

An xUnit test project has also been added, and the MVC project has been referenced.
you are not restricted to using xUnit if you would prefer to use nUnit feel free to replace the test project with one of your choosing.

## Submitting
Please contact your Recruitment agency or us directly with a link to your forked repository.

Good Luck.
