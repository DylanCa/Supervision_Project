# Server Architecture & Administration Project

For a 3rd year IT engineering school project, we had to setup two **Active Directory** forests in order to create **Group Policies, Rules concerning Passwords or Wallpapers, or even Security issues.** 

Moreover, a **Supervision** setup has to be made, in order to be aware of the provided services' vitality. In order to do so, we used **[CENTREON](centreon.com)** for several reasons, such as the possibility to use a poller, the ease to create dashboards, to add new services or plugins, or even hosts, and we already worked with this server monitoring tool.

##### Organizational chart

![iSEC Group](https://i.imgur.com/Hx6GJ74.png "iSEC Group")

![iSEC Telecom](https://i.imgur.com/omxVeJt.png "iSEC Telecom")

### Project Presentation

##### Organisation Breakdown Structure

![OBS](https://i.imgur.com/MkRp0CB.png "OBS")

##### Project Breakdown Structure

![PBS](https://i.imgur.com/quJuOIK.png "PBS")

##### Work Breakdown Structure

![WBS](https://i.imgur.com/YsVTVaw.jpg "WBS")

##### GANTT

![GANTT](https://i.imgur.com/G7cm1KC.png "GANTT")

### Realisation

**Functionnalities and Services - Windows Server & Users :**

* DNS & DHCP services
* Shared folder across every user of a same group
* Shared folder across everyone
* "C:/Documents" transparently redirected to "//Server/%username%/Documents" in order to be able to get files from every computer connected to the server
* Custom desktop wallpaper acording to the user's workgroup
* Passwords resetting after 90 days, 8 characters minimum
* Account locked after 3 password mistakes ( Security reasons )
* Auto-run deactivated when an USB is plugged in
* 7Zip automatically deployed

**Functionnalities and Services - Supervision Centreon :**

* CPU load
* RAM
* Free disk space
* Internet traffic
* DNS / DHCP interruptions
* Logging every state change
* Dashboard easy to understand

![Composite Diagram](https://i.imgur.com/vUrQtuI.jpg "Composite Diagram")


| Used for        | Operating System           | Name  |
| ------------- |:-------------:| -----:|
| iSEC Group - Main Server     | Windows Server 2012 R2 | SRV-GROUP-Principal |
| iSEC Group - Replica Server      | Windows Server 2012 R2      |   SRV-GROUP-Replica |
| iSEC Telecom - Main Server | Windows Server 2012 R2      |    SRV-TELECOM-Principal |
| Supervision | CentOS - Centreon      |    SRV-CENTREON |

*Since uploading Virtual Machines is too big of an operation, only Snap
shots of them are available.*


#### Credits

- [Dylan Peltre](https://github.com/D-Peltre)
- [Romain Verhaeghe](https://github.com/romainver)
- [Cédric Montes](https://github.com/Cedric-M)
- [Dylan Cattelan](https://github.com/DylanCa)

[Exia.CESi 3rd Year](https://exia.cesi.fr/)
