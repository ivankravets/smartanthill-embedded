SmartAnthill Embedded System
============================

Please follow to `Documentation <http://smartanthill-10.readthedocs.org/en/latest/specification/embedded/index.html>`_ section of *SmartAnthill Embedded System*.

*SmartAnthill Embedded System* allows main `SmartAnthill System <https://github.com/ivankravets/smartanthill>`_ to communicate with hardware part
(`Peripherals <http://smartanthill-10.readthedocs.org/en/latest/specification/embedded/peripherals.html>`_) of micro-based device through `Router Service <http://smartanthill-10.readthedocs.org/en/latest/specification/embedded/router.html>`_ that resides on *Network Layer* of `SmartAnthill Network Model <http://smartanthill-10.readthedocs.org/en/latest/specification/network/netmodel.html>`_.

Router Service
--------------

*Router Service* operates with *Packet* structures and performs the next
tasks:

* Parsing of incoming *Packet* from a "bytes flow"
* Acknowledging of incoming *Packet* if it has ``PACKET_FLAG_ACK``
* Sending an outgoing *Packet*
* Operating with Stack of outgoing *Packets*

Activity Diagram
~~~~~~~~~~~~~~~~

.. image:: https://raw.githubusercontent.com/smartanthill/smartanthill1_0/develop/docs/specification/embedded/router.png


Operational State Machine
-------------------------

The `Operational State Machine <http://smartanthill-10.readthedocs.org/en/latest/specification/embedded/osm.html>`_ is a
`Finite State Machine <http://en.wikipedia.org/wiki/Finite-state_machine>`_
with predefined operational states. It can be in only one operational state at
a time. The transition from one operational state to another can be initiated
by a *Triggering Event* (device interrupt) or *Condition* (based on `Channel Data Classifier <http://smartanthill-10.readthedocs.org/en/latest/specification/network/cdc/index.html>`_).


State Diagram
~~~~~~~~~~~~~

.. image:: https://raw.githubusercontent.com/smartanthill/smartanthill1_0/develop/docs/specification/embedded/osm.png

Questions
---------

Please use the
`issue tracker <https://github.com/ivankravets/smartanthill/issues>`_
to ask questions.

Licence
-------

Copyright (c) 2013-2014 Ivan Kravets

Licenced under the MIT Licence.
