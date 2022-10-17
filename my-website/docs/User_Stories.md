## 1. In memory database
### Epic 
As a Sys Admin, I want the an in memory database so i can store the frames.

:::important
### US-1 HDM evaluate if human is in N consecutive frames.

#### Description
As a system administrator, I want the HDM in my system to get the frames from the Redis database and analyse them, so that it can detect if N consecutive frames have a human in it.

#### Acceptance Criteria
Given frames received from camera and stored in Redis database, When the HDM pulls N frames and analyses them. It then should be able to detect a human or not.

### Priority = High 
:::

:::important
### US-2 Add Redis to the Human detection module.


#### Description
As system administrator I want my system to order and keep consecutive frames in a in memory database (REDIS) so the HDM can properly function.

#### Acceptance Criteria
Given that the camera is always sending frames to the HDM, when the frames are received by the HDM they are automatically stored in the Redis database in consecutive order.

#### Priority = High 
:::



## 2. Client UI

:::important
### Epic



### US-1

#### Description
As a client, I want to be able to see a listing of all my cameras and sensors, so that I can know how many I have and where they are located.

#### Acceptance Criteria
Given a client's UI, when I enter the dashboard page, then I see a list of all my cameras and a list of all my sensors.

### Priority = High
:::



:::important
### US-2

#### Description
As a client, I want to be able to see a list of all intrusion events, so that I can be informed about my property intrusion history.

#### Acceptance Criteria
Given a client's UI, when I enter the dashboard page, then I see a list of all intrusion events.

### Priority = Medium
:::

:::important
### US-3

#### Description
As a client, I want to be able to update my cameras' and sensors' information, so that I can configure and manage them whenever I want.

#### Acceptance Criteria
Given a list of my cameras and a list of my sensors, when I select one and click on the configure button then I update their information.

### Priority = Medium
:::


:::important
### US-4

#### Description
As a client, I want to obtain data from my cameras and alarms, so that I can take some conclusions about the performance of my equipment.

#### Acceptance Criteria
Given a list of my cameras and a list of my sensors, when I select one and click on the data button then I obtain the data from that equipment.

### Priority = Low
:::


:::important
### US-5

#### Description
As a client, I want to manage how I will receive intrusion notifications so that I can be informed quickest as possible.

#### Acceptance Criteria
Given a list of possible intrusion notification ways, when I select one then I update my intrusion notifications receive method.

### Priority = Low
:::


:::important
### US-6

#### Description
As a client, I want to check all events triggered on my property, so that I can be informed about what happened.

#### Acceptance Criteria
Given a client's UI, when I enter the dashboard page then I see an intrusion events history.

### Priority = Medium
:::


## 3. Log monitoring with ELK Stack 

:::important 
### US-7

#### Description
As a System Admin I want docker file that can bluid the ELK stack automatically so that i have an efficient way of deploying the logs monitoring environment.

#### Acceptance Criteria
Given the docker file when I run it  then it should deploy the logs monitoring environment.

### Priority = Medium
:::