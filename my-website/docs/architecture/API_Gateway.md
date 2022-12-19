---
title: API Gateway
---

In this project, the API gateway used was Amazon API gateway.
We use the API gateway as a proxy to route all the API calls. The client does not access the microservices 
directly, but through the API gateway. Due to problems with Deploying the IDP (keycloak) on AWS, microservices that make use of the IDP such as the Site's management API, Client and Management UI are not routing through the API gateway seen as they're running locally. 
<img src="/img/aws_api_gw.png" width="200"/>