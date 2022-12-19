---
title: Client's UI
---

The Client's UI was developed using React JS.

It has a main file called *"index.js"* that runs firstly the connection with our IDP (Identity Provider), keycloak. It verifies if the user logged has or not permissions to access this page. Only users with *admin* or *client* role has authorization to see this UI.

After this verification, the UI will render the app if the user has permissions, or will show a message warning about his lack of authorization.

The user has the possibility to see a list of his properties, cameras and alarms associated, and the intrusions verified. Beside this, it's also possible to activate or deactivate a camera or a alarm, and to delete them.  


![drawing](/img/clientsUI.png)