Delta Controls UDMI Gateway – Quick Start

1.	From a browser launch enteliWEB (e.g. http://localhost/enteliweb)
2.	Open the settings menu (use the cogs icon, top right) 
3.	Create a site and give it a Site Name , Device Number and a Device Name for BACnet
4.	Add a Network Connection to the local UDP/IP network (make sure you Connect to the local network)
5.	Select the Navigator accordian and you should see enteliWEB discover the devices on the local IP network – including the O3 Controller
6.	Select the O3 and the objects will be discovered in the main pane
7.	Using the ‘Manage’ menu in the main pane create a FIL object named ‘Google Cloud IoT.dlm’ and upload the UDMI Gateway module into it.
8.	Create a CSV object named ‘Google Cloud IoT Configuration’ and set the ‘Default Value’ to a JSON dictionary that defines the connection to GCP, e.g.

{
 "hostName": "mqtt.googleapis.com",
 "tcpPort": 8883,
 "location": "us-central1",
 "project": "bacnet-gateway",
 "registry": "US-MTV-918R",
 "device": "GAT-4121442",
 "poll-interval": 30000,
 "debug": 4,
 "cloud-write": 1
}

9.	Create a CSV object named ‘Google Cloud IoT Public Key’ and you should find the public key for the connection to GCP in the description property of the object. Load this into the Gateway device on GCP, create the Gateway and Device config blocks on GCP, bind the device(s) to the gateway


