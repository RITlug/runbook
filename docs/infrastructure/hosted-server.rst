RITlug Server
=============

RITlug has a hosted server, located in the Institute Hall Datacenter. It's currently owned and maintained by `Solomon Rubin (Serubin) <https://github.com/serubin/>`, however it periminently on lend to RITlug. He remains the primary contact for any major issues. RITlug related use will be maintained by disignated Club Server Admins. 

Specifications
--------------
PowerEdge R410 Server

* 4tb x 2 (only 2tb usable due to raid card) & 1tb x2 in RAID 10 for 3tb

* 32gb Ram

* Iten Xeon 6500 CPU

* Running Proxmox


Management
----------
RITlug's website is powered by Github pages and stored in a repository
in the RITlug Github organization. It is powered by vanilla Jekyll (no
plugins) as Github pages does not allow plugins for security reasons. In
order to update any aspect of the site, simply push or merge changes to
the repository and the changes will take effect within a few minutes.

Create a new VM
^^^^^^^^^^^^^^^
When creating a custom VM or a new template, use this set of instructions.

1) [General] Set Resource Pool to `RITLUG`

2) [General] Set VM ID using the following notation:

```
3xx: Student VMs
2xx: Club VMs
1xx: Solomon's VMs (Keep out)
Keep IDs incremental if possible.
```

3) [General] Give it a name!

4) [OS] Select OS

5) [CD/DVD] Select your ISO from the `local` storage.

6) [Hard Disk] Set Bus `VirtIO` and `0`

7) [Hard Disk] Set Format to `QEMU`

8) [Hard Disk] Do not change the `Cache` item

9) [Hard Disk] Select Size

10) [CPU] Set `Type` to `host`

11) [CPU] Set `Cores`. Do not change `Sockets`

12) [Memory] Use `fixed size memory`

13) [Network] Set `Model` to `VirtIO`

14) [Network] Set `MAC Addr` as necessary

15) Profit!

Create a VM from Template
^^^^^^^^^^^^^^^^^^^^^^^^^
When creating a new VM from a template.

1) Right click on desired template and click "Clone"

2) Set VM ID using the following notation:
```
3xx: Student VMs
2xx: Club VMs
1xx: Solomon's VMs (Keep out)
Keep IDs incremental if possible.
```

3) Set `Mode` to `Full Clone`

4) Set `Resource Pool` to `RITLUG`

5) Set name and continue.

6) Resize disk & modifiy resources as needed

7) Start VM and follow any setup scripts

8) Profit!

Use and Access
--------------
TBD

Contacts
--------



