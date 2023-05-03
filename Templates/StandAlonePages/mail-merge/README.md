Objectives
Understand what the solution does.
Understand what the Apps Script services do within the solution.
Set up the script.
Run the script.
About this solution
If you have various types of content you'd like to offer your audience, you can let users choose what content they receive from you with Google Forms. This solution lets users select the topics they're interested in, then automatically emails them their chosen content.

Demo of sending content with Google Forms and Gmail

How it works
The script installs an event-driven trigger that runs each time a user submits a form. With each form submission, the script creates and sends an email from a Google Docs template. The email includes the user's name and the content they selected. The content you offer can be of any type as long as it’s referenced by a URL.

Apps Script services
This solution uses the following services:

Script service–Installs the event-driven trigger that fires whenever someone submits the form.
Document service–Opens the Docs template that the script uses to create the email.
Mail service–Creates and sends the email with the user’s name and content selection.
Spreadsheet service–Adds a confirmation to the Form responses sheet after the script sends the email.
Prerequisites
To use this sample, you need the following prerequisites:

A Google Account (Google Workspace accounts might require administrator approval).
A web browser with access to the internet.
Send curated content

Set up the script

	1. Make a copy;
Use our curated content spreadsheet, the Apps Script project for this solution is attached to this folder.
Make a copy

	2. In your copied spreadsheet, click Extensions > Apps Script.

	3. In the function dropdown, select installTrigger.

	4. Click Run.

	5. When prompted, authorize the script. If the OAuth consent screen displays the warning, This app isn't verified, continue by selecting Advanced > Go to {Project Name} (unsafe).

Important: If you run installTrigger more than once, the script creates multiple triggers that each send an email when a user submits the form. To delete extra triggers and avoid duplicate emails, click Triggers alarm. Right-click on each extra trigger and click Delete trigger.

Run the script
	1. Switch back to the spreadsheet and click Tools > Manage form > Go to live form.
	2. Fill out the form and click Submit.
	3. Check your email for an email with links to the content you selected.


Review the code ==> Templates/StandAlonePages/mail-merge/mail-merge.js


