---
title: "Cloud, fluently."
date: "2018-05-07"
---

https://twitter.com/iStarr/status/989877859777941510

So, I really dig the Azure Fluent SDK. It feels incredibly intuitive. Once you have familiarity with the lay of the land in terms of resources in Azure, then following on from examples of using the Fluent SDK looks as easy as using linq to get data access queries done.

It looks like the team behind it is ensuring the SDK stays up to date with Azure resources as they are released. Prior to being introduced to Azure Fluently (my name, lol), I was trying to find a way to create Azure Function applications on demand.  One of my [recent Stack Overflow](https://stackoverflow.com/questions/50021153/is-there-a-way-to-invoke-the-azure-cli-in-an-azure-function) questions was in that vein.

But then along came this SDK. Now, I could do something like this:

\[code language="csharp"\]

IAzure azure = GetAzure();

var newName = (fnNamePrefix + DateTime.Now.Ticks).Substring(0, 19);

var storageAccount = azure.StorageAccounts.List() .Where(x => x.Name.Equals(storageAccountName))?.First();

MemoryStream stream = CreateZip(indexJs, functionJson);

var functionUrlZip = UploadZip(storageAccount, newName, stream); stream.Position = 0; var websiteApp = azure.AppServices.FunctionApps.Define(newName) .WithRegion("East US") .WithExistingResourceGroup(resourceGroup) .WithExistingStorageAccount(storageAccount) .WithAppSetting("WEBSITE\_USE\_ZIP", functionUrlZip) .Create() ;

\[/code\]

Which lets me programmatically create an archive of the bits for a function (JSON), upload it and then, **create the actual function.** Notice, this function is powered by that experimental feature -> pointing to a zip file for your web app (WEBSITE\_USE\_ZIP).

https://twitter.com/iStarr/status/989109191104229381

I could have used this creation step to instead get the function's publish profile and then upload the files via FTP to the newly created app as well.

This versatile way of engaging with Azure Resources, from a creational/management perspective is really compelling and I'm looking forward to using it more in the future.

#TheFutureIsFluent
