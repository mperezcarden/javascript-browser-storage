# javascript-browser-storage
Communication with Azure Storage using Javascript / Browser

# Links
* [Quickstart: Manage blobs with JavaScript v12 SDK in a browser](https://docs.microsoft.com/en-us/azure/storage/blobs/quickstart-blobs-javascript-browser)

# Prerequisites

* An Azure account with an active subscription
* An Azure Storage account.
* Node.js
* Microsoft Visual Studio Code
* A Visual Studio Code extension for browser debugging, such as:
  * Debugger for Microsoft Edge
  * Debugger for Chrome
  * Debugger for Firefox

# Available JavaScript Classes

* BlobServiceClient: The BlobServiceClient class allows you to manipulate Azure Storage resources and blob containers.
* ContainerClient: The ContainerClient class allows you to manipulate Azure Storage containers and their blobs.
* BlockBlobClient: The BlockBlobClient class allows you to manipulate Azure Storage blobs.

# Steps

# 1. Check Prerequisites

## Nodejs

```
node --version
```

You can install this one in windows with  [Chocolatey](https://chocolatey.org/)
Nodejs: ``choco install nodejs``

More information here: https://nodejs.org/en/download/

# 2. Create a CORS rule

Go to your storage account and search the blade "Resource sharing (CORS)".
More information here: [Create a CORS rule](https://docs.microsoft.com/en-us/azure/storage/blobs/quickstart-blobs-javascript-browser#create-a-cors-rule)

Note: Ensure any settings you use in production expose the minimum amount of access necessary to your storage account to maintain secure access.

# 3. Create a shared access signature

1. In the Azure portal, select your storage account.
2. Navigate to the Security + networking section and select Shared access signature.
3. Scroll down and click the Generate SAS and connection string button.
4. Scroll down further and locate the Blob service SAS URL field
5. Click the Copy to clipboard button at the far-right end of the Blob service SAS URL field.
6. Save the copied URL somewhere for use in an upcoming step.
   
Note: for this example, I have created a SAS with all allowed resource types and permissions.
But take into consideration that you should arrange that according to your requirements.
Make sure you copy the Connection String information, SAS token and Blob service SAS URL to a secure location ``Do not include that information in your code``

# 4. Add the Azure Blob Storage client Library

```
npm init -y
```