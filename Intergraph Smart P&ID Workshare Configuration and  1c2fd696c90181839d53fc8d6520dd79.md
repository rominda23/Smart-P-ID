# Intergraph Smart P&ID Workshare Configuration and Reference

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Workshare**

**Configuration and Reference**

**Hexagon Documentation**

Generated 03/19/2025

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 1/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Table of Contents**

Using Workshare

Workshare Common Tasks

Using Workshare with Projects

Networking for Connected Workshare

Workshare and Firewal s

DMZ vs. VPN

Isolating Network Clients in a DMZ Environment

Sample DMZ Environment Configurations

Sample VPN Environment Configuration

Configuring Oracle for Connected Workshare

Enabling Oracle Global Naming

Locking Oracle into Using a Static Port

Understanding the Database Link

Configuring Workshare

Configuring the Host Site

Enabling Workshare

Creating Satel ite Slots

Configuring a Satel ite Site

Concluding a Workshare Col aboration

Disabling Workshare

Managing a Workshare Col aboration

Ownership

Publishing Data for Synchronization

Changing the Workshare Password

Proxy Users

Creating Satel ite Templates

Publishing and Assigning Ownership

Publish a Drawing

Extract Published Drawings

Set Subscription Access for a Drawing

Assign Ownership to a Drawing

Publish Command (Workshare Menu)

Publish Dialog

Extract Published Drawings Command (Workshare Menu)

Extract Published Drawings Dialog

Extract Published Drawings Status Dialog

Subscribe Access Command (Workshare Menu)

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 2/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Subscribe Access Dialog

Assign Ownership Command (Workshare Menu)

Assign Ownership Dialog

Getting Latest Versions of Drawings

Get the Latest Version of a Drawing from a Remote Site

Get Latest Version from Remote Command (Workshare Menu)

Get Latest Version from Remote Dialog

Get Latest Version from Remote Dialog (status)

Get the Latest Version of a Drawing from the Local Computer

Get Latest Version from Local Command (Workshare Menu)

Get Latest Version from Local Dialog

Select Publish Folder Dialog

Get Latest Version from Local Dialog (status)

Synchronizing Reference Data

Synchronize Reference Data from Host

Synchronize Reference Data from a Copy

Synchronize Reference Data Command (Workshare Menu)

Synchronize Reference Data Dialog

Synchronize Reference Data from Copy Command (Workshare Menu)

Synchronize Reference Data from Copy Dialog

Default Report Template Path Dialog

P&ID Template Path Dialog

Catalog Explorer Root Path Dialog

Synchronizing Shared Items

Synchronize Shared Items

Synchronize Shared Items Command (Workshare Menu)

Synchronizing Shared Items Dialog

Sample Synchronize Shared Items Workflow

Scheduling Workshare Tasks

Schedule Publish Command (Workshare Menu)

Schedule Task Wizard

Schedule Get Latest Version from Remote Command (Workshare Menu)

Schedule Get Latest Version from Remote Dialog

Schedule Synchronize Reference Data Command (Workshare Menu)

Schedule Synchronize Shared Items Command (Workshare Menu)

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 3/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Using Workshare**

Workshare functions allow you to share Smart P&ID data within one plant structure with remote sites. Designed for companies running plants from multiple sites, EPCs or Owner/Operators, or for multiple companies that are working on a single plant, Workshare provides tools to manage changes as if they were created at the same site.

**Hosts and Satellites**

Workshare functions use a host/satellite model for sharing Smart P&ID data among multiple locations. The host, using Smart P&ID, creates satellite slots that include the entire Smart P&ID system and grants access to P&ID data by allowing the satellite sites to subscribe to an available satellite slot.

The satellite sites, after using Smart P&ID to subscribe to a satellite slot at the host site, use Smart P&ID Drawing Manager to create, view, or modify the drawings.

Drawing ownership is controlled at the site where they are created. When ready, the owner of a drawing can grant ownership to the host or to other satellites. Throughout this sharing process, synchronization tools in Smart P&ID Drawing Manager allow the host and the satellites to make sure they are working with the latest data.

**Workshare Modes**

Workshare can be configured in two modes:

**Connected**

Uses a database link established between the database servers at the host and satellite sites.

In other words, satellites are distributed databases linked to a host database. In connected Workshare, both the host and satellite must be using Oracle. If you plan to use Workshare in an integrated environment, we recommend using connected Workshare to ensure smooth claiming.

**Standalone**

Shares files and data without having a database link. Files are manually transmitted between host and satellites.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 4/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Any given site can host both connected and standalone satellites. In other words, the host can use Oracle and the satellite can use SQL Server, or any combination thereof. However, a site must use Oracle to host a connected Workshare collaboration.

**Configurations**

There are numerous configuration possibilities for implementing Workshare. For example, you can use Workshare to simulate the PDS 2D Task/Master configuration by using the Workshare host as the Task environment and the satellite as the Master. You could then publish drawings for sharing from the host to the satellite. By limiting user access at the satellite site to Read Only for Smart P&ID objects, the satellite becomes an issued drawing database.

You can also use standalone Workshare in a mixed database environment where the host can be using Oracle and the satellite can be using SQL Server, or vice-versa. This configuration is useful when multiple companies using different database standards are working on the same plant.

Standalone Workshare provides a means of implementing off-site projects.

Workshare can be used in an integrated environment. See Using Workshare in an Integrated Environment. Another possible configuration involves using Workshare at the project level within an As-Built plant scenario. See Using Workshare with Projects.

**Automation**

Several of the Workshare commands are available in the Smart P&ID automation layer. For more information about using these Workshare automation commands, see the *Smart P&ID*

Programmer’s Help.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 2003-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 5/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Version 12

Published 12/31/2024 at 10:38 AM

**Workshare Common Tasks**

After configuring Workshare at the host and satellite sites, the following tasks are used frequently when using Workshare in Smart P&ID. Most of these procedures can also be scheduled for a later time or at regular intervals.

**Publishing a Drawing**

To share a drawing with another site, you must first publish that drawing. Publishing the drawing does not grant access to the drawing: it only freezes a copy of the drawing in anticipation of ownership being transferred. Between the publication of a drawing and the transfer of ownership, the publishing site still owns the drawing and is free to modify it.

Granting subscription access to the drawing gives another site read-only access to the published copy of the drawing. Assigning ownership to the drawing allows the new owner to claim ownership of the drawing and obtain the published copy of the drawing.

**Granting Access to a Drawing**

After you publish a drawing, you can grant access to that drawing by using the **Subscribe** **Access** command. For connected Workshare, the designated satellite site will be able to open and view the published drawing, but will not be able to modify it. For standalone Workshare, the drawing will be writeable at the satellite site. You can grant write access to a drawing, too, by using the **Assign Ownership** command. The designated site will then not only be able to open the drawing but also to edit it.

As soon as you use the **Assign Ownership** command, the selected drawing is automatically published.

**Getting the Latest Version of a Drawing**

After a site has been granted access to a published drawing, that site must subscribe to the latest version in order to open or edit that drawing. Normally you get the latest version over a Workshare connection from the owner site by using the commands for remote access. You can also get the latest version from a local folder - for instance, if the site has sent you the latest version on CD.

Drawings are never dynamically linked between sites. That is, the version you view is only the latest version you subscribed to or only the latest version left on your site. If another site has https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 6/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

modified the drawing since then, you do not see those changes.

**Synchronizing Reference Data**

Because only the host site can change the reference data, satellite sites need to synchronize the reference data from the host site each time it changes. Synchronizing the reference data involves making sure both the host and satellites are using the same plant schema and data dictionary, plant structure, Smart P&ID schema and data dictionary, and various options settings. Synchronization also involves making sure various data files at the satellite site remain up to date with the files at the host. These files include the rules file, insulation specification file, report and drawing templates, symbology settings, CAD definition file, and so forth.

You can synchronize this data either with the host site or with a copy of the reference data on your local computer or network using the **Synchronize Reference Data** commands.

Reference data at the satellite site must be synchronized with the host reference data before drawings and shared items can be synchronized or transferred.

We recommend scheduling synchronization for a time when no users are working in the data.

**Synchronizing Shared Items**

Some drawing items, such as off-page connectors, instrument loops, and utility connectors, require special handling when using Workshare. Because these items can be shared by more than one drawing, any modifications made to a drawing at another site can have ramifications for the shared items contained in that drawing.

Several Workshare commands are available in the Smart P&ID automation layer.

See the *Smart P&ID*  Programmer’s Help.

**Using Workshare with Projects**

Workshare functions the same whether using projects or not. The only difference is that when using projects, only a project can function as a Workshare host. The Plant cannot be a host or a satellite when projects are enabled.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 7/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

In a Workshare collaboration, new plant groups cannot be created by standalone satellite sites or by the satellite sites in a project.

Connected Workshare is available only for sites using Oracle databases. If your plants and projects are using a SQL Server database, you cannot use connected Workshare.

Standalone Workshare allows you to mix the type of databases used in a Workshare collaboration.

When a project is used as a Workshare host, the satellites synchronize their reference data with the Plant reference data.

When transferring ownership of a drawing to another Workshare site, the corresponding versions are not transferred. Only the current version of the drawing is transferred.

New plant groups (plants, areas, units, and so forth) cannot be created by satellites hosted by a project.

**Using Projects in an Existing Workshare Collaboration** You must discontinue all Workshare collaboration in a plant before you can create projects in the plant. In other words, if the plant structure contains active **Satellites**, the **Enable Projects** command remains unavailable. We recommend completing the following tasks before enabling the plant for projects.

1. Transfer all drawings to the host.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 8/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

1. Delete all satellites.
2. Disable the plant for Workshare.
3. Enable the plant for projects.
4. Create a project to serve as the host.
5. Enable the project for Workshare.
6. Create satellite slots in the project host.
7. Create satellites.
8. Check out or fetch drawings at the host, then re-distribute drawings back out to the satellites.

**Projects vs. Workshare**

The following comparisons can be useful when making the decision about whether to use projects or Workshare or both.

**Category**

**Projects**

**Workshare**

Topology

Each plant can have many Each Workshare host can have projects. Each project

many satellites. Each satellite

belongs to exactly one

belongs to exactly one host.

plant.

Identity

Objects that are

Objects that are transferred

transferred between a

between a host and a satellite

plant and a project

maintain their identity.

maintain their identity.

Reference Data

One set of reference data The reference data must be the is used for a plant and all

same for a host and its satellites.

its projects. Changes can Changes can be made only

be made only through the through the host. Changes are https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 9/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Plant. Because all projects propagated to the satellites by use the same reference

means of the synchronize

data as the Plant, all

reference data commands in

projects immediately see

Drawing Manager.

changes to the reference

data.

Physical Separation

A plant and all its projects Connected Workshare allows data must exist on the same

to be distributed to multiple

server and within the

database instances on separate

same database instance.

servers that might be remote from

the host server.

Standalone Workshare allows

data to be distributed between

separate database types.

Organization

Projects are suited to

Workshare is suitable for dividing

dividing up work that will

up work among multiple

be done within a single

organizations.

organization.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 10/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Work Off-Site at a Satellite

No. In a

Yes, in a connected Workshare

Site?

projects/Workshare

configuration (without projects),

scenario, claim records

work can continue when the

are stored in the P&ID

database link goes down.

schema at the host site. If Standalone Workshare does not the database link goes

require any database connections.

down, claimed items at the

satellite site will not

recognize the claim status.

However, the claim status

of newly placed items will

be recognized when the

database link is re-

established.

When to Use?

When the work to be done When the work to be done must must be divided into

be divided into subsets and

subsets, but it is all done

assigned to different

by the same organization

organizations.

and can use the same

server.

When the subsets of work must

be done on servers that are

When an As-Built facility

physically separated.

model is to be built and

the changes to that model

need to be managed.

When a master database

is to be used for the

approved design and a

task database is to be

used for the ongoing

design work.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 11/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Sample Workshare with Projects Workflows**

The following scenarios provide example workflows for using connected Workshare with projects:

Scenario 1: Compare

Scenario 2: Loops

Scenario 3: OPCs

**Scenario 1: Compare**

The following workflow demonstrates how to compare drawings in a connected Workshare collaboration using projects.

**1**

Project 1 checks out Drawing A.

Project 1 assigns ownership of Drawing A to

Satellite 1.1.

**2**

Project 2 fetches Drawing A from Project 1.

**3**

Project 2 assigns ownership of Drawing A to

Satellite 2.1.

**4**

Satellite 2.1 opens, claims items, and

modifies Drawing A.

Drawing A becomes Drawing A’.

Satellite 2.1 exits Drawing A’.

**5**

Satellite 2.1 assigns ownership of Drawing A’

to Project 2.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 12/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**6**

Satellite 1.1 opens, claims items, and

modifies Drawing A.

Drawing A becomes Drawing A’’.

Satellite 1.1 releases claims and exits

Drawing A’’.

**7**

Satellite 1.1 assigns ownership of Drawing A’’

to Project 1.

**8**

Project 1 checks Drawing A’’ into the Plant.

**9**

Project 2 checks out Drawing A’’ (without

replacing Drawing A’).

**10**

Project 2 compares Drawing A’’ (modified in

Project 1) with its own Drawing A’.

**11**

Project 2 refreshes Drawing A’ with

differences from Drawing A’’.

Drawing A’ becomes Drawing A’’’.

**12**

Project 2 checks Drawing A’’’ in to the Plant.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 13/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Scenario 2: Loops**

The following workflow demonstrates using shared items in a connected Workshare collaboration using projects.

**1**

The Plant creates Drawing A and places 3

DCS instruments.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 14/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**2**

Project 1 checks out Drawing A and creates

the following loops:

P-100 in the drawing stockpile

P-101 in plant stockpile (shared = False)

P-102 in plant stockpile (shared = True)

Project 1 verifies via the EDE that there are 3

DCS instruments and 3 loops in the drawing.

**3**

Project 1 closes Drawing A.

Drawing A becomes Drawing A’.

**4**

Project 2 fetches (with read/write

permissions) Drawing A’ from Project 1.

Project 2 opens Drawing A’ and verifies via

the EDE that P-100 is in the drawing stockpile

and that there are 3 DCS instruments, then

closes Drawing A’.

Project 2 assigns ownership of Drawing A’ to

Satellite 2.1 and synchronizes shared items.

**5**

Satellite 2.1 executes Get Latest Version from

Remote command and synchronizes shared

items.

Satellite 2.1 opens Drawing A’ and verifies via

the EDE that P-100 is in the drawing stockpile

and that there are 3 DCS instruments, then

closes Drawing A’.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 15/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**6**

Project 1 assigns ownership of Drawing A’ to

Satellite 1.1 and synchronizes shared items.

Satellite 1.1 executes Get Latest Version from

Remote command and synchronizes shared

items.

Satellite 1.1 opens Drawing A’ and verifies via

the EDE that P-100 is in the drawing stockpile

and that there are 3 DCS instruments, then

closes Drawing A’.

**7**

Satellite 1.1 creates Drawing B and places an

instrument. Drawing B becomes Drawing B’.

**8**

Satellite 1.1 opens Drawing B’, verifies via the

EDE that only the P102 loop tag is available

for assignment (confirming that synchronizing

shared items brought the loop over to the

satellite), then closes Drawing B’.

**9**

Satellite 2.1 creates Drawing C and places an

instrument. Drawing C becomes Drawing C’.

**10**

Satellite 2.1 opens Drawing C’, verifies via the

EDE that only the P102 loop tag is available

for assignment (confirming that synchronizing

shared items brought the loop over to the

satellite), then closes Drawing C’.

**11**

Satellite 1.1 assigns ownership of Drawing A’

to Project 1 and synchronizes shared items.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 16/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**12**

Project 1 executes Get Latest Version from

Remote command and synchronizes shared

items.

Project 1 opens Drawing A’ and verifies the

following via the EDE:

P-100 in the drawing stockpile

P-101 in plant stockpile (shared = False)

P-102 in plant stockpile (shared = True)

## 3 DCS instruments

Project 1 closes Drawing A’ and then checks

Drawing A’ into the Plant.

**13**

The Plant opens Drawing A’ as read-only and

verifies via the EDE that P-100 is in the

drawing stockpile and that there are 3 DCS

instruments.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 17/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Scenario 3: OPCs**

The following workflow demonstrates handling OPCs in a connected Workshare collaboration using projects.

**1**

Project 1 checks out Drawing A from the

Plant.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 18/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**2**

Project 1 checks out Drawing B from the

Plant.

**3**

Project 1 assigns ownership of Drawing B to

Satellite 1.1.

**4**

Project 1 checks out Drawing C from the

Plant.

**5**

Project 1 assigns ownership of Drawing C to

Satellite 1.1.

**6**

Project 1 opens Drawing A, places OPC-100,

sends the partner OPC-100 to Drawing B,

and closes the drawing.

Drawing A becomes Drawing A’.

**7**

Project 1 synchronizes shared items with

Satellite 1.1.

**8**

Satellite 1.1 synchronizes shared items.

**9**

Satellite 1.1 opens Drawing B, places partner

OPC-100 from the drawing stockpile, and

closes the drawing.

**10**

Project 1 synchronizes shared items with

Satellite 1.1, then opens Drawing A’ and

verifies that “to drawing” name in the OPC

label is updated with information from

Drawing B.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 19/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Drawing A’ becomes Drawing A’’.

**11**

Project 2 fetches Drawing A’’ and assigns

subscription access to Satellite 2.1.

**12**

Satellite 2.1 opens drawing A’’ and verifies

that the OPC label is updated with

information from Drawing B, then closes

Drawing A’’.

**13**

Project 1 assigns ownership of Drawing A’’ to

Satellite 1.1 and synchronizes shared items.

Satellite 1.1 gets latest version of Drawing A’’

and synchronizes shared items.

Satellite 1.1 opens Drawing A’’ and verifies

that the “to drawing” name of OPC-100 is

updated, then closes Drawing A’’.

**14**

Satellite 1.1 opens Drawing B, deletes OPC-

100 to the Plant stockpile, then closes the

drawing.

**15**

Satellite 1.1 opens Drawing C, places OPC-

100 from the Plant stockpile, then closes the

drawing.

**16**

Satellite 1.1 assigns ownership of Drawing A’’

to Project 1 and synchronizes shared items.

**17**

Project 1 gets latest version from remote and

synchronizes shared items.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 20/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Drawing A’’ becomes Drawing A’’’.

**18**

Project 1 opens Drawing A’’’ and verifies that

the graphical label in OPC-100 contains the

correct information and that the data relating

to OPC-100 and its partner is correct in the

EDE, then closes the drawing.

**19**

Project 2 fetches Drawing A’’’ from Project 1.

Project 2 opens Drawing A’’’ and verifies that

the graphical label in OPC-100 contains the

correct information and that the data relating

to OPC-100 and its partner is correct in the

EDE, then closes the drawing.

Project 2 publishes and assigns subscription

access for Drawing A’’’ to Satellite 2.1, then

synchronizes shared items.

**20**

Satellite 2.1 gets latest version, subscribes to

the updated Drawing A’’’, and synchronizes

shared items.

Satellite 2.1 opens Drawing A’’’ and verifies

that the graphical label in OPC-100 contains

the correct information and that the data

relating to OPC-100 and its partner is correct

in the EDE, then closes the drawing.

In a standalone Workshare collaboration, the satellite site needs only to be given subscribe access to a drawing in order to access items (for example, OPCs) in the Plant stockpile.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 21/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 22/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Networking for Connected Workshare**

All connected Workshare collaborations require a live network connection to the host. To use connected Workshare over the network, you need to set up an Oracle Net Services environment where an Oracle database link can be established. The diagram below describes one possible intranet Workshare collaboration.

This environment can exist behind a firewall or, if you need to cross a firewall, it can exist by using a Demilitarized Zone (DMZ) at each site or by setting up a Virtual Private Network (VPN) tunnel to each site. Both of these options require that the IP addresses and port numbers remain static, unless you use Oracle’s Connection Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 23/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Ultimately, the decision about how to establish the networking and database environments must be made on a case-by-case decision based on the purpose of the connected Workshare collaboration, the security needs of the companies involved, and the expertise of the networking personnel.

The following sections discuss using a DMZ vs. a VPN and provide sample configuration diagrams.

**Workshare and Firewalls**

The following sections discuss the available networking technologies for establishing a connected Workshare collaboration in a firewall environment using either a Demilitarized Zone (DMZ) or Virtual Private Network (VPN) solution. Most corporate network firewalls have the ability to create a DMZ environment. A VPN solution can be implemented using Microsoft Windows® Server 2003; however, there are other hardware- and software-based VPN

solutions. Regardless of which firewall environment you configure, Smart Engineering Manager and Smart P&ID use Oracle Net connections to communicate with Oracle databases.

**Demilitarized Zone (DMZ)**

A DMZ places certain ports on your database server outside the firewall to allow communication over the Internet with other sites. When using a DMZ network implementation, https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 24/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

the servers placed outside the firewall can be locked down so that only a single IP address and one port for Oracle communication (port 1521) is allowed to communicate across the Internet to transfer data between the Oracle databases at the host and satellite sites.

Communication between the host and satellite sites transfers data only between each other.

With the proper firewall rules established, no other IP addresses are allowed on the connection.

In a DMZ environment, the Oracle server must reside outside the company’s domain.

**Virtual Private Network (VPN)**

A VPN can be used to enhance your data protection between sites by using packet encryption to further protect information as it is sent from and received at your network. A VPN can be set up using several different encapsulating protocols (for example, IPSec, L2TP, PPTP, or L2F) that wrap a protective encrypted packet around the data during the transfer between the host and satellite sites. In essence, this creates a virtual Local Area Network (LAN) between the host and satellite locations. Each computer participating in the VPN can be isolated so that no other computers on your corporate LAN are visible to the opposite site.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 25/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**DMZ vs. VPN**

The following questions should be considered before determining which networking environment you will use for creating and maintaining a database link between sites.

**Will the Smart P&ID connected Workshare collaboration need share-level access to** **update or synchronize plant and reference data files?**

If share-level access is used to update or synchronize plant and reference data for a company-internal plant between two or more company locations, then a corporate WAN

connection for this process is recommended.

If the connected Workshare collaboration is between different companies, a DMZ

environment is a better solution. If a DMZ solution is used, performing a manual update of the plant and reference data will be required as share-level access in a DMZ

environment is not recommended.

**What are the corporate firewall policies for customers or vendors that need access to** **data inside your corporate LAN?**

If customer or vendor access is not a possible solution for access to data inside your corporate firewall, a DMZ environment is the recommended solution.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 26/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**What if I have a secure VPN established between my location and the satellite location** **for a connected Workshare collaboration?**

If this environment is available, then we recommend share-level access for project and reference data updates and synchronization.

**What ports need to be open for database access in a DMZ environment?**

Port 1521 needs to be opened between the database servers at each location if the databases are using USE_SHARED_SOCKET to lock Oracle into using the single port for operation.

If USE_SHARED_SOCKET is not used, then all ports between the two locations must be open because Oracle uses random ports to communicate after the initial connection.

If both locations use Oracle Enterprise Edition, you can use Connection Manager to handle port connection between the databases at each location.

**Isolating Network Clients in a DMZ Environment**

All Smart P&ID clients inside the LAN that must access the database server in the DMZ can be isolated on their own sub-network (subnet). Doing this restricts their connections so that they can communicate only with other Smart P&ID clients, the Smart P&ID file server, the Smart Engineering Manager Server, and the Oracle database being used for the project.

To allow access rights on Smart Engineering Manager and file servers if a domain controller is not available, you need to establish a workgroup with local user accounts on the isolated subnet on the LAN.

**Subnet Addressing**

Two computers belonging to the same subnet do not require an external server (such as DNS

or Gateways) to exchange data. This example demonstrates how to determine which IP

addresses are considered in your subnet and which ones will not pass through the gateway.

Subnet masks work bitwise and by using a mask.

For example, the following three computers have the following assigned IP addresses: **A**: 192.168.1.1

**B**: 192.168.0.127

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 27/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**C**: 192.168.3.1

If **A**’s subnet is set to 255.255.254.0, then **B** is part of **A**’s sub-network.

Sub-network:

192.168.1.1 and 255.255.254.0 = 192.168.0.0

192.168.0.127 and 255.255.254.0 = 192.168.0.0

Because both **A** and **B** addresses are the same bitwise after using the subnet mask, both **A** and **B** are considered on the same subnet.

However, **C** is not part of the same sub-network: 192.168.3.1 and 255.255.254.0 = 192.168.2.0

**Using a Router to Segment Computers**

LAN segments can be interconnected by routers to enable communication between LANs.

Routers allow blocking of other types of traffic while also implementing broadcast filters and logical firewalls.

Routers offer the following benefits in LAN segmentation: **Media Transition**

Routers are used to connect networks of different media types, taking care of the Layer 3

address translations and fragmentation requirements.

**Packet Filtering**

Routers can filter packets either inbound or outbound between LAN segments or LAN and WAN segments.

**VLAN Communications**

Routers remain vital for switched architectures configured as logically defined virtual workgroups (VLANs) because they provide the communication between VLANs.

**Using a Switch to Segment Computers**

Switches are data link layer devices that enable multiple physical LAN segments to be interconnected into a single larger network. Switches forward and flood traffic based on MAC

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 28/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

addresses and are significantly faster because switching is performed in hardware instead of in software. Switches use either store-and-forward switching or cut- through switching when forwarding traffic.

Segmenting shared-media LANs divides the users into two or more separate LAN segments, reducing the number of users contending for bandwidth.

Switches have the intelligence to monitor traffic and compile address tables, which then allows them to forward packets directly to specific ports in the LAN. Switches also usually provide non-blocking service, which allows multiple conversations (traffic between two ports) to occur simultaneously.

LAN switches can be used to segment networks into logically defined virtual workgroups (VLANs). This logical segmentation, commonly referred to as VLAN communication, offers a fundamental change in how LANs are designed, administered, and managed. Logical segmentation provides substantial benefits in LAN administration, security, and management of network broadcast across the enterprise.

**Sample DMZ Environment Configurations**

The following general items should be considered when establishing a DMZ configuration.

Use a single network-ready computer with only one assigned IP address. No other networking connection should be allowed to a DMZ system (no backdoors).

Install and maintain virus scanning software on the NIC system.

Load and maintain all current operating system security patches.

Load and maintain all current application security patches.

Limit access from the Internet node (for example, a satellite site) to allow only the functions needed for Workshare. For example, telnet access is not needed for a system whose function is to be a host database server.

Grant full access from internal networks to the computer in the DMZ.

Limit access from the computer in the DMZ to the Internet to allow only those functions needed for Workshare.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 29/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Block access from the computer in the DMZ to internal networks. Only for special cases should holes be made to allow access from a DMZ to an internal system (for example, SQL authorization from a web server in the DMZ to an internal domain controller).

In the configuration below, Smart Engineering Manager and Drawing Manager reside inside the LAN behind the firewall to allow domain users and groups to be added to the Roles section in Smart Engineering Manager. This configuration allows domain users to authenticate against the local domain. The DMZ firewall rules need to be set up for the Smart Engineering Manager server on the LAN to allow access to the satellite database and the host database via an Oracle alias for the satellite database. At the satellite site, a database link needs to be created and pointed to the database at the host. This link allows the satellite database to connect to the host database and subscribe to a satellite slot.

In a DMZ environment, the Oracle server must reside outside the company’s domain.

The only communication between the host and the satellite databases is through the database link. There is no need to create a database alias from any satellite clients to the host.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 30/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Sample VPN Environment Configuration**

In the sample VPN configuration below, the database, Smart Engineering Manager, and Drawing Manager reside behind the firewall. A secure and encrypted tunnel is established between the host site and the satellite location. The database servers at both sites can be isolated on their own subnet at each location with rules applied to each firewall so that only these computers are visible in the VPN. This way, no other computer on a site’s LAN is accessible.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 31/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

The server containing Smart Engineering Manager, Drawing Manager, and the database resides in an isolated subnet separate from the Smart P&ID computers. Only the isolated subnet at each site is visible to the other site. The visible computers between locations and firewall rules for the connection are defined in the VPN.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 32/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Configuring Oracle for Connected Workshare**

If you have not already installed Oracle, use the instructions under Oracle Installation and Configuration in the *Smart P&ID*  Installation and Upgrade Help to install and configure your database, then complete the following steps to configure your Oracle database for Workshare.

1. Create a global name for your database, if it was not created during database

installation. See Enable Oracle Global Naming.

1. Add a **USE_SHARED_SOCKET** registry key to

HKEY_LOCAL_MACHINE\SOFTWARE\ORACLE\HOME0 to lock Oracle into using a single port. This key tells Oracle to use port 1521 for all Oracle communications to and from the database in the DMZ or VPN environment instead of using random ports after the initial communication connection (that is, the first time the database link is connected). See Lock Oracle into Using a Static Port.

Create the database link from the satellite database server to the host database server. See

Create the Database Link.

**Enabling Oracle Global Naming**

Before you can create a database link, you must define the Oracle global database name **global_names** parameter at the host and at each satellite database site. The global database name is the full name of the database and uniquely identifies it from any other database.

The global database name is either in the form *database_name.database_domain* for a VPN

or *database_name* for a DMZ, where *database_name* is the database name, and the *database_domain* is the fully qualified domain name where the database is located. For example, if the *database_domain* is myserver.b30.ingr.com and *myserver* has a database named hostbeta, then the **global_names** parameter should be set to hostbeta.myserver.b30.ingr.com for a VPN or to hostbeta for a DMZ.

The global database name should have been defined during database installation and configuration. To verify that the global database name is properly defined, be sure the **global_names** and **db_domain** parameters are set properly. To determine the current global database name, run the following SQL statement: select * from global_name;

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 33/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Enable Oracle Global Naming**

1. Use SQL Plus to connect to the database and then run one of the following SQL

statements:

ALTER DATABASE RENAME global_name TO

*database_name.database_domain*; (for a VPN)

ALTER DATABASE RENAME global_name TO *database_name*; (for a DMZ) 2. For a VPN only, set the **db_domain** parameter to match the *database_domain* above.

1. Set the **global_names** parameter to be **TRUE**. This setting is required for **all** databases used in the connected Workshare process.

**Locking Oracle into Using a Static Port**

To lock Oracle into using a single port for operation, add a **USE_SHARED_SOCKET** key to the Registry as described in the steps below. This key tells Oracle to use port 1521 instead of using random ports after the initial communication connection (that is, the first time the database link is connected).

You do not need to create this key if you are using Workshare within a single network domain (LAN) because you will not have a port availability problem.

You must add this **USE_SHARED_SOCKET** key to the Registry on the Oracle server and on each Oracle client computer.

**Lock Oracle into Using a Static Port**

1. Select **Start** > **Run**, type **regedit**, and then browse to the **HKEY_LOCAL_MACHINE\SOFTWARE\ORACLE\HOME0** registry location.
2. Select the **HOMEO** folder, and then right-click and select **New** > **String Value**.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 34/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

If you have more than one Oracle instance, you can have multiple Oracle HOMES. In this case, be sure to select the HOME<#> folder that corresponds to the database instance being used for Workshare.

1. Type **USE_SHARED_SOCKET** for the name of the new string value.
2. Select the new string variable, right-click and select **Modify**.
3. On the **Edit String** dialog, type **True** in the **Value data** field and then select **OK**.

**Understanding the Database Link**

The database link is a network object stored in the local database that identifies a remote database, a communication path to that database, and optionally, a user name and password.

After it is defined, the database link is used to access the remote database and is vital to a successful connected Workshare collaboration.

Configuring a database link is not necessary for standalone Workshare collaboration.

**Plant Schema**

The database link allows each satellite to view all plant data in the plant schema. When you are at a satellite and are viewing the plant schema over an active database link, you are actually viewing the database at the host site. This plant schema, containing the data available at the time of the last reference data synchronization, is replicated at each satellite, to be used by the satellite in the event the database link is not active.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 35/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

The Smart P&ID Modeler always uses the local replication plant schema, even when the database link is up. All other Smart P&ID applications use the host plant schema when the link is up.

Drawing Manager dynamically changes both the host and replication schemas when adding new drawings. All drawing-level changes are reflected in both schemas when the change is made at the satellite, allowing the Smart P&ID Modeler environment to be aware of new drawings created locally without having to synchronize reference data.

**Drawing Transfer**

The transfer of published drawings takes place automatically over the database link, rather than you having to manually bundle and transmit the data to the satellites.

**Reference Data Synchronization**

The reference data consists of data in the file system and data in the plant and P&ID

schemas. Because only the Workshare host has permission to modify the reference data, the updated reference data must be shared with all satellites whenever the reference data is modified. Satellites cannot publish drawings or get the latest version of drawings until the satellite site reference data is in sync with the host.

The file system reference data (rules file, symbol files, and so forth) must be transmitted manually to satellite sites no matter the mode of Workshare collaboration. However, in a connected Workshare collaboration, the database portion (plant and application schemas) of the reference data is synchronized via the database link.

**Shared Items Synchronization**

Shared items are defined as OPCs, utility connectors, shared instrument loops, and package systems. These items are referred to as “shared items” because they are designed to intelligently cross drawing boundaries. If one or more of these items crosses the boundary https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 36/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

from one drawing to another drawing at another connected Workshare site, the **Synchronize** **Shared Items** command uses the database link to maintain data for the shared items at each site.

**Create the Database Link**

1. On the host database server, use Oracle Net Manager to create a net service name for the host database (for example, set the name to **hostbeta**).
2. On the satellite database server, use Net Manager to create a net service name for both the satellite database and the host database. The net service name at the satellite site must match the net service name at the host site.

The database server at the host or satellite site usually has two IP

addresses, one for internal and the other for external use. The database server (either the host or the satellite) should open to the IP addresses of the database servers of the other sites.

1. Connect to the satellite database using the SQLPLUS Utility or the SQL Developer Utility on the satellite server.
2. To create the database link, refer to Oracle documentation for dblink.

The database link should be created with the **Connected User** option. Defined in this manner, the database link user does not automatically inherit DBA privileges, but rather the database link user privileges are determined at runtime when the link is accessed by the connected user. If the connected user has credentials at the destination of the link, then those credentials determine what actions are possible via the database link with respect to the destination or remote database.

Another option is to create a special user with system **Create Database Link** privileges and then use this special user to create the database link. However, when the database link is defined with the **Connected User** option, the application will have the same privileges as if the database link were created using a system account.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 37/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Breaking the Database Link: The Significance**

If the database link is unavailable, the connected Workshare collaboration can continue, but is not recommended. If you do proceed with the connected Workshare collaboration while the database link is down, the following limitations apply.

**Projects**

At connected project satellites, all claim operations (claim and unclaim) are persisted at the host and the local satellite database in case the database link is disconnected. While the database link is down, the local claim information is used and all items that were previously claimed are still known to be claimed. As new items are created, they are automatically claimed and this information is stored locally. Pre-existing items cannot be claimed or unclaimed. In other words, the claim state of pre-existing items is frozen.

When the database link is re-established, the local claim information is automatically synchronized with the host claim information and all claim operations are allowed. This automatic synchronization occurs during the first Smart P&ID session initiated after the database link is restored.

**Plant Schema**

The Smart P&ID Modeler always uses the local replication plant schema, even when the database link is up. All other Smart P&ID applications use the host plant schema when the link is up.

Drawing Manager dynamically changes both the host and replication schemas when adding new drawings. All drawing-level changes are reflected in both schemas when the change is made at the satellite, allowing the Smart P&ID Modeler environment to be aware of new drawings created locally without having to synchronize reference data.

**Drawing Creation**

New drawings cannot be created when the database link is down because drawing name and number uniqueness must be checked against the host schema.

When the database link is down, we recommend not using Drawing Manager to open drawing files because Drawing Manager still attempts to use the database link. Instead, run Smart P&ID directly and use the **File** > **Open** command to open a drawing when the database link is down.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 38/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Drawing Transfer**

Publishing drawings, giving ownership or subscribe access, taking ownership, and subscribing activities are not available when the database link is inactive.

**OPC Placement**

When the database link is inactive, you can place OPCs in drawings at your site, but you cannot assign the mates to drawings located in other sites. For example, when you place an OPC on your drawing when the database link is down, the mate OPC is assigned to the local plant stockpile. When the database link is reactivated, you can then move the mates to the drawing stockpiles at other sites.

**Reference Data Synchronization**

The reference data cannot be synchronized when the database link is inactive.

The satellite can add, modify, and delete the contents of drawings that they owned at the time the reference data was last synchronized with the host. The satellite cannot, however, delete or rename such drawings until the database link is re- established. Therefore, reference data should be synchronized on a regular/frequent basis.

**Shared Items Synchronization**

Shared items cannot be synchronized when the database link is inactive.

**Local Model Item Lookup Table Utility**

Use the LocalModelItemLookupTable.sql utility if your connected Workshare satellite experiences performance problems when transferring piping data from Smart P&ID to PDS.

This script converts a satellite database view (namely, the T_ModelItemLookup) that references a host table into a local table, allowing the data transfer to proceed without using a database link.

Smart P&ID uses the database link to fetch unique Long IDs from the Host when running from a connected Workshare satellite. If the performance of opening the PID file in PDS is an issue or if maintaining the correlation between Smart P&ID and PDS after the merge is not an issue, then you can run this script to change the lookup for the Long ID from a view to the host to a local query.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 39/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

This utility is delivered as an SQL script to the ..\SmartPlant\P&ID Workstation\bin folder and can be executed using any Oracle user interface, such as SQLPlus.

Do not use this script if the transferred PDS data will be merged back into a host PDS

database because the Long IDs will not be unique at the host.

For more information about Workshare and database links, see the Workshare Configuration and Reference Help.

For more information about transferring piping data, see the Smart P&ID Piping Data Transfer Configuration and Reference Help.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 40/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Configuring Workshare**

Whether you are using connected or standalone Workshare, you must complete the following tasks at the host and satellite sites:

1. Enable the host site for Workshare.
2. Create satellite slots at the host site.
3. Configure the satellite site.
4. Subscribe to a satellite slot from the satellite site.

If you are using connected Workshare, you must configure your network and establish a database link before configuring the host and satellite sites.

**Configuring the Host Site**

To configure the host site for Workshare, you must do the following: 1. Enable the plant structure for Workshare

1. Create satellite slots.
2. Manually transmit the Workshare password, satellite template (.sat) files, and reference data, if it has been modified, to the satellite sites via e-mail, network share, CD, or other means.

Prior to enabling Workshare, you must have already created a site and plant structure, associated the Smart P&ID application with the plant structure, and defined user access rights for the Smart P&ID application.

**Enabling Workshare**

Before you can share data between the host and satellite sites, you must use Smart Engineering Manager to activate Workshare at the host site for each plant structure that you plan to share.

When you enable Workshare, you are asked to select the publishing method to be used between the host and the satellite for the selected plant structure. Each plant structure can https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 41/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

use either the database publishing or the file sharing method.

After Workshare is enabled for the selected plant structure, the **Satellites** node is added to the plant structure node.

You must have Smart P&ID associated with your plant before you can access the **Enable Workshare** command.

**Enable Workshare**

1. Select the plant structure in which you want to create a Workshare collaboration.
2. Right-click and select the **Enable Workshare** command.
3. Enter the requested information on the **Enable Workshare** dialog.

You must enable each plant structure for Workshare separately.

**Enable Workshare Command (Workshare Menu)**

Allows you to enable Workshare for the plant structure or project using the **Enable** **Workshare** dialog. The **Enable Workshare** command is disabled unless you have Smart P&ID associated with your plant and you have selected a plant structure in the **Plant** **Structures** node.

For information about enabling Workshare while using projects, see Using Workshare with

Projects.

For information about enabling Workshare while working in an integrated environment, see Using Workshare in an Integrated Environment.

**Enable Workshare Dialog**

Allows you to activate Workshare for the plant structure.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 42/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Workshare name**

Type a name for the plant being enabled for Workshare. This name will be seen by the satellite site/location.

**Publishing method**

Select the publishing method to be used to share data contained in the plant.

**Database**

Recommended) Published files are stored in the database as Oracle blobs at the host.

Oracle database links are used to transfer published files between host and satellites.

**File share**

Published files are stored on a file share at either the host or satellite site.

**Publish location**

Type a UNC path to the shared location on the host site where the published drawings are to be stored. The default location is the **WsPublish** folder in the plant folder. This field is limited to 255 characters.

The name cannot contain any of the following characters: ’ % ”

Location paths cannot contain any of the following characters: ~ ` ! % * ( ) { } [ ] / ; : ’ ” <

> , ? |
> 

For standalone Workshare mode, the **File share** publishing method must be selected.

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 43/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

**Creating Satellite Slots**

After enabling Workshare, the host site must create a satellite slot to which the satellite site can subscribe. Satellite slots appear in the **Satellites** node inside the plant structure in the **List** view.

**Create a New Satellite Slot**

1. Select the **Satellites** node in the plant structure in which you want to create a satellite slot.
2. Select **File** > **New**.
3. Follow the prompts in the New Satellite Slot Wizard.
4. Send the Workshare password, the satellite template (.sat) file, and reference data, if it has been modified, to the satellite sites via e-mail, file sharing, floppy disk, CD, or other means.

If the **Satellites** node does not appear in the plant structure node, you must enable the plant for Workshare before you can create a satellite slot.

**New Satellite Slot Wizard**

Steps you through creating satellite slots in the host plant. You must enable the plant structure for Workshare before you can create a satellite slot.

To start the wizard, select the **Satellites** node in the plant structure in which you want to create a satellite slot, right-click and select** New Satellite**.

**Type and Name (New Satellite Slot Wizard)**

Allows you to define the unique name and password for the satellite slot. The password is used as a key of sorts so that only the correct remote site can connect to the satellite slot at https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 44/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

the master plant structure. An asterisk (*) means a value is required for that box.

**Workshare satellite type**

Select the type of Workshare collaboration for this new satellite slot: **Connected**

Specifies that this satellite slot will use a database link and will collaborate through an Oracle database.

**Standalone**

Specifies that this satellite slot will not collaborate through a database. This type of Workshare collaboration allows the host and satellite to use different databases locally.

**Workshare name**

Use the default name provided or type a name for this satellite slot. This name is used as the name of the slot in the **Satellites** node and must be unique per satellite slot. The name cannot contain any of the following characters: ’ % ”

**Workshare password**

Type a password for the satellite slot. The password is case-sensitive. This password will be needed by the user at the remote site who will be connecting to this satellite slot, and can be https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 45/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

changed later if desired.

**Confirm password**

Re-type the password.

Be sure to make a note of this password because there is no way to retrieve it if you forget it. You must delete and re-create the satellite slot if you forget the password that you set here.

**Connected Workshare (New Satellite Slot Wizard)**

Allows you to specify combinations of users for a connected Workshare satellite slot. These database users can be the same as or different from the users at the host plant structure or any combination thereof.

**Satellite will exist in the same Oracle instance** Select this option if you want the satellite users to exist in the same Oracle instance as the host plant structure. This option is usually used only when Workshare is implemented internally and not across different geographic locations. In this situation, the host and satellite sites will reside in the same database instance. The individual user options below are disabled when this option is selected because the satellite slot user names cannot be identical to the host user names in the same Oracle instance. When this option is selected, you are prompted to define the satellite user names (proxy user names) on subsequent pages in this wizard.

**Plant schema users identical**

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 46/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Select this option if you want to use the same users for the satellite schema that are used for the host plant schema.

**Data dictionary users identical**

Select this option if you want to use the same users for the satellite data dictionary that are used for the host plant data dictionary.

**Smart P&ID schema users identical**

Select this option if you want to use the same users for the satellite Smart P&ID schema that are used for the host plant Smart P&ID schema.

**Smart P&ID data dictionary users identical**

Select this option if you want to use the same users for the satellite Smart P&ID data dictionary that are used for the host plant Smart P&ID data dictionary.

**Plant Schema (New Satellite Slot Wizard)**

Allows you to define the plant schema user name for the satellite. This page does not display if the Plant schema users identical option is selected on the Location page. An asterisk (*) means a value is required for that box.

**Plant schema username**

Type the user name you want to use for the satellite plant schema. See Understanding Default Database User Names.

**Database password**

Type the password for the satellite plant schema.

**Confirm password**

https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 47/125

3/19/25, 10:38 AM

Hexagon Documentation Site Export

Re-type the password for the satellite plant schema.

The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
**Plant Data Dictionary (New Satellite Slot Wizard)** Allows you to define the plant data dictionary user name for the satellite. This page does not display if the **Data dictionary users identical** option is selected on the **Location** page. An asterisk (*) means a value is required for that box.
**Plant data dictionary username**
Type the user name you want to use for the satellite plant data dictionary. See Understanding Default Database User Names.
**Database password**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 48/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Type the password for the satellite plant data dictionary.
**Confirm password**
Re-type the password for the satellite plant data dictionary.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names using the formulas above.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
**Smart P&ID Schema (New Satellite Slot Wizard)** Allows you to define the Smart P&ID schema user name for the satellite. This page does not display if the **Smart P&ID schema users identical** option is selected on the **Location** page.
An asterisk (*) means a value is required for that box.
**Smart P&ID schema username**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 49/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Type the user name you want to use for the satellite Smart P&ID schema. See Understanding Default Database User Names.
**Database password**
Type the password for the satellite Smart P&ID schema.
**Confirm password**
Re-type the password for the satellite Smart P&ID schema.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
**Smart P&ID Data Dictionary (New Satellite Slot Wizard)** Allows you to define the Smart P&ID data dictionary user name for the satellite. This page does not display if the **Smart P&ID** **data dictionary users identical** option is selected on the **Location** page. An asterisk (*) means a value is required for that box.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 50/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Smart P&ID data dictionary username**
Type the user name you want to use for the satellite Smart P&ID data dictionary. See Understanding Default Database User Names.
**Database password**
Type the password for the satellite Smart P&ID data dictionary.
**Confirm password**
Re-type the password for the satellite Smart P&ID data dictionary.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 51/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Finish (New Satellite Slot Wizard)**
Displays all the settings that you have defined to create the new satellite slot. Review these settings carefully. If you are satisfied with the settings, select **Finish**. Otherwise, select **Back** to change one or more of the settings.
After creating the satellite slot, send the Workshare password, the satellite template (.sat) file, and reference data, if it has been modified, to the satellite sites via e-mail, file sharing, floppy disk, CD, or other means.
**Satellite Slot Properties Dialog**
Allows you to view the properties for the selected satellite slot. The tabs, and the options on those tabs, displayed differ depending on the Workshare mode and use status for each satellite slot.
Data Access Tab
Proxy Users Tab
Standalone Slot Properties Tab
**Data Access Tab (Satellite Slot Properties Dialog)** Displays the data access information for the satellite slot. This tab displays only when a connected satellite site is using the slot.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 52/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Workshare name**
Displays the name of the satellite slot. You cannot change the satellite slot name after the satellite slot has been created.
**Workshare type**
Displays the type of Workshare mode for the satellite slot.
**Owned drawings**
Displays the number of drawings currently owned by the satellite connected to this slot.
**Proxy Users Tab (Satellite Slot Properties Dialog)** Displays the user names defined for the satellite proxy users. This tab displays only when a connected satellite site is using the slot.
**Plant schema username**
Displays the user name defined for access to the plant schema.
**Plant data dictionary username**
Displays the user name defined for access to the plant data dictionary.
**Smart P&ID schema username**
Displays the user name defined for access to the Smart P&ID schema.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 53/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Smart P&ID** **data dictionary username**
Displays the user name defined for access to the Smart P&ID data dictionary.
**Standalone Slot Properties Tab (Satellite Slot Properties Dialog)** Displays the data access information for the satellite slot. This tab displays only for standalone satellite slots.
**Workshare name**
Displays the name of the satellite slot. You cannot change the satellite slot name after the satellite slot has been created.
**Workshare type**
Displays the type of collaboration this satellite slot allows.
**Owned drawings**
Displays the number of drawings currently owned by the satellite.
**Configuring a Satellite Site**
Prior to configuring the satellite site for Workshare, you should have already created a site using Smart Engineering Manager at the satellite location. See New Site Server Wizard.
1. At each satellite site, subscribe to a satellite slot at the host site by creating a new Workshare collaboration. The host site must provide you with the Workshare password https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 54/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
and the satellite template (.sat) file for the satellite slot to which you are subscribing.
1. Define user access rights. You must grant at least **Modify Settings** access rights in the **Smart P&ID Options** category.
2. Using Options Manager in Smart P&ID, adjust the starting sequence numbers for the **OPCItemTag**, **EquipNextSeqNo**, **InstrLoopNextSeqNo**, and **PipeRunNextSeqNo** settings to avoid duplicate item numbers.
3. Using Smart P&ID Options Manager, modify the **Export to CAD Definition File** entry by changing .xls to Exportlayer.xlsx.
All satellites use the host plant schemas. During satellite slot creation, the host creates a satellite creation template (.sat) that contains all of the plant schema information needed to create the same schemas at the satellite site. This template file must be sent from the host to the satellite via e-mail, file sharing, floppy disk, CD, and so forth.
If you are working across multiple sites and are using separate database instances, we suggest using the same user names at the satellites that are used at the host so that creating proxy users is not necessary.
New plant groups (plants, areas, units, and so forth) cannot be created by standalone satellites or by satellites hosted by a project.
You cannot create a plant or application data dictionary template at a satellite site. You must create the templates at the host site.
**Subscribe to a Satellite Slot**
1. Open the satellite site in Smart Engineering Manager.
2. Select **Workshare** > **New Collaboration**.
3. Follow the prompts in the **New Workshare Collaboration** wizard.
4. Set the user access rights for the satellite plant.
5. Run Smart P&ID Options Manager and edit the sequence numbers as needed for the satellite site.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 55/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
You cannot create a satellite in the same site as the host site. You must have a separate site for the satellite.
You must obtain the Workshare password from the host site administrator, as it will be needed to complete the **New Workshare Collaboration** wizard.
**New Collaboration Command (Workshare Menu)**
Starts the **New Workshare Collaboration** wizard. To complete the Workshare configuration, the satellite site must subscribe to an available satellite slot at the host site. The **New** **Workshare Collaboration** wizard steps you through the subscription process by using the satellite template, Workshare password, and reference data received from the host site to create a *copy* of the host plant structure.
You cannot create a satellite in the same site as the host site. You must have a separate site for the satellite.
You must obtain the Workshare password and the satellite template from the host site administrator prior to subscribing to a satellite slot.
**New Workshare Collaboration Wizard**
Steps you through subscribing to a satellite slot. This process is much like creating a plant structure, except that the satellite plant is based on a “copy” of the host plant structure instead of being created from scratch. The “copy” information is provided by the host site in the satellite template file. Upon completing this wizard, the satellite is connected to a satellite slot at the host site.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 56/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
You cannot create a satellite in the same site as the host site. You must have a separate site for the satellite.
You must obtain the Workshare password and the satellite template (.sat) file from the host site administrator before you can complete this wizard. Both of these items were created when the satellite slot was created at the host. This information can be sent to you via e-mail, file sharing, floppy disk, or CD.
**Template and Password (New Workshare Collaboration Wizard)** Displays the options for creating the satellite plant structure in the satellite site.
**Oracle alias**
Specifies the Oracle net service alias that allows connection to the Oracle database at the satellite site. This field defaults to the alias specified when the satellite site was created.
**Database node**
Type the node name of the server on which the SQL Server database resides. This option appears only if SQL Server is selected as the database type.
**System user**
Type a database system user name. This name does not have to be the database administrator user name, but this user must have minimum DBA privileges to be able to perform Smart Engineering Manager procedures. See Create Oracle Admin Users with Limited Privileges and Create SQL Server Admin Users with Limited Privileges.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 57/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**System password**
Type a system user password.
Oracle system passwords cannot contain any special characters other than: @ (‘at’
symbol), . (period), and _ (underscore). SQL Server database passwords cannot contain the character: ’.
On an Oracle platform using different instances, when exiting this Wizard page, you might receive a message about having insufficient privileges to create the plant structure, followed by a list of the required privileges. To fix this problem, you must create one or more of these privileges manually using Oracle tools.
**Satellite template**
Type the UNC path or browse to the location where you placed the satellite template file (.sat) received from your host administrator. This field is limited to 255 characters.
**Workshare password**
Type the Workshare password. This password, sometimes called a location key, is specified during the satellite slot creation at the host site. The host administrator must provide you with this password as the key to connecting your satellite with a satellite slot at the host site.
**Template Verification (New Workshare Collaboration Wizard)** Displays the information obtained from the satellite template that is based on the satellite slot information defined at the host site.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 58/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Workshare name**
Displays the name of the satellite slot at the host to which you are connecting.
**Workshare type**
Displays the type of Workshare collaboration available through the satellite slot.
**Plant structure name**
Displays the name of the plant containing the satellite slot.
**Plant structure description**
Displays the available information about the plant containing the satellite slot.
**Paths (New Workshare Collaboration Wizard)**
Allows you to specify a storage folder for the files that the satellite pulls from the host and the paths to the reference data.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 59/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Plant structure path**
Specify the path to the storage location on the satellite server for the plant data and the drawing files. You must create the plant structure share before running this wizard, using the form *\\siteserver\sitename\plantname*. The wizard will create the *plantname* folder if it does not already exist.
**Backup location**
Type, or browse to, the path to the storage location to use when backing up the satellite plant files. We recommend specifying a backup location outside the **Plant structure path** to avoid recursive backups being stored in a single backup file. For example, if the **Plant structure** **path** is *\\siteserver\sitename\plantname*, do not set the backup location for plantname to
*\\siteserver\sitename\plantname\backups*.
**Smart P&ID reference data path**
Type or browse to the path where the reference data is located at the satellite site.
Specify a reference data path outside the plant structure path to avoid duplicate sets of reference data and longer process times when saving or backing up your plant and also to avoid deleting the reference data if you delete the plant. For example, if the **Plant structure path** is \\siteserver\sitename\plantname, do not set the **Smart P&ID**
**reference data path** to \\siteserver\sitename\plantname\refdata.
**Publishing method**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 60/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Select the publishing method to be used to share data contained in the plant: **Database**
(Recommended) Published files are stored in the database as Oracle blobs at the host.
Oracle database links are used to transfer published files between host and satellites.
**File share**
Published files are stored on a file share at either the host or satellite site.
**Publish location**
Type a UNC path to the shared location on the satellite site where the published drawings are to be stored. This field is limited to 255 characters and is available only for standalone satellites or for connected satellites using the file share publishing option.
All paths must use the Universal Naming Convention (UNC) format and are limited to 255 characters per path.
Paths and locations cannot contain any of the following characters: ~ ` ! % * ( ) { } [ ] / ; :
’ ” < > , ? |
**Plant Schema (New Workshare Collaboration Wizard)** Defines the plant schema database information for your new standalone Workshare collaboration. An asterisk (*) at the end of an item name indicates a value is required for that item.
This page displays only when configuring a satellite for standalone Workshare.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 61/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Database type**
Displays the database type used at the satellite site.
**Oracle service/alias**
Displays the Oracle net service alias specified earlier. This option appears only if the satellite site is using Oracle.
**Database server**
Displays the node name of the server on which the SQL Server database resides. This option appears only if SQL Server is used by the satellite site.
**Database name**
Select the name of the SQL Server database where the satellite plant will be created. This option appears only if SQL Server is selected as the database type.
**Oracle tablespace**
Select the default Oracle tablespace name for your satellite plant database. These tablespaces were defined when the database administrator created the default database instance using Oracle Database Assistant. This option appears only if the satellite site is using Oracle.
**Oracle temp tablespace**
Select the default Oracle temporary tablespace name for your satellite plant database. If this list is empty, contact your database administrator. This option appears only if the satellite site is using Oracle.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 62/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
We recommend that you do not use SYSTEM for the default tablespace because Oracle uses this tablespace for its own uses.
If you create new Oracle tablespaces or SQL Server databases after starting this wizard, you must refresh the tablespace list by selecting **Back** and then selecting **Next** to return to this page before the new information will display in the appropriate lists.
**Database username**
Type the user name you want to use for the plant user. This value, which must be unique in the database, defaults to the satellite plant name. See Understanding Default Database User Names.
**Database password**
Type the password for the database user. We recommend using the satellite plant database user name, entered above, as this password.
**Confirm password**
Re-type the password for the database user.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 63/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Plant Data Dictionary (New Workshare Collaboration Wizard)** Allows you to specify the database information for the satellite plant data dictionary. An asterisk (*) at the end of an item name indicates a value is required for that item.
This page displays only when configuring a satellite for standalone Workshare.
**Database type**
Displays the database type used at the satellite site.
**Oracle service/alias**
Displays the Oracle net service alias specified earlier. This option appears only if the satellite site is using Oracle.
**Database server**
Displays the node name of the server on which the satellite SQL Server database resides.
This option appears only if SQL Server is used by the satellite site.
**Database name**
Displays the name of the SQL Server database where the satellite plant will be created. This option appears only if SQL Server is selected as the database type.
**Oracle tablespace**
Select the default Oracle tablespace name for your satellite plant data dictionary. These tablespaces were defined when the database administrator created the default database https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 64/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
instance using Oracle Database Assistant. This option appears only if the satellite site is using Oracle.
**Oracle temp tablespace**
Select the default Oracle temporary tablespace name for your satellite plant data dictionary. If this list is empty, contact your database administrator. This option appears only if the satellite site is using Oracle.
We recommend that you do not use SYSTEM for the default tablespace because Oracle uses this tablespace for its own uses.
If you create new Oracle tablespaces or SQL Server databases after starting this wizard, you must refresh the tablespace list by selecting **Back** and then selecting **Next** to return to this page before the new information will display in the appropriate lists.
**Database username**
ype the user name you want to use for the plant data dictionary user. This value, which must be unique in the database, defaults to satellite plant name with the letter ‘d’ appended. See Understanding Default Database User Names.
**Database password**
Type the password for the plant data dictionary user. We recommend using the satellite plant database user name, entered above, as this password.
**Confirm password**
Re-type the password.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 65/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @ SQL Server database passwords cannot contain the character: ’
**Smart P&ID Schema (New Workshare Collaboration Wizard)** Allows you to enter database information for the Smart P&ID application schema at the satellite site. The tablespaces and other database information displayed in the drop-down lists are based on the information specified on the satellite plant structure creation page. An asterisk (*) means a value is required for that box.
This page displays only when configuring a satellite for standalone Workshare.
**Application to associate**
Displays the application being associated to the satellite plant.
**Schema type**
Displays the application schema type being created.
**Oracle service/alias**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 66/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Specifies the Oracle net service name for the satellite plant database. This value is carried forward from the satellite plant structure definition page and appears only if using Oracle.
**Database server**
Displays the node name of the server on which the satellite SQL Server database resides.
This option appears only if using SQL Server.
**Database name**
Displays the name of the SQL Server database used by the satellite plant to which the application is being associated. This option appears only if using SQL Server.
**Oracle tablespace**
Select the default tablespace name for your application schema. These tablespaces are defined when the database administrator created the default database instance using Oracle Database Assistant.
**Oracle temp tablespace**
Select the default temporary tablespace name for your application schema. The temporary tablespace was defined when the database administrator created the temporary database instance using Oracle Database Assistant. If this list is empty, contact your database administrator.
We recommend that you do not use SYSTEM for the default tablespace because Oracle uses this tablespace for its own use. This option appears only if using Oracle.
If you create new Oracle tablespaces or SQL Server databases after starting this wizard, you must refresh the tablespace list by selecting **Back** and then selecting **Next** to return to this page before the new information will display in the appropriate lists.
**Database username**
Type the user name you want to use for the satellite Smart P&ID database user. This name must be unique in the database. See Understanding Default Database User Names.
**Database password**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 67/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Type the password for the satellite Smart P&ID database user. We recommend using the satellite Smart P&ID user name defined above as this password.
**Confirm password**
Re-type the password.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
**Smart P&ID Data Dictionary (New Workshare Collaboration** **Wizard)**
Allows you to enter database information for the Smart P&ID application data dictionary at the satellite site. The tablespaces and other database information displayed in the drop-down lists are based on the database used in the plant structure creation. An asterisk (*) means a value is required for that box.
This page displays only when configuring a satellite for standalone Workshare.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 68/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Application to associate**
Displays the application being associated to the satellite plant. This value is carried forward from the previous page.
**Schema type**
Displays the schema type being created. This value is carried forward from the previous page.
**Oracle service/alias**
Specifies the Oracle net service name as defined by your database administrator. This value is carried forward from the previous page and appears only if using Oracle.
**Database server**
Displays the node name of the satellite server on which the SQL Server database resides.
This option appears only if using SQL Server.
**Database name**
Displays the name of the SQL Server satellite database used by the satellite plant to which the application is being associated. This option appears only if SQL Server is selected as the database type.
**Oracle tablespace**
Select the default tablespace name for your application data dictionary database. These tablespaces are defined when the database administrator created the default database https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 69/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
instance using Oracle Database Assistant.
**Oracle temp tablespace**
Select the default temporary tablespace name for your application data dictionary database.
The temporary tablespace was defined when the database administrator created the temporary database instance using Oracle Database Assistant. If this list is empty, contact your database administrator. This option appears only if using Oracle.
We recommend that you do not use SYSTEM for the default tablespace because Oracle uses this tablespace for its own use. This option appears only if using Oracle.
If you create new Oracle tablespaces or SQL Server databases after starting this wizard, you must refresh the tablespace list by selecting **Back** and then selecting **Next** to return to this page before the new information will display in the appropriate lists.
**Database username**
Type the user name you want to use for the application data dictionary user. This name must be unique in the database. See Understanding Default Database User Names.
**Database password**
Type the password for the application data dictionary user. We recommend using the application data dictionary user name defined in the field above as this password.
**Confirm password**
Verify the password by retyping it.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 70/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
**Replication Schema (New Workshare Collaboration Wizard)** Allows you to create a replication schema for use when the satellite is working offline. This schema is a replica of the plant schema at the host site. The plant schema is not always replicated, but the plant data dictionary is always replicated.
This page displays only for connected Workshare collaborations.
**Oracle alias**
Specifies the Oracle net service alias that allows connection to the Oracle database at the satellite site.
**Database link**
Select the database link that points to your host database server. The drop-down list displays all available database links on your satellite database server. This option displays only for connected different-instance collaborations.
**Oracle tablespace**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 71/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Select the user tablespace of the Oracle database at the satellite location.
**Oracle temp tablespace**
Select the temporary tablespace of the Oracle database at the satellite location.
**Database username**
Type the user name you want to use for the replication plant user. This name must be unique in the database. See Understanding Default Database User Names.
**Database password**
Type the password for the replication database user. This value defaults to the value in the **Database username** field.
**Confirm password**
Re-type the password for the replication database user. This value defaults to the value in the **Database username** field.
The software sets the related password defaults for the above user name automatically to

for Oracle and to
+ ‘1’ for SQL Server. In the case of SQL Server running on Windows Server, if you are using SQL Server authentication, you can specify that SQL Server is to use the password validation rules that are used by Windows Server.
Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) - + = { } [ ] \ / ; : ‘ ” < > , . ? |
Database user names are limited to 30 characters. Because these are derived from plant names that can be up to 64 characters long, the software truncates any excess characters to the maximum allowed in creating the default database user names.
Oracle database passwords cannot contain the characters: ” ’ @. SQL Server database passwords cannot contain the character: ’
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 72/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Finish (New Workshare Collaboration Wizard)**
Displays all the settings that you have defined to create the new Workshare collaboration.
Review these settings carefully. If you are satisfied with the settings, select **Finish**. Otherwise, select **Back** to change one or more of the settings.
After completing this wizard, be sure to set the user access rights for the satellite plant.
Also, you must run Smart P&ID Options Manager and edit the sequence numbers as needed for the satellite site. Each satellite site can have its own settings (except path), however, the reference data is controlled by the host.
**Concluding a Workshare Collaboration**
Just as you use the **Enable Workshare** command to begin using Workshare, you use the **Disable Workshare** command to conclude a Workshare collaboration. Similarly to when you configured the Workshare collaboration, concluding a Workshare collaboration involves several steps at both the host and satellite sites using Smart Engineering Manager and other Smart P&ID products.
**Conclude a Workshare Collaboration**
1. Ensure that both host and satellite sites are running the latest Smart P&ID and Smart Engineering Manager service packs.
2. Satellites transfer ownership of all drawings to the host.
3. The host gets the latest versions of all drawings.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 73/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
1. The host synchronizes shared items. This step cleans up the T_INTERSITEOPC table.
2. Using Smart Engineering Manager, satellite sites delete satellite plants from their sites.
This cleans up the schema users for the plant, plant data dictionary, Smart P&ID, and Smart P&ID data dictionary.
1. Using Smart Engineering Manager, the host site runs **Workshare** > **Disable** **Workshare**.
2. The host ensures that all drawings and shared items are owned by the host. For example, open a drawing and, in the plant stockpile, select a loop that was created at the satellite site. Make sure it can be edited. Also, check the **Engineering Data Editor** to make sure OPC labels match correctly.
3. The host runs **Delete Orphan Model Items** > **Clean DB**.
If the satellites do not delete the satellite plants from their sites, orphan data is left behind in their databases, but the host can still disable Workshare.
For more information about using the **Delete Orphan Model Items** utility, see Clean Data Utility (DelOrpModItems.dll) in the *Smart P&ID*  Utilities Help.
**Disabling Workshare**
Disabling a plant for Workshare returns the plant to a pre-Workshare state. When you disable a plant for Workshare, the plant returns to its original plant structure status, and the **Satellites** node is removed from under the plant node.
**Disable Workshare**
1. In the **Tree** view, select the plant node.
2. Select **Workshare** > **Disable Workshare**.
In a connected Workshare collaboration, all connected satellite slots under the **Satellites** node must be inactive before you can disable Workshare. In other words, https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 74/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
connected satellite plants must be deleted and the **In Use** state must be **False** for all connected satellite slots before you can disable a connected Workshare collaboration.
Standalone Workshare collaborations can be disabled only after all drawings at the satellite site are deleted. All drawings originating from the host must be transferred back to the host with ownership assigned to the host.
**Disable Workshare Command (Workshare Menu)**
Returns the plant structure to a pre-Workshare state. When you disable a plant for Workshare, the **Satellites** node is removed from under the plant node.
Before you can access the **Disable Workshare** command in a connected Workshare collaboration, all connected satellite slots under the **Satellites** node must be inactive. In other words, connected satellite plants must be deleted and the **In Use** state must be **False** for all connected satellite slots before you can disable a connected Workshare collaboration.
Standalone Workshare collaborations can be disabled only after all drawings at the satellite site are deleted. All drawings originating from the host must be transferred back to the host with ownership assigned to the host.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 75/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Managing a Workshare Collaboration**
The following administrative commands are available in Smart Engineering Manager to help you manage your Workshare collaborations.
Change Password Command (Workshare Menu)
New Template Command (Workshare Menu)
Owner Command (Workshare Menu)
Publish Standalone Package Command (Workshare Menu)
Recreate Proxy Users Command (Workshare Menu)
Several of the Workshare commands are available in the Smart P&ID automation layer. For more information about using these Workshare automation commands, see the *Smart P&ID*  Programmer’s Help.
**Ownership**
During the course of administering a connected Workshare collaboration, you can decide to transfer the ownership of a plant group item, such as a unit, to a satellite site. Transferring ownership at this level allows the connected satellite site full control over plant group properties modifications. The owner can also delete the plant group item if all the drawings under it have been deleted.
**Transfer Ownership of a Plant Group**
1. In the **List** view, select the plant group for which you want to transfer ownership.
2. Right-click and select the **Owner** command.
3. On the **Plant Group Ownership** dialog, select the satellite site to which you want to grant ownership privileges.
The **Owner** command is available only at the host site in a greenfield connected Workshare collaboration. In other words, the connected Workshare collaboration cannot https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 76/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
involve projects at any level.
The **Owner** command is enabled at the host only if there is at least one connected satellite slot in use.
**Owner Command (Workshare Menu)**
Allows you to transfer ownership of a plant group item in a plant group. The owner can edit, modify, or delete plant group item properties.
The **Owner** command is available at the host only if there is at least one connected satellite slot in use.
At the host site, you do not need to have ownership of the plant group item to create drawings in that plant group item.
**Plant Group Ownership Dialog**
Allows you to specify the owner of the selected plant group. Transferring ownership at this level allows the connected satellite site full control over plant group properties modifications.
The owner can also delete the plant group item if all the drawings under it have been deleted.
Only a host site in a greenfield connected Workshare collaboration can assign plant group ownership. In other words, the connected Workshare collaboration cannot involve projects at any level.
**Workshare owner name**
Lists the host site and the currently connected satellite sites. Select the location to which you want to grant ownership privileges.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 77/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Publishing Data for Synchronization**
Because only the Workshare host has permission to modify the reference data, the updated reference data must be shared with all satellites whenever the reference data is modified (for example, adding a new attribute, creating a new select list, and so forth). Satellites cannot publish drawings or get the latest version of drawings until the satellite site reference data is in sync with the host.
In a standalone Workshare collaboration, the user bears full responsibility of making sure the reference data is in sync between the host and satellites.
Reference data consists of two parts: data in the file system and data in the plant and P&ID
schemas and data dictionaries.
The file system reference data (rules file, symbol files, and so forth), no matter the Workshare mode, must be transmitted manually to satellite sites for synchronization.
Synchronizing the database portion (plant and application schemas) of the reference data depends on the Workshare mode. For connected Workshare collaborations, the database portion of the reference data is synchronized automatically via the database link. For standalone Workshare collaborations or connected collaborations in which the database link is down (the **Synchronize Reference Data from Copy** command is unavailable), this portion of the reference data must be extracted from the database, bundled into a zip file, and manually transmitted to the satellite site. The **Publish Standalone Package** command creates this bundled zip file.
**Publish Standalone Package for Synchronization**
1. At the host site, select the host plant in the **List** view.
2. Select **Workshare** > **Publish Standalone Package**.
3. Send the *plantname* _sync.zip file to the satellite site for synchronization.
The * plantname* _sync.zip file is placed in the **Synchronization Templates** folder under the plant folder at the host site.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 78/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Publish Standalone Package Command (Workshare Menu)** Bundles the database portion of the reference data (plant and application schemas and data dictionaries, plant structure, and options data) into a zip file ( *plantname* _sync.zip) for manual transmission to the standalone satellite. This zip file is placed in the **Synchronization** **Templates** folder under the plant folder at the host site.
The satellite site accesses this file in Drawing Manager using the **Published standalone** **package file** field on the **Synchronize Reference Data by Copy** dialog.
This command is available only at the host in a standalone Workshare collaboration.
The host should run this command before publishing drawings to standalone satellite sites.
**Changing the Workshare Password**
During the course of administering a Workshare collaboration, you can decide to change the Workshare password for any of the satellite sites. The Workshare password is the key used by a satellite site to subscribe to a satellite slot at the host site. Created during the satellite slot creation at the host site, each satellite slot has its own password. This password must be communicated from the host to the satellite user, usually by e-mail or phone, before the satellite site can subscribe to a satellite slot.
**Change the Workshare Password**
1. In the **List** view, select the satellite slot for which you want to change the password.
2. Right-click the **Satellite Slot** and select the **Change Password** command.
3. Type the current Workshare password in the **Change Password** dialog.
4. Type and confirm the new Workshare password.
**Change Password Command (Workshare Menu)**
Allows you to change the Workshare password that you set during the satellite slot creation process. This password is the key that allows remote users to establish a new collaboration https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 79/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
with the satellite slot at the host. The password is case-sensitive and is available only at the host site.
**Change Password Dialog**
Allows you to modify the Workshare password.
**Current Workshare password**
Type the current Workshare password. This password was set when you created the satellite slot in the plant structure.
**New password**
Type a new password for the Workshare access to the plant structure data.
**Confirm new password**
Re-type the new Workshare password.
**Proxy Users**
Designating proxy users provides a way of granting users at remote satellites the ability to
“talk” to the tables in the host database instance. Proxy users are necessary for connected, same-instance Workshare collaborations. If the user names at the host and the satellite sites are identical and the databases are in separate database instances, you do not need to use proxy users.
**Add a Proxy User**
1. In the **List** view, select the satellite slot for which you want to create a new proxy user.
2. Right-click and select the **Add Proxy User** command. This command is available only at the host site.
3. On the **Add Proxy User** dialog, select **Workshare User Type** from the list of available user types.
4. Type a user name for this new proxy user.
5. Type and confirm a password for the new proxy user.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 80/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Add Proxy User Command (Workshare Menu)**
Available only at the host site, this command allows you to add authorized users to a satellite slot. When working with proxy users, keep the following scenarios in mind: **Same database instance**
Sites are in different database instances, but the plant structures are in the same database instance. In this situation, the user names at the host and satellite sites cannot be the same.
You were asked to create the proxy user names during the satellite slot creation.
**Different database instance**
If user names at the host do not match the user names at the satellite, a proxy user must be created at the host site to provide a way of granting the remote user the ability to talk to the tables in the host database instance. If the user names at the host do match the user names at the satellite, proxy user names are not needed.
**Add Proxy User Dialog**
Allows you to define a new satellite user name in the host database.
**Workshare proxy user**
Select the user proxy that you want to add. Only the user proxies without a user name defined will appear in the list.
**Database username**
Displays the user name last defined for the selected user type. Database usernames cannot start with a numeric digit and cannot contain any of the following characters: ~ ` ! % ^ & * ( ) -
+ = { } [ ] \ / ; : ‘ ” < > , . ? |
**Database password**
Type a password for the user name.
**Confirm password**
Re-type the password. Oracle database passwords cannot contain the characters: ” ’ @ and SQL Server database passwords cannot contain the character: ’
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 81/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Drop a Proxy User**
1. In the List view, select the satellite slot from which you want to drop a proxy user.
2. Right-click and select the **Drop Proxy User** command. This command is available only at the host site.
3. On the **Drop Proxy User** dialog, select the** Proxy User Type** that you want to drop.
Note the user name of the proxy user that you have selected to drop.
**Drop Proxy User Command (Workshare Menu)**
Allows you to remove proxy users from a satellite slot. This command is available only at the host site.
**Drop Proxy User Dialog**
Allows you to remove satellite user names from the host database.
**Proxy user type**
Select the user type containing the user name you want to drop.
**User name**
Displays the user name currently defined for the selected user type.
**Re-create Proxy Users**
1. In the **List** view, select the satellite slot for which you want to re-create proxy users.
2. Right-click and select the **Recreate Proxy Users** command.
**Recreate Proxy Users Command (Workshare Menu)**
Available only at the host site and only when a satellite slot is not in use, this command drops and re-creates all existing proxy users for the satellite slot.
We recommend re-creating proxy users when collaboration has failed for a same-instance satellite or when a privilege problem seems to exist, causing collaboration to fail for either separate or same-instance satellite slots.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 82/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
When working with proxy users, keep the following scenarios in mind: **Same database instance**
Sites are in different database instances, but the plant structures are in the same database instance. In this situation, the user names at the host and satellite sites cannot be the same.
You were asked to create the proxy user names during the satellite slot creation.
**Different database instance**
If user names at the host do not match the user names at the satellite, a proxy user must be created at the host site to provide a way of granting the remote user the ability to talk to the tables in the host database instance. If the user names at the host do match the user names at the satellite, proxy user names are not needed.
**Creating Satellite Templates**
The satellite template, created during satellite slot creation at the host site, is used at the satellite site to create a view of the host plant schema. The template also contains the Workshare password and the database user names for the satellite slot.
During the course of a Workshare collaboration, the data at the host site can change and thereby impact the content of the satellite template. When this happens, or when proxy users change, the host must generate a new template and send the updated template to the satellite.
**Create a New Template**
1. In the **List** view, select the satellite slot for which you want to create a new template.
2. Right-click and select the **New Template** command.
3. Type the path and file name for the connection template.
This command is available only at the host site.
**New Template Command (Workshare Menu)**
Allows the host to create a new Workshare template. During the course of a Workshare collaboration, the data at the host site might change, thereby impacting the content of the https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 83/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
satellite template. When this happens, or when proxy users change, the host must generate a new template and send the updated template to the satellite.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 84/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Publishing and Assigning Ownership**
To share a drawing with another site, you must first publish that drawing. Publishing the drawing does not grant access: it only freezes a copy of the drawing in anticipation of ownership being transferred. Between the publication of a drawing and the transfer of ownership, the publishing site still owns the drawing and is free to modify it.
Granting subscription access to the drawing gives another site access to the published copy of the drawing; for standalone Workshare, the drawing will be writable at the satellite site, while for connected Workshare, the drawing will be read-only. Assigning ownership, on the other hand, allows the site to claim ownership of the drawing and to obtain the published copy of the drawing for either Workshare mode.
In a standalone Workshare collaboration, drawing ownership controls from which site the host receives a published file of a given drawing. In other words, if a published file did not originate from the site with ownership, the host will ignore it when receiving the latest version of drawings. Only the host can assign ownership, which means that the host can “take back” or revoke ownership of a drawing at any time.
Hosts and satellites can create drawings in either Workshare mode. However, uniqueness of drawing names and numbers is not enforced across a standalone Workshare collaboration.
In connected Workshare collaborations, published files are stored in the database at the publishing site and the Oracle database link is used to transfer published files between sites.
In standalone Workshare collaborations, published files are stored in the WSPublish folder at the publishing site and must be manually transmitted to the other sites by e-mail, CD, network share, or other means.
**Publish a Drawing**
1. In the **List** view, select the drawings that you want to publish.
2. Grant access to the drawings by using either the **Subscribe Access** or **Assign** **Ownership** commands.
3. Select **Workshare** > **Publish**. If you used the **Assign Ownership** command in the previous step, the Publish process is launched automatically.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 85/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
1. On the **Publish** dialog, you can select **View Log** to see the history of the Workshare operation just completed.
2. If you are using connected Workshare, drawings need to be extracted if the files need to be transmitted manually in a case where the default publishing method is through the database. For details, see Extract Published Drawings.
3. If you are using standalone Workshare and changes have been made to the reference data, be sure to use the **Publish Standalone Package** command in Smart Engineering Manager to bundle the database reference data for synchronization with the satellite.
For standalone Workshare, you must run the **Subscribe Access** command before you publish, whereas for connected Workshare, the order of these actions is unimportant.
Linked or embedded files are not transferred by Workshare. Those files must be transferred manually. We do not recommend using linked files in a Workshare collaboration.
You can schedule the selected drawings for publishing at a later time or on a regular interval by using the **Schedule Publish** command in Drawing Manager and following the prompts on the Schedule Task Wizard.
When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.
**Extract Published Drawings**
1. In Drawing Manager, select the plant structure in the **Tree** view.
2. Select **Workshare** > **Extract Published Drawings**.
3. On the **Extract Published Drawings** dialog, browse to the directory to which you want your drawings published.
4. Select **OK**.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 86/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
A new folder is created in this directory and named using the day, date, and time of the publishing operation. This folder contains the results of the extraction operation. The folder could be on a local or network drive.
Extracting published drawings is later used with the **Get Latest Version from Local** command.
This command is available only in connected Workshare collaborations.
**Set Subscription Access for a Drawing**
1. In Drawing Manager, select the drawings for which you want to set the subscription access.
2. Select **Workshare** > **Subscribe Access**.
3. On the **Subscribe Access** dialog, select the site that you want to grant access to from the **Available Sites** list.
4. Select **Add** to move that site into the **Selected Sites** list.
You can remove read access from these permissions by using the **Remove** button to move a site out of the **Selected Sites** list.
You must have published a drawing before you can assign access to another site.
When assigning subscription access, drawings in standalone Workshare mode are writable, whereas drawings in connected Workshare mode are read-only.
If a drawing in standalone Workshare mode is modified at the satellite site and then published and sent back to the host, it will not be available for selection at the host when the **Get Latest Version from Local** command is run. To grant read/write permission for the drawing at the host site, use the Assign Ownership option. For details, see Assign
Ownership to a Drawing.
When the other site gets a copy of a drawing to which they have read access, they do not see updates to that drawing after the point when they receive that version. That is, the two instances of the drawing are not linked dynamically. For more information about getting the latest version of a drawing, see Getting Latest Versions of Drawings.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 87/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Assign Ownership to a Drawing**
1. In the List view, select the drawings to which you want to grant write access.
2. Select **Workshare** > **Assign Ownership**.
3. On the **Assign Ownership** dialog, choose the appropriate site from the list.
4. Select **OK**.
*The drawings are immediately published.* 
The sites available on the **Assign Ownership** dialog are specified automatically according to the sites currently participating in the Workshare collaboration. These Workshare sites are set up in Smart Engineering Manager.
Assigning ownership of a drawing also publishes the drawing.
If you want to grant read access only, see Set Subscription Access for a Drawing.
For drawings owned by the host, ownership can be given by the host to any standalone or connected satellite.
For drawings owned by a standalone satellite, ownership can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer ownership to a drawing from one satellite to another, the host must first transfer ownership back to itself before granting ownership to the other satellite.
For drawings owned by a connected satellite, ownership cannot be set by the host.
When transferring ownership of a drawing, the corresponding drawing versions are not transferred. Only the current version of the drawing is transferred.
When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.
**Publish Command (Workshare Menu)**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 88/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Publishes the selected drawing or drawings. The **Publish** dialog displays the status of the operation.
The act of publishing a drawing actually bundles the drawing and its related data and places it as a “blob” object in the host database.
In a connected Workshare collaboration, when the satellite uses the **Get Latest Version from** **Remote** command, the published “blob” is copied from the host database to the satellite site database. At the satellite site, the “blob” is then unpacked and the drawing is placed in the local file system while its related data is placed in the local Smart P&ID database.
In a standalone Workshare collaboration, the published “blob” is automatically extracted into a published zip file. The **Publish** command derives which sites have been given subscribe access to the drawings being published and places the published zip files in the target WSPublish folder in individual folders corresponding to each subscribing site, allowing you to more easily determine which published zip files to transmit to a given site. The receiving site then uses the **Get Latest Version from Local** command to unpack the zip file, placing the drawing in the local file system and the related data into the local Smart P&ID database.
For mixed Workshare collaborations, the publishing process detects the types of satellites involved and performs the appropriate actions. For example, when a drawing is published for both a standalone and a connected satellite, the **Publish** command creates the published zip file in the WSPublish folder and places the corresponding “blob” in the database.
For standalone Workshare collaborations, before the connected satellite site can access the published drawing, you must grant subscription access to or assign ownership of the drawing to the satellite site.
For standalone Workshare collaborations, if you do not grant subscription access to or assign ownership of a drawing before you publish it, the published drawing zip file will not be created in the WSPublish folder.
Satellite-to-satellite data transfer is not supported in standalone Workshare.
Published zip files in the WSPublish folder are overwritten without warning as needed by subsequent publishes.
When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 89/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
retrieved documents to have tasks updated within the satellite drawings.
**Publish Dialog**
Displays the status of your publishing operation. This status dialog opens when you publish drawings or when you assign ownership to drawings.
**Drawings**
Lists the drawings that are being published, and shows the status of that operation.
**View Log**
Opens the log file that is created when you perform a Workshare operation.
**Extract Published Drawings Command (Workshare Menu)** Extracts all plant-wide published drawing and related data from the database into zip files (one zip file per drawing) so that the data can be manually transmitted to a satellite. The satellite then unpacks the zip file using the **Get Latest Version from Local** command, which places the drawing in the local file system and the related data into the local Smart P&ID
database.
This command is available only in connected Workshare collaborations.
**Extract Published Drawings Dialog**
Allows you to specify the location, on a local or network drive, where the extracted data will be placed into a new folder named using the day, date, and time of the publishing operation.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 90/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Look in**
Lists the available directories. You can choose a folder and select **OK**. A new folder to hold your published drawings is created inside the folder you select.
**Drives**
Displays the currently active drive. To change to another drive, select **Network**.
**Network**
Opens the Microsoft standard **Map Network Drive** dialog with which you can specify a new active drive.
**OK**
Extracts all published data plant-wide and places it in a new folder inside the folder selected in the **Look in** list.
**Extract Published Drawings Status Dialog**
Displays the progress of the extraction operation.
**Extraction Progress Bar**
Displays the name of the drawing which is being extracted and the progress of that operation.
**Cancel**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 91/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Quits the process if the publishing operation is underway. If the extraction is complete, **Close** simply dismisses the dialog.
**Subscribe Access Command (Workshare Menu)**
Designates which sites should receive a published drawing and grants access to those sites.
In standalone Workshare mode, only the host can set subscribe access and the access to the drawings is read-write. In connected Workshare mode, this command is available to the host and the connected satellites and the access to the drawings is read-only.
In a mixed-mode Workshare collaboration, the following limitations apply: For drawings owned by the host, subscribe access can be given by the host to any standalone or connected satellite.
For drawings owned by a standalone satellite, subscribe access can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer subscription access to a drawing from one satellite to another, the host must first transfer the access back to itself before granting subscription access to the other satellite.
For drawings owned by a connected satellite, subscribe access cannot be set by the host.
**Subscribe Access Dialog**
Allows you to specify the sites that have subscribe access to drawings that you publish.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 92/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Available sites**
Lists the satellite sites that are available to subscribe to the selected drawing.
**Selected sites**
Lists the sites that currently have subscribe access to the drawings that you publish.
**Add**
Moves a selected site from the **Available sites** list to the **Selected sites** list.
**Remove**
Moves a selected site from the **Selected sites** list to the **Available sites** list.
**Add selected**
Gives subscription access to all the sites selected in **Available sites**.
**Delete selected**
Removes subscription access from all the sites selected in **Selected sites**.
**Assign Ownership Command (Workshare Menu)**
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 93/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Opens the **Assign Ownership** dialog, where you can specify which Workshare sites have read/write permission for published drawings. Drawing ownership is used to control, for a given drawing, which satellite’s published data the host receives during a Get Latest Version operation.
In a mixed-mode Workshare collaboration, the following limitations apply.
For drawings owned by the host, ownership can be given by the host to any standalone or connected satellite.
For drawings owned by a standalone satellite, ownership can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer ownership to a drawing from one satellite to another, the host must first transfer ownership back to itself before granting ownership to the other satellite.
For drawings owned by a connected satellite, ownership cannot be set by the host.
When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.
When the host, in standalone mode, is functioning as a project, all items on the selected drawings are automatically claimed when the drawing ownership is assigned to a satellite site.
If exclusive claiming is being used and one or more items have already been claimed by another project, assigning ownership is not allowed.
Assigning ownership of a drawing automatically publishes the drawing.
When transferring ownership of a drawing, the corresponding drawing versions are not transferred. Only the current version of the drawing is transferred.
If the site to which ownership has been assigned has subscription access, the subscription access will be removed.
**Assign Ownership Dialog**
Allows you to specify the site to which you want to grant ownership of the selected drawing.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 94/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Available Workshare sites**
Lists the sites that are currently linked to your site and available to take ownership of the selected drawing.
**OK**
Assigns ownership of the drawing to the specified site and publishes the selected drawing.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 95/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Getting Latest Versions of Drawings**
After a site has been granted access to a published drawing, that site must subscribe to the latest version of the drawing in order to open or edit that drawing. In a connected Workshare collaboration, you get the latest version from the owner site over a database connection by using the commands for remote access. In a standalone Workshare collaboration or a connected collaboration where the satellite does not have remote access to the host, you get the latest version from the owner site by getting the latest version from a local directory after the published files have been extracted into a zip file and manually transmitted to the satellite site via e-mail, CD, network share, or so forth.
Drawings are never dynamically linked between sites. That is, the version you view is only the latest version to which you subscribed or the latest version left on your site. If another site has modified the drawing since you retrieved the latest version of a published drawing, you do not see those changes. At sites that have a copy of a drawing but do not own the drawing, a red lock on the drawing icon
appears in the **List** view. This icon indicates that your version of the drawing may not be the most current.
**Get the Latest Version of a Drawing from a Remote Site** 1. In the **Tree** view in Drawing Manager, select the plant structure to accept the latest versions of drawings.
This site must have either subscription access or ownership of the latest versions of drawings.
1. Select **Workshare** > **Get Latest Version from Remote**.
2. On the **Get Latest Version from Remote Site** dialog, select the location from which you want to get the latest versions of drawings, and then select **OK**. The **Get Latest** **Version from Remote** dialog opens and displays the status of the operation.
You must have a network connection or DBLink with the remote site to use this command. If you received the published drawings from the remote site via a CD
or e-email and have stored those files locally, use the **Get Latest Version from Local** command to access those files.
1. Select **View Log** to see the history of the subscription operation just completed.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 96/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
The locations available in the list in the **Get Latest Version from Remote Site** dialog are specified automatically according to the satellites connected to the host.
When you get a version of a drawing, you do not see updates to that drawing after the point in time when you subscribed to it. That is, the two versions of the drawing are not linked dynamically.
Linked files are not transferred by Workshare. Those files must be transferred manually.
We do not recommend using linked files in a Workshare collaboration.
You can select **Workshare** > **Schedule Get Latest Version from Remote** to open the
Schedule Task Wizard and defer the subscription to a later time or on a regular interval.
You must still complete the next step in this procedure.
**Get Latest Version from Remote Command (Workshare** **Menu)**
Typically used only in a connected Workshare collaboration, this command opens the **Get** **Latest Version from Remote** dialog, which allows you to specify the site from which you want to receive the latest versions of published drawings.
When you get the latest version of a drawing, you do not see updates to that drawing after the point in time when you got that version. That is, the two versions of the drawing are not linked dynamically.
Before you can get the latest version of a drawing, that drawing must first be published and assigned to you with the appropriate permissions, and you must have a network or database connection to the Workshare site where the published drawing currently resides.
The latest version of a drawing replaces any versions of that drawing currently at your site; therefore, use caution when subscribing to the latest versions.
**Get Latest Version from Remote Dialog**
Allows you to specify the remote site from which you want to receive the latest versions of drawings.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 97/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Available Workshare Sites**
Lists the sites in your Workshare collaboration that have published drawings available to you.
If the site you are looking for is not in the list, check to see if that site has published any drawings and, if so, has it assigned access to you.
**Get Latest Version from Remote Dialog (status)**
Displays the status of the Get Latest Version operation.
**Drawings**
Lists the drawings that are being updated and shows the status of that operation.
**View Log**
Opens the log file that is created during this procedure.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 98/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Get the Latest Version of a Drawing from the Local** **Computer**
1. In the **Tree** view in Drawing Manager, select the plant structure to accept the latest versions of drawings. This plant must have either subscription access or ownership of the latest versions of drawings.
2. Select **Workshare** > **Get Latest Version from Local**.
3. On the **Get Latest Version from Local** dialog, select **Browse**.
4. On the **Select Publish Folder** dialog, browse to the folder that contains the zip file containing the extracted files associated with the latest drawing version.
5. Select **OK**.
*The **Get Latest Version from Local Status** dialog opens and displays the status of the* *operation.* 
1. Select **View Log** if you want to read notes from this process.
2. Be sure to synchronize reference data before trying to open the newly obtained drawings. For details, see Synchronizing Reference Data.
You can schedule this process for a later time by using the Schedule Task Wizard.
If you are using a connected Workshare collaboration and have an active network connection to the remote site, you can get the latest version from there, too. For more
information, see Get the Latest Version of a Drawing from a Remote Site.
**Get Latest Version from Local Command (Workshare** **Menu)**
Typically used in a standalone Workshare collaboration, this command opens the **Get Latest** **Version from Local** dialog, which allows you to browse to the published zip file you received from another site and to select the drawings you want to receive. The **Get Latest Version** https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 99/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**from Local** command detects if the incoming published files originated from the expected host site. If they did not, the files are skipped and an entry is written in the log file.
When you get the latest version of a drawing, you do not see updates to that drawing after the point in time when you got that version. That is, the two versions of the drawing are not linked dynamically. In a connected Workshare collaboration, the latest version of a drawing replaces the version of a drawing that you currently have on your computer. In a standalone collaboration, a version is created for each replaced drawing.
When a new drawing created at a satellite is obtained by the host, the drawing ownership at the host is set to the originating site. For projects, when new objects created by a satellite site are obtained by the host, new claim records are created at the host.
Before you can get the latest version of a drawing, that drawing must first be published and assigned to you with the appropriate permissions, and you must have placed the zip file containing the extracted published files on your local computer or a network share to which you have access.
**Get Latest Version from Local Dialog**
Allows you to open the zip file containing the extracted published drawings you received from another site. After opening the zip file, you can view a drawing or compare it with an existing version at your site prior to actually obtaining the drawing and writing it to your local database.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 100/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Published files**
Displays the drawings included in the published zip file. In the following situations, certain published drawings are excluded from this list:
At a connected satellite, excludes published files for drawings owned by that site and drawings from a site not collaborating with the same host.
At the host, excludes published drawings not owned by the originating site and drawings from a site not collaborating with the same host.
At a standalone satellite, excludes published files for drawings from a site not collaborating with the same host.
Drawings that already have assigned ownership at the current site are displayed in grey.
**Browse**
Opens the **Select Publish Folder** dialog, which allows you to browse to the location where you saved the zip file containing the Extract Published Drawings.
**View**
Opens the **View** dialog, which displays a read-only view of the selected drawing version without opening Smart P&ID. You can manipulate the view or select drawing items and review their properties.
**Compare With**
Opens the **Compare With** dialog, allowing you to compare the current drawing version at your site with the incoming data. You cannot compare incoming data to a previous version of the drawing.
**Select All**
Marks all drawings in the **Published files** list to be extracted from the zip file and written to your local plant database.
**Clear All**
Clears all drawings in the **Published files** list.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 101/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Schedule**
Opens the Schedule Task Wizard, which allows you to schedule the get latest from local process for a later time.
**Select Publish Folder Dialog**
Allows you to locate the folder in which the zip file containing the extracted published drawing is stored.
**Look in**
Lists the available folders.
**Drives**
Displays the currently active drive. To change to another drive, select **Network** or select a drive from the list.
**Network**
Opens the Microsoft standard **Map Network Drive** dialog, allowing you to specify a new active drive.
**OK**
Opens the zip file containing the extracted published drawings and lists the drawings in the **Get Latest Version from Local** dialog.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 102/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Get Latest Version from Local Dialog (status)**
Displays the status of the **Get Latest Version from Local** process.
**Drawings**
Lists the drawings that are being updated and shows the status of that operation.
**View Log**
Opens the log file.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 103/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Synchronizing Reference Data**
Because only the host site may change the reference data, satellite sites need to synchronize the reference data from the host site each time it changes.
Synchronizing the reference data (RDB) involves making sure both the host and satellites are using the same plant schema and data dictionary, plant structure, Smart P&ID schema and data dictionary, and various options settings. Synchronization also involves making sure various data files at the satellite site remain up to date with the files at the host. These files include the rules file, insulation specifications, report and drawing templates, symbology settings, CAD definition file, and so forth.
Changes made to a data dictionary require reference data synchronization before any publishing or subscription activity. Because the data dictionary can be modified only at the host site, the host administrator should inform the satellite administrators when any data dictionary at the host is modified. Reference data stored in the data dictionary that can be changed or updated includes, but is not limited to, new properties or changes to existing properties (such as display name, category) Validation or Calculation IDs, filters, and **Engineering Data Editor** layouts.
You can synchronize reference data either directly with the host site over a network connection or with a copy of the reference data on your local computer (or network share) using the **Synchronize Reference Data** commands.
There are two synchronization stages:
**Database, Schema, and Data Dictionary Synchronization** Involves synchronizing the database-related data listed below. In connected Workshare collaborations, synchronizing this portion of the reference data is accomplished automatically over the DBLink using the **Synchronize Reference Data** command. For standalone Workshare collaborations, the host uses the **Publish Standalone Package** command in Smart Engineering Manager to bundle this information into a zip file (plantname_sync.zip) for the satellite site to access in the **Published standalone package file** field on the **Synchronize Reference Data from Copy** dialog.
Plant schema and data dictionary
Plant structure
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 104/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Plant replication schema, if using connected Workshare Smart P&ID schema and data dictionary
Formats
Options settings
**File Synchronization**
Involves the host site manually transmitting the following data files to the satellite site for access using either of the **Synchronize Reference Data** commands.
Rules file (rules.rul)
Insulation specification file (InsulationSpec.isl)
Report and drawing templates (border files are synchronized only if they are in the same location as the drawing templates)
Symbology settings (ProjectStyles.spp)
CAD definition file (Exportlayer.xlsx)
Templates
Path to the symbol catalog
Plant Configuration file for ‘Save as XML’ (PlantConfig.xml) For connected Workshare collaborations across domains, the satellite site can use the **Synchronize Reference Data** command to synchronize the database part of the reference data only if it has no access to the reference data shared folder at the host. If file synchronization is also needed, then the satellite should use the **Synchronize Reference** **Data from Copy** command.
During the synchronization process, a log file, SynchRefData.log or SynchRefDataFromCopy.log is created in the user’s temp folder (%temp%). This log file contains a list similar to the list that is displayed in the **Synchronize Reference Data** dialog.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 105/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Customizations should be done at the host. For example, Plant Filters should not be created at a satellite site because when you synchronize reference data with the host, you lose that information. However, you can always create My Filters in the Filter Manager environment.
Automation programs (for example, DLL and OCX files) are not synchronized. For more information about automation, see *Smart P&ID Programmer’s Guide*.
Reference data at the satellite site must be synchronized with the host reference data before any drawings and shared items can be synchronized or transferred.
Border files are synchronized only if they are in the same location as the drawing templates.
We recommend scheduling synchronization for a time when no users are working in the data.
**Synchronize Reference Data from Host**
1. In Drawing Manager, select **Workshare** > **Synchronize Reference Data**.
2. When the synchronization process finishes, select **Close**.
3. Exit, then re-open Drawing Manager. You can now publish or get the latest version of drawings.
In order to synchronize the databases, the DBLink or other network connection between host and satellite must be active.
You can view the progress of the synchronization process on the **Synchronize** dialog.
If a satellite does not synchronize reference data, the satellite can neither publish nor get the latest version of a drawing.
For information about synchronizing reference data without a remote connection to the
host, see Synchronize Reference Data from a Copy.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 106/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Synchronize Reference Data from a Copy**
1. Select **Workshare** > **Synchronize Reference Data from Copy**.
2. On the **Synchronize Reference Data from Copy** dialog, select each **Browse** button and specify the paths to the copies of the reference data files.
You must have a live network connection to these files if they are not on your local computer.
1. Specify a path for every file listed on this dialog.
Until every path is specified, the **OK** command is not available.
The path you specify for the rules library is also used to determine the path for the PlantConfig.xml file.
*The **Synchronize Reference Data** dialog opens and displays the progress of the* *synchronization operation.* 
1. You can select **View Log** if you want to read notes on the synchronization operation.
2. Exit and then re-open Drawing Manager. You can now publish or get latest version of drawings.
If a satellite does not synchronize reference data, the satellite cannot publish or get the latest version of a drawing.
If you are using a Workshare environment in the Smart P&ID Modeler and you are at a satellite site, you should not store custom layouts for the **Engineering Data Editor** or Plant Filters because when you synchronize reference data, you lose that information.
You can select **Schedule** to defer this task to a later time or schedule it on a regular
interval. When the Schedule Task Wizard opens, follow directions in the wizard to complete the scheduling of this synchronizing operation.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 107/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Synchronize Reference Data Command (Workshare Menu)** Typically used in a connected Workshare collaboration, this command uses the DBLink or network connection between host and satellite to synchronize the data. The **Synchronize** dialog displays the progress of synchronizing your reference data with the host reference data.
**Synchronize Reference Data Dialog**
Displays the progress of synchronizing reference data.
**Tasks**
Lists the individual parts of the reference data and displays their status in the synchronization process.
**View Log**
Opens the log file that is created when you perform a Workshare operation.
**Synchronize Reference Data from Copy Command**
**(Workshare Menu)**
Typically used in a standalone Workshare collaboration, this command allows you to synchronize the reference data with a copy of the data as opposed to over a network connection. The **Synchronize Reference Data from Copy** dialog allows you to specify the directories or files that contain the copies of the reference data.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 108/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Synchronize Reference Data from Copy Dialog**
Specifies the paths to the copies of the specific reference data with which you want to synchronize your data.
**Rules library**
Allows you to specify the path to the rules file (Rules.rul) in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.
The path you specify for the rules library is also used to determine the path for the PlantConfig.xml file.
**Insulation specifications file**
Allows you to specify the insulation specification file (InsulationSpec.isl) in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 109/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Default report template path**
Allows you to specify the path to the default report templates folder in the copied reference data. This path typically points to the Report Files folder in the SmartPlant\P&ID Reference Data folder on your computer.
**Plant style file**
Allows you to specify the plant styles file (ProjectStyles.spp) in the copied reference data.
**CAD definition file**
Allows you to specify the CAD definition file (Exportlayer.xlsx) in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.
**P&ID template path**
Allows you to specify the path to the P&ID templates in the copied reference data. This path typically points to the Template Files folder in the SmartPlant\P&ID Reference Data folder on your computer.
**Catalog Explorer root path**
Displays the path to the **Catalog Explorer** root path in the copied reference data. This path typically points to the Symbols folder in the SmartPlant\P&ID Reference Data folder on your computer.
**Pipe jacket nominal diameter configuration file**
Allows you to specify the path to the pipe jacket nominal diameter configuration file (JacketNDCoreND.XML) if it exists in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.
Because this file may not exist at the host, the software does not **require** that the field be filled in order to synchronize the Reference Data. It is the user’s responsibility to select the file to synchronize it with the satellite.
**Standalone package file**
Allows you to specify the zipped file ( *plantname* _sync.zip) containing the database reference data information bundled by the host using the **Publish Standalone Package** command. This field is available only for standalone Workshare collaborations.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 110/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Browse**
Allows you to browse to the appropriate file or folder for the pertinent reference data.
**Schedule**
Opens the Schedule Task Wizard, which allows you to defer synchronizing data to a later time or to schedule it on a regular interval.
**Default Report Template Path Dialog**
Allows you to search for a folder on your computer or the local network. This dialog opens only when you are browsing for the **Default report template path** on the **Synchronize** **Reference Data from Copy** dialog.
**Look in**
Lists the available directories. Choose a folder and select **OK**.
**Drives**
Displays the currently active drive. To change to another drive select **Network**.
**Network**
Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 111/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**P&ID Template Path Dialog**
Allows you to search on your computer or the local network for a folder. This dialog opens only when you are browsing for the **P&ID template path** on the **Synchronize Reference** **Data from Copy** dialog.
**Look in**
Lists the available directories. Choose a folder and select **OK**.
**Drives**
Displays the currently active drive. To change to another drive select **Network**.
**Network**
Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.
**Catalog Explorer Root Path Dialog**
Allows you to search for a folder on your computer or the local network. This dialog opens only when you are browsing for the **Catalog Explorer root path** on the **Synchronize** **Reference Data from Copy** dialog.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 112/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Look in**
Lists the available directories. Choose a folder and select **OK**.
**Drives**
Displays the currently active drive. To change to another drive, select **Network**.
**Network**
Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 113/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Synchronizing Shared Items**
Some drawing items, such as off-page connectors, instrument loops, and utility connectors, require special handling when using Workshare. Because these items can be shared by more than one drawing, any modifications made to a drawing at another site may have ramifications for the shared items contained in that drawing. Consequently you must synchronize these shared items.
**Connectors** (OPCs such as off-unit connector, off-page connector, and utility connector) To be sure that OPCs synchronize properly, when placing a connector in a drawing at your site, use the **Move Partner OPC** command in the Smart P&ID Modeler to specify the drawing at another site on which the partner OPC should be placed. After synchronizing shared items at both sites, the partner OPC is transferred to the drawing stockpile for the specified drawing at the other site.
**Plant Item Groups** (instrument loop, package, safety class, and test system) These items can be placed only in the stockpile. To share these items with another site, first place them in the stockpile in Smart P&ID and then set the **IsShared** property in the **Properties** window to **True**. After synchronizing shared items at both sites, this plant item group appears in the stockpile at the other site and can now be associated with items at that site, but can only be modified by the originating site.
**Synchronize Shared Items**
1. Select **Workshare** > **Synchronize Shared Items**.
2. On the **Synchronizing Shared Items** dialog, select **View Log** to see the record of this synchronization operation.
If you want to defer this activity, or schedule it on a regular interval, you can select **Workshare** > **Schedule Synchronize Shared Items**. Follow the instructions on the Schedule
Task Wizard.
**Synchronize Shared Items Command (Workshare Menu)** Opens the **Synchronizing Shared Items** dialog, which allows you to start and monitor the synchronization operation.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 114/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
Run this command at the host and then at the satellite site.
**Synchronizing Shared Items Dialog**
Displays the progress of the synchronization operation.
**View Log**
Opens the log file that is created when you perform a synchronizing operation.
**Sample Synchronize Shared Items Workflow**
Synchronizing shared items is an automated process in a connected Workshare collaboration but is unsupported in standalone Workshare. Shared items must be manually synchronized in standalone Workshare collaborations as shown in the sample workflow below.
1. Host creates Dwg1 and assigns to Site1 and creates Dwg2 and assigns to Site2.
2. Host publishes these two drawings and sends the resulting .zip files to their respective sites.
3. Site1 and Site2 perform a Get Latest Version from Local to receive their drawings.
4. Site1 places an OPC on Dwg1.
5. Site1 creates a new drawing, Dwg3.
6. Site1 moves the partner OPC from Dwg1 into the drawing stockpile of Dwg3.
7. Site1 publishes Dwg1 and Dwg3 and sends the resulting .zip files to the Host.
8. Host performs a Get Latest Version from Local on both drawings.
9. Host publishes Dwg1 and Dwg3 and sends the resulting .zip files to Site2.
10. Site2 performs a Get Latest Version from Local on both drawings.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 115/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
1. Site2 moves the partner OPC from Dwg3 to the drawing stockpile of Dwg2.
2. Site2 places the OPC in Dwg2.
3. Site2 publishes Dwg2 and sends the resulting .zip file to the Host.
4. Host performs a Get Latest Version from Local on Dwg2. (The Host receives a moved items error condition and must move the OPC currently in Dwg3 to the plant stockpile before the **Get Latest Version from Local** command can succeed.) 15. Host publishes Dwg2 and sends to Site1.
5. Site1 performs a Get Latest Version from Local on Dwg 2. (Site1 receives a moved items error condition and must move the OPC currently in the Dwg3 stockpile to the plant stockpile before the **Get Latest Version from Local** command can succeed.) 17. Site1 opens Dwg 1 to cause the OPC label to refresh.
https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 116/125
3/19/25, 10:38 AM
Hexagon Documentation Site Export
**Scheduling Workshare Tasks**
**Schedule Publish Command (Workshare Menu)**
Opens the Schedule Task Wizard, which allows you to schedule publishing the selected drawing or drawings at a later time or on a regular interval.
**Schedule Task Wizard**
Allows you to specify options for scheduling a task, such as printing, archiving, publishing, and so forth. Follow the directions on the wizard as you choose options. Selecting **Next** advances you to the next appropriate screen in the wizard where you further specify options for the task that you are scheduling. On the final screen, selecting **Finish** completes the schedule and closes the wizard.
If you are logged in as a standard user on a Windows 10 operating system, your System Administrator must assign you special user rights to be able to run scheduled tasks. For details, see Assign User Rights for Scheduled Tas

1. 1. At each satellite site, subscribe to a satellite slot at the host site by creating a new Workshare collaboration. The host site must provide you with the Workshare password https://docs.hexagonppm.com/internal/api/webapp/print/510841de-3e5b-441f-83d0-c69cb6adedcd 54/125
2. 1.
    
    Define user access rights. You must grant at least **Modify Settings** access rights in the **Smart P&ID Options** category.
    
3. 2.
    
    Using Options Manager in Smart P&ID, adjust the starting sequence numbers for the **OPCItemTag**, **EquipNextSeqNo**, **InstrLoopNextSeqNo**, and **PipeRunNextSeqNo** settings to avoid duplicate item numbers.
    
4. 3.
    
    Using Smart P&ID Options Manager, modify the **Export to CAD Definition File** entry by changing .xls to Exportlayer.xlsx.
    
5. 1.
    
    Open the satellite site in Smart Engineering Manager.
    
6. 2.
    
    Select **Workshare** > **New Collaboration**.
    
7. 3.
    
    Follow the prompts in the **New Workshare Collaboration** wizard.
    
8. 4.
    
    Set the user access rights for the satellite plant.
    
9. 5.
    
    Run Smart P&ID Options Manager and edit the sequence numbers as needed for the satellite site.
    
10. 1.
    
    Ensure that both host and satellite sites are running the latest Smart P&ID and Smart Engineering Manager service packs.
    
11. 2.
    
    Satellites transfer ownership of all drawings to the host.
    
12. 3.
    
    The host gets the latest versions of all drawings.
    
13. 1.
    
    The host synchronizes shared items. This step cleans up the T_INTERSITEOPC table.
    
14. 2.
    
    Using Smart Engineering Manager, satellite sites delete satellite plants from their sites.
    
15. 1.
    
    Using Smart Engineering Manager, the host site runs **Workshare** > **Disable** **Workshare**.
    
16. 2.
    
    The host ensures that all drawings and shared items are owned by the host. For example, open a drawing and, in the plant stockpile, select a loop that was created at the satellite site. Make sure it can be edited. Also, check the **Engineering Data Editor** to make sure OPC labels match correctly.
    
17. 3.
    
    The host runs **Delete Orphan Model Items** > **Clean DB**.
    
18. 1.
    
    In the **Tree** view, select the plant node.
    
19. 2.
    
    Select **Workshare** > **Disable Workshare**.
    
20. 1.
    
    In the **List** view, select the plant group for which you want to transfer ownership.
    
21. 2.
    
    Right-click and select the **Owner** command.
    
22. 3.
    
    On the **Plant Group Ownership** dialog, select the satellite site to which you want to grant ownership privileges.
    
23. 1.
    
    At the host site, select the host plant in the **List** view.
    
24. 2.
    
    Select **Workshare** > **Publish Standalone Package**.
    
25. 3.
    
    Send the *plantname* _sync.zip file to the satellite site for synchronization.
    
26. 1.
    
    In the **List** view, select the satellite slot for which you want to change the password.
    
27. 2.
    
    Right-click the **Satellite Slot** and select the **Change Password** command.
    
28. 3.
    
    Type the current Workshare password in the **Change Password** dialog.
    
29. 4.
    
    Type and confirm the new Workshare password.
    
30. 1.
    
    In the **List** view, select the satellite slot for which you want to create a new proxy user.
    
31. 2.
    
    Right-click and select the **Add Proxy User** command. This command is available only at the host site.
    
32. 3.
    
    On the **Add Proxy User** dialog, select **Workshare User Type** from the list of available user types.
    
33. 4.
    
    Type a user name for this new proxy user.
    
34. 5.
    
    Type and confirm a password for the new proxy user.
    
35. 1.
    
    In the List view, select the satellite slot from which you want to drop a proxy user.
    
36. 2.
    
    Right-click and select the **Drop Proxy User** command. This command is available only at the host site.
    
37. 3.
    
    On the **Drop Proxy User** dialog, select the** Proxy User Type** that you want to drop.
    
38. 1.
    
    In the **List** view, select the satellite slot for which you want to re-create proxy users.
    
39. 2.
    
    Right-click and select the **Recreate Proxy Users** command.
    
40. 1.
    
    In the **List** view, select the satellite slot for which you want to create a new template.
    
41. 2.
    
    Right-click and select the **New Template** command.
    
42. 3.
    
    Type the path and file name for the connection template.
    
43. 1.
    
    In the **List** view, select the drawings that you want to publish.
    
44. 2.
    
    Grant access to the drawings by using either the **Subscribe Access** or **Assign** **Ownership** commands.
    
45. 3.
    
    Select **Workshare** > **Publish**. If you used the **Assign Ownership** command in the previous step, the Publish process is launched automatically.
    
46. 1.
    
    On the **Publish** dialog, you can select **View Log** to see the history of the Workshare operation just completed.
    
47. 2.
    
    If you are using connected Workshare, drawings need to be extracted if the files need to be transmitted manually in a case where the default publishing method is through the database. For details, see Extract Published Drawings.
    
48. 3.
    
    If you are using standalone Workshare and changes have been made to the reference data, be sure to use the **Publish Standalone Package** command in Smart Engineering Manager to bundle the database reference data for synchronization with the satellite.
    
49. 1.
    
    In Drawing Manager, select the plant structure in the **Tree** view.
    
50. 2.
    
    Select **Workshare** > **Extract Published Drawings**.
    
51. 3.
    
    On the **Extract Published Drawings** dialog, browse to the directory to which you want your drawings published.
    
52. 4.
    
    Select **OK**.
    
53. 1.
    
    In Drawing Manager, select the drawings for which you want to set the subscription access.
    
54. 2.
    
    Select **Workshare** > **Subscribe Access**.
    
55. 3.
    
    On the **Subscribe Access** dialog, select the site that you want to grant access to from the **Available Sites** list.
    
56. 4.
    
    Select **Add** to move that site into the **Selected Sites** list.
    
57. 1.
    
    In the List view, select the drawings to which you want to grant write access.
    
58. 2.
    
    Select **Workshare** > **Assign Ownership**.
    
59. 3.
    
    On the **Assign Ownership** dialog, choose the appropriate site from the list.
    
60. 4.
    
    Select **OK**.
    
61. 1.
    
    Select **Workshare** > **Get Latest Version from Remote**.
    
62. 2.
    
    On the **Get Latest Version from Remote Site** dialog, select the location from which you want to get the latest versions of drawings, and then select **OK**. The **Get Latest** **Version from Remote** dialog opens and displays the status of the operation.
    
63. 1. Select **View Log** to see the history of the subscription operation just completed.
64. 1.
    
    In the **Tree** view in Drawing Manager, select the plant structure to accept the latest versions of drawings. This plant must have either subscription access or ownership of the latest versions of drawings.
    
65. 2.
    
    Select **Workshare** > **Get Latest Version from Local**.
    
66. 3.
    
    On the **Get Latest Version from Local** dialog, select **Browse**.
    
67. 4.
    
    On the **Select Publish Folder** dialog, browse to the folder that contains the zip file containing the extracted files associated with the latest drawing version.
    
68. 5.
    
    Select **OK**.
    
69. 1.
    
    Select **View Log** if you want to read notes from this process.
    
70. 2.
    
    Be sure to synchronize reference data before trying to open the newly obtained drawings. For details, see Synchronizing Reference Data.
    
71. 1.
    
    In Drawing Manager, select **Workshare** > **Synchronize Reference Data**.
    
72. 2.
    
    When the synchronization process finishes, select **Close**.
    
73. 3.
    
    Exit, then re-open Drawing Manager. You can now publish or get the latest version of drawings.
    
74. 1.
    
    Select **Workshare** > **Synchronize Reference Data from Copy**.
    
75. 2.
    
    On the **Synchronize Reference Data from Copy** dialog, select each **Browse** button and specify the paths to the copies of the reference data files.
    
76. 1. Specify a path for every file listed on this dialog.
77. 1.
    
    You can select **View Log** if you want to read notes on the synchronization operation.
    
78. 2.
    
    Exit and then re-open Drawing Manager. You can now publish or get latest version of drawings.
    
79. 1.
    
    Select **Workshare** > **Synchronize Shared Items**.
    
80. 2.
    
    On the **Synchronizing Shared Items** dialog, select **View Log** to see the record of this synchronization operation.
    
81. 1.
    
    Host creates Dwg1 and assigns to Site1 and creates Dwg2 and assigns to Site2.
    
82. 2.
    
    Host publishes these two drawings and sends the resulting .zip files to their respective sites.
    
83. 3.
    
    Site1 and Site2 perform a Get Latest Version from Local to receive their drawings.
    
84. 4.
    
    Site1 places an OPC on Dwg1.
    
85. 5.
    
    Site1 creates a new drawing, Dwg3.
    
86. 6.
    
    Site1 moves the partner OPC from Dwg1 into the drawing stockpile of Dwg3.
    
87. 7.
    
    Site1 publishes Dwg1 and Dwg3 and sends the resulting .zip files to the Host.
    
88. 8.
    
    Host performs a Get Latest Version from Local on both drawings.
    
89. 9.
    
    Host publishes Dwg1 and Dwg3 and sends the resulting .zip files to Site2.
    
90. 10.
    
    Site2 performs a Get Latest Version from Local on both drawings.
    
91. 1.
    
    Site2 moves the partner OPC from Dwg3 to the drawing stockpile of Dwg2.
    
92. 2.
    
    Site2 places the OPC in Dwg2.
    
93. 3.
    
    Site2 publishes Dwg2 and sends the resulting .zip file to the Host.
    
94. 4.
    
    Host performs a Get Latest Version from Local on Dwg2. (The Host receives a moved items error condition and must move the OPC currently in Dwg3 to the plant stockpile before the **Get Latest Version from Local** command can succeed.) 15. Host publishes Dwg2 and sends to Site1.
    
95. 5.
    
    Site1 performs a Get Latest Version from Local on Dwg 2. (Site1 receives a moved items error condition and must move the OPC currently in the Dwg3 stockpile to the plant stockpile before the **Get Latest Version from Local** command can succeed.) 17. Site1 opens Dwg 1 to cause the OPC label to refresh.
    
96. 1.
    
    Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
    
97. 2.
    
    For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.
    
98. 1. To Cuba, Iran, North Korea, Syria, or the Crimean, “Donetsk People’s Republic”,
99. 1. To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List. Visit www.export.gov for more information or follow this link for the screening tool:
100. 1.
    
    To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Hexagon, its subsidiaries, or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.
    
101. 2.
    
    To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.