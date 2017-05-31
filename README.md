# PTWS
####Persistent Time and Weather System####

PTWS is a script made for Exile that allows time and weather to persist through server restarts. It also has seasons defined by months that will change the temperature. 

#### Features
* Persistent time (year, month, day, hour, minute)
* Persistent weather
* Dynamic weather (thanks to code34's Real weather)
* Seasons that change the temperature
* Snow based on temperature and current overcast
* Time accleration
* 64bit compatibility.

#### To-do List
* ~~Add Persistent weather~~
* ~~Configure seasons based on months~~
* ~~~Make the seasons affect more than the temperature~~ <~ Not sure if im gonna do that
* Get a simple message out to players when body temperature drops below "?"
* Season change message or toast.. 
* Some kind of heavy storm with thunder or nuclear storm.
* Rework the configuration to include min/max value's for certain weather types/months.
* Add a little more debug information.. 
* **Open to suggestions...**

## Installation

#### extDB
1) Execute `PTWS-SQL.sql` in your mySQL viewer.

2) You should now have a ptws table.

3) For 32bit: Copy the contents of `PTWS.ini` into your `@ExileServer\extDB\sql_custom_v2\exile.ini` file at the bottom.
3) For 64bit: Copy the contents of `PTWS_x64.ini` into your `@extdb3\sql_custom\exile.ini` file at the bottom.

##### Server
1) Take either the PTWS.pbo or the file and put it in your `@ExileServer\addons`. Use the file if you want to configure the settings and pack it after you're done.

##### Mission
1) Copy `PTWS` from `Mission Files\mpmissions\Exile.Yourmap` into the root of your Exile.Yourmap folder.

2) Open your `config.cpp` in your mission folder and edit your `CfgExileCustomCode` and add a two new lines inside like this:
`ExileServer_system_weather_initialize = "PTWS\ExileServer_system_weather_initialize.sqf";`
`ExileClient_object_player_stats_updateTemperature = "PTWS\ExileClient_object_player_stats_updateTemperature.sqf";`
`ExileClient_system_snow_thread_update = "PTWS\ExileClient_system_snow_thread_update.sqf";`

#### You are done!

#### Credits go where credits due:
* **MajorXAcE** for the original work.
* **DirtySanchez** for the database fix and 64Bit compatibility. 
