
<!---
Version: 1.0 
-->
# Exercise 1: Creating an Azure Service Bus Namespace
## INTRODUCTION MESSAGE
In this exercise, you will:  
  
Create a Service Bus namespace by using the Portal.  
The main tasks for this exercise are as follows:  
  
Create the Service Bus namespace by using the Portal.
## COMPLETION MESSAGE
Results: After completing this exercise, you will have created a Service Bus namespace and queue by using the Portal.
### Login as Student
Login as Student with a password of Pa$$w0rd.

#### :bulb: KNOWLEDGE
You can use the Commands menu and choose Ctrl\+Alt\+Delete then click Student and enter Pa$$w0rd and press Enter. You can also use the Command menu and choose Paste/Paste Password instead of typing the password manually.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666673.jpg
>* ShowAutomatically = No





### On the Start screen, click Internet Explorer
On the Start screen, click the Internet Explorer tile

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666674.jpg
>* ShowAutomatically = No





### Go to the new Azure Portal
Go to https://portal.azure.com. Enter the email address of your Microsoft account associated with your Azure subscription. Then enter the password for your Microsoft account. Check Keep me signed in. Click Sign In.

#### :bulb: KNOWLEDGE
Before starting this lab, you must have completed the lab in Module 2. All work in this lab is done within vm20532 created in the lab in Module 2. Start and Connect via Azure Portal.  
  
If you see a pop-up for Skype for Business click Don't Enable.  
  
Ignore any updates to OneDrive

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666675.jpg
>* ShowAutomatically = No



#### :calling: COMMAND
```TypeText
https://portal.azure.com
```


### Browse Virtual Machines
In the navigation pane on the left side of the Azure Portal, click Virtual Machines.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666676.jpg
>* ShowAutomatically = No





### Start the VM
Click the vm20532 VM that was created in the lab in Module 2 for development. In the Overview blade, if the VM is stopped, click Start and wait for the VM to start up. This may take a few minutes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666677.jpg
>* ShowAutomatically = No





### Connect to the VM via RDP
When the vm20532 VM has started, click Connect.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666678.jpg
>* ShowAutomatically = No





### Allow pop-ups
If presented with a message box that shows a pop-up has been blocked, select Options for this site and choose Always Allow. Then click Connect again.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672700.jpg





### Click Open
When presented with the RDP download popup at the bottom of the screen, click Open.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672701.jpg





### In the Remote Desktop Connection dialog box:
In the Remote Desktop Connection dialog box, perform the following steps:  
a. Click Don’t ask me again for connections to this computer to prevent this dialog box from displaying again.  
b. Click Connect.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666679.jpg
>* ShowAutomatically = No





### In the Windows Security dialog box:
In the Windows Security dialog box, perform the following steps:  
a. For the User name dialog box, provide the value, Student.  
b. For the Password dialog box, provide the value, AzurePa$$w0rd.  
c. Click OK.

#### :bulb: KNOWLEDGE
Note: If you computer is on a domain, you may need to add a backslash before the username to "escape" the domain.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666680.jpg
>* ShowAutomatically = No





### In the Remote Desktop Connection dialog box:
In the Remote Desktop Connection dialog box, perform the following steps:  
a. Verify if the Remote certificate name matches the name of your virtual machine.  
b. Click Don’t ask me again for connections to this computer to prevent this dialog box from displaying again.  
c. Click Yes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666681.jpg
>* ShowAutomatically = No





### Close Server Manager
If you have just re-started the VM, Server Manager will start automatically after 30 seconds. If it starts, you can close it.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666682.jpg
>* ShowAutomatically = No





### On the Start screen, open Internet Explorer
On the Start screen, click the Internet Explorer tile.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666683.jpg
>* ShowAutomatically = No





### Sign in to the Azure Portal
Sign in to the Azure Portal at https://portal.azure.com.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666684.jpg
>* ShowAutomatically = No



#### :calling: COMMAND
```TypeText
https://portal.azure.com
```


### New Service Bus
Click the +New button in the top left of the portal and type Service, press Enter then select Service Bus from the list.




### Create Service Bus
At the bottom of the screen, click the Create button.




### In the Create a Namespace dialog box:
In the Create a Namespace dialog box, perform the following steps:  
a. In the Namespace Name box, type sb20532\[Your Name\].  
b. In the Pricing Tier, select the Standard option.  
c. In the Resource Group section, click Use existing then select the pre-existing resource group used previously from the dropdown.
d. In the Region list, select the region that is closest to your location. 
e. Click the Create button to create your namespace.

#### :bulb: KNOWLEDGE
Note: It takes approximately 1-2 minutes to create your Service Bus namespace instance.


### Click the new Service Bus namespace:
Click the More Services option in the portal menu, then type Service Bus, and select Service Bus. In the list of Service Bus namespaces, click the namespace that you just created.




### At the bottom of the screen, click Connection Info
Under Settings, click the Shared Access Policies blade, then click RootManageSharedAccessKey.



### Copy the connection string
Click the Copy button next to the Connection string-Primary Key. If prompted, click Allow Access. Close the Policy blade.




### Paste in Notepad
Click the Start button, then type Notepad and paste the Endpoint into Notepad and leave it open for later in the lab.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672707.jpg





### Under Entities, click the Queues blade
In the Service Bus blade, under Entities, click the Queues blade.



### At the top, click +Queue
At the top, click +Queue 



### In the Create Queue blade:
In the Create Queue blade, perform the following steps:  
a. In the Name box, type signin.  
b. Leave all fields as their default values.  
c. Click the Create button to create the new queue.



### Verify Queue created
Verify Queue created by clicking on the queue name (signin) to view the queue blade.





# Exercise 2: Using Azure Queue Storage for Document Generation
## INTRODUCTION MESSAGE
In this exercise you will:  
  
Create queue messages by using Storage queues.  
Consume queue messages from Storage queues.  
  
The main tasks for this exercise are as follows:  
Update worker role to consume requests from the queue.  
Update administration application to add requests to the queue.  
Create a Storage account instance.  
Generate the test data.  
Debug and verify the application.
## COMPLETION MESSAGE
Results: After completing this exercise, you will have created and consumed messages from Storage queues.
### Open Contoso.Events solution in Visual Studio
On the taskbar, click the File Explorer icon. In the Libraries window, go to Allfiles \)F):\\Mod08\\Labfiles\\Starter\\Contoso.Events, and then double-click Contoso.Events.sln.

#### :bulb: KNOWLEDGE
Note that Known file extensions \)such as .sln) may be hidden. See screenshot.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666747.jpg
>* ShowAutomatically = No





### Open the TableStorageQueueHelper.cs file
In the Solution Explorer pane, expand the Roles folder. Expand the Contoso.Events.Worker project. Double-click the TableStorageQueueHelper.cs file.

#### :bulb: KNOWLEDGE
Ignore Intellisense errors

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666748.jpg





### Add a using statement for System.Configuration:
Add a using statement for the System.Configuration namespace to the top of the file:  
using System.Configuration;

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666749.jpg



#### :calling: COMMAND
```TypeText
using System.Configuration;
```


### Store the StorageAccount property
At the end of the TableStorageQueueHelper constructor and before the closing brace, store the StorageAccount property from the base class in a CloudStorageAccount variable:  
CloudStorageAccount storageAccount = base.StorageAccount;

#### :bulb: KNOWLEDGE
Ignore Intellisense errors

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666750.jpg



#### :calling: COMMAND
```TypeText
CloudStorageAccount storageAccount = base.StorageAccount;
```


### Invoke the CreateCloudQueueClient method:
Invoke the CreateCloudQueueClient method and assign the result to the \_queueClient variable:  
\_queueClient = storageAccount.CreateCloudQueueClient\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666751.jpg



#### :calling: COMMAND
```TypeText
_queueClient = storageAccount.CreateCloudQueueClient();
```


### Invoke static AppSettings property:
Invoke the static ConfigurationManager.AppSettings property and assign the result to the \_signInQueueName variable:  
\_signInQueueName = ConfigurationManager.AppSettings\["SignInQueueName"\];

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666752.jpg



#### :calling: COMMAND
```TypeText
_signInQueueName = ConfigurationManager.AppSettings["SignInQueueName"];
```


### Find the method with the following signature:
In the TableStorageQueueHelper class, find the method with the following signature:  
public IQueueMessage<CloudQueueMessage> Receive\))

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666753.jpg





### Remove the single line of code in the class:
Remove the single line of code in the class:  
return new TableStorageQueueMessage\)null);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666754.jpg





### Create a new instance of the CloudQueue class
At the end of the Receive method and before the closing brace, create a new instance of the CloudQueue class by calling the GetQueueReference method of the CloudQueueClient variable by using the string name of the queue, as shown in the following code:  
CloudQueue queue = \_queueClient.GetQueueReference\)\_signInQueueName);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666755.jpg



#### :calling: COMMAND
```TypeText
CloudQueue queue = _queueClient.GetQueueReference(_signInQueueName);
```


### Invoke the CreateIfNotExists method:
Invoke the CreateIfNotExists method to ensure that the queue exists.  
queue.CreateIfNotExists\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666756.jpg



#### :calling: COMMAND
```TypeText
queue.CreateIfNotExists();
```


### Invoke the GetMessage method:
At the end of the Receive method and before the closing brace, invoke the GetMessage method of the CloudQueue class and store the result in a CloudQueueMessage variable, as shown in the following code:  
CloudQueueMessage message = queue.GetMessage\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666757.jpg



#### :calling: COMMAND
```TypeText
CloudQueueMessage message = queue.GetMessage();
```


### Pass the CloudQueueMessage variable:
Pass the CloudQueueMessage variable into the constructor of the TableStorageQueueMessage class and return the result:  
return new TableStorageQueueMessage\)message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666758.jpg



#### :calling: COMMAND
```TypeText
return new TableStorageQueueMessage(message);
```


### Create a new instance of the CloudQueue class
At the end of the CompleteMessage method and before the closing brace, create a new instance of the CloudQueue class by calling the GetQueueReference method of the CloudQueueClient variable by using the string name of the queue, as shown in the following code:  
CloudQueue queue = \_queueClient.GetQueueReference\)\_signInQueueName);

#### :bulb: KNOWLEDGE
Ignore Intellisense errors

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666759.jpg



#### :calling: COMMAND
```TypeText
CloudQueue queue = _queueClient.GetQueueReference(_signInQueueName);
```


### Invoke the CreateIfNotExists method:
Invoke the CreateIfNotExists method to ensure that the queue exists:  
queue.CreateIfNotExists\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666760.jpg



#### :calling: COMMAND
```TypeText
queue.CreateIfNotExists();
```


### Invoke the DeleteMessage method:
At the end of the CompleteMessage method and before the closing brace, invoke the DeleteMessage method by using the CloudQueueMessage variable as the parameter, as shown in the following code:  
queue.DeleteMessage\)message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666761.jpg



#### :calling: COMMAND
```TypeText
queue.DeleteMessage(message);
```


### Open the SignInSheetViewModel.cs file.
In the Solution Explorer pane, expand the Shared folder. Expand the Contoso.Events.ViewModels project. Double-click the SignInSheetViewModel.cs file.

#### :bulb: KNOWLEDGE
Ignore Intellisense errors

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666762.jpg





### Create a CloudStorageAccount instance:
At the beginning of the GenerateSignInSheetTableStorage method and after the opening brace, create a CloudStorageAccount instance by using the static CloudStorageAccount. Parse method and the table storage connection string, as shown in the following code:  
CloudStorageAccount storageAccount = CloudStorageAccount.Parse\)tableStorageConnectionString);

#### :bulb: KNOWLEDGE
Ignore Intellisense errors

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666763.jpg



#### :calling: COMMAND
```TypeText
CloudStorageAccount storageAccount = CloudStorageAccount.Parse(tableStorageConnectionString);
```


### Create a new instance of CloudQueueClient class:
Create a new instance of the CloudQueueClient class by using the CreateCloudQueueClient method of the CloudStorageAccount variable:  
CloudQueueClient queueClient = storageAccount.CreateCloudQueueClient\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666764.jpg



#### :calling: COMMAND
```TypeText
CloudQueueClient queueClient = storageAccount.CreateCloudQueueClient();
```


### Create a new instance of the CloudQueue class:
After the above mentioned code, create a new instance of the CloudQueue class by invoking the GetQueueReference method of the CloudQueueClient variable by using the queue name string variable, as shown in the following code.:  
CloudQueue queue = queueClient.GetQueueReference\)signInQueueName);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666765.jpg



#### :calling: COMMAND
```TypeText
CloudQueue queue = queueClient.GetQueueReference(signInQueueName);
```


### Invoke the CreateIfNotExists method:
Invoke the CreateIfNotExists method of the CloudQueue class to ensure that the queue exists:  
queue.CreateIfNotExists\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666766.jpg



#### :calling: COMMAND
```TypeText
queue.CreateIfNotExists();
```


### Create a new instance of CloudQueueMessage:
After the above mentioned code, create a new instance of the CloudQueueMessage class by passing in the string message into the constructor:  
CloudQueueMessage queueMessage = new CloudQueueMessage\)message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666767.jpg



#### :calling: COMMAND
```TypeText
CloudQueueMessage queueMessage = new CloudQueueMessage(message);
```


### Invoke the AddMessage method of CloudQueue:
Invoke the AddMessage method of the CloudQueue variable by using the CloudQueueMessage as the parameter:  
queue.AddMessage\)queueMessage);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666768.jpg



#### :calling: COMMAND
```TypeText
queue.AddMessage(queueMessage);
```


### Switch to the new Azure Portal in IE:
Switch to the new Azure Portal by clicking the tab in Internet Explorer, or by entering https://portal.azure.com

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666769.jpg





### Add a new Storage Account:
In the Browse blade that displays, click Storage accounts. In the Storage accounts blade that displays, view your list of storage account instances. At the top of the Storage accounts blade, click the Add button.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666770.jpg





### In the Create storage account blade:
In the Create storage account blade that displays, perform the following steps:  
a. In the Name box, provide a globally unique value.  
b. In the Deployment model section, ensure that the Resource manager option is selected.  
c. In the Account kind list, ensure that the General purpose option is selected.  
d. In the Performance section, ensure that the Standard option is selected.  
e. Click on the Replication list and select the Locally Redundant \)LRS) option.  
f. In the Location list, select the region closest to your current location.  
g. In the Resource group section, select the Use existing option, locate the dropdown listbox and select the pre-existing resource group used previously.  
h. Leave other options to default
i. Ensure that the Pin to dashboard option is selected.  
j. Click Create.




### Verify new Storage account:
Once the Storage account instance is created, the blade for the new instance should open automatically.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666772.jpg





### View Access Keys
In the Storage account blade, record the name of your storage account. In the Access keys blade, locate a key that you wish to use.  
           

#### :bulb: KNOWLEDGE
Note: you can use any of the keys listed for this lab.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666773.jpg



### View connection string option:
For the access key you selected, click the Copy button to the right of the connection string field. If prompted, click Allow Access.



### Paste to Notepad
Open Notepad and paste the access key to below the Endpoint copied earlier.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672708.jpg





### Switch to Visual Studio, open app.config file
Switch to Visual Studio. In the Solution Explorer pane, expand the Shared solution folder. Expand the Contoso.Events.Data.Generation project. Locate and open the app.config file in the project.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666776.jpg





### Locate the following configuration setting:
Within the app.config file, locate the following configuration setting:  
 <add key="StorageConnectionString" value="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666777.jpg





### Update the connection string setting
Update the setting by replacing the value of the value attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666778.jpg





### Verify Connection String
Verify Connection String

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666779.jpg





### Start Debug, and then click Start New Instance:
In the Solution Explorer pane, right-click the Contoso.Events.Data.Generation project, point to Debug, and then click Start New Instance. Wait for debugging to complete \)when the console window closes).

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666780.jpg





### Verify Output
Verify Output by clicking the Output tab and checking for success and code 0

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666781.jpg





### Select the Multiple startup projects option:
In the Solution Explorer pane, right-click the Contoso.Events solution, and then click Properties. Navigate to the Startup Project section located under the Common Properties header. In the Startup Project section, locate and select the Multiple startup projects option.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666782.jpg





### Within the Multiple startup projects table:
Within the Multiple startup projects table, perform the following actions:  
a. Locate the Contoso.Events.Web entry and change it's Action from None to Start.  
b. Locate the Contoso.Events.Management entry and change it's Action from None to Start.  
c. Locate the Contoso.Events.Worker entry and change it's Action from None to Start.  
d. Ensure that all the remaining projects have their Action set to None.  
Click the OK button to close the Property dialog.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666783.jpg





### Open the web.config file in the project:
In the Solution Explorer pane, expand the Administration solution folder. Expand the Contoso.Events.Management project. Locate and open the web.config file in the project.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666784.jpg





### Locate the following configuration setting:
Within the web.config file, locate the following configuration setting:  
 <add key="Microsoft.WindowsAzure.Storage.ConnectionString" value="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666785.jpg





### Update the connection string setting
Update the setting by replacing the value of the value attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666786.jpg





### Open the web.config file in the project:
In the Solution Explorer pane, expand the Roles solution folder. Expand the Contoso.Events.Web project. Locate and open the web.config file in the project.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666787.jpg





### Locate the following configuration setting:
Within the web.config file, locate the following configuration setting:  
 <add key="Microsoft.WindowsAzure.Storage.ConnectionString" value="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666788.jpg





### Update connection string
Update the setting by replacing the value of the value attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666789.jpg





### Open the app.config file in the project:
In the Solution Explorer pane, expand the Contoso.Events.Worker project. Locate and open the app.config file in the project.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666790.jpg





### Locate the following configuration setting:
Within the app.config file, locate the following configuration setting:  
 <add name="AzureWebJobsStorage" connectionString="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666791.jpg





### Update the  connection string setting
Update the setting by replacing the value of the connectionString attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666792.jpg





### Locate the following configuration setting:
Within the app.config file, locate the following configuration setting:  
 <add name="AzureWebJobsDashboard" connectionString="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666793.jpg





### Update the connection string setting
Update the setting by replacing the value of the connectionString attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666794.jpg





### Locate the following configuration setting:
Within the app.config file, locate the following configuration setting:  
 <add key="StorageConnectionString" value="UseDevelopmentStorage=true" />

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666795.jpg





### Update the connection string setting:
Update the setting by replacing the value of the value attribute \)currently UseDevelopmentStorage=true) with your Storage Account's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666796.jpg





### Locate the AzureWebJobsServiceBus setting:
Within the app.config file, locate the following configuration setting:  
 <add name="AzureWebJobsServiceBus" connectionString="Endpoint=sb://\[yourServiceNamespace\].servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=\[yourKey\]"/>

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666797.jpg











### Copy the connection string for the Service Bus
Copy the connection string for the Service Bus SAS by switching to Notepad, highlighting the connection string that begins with Endpoint=sb:// and copying it to the clipboard by using Ctrl\+C.




### Switch back to Visual Studio
Switch back to Visual Studio by clicking the icon in the task bar

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666801.jpg





### Update the Service Bus's connection string:
Update the setting by pasting the value of the connectionString attribute \)currently Endpoint=sb://\[yourServiceNamespace\].servicebus.windows.net/;SharedAccessKeyName=RootManageSharedAccessKey;SharedAccessKey=\[yourKey\]) with your Service Bus's connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666802.jpg





### On the Debug menu, click Start Debugging.
On the Debug menu, click Start Debugging.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666803.jpg





### View Contoso Events web site
View Contoso Events web site

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666804.jpg





### Switch back to Visual Studio, open Functions.cs
On the desktop, click the Contoso.Events – Microsoft Visual Studio window. \)Debug is still running). Click the View menu and select the Solution Explorer option. In the Solution Explorer pane, expand the Roles folder. Expand the Contoso.Events.Worker project. Double-click the Functions.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666805.jpg





### Insert Breakpoint:
Locate the ProcessQueueMessage method. Locate the target line of code:   
HandleMessage\)message);  
Right-click the target line of code, point to Breakpoint, and click Insert Breakpoint.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666806.jpg





### Verify Breakpoint set:
Verify that the Breakpoint was set.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666807.jpg





### Switch back to Contoso Events Administration:
On the desktop, click the Home - Contoso.Events.Administration browser window. On the home page of the Contoso Events Administration web application, click the Go to Events button to go to the list of events.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666808.jpg





### Click Sign-In Sheet for any event in the list.
Click Sign-In Sheet for any event in the list.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666809.jpg





### View Sign-In Document Generation in Progress:
View the sign-in page which notifies you that the sign-in sheet is being generated with the following message: Sign-In Document Generation in Progress. Wait for one minute for the worker role to receive the queue message.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666810.jpg





### Switch back to Visual Studio to see breakpoint:
Verify that the application temporarily pauses execution at the breakpoint.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666811.jpg





### On Debug menu, select Continue (F5):
On the Debug menu, select Continue \)F5) resume execution of the application

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666812.jpg





### Wait one minute, and then refresh sign-in page:
Wait for one minute, and then refresh the sign-in sheet page.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666813.jpg





### Click Sign-In Sheet to download the sign-in sheet
Click Sign-In Sheet to download the sign-in sheet from the server. Click Open.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666814.jpg





### View Sign-in sheet in WordPad
View the sign-in sheet in WordPad. Close WordPad when done.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666815.jpg





### Close the Internet Explorer application
Close the Internet Explorer application to end the Debug session

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666816.jpg






# Exercise 3: Using Service Bus Queues for Document Generation
## INTRODUCTION MESSAGE
In this exercise, you will:  
  
Create queue messages by using Service Bus queues.  
Consume queue messages from Service Bus queues.  
  
The main tasks for this exercise are as follows:  
Update worker role to consume requests from the queue.  
Update administration application to add requests to the queue.  
Debug and verify the application.
## COMPLETION MESSAGE
Results: After completing this exercise, you will have created and consumed messages from Service Bus Queues
### In Visual Studio, open the app.config file:
In Visual Studio, in the Solution Explorer pane, expand the Contoso.Events.Worker project. Double-click the app.config file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666696.jpg
>* ShowAutomatically = No





### Locate Microsoft.ServiceBus.ConnectionString:
Locate the Setting element with the name Microsoft.ServiceBus.ConnectionString.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666704.jpg


### Copy the connection string for the Service Bus
Copy the connection string for the Service Bus SAS by switching to Notepad, highlighting the connection string that begins with Endpoint=sb:// and copying it to the clipboard by using Ctrl\+C.




### Update Microsoft.ServiceBus.ConnectionString
Back in Visual Studio, update the Setting element with the name Microsoft.ServiceBus.ConnectionString. Replace the value with your previously recorded connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666706.jpg





### Open the ServiceBusQueueHelper.cs file:
In the Solution Explorer pane, expand the Roles folder. Expand the Contoso.Events.Worker project. Double-click the ServiceBusQueueHelper.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666707.jpg





### Add a using statement for the System.Configuration
Add a using statement for the System.Configuration namespace to the top of the file:  
using System.Configuration;

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666708.jpg



#### :calling: COMMAND
```TypeText
using System.Configuration;
```


### Store the Microsoft.ServiceBus.ConnectionString:
At the end of the ServiceBusQueueHelper constructor and before the closing brace, store the Microsoft.ServiceBus.ConnectionString setting value from your configuration in a string variable, as shown in the following code:  
string serviceBusConnectionString = ConfigurationManager.AppSettings\["Microsoft.ServiceBus.ConnectionString"\];

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666709.jpg



#### :calling: COMMAND
```TypeText
string serviceBusConnectionString = ConfigurationManager.AppSettings ["Microsoft.ServiceBus.ConnectionString"];
```


### Store the queue name in a string variable:
Store the queue name in a string variable.  
string signInQueueName = ConfigurationManager.AppSettings\["SignInQueueName"\];

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666710.jpg



#### :calling: COMMAND
```TypeText
string signInQueueName = ConfigurationManager.AppSettings["SignInQueueName"];
```


### Assign the Connection String to _client variable:
Invoke the static QueueClient.CreateFromConnectionString method using the queue name and connection string as parameters, and assign the result to the \_client variable, as shown in the following code:  
\_client = QueueClient.CreateFromConnectionString\)serviceBusConnectionString, signInQueueName);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666711.jpg



#### :calling: COMMAND
```TypeText
_client = QueueClient.CreateFromConnectionString(serviceBusConnectionString, signInQueueName);
```


### Find the method with the following signature:
In the ServiceBusQueueHelper class, find the method with the following signature:  
public IQueueMessage<BrokeredMessage> Receive\))

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666712.jpg





### Remove the single line of code in the class:
Remove the single line of code in the class:  
return new ServiceBusQueueMessage\)null);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666713.jpg





### Create a new instance of the CloudQueue class:
At the end of the Receive method and before the closing brace, create a new instance of the CloudQueue class by calling the GetQueueReference method of the CloudQueueClient variable using the string name of the queue, as shown in the following code:  
BrokeredMessage message = \_client.Receive\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666714.jpg



#### :calling: COMMAND
```TypeText
BrokeredMessage message = _client.Receive();
```


### Invoke the CreateIfNotExists method:
Invoke the CreateIfNotExists method to ensure that the queue exists  
return new ServiceBusQueueMessage\)message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666715.jpg



#### :calling: COMMAND
```TypeText
return new ServiceBusQueueMessage(message);
```


### Invoke the Complete method
At the end of the CompleteMessage method and before the closing brace, invoke the Complete method on the message parameter, as shown in the following code:  
message.Complete\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666716.jpg



#### :calling: COMMAND
```TypeText
message.Complete();
```


### Invoke the Abandon method:
At the end of the AbandonMessage method and before the closing brace, invoke the Abandon method on the message parameter, as shown below:  
message.Abandon\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666717.jpg



#### :calling: COMMAND
```TypeText
message.Abandon();
```


### Save All
Click trhe Save All button on the toolbar

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666721.jpg





### Open Package Manager Console:
On the View menu, point to Other Windows, and then click Package Manager Console.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666718.jpg





### Select Contoso.Events.Worker as default
a. In the Package Manager Console pane, in the Default Project list, select Contoso.Events.Worker.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666719.jpg





### In the Package Manager Console text area:
In the Package Manager Console text area, place the cursor after the text PM, and then type the following command then press Enter:  
Install-Package Microsoft.Azure.WebJobs.ServiceBus -Version 1.1.2

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/624636.jpg



#### :calling: COMMAND
```TypeText
Install-Package Microsoft.Azure.WebJobs.ServiceBus -Version 1.1.2
```


### If prompted to reload, click Yes
If prompted to reload file, click Yes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672709.jpg





### Open the Functions.cs file:
In the Solution Explorer pane, expand the Roles folder. Expand the Contoso.Events.Worker project. Double-click the Functions.cs file.

#### :bulb: KNOWLEDGE
You can Auto Hide the Package Manager Console window by pushing the push-pull pin on the window

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666722.jpg





### Locate the ProcessQueueMessage method:
Locate the ProcessQueueMessage method.  
 public static void ProcessQueueMessage\)\[QueueTrigger\)"signin")\] QueueMessage message, TextWriter log)

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666723.jpg





### Update the ProcessQueueMessage method:
Update the ProcessQueueMessage method by changing the parameter attribute of type QueueTrigger to type ServiceBusTrigger.  
 public static void ProcessQueueMessage\)\[ServiceBusTrigger\)"signin")\] QueueMessage message, TextWriter log)

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666724.jpg





### Open the Program.cs file:
In the Solution Explorer pane, expand the Roles folder. Expand the Contoso.Events.Worker project. Double-click the Program.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666725.jpg





### Create a new instance of JobHostConfiguration:
At the beginning of the Main method and after the opening brace, create a new instance of the JobHostConfiguration class as shown below:  
JobHostConfiguration config = new JobHostConfiguration\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666726.jpg



#### :calling: COMMAND
```TypeText
JobHostConfiguration config = new JobHostConfiguration();
```


### Enable the Service Bus extension:
After the previous line of code, enable the Service Bus extension as shown below:  
config.UseServiceBus\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666727.jpg



#### :calling: COMMAND
```TypeText
config.UseServiceBus();
```


### Locate the initialization of the JobHost instance
After the previous line of code, locate the initialization of the JobHost instance as shown below:  
var host = new JobHost\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666728.jpg





### Replace the line of code:
Replace the line of code with the following line of code that updates the initialization of the JobHost instance by passing in the JobHostConfiguration as a constructor parameter:  
var host = new JobHost\)config);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666729.jpg



#### :calling: COMMAND
```TypeText
var host = new JobHost(config);
```


### Open the Web.config file:
In the Solution Explorer pane, expand the Administration folder and then expand the Contoso.Events.Management project. Double-click the Web.config file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666730.jpg





### Locate Microsoft.ServiceBus.ConnectionString
Locate the appSettings element. Locate the add element with the key Microsoft.ServiceBus.ConnectionString.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666731.jpg





### Update Microsoft.ServiceBus.ConnectionString
Update the add element with the key Microsoft.ServiceBus.ConnectionString. Replace the value with your previously recorded connection string.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666732.jpg





### Open the SignInSheetViewModel.cs file:
In the Solution Explorer pane, expand the Shared folder. Expand the Contoso.Events.ViewModels project. Double-click the SignInSheetViewModel.cs file

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666733.jpg





### In the constructor, locate the following line:
In the constructor, locate the following line of code:  
GenerateSignInSheetTableStorage\)context, eventItem, messageString);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666734.jpg





### Replace the above line of code with the following:
Replace the above line of code with the following line of code:  
GenerateSignInSheetServiceBus\)context, eventItem, message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666735.jpg



#### :calling: COMMAND
```TypeText
GenerateSignInSheetServiceBus(context, eventItem, message);
```


### Create a QueueClient instance:
At the beginning of the GenerateSignInSheetServiceBus method and after the opening brace, create a QueueClient instance by using the connection string, as shown in the following code:  
QueueClient client = QueueClient.CreateFromConnectionString\)serviceBusConnectionString, signInQueueName);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666736.jpg



#### :calling: COMMAND
```TypeText
QueueClient client = QueueClient.CreateFromConnectionString(serviceBusConnectionString, signInQueueName);
```


### Create a new instance of the BrokeredMessage class
After the above code, create a new instance of the BrokeredMessage class by passing in the QueueMessage message into the constructor, as shown in the following code:  
BrokeredMessage queueMessage = new BrokeredMessage\)message);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666737.jpg



#### :calling: COMMAND
```TypeText
BrokeredMessage queueMessage = new BrokeredMessage(message);
```


### Invoke the Send method of QueueClient:
Invoke the Send method of the QueueClient variable by using the BrokeredMessage as the parameter:  
client.Send\)queueMessage);

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666738.jpg



#### :calling: COMMAND
```TypeText
client.Send(queueMessage);
```


### On the Debug menu, click Start Debugging.
On the Debug menu, click Start Debugging. Note that two web apps start in separate instances of Internet Exlorer: Upcoming Events and Events Administration

#### :bulb: KNOWLEDGE
If you get an error on UseServiceBus\)) method:  
  
Then uninstall Package Management Console via PMC console:  \)in the Default Project list, select Contoso.Events.Worker)  
UnInstall-Package Microsoft.Azure.WebJobs.ServiceBus -Version 1.1.2  
  
Then try install again: \)in the Default Project list, select Contoso.Events.Worker)  
Install-Package Microsoft.Azure.WebJobs.ServiceBus -Version 1.1.2  
  
  


#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666739.jpg





### On Contoso Events Administration web site:
Switch to the home page for the Contoso Events Administration web application, then click the Go to Events button to view the list of events.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666740.jpg





### Click Sign-In Sheet button for any event in list:
Click the Sign-In Sheet button for any event in the list. \)Choose a different event from before)

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666741.jpg





### If Debug stops at breakpoint:
If Debug stops at breakpoint, right-click on breakpoint and choose Delete Breakpoint. Then choose Continue \)F5) on Tool bar to resume execution of the application

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666742.jpg





### View the sign-in page and wait:
View the sign-in page which notifies you that the sign-in sheet is being generated with the message:  
Sign-In Document Generation in Progress.  
Wait for one minute for the worker role to receive the queue message.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666743.jpg





### Wait for one minute, and then refresh the sign-in
Wait for one minute, and then refresh the sign-in sheet page

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666744.jpg





### Click Sign-In Sheet to download the sign-in:
Click Sign-In Sheet to download the sign-in sheet from the server. Click Open to view sign-in sheet in WordPad.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666745.jpg





### View sign-in sheet in WordPad
View sign-in sheet in WordPad. Close WordPad.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666746.jpg





### Close Internet Explorer
Close Internet Explorer





### Close Visual Studio 2015
Close Visual Studio 2015





### Close File Explorer
Close File Explorer





### Close RDP session
Close RDP session and click OK to disconnect

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666700.jpg
>* ShowAutomatically = No





### Stop VM to save billing charges
If you are stopping labs for the day, on the vm2032 Overview page in the Azure Portal, click Stop to stop billing charges until you start labs again. If prompted, click Yes to stop the VM. Close Internet Explorer 

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666701.jpg
>* ShowAutomatically = No






