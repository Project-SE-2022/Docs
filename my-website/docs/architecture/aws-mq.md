---
title: AWS MQ (RabbitMQ)  
---

## Steps to Create a Broker

1. Go to **Amazon MQ web console**

2. click on **Get started** button.

3. Select broker engine:

	* Broker engine types: **RabbitMQ**

4. Select deployment mode:

	* Deployment mode: **Single-instance broker**

5. Configure settings:
	* **Details**: 
		* Broker name: **RabbitBroker**
		* Broker instance type: **mq.t3.micro**

	* **RabbitMQ access**:
		* Username: **broker**
		* Password: **rabbitmqbroker**

	* **RabbitMQ access**:
		* Broker engine version: **3.9.16 (latest)**
		* Network and security (Access type): **Public access**
		* Network and security (VPC and subnets): **Select existing VPC and subnet(s)**
			* VPC: **Seccom-vpc**
			* Subnet(s): **Seccom-subnet-public1-eu-west-3a**

		* Maintenance: Enable automatic minor version upgrades





