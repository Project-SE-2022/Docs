---
title: Management Web UI
---

The Management Web UI, like the Client's UI, was developed using React JS.

It has a main file called *"index.js"* that runs firstly the connection with our IDP (Identity Provider), keycloak. It verifies if the user logged has or not permissions to access this page. Only users with *admin* role has authorization to see this UI.

After this verification, the UI will render the app if the user has permissions, or will show a message warning about his lack of authorization.

The admin is able to see all properties being monitored, the intrusions that took place, a list of each property cameras and sensors, and all data regarding the platform’s clients. Basically, this UI is used to manage the entire platform

(screenshot of the Management Web UI two pages)
