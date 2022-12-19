---
title: Identity Provider (IDP)
---

This module is delivered by Keycloak. On keycloak we create the user's acounts and atribute them the roles associated. 

To manage the roles, we follow an RBAC (Role Based Access Control) protocol. The system only recognizes to roles, *admin* or *client*. Giving the *admin* users permissions to access all the UI developed, Client's UI and Management Web UI, and the *client* users only acces to the Client's UI. 

<img src="/img/keycloak.png" width="250"/>