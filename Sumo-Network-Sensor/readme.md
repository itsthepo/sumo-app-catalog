# This doc will provide instructions on how to get this app into your Sumo instance!

## **Bring light to dark with network visibility using the Sumo Logic's Network Sensor**

- Background: The Network Sensor app aims to enable incident responders and threat hunters to work faster and more effectively resulting in powerful security insights through key traffic dashboards and [YARA detections](https://help.sumologic.com/docs/cse/rules/import-yara-rules/) such as:

    - Connections: Creating situational awareness using lists of top services, ports, data flows, sources, and destinations.

    - DNS: Detect potential DNS exfiltrations by spotting queries to non-existent domains and other high connection counts.

    - Files: Potentially find executables hidden in benign extensions and compressed files. In addition, you can leverage an additional detection methodology here known as YARA. Please see [here](https://help.sumologic.com/docs/cse/rules/import-yara-rules/) for more information.

    - HTTP: Find potentially suspicious HTTP transactions by reviewing a list of top host headers, sources, rare user agents and rare host headers.

    - IP Investigation: Potentially identify anomalies by reviewing top protocol usage, internal vs. external connections, top connections by bytes transferred and where that IP address has been seen in other data sources in your environnement. 

    - SMB: Detect potential SMB crawling/enumeration by understanding what systems/assets are still using SMB and what version of SMB. Gather real insights on where potential low hanging fruit may hide!

    - SSL: Potentially find risky external/internal user connections to weaker SSL versions.



### **Step 1 - Ensure Sumo Logic's Network Sensor is deployed**:
- Ensure that you have Sumo Logic's [Network Sensor](https://help.sumologic.com/docs/cse/sensors/network-sensor-deployment-guide/) deployed within your environment. 
    - *If you need assistance with deployment of the network sensor please reach out to your SE/CSM/TAM*


### **Step 2 - Import the JSON in the folder labeled '[CloudSIEM_Network_Sensor.json](/Sumo-Network-Sensor/CloudSIEM_Network_Sensor.json)' to your Sumo Logic Instance**:  

*Please note, most of the time you will have to edit the json file to find and replace the default _sourceCategory with whatever matches your environment. Due to this being a Sumo Logic Network Sensor, the SCs are not different UNLESS changed by you. If you did change the default sourceCategories then please update accordingly*. 

![alt text](/Sumo-Network-Sensor/screenshots/import.png)

After you have opened the import window, you will be presented with a name box and a field to copy and paste the json (as shown below):

*Please note that it is much easier to give it a name first and THEN copy and paste the json. Once you paste the JSON, the windows auto scrolls to the bottom of the page to be imported.*


![alt text](/Sumo-Network-Sensor/screenshots/copy-paste.png)




### **Step 3 - Enjoy!**

Here is an example of the connections tab: 
![alt text](/Sumo-Network-Sensor/screenshots/connections.png)

Here is an example of the ip-investigations tab: 
![alt text](/Sumo-Network-Sensor/screenshots/ip-investigation.png)



***Please note, there could be improvements to the app leveraging Sumo's outlier function and other functionality list. In addition, this app may work for normal corelight/zeek users as well. (Needs testing)***
