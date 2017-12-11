# Server Architecture & Administration Project

For a 3rd year IT engineering school project, we had to setup two **Active Directory** forests in order to create **Group Policies, Rules concerning Passwords or Wallpapers, or even Security issues.** 

Moreover, a **Supervision** setup has to be made, in order to be aware of the provided services' vitality. In order to do so, we used **[CENTREON](centreon.com)**

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

| Used for        | Operating System           | Name  |
| ------------- |:-------------:| -----:|
| iSEC Group - Main Server     | Windows Server 2012 R2 | SRV-GROUP-Principal |
| iSEC Group - Replica Server      | Windows Server 2012 R2      |   SRV-GROUP-Replica |
| iSEC Telecom - Main Server | Windows Server 2012 R2      |    SRV-TELECOM-Principal |
| Supervision | CentOS - Centreon      |    SRV-CENTREON |

![Composite Diagram](https://i.imgur.com/vUrQtuI.jpg "Composite Diagram")

### Conclusion
