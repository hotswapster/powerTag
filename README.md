# powerTag
 Node-red interface for Schneider Powertag products. This Git uses Node-Red Projects.
 powerTag
 ========

 **Description**
 A user interface for the Schneider PowerTag product

 Schneider Powertag is an energy sensing product used for retro fitting or new installation in distribution boards.
 ### About

 The sensors communicate wirelessly to a gateway, which in turn makes the data available via MODBUS TCP or web interface. The gateway used in this project is Acti9 Smartlink SI D.

 This project is a set of flows for node-red.

 The basis of the flow is:
 1. Trigger timers to read data
 2. Select which modbus units are to be read from
 3. Select either Single Phase or Three Phase modbus map
 4. Request data from gateway using Modbus TCP
 5. Extract data to human readable values
 6. Display data

 **Notes:**

 - Mapping has only been done for sensors at present - there is more information available from the gateway as described in Schneider Electric document DOCA0115EN-03

 - The Three Phase modbus map is the master, the single phase map needs updating. 
 - Templates could be used better in this flow. I'm new to node-red.
 - The Node-red UI is not intened as the end user UI.
 - The end goal is to have the information available via MQTT, to MySQL or to HomeAssistant.
 - This is my first Github project. If you have constructive comments or advice on better ways to manage or do things, I'm all ears.
