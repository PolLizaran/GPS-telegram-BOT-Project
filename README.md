# iGo
iGo is a program implemented in a bot in Telegram that offers the fastest path
from the user's location to a requested destination, all by driving in the city
of Barcelona.

## Introduction
The project is divided into two main parts:

* The `bot.py` module is used to interact with the users through Telegram by
responding to a defined group of functions, which are mainly focused on offering
a visual representation of the most optimal path from a place to another.

* The `igo.py` module consists of the functions that manage different graphs of
the city to compute the fastest path, taking into consideration up-to-date
information about how congested are the roads in Barcelona.

## Bot in Telegram
- The `TrafficAdvisor` bot, which can also be identified by the username `@DrivingToBot`,
  supports the following functionalities:

  - Being able to start an interaction with the bot by writing the command `/start`.

  - Receiving information about each possible command that works in the bot with
  `/help`.

  - Asking for information about the developers of the project by using the command
  `/author`.

  - Showing the current location of the user by using the function `/where`.

  - Obtaining the fastest path to the destination that has been chosen by the user,
  which is displayed in a map, when using `/go DESTINATION`.

  - Introducing a chosen current location, which can be different from the user's real
  current position, with `/pos`.

### Interact with the bot
Interacting with the bot is very easy, as it is possible to do it with any device that supports
Telegram. However, to be able to use it, the program `bot.py` must be executing.

## Computing the fastest path
- The `igo.py` module uses NetworkX, graphs from OSMnx, and information provided by the
Ajuntament de Barcelona to:

  - Download information from a CSV file by creating a list with the data.

  - Load a graph to the memory and be able to get it.

  - Know if a graph has been already created or not.

  - Print an image graph of the city of Barcelona, which can contain only the
  edges that correspond to the main roads or all the roads.

  - Compute the travel time in an edge knowing the `speed`, `length`, and the state of
the congestion, which is uploaded as a new attribute to a graph by the name of `itime`.

  - Obtain the shortest path from two different locations.

  - Print a map that highlights a determined path.

### Usage of the module `igo`
- The examples that would be

```{python}

```

## Requirements
To be able to execute the different modules, it is necessary to install a set of packages that are
in the `requirements.txt`, which includes the versions used in the project. This can be done by
using the command:

> pip install -r requirements.txt


## Authors
Andrea Bellmunt Fuentes (https://github.com/PolLizaran/) and Pol Lizaran Campano (https://github.com/PolLizaran/)

Data Science and Engineering, UPC, 2021
