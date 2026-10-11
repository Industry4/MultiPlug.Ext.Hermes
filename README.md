# MultiPlug.Ext.Hermes

The MultiPlug IPC HERMES 9852 Extension is used for the transfer of PCB related data between manufacturing equipment on a electronics assembly line.

## Functionality

This Extension, with the use of the [MultiPlug.Ext.Network.Sockets](https://www.nuget.org/packages/MultiPlug.Ext.Network.Sockets/) [MultiPlug](https://www.multiplug.app/) Extension allows you to connect to Upstream and Downstream electronics production equipment (SMT) that are capable of communicating using the [IPC-HERMES-9852](https://www.the-hermes-standard.info) messaging standard.

The modes of operation are Pass Through and SMEMA Gateway:

* The Pass Through mode allows the creation of a Hermes man-in-the-middle to capture message data which will include PCB (Printed Circuit Board) information.

* The SMEMA Gateway mode (IPC-SMEMA-9851) requires an additional hardware Extension to interface with the SMEMA I/O, eg [MultiPlug.Ext.RasPi.GPIO](https://www.nuget.org/packages/MultiPlug.Ext.RasPi.GPIO/) or [MultiPlug.Ext.Brainboxes](https://www.nuget.org/packages/MultiPlug.Ext.Brainboxes/) . This mode allows SMEMA equipment to be upgraded and prevents PCB data from being lost as a PCB (printed circuit board) moves along an assembly line. There is also a [SMEMA Simulator](https://github.com/Industry4/MultiPlug.Ext.Hermes/wiki/User-Manual-About#smema-simulation-and-debugging) for software development.

## More Information

* MultiPlug.Ext.Hermes is not a software development library, but runs as a Windows or Linux Service with MultiPlug
* [Read the Wiki](https://github.com/Industry4/MultiPlug.Ext.Hermes/wiki) for more information

## Setup

1. Within [Multiplug.Ext.Network.Sockets](https://www.nuget.org/packages/MultiPlug.Ext.Network.Sockets/), create a Client Socket for the Upstream machine and use its IP address and the default port 50101.
2. Within [Multiplug.Ext.Network.Sockets](https://www.nuget.org/packages/MultiPlug.Ext.Network.Sockets/), create a Socket Endpoint for the Downstream machine and use the default port 50101.
3. Within Multiplug.Ext.Network.Sockets Client Socket, subscribe to the Hermes Upstream XML message send event, of MultiPlug.Ext.Hermes.
4. Within Multiplug.Ext.Network.Sockets Socket Endpoint, subscribe to Herme Downstream XML message send event, of MultiPlug.Ext.Hermes.
5. Within MultiPlug.Ext.Hermes Upstream settings, subscribe to the Client Socket read event, of Multiplug.Ext.Network.Sockets.
6. Within MultiPlug.Ext.Hermes Downstream settings, subscribe to the Socket Endpoint read event, of Multiplug.Ext.Network.Sockets.
7. Click Deploy within MultiPlug and the Event connections will be made.

## Purchase a Software License

This Extension works under a 60 minute evaluation. Restarting the software will restart the evaluation period. To purchase a licence visit: [SmartFactoryDirect.com](https://www.smartfactorydirect.com/multiplugexthermes-software-license)

## Runtime Digital Twin Animation
![](https://github.com/user-attachments/assets/5caa75a4-af24-4b99-b87e-670b61068d44)
