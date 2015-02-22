RockStorUI

This is a prototype project to create a server monitoring application with asychronous connection. 

The RockStor dashboard is a view for an admin to monitor the storage, compute and network resources of the appliance. The dashboard is designed as a configurable set of widgets, each displaying information about the resources such as uptime, CPU, network activity, and storage capacity. 

More information available here:
http://rockstor.com/docs/dashboard.html

Our project is an upgrade to the Rockstar dashboard, which currently uses periodic polling to load new data from the server. This method suffers from latency issues due to the synchronous nature of the server and the overhead of HTTP requests:

![](https://cloud.githubusercontent.com/assets/8097623/6320700/1ce4ac1c-ba9a-11e4-89e8-d50b339c5730.jpg)

We replace these high frequency HTTP requests with WebSockets, which provide a persistent, low latency connection that can support transactions initiated by the server. This allows us to receive event-driven responses without having to poll the server for a reply. The end result is reduced latency and a better user experience.



