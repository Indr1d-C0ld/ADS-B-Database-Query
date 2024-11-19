# ADS-B-Database-Query
Query and analyze local unique ADS-B contacts database (SQLite), updated by remote TAR1090 source session.

Install sqlite3 package, first! 

Currently running in Raspberry Pi 4B for the DB maintenance, while for ADS-B (feeding adsb.fi service) remote receiving station I'm using Raspberry Pi 3B, all in my LAN. 

Remember to update the DB with the help of cron, for example:

* * * * * /usr/bin/python3 /home/pi/db.py

Here's you are current main menu, working on it! (Currently in IT language):

   Interrogazioni Database
-----------------------------
1. Ricerca Specifica (HEX o Callsign)
2. Filtra per Data
3. Mostra Record e Classifiche
4. Mostra voli con Squawk di Emergenza
5. Isola voli militari
6. Mostra voli Ground (altezza = 'ground')
7. Esci

