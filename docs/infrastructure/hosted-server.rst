#############
Hosted server
#############

RITlug has a hosted server in the Institute Hall data center.
It is currently owned and maintained by `Solomon Rubin`_ (Serubin).
It is permanently on lend to RITlug.
He remains the primary contact for any major issues.
RITlug-related use  is maintained by designated club Server Admins. 


**************
Specifications
**************

PowerEdge R410 Server

- **Storage**:
  
  - 4TB x2 (only 2TB usable due to RAID card)

  - 1TB x2 (in RAID 10 for 3TB)

- **Memory**: 32GB RAM

- **CPU**: Intel Xeon 6500

- **Software**: Proxmox


**********
Management
**********

This section is for management of resources on the hosted server.
Some parts of RITlug's infrastructure are hosted in GitHub, like our website (see :doc:`website`).

Create new VM
=============

When creating a custom VM or a new template, use this set of instructions.

#. [*General*] Set Resource Pool to `RITLUG`
#. [*General*] Set VM ID using the following notation:

   - `3xx`: Student VMs
   - `2xx`: RITlug club VMs
   - `1xx`: Solomon's private VMs (not for club use)
   - **Keep IDs incremental** if possible

#. [*General*] Give it a clear name!
#. [*OS*] Select OS
#. [*CD/DVD*] Select your ISO from the `local` storage.
#. [*Hard Disk*] Set Bus `VirtIO` and `0`
#. [*Hard Disk*] Set Format to `QEMU`
#. [*Hard Disk*] Do not change the `Cache` item
#. [*Hard Disk*] Select Size
#. [*CPU*] Set `Type` to `host`
#. [*CPU*] Set `Cores`. Do not change `Sockets`
#. [*Memory*] Use `fixed size memory`
#. [*Network*] Set `Model` to `VirtIO`
#. [*Network*] Set `MAC Addr` as necessary
#. Profit!

Create VM from Template
=======================

When creating a new VM from a template…

#. Right click on desired template and click "Clone"
#. Set VM ID using the following notation:

   - `3xx`: Student VMs
   - `2xx`: RITlug club VMs
   - `1xx`: Solomon's private VMs (not for club use)
   - **Keep IDs incremental** if possible

#. Set `Mode` to `Full Clone`
#. Set `Resource Pool` to `RITLUG`
#. Set name and continue
#. Resize disk, modify resources as needed
#. Change MAC address in network settings.
   Use an unallocated MAC from the list on the eboard GitLab and record the new use in the list.
#. Start VM, follow any setup scripts
#. Profit!

Use and Access
==============

Use and access is limited to members of the executive board.
In the future, there may be opportunities for club members to participate in managing RITlug's infrastructure.

Contacts
========

- `Solomon Rubin`_


.. _`Solomon Rubin`: https://github.com/Serubin
