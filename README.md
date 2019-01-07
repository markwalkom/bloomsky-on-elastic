# bloomsky-on-elastic
BloomSky analytics using the Elastic Stack

## Why?
The BloomSky app is great for your phone, but I wanted something I could pull up at home on a monitor and also just have the stats around for my own curiosity. BloomSky has an API, and the Elastic Stack can consume that :)

# Setup
## Elasticsearch
1. Open `Dev Tools` in Kibana and then copy and paste the `mapping.json` contents in
2. Apply the template

## Logstash
1. Copy `logstash.conf` to your Logstash instance
2. Rename the file, I use `bloomsky-api.conf`
3. Edit the config file and update;
 1. `Authorization`
 2. `hosts`
 3. `user`
 4. `password`
4. (Re)Start Logstash and watch the data come in

## Kibana
1. [Import](https://www.elastic.co/guide/en/kibana/6.5/managing-saved-objects.html#_import_objects) the `kibana-objects.json` file

# The Results
Should be something like this;
![Dashboard Screenshot](https://raw.githubusercontent.com/markwalkom/bloomsky-on-elastic/master/Last_24_Hours_Dashboard.png)

# To do
* Show the latest image from the camera
* Finish the Yearly dashboard
