# powerTag
Node-red interface for Schneider Powertag products

**Description**

Schneider Powertag is an energy sensing product used for retro fitting or new installation in distribution boards.

The sensors communicate wirelessly to a gateway, which in turn makes the data available via MODBUS TCP or web interface. The gateway used in this project is Acti9 Smartlink SI D.

powerTagModbus.json is a set of flows for node-red.

The basis of the flow is:
1. Trigger timers to read data
2. Select which modbus units are to be read from
3. Select either Single Phase or Three Phase modbus map
4. Request data from gateway using Modbus TCP
5. Extract data to human readable values
6. Display data

**Notes:**

- Mapping has only been done for sensors at present - there is more information available from the gateway as described in Schneider Electric document DOCA0115EN-03

- The Three Phase modbus map needs building from the single phase map with the additional registers for 3 phase.
Templates could be used better in this flow. I'm new to node-red.

- Instead of using the built in UI, the end goal is to make the information availble to MQTT or an OPC server.

- This is my first Github project. If you have constructive comments or advice on better ways to manage or do things, I'm all ears.
