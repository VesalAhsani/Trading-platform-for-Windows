# Trading_Platform
This platform is just a prototype and many strategies will be added soon! 👍

DO NOT USE IT FOR TRADING AS IT IS.

## For Windows:
This repo discusses the creation of a trading robot application. It covers the advantages and disadvantages of desktop and web applications for this purpose, as well as the key features that should be included in a trading application. The organization and structure of the code for the application is also discussed, including the requirement for connectors for specific exchanges and the use of a code editor. Additionally, the repo covers how to obtain API keys for Binance and Bitmex exchanges and how to use the tkinter library in Python to create a GUI for the application. The use of websocket-client library to create websocket connections, adding data models to improve the code for a Binance connector, adding error handling and reconnection capabilities to a Binance connector, creating a connector for the Bitmex API, and adding various methods to the Bitmex connector to retrieve and manipulate data, place and cancel orders, and handle errors are described. Finally, the main topics of threading in Python, including the threading module, locks, and condition variables, are discussed.

To summarize, the repo addressed the implementation of a trading platform with a strategy component that allows users to input and manage their trading strategies. The component includes two strategies: a TechnicalStrategy and a BreakoutStrategy. The component uses connectors for Binance and Bitmex exchanges to retrieve a list of symbols for an OptionMenu. The switch_strategy method activates or deactivates a strategy and verifies that all mandatory parameters have been input by the user. When a new strategy is selected, the component initializes a new Strategy object based on the selected strategy and retrieves historical data for the strategy. The new Strategy object is then added to the appropriate connector, either Binance or Bitmex. The TechnicalStrategy and BreakoutStrategy include check_signal methods that return an integer indicating a long, short, or no signal based on the price and volume of the current and previous candles. The system also includes a method for checking for signals and opening trades, as well as a method for monitoring the performance of the check_signal method. The open_position method is responsible for sending a market order to buy or sell based on the signal and the trade size, which is calculated as a percentage of the account balance. The system also allows for the option of passing the bid or ask price to the open_position method in order to trade at a specific price.

![Uploading Capture 2.PNG…]()


To open the trading platform outside of Pycharm on Windows, you need to create a new file with the .bat file extension. In the file, you can use the command to navigate to the directory where the start.bat file is located and the command that Pycharm uses to start the Python file. You should copy it. so it knows where your program is.

SQLite is a popular choice for a database management system, especially for smaller projects or applications where a full-fledged database management system like MySQL or PostgreSQL may be overkill. One of the benefits of using SQLite is that it is self-contained and does not require a separate server process to be running, which makes it easy to set up and use.

To create a connection to an SQLite database in Python, you can use the sqlite3 module, which is part of the Python Standard Library. Here is an example of how you can create a connection to an SQLite database and execute a simple SELECT statement to retrieve data from a table:

```
import sqlite3

# Connect to the database
conn = sqlite3.connect('database.db')

# Create a cursor
cursor = conn.cursor()

# Execute a SELECT statement
cursor.execute('SELECT * FROM table_name')

# Fetch all rows from the SELECT statement
rows = cursor.fetchall()

# Iterate over the rows and print the column values
for row in rows:
    print(row['column_name'])

# Close the connection
conn.close()
```
Using the sqlite3.Row class as you mentioned allows you to access the data in each row as a dictionary, which can be more convenient than accessing the data as a tuple.

As for the DB Browser for SQLite, it is a graphical tool that allows you to view, create, and edit SQLite databases. It is a useful tool for exploring and working with SQLite databases, and can be a helpful tool when you are working with SQLite in your Python projects.



#### Required libraries:
pandas==1.5.2

python_dateutil==2.8.2

requests==2.28.1

websocket_client==1.4.2
