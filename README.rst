========
sportinf
========
Sportinf is a convenient python module to get data of sport teams, players, leagues and events. You can know
information from many sports, such as: football, hockey, basketball, tennis, golf, athletics and so on. Sportinf gets
data from TheSportsDB API (<https://www.thesportsdb.com>).

============
Installation
============
Python >= 3.5

pip install sportinf

=====
Usage
=====
First things first we have to import class called SportInfo:

    from sportinf import SportInfo

After this we make an object of this class:

    info = SportInfo(option="name of the option", name_of_parameter="value of the parameter")

First parameter is option. This parameter shows what information you want to get. Here are all options that available in
module and their description:

- Information about team - shows an information about team. Requires name of the team.
- Information about player - returns an information about player. Requires first and last name of the player.
- Information about event - shows an information about event. Requires name of the event.
- List all sports - returns list of all sports that available in this module. Requires nothing.
- List all leagues - returns list of all leagues from any sport and country that available in this module. Requires nothing.
- List all countries - returns list of all countries that available in this module. Requires nothing.
- List all Seasons in a League - returns list of all seasons from any league that available in this module. Requires name of the league.
- List all Teams in a League - returns list of all teams from any league that available in this module. Requires name of the league.
- League Details - shows a detailed information about any league. Requires name of the league.
- Player Honours - shows all honours that player got through his career. Requires first and last name of the player.
- Player Former Teams - returns all former teams of player. Requires first and last name of the player.
- Player Contracts - shows an information about contract by player. Requires first and last name of the player.
- Lookup Table by League and Season - shows a table from any league and season. Requires name of the league and season.
- Lookup Equipment by Team - returns an information about every equipment by team. Requires name of the team.
- Last 15 Events by League - shows an information about 15 last events from any league. Requires name of the league.

When you created an object of SportInfo class, you have to write only option and
those parameters that are written in the description for every option. For example, you need to an information about player Lionel Messi.
You have to write next:

    info = SportInfo(option="Information about player", player_name="Lionel Messi")

You get a result as python dictionary. In this dictionary keys are parameters. For every option they are different.
List of all parameters for every option you can find in parameters.txt.
So, if you want to know an information for player Lionel Messi, you will result like in result_Lionel_Messi.txt.

Sometimes happens situation when you get more than one result. For instance, when you want to know information about team called Arsenal, you will get data about six teams,
such as: Arsenal London, Arsenal U21, Arsenal WFC, Arsenal Kyiv, Arsenal Tula and Arsenal Sarandi.
In this case sportinf will return dictionary, where as a key will be name of the team, league, event etc.
As a value will be dictionary with parameters and values of this one.

=============
Configuration
=============
There is nothing to configure

=======
Credits
=======

Contributors
------------
- Alexander Maudza <alex.maudza@gmail.com>

Author & Maintainer
-------------------
This module is maintained by Alexander Maudza
