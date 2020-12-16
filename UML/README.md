# NagBot
SD&amp;D project

Some diagrams to show how the implementation works so far. From an implementation standpoint here's how the different parts/python files interact (arrows showing flow if information not inheritance):
![](overall.png)

Inside database is the main class structure that stores all the data for the app, the other files contain classes with methods that perform functions based on this data. The class structure for database.py looks something like this (with the exceptions that can be thrown by each class):
![](database_exceptions.png)

Removing the exceptions cleans up the diagram a bit and you can see the generic storage structure:
![](database.png)

You can ignore the pickle.load box, that's just generated b/c we use pickle to store and load the 2 instance variables of Database.

The NagBot (UI) file contains classes for each Page (large boxes), which are all used in the NagBotApp through the ScreenManager Kivy object. All UI elements as well as the ScreenManager and App are also classes inside Kivy (shown as smaller boxes):
![](nagbot_kivy.png)

Removing the Kivy internals leaves us with the pages which are all stored and used in the NagBotApp:
![](nagbot.png)

## UI Flowchart (UI may differ a bit since we are still in beta)
![](images/GUI_Flowchart.svg)