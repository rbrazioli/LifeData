# Getting SproWeight Data
Since (I don't really know) SproWeight does not offer anymore a data export functionality, unless you upgrade to a "pro" version.

After a few trial, using applications to access data on iPhone (or iPhone Backups) proven to be unseccesfull. Neither PhoneView, nor iPhone Backup Extractor have been able to locate and extract the data.

Therefore I've resorted to a more "brute force" approach:
1. using iTunes, I've created a not encripten backup on my Mac. It can be found in ˜/Library/Application Support/MobileSync/Backups/cf85a3a47a95d18bf56398ee579e9021ae630470
2. I've opened the file "Manifest.db" with DB Browser for SQLite and locate the SproWeight SQLite database using it
3. The table "t_record" contains all the collected data. I've copied and pasted the data in an Excel file. Trying to export in CSV format was generating some weird results, probably due to the formatting of the "note" column.

### Record ID### User ID### Date
Date as an integer, the number of days since 1-JAN-1970. Similar to Unix date format, but with days insetad of seconds. ### Mtime### Mweight
Morning weight measure, Integer, last two digits are decimal ones### Mfat
Morning body fat measure, Integer, last two digits are decimal ones### Etime### Eweight
Evening weight measure, Integer, last two digits are decimal ones### Efat
Evening body fat measure, Integer, last two digits are decimal ones### Temp
Temperature, Integer, last two digits are decimal ones### Note
Free form text### is_send### ext### version### Ttime