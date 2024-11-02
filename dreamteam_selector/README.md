# DREAM TEAM SELECTOR
PyQt5 User Interface Class for Dream Team Selector
This code defines a PyQt5 GUI (graphical user interface) application for selecting a dream sports team, likely for fantasy sports or a similar game. The main UI is structured around selecting and organizing team members within various roles, displaying points, and handling various menu actions.
1. Main Window Setup (setupUi)
The Ui_MainWindow class is the core UI component, with setupUi() setting up the layout, widgets, and basic properties for the main window.

Main Window:
Set up the window with a custom position (100,10) and a specific background color (rgb(192, 200, 104)).
Size policy is set to adjust based on the content but generally fills the allocated space.
Widgets and Layouts
Central Widget: Holds the primary content of the application.
Layout Hierarchy:
Vertical and Horizontal Layouts:
The primary layout, verticalLayout, organizes content vertically.
Nested layouts (horizontalLayout, horizontalLayout_5, etc.) manage specific groups of widgets.
Labels, Input Fields, and Spacers
Labels (label_4, label_6, etc.): These labels show category names for team roles (Batsmen, Bowlers, All-Rounders, Wicketkeepers) in bold font.
Input Fields (e1, e2, etc.): These are QLineEdit widgets that display numbers or other information relevant to each role (disabled by default).
Spacers: Used to control spacing within the layout to keep widgets aligned.
2. Role Selection (Radio Buttons)
A QGroupBox is created with four radio buttons (rb1, rb2, rb3, and rb4), allowing users to select player roles:

Player Categories:
"BAT" for Batsmen
"BOWL" for Bowlers
"AR" for All-Rounders
"WK" for Wicketkeepers
Each radio button connects to the ctg function (likely categorizing players by role).
3. Player Lists (QListWidget)
Available Players (list1):

Displays available players for selection in the chosen category.
Styling: Text color (rgb(0, 0, 127)) and bold font.
Connects to removelist1() method on double-click, possibly to remove players from this list.
Selected Players (list2):

Displays selected players within the team.
Similar styling to list1 and connects to removelist2() for removal functionality.
4. Point Management
Points Display and Update:

Available Points Button (btn1): Displays "Available Points : 1000" as a button that updates the user on points left for team selection.
Points Used Button (btn2): Updates based on points spent on selected players.
Attribute Variables:

Four attributes manage the count of each player type: bat, bwl, ar, and wk.
avl (available points, initially 1000) and used (points used) track points allocation.
 5. Menu Bar
The menu includes File and Help options, each with specific actions:

File Menu:
New Team: Starts a new team creation.
Open Team: Opens a saved team.
Save Team: Saves the current team configuration.
Quit: Exits the application.
Function Connection: The menu connects to menufunction, which likely defines specific behaviors for each action.
Help Menu:
Rules: Provides game rules.
Instructions: Offers usage instructions.
6. Context Menu and Event Connections
Context Menu: The window is set to use a custom context menu.
Event Handling:
Custom Slots:
ctg: Connected to radio buttons, categorizes selected players.
removelist1, removelist2: Allow removing items from list1 and list2 on double-click.
menufunction: Handles menu actions based on File menu selections.
7. retranslateUi() Method
This method sets text for each widget, making it easier to update language strings or change widget titles.

Examples:
Window Title: "Dream Team Selector"
Buttons and Labels: Clear names for buttons and categories to enhance usability.
Summary of Key Features
Team Selection Interface: User selects players by role, with each role having its own point allocation.
Points Management: Displays available and used points to help users manage their team within budget.
Menu Options: Facilitates team saving, opening, and quitting, as well as accessing rules and instructions.
Event-Driven Layout: Uses Qt slots and signals for user interaction, e.g., radio button toggling and list item selection.
