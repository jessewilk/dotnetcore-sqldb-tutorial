---
languages:
- csharp
- aspx-csharp
page_type: sample
description: "This is a sample application you can use to follow along w/ the Build a .NET Core and SQL Database web app in Azure Web Apps for Containers tutorial."
products:
- azure
- aspnet-core
- azure-app-service
---

# .NET Core MVC sample for Azure App Service

This is a sample application that you can use to follow along with the tutorial at 
[Build a .NET Core and SQL Database web app in Azure Web Apps for Containers](https://docs.microsoft.com/azure/app-service/containers/tutorial-dotnetcore-sqldb-app). 

Tutorial Link:
https://docs.microsoft.com/en-us/azure/app-service/app-service-web-tutorial-dotnetcore-sqldb

## License

See [LICENSE](LICENSE.md).

## Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
  
  Server=tcp:db1221.database.windows.net,1433;Database=coreDB;User ID=jwilkadmin;Password=R3l3ntl3ss;Encrypt=true;Connection Timeout=30;

  "https://jwilkadmin@dotnetsqlapplication.scm.azurewebsites.net/dotNetSqlApplication.git"


  az webapp config connection-string set --resource-group DotNetSqlApp --name dotNetSqlApplication --settings MyDbConnection="Server=tcp:db1221.database.windows.net,1433;Database=coreDB;User ID=jwilkadmin;Password=R3l3ntl3ss;Encrypt=true;Connection Timeout=30;" --connection-string-type SQLServer


  az webapp config appsettings set --name dotNetSqlApplication --resource-group DotNetSqlApp --settings ASPNETCORE_ENVIRONMENT="Production"
git remote add azure "https://jwilkadmin@dotnetsqlapplication.scm.azurewebsites.net/dotNetSqlApplication.git"

az webapp log config --name dotNetSqlApplication --resource-group DotNetSqlApp --application-logging true --level information

az webapp log tail --name dotNetSqlApplication --resource-group DotNetSqlApp