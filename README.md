# puppy

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

Puppy is a self-driven system of the little car. It was came up with by [KITTCAMP](http://www.kittcamp.com/), self-driven car school,  and aimed to become a stable and powerful self-driven system.

Welcome to join us ^_^

# Usage
You need to follow the steps below to perform it. 
### Step 1: set static IP of raspiberry wifi connection
As an example, it was set default to 192.168.3.111
+ open dhcpcd.conf
```
sudo vim /etc/dhcpcd.conf
```
+ add config at the end of dhcpcd.conf
```
interface wlan0       
static ip_address=192.168.3.111            #static IP
static routers=192.168.3.1                 #address of router
static domain_name_servers=192.168.3.1 114.114.114.114     #address of DNS
```

### Step 2: modify the ip config in config/config.py
In this example, the IP of my PC is 192.168.3.4, so you need to modify raspi_ip and compu_ip as the below
```
raspi_ip = '192.168.3.111'
compu_ip = '192.168.3.4'
```

### Step 3: run
+ make both raspiberry and pc connect to a same wifi
+ run compu_main.py on pc
```
python compu_main.py
```
+ run raspi_main.py on raspiberry
```
python raspi_main.py
```

enjoy yourself

### *License*

puppy is released under the [Apache 2.0 license](license.txt).

```
Copyright 1999-2018 KITTCAMP.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at following link.

     http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
