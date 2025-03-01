.. _ug_matter_overview_dev_model:

Matter development model
########################

.. contents::
   :local:
   :depth: 2

The Matter stack is developed on the official `Matter GitHub repository`_ and is open-sourced.

The Matter stack implementation contains separation between platform-agnostic and platform-dependent functionality.
The open-source implementation offers ports for several resource-constrained, embedded SoCs as well as POSIX-based platforms.

Matter strives for reusing technologies from market-proven solutions, such as Apple HomeKit or Google Weave.
Wi-Fi and :ref:`ug_thread` are its main wireless connectivity protocols that offer seamless integration with other IPv6-based networks and are application-layer agnostic.
Bluetooth® LE can be used for commissioning of the Matter accessories, and QR codes and NFC tags can be used to initiate the commissioning.

For more information about Matter architecture, read :ref:`ug_matter_overview_architecture_integration`.

Matter in the |NCS|
*******************

The |NCS| provides full toolchain for Linux, macOS, and Windows, and is built on top of the Zephyr RTOS.
It includes west for managing repositories, toolchain manager for managing toolchain, Kconfig for feature configuration, and Devicetree for board description.
Finally, it integrates the OpenThread and Wi-Fi stacks, both of which can work in a multiprotocol scenario with the integrated Bluetooth® LE stack.

Nordic Semiconductor integrates the Matter stack in the |NCS| using a dedicated fork ``nrfconnect/sdk-connectedhomeip``.
The official Matter repository is fetched into the fork and the fork is included in the |NCS| as a Zephyr module.
The fork is maintained and verified as a part of the nRF Connect SDK release process.

For more information about Matter in the |NCS|, read :ref:`ug_matter_overview_architecture_integration`.
