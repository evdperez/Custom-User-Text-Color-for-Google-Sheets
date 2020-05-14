Function:

Allows each user editing a Google Sheets document to have their own custom color. Whenever they make an edit, the text color of the cell will be automatically changed to their color by the program. I have seen similar programs on Stack Exchange, but none of them worked, so I made this.  

Requirements:

All users must have emails from the same domain/organization. Due to onEdit's privacy restrictions, the script must be deployed as an add-on in order to function. The add-on can be published internally if all users are from the same domain/organization and avoid the review process for G Suite Apps.

Installation:

In your web browser, navigate to the Apps Script Dashboard: https://script.google.com/home
Create a new project. Give it a name like Color Change Script.
Copy and paste the code into the project. Change the emails to match those of the users on your domain who will be editing the document. Change the hex codes to the hex codes for the desired color for each user. You can get hex codes for a partiular color by clicking the text color icon and selecting custom color. The hex code for the color you select is displayed in the dialogue box.

In a new tab, go to the Google Developer Console: https://console.developers.google.com/
Create a new project. Give it a name like Color Change Add-on
After creating the project, go to IAM & Admin >> Settings to view the project number. 

Return to the script editor. Go to Resources >> Cloud Platform project...
Enter the project number to associate the script with the project. 
Go to File >> Manage versions... 
Type a description and click Save new version.
Go to File >> Project properties.
Copy the script ID. You will need this later. 

Return to the Google Developer Console. 
Under APIs & Services >> OAuth consent screen, select Internal application type. Add email and profile scopes. Enter the other neccessary information and save changes. 
Under APIs & Services >> Dashboard, check for the G Suite Marketplace SDK and Google Sheets API. If these are not already enabled, search for and enable them. 
After enabling, select G Suite Marketplace SDK >> Configuration.
Enter the necessary information. You can use some random images. No one will see them. 
Click the checkbox for Sheets add-on extension. Paste the script ID you copied into the Sheets add-on Project Script ID box. Enter the version number of the version you created. (Most likely 1)
Set visibility to My Domain and save changes. 

Congratulations! The add-on should now be available for installation on all of your domain's Google spreadsheets. In can be installed by going to Add-ons >> Get add-ons and searching for the the name you gave it. 





