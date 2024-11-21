# ADS-B-Database-Query
Query and analyze local unique ADS-B contacts database (SQLite), updated by remote TAR1090 source session.

Install sqlite3 package, first! 

Currently running in Raspberry Pi 4B for the DB maintenance, while for ADS-B (feeding adsb.fi service) remote receiver I'm using Raspberry Pi 3B, all in my LAN. 

The DB file will be automatically created the first time db.py is run, in /home/pi. 

Files callsign_patterns.txt and hex_prefixes.txt contain known military partial callsigns and Hex codes, and these are used by the script in the section "Show Military Flights" ("Isola voli militari").

Remember to modify the main python script and update the DB with the help of cron, for example:

* * * * * /usr/bin/python3 /home/pi/db.py

Here's you are current main menu, working on it! (Currently in IT language):

       Flight Tracker
------------------------------
1. Ricerca Specifica
2. Filtra per Data
3. Voli a Terra
4. Voli con Squawk d'Emergenza
5. Isola Voli Militari
6. Classifiche
7. Ricerca Online (adsb.fi)
8. Statistiche Database
9. Info Hardware
0. Esci

