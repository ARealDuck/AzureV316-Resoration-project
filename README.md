# AzureV316 (Duck's Restoration Project) NOW DEPRECATED
AzureMS v316 KMS,

NOTE:

This repository is no longer being maintained as a better version ElectronMS https://github.com/Bratah123/ElectronMS Is much more up to date and contains more history of the AzureMS sources. 
I have forked that version for the fixes to continue this project. 
link here: https://github.com/ARealDuck/ElectronMS-Ducks-Azure-Resto-Project
From there I will be continuing and maintaining the project.
Thanks! -Duck

I will be working on fixing and restoring a bunch of stuff in the server and hopefully reboot it into a decent source for people to either use or I will use myself and build a server out of

Credits (growing list, if you have made anything please DM me on discord A_Duck#5385 with proof and you will be added)
- SoulGirlJP
- Dipi 
- Brandon
- Desc
- Kookiie


## Trello:
 - I will be using trello in order to keep on track with what is being worked on
  - The trello board can be found here. https://trello.com/b/ChfbGUdG/azurems-v316-restoration
---
## Features:
(Will add later once I figure out what the fuck im doing with this and learn the source)


## Related Features/Additions:
- In addition to the server source code repository, the Azure team also has other AzureMS-based tools.
  - ~**[Discord Bot](https://github.com/Bratah123/MapleDiscBot)**~  
      - ~Feature-rich Discord bot that the original v316 AzureMS used for majority of its server life~  
      - ~Easy to set-up~  
    - *Deprecated: Breaking API changes in the discord.js module*  
  - **[Lapis](https://github.com/TEAM-SPIRIT-Productions/Lapis)**  
    - Feature-rich Discord bot that attempts to be SUPER plug-n-play  
    - Lightweight and easy to set-up *(see [Wiki](https://github.com/TEAM-SPIRIT-Productions/Lapis/wiki/General-Flow))*  
    - Built on Lazuli (see below)!  
  - **[Lazuli](https://github.com/TEAM-SPIRIT-Productions/Lazuli)**  
    - A Python-based API for connecting to AzureMS-based servers.  
    - Easy to use; complete with [example code](https://github.com/TEAM-SPIRIT-Productions/Lazuli/wiki/Sample-Code-Fragments#loading-a-database)!  

---
## Quick Start Reference:  
### ***See our [Wiki](https://github.com/SoulGirlJP/AzureV316/wiki/Setup) for a more detailed guide (with screenshots)!***
1. `Clone` or `Fork` this repository
2. Setup the DB management system (i.e. MariaDB or MySQL Workbench)
    - By default the username may be set to `root` and the password left empty, with SSL disabled. Port should be set to `3306`.
3. Setup the DB administrion tool (i.e. HeidiSQL or MySQL Workbench)
    - Run either one of the SQL script files found in `AzureV316/sql/`
    - It should create a new schema named `kms_316`.
    - Note that this will cause errors if MySQL Workbench is running in safe mode. Follow the error message instructions to disable safe mode.
4. Turn **off** innodb strict mode.
    - This can be achieved by editing the `.ini` file in the install path of the DB management system, and requires a restart
5. Open the project in IntelliJ (or your IDE of choice), and allow the IDE to finish indexing (if applicable).
6. Configure project settings. (IntelliJ: File -> Project structure)
    - Set the project SDK to an appropriate JDK version (see above in tech specs)
    - Ensure that all the required libraries (in `AzureV316/AzureMS/lib/`) are imported.
7. Ensure that the details in **Step 2** are reflected in the source code.
    1. Hit `Shift` twice to bring up the search menu.
    2. Select the first option.
    3. Check the username and password strings in `MYSQL.java` are correct.
8. Navigate to `Azure_316\AzureV316\AzureMS\src\launcher` to reach `Start.java`.
    - Try `Build` and `Run` this file. (HeidiSQL or WAMP should be running in background)
    - Note that the first build/run may take quite a while!
