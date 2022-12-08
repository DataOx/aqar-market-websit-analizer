### **Project Objective**
1. You need to give the client 4 values: how many unique ads are on each link (links are given below).
2. There are identical ads on the site, and they need to be filtered out. The only way to compare if they match, the ads have the same pictures.
3. In the case of scraping, if there are identical ads (same pictures), then the second ad with the same pictures we do not count as unique.
4. If there is more than one picture in add, we will only compare the main one on the first page.
5. If the ad does not have any pictures, we count it as a real ad, not a duplicate.

* [Villa for sale in Riyadh](https://sa.aqar.fm/فلل-للبيع/الرياض)
* [Villa for sale in jeddah](https://sa.aqar.fm/فلل-للبيع/جدة)
* [Land for sale in Riyadh](https://sa.aqar.fm/أراضي-للبيع/الرياض)
* [Land for sale in Jeddah](https://sa.aqar.fm/أراضي-للبيع/جدة)

### **Used libs** 
* celery
* fiftyone
* redis
* requests

### **Project architecture**

![Project architecture](images/architecture.png "Title")


**Deploy**

Step 1. Install docker and docker-compose
- `sudo apt update -y`
- `sudo apt upgrade`
- `sudo apt install apt-transport-https ca-certificates curl software-properties-common`
- `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
- `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"`
- `sudo apt update`
- `sudo apt install docker-ce`
- `sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
- `sudo chmod +x /usr/local/bin/docker-compose`

Step 2. Project deploy

NOTE: Execute commands in the project folder!
- **up project**: `docker-compose up --build -d`
- **down project:** `docker-compose down`
