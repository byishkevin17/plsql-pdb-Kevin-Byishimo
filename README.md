## Student ID: 28056
## Names: BYISHIMO Kevin

Introduction

This report presents the practical work completed on Oracle Database Creation, Deletion, and Oracle Enterprise Manager (OEM) configuration. The objective of the assignment was to create a pluggable database (PDB) that will be used for storing class work, demonstrate how to delete another PDB, and finally configure and access Oracle Enterprise Manager to monitor database performance. These tasks were designed to help understand how Oracle’s multitenant architecture operates and how database administration can be efficiently managed using OEM.


TASK 1: Create a New Pluggable Database (PDB)
🔹 Step-by-step (SQL*Plus or SQL Developer)

Connect to CDB (as SYSDBA)
sqlplus / as sysdba

Check existing PDBs
SHOW PDBS;
Create your PDB
![altext](screenshots/Screenshot%202025-10-06%20144701.png)
![altext](screenshots/Screenshot%202025-10-06%20144716.png)
Open the new PDB
ALTER PLUGGABLE DATABASE ke_pdb_28056 OPEN;
Save state
ALTER PLUGGABLE DATABASE ke_pdb_28056 SAVE STATE;
Verify
SHOW PDBS;

TASK 2: Create and Delete a PDB
🔹 Create another PDB (for deletion demo)
Open it
ALTER PLUGGABLE DATABASE ke_to_delete_pdb_28056 OPEN;
🔹 Delete it afterward
ALTER PLUGGABLE DATABASE ke_to_delete_pdb_28056 CLOSE IMMEDIATE;
DROP PLUGGABLE DATABASE ke_to_delete_pdb_28056 INCLUDING DATAFILES;
![altext](screenshots/Screenshot%202025-10-06%20153129.png)
![altext](screenshots/Screenshot%202025-10-06%20153249.png)

Before deletion (PDB visible in SHOW PDBS;)

TASK 3: Configure Oracle Enterprise Manager (OEM)
Access OEM in your browser
URL format:https://localhost:5500/em

Login using your username: sys

Take a screenshot of your OEM dashboard showing:
![altext](screenshots/Screenshot%202025-10-06%20144614.png)
![altext](screenshots/Screenshot%202025-10-06%20144546.png)


Status as Available / Open