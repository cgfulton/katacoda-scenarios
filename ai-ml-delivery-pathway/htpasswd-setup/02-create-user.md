## Create User

Generated __htpasswd__ file

`htpasswd -c -B -b users.htpasswd developer 'developer'`{{execute}}

## Upload htpasswd file

**Access Openshift Console** 

As cluster admin navigate to __Cluster Settings__.

`Administration -> Cluster Settings`

![admin-menu](assets/admin-menu-cluster-settings.png)

**Manage OAuth Configurations**

From __Cluster Settings__
* Select the __Global Configuration__ tab
* Search for __oauth__
* Click the __OAuth__ link   

![cluster-settings](assets/cluster-settings-page.png)

**Select Identity Provider**

* Scroll to the bottom of the oAuth page
* Click __Add__ under __Identity Providers__
* Select HTPasswd

![oauth-page](assets/oauth-page-cluster-settings.png)

**Add HTPassword Identity Provider**

On the __Add Identity Provider__ page 
* Click Browse
* Select the generated __htpasswd__ file
* Click Add

**Login With HTPasswd**
* Logout out of the Openshift Console
* From the Openshift login menu select __htpasswd__ to login

![ocp-login-menu](assets/ocp-login-menu.png)

