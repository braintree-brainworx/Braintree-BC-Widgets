# Setting up pages

BC Widgets allows you to build personalised pages which resemble a standard Microsoft Dynamics 365 Business Central role centre. You can use these to
- simplify the user experience by removing the clutter of unneeded functions
- build personalised 'role centres' without the need to rely on a developer
- build dashboards to display key performance indicators.

The app comes with a few prebuilt pages, giving access to each major module of Microsoft Dynamics 365 Business Central.

This section provides instructions on how to build a page to be displayed as a role centre, or to run a widget page.

## Create a new page
From the role centre, select 'Page Setups':

![alt text](image-21.png)

Or search for Widget Setup List. The pages already defined will be displayed:

![alt text](image-22.png)

Click on New. The Page Setup card will open:

![alt text](image-23.png)

Create the page header as follows:

|**Field** |**Value**|
|---|---|
|Setup ID|Supply an integer number |
|Page Name |Enter a text description|
|Template Code|Select an option from the dropdown|

Reply Yes to the dialog.

![alt text](image-24.png)

Reply Yes or No to the next dialog. (Replying YES will cause the system to create some placeholder activities in the subpage.)

![alt text](image-25.png)

The system will copy the formatting options - colours, sizes, fonts etc - from the template. From here, you can edit as required.

You can edit the remaining fields as follows:

![alt text](image-26.png)

|**Field** |**Value**|
|---|---|
|Banner Background Style |Click on ... to open the style helper |
|Banner Foreground Style |Click on ... to open the style helper|
|Banner Height|Enter the height in pixels for the page banner. This should be a smallish number such as 30|
|Application Title|Enter a text description |
|Main Control Background Style |The formatting style for the background on which buttons will be located. Click on... to open the Style Helper|
|Main Control Width|Height in points of the main control on which the buttons will be located|
|Main Control Height|Width in points of the main control on which the buttons will be located|
|Button Height|Height in points of the buttons on the page |
|Button Width|Width in points of the buttons on the page |
|Info Area Height|Height in points of the information area of each button|

## Adding tasks to the page
For each button or section heading that you want to display on the page, create a line on the 'Activity Setup' section of the page. These can be grouped into sections. There are a few ways to do this:

- Create Widgets: sets up a group of buttons based on a selected table and field.
- Create Ageing Widgets: sets up a group of buttons based on age, for analysing data based on dates
- Manual Entry

### Adding a section heading