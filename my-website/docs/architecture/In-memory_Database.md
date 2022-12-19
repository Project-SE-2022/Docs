---
title: In Memory DataBase
---

## 1. In Memory DataBase

#### Technology
The technology chosen for the in memory database is Redis, an in memory data structure store.
<img src="/img/Redis.png" width="300"/>

### Functionality
The *Human_Detection_Module* class instatiates a dictionary called "database" and this dictionary is sent as a parameter to the *Human_Detection_Worker* class when called. This dictionary will contain all the ordered frames sent from the camera.
In the *Human_Detection_Worker* class the Redis database is instantiated on port **6379**, `self.redisDB = redis.Redis(host= 'localhost', port= '6379')`.
We flush database in case its carrying data from an old run using `self.redisDB.flushdb()`.

On the *create_database_entry* funtion we get the updateded stored dictionary form the in memory databse, `self.database = self.redisDB.hgetall("redisDB")` decode it and equal it to the current dictionary. we than use this dictionary to add new values and after that it is stored back in the in memory database as a hashmap, using Redis's `hmset` funtion. 

```

        self.database = {key.decode('utf-8'):value.decode('utf-8') for key,value in self.database.items()}
        self.database[num_humans_key] = num_humans
        self.database[timestamp_key] = ts
        # Save the updated dictionary into Redis In-Memory Database
        self.redisDB.hmset("redisDB",self.database)

```

Lastly the in memory database is applied to the *alarm_if_needed* function, this is done by getting the stored dictionary from the in memory database (`hgetall` function) and decoding it (The result is a normal dictionary). The *alarm_if_needed* function then analises the frames in the dictionary.

