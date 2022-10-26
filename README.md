# Discord RPC

This library is an easy to use client for Discord Rich Presence.



# Features

  - Customise your discord activity with ease
  - Optimised well to save on resources



### Installation

```sh
pip install ShivBox
```


### Example
```py
from RPC import presence
import time

client_id = '1283743838' #Your application ID# 
RPC = presence.Client(client_id)
RPC.start() #Starts the connection to discord's pipe#

current_time = time.time()


activity = {
    "state": "Some random state here",
    "details": "Some details here",
    "timestamps": {
        "start": int(current_time)
    },
    "assets": {
        "large_text": "Large text here", 
        "large_image": "Large image ID here",
        "small_text": "Small text here",
        "small_image": "Small image ID here"
    }
}

while True:
    RPC.update(activity)
    time.sleep(20) #You can only make changes to the RPC every 15 seconds#
```
