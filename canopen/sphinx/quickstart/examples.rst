Running Examples
================

In order to try out the examples provided in the ``canopen_tests`` follow these steps:

Ensure that the virtual CAN interface is active. You can start it by following the instructions from  :ref:`started the vcan0 interface <quick-start-setup-can-controller>`.

Once, the Virtual CAN is active, the following examples can be carried out.

Service Interface
---------------------

The ``cia402_setup.launch.py`` example typically sets up an environment for interacting with devices that use the CIA402 application layer of the CANopen protocol.

.. code-block:: bash

    ros2 launch canopen_tests cia402_setup.launch.py

This setup allows you to test and interact with CANopen devices in a controlled environment.

Managed Service Interface
-------------------------

The ``cia402_lifecycle_setup.launch.py`` example is designed to demonstrate the lifecycle management features of CANopen devices that follow the CIA402 protocol.

.. code-block:: bash

    ros2 launch canopen_tests cia402_lifecycle_setup.launch.py

By following these steps, you will successfully start the managed service interface example. This setup allows you to interact with and test the lifecycle management features of CANopen devices using the CIA402 protocol.

ROS2 Control
------------

Proxy Setup
,,,,,,,,,,,

.. code-block:: bash

   ros2 launch canopen_tests canopen_system.launch.py

This command launches a CANopen proxy, which acts as a mediator between ROS2 and CANopen devices. It helps in managing communications and data exchange.


CiA402 Setup
,,,,,,,,,,,,

.. code-block:: bash

   ros2 launch canopen_tests cia402_system.launch.py

This example sets up a system configuration for interacting with multiple CIA402-compliant devices, allowing for coordinated control and monitoring.

Robot Setup
,,,,,,,,,,,,

.. code-block:: bash

    ros2 launch canopen_tests robot_control_setup.launch.py

This command sets up the overall robot control system, preparing it to manage the connected devices and handle control logic.

.. Note::  To know about the output of these examples, below can command can be run in a new terminal. 
.. code-block:: bash

   sudo apt install can-utils
   candump
