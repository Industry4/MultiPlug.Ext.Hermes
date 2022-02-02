# MultiPlug.Ext.Hermes

## Functionality

This Extension, with the use of MultiPlug.Ext.Networks, allows you to connect to Up-line and Down-line electronics production equipment that are also capable of communicating using the IPC-HERMES-9852 messaging standard (https://www.the-hermes-standard.info).

The modes of operation are Pass Through and SMEMA Adaptor.

The Pass Through mode allows the creation of a Hermes man-in-the-middle to capture message data which will include PCB (Printed Circuit Board) information.

The SMEMA Adaptor mode (IPC-SMEMA-9851) requires additional hardware (available at https://www.4ir.uk/products/smema-hermes-adaptor/) to interface with the SMEMA I/O. This mode allows SMEMA equipment to be upgraded and prevents PCB data from being lost as a PCB moves along an assembly line.

## Setup

.. Read the Wiki above.

1. Within MultiPlug.Ext.Networks, create a Client Socket for the Up-line machine and use its IP address and the default port 50101.
2. Create a Socket Endpoint for the Down-line machine and use the default port 50101.
3. For the Client Socket, subscribe to the Hermes Up-line message send event.
4. For both the Socket Endpoint, subscribe to Herme Down-line message send event.
5. Within MultiPlug.Ext.Hermes Up-line settings, subscribe to the Client Socket read event.
6. For the Hermes Down-line setting, subscribe to the Socket Endpoint read event.

Setup for the SMEMA Adaptor mode will be documented with the adaptor instructions.

## Software License

The Extension works under evaluation. To purchase a licence contact hello@industry4.uk (4IR.UK British Systems)

## User Interface
![](https://www.the-hermes-standard-smema-adaptor.info/images/hermes-smema-adaptor-user-interface.png)

## Setup Interface
![](https://www.the-hermes-standard-smema-adaptor.info/images/hermes-smema-adaptor-setup-interface.png)
