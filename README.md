RockStorUI

This is a prototype project to create a server monitoring application with asychronous connection. 

The RockStor dashboard is a view for an admin to monitor the storage, compute and network resources of the appliance. The dashboard is designed as a configurable set of widgets, each displaying information about the resources such as uptime, CPU, network activity, and storage capacity. 

More information available here:
http://rockstor.com/docs/dashboard.html

Our project is an upgrade to the Rockstar dashboard, which currently collects data from the server through continuous polling, which suffers from latency issue due to the synchronous nature of the server and the overhead of HTTP:

![](https://cloud.githubusercontent.com/assets/8097623/6320700/1ce4ac1c-ba9a-11e4-89e8-d50b339c5730.jpg)

We replace these high frequency API requests with WebSockets, which provide a persistent, low latency connection that can support transactions initiated by the server. The end result is increased performance and a better user experience.



