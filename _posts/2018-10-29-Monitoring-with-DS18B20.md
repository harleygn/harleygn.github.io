During the winter, weather conditions overnight can reach very low temperatures, and while snow is rare, frost is common with temperatures dropping below zero celsius in the coldest months. For chickens kept outside, this can be a tough time of year, and so it is essential for their wellbeing that they are kept warm enough. In order to keep an eye on the conditions within their coop, this simple monitoring unit will read and transmit readings from a probe inside the roosting area, raising a warning when conditions become severe.

Building on the simple data logger described previously, this unit will use a DS18B20 waterproof temperature sensor, and be housed inside a weatherproof container to allow it to be mounted externally. It will make use of the Thinger.io platform, and communicate using WiFi to the local network. Notifications will be provided either by Thinger.io or using a third-party service given access to Thinger.io device instance.

## Hardware

Only a few components are required for the unit, using only a NodeMCU board, 4.7K resistor and the waterproof variant of the DS18B20 digital temperature sensor, all connected using a few jumper cables and mounted on a breadboard. The below diagram gives simple explanation of the connections.

![ nodemcu_ds18b20_bb](/Users/harleygn/Documents/harleygn.github.io/images/nodemcu_ds18b20_bb.png)Before mounting the electronics inside a box, the componetns will be soldered to a sheet of proto-board.