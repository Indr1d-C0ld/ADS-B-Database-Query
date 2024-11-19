# ADS-B-Database-Query
Query and analyze local unique ADS-B contacts database (SQLite), updated by remote TAR1090 source session.

Install sqlite3 package, first! 

Currently running in Raspberry Pi 4B for the DB maintenance, while for ADS-B (feeding adsb.fi service) remote receiving station I'm using Raspberry Pi 3B, all in my LAN. 

The DB file will be automatically created the first time db.py is run, in /home/pi. 

Remember to modify the main python script and update the DB with the help of cron, for example:

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

Output example:

hex      callsign  altitude  speed  squawk  seen  last_updated              
-------  --------  --------  -----  ------  ----  --------------------------
346644   VOE7XT    7975                     57.3  2024-11-18 00:04:01.864414
4d2003   AIZ338    36025     479.8  0451    2.8   2024-11-18 00:09:01.837687
4246a2   AZG1223   41000                    57.8  2024-11-18 00:19:02.340736
a89872   LXJ653    47000            2367    47.9  2024-11-18 00:26:02.268990
4d2300   RYR656L                            57    2024-11-18 00:39:01.610035
02012b   MAC523    37000     456.4  7351    45.3  2024-11-18 00:45:01.702569
710112   SVA020    35000            1145    49.8  2024-11-18 00:48:01.713686
71c081   KAL922    34500     493    1155    10.5  2024-11-18 00:54:01.431272
738056   ELY392              476.4          38.4  2024-11-18 00:56:02.219543
040047   ETH575                             54.2  2024-11-18 01:18:01.972548
~7365b8                                     20.5  2024-11-18 01:19:01.671894
4bb868   PGT1742   36000     473.5  1143    7.1   2024-11-18 01:20:02.189509
471f83   WMT498    36000                    57.3  2024-11-18 01:58:02.380722
~9b618b                                     24    2024-11-18 02:00:01.659048


