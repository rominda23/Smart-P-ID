# Intergraph Engineering and Schematics Projects Configuration and Reference

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Intergraph Engineering and Schematics**

**Projects Configuration and Reference**

**Hexagon Documentation**

Generated 03/19/2025

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

1/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Table of Contents**

Introduction to Projects

Understanding the Basic Project Concepts

Using Projects Within SmartPlant

Working with Plants and Projects

Working Directly in a Plant

Using a Project for New Design Work

Using Projects with an As-Built Facility Model

Using Projects for Multiple, Overlapping Projects

Using Projects to Explore Alternative Designs

Reviewing the Project Status

Smart P&ID Project Management

Projects vs. Workshare

Using Projects in an Existing Workshare Col aboration

Working with Off-Site Projects

Working with Smart P&ID Projects

Working with Drawings within a Project

Editing Drawing Items Within a Project

Viewing Overlapping Drawings

Sample Project Workflows

Finishing a Project

Smart Electrical Project Management

Smart Electrical Project and Item Statuses

Project Management Common Tasks in the As-Built

Project Management Table (As-Built)

Project Management Common Tasks in a Project

Project Management Table (Project)

Managing Revisions in an As-Built and Project Environment

Scoping Items

Claiming Items

Merging Items into As-Built

Plant Operating Cases in As-Built and Projects

About Security and Encryption

What techniques are used for Encryption?

Database encryption

Communication encryption between application client and server

Disk encryption

File share encryption

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

2/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

3/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

## Introduction to Projects

Plants, after designed and built, are often modified throughout their lifecycles. During these modifications, information assets of the “As-Built” state must be maintained. Using projects in your plant allows you to maintain this information while allowing multiple projects, possibly overlapping and running concurrently, to be designed, approved, constructed, and/or canceled. This guide explains how to implement projects in Intergraph Smart® P&ID and Intergraph Smart® Electrical.

Project configuration (enable, create, set scope, delete, and disable) is done in Intergraph Smart® Engineering Manager. For details, see Working with Projects.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2025 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 2/28/2025 at 12:57 PM

**Understanding the Basic Project Concepts**

To configure a successful projects environment, you must first understand the building blocks used to create this environment.

**What is a Site?**

A site is a logical unit of data that is normally used to model a collection of physical plants.

Every plant within a site has a unique identity. You access a site by opening the SmartPlantv4.ini file, which contains the database type, connection alias, and the schema information for the site and the site data dictionary. The site schema basically keeps track of the plants in the site.

The **Site Server** node is the root directory for each site when opened in Smart Engineering Manager.

**What is a Plant?**

A plant is a logical unit of data that is normally used to model a single physical plant. A plant has a single plant hierarchy that defines the breakdown of the whole plant into its functional parts. Every object within a plant has a unique identity.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

4/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

A plant makes use of a single data dictionary and a single set of reference data. Named objects are normally unique within a plant, but this is not a requirement.

A plant defines the largest scope of a report, and a plant can contain many P&ID drawings.

Plant items such as equipment, instruments and pipes are shown in schematic form on the drawings.

**What is a Project?**

A project is a logical unit of data that is related to a plant. A project is used for making controlled, incremental changes to the data in a plant. There can be multiple projects for a plant at any given time.

The identity of objects within a project is the same as their identity within the plant. All projects of a plant share the same data dictionary and the same reference data that is used by the plant. All projects of a plant share the same plant hierarchy, with a few exceptions as noted later.

The scope of a project may be limited so that it deals only with a subset of the drawings and plant items that exist within the plant. Changes made to items in a project do not immediately affect the corresponding items in the plant. A project may be completed and merged back into the plant, or canceled and discarded without affecting the plant.

**What is Claiming?**

The Claim operation identifies the scope of a project within a drawing. A project may affect some items on a drawing and leave others unchanged. All items that are affected by the project must be claimed before they can be modified or deleted. When a new item is placed on a drawing (in a project) it is automatically claimed.

In Options Manager, a plant setting called **Claim Mode** controls how items are claimed by concurrent projects. If the claim mode is Exclusive, only one project can claim an item at any given time. Exclusive claim mode enforces the rule that concurrent projects do not overlap at the object level. With this setting, conflict resolution at check-in time is simplified. If the claim mode is Shared, a single item can be claimed to more than one project. Shared claim mode allows concurrent projects to overlap at the object level. This setting may be required for plants that have truly overlapping projects; however, conflict resolution at check in time will be more complex.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

5/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

You can change the claim mode to Shared at any time. However, you can change the mode to Exclusive only when there are no claims in any project in the Plant.

**Using Projects Within SmartPlant**

Connecting your plant to SmartPlant introduces extra ramifications for projects in Drawing Manager. For instance, if you want to fetch a version of a drawing from your own project database (to roll back to an earlier version, for instance) the version creation timestamp must be later than the timestamp for the last publishing to SmartPlant.

When you are connected to SmartPlant and try to delete a fetched drawing that you have claimed items on, you must release all claims before you can do so. You must manually release these claims; Smart P&ID does not release your claims automatically. When you try to delete the fetched drawing, you see the message **Release all claims prior to Delete**.

Likewise, if a checked-out drawing has claimed items on it when you try to undo the checkout, the **Remove from Project** option on the **Undo Checkout** dialog displays this message: **Release all claims prior to Undo Checkout with this option**.

You are always free to fetch a drawing in read-only or read/write mode, whether there are claimed items or not. However, SmartPlant does not allow a fetched drawing with read/write permissions to be overwritten when it is checked out or fetched again. In order *not* to replace an existing fetched drawing with read/write permissions in a project database when you check out a version of it, the **Replace Existing P&ID** option on the **Check Out** dialog is never available. Likewise the **OK** button on the **Fetch** dialog is not available if you select a drawing to fetch that you have already fetched with read/write permissions. Of course, if you really want to overwrite a drawing you already have fetched, you can delete the fetched version first.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

6/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Working with Plants and Projects**

Depending on your design requirements, projects can be used in several different configurations.

**Working Directly in a Plant**

The traditional method of creating drawings and working directly in the plant is still supported.

There is no requirement to make use of the new project features if they are not needed. When a new plant is created, projects are disabled by default. You must explicitly enable projects before any project can be created. However, after you have enabled projects for a plant, you can no longer edit the plant directly. All changes to the plant must be done through a project.

**Using a Project for New Design Work**

When working on the design for a new plant, some organizations adopt the Task/Master approach. In this approach, all new design work is done in the task database. At certain important milestones, drawings and data from the Task database are merged into the Master database. Usually, drawings and data from the Task database are merged only after they have been approved. The drawings and data in the Master database are available to be viewed by a wider audience, including other groups within the organization.

The project features in Smart P&ID can be used to implement this Task/Master approach. In this scenario, the Plant is the Master database and a single project created in the Plant is used as the Task database. The project remains active as long as work continues in the Plant, with all new design work being performed within the project. When drawings are approved and they need to become visible to a wider audience, they are merged into the Plant. If approved drawings need to be revised, the drawings can be fetched from the Plant into the project for revisions. After the revisions are complete, they can be merged back into the Plant.

**Using Projects with an As-Built Facility Model**

Owners of existing plants frequently need to maintain a facility model that documents the current state of the physical plant. This facility model is sometimes called the As-Built model.

As changes are made to the physical plant, the As-Built model must be updated to reflect those changes. Changes come in all sizes from minor maintenance projects to major capital improvement projects. Frequently, multiple projects are active at any point in time.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

7/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The project features in Smart P&ID can be used to implement a Project/As-Built model. The Plant is designated as the As-Built database and a project is created in the Plant for each revamp or major capital improvement to the Plant. Existing drawings that need to be changed are fetched to the project. The scope of the project is defined by claiming the existing objects that need to be modified. New items on existing drawings can be created within the project.

Also, totally new drawings can be created within the project. When the project work is done and approved, the project drawings are merged back into the plant. The completed project can then be deleted to free up resources for other projects.

Maintenance work and smaller projects can be handled via formal projects as described above. Alternatively, this kind of work can be handled by an on-going project that is reserved exclusively for maintenance work. Individual drawings can be fetched into the maintenance project, as needed, and the necessary changes can then be performed within the context of the project. The individual drawings can then be merged back into the plant without terminating the project.

**Using Projects for Multiple, Overlapping Projects** A typical Plant may have many active projects at any point in time. Some of these projects may affect unrelated areas of the Plant. However, some projects may overlap in both their scope and their timelines. For example, there may be a long range capital project and a smaller revamp project that both involve changes to some of the same drawings and/or items in the Plant. Another factor to consider is that some projects build on each other. The final design of one project may be the starting point of the next project.

The project features in Smart P&ID can be used to support these types of concurrent engineering activities. For unrelated projects, the basic fetch/check out and merge/check in operations allow the facility model to be updated in a controlled fashion. For overlapping projects, the basic fetch and merge operations combined with the object-level claim and the compare and refresh operations allow the user to resolve all conflicts. The ability to fetch drawings not only from the Plant but also from other projects allows users to build on the current work being done in other projects.

**Using Projects to Explore Alternative Designs**

During a design cycle it may become necessary to explore the implications of two or more fundamentally different solutions for the same problem. Each solution may need to be elaborated with sufficient detail to be able to judge its technical and economic benefits. After https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

8/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

these analyses are complete, the best solution is selected for implementation and the remaining alternatives are discarded.

The project features in Smart P&ID can be used to explore such alternative designs. A separate project can be created for each alternative and the relative existing drawings can be fetched into each of these projects. The same drawing can be fetched into multiple projects, if necessary. Design work in each project can then proceed independently. After all of the designs are finished and a winner is selected, it can be merged back into the Plant and the other projects can be canceled.

**Reviewing the Project Status**

The status for a project displays in the **List** view when the **Projects** node is selected in the Plant. The project status is set in Smart P&ID Drawing Manager or in Smart Electrical. For details of how to modify the project status, see the following topics:

Modify Project Status in Smart P&ID

Modify Project Status in Smart Electrical

The following diagram shows the four possible project states: **Active**, **Completed**, **Merged**, and **Canceled** states.

**Active**

Indicates that the project is ready for design work to proceed. When a project is created, it automatically becomes active and remains in this state until it is either completed or canceled.

While a project is active, all the various project design activities, such as checking out and revising drawings, checking in drawings, and so forth, can be performed.

**Completed**

Indicates that work on the project has come to an end. All drawings checked out to the project are verified for check-in by Drawing Manager when the project is promoted to **Completed**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

9/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Work in a completed project is not allowed. You can reactivate a completed project and do more work, but to finish the project, you must change the status back to **Completed**.

**Merged**

Indicates that a project is complete and that all project data has been merged back into the Plant. When the project is promoted to **Merged**, Drawing Manager checks in all drawings and merges all project data back into the Plant.

**Canceled**

Indicates that the project can no longer be worked on. In this state, drawings cannot be checked into or out of the Plant. Canceling a project releases all claimed items and reverses the checkout of all drawings. A canceled project can be deleted in Smart Engineering Manager.

**Project Status and User Rights**

User access allows you to define rights that are assigned to roles. These rights define which commands are enabled or disabled for each user. When projects are enabled for a plant, the user defined rights are overlaid with additional rights that depend on the active database and the project status. These rights and overlays combine to define which commands are available to the user.

**Plant without Projects Enabled**

In a plant without the project feature enabled, the user defined rights have complete control over which commands are enabled. Both reference data and drawings can be edited in this environment. All the project commands (such as Check **Out, Check In**, and so forth) are, of course, not enabled.

**Plant with Projects Enabled**

After projects are enabled, the creation and modification of drawings must be done through a project. For a plant that has the project feature enabled, all the commands for creating and editing drawings are disabled. There is one notable exception to the general rule that all editing takes place within projects. The **Delete Drawing** command is available from within the Plant.

The reference data for the Plant is shared with all its projects. All editing of the reference data must be done through the Plant; therefore all reference data commands are enabled. The https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

10/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

project commands (such as **Check Out**, **Check In**, and so forth) are disabled.

**Project**

Within a project, all the commands for editing reference data are disabled. Reference data can only be edited through the associated plant. The availability of the project commands and the commands for editing drawings depends on the project status.

**Active**

This is the initial state when a project is created and the state in which most design activity takes place. All commands for editing drawings are enabled. The project commands for pulling drawings into a project (Fetch and Check Out) and merging drawings back into the plant (Check In) are enabled.

**Completed**

All drawings have been verified and are ready to be merged into the plant. All commands for editing drawings are disabled. The Check In command is enabled, but the other project commands are disabled.

**Merged**

All project drawings have been merged back into the plant and the project is ready to be deleted. All commands for editing drawings are disabled. All project commands are disabled.

**Cancelled**

The project has been marked as ready to be deleted (even though it was not merged back into the Plant). All commands for editing drawings are disabled. All project commands are disabled.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

11/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Smart P&ID Project Management**

The functionality for creating, manipulating and maintaining projects for Smart P&ID is spread throughout the Smart P&ID and Smart Engineering Manager products as described below.

**To…**

**Use…**

Configure projects (enable, create, set

Smart Engineering Manager. For details, see

scope, delete, and disable)

Configuring Projects.

Manage drawings (fetch, check in,

Smart P&ID Drawing Manager. For details, see:

check out, create and compare

versions)

Working with Drawings within a Project.

Compare Drawing Versions for As-Built and

Projects.

Manage drawing items (claim, compare Smart P&ID. For details, see: and refresh)

Editing Drawing Items Within a Project.

Comparing and Refreshing Versions.

To determine whether projects or Workshare are best suited to your needs, refer to

Projects vs. Workshare.

For details of the requirements for setting up projects in an existing workshare collaboration, see Using Projects in an Existing Workshare Collaboration.

To implement off-site projects in Smart P&ID, you use standalone workshare functionality. See Working with Off-Site Projects.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

12/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

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

be made only through the through the host. Changes are Plant. Because all projects propagated to the satellites by use the same reference

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

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

13/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

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

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

14/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

When a master database

is to be used for the

approved design and a

task database is to be

used for the ongoing

design work.

**Using Projects in an Existing Workshare Collaboration** You must discontinue all Workshare collaboration in a plant before you can create projects in the plant. In other words, if the plant structure contains active **Satellites**, the **Enable Projects** command remains unavailable. We recommend completing the following tasks before enabling the plant for projects.

1. Transfer all drawings to the host.
2. Delete all satellites.
3. Disable the plant for Workshare.
4. Enable the plant for projects.
5. Create a project to serve as the host.
6. Enable the project for Workshare.
7. Create satellite slots in the project host.
8. Create satellites.
9. Check out or fetch drawings at the host, then re-distribute drawings back out to the satellites.

**Working with Off-Site Projects**

To implement off-site projects in Smart P&ID, you use standalone workshare functionality. See the following help topics:

Using Workshare

Using Workshare with Projects

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

15/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Configuring Workshare

Managing a Workshare Collaboration

Publishing and Assigning Ownership

Getting Latest Versions of Drawings

Synchronizing Reference Data

Synchronizing Shared Items

**Working with Smart P&ID Projects**

Plants, after designed and built, are often modified throughout their lifecycles. During these modifications, information assets of the “As-Built” state must be maintained. Using projects in your plant allows you to maintain this information while allowing multiple projects, possibly overlapping and running concurrently, to be designed, approved, constructed, and/or canceled.

Before creating a project in a plant, you must enable that plant for projects. When enabled for projects, the plant structure becomes the Plant, sometimes referred to as the Master or As-Built plant. In a Task/Master scenario, the Plant is the Master and the projects are the individual Tasks.

**Database Configuration**

To allow work on projects to proceed without affecting the Plant, separate schemas are created for each project. In other words, all projects must be located in the same database instance as the Plant, with each project contained within a separate schema (separate database user names).

The Plant shares reference data with its projects. Changes to the reference data can be made only in the Plant. In other words, you can use Catalog Manager, Data Dictionary Manager, Filter Manager, and Format Manager in a project, but you have read-only permissions and are not allowed to modify any of the data from within these managers.

**Fetching and Checking Out Drawings**

After projects are enabled in Smart Engineering Manager, the As-Built can no longer create drawings; drawings are created inside projects. However, any drawings that might have https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

16/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

existed in the plant before projects were enabled remain in the As-Built. All drawing versions in the As-Built are read-only drawings when projects are enabled, but these drawings can still be deleted in the As-Built, unless the drawing is either fetched or checked out to a project. If the plant is registered in SmartPlant Foundation, drawings can be created and edited in the As-Built, except for drawings that are checked out to a project.

**Projects and Claiming**

One of the main capabilities associated with using projects in an integrated environment is the ability for a project to *claim* a drawing object. When a project claims an object, the project controls modifications to that object. A project cannot modify objects it has not claimed. All the modifications and claiming of objects is carried out in the design software, but the claim states of objects inside drawings do have ramifications for drawing manipulation and for completing projects. You do not need to check out a drawing to claim items on it; you can claim items on a fetched drawing.

Projects claim objects in either Exclusive (default) or Shared mode. If you plan to use the project in an integrated environment, Exclusive mode is mandatory. Use the **Settings** view in Options Manager to set the Claim Mode before creating a project.

When publishing from a project, an instruction container, which contains all the claimed objects, is created within the tombstone file.

You can change the Claim Mode to Shared at any time. However, you can change the mode to Exclusive only when there are no claims in any project in the Plant.

**Using Workshare with Projects**

Workshare functions the same whether using projects or not. The only difference is that when using projects, only a project can function as a Workshare host. The Plant cannot be a host or a satellite when projects are enabled.

**Working with Drawings within a Project**

After enabling and creating projects in Smart Engineering Manager for Smart P&ID, use Drawing Manager to manipulate the drawings. Actual design work is still accomplished in Smart P&ID; however, managing and setting out that work is largely controlled from the https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

17/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Drawing Manager interface. Only the project can use the commands on the **Project** menu in Drawing Manager to fetch, check in, and check out drawings.

After projects are enabled in Smart Engineering Manager, the As-Built can no longer create drawings; drawings are created inside projects. However, any drawings that might have existed in the plant before projects were enabled remain in the As-Built. All drawing versions in the As-Built are read-only drawings when projects are enabled, but these drawings can still be deleted in the As-Built, unless the drawing is either fetched or checked out to a project. If the plant is registered in SmartPlant Foundation, drawings can be created and edited in the As-Built, except for drawings that are checked out to a project.

When you are using projects inside Smart P&ID, remember that the reference data belongs to the Plant and is used by projects of the As-Built. You cannot change reference data, such as table layouts or formats or rules, at the project level.

**Claiming**

Claiming Items on a drawing is one of the main features of using projects in an integrated

environment. When a project claims an object on a drawing, the project controls modifications to that object. A project cannot modify objects that it has not claimed.

Projects claim objects in either Exclusive (default) or Shared claim mode. If you plan to use the project in an integrated environment, Exclusive mode is mandatory. Use the **Settings** view in Options Manager to set the **Claim Mode** value before creating a project.

You can change the claim mode to Shared at any time. However, you can change the claim mode to Exclusive only when there are no claims in any project in the Plant.

All the modifications and claiming of objects is carried out in the design software, but the claim states of objects inside drawings do have ramifications for drawing manipulation and for completing projects. You do not need to check out a drawing to claim items on it; you can claim items on a fetched drawing.

**Smart P&ID Project Statuses**

You can review the status of the active project using the **Project Status** command in Drawing Manager. The **Project Status** dialog shows the status of the active project and tells you

where the project is in its lifecycle. See Modify Project Status in Smart P&ID.

A **project** status shows the stage of the project life-cycle. Possible project statuses are: https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

18/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Active**

The initial state of a project right after its creation.

**Completed**

Indicates that all the work on the project items has been completed and that the items are ready to be merged back into the As-Built. You cannot claim items in a project whose status has been set to **Completed** or **Merged**.

In a project, when searching for completed items in the **Project Management** window, it is possible to select the related items which have not been completed yet and to change their status to **Completed**.

**Merged**

Indicates that all the project items have been merged back into the As-Built.

**Canceled**

Indicates that the project has been canceled and it can be deleted. Selecting this project status changes the status of the items in the project from **Claimed** to **Scoped**.

**Project Status Command (Project Menu)**

Opens the **Project Status** dialog, which allows you to update, modify, and verify the status of your project with respect to the Plant and/or SmartPlant Foundation. Possible statuses include **Active**, **Completed**, **Merged**, and **Canceled**. This command is not available if you are currently in the Plant; it is only available if your current database is a project database.

After a project enters the **Completed** state, all the commands are disabled and design work is no longer possible within that project. If you later determine that the project is really not done, use the **Return to Active** button on the **Project Status** dialog. This command resets the project status to **Active**, allowing work to continue in the project. This command is only enabled when the project is in the **Completed** state.

**Project Status Dialog**

Displays the current project status, both with respect to SmartPlant Foundation and the plant and allows you to update or modify those statuses. This dialog opens when you select https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

19/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Project** > **Project Status** on the main menu bar.

A project can only be returned to an **Active** state from the **Completed** state. If a project has been set to **Merged** or **Canceled**, it cannot be changed back to **Active**. **Merged** and **Canceled** are permanent states.

**SmartPlant project status**

Displays information about the status of the active project with respect to SmartPlant Foundation. This area is not active if the plant is not registered with SmartPlant Foundation.

**Refresh Status**

Searches for and displays the status of this project in SmartPlant Foundation and updates this information in SmartPlant Foundation if appropriate. This button is not available if the plant is not registered with SmartPlant Foundation.

**Smart P&ID project status**

Indicates whether the project is **Active**, **Completed**, **Merged**, or **Canceled**. If your project status is** Merged** or **Canceled**, then no further actions are available on this dialog.

**Return to Active**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

20/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Returns the project status to **Active**. This command is available only when the initial project status is **Completed** and the **SmartPlant project status**, if applicable, is **Active**.

**Complete Project**

Sets the project status to **Completed**. This command is available only when the initial project status and the **SmartPlant project status** are both **Active**. When you select **Complete** **Project**, a confirmation message appears.

**Merge Project**

Sets the project status to **Merged**. This command is available only when the initial project status and the **SmartPlant project status** are both **Completed**. When you select **Merge** **Project**, a confirmation message appears.

**Cancel Project**

Clears all claims on all objects and sets the project status to **Canceled**. This command is available only when the initial project status is **Active**. If the Plant is not registered, then the project is simply canceled out of Drawing Manager.

**Modify Project Status in Smart P&ID**

1. In Drawing Manager, open the project for which you want to view the status.
2. Select **Project** > **Project Status**.
3. In the **Smart P&ID project status** area, ascertain the current status of your project with respect to the plant.

A check mark denotes the current status. Possible statuses include **Active**, **Completed**, **Merged**, and **Canceled**.

1. Do any of the following to change the status of your project: To change an active project to completed, select **Complete Project**. This command is available only when the initial project status is **Active**.

When you change the project status to **Completed**, all the drawings in the project are verified for checking into the plant. You can verify each drawing separately if you

want to. See Verify a Drawing for Checkin.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

21/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

To change a completed project back to active, select **Return to Active**. This command is available only when the initial project status is **Completed**.

To merge a completed project into the plant, select **Merge Project**. This command is available only when the initial project status is **Completed**.

To cancel an active project, select **Cancel Project**.

If the plant is registered, select **Refresh Status** on the **Project Status** dialog to update the **SmartPlant project status** display.

In SmartPlant Foundation, the **Complete Project**, **Return to Active**, and **Merge** **Project** options are not available unless the **SmartPlant project status** is also **Active**.

The **Cancel Project** option is not available unless the **SmartPlant project status** is also **Canceled**.

**Fetching a Drawing to an Active Project**

Fetching a drawing from the Plant places a copy of the drawing in the project. Only one project at a time can check out a drawing, but numerous projects can *fetch* the same drawing.

Fetched drawings can have read-only or read/write permissions. If you want to save changes to a read/write fetched drawing into the Plant, you must check the drawing out first, apply your changes, and then check it back into the Plant.

If you are working with projects but are not connected to SmartPlant Foundation, all claims on items in that drawing are automatically released when you delete a fetched drawing from your project database.

A Workshare satellite can only fetch drawing versions from its own database by using the **Fetch** command in the **Version History** dialog. If you want a drawing version from another project or the Plant, it must be fetched into the host project and then the satellite can use the **Get Latest Version** commands on the **Workshare** menu.

**Fetch Command (Project Menu)**

Displays the **Fetch** dialog, which provides options for fetching a drawing version from the Plant or another project. You can fetch a drawing with read/write permissions or with read-https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

22/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

only permissions.

The **Fetch** command is not available if you are currently working in the Plant. You cannot fetch a deleted drawing, but a deleted drawing can be retrieved if a version of it is saved, and then you can fetch it.

**Fetch Dialog**

Displays the active Plant hierarchy and lists its drawings, allowing you to fetch a drawing from a specified database. This dialog appears when you select **Project** > **Fetch** or the **Fetch** command.

**Open Database**

Opens the **Projects** dialog, which allows you to specify a different project or the Plant.

**Filter**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

23/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Opens the **Filter** dialog, which allows you to specify the drawings that are displayed in the **List** view.

**Cancel Filter**

Deactivates any ad hoc filter you have applied to the **List** view.

**Include Subnodes**

Displays all the drawings and node names that reside in the currently selected node.

**List**

Displays the **List** view. The **List** view displays only one property for each drawing. To specify which property displays, select **Customize View** . The first item in the **Selected Properties** list is the property that appears in the **List** view.

**Details**

Displays the **Detail** view, which contains all the properties specified in the **Selected** **Properties** list on the **Customize Current View** dialog. Using the **Detail** view allows you to view and sort drawings by several attributes.

**Customize View**

Opens the **Customize Current View** dialog, which allows you to specify the information about each drawing that is displayed in the **List** view.

**Options**

Displays options specific to this fetch operation.

**Create New Version**

Saves a new version of the drawing before overwriting the existing version. This option is not enabled if the current drawing is not already fetched or checked out to the project.

**Read-only**

Fetches a read-only version of the drawing so that your project can examine the drawing but not alter it.

**Comments**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

24/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Allows you to enter comments pertinent to this fetch operation.

**History**

Opens an abbreviated version of the **Version History** dialog, which allows you to choose a saved version of the drawing you select in the **Fetch** dialog **List** view.

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions, when you select the same drawing to fetch, the **OK**

button on this dialog is not available.

**Projects Dialog**

Allows you to choose the Plant or a project that you want to fetch a drawing version from. You can fetch a version from a different project only if that project is part of the same plant in which you are working. This dialog opens when you select the **Open Database** button on the **Fetch** dialog toolbar.

**Available databases**

Lists the active Plant and the projects associated with it, other than the project in which you are currently working. Choosing from this list changes the plant hierarchy and the drawings displayed in the **Tree** and **List** views.

**Fetching Drawings Dialog**

Displays the progress of the version fetching operation currently under way. This dialog opens when you select **OK** on the **Fetch** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

25/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that are being fetched, and shows the status of that operation.

**View Log**

Opens the log file, Fetch.log, which is created when you fetch a drawing version.

**Fetch a Drawing**

1. Select **Fetch** .
2. On the **Fetch** dialog, select the pertinent node in the **Tree** view if it is not already selected.
3. In the **List** view, select the drawing that you want to fetch.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

26/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Select **History** if you need to fetch a version of this drawing other than the current version.
2. On the **Version History** dialog, select the version that you want to fetch, and then select **OK**.
3. Select the **Read-only** option if you want to fetch a version of the drawing for review only.
4. (Optional) Enter appropriate comments in the **Comments** box.
5. Select **OK**. You can follow the progress of the fetch operation on the **Fetching** **Drawings** dialog. Select **View Log** if you want to examine notes from the fetch operation.

If you want to fetch a drawing version from another project and not from the Plant, select **Open Database** on the **Fetch** dialog toolbar. On the **Projects** dialog, select the Plant or a project from the **Available databases** list, and then select **OK**.

You can open a read-only version of the drawing for review by selecting **View**. For more information about viewing drawing versions without fetching or checking them out, see Show the Version History of a Drawing.

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions when you check the drawing out, the fetched version remains intact and only its status changes to checked-out. That is, you cannot replace the fetched version with the version in the Plant.

**Checking a Drawing Out to an Active Project**

Checking out a drawing places that drawing under the control of the project. No other project can check out the same drawing while your project has it checked out. The advantage of https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

27/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

checking out rather than fetching a drawing is that only checked out drawings can have their changes reflected back in the Plant.

The software notifies you if you try to fetch a version of a drawing that you have already checked out.

When working with projects in an integrated environment, you must select **No** for the **Enable “Keep Checked Out” on Check-In** option in Options Manager.

After you check out a drawing to a project, the drawing will be read only in the As-Built and the following actions are not allowed:

Modifying drawing properties

Modifying the drawing or any drawing items or properties Deleting the drawing

Updating the drawing using Drawing Manager

Updating the drawing using automation

You cannot check out a drawing to a project if it is open in the As-Built.

The software cannot validate a drawing in the As-Built using the Global Validation functionality if you have checked out that drawing to a project.

**Check Out Command (Project Menu)**

Displays the **Check Out** dialog, allowing you to check drawings out from the Plant and into your current project. This command checks user permissions, assigned in Smart Engineering Manager, before it allows you to check out a drawing.

You can check out drawings that you have already fetched to your project, too. The **Check** **Out** command is available only inside a project of the Plant; that is, you cannot check a drawing out from a project and into the Plant. After a drawing is checked out to a project, the drawing icon changes to reflect the new status.

You do not have to check out a drawing to claim items on that drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

28/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions, when you check the drawing out, the fetched version remains intact and only its status changes to checked-out. That is, you cannot replace the fetched version with the version in the Plant.

**Check Out a Drawing**

Select **Check Out** .

1. On the **Check Out** dialog, select the drawing that you want to check out from the Plant hierarchy.
2. If you already have a fetched version of the drawing in your project and you want to replace it with the version that you check out, select the **Replace existing P&ID** option.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

29/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

If you do not replace the existing P&ID, your previously fetched version remains, but its status changes to **Checked-out**.

1. (Optional) Enter comments in the **Comments** area.
2. Select **OK**. If you want to review notes about this operation after it is completed, select **View Log** on the **Checking Out Drawings** dialog.

To undo the checkout, see Undo a Drawing Checkout.

**Check Out Dialog**

Displays the active Plant hierarchy and lists its drawings, allowing you to fetch a drawing from the specified database. This dialog appears when you select **Project** > **Check Out** or the **Check Out** button .

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

30/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Open Database**

Opens the **Projects** dialog, which allows you to specify a different project or the Plant.

**Filter**

Opens the **Filter** dialog, which allows you to specify the drawings that are displayed in the **List** view.

**Cancel Filter**

Deactivates any ad hoc filter you have applied to the **List** view.

**Include Subnodes**

Displays all the drawings and node names that reside in the currently selected node.

**List**

Displays the **List** view. The **List** view displays only one property for each drawing. To specify which property displays, select **Customize View** . The first item in the **Selected Properties** list is the property that appears in the **List** view.

**Details**

Displays the **Detail** view, which contains all the properties specified in the **Selected** **Properties** list on the **Customize Current View** dialog. Using the **Detail** view allows you to view and sort drawings by several attributes.

**Customize View**

Opens the **Customize Current View** dialog, which allows you to specify the information about each drawing that is displayed in the **List** view.

**Options**

Displays options specific to this check-out operation.

**Replace existing P&ID**

Overwrites the existing P&ID in the project if you have previously fetched a version of this drawing. If you have more than one drawing selected, at least one of them must exist in the project as a fetched drawing for this option to be available. If you are connected to SmartPlant https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

31/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Foundation and you have already fetched the drawing with read/write permissions, when you check the drawing out, the fetched version remains intact and only its status changes to checked-out.

**Create New Version**

Saves a new version of the drawing before overwriting the existing version. This option is not enabled if the current drawing does not already exist in the project. Also, if the drawing being checked out is already fetched to the project, you must first select **Replace existing P&ID** to enable the option.

**Comments**

Allows you to enter comments pertinent to this check-out operation.

**Checking Out Drawings Dialog**

Displays the progress of the version checking out operation currently underway. This dialog opens when you select **OK** on the **Check Out** dialog.

**Drawings**

Lists the drawings that are being checked out, and shows the status of that operation.

**View Log**

Opens the log file, CheckOut.log, which is created when you check out a drawing version.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

32/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Undo Checkout Command (Project Menu)**

Opens the **Undo Checkout** dialog, which enables you to return the drawing to the status of not being checked out without going through the process of checking the drawing in. This command is available only when you are working in the project that has the drawing in question checked out. You must select the checked-out drawing in the **List** view in order to use this command.

If you do not choose to remove the drawing from the project when you undo the checkout, the drawing remains in the project as a fetched drawing with read/write permissions.

If the project has claimed items on the checked-out drawing, then selecting **Undo** **Checkout** and using the **Remove from project** option, the software reminds you to release all claims prior to undoing the check out.

**Undo a Drawing Checkout**

1. In the **List** view in the project, select the checked-out drawing that you want to return to the Plant.
2. Select **Project** > **Undo Checkout**.
3. On the **Undo Checkout** dialog, choose an option for either retaining or completely removing the drawing from the project database.

**Undo Checkout Dialog**

Allows you to return the selected drawing to the Plant without going through the process of checking the drawing in. With the options on this dialog, you can choose to leave a fetched version of the checked-out drawing in the active project or to delete the drawing from the project database altogether. This dialog opens when you select **Project** > **Undo Checkout** on the main menu bar.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

33/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Remove from project**

Returns the drawing to the Plant and deletes it from the project. If the project has claimed items on the checked-out drawing, you must release all claimed items before you can undo checkout.

**Leave in project**

Returns the drawing to the Plant while leaving a fetched drawing with read/write permissions in the project.

**Compare Drawing Versions for As-Built and Projects** 1. In the **List** view, select the drawing.

1. Select **Version History** .
2. In the drawing list on the **Version History** dialog, select the version in the active project that you want to compare against a version elsewhere.
3. Select **Compare With**.
4. On the **Compare With** dialog, select the correct target project or the Plant database from the **Available Databases** list.
5. In the **History** list, choose the version of the drawing that you want to compare against your version and select **OK**.
6. On the **Compare** dialog, you can view the differences between the two versions, but you cannot make changes to the designs. To change the design, you must use Smart P&ID. For more information about using the compare-and-refresh capabilities inside Smart P&ID, see Comparing and Refreshing Versions in *Smart P&ID Help*.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

34/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

You can manipulate the views and navigate through the listed changes by using the commands on the **Compare** dialog toolbar. Each **Drawing** view also has its own shortcut menu, which includes manipulation commands that apply only to that view.

You can select an item in either **Drawing** view. The item is then located in the appropriate group in the **Change details** list. If you select an item in the **Change details** list, then you can use the **Find in Drawings** button on the toolbar to locate the item in one or both **Drawing** views.

You can select an item in the **Drawing** view or in the **Change details** list. Properties for that item appear in the **Properties** window. Selecting multiple items is not possible on the **Compare** dialog.

The following differences are ignored: claim status, select list strings, linked or embedded objects, symbology, and inconsistency indicators.

You can only compare a drawing against a version of itself; that is, you cannot compare one drawing to another drawing.

You can also compare versions when you are checking in a drawing. See Check In a

Drawing.

If you attempt to compare two versions that are actually identical to each other, the **Compare** dialog does not open and a confirmation message alerts you as to why.

**Returning a Drawing to the Plant Using Check In**

Checking in a drawing writes all of the changes made to the drawing by the project into the drawing stored in the Plant. When a drawing is checked in, all versions of that drawing are deleted from the project.

**Verification Processes Performed During Check In**

All objects that exist in the project but don’t exist in the Plant must be claimed.

All objects that exist in the Plant but don’t exist in the project (they were deleted) must have been claimed.

All objects that exist in both the Plant and the project must be identical if not claimed.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

35/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The claim state must be valid for the project.

If any claim on an object on this drawing is invalid, then check in cannot occur.

The timestamp on all objects that exist in the project must be earlier than or equal to the timestamp on the drawing.

Last Publish Date > Drawing date.

Check in is not allowed if drawing is in a **Re-create** state.

The **Verify for Checkin** command for new drawings should ensure that all items on the drawing have been claimed.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Check In Command (Project Menu)**

Enables you to check drawings into the Plant. This command is available only when drawings are selected in the **List** view and when those drawings are checked out to the current project. Drawings created in a project automatically belong to that project and can be selected and checked in. This command is not available from within the Plant.

You must have the correct permissions, assigned in Smart Engineering Manager, to check drawings in or out.

You cannot check a drawing in if any of the objects that belong to that drawing were modified after the latest version of a drawing was created. For more information about creating versions, see Save a Version of a Drawing.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Check In a Drawing**

1. In the **List** view, select the drawings that you want to check into the Plant.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

36/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Select **Project** > **Check In** or select on the main toolbar.
2. On the **Check In** dialog, select either **Keep checked out and maintain claims,** **Remove from project** or **Leave in project**. If you leave the drawing in the project, it becomes a fetched drawing with read/write permissions.
3. (Optional) Enter comments in the **Comments** box.
4. Select the **Compare** button if you want to compare the version you have selected to check in with other versions of the drawing. See Comparing Drawing Versions.
5. On the **Checking In Drawings** dialog, follow the progress of the operation. Select **View** **Log** if you want to review notes about this drawing check-in.

You cannot check in a fetched drawing. In order to check a drawing in, it must be checked out. For more information about checking out drawings, see Check Out a

Drawing.

If your current active database is the Plant database, you cannot check in drawings.

See *Connect to a Database* in the *Smart P&ID Drawing Manager Help*.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

37/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

When you check a drawing into the Plant, any claims on objects on that drawing are automatically released. See Claiming Items.

When you check a drawing into the Plant, your version of the drawing becomes the current version in the Plant. However, the version that was in the Plant already is automatically saved as the previous version.

You can select a checked out drawing and use the **Verify for Checkin** command to make sure claims and conflicts are resolved before you try to check in a drawing. See

Verify a Drawing for Checkin.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Related Drawings Dialog**

This dialog opens when you run the **Check In** command after selecting a drawing for check-in that is related to other drawings that were not selected. You must check in all related drawings together. To enable check-in of the selected drawing, close this dialog and select all the related drawings before running the **Check In** command.

**Check In Dialog**

Allows you to return ownership of drawings to the Plant. This dialog opens when you select **Project** > **Check In** on the main menu bar.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

38/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Remove from project**

Deletes the selected drawings from the active project’s **List** view and moves them into the Plant hierarchy.

**Leave in project**

Leaves a copy of the selected drawings in the active project’s **List** view and moves them into the Plant hierarchy. The version left at the active project is a fetched drawing in read/write mode.

**Keep checked out and maintain claims**

Checks in the selected drawings to the plant, but keeps the drawings checked out and maintains all claims to allow you to continue working on the drawings in the project. This option is enabled only when the **Enable “Keep Checked Out” on check-in** option is set to **Yes** in Options Manager.

**Comments**

Allows you to enter notes that apply to this check-in operation.

**Major revision**

Displays the new major revision for the selected drawings, if added.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

39/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Minor revision**

Displays the new minor revision for the selected drawings, if added.

**New Revision**

Opens the **New Revision** dialog and allows you to add a revision for the drawings prior to check-in. The values that you enter appear in the **Major revision** and **Minor revision** boxes.

**Compare**

Performs a comparison between the latest versions of the drawings in the active project and As-Built. The **Compare** button is not available when you have selected more than one drawing for check-in or if no drawing version exists in As-Built for the selected drawings.

**Checking In Drawings Dialog**

Displays the status of the check-in operation and allows you to review notes on the task. This dialog opens when you select **OK** on the **Check In** dialog.

**Drawings**

Lists the drawings that you selected to check into the Plant and displays the progress of the process through the list.

**View Log**

Allows you to review the log file for the check-in operation when the task is finished.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

40/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Verify a Drawing for Checkin**

1. Select the project in the **Tree** view.
2. In the **List** view, select the checked-out drawings that you want to check into the Plant.
3. Select **Project** > **Verify for Checkin**.
4. On the **Verifying Drawings for Checkin** dialog, observe the progress of the verification operations. Select **View Log** if you want to examine notes on the operation.

After verifying the drawing for checkin, check the drawing into the Plant as soon as possible because the verification process does not freeze the drawing state and the changes can be made to the drawing during any interim time between verification and actual check in. See Check In a Drawing.

You cannot check in a fetched drawing, it must be checked out first. You can, however, check in a new drawing created in the project. See Check Out a Drawing.

Verifying a drawing for checkin checks exactly the same drawing conditions as the **Check In** command, but without actually checking the drawing into the Plant.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Verification Processes Performed During Check In**

All objects that exist in the project but don’t exist in the Plant must be claimed.

All objects that exist in the Plant but don’t exist in the project (that is, they were deleted) must have been claimed.

All objects that exist in both the Plant and the project must be identical if not claimed.

The claim state must be valid for the project.

If any claim on an object on this drawing is invalid then check in cannot occur.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

41/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The timestamp on all objects that exist in the project must be earlier than or equal to the timestamp on the drawing.

Last Publish Date > Drawing date.

Check In not allowed if Drawing is in a **Re-create** state.

The Verify for Checkin for new drawings should ensure that all items on the drawing have been claimed.

**Verify for Checkin Command (Project Menu)**

Checks the selected drawing to see if there are any conditions that would keep it from successfully being checked into the Plant. For a list of items or issues checked during the verification process, see Returning a Drawing to the Plant Using Check In.

If the drawing fails this verification, select the **View Log** button on the **Verifying Drawings for** **Checkin** dialog and review the items listed there.

Even though a drawing passes verification, the state of the drawing is not then frozen.

Subsequent actions can cause a drawing not to be ready for checking in. If your drawing is verified and you do want to check it into the Plant, then you should do so as soon as possible after verifying it for checkin.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify** **for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Verifying Drawings for Checkin Dialog**

Displays the progress of the version verification operation currently underway. This dialog opens when you select **Project** > **Verify for Checkin**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

42/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that are being verified for checkin, and shows the status of that operation.

**View Log**

Opens the log file that is created by the verification process.

**Reviewing the Drawing Status**

Checking the drawing status allows you to see which projects that have fetched or checked out the selected drawings.

**Check Drawing Status**

1. In the **List** view, select a drawing.
2. Select **Project** > **Drawing Status** or select on the toolbar.
3. Review the information on the **Drawing Status** dialog.

**Drawing Status Command (Project Menu)**

Displays the projects that have fetched or checked out the selected drawing. This command is available in the Plant and in any of its projects. You can select more than one drawing and display their statuses at the same time.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

43/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The **Drawing Status** dialog displays information about the project and the user who changed the status, the time of the change, and any comments that were added during the status change. These comments can be entered during any status-changing operations, such as fetching, checking out, checking in, and undoing a checkout.

**Drawing Status Dialog**

Displays information about the project and user that changed the drawing status, the time the status was changed, and any comments that were added when the status was changed.

Status changing operations include checking out, checking in, fetching a drawing, and undoing a checkout. This dialog opens when you select drawings in the **Tree** view and then select **Project** > **Drawing Status**.

**History**

Displays the pertinent information about the selected drawings.

**Editing Drawing Items Within a Project**

New items can be created in a project drawing using Smart P&ID. As these items are added to the drawing, they are automatically claimed by the project. If your edits to an item cause related items to be modified, those related items must be claimed also. Moving items and adding labels, for example, can be accomplished without claiming.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

44/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

When an existing drawing is fetched or checked out to a project, none of the items are claimed. You will not be able to modify or delete any items until they are claimed. Use the **Claim** command to define the scope for your project. Claim modes include Exclusive and Shared. Exclusive mode allows only a single project to claim an item. Using Shared mode, multiple projects can claim the same item at the same time.

You can compare your current drawing with a previous version to locate any differences.

These differences display as change groups. The change group contains a list of changes that can be made in the current drawing and still maintain consistency. You can then choose to accept the changes, if needed. Each change group is marked if it affects items you have claimed. You should accept, or refresh, all of the changes that do not involve items claimed by you because these items represent changes checked in by other projects. See Comparing and Refreshing Versions

Items must be claimed before you can delete them. If deleting an item results in changes to related items, then those related items must be claimed also.

**Claiming Items**

A project in the Plant frequently deals with a subset of items within a drawing. The Claim functionality provided by Smart P&ID allows you to grant control of an item to a project.

Because claiming makes it possible for a project to work on an item-by-item basis, claiming fosters an ability to define the scope of work as narrowly as necessary.

A new item is created in a project in the same ways it can be created in a greenfield plant (not applicable for Smart P&ID Engineering). The simplest way to create a new item is to drag a catalog item from the Catalog Explorer** **and drop it onto a drawing. A new item in a drawing is automatically claimed to the project.

However, when an existing drawing is fetched or checked out to a project, none of the items on that drawing are initially claimed. Before you can modify any of those items, you must claim them.

After you have claimed an item, you can modify it using the same methods that you would use in a plant that is not project enabled. Purely graphical modifications to drawing items are allowed without claiming those items (not applicable for Smart P&ID Engineering). For example, a symbol can be repositioned or the vertices of a connector can be moved. Also, labels can be added or removed without claiming anything.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

45/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Any modification that changes the meaning of the schematic design (not applicable for Smart P&ID Engineering), however, requires that the affected items be claimed. For example, if you break a pipe run, some of the piping components and inline instruments in that pipe run will be reassigned to the new pipe run. Therefore, the pipe run, the piping components and the instruments in that pipe run must all be claimed before you break it. If they are not claimed, an error message will be displayed.

Properties of items that are not claimed by the active project cannot be changed. In the Smart P&ID modeler, the mirror and rotate handles are not available for any item you select that was not claimed by your project. The **Properties** window and the **Engineering Data Editor** do not allow editing of properties on items that are not claimed: the properties are read-only as if the drawing is in a read-only state. No other explicit prompts let you know that you cannot edit an item that you have not claimed. However, you can manipulate the **Drawing** view properties so that the claim state of items is visually apparent.

System Editing does not allow property values to flow to unclaimed objects. If you have a claimed object that is connected to some unclaimed objects, and if you change a property on the claimed object, propagation will not change the property value on the unclaimed objects.

The items in the propagation scope are initially collected using the standard propagation rules. However, all unclaimed items are removed from the propagation scope before any property values are changed.

Items that are claimed for relationship are treated as unclaimed for the purpose of propagation.

You cannot delete items that have not been claimed (not applicable for Smart P&ID

Engineering). After you have claimed an item, you can delete it using the same methods that you would use in a greenfield plant. However, if the deletion of an item would result in related items being deleted or modified, then those related items must also be claimed. For example, if you delete a vessel, the nozzles attached to it will be deleted and the pipe runs connected to the nozzles will be modified. Therefore, the vessel, the nozzles and the pipe runs must all be claimed before you delete the vessel. If they are not claimed, an error message will be displayed.

You do not need to check out a drawing to claim objects; you can fetch a drawing with read/write permissions and claim its objects. Claim commands appear on shortcut menus in the **Drawing** view, in the **Engineering Data Editor**, and on the **Edit** menu.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

46/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Releasing Claims**

From inside a project, you can invoke a claim at any time to expand the scope of your project, and any new item created in a project is automatically claimed by that project. You can also release a claim at any time, but you cannot release the claim that is automatically created when your project creates a new item.

Claims are automatically released on all drawing items when that drawing is checked into the Plant; however, a drawing cannot be checked in if any objects that are *not* claimed differ from the Plant.

**Claim Mode**

The claim mode can be set to either **Exclusive** or **Shared** by using the **Settings** option in Smart P&ID Options Manager. The claim mode controls how items are claimed by concurrent projects.

If the claim mode is set to **Exclusive**, only one project can claim an item at any given time.

Exclusive mode enforces the rule that concurrent projects do not overlap at the object level. With this setting, conflict resolution at check in time is simplified.

If the claim mode is set to **Shared**, a single item can be claimed to more than one project.

Shared mode allows concurrent projects to overlap at the object level. This setting might be required for plants that have overlapping projects. Conflict resolution at check in time will be more complex.

**Invalid Claims**

When an item is claimed by a project, it must be consistent with the state of the item in the Plant. Otherwise, an invalid claim exists. Invalid claiming can happen only for Plants that support shared claiming of database items. Invalidly claimed items differ from the Plant items in that you cannot check in a drawing to the Plant without first establishing a valid claim on items that have been modified.

When the Plant uses Shared claim mode and a project checks in a drawing, the claims made by other projects to objects on that same drawing are now invalid if the project that checked in the drawing also changed an item claimed by a different project.

You can determine the validity of a claim by using the **Claim Status** command.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

47/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify** **for Check In** to resolve the situation. This process automatically sets the claim to valid and allows the check in to occur.

**Partial Claim**

When a claimed item has a relationship with another item that has not been claimed, any change made to the claimed item that also changes the relationship, causes the non-claimed item to receive Partial Claim status, denoted by . Partial Claim status only applies to objects connected to pipe runs (inline components such as instrumentation and piping components).

Partial claim works automatically when a claimed pipe run is ‘broken’. There is a routine that determines which side of the broken pipe run gets the new GUID and which side maintains the original GUID. Inline components on the side that gets the new GUID receive Partial Claim status, which is only for the purpose of changing their database relationship to the pipe run with new GUID. Data cannot be edited on items that are ‘claimed for relationship purposes’.

A list of claimed items is automatically published to SmartPlant.

Claim commands are not available when you open a fetched drawing with read-only permissions.

Claiming of labels is ignored.

Drawing Manager is the only tool for checking in, checking out, and fetching drawings.

You must have full control user access permissions for P&ID objects before you can claim objects. See *Smart Engineering Manager*  Help.

Objects are claimed by the *project*, not by a single user. After a project claims an item, it can be modified by anyone with the appropriate permissions in that project.

In Exclusive claim mode, the software allows the user to claim all the selected items that were not already claimed by other projects. The claim log shows which items could not be claimed because they were already claimed by other projects.

Claiming items clears the Undo stack. Thus, claiming is not a command that can be undone.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

48/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Enforcing Claims**

Whether you are using shared or exclusive claiming mode, claiming objects to your project involves many special relationships. The following topics discuss some of the ways that claiming restricts your activities.

The claim mode (Exclusive or Shared) is defined in Options Manager for the Plant and all its projects. When you claim an item, it is claimed to your active project. No items are ever claimed by the Plant.

**Controlling Access**

Each command in the software checks your permissions for the items that it modifies. When possible, commands simply do not allow the operation to proceed if you do not have the necessary permissions. In cases where the software cannot prevent you from initiating a command, an error message is displayed.

You must have full control permissions on P&ID Objects before you can claim any drawing items. See User Access in *Smart Engineering Manager Help*.

**Modifying Properties**

Claiming impacts properties modifications in the following manner.

**Properties Window**

When you select a claimed item, the **Properties** window allows the properties of that item to be viewed and modified. When you select an item that has not been claimed, the **Properties** window allows the properties to be viewed but not modified. The properties of unclaimed items are read-only.

When you select a line segment, the **Properties** window displays the properties of the associated pipe or signal run. If the run has been claimed, the properties can be edited; otherwise, the properties are read-only.

When you select multiple items, if they are all claimed, the **Properties** window allows them to be modified. If any of the selected items are not claimed, the **Properties** window treats the whole group as read-only.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

49/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Engineering Data Editor (EDE)**

If the item has been claimed, you can edit its properties through the EDE; otherwise, the EDE

treats the item properties as read-only. The EDE behaves similarly to the **Properties** window.

**Consistency Check Dialog**

The **Solutions** section of the **Consistency Check** dialog allows you to copy property values from one item to another. For the selected solution, if the destination item is not claimed, the **Apply** button is not available.

**Implied Items**

When a drawing item is claimed, it means that you can modify that model item and all of its implied items. If a model item is not claimed, the user cannot modify any of the implied items that the model item owns.

**Placement Rules**

When a new relationship is created, such as when you place a nozzle on a vessel, the applicable rules copy property values across the relationship. When a relationship to an unclaimed item is created, properties can be copied *from* that item without any problem; however, if the rule calls for properties to be copied *to* an unclaimed item, the action is not allowed, and the properties are not copied. An inconsistency indicator shows the inconsistency between the two related items.

**Placing and Moving Drawing Items**

Sometimes the target item must be claimed, but other times it does not have to be claimed.

The following list explains how the relationship between an object and its target effects claiming.

**Placing Nozzles**, **Equipment Components**, **Room Components**, or **Instrument** **Components**: The target item does not need to be claimed.

**Placing Piping Components or Instruments in Pipe or Signal Runs**: The target run must be claimed. In certain cases, placing a piping component or inline instrument causes a zero-length line segment to be created and automatic line connectivity causes it to be joined to an existing run. The target of that zero-length line must be claimed.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

50/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Placing Reducers**: A reducer is a “line-breaking component”. The target pipe run and all of its components must be claimed.

**Placing Flow-Oriented Components**: A flow-oriented component sets the flow direction of the target process run, if it is not already set. The target process run must be claimed. You can place a flow arrow label, however, if the flow direction is already defined.

**Placing OPCs on Runs**: The target connector must be claimed.

If the target item needs to be claimed but is not claimed, then you cannot place your item onto the target; the target will not highlight, and your item will not “snap” into position. If no type of placement is allowed at that point, the “no place” indicator is displayed. In most cases,

freestanding placement is still allowed.

**Geometric Modifications**

Geometric operations include a geometric move, with the ALT key pressed where necessary, a rotation, a mirroring, and a scale or parametric modification. The selected symbol does not have to be claimed to perform these operations. None of the connected items have to be claimed either.

**Rotation and Mirroring of Inline Components**

Rotations of 180 degrees and mirroring about the local y-axis for inline components are special geometric modifications cases because the lines are disconnected before and reconnected after the operations. Therefore, the lines, but not the selected symbol, must be claimed before these operations are allowed. If the lines are not claimed, the standard claim violation message displays.

**Rule-Based Moves**

All connected items must be claimed, as described above. If the required connected items are not all claimed, the move operation can become a geometric move, as if you pressed the ALT

key.

**Placing and Modifying Lines**

Sometimes the target item must be claimed, sometimes not. Here is a list of the cases where claiming plays a role:

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

51/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Routing Lines up to Nozzles**:The nozzles do not have to be claimed.

**Routing Lines up to Freestanding Piping Components or Instruments**: The piping component or instrument must be claimed because it will be adopted by the new run.

**Routing Lines up to Owned Piping Components or Instruments**: The piping component or instrument does not have to be claimed. In certain cases, when routing a line segment up to an existing inline component, automatic line connectivity will cause an existing zero length run to be joined to the new run. The target run must be claimed.

**Routing Lines up to OPCs:** The OPC does not have to be claimed.

**Routing Lines up to Another Pipe or Signal Run:** The target run must be claimed.

If the target item needs to be claimed but is not claimed, you are not allowed to connect to the target. The black connection handle does not appear at the required point.

**Geometric Modification**

If you move a line segment or a line vertex that is internal to a line, then the piping or signal run that owns the selected segment does not have to be claimed.

**Extreme End of a Run**

If you modify the start point of the first line segment in a run or the end point of the last line segment in a run, then the following stipulations apply: 1. The selected run must be claimed.

1. The target item might need to be claimed.
2. If the existing connected item is a branch point for the run, then the run it belongs to must be claimed because the branch point is deleted and the adjacent line segments in the existing connected run are merged.
3. If a component is connected to the endpoint, it does not need to be claimed.

**Internal Vertex of a Run**

Modification of an internal vertex can result in the run being split; consequently, the following stipulations apply:

1. The entire run and all components must be claimed.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

52/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. The target item might need to be claimed.

**Breaking and Joining Runs**

The **Break Run** command allows you to split one piping or signal run into two pieces. The run to be broken and all components within that run must be claimed.

The **Join Runs** command allows you to combine two connected piping or signal runs into a single run. Both of the runs and all components in both runs must be claimed.

**Placing and Modifying Labels**

The target item for a label usually does not need to be claimed. However, claiming plays a role in the following cases:

**Placing Driving Labels**

A driving label sets one or more properties on the labeled item. The target item must be claimed. This includes flow arrow labels, unless the flow direction is already defined for the process run.

**Placing Labels on Area Breaks**

Placing a label on an area break causes a dynamic property to be added to the area break.

For this to happen, the area break must be claimed.

If you modify a label, you do not need to claim it. However, modifying a driving label modifies the labeled item. Therefore, you must claim the item.

Deleting a driving label nulls the value on the related object.

**Place Multiple Representations Command**

This **Stockpile** command enables you to place an additional representation of an existing equipment item into the design in a different drawing, thus creating a multiple representation in the database. You must claim the selected equipment item before this command is made available on the **Stockpile** menu in the EDE.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

53/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Placing and Modifying Area Breaks**

The placement of an area break does not create any new relationships and therefore does not require any claiming. Modifying an area break allows the shape to be changed. This is a purely geometric modification, and so no claiming is required.

**Placing Gaps**

Placing a gap symbol into a piping or signal line implies that the target line must be claimed. If the target line run is not claimed, it is not highlighted as a valid target when you move the pointer over it.

**Replacing Drawing Items**

The **Replace** and **Replace Mode** commands replace one item representation in the design with a different representation and change the value of the “type” attribute for the design item.

To replace an item using these commands, you must claim that item.

**Replace Mode**

The claim status check takes place as you move the pointer over the target. If the target is not claimed, the target is not highlighted as a valid replacement target.

**Find and Replace**

Items that are not claimed can be found, but they cannot be replaced. The **Replace** button is not available if an unclaimed item is selected.

**Deleting Items**

Claiming impacts item deletion in the following manner.

**Drawing Items**

Drawing items are deleted from a design using a number of different commands: **Delete to** **Stockpile** > **Plant**, **Delete to Stockpile** > **Drawing**, **Delete from Model**, and **Cut**. When implementing these commands, all dependent items must be claimed. That is, all items that are to be deleted along with a selected item must be claimed. Any lines attached to or dependent on selected items must be claimed. If any attached or dependent items are not claimed, an error message appears if you attempt to delete them.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

54/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

It is not permitted to delete an item that has an invalid claim status. If you attempt to delete one or more items on a drawing that have invalid claims, the deletion will fail for those items and an error message will be displayed. The SP_ID and Item Tag for those items will be logged in the Smart P&ID log file.

The following table lists dependent items which must be claimed, item type by item type.

**Item in Select Set**

**Additional items that must be claimed for Delete**

Equipment

All nozzles, equipment components, and item notes

All item notes on those equipment components and nozzles All runs with lines attached to those nozzles

Nozzle

All item notes

All runs with lines attached to the nozzle

Equipment Component All item notes

Room

All nozzles, room components, and item notes

All item notes on those room components and nozzles

All runs with lines attached to those nozzles

Room Component

All item notes

Line Segment

The pipe or signal run that owns the segment

All components in that run

Branch Point

All runs with lines that attach to that branch point https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

55/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

All item notes

Piping Component

All item notes

All runs with lines that attach to that piping component Instrument

All instrument components – actuators, functions, and so forth All item notes

All runs with lines that attach to the instrument

OPC

All item notes

All runs with lines that attach to the OPC

The partner OPC must be claimed also

**Stockpile Items**

Most items in the stockpile do not have any relationships. For these items, if the item is claimed, it can be deleted from the stockpile. If the item is not claimed, the **Delete** command opens the standard claim violation message.

Plant item groups, for example loops, packages, and so forth, exist in the stockpile and have relationships to member items on a drawing or in a stockpile. If the plant item group is claimed and all of its members are claimed, then the plant item group can be deleted. If the plant item group or any of its members is not claimed, the **Delete** command opens the standard claim violation message.

When an OPC is in the stockpile, it maintains its relationship to the partner OPC. OPCs can be deleted from the stockpile only if both OPCs in a pair are in the stockpile and are deleted at the same time. In a project context, both OPCs in a pair must be claimed before they can be deleted.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

56/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Moving Between Stockpiles**

The Move to Different Stockpile command in the Engineering Data Editor allows you to move an item from one stockpile to a different stockpile. The selected model item must be claimed before you can use this command (if you are using a Project).

**Validating Properties**

The software uses validation functions before setting properties on items. The software checks the claim status before setting any values. If the item is claimed, the property can be changed. If the item is not claimed, the property cannot be changed. For more information about validating properties, select **Start** > **Programs** > **Intergraph Smart P&ID**

**Programming Help** and see the *Extending the Capabilities of Smart P&ID* and *Logical Model* *Automation Reference* topics.

You can use the validation and calculation functions on drawing item type. The software uses the same automation interface managing all other item types.

**To Do List and Correlating Items**

Claiming impacts the To Do List and other SmartPlant commands in the following manner.

**Create Task**

Running a Create task creates a new item in the stockpile. The new item is claimed automatically as soon as it is created.

**Update Task**

Running an Update task sets or changes some properties of an existing item. The item to be updated must be claimed before it can be updated. If it is not claimed, the task status is set to **Error** and a note is added to the **Notes** area on the **General** tab of the **Task Properties** dialog.

**Delete Task**

Running a Delete task causes the target item to be deleted. The item to be deleted and possibly other related items must be claimed before the task can do its work. If all of the necessary items are not claimed, the task status is set to **Error** and a note is added to the **Notes** area on the **General** tab of the **Task Properties** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

57/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Correlate Item**

The **SmartPlant** > **Correlate** command correlates pipe runs to the same design basis as an existing pipe run that is already correlated. Properties are copied from the primary pipe run to the other pipe runs. You must claim the pipe runs to be modified. If they are not claimed, they cannot be correlated.

Creating or deleting tasks is not allowed in Smart P&ID Engineering.

**Reviewing a Claim Status**

Use the **Claim Status** command to see if an item has been claimed. This command displays a dialog that shows if the item is claimed by this project or by any other project and, if it is claimed, the date of the operation, the name of the user and any related comments.

Another way to see which items are claimed is with the **Show Claims** command, which paints the items on the drawing with different colors depending on whether the item has been claimed. The typical way to configure the colors is to show unclaimed items in a light gray color and claimed items with their normal symbology. With the **Show Claims** switch turned on, you can very quickly see what is claimed and what is not.

**Display the Claim Status of a Drawing Item**

1. In the Drawing view or **Engineering Data Editor**, select the items for which you want to display the claim status.
2. Select **Edit** > Claim Status to display the Claim Status Dialog.
3. Review the information in the list of items.
4. To claim the items to your project, select elements in the list and select **Claim**.
5. To relinquish claims on those items by your project, select elements in the list and select **Release Claim**.
6. To see more detailed information about the claim status of that item, the project that has claimed the item, the user who claimed it, and any related comments, select an element in the list and select **Details**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

58/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Claim Status Dialog**

Opens when you select one or more items and select **Edit** > **Claim Status** on the main menu bar. You can review the details of the claimed state of the selected items, claim items, release the claims to items, and discover other details of the claim status. To perform an action on an item (claim, release claim, or show details), you must first select the row of the item. Hold down CTRL or SHIFT to select multiple items.

**Item Tag**

The tag that identifies the item. If a selected item that appears in this dialog does not have an item tag, the value is blank.

**Item Type**

The item type to which the item belongs, for example: Mechanical, Nozzle, PipingComp, SignalRun.

**Claimed**

Indicates the claim status of items claimed in the current project. An item claimed by your active project is denoted by ; an item with an invalid claim on it is denoted by ; an item which has a relationship with another item that has been claimed, but which itself was not explicitly claimed is denoted by (partial claim); otherwise, this field is blank.

**Claimed by Others**

Indicates the claim status of items claimed by other projects. The symbols are the same as for the **Claimed** column. If you are working in ‘Exclusive mode’, you cannot claim an item that is already claimed by another project.

**Claim**

Opens the **Claim** dialog, where you can claim the item and record claim comments.

**Release Claim**

Releases the claim from your project. A confirmation message is displayed; choose **Yes** to release the claim.

**Details**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

59/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Opens the **Details** dialog, where you can discover what project has claimed the selected item, the user that claimed it, and any claim comments that were entered when it was claimed.

**Details Dialog**

Displays details about the claim status of the item that you selected in the **Claim Status** dialog. You can discover the project that has the claim, the user that claimed the item, and claim comments that were entered when the claim was made. Because newly placed items are automatically claimed by the project that places them, their claim comments are always

“New Item”. This dialog opens when you select **Details** on the **Claim Status** dialog. You can select all the items in the list by using CTRL + A, and using CTRL + C makes the selected items available to paste into another document.

The **New Item** entry is automatically added to the comments for an item that is new to the drawing. New items are automatically claimed to the project that created them.

**Show Claims Command (View Menu)**

Sets the appearance of drawing objects as it is specified in the **Claims** tab of the **View** **Properties** dialog. You can use this command to switch the claim symbology on and off.

Using the options on the **Claims** tab causes only the color and line weight to change, not the line pattern.

**Display Claim Status in the Drawing Symbology**

1. Select **View** > Show Claims.
2. Select **View** > Show Claims again to turn off the display of claim status in the symbology of drawing items.

You can define the line color and weight used to designate claim status on the **Claims** tab of the **View Properties** dialog.

If you turn on the display of claim status in the drawing, then when you print the drawing, the claim status will be plotted.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

60/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Releasing a Claimed Item**

If an item is initially claimed by a project, but then later it is decided that the item does not need to be modified, you can remove the item from the project scope using the **Release** **Claim** command. New items that are automatically claimed when they are created cannot be *unclaimed* with this command.

**Release Claim Dialog**

Opens when you select an item and select **Edit** > **Release Claim** on the main menu bar and displays details of the items that you select to be released from claiming.

**Items to be released**

Lists the items that are selected in the Drawing view or **Engineering Data Editor** and their details. These are the items that you release from your project when you select **OK**. You can also select multiple elements of this list. In this list, you can also see if a selected item has not been claimed nor does it have any other errors or warnings associated with it.

**Release a Claim**

1. In the Drawing view or **Engineering Data Editor**, select the items for which you want to release claims.
2. Right-click the item or select set and select **Release Claim**. If there are any errors or warnings during the release, the Release Claim Dialog displays. Review any warnings and error messages about each item.
3. Select **OK** to complete the claim release operation.

After setting the claim mode to **Release Claim**, the status of the items still remains behave exactly in the same way as the scoped items as the software re-scopes them.

You cannot release the claim on an item that is claimed to your project if it is a new item that was created in your project.

You can also release claims on items when you display their claim status. See Display

the Claim Status of a Drawing Item.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

61/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

You can only release the claim on an item in the **Engineering Data Editor** if that item belongs to the active drawing.

**Viewing Overlapping Drawings**

When a drawing is fetched or checked out to multiple projects, changes might be made simultaneously to the same object(s). The **Show Overlapping** feature allows you to compare a drawing in different projects by displaying the drawing views on top of each other. Any newly placed or modified object can thus be easily identified, and the drawing can then be edited to avoid positioning conflicts.

The **Show Overlapping** command can be executed from Smart P&ID Drawing Manager or from the Smart P&ID Modeler. In both cases, the overlapping view opens in the Smart P&ID

Modeler. To enable the **Show Overlapping** command in Smart P&ID Drawing Manager, select any drawing in the List view.

When you execute the **Show Overlapping** command, the software fetches the latest .pid files from the selected projects and displays the overlapping view in the Smart P&ID Modeler in the display color selected on the **Overlapping** dialog. Each project displays on a separate tab.

Overlapping drawings can be viewed for a maximum of 15 projects including your currently active project and the As-Built plant.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

62/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The **Show Overlapping** command is enabled after you select a drawing from the List view in Drawing Manager.

You cannot edit the drawings in the overlapping view. To edit, you must open them from the Smart P&ID Modeler.

The overlapping view will only display the most recently saved changes.

**Show Overlapping Command (View Menu)**

Generates an overlapping view of the drawing for the projects selected. The **Overlapping** dialog allows you to select projects and assign display colors to them.

**Overlapping Dialog**

Lists all projects to which the selected drawing is fetched or checked out. Each project is listed with a checkbox and a default display color. You can select the projects to be included in the overlapping view and assign display colors to them.

Overlapping drawings can be viewed for a maximum of 15 projects including your currently active project and the As-Built plant. For any project, the default display color can be changed to a unique color of your choice. Unique display colors aid in identifying new or modified objects in different projects.

**Select**

Allows you to select the projects for the overlapping view. Your currently active project is selected by default and cannot be deselected.

**Project Name**

Indicates the name of the project to which the drawing is fetched or checked out.

**Display Color**

Shows the default display color assigned and allows you to choose a different color, from the color palette.

The **OK** button is activated when you select at least one project in addition to the currently active project that is selected by default.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

63/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Display Overlapping View for a Drawing**

1. Select a drawing from Drawing Manager, or open a drawing from Smart P&ID Modeler.
2. On the **Main** toolbar, select

.

1. In the **Overlapping** dialog, select two or more projects, up to a maximum of 15.
2. Accept the default display color or change it by selecting the drop-down arrow and selecting a color from the color palette displayed.
3. Select **OK**.

The overlapping view opens for the selected projects with a **Legend** box, representing the color code for each project.

In the **Design** window, each project in the overlapping view is displayed on a separate tab. Your currently active project is displayed on the first tab.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

64/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Deactivating a Project in the Overlapping View**

You can hide a project from the overlapping view by deactivating the tab. Objects specific to that project will then not be seen in the overlapping view.

To deactivate, hold **Control** key and select a project tab (**CTRL + Click**).

To reactivate the project, use the same method. You cannot deactivate all the projects in the overlapping view. At least one project must remain active.

Selecting a project tab displays the drawing in that project on top, moving the rest of the drawings to the background. All objects in the currently selected project will be displayed in the project’s assigned color. Objects that exist only in other projects or objects that have been moved will be displayed in the colors assigned to their respective projects.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

65/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Legend Box**

The **Legend** box representing the display color used for each project appears at the bottom right side of the overlapping document based on a D-size template. For other templates, it might not appear at this position.

The **Legend** box can be moved, resized or hidden.

**To move**: Double-click the **Legend** box and drag and drop it at your desired location.

**To resize**: Double-click the **Legend** box, position the mouse pointer over one of the item handles and click-and-drag the handle.

**To hide**: Right-click the overlapping document and clear the selection **Show Overlap View** **Legend**.

The **Legend** box is attached to the currently active project tab. It will not be seen in the overlapping document when you deactivate the currently active project tab.

You cannot make changes to the drawing in the overlapping view. However, the following commands from the **View** menu are available for use: Previous Command

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

66/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Zoom Area Command

Zoom In Command

Zoom Out Command

Fit Command

Pan Command

Show Grid

**Print Overlapping View**

The **Print** feature functions for the overlapping view as it does for the drawing itself.

All active tabs will be printed with projects in their respective colors, as displayed in the overlapping view, unless different settings are chosen in the **Print** dialog.

The following commands in the **Print** dialog are not applicable to the overlapping document: Selection

All

Collate

**Sample Project Workflows**

The following scenarios provide workflows for using projects in various configurations. You must perform the activities below before executing the workflows.

1. In Smart Engineering Manager, do the following:
2. Create a site.
3. Create a plant.
4. Associate the application.
5. Create plant groups that allow drawings.
6. In Smart P&ID Drawing Manager, create new drawings A - E and G, as shown.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

67/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. In , do the following:
2. Open Drawing A.
3. Create Assembly A-1 and assign the item tags as shown.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

68/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Choose vessel type **Equipment** > **Vessels** > **Vertical Drums** > **Short 1D 1C**

**1to1**.

Place both OPC partners in the Plant Stockpile.

1. Make the assembly available in Catalog Explorer by opening Options Manager and running the **Tools** > **Generate Symbol Images** command.
2. Open Drawings B, C, D, and G and place Assembly A-1 in each of the drawings.

*The software assigns unique item tags to the vessel, pipe runs, and OPCs in each* *drawing.*

1. Open Drawing E and place the instrument OPC partner from Drawing D.
2. In Smart P&ID Drawing Manager, create a version of Drawing G and make a note of the version number (1).
3. In Smart Engineering Manager, do the following:
4. Enable projects for the plant.
5. Create three projects: Project 1, Project 2, and Project 3 and for each, set the Project Scope at the level of the unit in which you created the drawings.
6. Define Roles for each of the projects if not defined already.
7. In Smart P&ID Options Manager, under **Settings**, set the **Claim Mode** option to **Shared**.

**Undo a Checkout**

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing A from the Plant.
2. Open Drawing A.
3. Claim Vessel V-100.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

69/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Find and replace Vessel V-100 with a 1 to 1 Parametric V Drum.
2. Exit Drawing A.

*Drawing A becomes Drawing A’.*

1. In Project 2, fetch Drawing A’ from Project 1.
2. In Project 1, execute the **Undo Checkout** command on Drawing A’, leaving Drawing A’

in Project 1.

1. In Project 2, open Drawing A’.
2. Claim Nozzle N1.
3. Change the Tag Sequence Number of the nozzle to 4.
4. Exit Drawing A’.

*Drawing A’ becomes Drawing A’’.*

1. Check out Drawing A from the Plant to Project 2 *without replacing the existing P&ID*.

*Drawing A becomes Drawing A’’.*

1. In Project 2, attempt to check in Drawing A’’.
2. View the check in log file.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

70/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

*Unclaimed changes prevent check in.*

1. Open Drawing A’’.
2. Claim Vessel V-100.
3. Exit Drawing A’’.

*Drawing A’’ becomes Drawing A’’’.*

1. Check in Drawing A’’’ with removal of the drawing from the project.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

71/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an**

**arrow indicates changes to the drawing or**

**to drawing item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Undo drawing check-out**

**Refresh: Modify a Drawing Concurrently in Two Projects** Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing B from the Plant.
2. Open Drawing B.
3. Fence select all items and claim the selected items.
4. Exit Drawing B.
5. In Project 2, fetch Drawing B from the Plant.
6. Open Drawing B.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

72/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Fence select all items except both OPCs and claim the selected items.

*The claim status for the items indicates that they have already been claimed by another* *project.*

1. Change the Tag Sequence Number for the vessel to **110**.
2. Change the Construction Status of the vessel from **New** to **Existing**.
3. Exit Drawing B.

*Drawing B becomes Drawing B’.*

1. In Project 1, open Drawing B.
2. Place an Area Break around the vessel and Nozzle N1.
3. Place an Alt Dgn Press-Temp Equipment Label on the Area Break.
4. Select the Area Break, right-click, and on the shortcut menu, select **Select Contents**.
5. In the **Properties** window, if you cannot see the pressure and temperature properties, select **Show Case Data** for the Select Set to display those properties.
6. Assign **Alt Dgn Max Press** of **100 psi**.
7. Assign **Alt Dgn Max Temp** of **101 F**.
8. Exit Drawing B.

*Drawing B becomes Drawing B’’.*

1. In Project 1, check in Drawing B’’ with removal of the drawing from the project.
2. Select **Project** > **Project Status**.
3. Select **Complete Project**.
4. Select **Merge Project** to merge Project 1 into the Plant.

If you complete and merge Project 1, you will not be able to use it for the other workflows unless you delete and re-create Project 1. If you want to continue without deleting and re-creating the project, you should skip both the Complete and Merge operations until you have completed all of the workflows.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

73/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. In Project 2, check out Drawing B’’ *without replacing the existing P&ID*.

*Drawing B’’ becomes Drawing B’ in Project 2.*

1. In Project 2, attempt to check in Drawing B’.

*Invalid Claim prevents check-in.*

1. In Project 2, open Drawing B’ and compare it with the drawing in the Plant.
2. Do the following:
3. Refresh Drawing B’ for the Area Break and label and all other differences that result in invalid claims (see Compare and Refresh Drawing Versions).
4. Place a Revision Cloud around the Control Valve (FV-…) and the Actuator (ACT-…).
5. Place a Revision Triangle on the Revision Cloud. Label the Revision Triangle RT-1.
6. Exit Drawing B’.

*Drawing B’ becomes Drawing B’’’.*

1. Check in Drawing B’’’.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

74/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

75/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Continuity between procedure steps (an**

**arrow indicates changes to the drawing or**

**to drawing item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Fetch a Deleted Drawing**

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Drawing Manager, select Project 1 and check out Drawing C from the Plant.
2. Open Drawing C.
3. Claim Flow Indicator FI-100.
4. Change the Tag Sequence Number of the Flow Indicator from 100 to 101.
5. Exit Drawing C.

*Drawing C becomes Drawing C’.*

1. In Project 2, fetch Drawing C from the Plant.
2. Open Drawing C.
3. Claim Flow Indicator FI-100.
4. Change the Tag Sequence Number of the Flow Indicator from 100 to 202.
5. Exit Drawing C.

*Drawing C becomes Drawing C’’.*

1. In Project 1, delete Drawing C’.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

76/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. In Project 2, check out Drawing C from the Plant *without replacing the existing P&ID*.
2. In Project 3, fetch Drawing C’’ from Project 2.
3. Open Drawing C’’.
4. Add a Generic Tray to the vessel.
5. Exit Drawing C’’.

*Drawing C’’ becomes Drawing C’’’.*

1. In Project 2, undo the check-out of Drawing C’’.
2. In Project 3, check out Drawing C from the Plant, ensuring that the existing P&ID is not replaced.

*Drawing C becomes Drawing C’’’ in Project 3.*

1. Open Drawing C’’’.
2. Claim Flow Indicator FI-202.
3. Exit Drawing C’’’.

*Drawing C’’’ becomes Drawing C’’’’ in Project 3.*

1. Check in Drawing C’’’’.
2. In Project 1, select **Revisions** > **Fetch Deleted Drawing** and select deleted Drawing C’.
3. Check out Drawing C’’’’ from the Plant, ensuring that the existing P&ID is not replaced.

*Drawing C’’’’ becomes Drawing C’ in Project 1.*

1. Attempt to check in Drawing C’.

*Unclaimed changes prevent check-in.*

1. Open Drawing C’.
2. Claim the vessel.
3. Claim Flow Indicator FI-101.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

77/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Perform Compare and Refresh for the generic vessel tray.
2. Exit Drawing C’.
3. Check in Drawing C’.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

78/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

79/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an**

**arrow indicates changes to the drawing or**

**to drawing item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Undo drawing check-out**

**Delete drawing**

**Check in Multiple Representations**

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing D from the Plant.
2. Open Drawing D.
3. Claim the vessel and make a note of its Item Tag.
4. Claim the instrument, instrument OPC, and the signal run connected to it.
5. Make a note of the instrument OPC’s Item Tag and delete it to the Plant Stockpile.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

80/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Exit Drawing D.

*Drawing D becomes Drawing D’.*

1. In Project 1, create Drawing F.
2. Open Drawing F.
3. Place the instrument OPC that was placed in the Plant Stockpile after being deleted from Drawing D.
4. Place a Multiple Representation of the vessel.
5. Add an Equipment Name label to the vessel.
6. Exit Drawing F.

*Drawing F becomes Drawing F’.*

1. Attempt to check in Drawing F’.

*Related Drawings error prevents check in.*

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

81/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Check in Drawings D’ and F’ together.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

82/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an**

**arrow indicates changes to the drawing or**

**to drawing item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Fetch Older Drawing Versions and OPCs**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

83/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing G.
2. Open Drawing G.
3. Claim the vessel, Nozzle N1, and the pipe run connected to the nozzle.
4. Delete the vessel and Nozzle N1 from the model.
5. Exit Drawing G.

*Drawing G becomes Drawing G’.*

1. In Project 2, create Drawing H.
2. In Project 3, create Drawing I.
3. Check in Drawing I from Project 3 to As-Built and checkout Drawing I to Project 2 from As-Built.
4. Open Drawing H.
5. Place 3 Piping Off Drawing OPCs (OPC1, OPC2, and OPC3), sending the partner OPCs to the Drawing I stockpile.
6. Make a note of the OPC tags.
7. Exit Drawing H.

*Drawing H becomes Drawing H’.*

1. Open Drawing I.
2. Place OPC3 into Drawing I from the Drawing I stockpile.
3. Exit Drawing I.

*Drawing I becomes Drawing I’.*

1. In Project 2, check in Drawing I’, removing it from the project.
2. Check out Drawing I’ from As-Built in Project 3.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

84/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. In Project 3, open Drawing I’.
2. Claim OPC2 (in Drawing I stockpile).
3. Use the Delete to Stockpile command to remove OPC2 from Drawing I’.
4. Use the Move to Different Stockpile command to place OPC2 into Project 3 Plant stockpile.
5. Exit Drawing I’.

*Drawing I’ becomes Drawing I’’.*

1. In Project 1, check in Drawing G’.
2. In Project 3, fetch Version 1 of Drawing G’ from As-Built.

To fetch the correct version of Drawing G’, select **History** on the Fetch dialog and

Version 1 on the **Version History** dialog.

1. From Project 2, check in Drawing H’ and then check it out to Project 3.
2. Open Drawing H’.
3. Claim OPC1, OPC2, and OPC3.
4. Exit Drawing H’.

*Drawing H’ becomes Drawing H’’.*

1. Check in Drawing I’ and Drawing H’ from Project 3 into As-Built.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

85/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

86/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an**

**arrow indicates changes to the drawing or**

**to drawing item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Finishing a Project**

Finishing a project is a two-step procedure: First, you must complete the project, and then you must merge the project back into the Plant.

**Complete a Project**

1. In Drawing Manager, open the **Project Status** dialog.
2. Select the **Complete Project** button.

This command performs several tests, including verifying all the drawings for check in. If the project passes all the tests, the project status is set to **Completed**. If the project fails to pass one of the tests, the project remains in the **Active** state and you have more work to do before completing the project.

The **Verify for Check In** command in Drawing Manager allows you to perform the same tests on individual drawings that are done by the **Complete Project** process on all drawings. This https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

87/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

allows you to check if individual drawings are ready for check in as work on them is completed.

Before a project can be completed, all the drawings that exist in the project must be checked out (not just fetched). Checking out a drawing to a project means that this project is the only one that can check it back into the plant.

All drawings must be up-to-date with the version in the Plant. If another project has checked in changes to one of the project drawings because it was fetched from the Plant, then the project will fail to complete. In this case, you must refresh the affected drawings before the project can be completed. This ensures that overlapping projects with shared drawings do not destroy each other’s changes. If projects do not share any drawings, this is not an issue.

**Merge a Project**

1. After completing a project, the next step of finishing the project is to merge the project back into the Plant. Merging the project causes all the changes that were made in the project to be merged back into the Plant. Prior to merging, the Plant is not affected by any of the changes that are done in the project. After merging, all the project changes are incorporated into the Plant database.In Drawing Manager, open the **Project Status** dialog.
2. Select **Merge Project**.

*This command performs the check in operation on each of the checked-out drawings* *and sets the state of the project to **Merged**.*

In some workflows, it is desirable to merge some of the drawings back into the Plant before the project is completed. Individual drawings can be merged into the Plant with the **Check In** command in Drawing Manager.

Merged projects cannot be returned to active status.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

88/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Cancel a Project**

If you decide that a project should not be merged into the Plant, the other alternative is to cancel the project. Canceling a project causes all the project changes to be discarded.

Canceled projects cannot be returned to the **Active** status.

1. In Drawing Manager, open the **Project Status** dialog.
2. Select the **Cancel Project** button.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

89/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Smart Electrical Project Management**

Smart Electrical supports Owner operator and EPC activities with As-Built functionality. You define the main plant as the As-Built and you can then add any number of additional plant groups to create your projects. The Plant Administrator needs to activate the plant and scope it with the particular As-Built. When you work with projects, the database is partitioned into several schemas: a single schema for As-Built and separate schemas for projects. An operational plant exists and most of the activities are concerned with routine maintenance or plant modernization (revamps).

To facilitate plant modernization, the software enables you to create one or more projects using existing electrical data for the operating plant as a starting point for plant modernizations (revamps). Each project is defined for one plant only, and a plant can have several associated projects.

You can also use projects when working in an integrated environment.

After merging project data with As-Built, you cannot reverse the process. For this reason, at all stages of plant modernization, you should ensure that there is full coordination of engineering activities between As-Built and projects to avoid inadvertent loss of data. It is also recommended that you back-up your database before starting the projects.

You can work only in online mode that is, As-Built and projects must be connected to the same database.

When working in a plant that is registered with SmartPlant Foundation, the software automatically determines the project status in the database according to the SmartPlant project status.

To be able to view and edit data in As-Built, make sure that in the Options Manager, on the **General Settings** page, the **Allow Full Access to As-Built** is set to **Yes**.

**Smart Electrical Project and Item Statuses**

A **project** status shows the stage of the project life-cycle. Possible project statuses are: **Active**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

90/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The initial state of a project right after its creation.

**Completed**

Indicates that all the work on the project items has been completed and that the items are ready to be merged back into the As-Built. You cannot claim items in a project whose status has been set to **Completed** or **Merged**.

In a project, when searching for completed items in the **Project Management** window, it is possible to select the related items which have not been completed yet and to change their status to **Completed**.

**Merged**

Indicates that all the project items have been merged back into the As-Built.

**Canceled**

Indicates that the project has been canceled and it can be deleted. Selecting this project status changes the status of the items in the project from **Claimed** to **Scoped**.

The status of **an item** in a project determines what you can do with the item, for example, editing the properties in the project. Possible item statuses in the project are: **Scoped**

Indicates that the item becomes available for viewing in the project and that it can be claimed.

**Claimed**

Indicates scoped items that have been copied to the project and they are enabled for editing.

There are two modes of claiming:

**Exclusive** - Items can only be edited in the current project and cannot be claimed for another project.

**Shared** - Items can be claimed for another project and edited in that project.

**Completed**

Indicates that the work on the item has been completed and the item is ready to be merged back into the As-Built.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

91/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Merged**

Indicates that the item has been merged back into the As-Built.

The **Project Management** table displays the status of claimed items.

To view the status of a claimed item in a project while in the As-Built, right-click an item in the list view pane of the **Electrical Index** and then select **Item Status in Projects**. This command opens the **Item Status in Projects** dialog, which shows the item status, claim mode, and project name for each project in which the selected item is claimed.

**Rules for Changing Statuses**

The following rules apply to the relationship between the project status and item status in a project:

1. To be able to scope items, the project status must be **Active** or **Merged**.
2. To be able to merge items, the item status in the project must be **Completed**.
3. You cannot re-scope an item (refresh the scope) if the item has already been claimed. You have to change the status of the item to **Scoped** and then reclaim it.
4. To be able to merge a project, all the items of that project must have status **Completed**.
5. It is possible to set the status of a project to **Completed** in As-Built if all the status of all claimed items is **Completed**.
6. In a project, it is possible to change the status of a project to **Completed** disregarding the status of the items in project. This operation automatically sets the status of all the items in the project to **Completed**, except for registered reports and all documents (SLDs, schematics, miscellaneous drawings and electrical analysis SLDs). To include these items when merging the project, you must mark them manually as completed in a separate session.

The following table shows the various commands available for changing the status of the items in the project and how they affect these statuses.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

92/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Command**

**Initial Status**

**Final Status**

**Comments**

Scope

None, Scoped

Scoped

Performed in As-

Built. If the initial

status is **Scoped**,

refreshes the data by

re-scoping the item.

Set Claim Mode

Scoped

Claimed

Performed in a

(Exclusive, Shared,

project. Invoked after

or Release Claim)

selecting **Apply**.

Mark as Completed Claimed

Completed

Performed in a

project. Invoked after

selecting

**Apply**. Item stops

being editable and is

ready to be merged.

Clear Mark as

Completed

Claimed

Performed in a

Completed

project. Invoked after

selecting **Apply** and

receives same claim

mode as when first

claimed. Makes the

item editable.

Mark as Reclaimed Merged

Claimed

Performed in a

project. Invoked after

selecting **Apply** and

receives same claim

mode as when first

claimed. Makes the

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

93/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

item editable. This

command is option is

required when

working with

SmartPlant

Foundation.

Release Claim

Claimed

Released

Performed in a

project. Invoked after

selecting **Apply**. The

claim mode changes

to

**Released**. Enables

re-scoping of the

item in As-Built.

Merge

Completed

Merged

Performed in As-

Built. Overwrites the

previous As-Built

data.

In a project, when searching for completed items in the **Project Management** window, it is possible to select the related items which have not been completed yet and to change their status to **Completed**.

**Scoping the Project**

The Plant Administrator must specify those plant groups from which it will be possible to scope items. When the Plant Administrator specifies a plant group for scoping, the software includes in the scoping all higher-level plant groups in the same branch as the selected plant group, for example, if the plant groups are Plant-Area-Unit, and the Plant Administrator selects an area for scoping, the plant above that area is also included in the scope. For more information, see Set Project Scope in *Smart Engineering Manager Help*.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

94/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Project Status Dialog**

Displays the current project status with respect to the As-Built plant and allows you to update or modify those statuses. This dialog opens when you select on the **Project Management** toolbar. The available options in the Smart Electrical **Project Status** dialog depend on whether you open it from the As-Built or from the project.

You cannot claim items in a project whose status has been set to **Completed** or **Merged**.

**Smart Electrical project status**

Indicates whether the project is **Active**, **Completed**, **Merged**, or **Canceled**. If your project status is** Merged** or **Canceled**, then no further actions are available on this dialog.

**Reactivate** (only available from the As-Built) Returns the project status to **Active**. This command is available only when the initial project status is **Completed**, **Merged**, or **Canceled**.

**Complete Project** (only available from projects) Sets the project status to **Completed**. This command is available only when the initial project status is **Active**. When you select **Complete Project**, a confirmation message appears.

**Merge Project** (only available from the As-Built) https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

95/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Sets the project status to **Merged**. This command is available only when the initial project status is **Completed**. When you select **Merge Project**, a confirmation message appears.

**Cancel Project** (only available from the As-Built) Clears all claims on all objects and sets the project status to **Canceled**. This command is available only when the initial project status is **Active**, **Completed**, or **Merged.**  If the Plant is not registered with SmartPlant Foundation, then the project is simply canceled out of Smart Electrical.

**Claim All Completed Items** (only available from projects) Reverts the status of all completed items to **Claimed**. This command is available only when the initial project status is **Active**.See Change the Status of All Completed Items to Claimed.

**Modify Project Status in Smart Electrical**

1. Open the project for which you want to view the status.
2. On the **Project Management** window toolbar, select to open the **Project Status** dialog.
3. In the **Smart Electrical project status** area, determine the current status of your project with respect to the plant. A check mark denotes the current status. Possible statuses include **Active**, **Completed**, **Merged**, and **Canceled**.
4. Change the status of your project of your project as needed: To change an active project to completed, select **Complete Project**. This command is available only in the project when the initial project status is **Active**.

To change a completed project back to active, select **Reactivate**. This command is available only in the As-Built when the initial project status is **Completed**, **Merged**, or **Canceled**.

To merge a completed project into the plant, select **Merge Project**. This command is available only in the As-Built when the initial project status is **Completed**.

To cancel an active project, select **Cancel Project**. This command is available only in the As-Built when the initial project status is **Active**, **Completed**, or **Merged**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

96/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

When you change the project status to **Completed**, the software automatically sets the status of all the items in the project to **Completed**, except for registered reports and all documents (SLDs, schematics, miscellaneous drawings and electrical analysis SLDs). To include these items when merging the project, you must mark them manually as completed in a separate session.

**Project Management Common Tasks in the As-Built**

The following tasks are used frequently when working with As-Built in Smart Electrical.

**Select a Project**

This procedure shows you how to select a project for the current As-Built plant. Note that you have to select a project every time you reopen the **Project Management** table. See Select a

Project.

**Modify Project Status**

This procedure explains how to display the current project status, both with respect to SmartPlant and the plant and to update or modify those statuses. See Modify Project Status

in Smart Electrical.

**Add Items to the Project Management Table in As-Built** This procedure explains how to open the **Project Management** table and add the items that you require. Note that you have to add items that you want to work with every time you reopen the **Project Management** table. See Add Items to the Project Management Table in

As-Built.

**Scope Items**

After the Plant Administrator has scoped your project, you can start scoping the items that will be available for viewing in the project. See Scope Items.

**Use the Buffer to Scope Items**

The buffer in the **Project Management** table allows you to make a preliminary selection of items that you want to scope. See Use the Buffer to Scope Items.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

97/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Run a Test Merge**

You can run a test merge before merging the items into As-Built. This operation allows you to check whether there are any problems with the items that you want to merge into As-Built.

The software creates a log file that describes the problem that may occur during a test run.

See Run a Test Merge.

**Compare a Document in a Project with a Document in As-Built** After scoping and modifying items in a project, you can compare documents of the same type in As-Built and in the project, for example, registered reports, SLDs, schematics. If changes that you made to the item are reflected in the document, the software compares the changes and indicates them on a comparison report. Note that the software generates As-Built and project reports automatically when you run this command. This comparison can serve as a precautionary measure before merging project documents into As-Built. See Compare a

Document in a Project with a Document in As-Built.

**Merge Items into As-Built**

Merging is the final stage of a project cycle. After you have edited items in your project, you can merge those items into As-Built. The merge operation completely overwrites existing data in As-Built with data from the project. For this reason, after you have committed to merge

data, the changes are irreversible. See Merge All Project Items into As-Built (Full Merge) and

Merge Selected Project Items into As-Built (Partial Merge).

**Filter the Project Management Table Display**

This option allows you to filter the display of the items in the **Project Management** table

according to the status of items in the project. See Filter the Project Management Table

Display.

**Generate an Excel Report**

This option allows you to generate a report in Excel showing the current selection in the **Project Management** table, arranged according to the main items. In the report, you can

expand the main items to display their related items. See Generate an Excel Report.

**Select a Display Option**

This option allows you to specify the display mode in the data window. You can display the main items only, the main items expanded to show their related items, or a list showing all https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

98/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

items. If a particular related item is associated with more than one main item, that related item appears once only in the list view. In list view only, you can sort the items as desired by clicking the column headers in the data window. See Select a Display Option.

**Project Management Table (As-Built)**

The Project Management table in As-Built allows you to select a target project and to scope items for that project, and to merge items in the project back to As-Built after you have edited or created them in the project. The commands associated with the **Project Management** table are all on the Project Management Toolbar. This table opens when you select **Window** > **New** > **Project Management** on the main menu bar.

**Header**

**Description**

**(Check box)**

Applies to main items only. When selected, includes those items in the action specified the **Scope**, **Clear**, and **Merge** commands. The check box in the main header row is used to select or clear all the check

boxes in the column.

**Main Item Tag**

The tag of the main item. A main item can be a motor or some other load, converting equipment, a power

source, any free cable, a PDB, or a document.

**Related Item Tag**

The tag of the related item which has an electrical

association with the main item; for example, if the main item is a motor, related items can include cables,

signals, control stations, and circuits.

**Item Type**

Indicates the item type of the main item or related item.

**Status in project**

Indicates the status of the item. For details, see Smart

Electrical Project and Item Statuses.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

99/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Claim Mode**

Indicates whether the item, if claimed, has been

claimed exclusively or shared, or whether it has been released from the claim. In As-Built, this property is read-only.

**New Item**

Indicates whether an item has been newly-created in

the project. Note that after merging the item, this field appears blank.

**Item Path**

Indicates the parent hierarchy of a non- unique

item. For example, in the case of a circuit, the item path shows the PDB\Bus\(Cell) hierarchy.

**Description**

The item description, if appropriate, as it appears for the item properties.

**Plant Group**

Indicates the plant group to which the item belongs.

**Deleted**

Indicates whether the item has been deleted in the

project since the last time it was scoped.

**Result Status**

Indicates the result of a major operation such as

**Merge**. For example, the status **Done** appears after the software commits an operation successfully.

**Project Management Toolbar**

Contains the commands that you can run from the Project Management Table (As-Built).

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

100/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Icon**

**Command**

**Explanation**

**Select Project**

Allows you to select a project for

scoping and claiming As‑Built data. You

must select a project that already exists

and is assigned to the plant before you

can perform any other activities.

**Project Status**

Allows you to change the current status

of the project. Possible project statuses

are: **Active**, **Completed**, **Merged**, or **Canceled**. For details of the rules

governing changes in the project status,

seeRules for Changing Statuses.

**Add Items**

When you select one or more items

from the **Electrical Index** or the EDE,

adds those items to the **Project**

**Management** table where you can

select them for scoping to your project.

For items that you select in the

**Electrical Engineer**, adds the selected

item with any related items below it, and

also related items above it up to the

feeder PDB.

**Scope**

Makes each main item from the **Project**

**Management** table available for the

project if the check box beside it is

selected. If a selected main item has

related items, these are also included in

the scope. If you scope an item that is

not a main item, such as a control

station, the software automatically

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

101/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

selects the associated main item for

scoping. Where an item was previously

scoped, this command refreshes the

data.

**Test Merge**

Allows you to test the merging of items

that have status **Completed** and for

which you have selected the check

boxes. This operation can assist you in

troubleshooting problems before you

commit to merging the data.

**Merge**

Allows you to merge items that have

status **Completed** and for which you

have selected the check boxes.

**Find Completed Items**

Opens the **Find** dialog, which allows

you to find all the completed items in

the project. You can select all or some

of the completed items and then merge

them into As-Built.

**Show Merged Items**

Filters the display to show only those

items that have been merged back into

As-Built. Note that the filter relates to

the status of the items in the database

and not necessarily the status currently

displayed in the **Project Management**

table.

**Show Claimed Items**

Filters the display to show only those

items that have been claimed for the

project. Note that the filter relates to the

status of the items in the database and

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

102/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

not necessarily the status currently

displayed in the **Project Management**

table.

**Show Items Deleted from As-**

Filters the display to show only those

**Built**

items that have been deleted in As-

Built. Note that the filter relates to the

status of the items in the database and

not necessarily the status currently

displayed in the **Project Management**

table.

**Show Item Properties**

Displays the values of the item

properties for an item similar to the

**Properties** window view, but in read-

only mode. Select **Alphabetic** to

display the properties in alphabetical

order. Select **Categorized**

to display

the properties grouped by specific

categories. The software can display

the properties of only one item at a

time; the item for which the row is

highlighted.

**Clear All**

Clears all items from the **Project**

**Management** table.

**Clear**

Clears each main item from the **Project**

**Management** table if the check box

beside it is selected. If a selected main

item has related items, these are also

cleared.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

103/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Show / Hide Buffer**

Toggles the buffer display, which you

use to make a preliminary selection of

items that you may want to add to the

**Project Management** table. You drag

selected items to the buffer from the

**Electrical Index**, the **Electrical**

**Engineer**, or the EDE.

**Paste from Buffer**

Pastes to the **Project Management**

table items from the buffer whose check

boxes are selected.

**Excel Report**

Generates a report in Excel showing

the current selection in the **Project**

**Management** table, arranged according

to the main items. In the report, you can

expand the main items to display their

related items.

**Display**

Allows you to specify the display mode

in the data window. You can display the

main items only, the main items

expanded to show their related items,

or a list showing all items. If a particular

related item is associated with more

than one main item, that related item

appears once only in the list view. In list

view only, you can sort the items as

required by clicking the column headers

in the data window.

**Compare Documents**

After scoping and modifying items in a

project, you use this command to

compare documents of the same type

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

104/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

in As‑Built and in the project, for

example, registered reports, SLDs,

schematics. If changes that you made

to the item are reflected in the

document, the software compares the

changes and indicates them on a

comparison report. Note that the

software generates As-Built and project

reports automatically when you run this

command.

**Project Management Common Tasks in a Project**

The following tasks are used frequently when working with a project in Smart Electrical **Add Items to the Project Management Table in a Project** This procedure explains how to open the **Project Management** table and add the items that you require. Note that you have to add items that you want to work with every time you reopen the **Project Management** table. See Add Items to the Project Management Table in a

Project.

**Claim Items**

You claim items by opening the project to which they were scoped, and then you select individual items to claim. Note that you can claim main or related items separately. When claiming an item in a project, with the appropriate Options Manager setting, you can choose claim mode **Shared** or **Exclusive**. See Claim Items.

**Set Claim Mode**

This option allows you to set the required claim mode. The following claim modes are available:

**Exclusive** allows you to claim As-Built items in the current project only.

**Shared** allows users of different projects to claim the same As-Built items for their projects.

**Release Claim** allows you to cancel the claim of the selected items and then re-scope them in As-Built. Re-scoping the items will update the data in the project.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

105/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The Shared claim mode is available only after making an appropriate setting in the Options Manager. Also, if your plant is registered with SmartPlant, the Shared mode is not available, regardless of the setting you define in Options Manager. See Set Claim Mode.

**Release Claim**

Releasing the claim of an item enables you to cancel the claim of an item. This action makes it possible to re-scope the item in As-Built if you need to update the data in the project. After the item has been re-scoped, you can claim it again in the project and then edit the updated data. Note that when releasing the claim of an item, it status in the project remains Claimed.

However, the claim mode changes to Release Claim. Items whose claim mode is Release Claim behave exactly in the same way as the scoped items as the software re-scopes these items. See Release Claim in Smart Electrical.

**Mark Items as Completed**

Just before you are ready to return the items from your project to As-Built, you have to change the status of these items in the project to Completed. The items that have been marked as completed are no longer available for editing in the project and are ready for merging into As-Built. See Mark Items as Completed.

**Clear Mark as Completed**

This option allows to you to change the Completed status back to Claimed. These items will again become available for editing in the project. See Clear Mark as Completed.

**Release Items from Merge**

After merging items into the As-Built plant, users of other projects cannot claim these items.

This option makes it possible to release merged items so that they can be claimed for other projects. After applying this option, the merged items in your current project become marked as scoped. See Release Items from Merge.

**Filter the Project Management Table Display**

This option allows you to filter the display of the items in the **Project Management** table

according to the status of items in the project. See Filter the Project Management Table

Display.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

106/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Generate an Excel Report**

This option allows you to generate a report in Excel showing the current selection in the **Project Management** table, arranged according to the main items. In the report, you can

expand the main items to display their related items. See Generate an Excel Report.

**Select a Display Option**

This option allows you to specify the display mode in the data window. You can display the main items only, the main items expanded to show their related items, or a list showing all items. If a particular related item is associated with more than one main item, that related item appears once only in the list view. In list view only, you can sort the items as desired by clicking the column headers in the data window. See Select a Display Option

**Project Management Table (Project)**

The Project Management table, when opened in the project, displays all items that you last scoped from As-Built, along with any previously scoped items whether or not they have been claimed. Its main purpose is for claiming items and releasing claimed items. Note that you can claim related items independently of their main items. The commands associated with the **Project Management** table are all on the Project Management Toolbar. This table opens when you select **Window** > **New** > **Project Management** on the main menu bar.

**Header**

**Description**

**(Check box)**

Applies to main items only. When selected, includes

those items in the action specified the **Scope**, **Clear**, and **Merge** commands. The check box in the main header row is used to select or clear all the check

boxes in the column.

**Main Item Tag**

The tag of the main item. A main item can be a motor or some other load, a PDB, a cable.

**Related Item Tag**

The tag of the related item which has an electrical

association with the main item; for example, if the main https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

107/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

item is a motor, related items can include cables,

signals, control stations, and circuits.

**Item Type**

Indicates the item type of the main item or related item.

**Status in project**

Indicates the status of the item. For details, see Smart

Electrical Project and Item Statuses.

**Claim Mode**

Indicates whether the item, if claimed, has been

claimed exclusively or shared, or whether it has been released from the claim. In As-Built, this property is read-only.

**New Item**

Indicates whether an item has been newly-created in

the project. Note that after merging the item, this field appears blank.

**Item Path**

Indicates the parent hierarchy of a non- unique

item. For example, in the case of a circuit, the item path shows the PDB\Bus\(Cell) hierarchy.

**Description**

The item description, if appropriate, as it appears for the item properties.

**Plant Group**

Indicates the plant group to which the item belongs.

**Result Status**

Indicates the result of a major operation such as

**Merge**. For example, the status **Done** appears after the software commits an operation successfully.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

108/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Project Management Toolbar**

Contains the commands that you can run from the Project Management Table (Project).

**Icon**

**Command**

**Explanation**

**Project Management**

Opens the **Project Status** dialog, which

displays the status of the current project

status, both with respect to SmartPlant

Foundation.

**Add Items**

Allows you to add items that you added

or modified in the project for eventually

merging to As-Built.

**Apply**

Applies the command to change the

status of the items whose check boxes

are selected. The action performed

depends on the status of the item.

**Set Claim Mode**

Allows you to mark any item with status

**Scoped** or **Merged** for claiming, if the

check box beside the item is

selected. Note that after claiming an

item exclusively, it becomes unavailable

for claiming to other projects. After

selecting** Apply**, the status of each

marked item changes to **Claimed**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

109/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Mark as Reclaimed**

Marks an item with status **Merged** for

claiming again in the project, if the

check box beside the item is

selected. After selecting **Apply**, the

status of the item changes to** Claimed**.

**Mark as Completed**

Marks an item with status **Claimed** for

being ready to merge back to As-Built, if

the check box beside the item is

selected. You can then merge these

items in As-Built.

**Clear Mark as Completed**

Marks an item with status** Completed**

for returning to **Claimed** status, if the

check box beside the item is

selected. After selecting** Apply**, the

status of each marked item changes to

**Claimed**. The claim mode, **Exclusive**

or **Shared**, returns to what it was when

the item was originally claimed.

**Release Claim**

Marks an item with status **Claimed** for

releasing from the claim, if the check

box beside the item is selected. After

selecting **Apply**, the status of the item

changes to** Scoped** as the software re-

scopes these items.

**Release from Merge**

Marks an item with status **Merged** for

releasing from the merge, if the check

box beside the item is selected. After

selecting **Apply**, the status of the item

changes to** Scoped** and the software

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

110/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

makes it possible to claim these items

for other projects.

**Test Merge**

Allows you to test the merging of items

that have status **Completed** and for

which you have selected the check

boxes. This operation can assist you in

troubleshooting problems before you

commit to merging the data.

**Publish After Merge**

Publishes all documents that have

already been published in the scope of

the project and afterwards merged into

As-Built. (For use with an integrated

environment.)

**Find Completed Items**

Opens the **Find** dialog, which allows

you to find all the completed items in

the project. You can select all or some

of the completed items and then merge

them into As-Built.

**Show Merged Items**

Filters the display to show only those

items that have been merged back into

As-Built. Note that the filter relates to

the status of the items in the database

and not necessarily the status currently

displayed in the **Project Management**

table.

**Show Claimed Items**

Filters the display to show only those

items that have been claimed for the

project. Note that the filter relates to the

status of the items in the database and

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

111/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

not necessarily the status currently

displayed in the **Project Management**

table.

**Show Items Deleted from**

Filters the display to show only those

**Project**

items that have been deleted from the

project. Note that the filter relates to the

status of the items in the database and

not necessarily the status currently

displayed in the **Project Management**

table.

**Show Item Properties**

Displays the values of the item

properties for an item similar to the

**Properties** window view, but in read-

only mode. Select **Alphabetic** to

display the properties in alphabetical

order. Select **Categorized**

to display

the properties grouped by specific

categories. The software can display

the properties of only one item at a

time; the item for which the row is

highlighted.

**Select Related Items**

Allows you to select all related items for

which the main item is already selected

for the next action that you want to

perform. A sub-menu option also allows

you to clear the selection of all related

items.

**Clear All**

Clears all items from the **Project**

**Management** table.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

112/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Clear**

Clears each item from the **Project**

**Management** table if the check box

beside it is selected.

**Excel Report**

Generates a report in Excel showing

the current selection in the **Project**

**Management** table, reflecting the

selected display mode. In the report,

you can expand the main items to

display their related items.

**Display**

Allows you to specify the display mode

in the data window. You can display the

main items only, the main items

expanded to show their related items,

or a list showing all items. If a particular

related item is associated with more

than one main item, that related item

appears once only in the list view. In list

view only, you can sort the items as

required by selecting the column

headers in the data window.

**Managing Revisions in an As-Built and Project**

**Environment**

In an As-Built environment the revision uniqueness must be maintained between the Projects and the As-Built across the whole Plant. You can maintain uniqueness in either of the following ways:

Using a SmartPlant Foundation revision scheme, where the software tracks incremental changes.

Using a tool revision scheme.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

113/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

SmartPlant Foundation also uses the reserved revision method. The software generates a number following the highest existing minor revision when there is a gap in the minor revision sequence.

**Example:**

Drawing_Proj was claimed to Project 1. It was modified in the project and saved in Project 1

with revision C01. Drawing_Proj was claimed to Project 2, was modified in the project and saved later in Project 2 with revision C02.

- SmartPlant Foundation maintains the next revision number to the item (in this case: document) that gets published *first*, and a subsequent number to the item that gets published second. In the table below, the Drawing_Proj from Project 1 was published first, and Drawing_Proj from Project 2 was published second.

Plant Entity

Document name Start of available Changes to

Published Major

major and minor major and minor and minor

revision

revision when in

revision numbers

Projects

generated by

SPF*

As-Built

Drawing

C00

Project 1

Drawing_Proj

C00

C01

C03

Project 2

Drawing_Proj

C00

C02

C04

**Scoping Items**

After the Plant Administrator has scoped the project, you can start specifying which items will be available for viewing in the project. This selection is called scoping items.

You scope items by selecting the required items in As-Built. The selection can be one of the following:

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

114/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The entire plant hierarchy that was assigned in Smart Engineering Manager, according to the scoping definitions that the Plant Administrator has made.

Individual items in the **Electrical Engineer**.

Individual items in the **Electrical Index**.

Multiple items in the EDE.

You can select loads, converting equipment, power sources, free cables, PDBs, and so forth. Note that the software automatically scopes all the items that are associated with the scoped items. These items are called related items. Related items are those items that have an electrical or functional relationship to a main item. Related items may include control stations, associated cables, circuits, and signals.

In addition to the items that are included in the scoped plant groups, you can also scope items that belong to unscoped plant groups. However, you will not be able to claim these items or edit them in the project.

When scoping, the software follows certain rules that govern which items become available for viewing in the project. For details, see Rules for Scoping Items.

**Select a Project**

1. In an As-Built plant, select **Window** > **New** > **Project Management**.
2. In the **Project Management** table, right-click in the **Project Management** table and then select **Select Project,** or select .

After closing the **Project Management** table, the software removes all the items from the **Project Management** table. Also, you have to select a project every time you reopen the **Project Management** table.

**Select Project Dialog**

Allows you to select a project for scoping items.

**Project**

Allows you to select a project for scoping items.

**Description**

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

115/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Displays the project description.

**Status**

Displays the project status: **Active**, **Completed**, **Merged**, or **Canceled**.

**View related items in scope**

Allows you to view the items related to the items you select for scoping. Note that selecting this option slows down the performance. The software scopes related items automatically even if they are not viewed.

**Rules for Scoping Items**

The general rule for scoping is that when selecting items, the software automatically scopes all the related items and all the items that extend up to and including the item power source.

For example, selecting a motor that is connected to a feeder circuit, the software will scope the motor control stations, the motor feeder cable, the feeder circuit, the bus, and the PDB.

You can automate the process of scoping plant items by scoping a composite drawing. After a composite drawing is scoped, all the plant items that are associated with graphical elements on the drawing are scoped automatically. Furthermore, the parent items of those plant items are also scoped automatically even if the parent items are not on the scoped composite drawing.

The extent of the related items that are scoped along with the main selected item are indicated in the following table.

**Main Item**

**Related Item**

**Notes**

Loads, converting equipment,

Cables of any category (From / To

When

power sources (generators,

sides)

scoping loads

battery banks, offsite power)

and

Control stations and their cables

equipment

Instruments and their cables

connected to

a bus, the

I/O signals

scope

includes all

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

116/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Associated Circuits, their internals

the items in

and their PDB-Bus-Cell

the **Electrical**

associations

**Engineer**

branch up to

Metering equipment

and including

the circuit

and circuit

internals,

excluding the

PDB and bus

and any other

irrelevant

circuits of that

PDB.

Any cables

connected to

the circuit

rather than

directly to the

scoped load

will not be

scoped with

the circuit.

Instead,

those cables

will be

scoped with

related

equipment

like control

stations.

Power distribution boards

None

All buses,

circuits and

internals, up

to the

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

117/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

boundary of

the PDB have

to be scoped

separately as

they are not

included in

the scope

automatically

when scoping

a PDB.

No

associated

items

external to

the PDB

items, such

as cables or

signals

associated

with the PDB

or circuits will

be scoped.

Drums

Does not include

cables assigned to

the drum that have

not been scoped.

Cableways

All cableway segments

Entire cable that is routed through

one or more segments of the

cableway

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

118/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Instruments

Cables of any category (From / To

sides)

I/O signals

Associated Circuits, their internals

and their PDB-Bus-Cell

associations

Metering equipment

Local panels, junction boxes,

Cables of any category (From / To

cabinets

sides)

I/O signals

Associated Circuits and their

internals

Metering equipment

To scope space heaters and auxiliary contacts, see Guidelines for Scoping Space

Heaters and Auxiliary Contacts.

When scoping an item that is connected in parallel with another equipment item, the software automatically scopes all the items that are connected in parallel to the scoped item. For example, if you select Motor-1 that has been connected in parallel with Motor-2 and Motor-3, the software will also automatically scope Motor-2 and Motor-3 together with their upstream items all the way to their power sources.

You can scope the same item for more than one project.

**Guidelines for Scoping Space Heaters and Auxiliary Contacts** When creating projects and scoping disconnect electrical equipment items that have auxiliary contacts, follow the guidelines specified below:

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

119/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**As-Built Items**

**Project Requirement**

**Scoping and Merging**

A motor connected to

Design the space heater and its Scope the motor branch and the a standard feeder

complete power source and add PDB with its circuit so that it can circuit

the required disconnect

be claimed in the project.

equipment

Add a space heater, auxiliary

When merging, select both the

contacts, the power supply

motor, its new circuits, and the

circuits, and the interconnecting space heater circuitry cables.

A motor with a space

Delete all or part of the space

Select the motor as a scoped item

heater connected to

heater circuitry.

all its related space heater

the auxiliary contact of

circuitry (space heater, its feeder

the motor circuitry and

cable, the auxiliary contacts, the

the feeder to the

cable that feeds the auxiliary

auxiliary contacts

contacts. Note that the bus and

circuitry

the PDB that feeds the auxiliary

circuitry will be scoped as view

only.

**Add Items to the Project Management Table in As-Built** 1. In an As-Built plant, select **Window** > **New** > **Project Management**.

1. Select the required project. For details, see Select a Project.
2. Drag the required items one-by-one to the **Project Management** table. You can drag items from any of the following:

**Electrical Index**

**Electrical Engineer**

EDE

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

120/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

a schematic

a single line diagram

You have to add items every time you reopen the **Project Management** table.

You cannot add items to a project that has been set to **Completed**.

**Scope Items**

1. In Smart Electrical, select **File** > **Open** > **Plant Group** to open an As-Built plant.
2. On the **Open Plant Group** dialog, select **Select Plant**.
3. On the **Open Plant Group** dialog, select the appropriate plant hierarchy level and select **OK**.
4. Select **Window** > **New** > **Project Management**.
5. In the **Project Management** table in As-Built, select .
6. On the **Select Project** dialog, select the project you require and select **OK**.
7. With the **Project Management** table in As-Built open, select the main items for scoping 8. Select **Add** command or select on the **Project Management** toolbar. For single item,drag the selected item to the **Project Management** table.

You can use the buffer to make a preliminary selection of items that you may want to add to the **Project Management** tables. For details, see Use the Buffer to Scope

Items.

1. Select the check box beside each main item that you want to scope.
2. Select to scope the items.

The software also scopes related items automatically.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

121/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

You can automate the process of scoping plant items by scoping a composite drawing.

After a composite drawing is scoped, all the plant items that are associated with graphical elements on the drawing are scoped automatically. Furthermore, the parent items of those plant items are also scoped automatically even if the parent items are not on the scoped composite drawing.

When scoping an item that is connected in parallel with another equipment item, the software automatically scopes all the items that are connected in parallel to the scoped item. For example, if you select Motor-1 that has been connected in parallel with Motor-2 and Motor-3, the software will also automatically scope Motor-2 and Motor-3 together with their upstream items all the way to their power sources.

Certain related items that are scoped, such as circuit internals, do not appear in the **Project Management** table.

**Use the Buffer to Scope Items**

The buffer in the **Project Management** table allows you to make a preliminary selection of items that you want to scope.

1. With the **Project Management** table in an As-Built plant open, right-click in the **Project** **Management** table and then select **Show/Hide Buffer**, or select .
2. Drag the required items one-by-one to the **buffer** in the **Project Management** table. You can drag items from any of the following: **Electrical Index**

**Electrical Engineer**

EDE

a schematic

a single line diagram

1. In the **Buffer**, select the check boxes next to the items that you want to scope.
2. Select on the **Project Management** toolbar or right-click in the **Project Management** table and then select **Paste from Buffer**.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

122/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Filter the Project Management Table Display**

1. In an As-Built plant or project, select **Window** > **New** > **Project Management**.
2. If your work environment is an As-Built plant, select the required project. For more

information, see Select a Project.

1. Select the required icon on the **Project Management** toolbar, or right-click in the **Project Management** table and then select one of the following commands: Icon

Command

Explanation

**Find Completed Items**

Opens the **Find** dialog to

allow searching for items

that have been completed

in the project.

**Show Merged Items**

Filters the display to show

only those items that have

been merged back into the

As‑Built.

**Show Claimed Items**

Filters the display to show

only those items that have

been claimed for the

project.

**Show Items Deleted from** Filters the display to show **As‑Built**

only those items that have

been deleted in the As‑Built.

**Show Item Properties**

Displays the values of the

item properties for an item

similar to the **Properties**

window view, but in read-

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

123/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

only mode. The software

can display the properties of

only one item at a time; the

item for which the row is

highlighted.

**Generate an Excel Report**

1. In an As-Built plant or project, select **Window** > **New** > **Project Management**.
2. If your work environment is an As-Built plant, select the required project. For more

information, see Select a Project.

1. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and then select **Excel Report**.

**Select a Display Option**

1. In an As-Built plant or project, select **Window** > **New** > **Project Management**.
2. If your work environment is an As-Built plant, select the required project. For more

information, see Select a Project.

1. Select on the **Project Management** toolbar and then select the required option, or right-click in the **Project Management** table, select **Display**, and then select a command: **Main Items Only**, **Main Items with Related Items**, or **All Items as List**.

**Claiming Items**

Claiming items is the first action that you do when starting to work in a project. The items that have been scoped to your current project become available only after you claim them.

Claimed items in a project become editable and you can modify them or delete them as needed. Unclaimed items are not available in your project even if they have been scoped for this project in the As-Built. The new items that you create in the project need not be claimed.

You claim items by opening the project to which they were scoped, and then you select individual items to claim.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

124/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

You can claim main or related items separately. When claiming an item in a project, with the appropriate Options Manager setting, you can choose claim mode **Shared** or** Exclusive**.

**Add Items to the Project Management Table in a Project** 1. Open the required project.

1. Select **Window** > **New** > **Project Management**.
2. Do one of the following:

Drag a single item to the **Project Management** table from the **Electrical Index**, **Electrical Engineer**, or the EDE to the **Project Management** table.

Select a single item in a schematic or SLD and select .

Select multiple items the **Electrical Index**, or the EDE and select .

After closing the **Project Management** table, the software clears all the items from the table.

You should add items every time you reopen the **Project Management** table.

**Claim Items**

1. In a project, select **Window** > **New** > **Project Management**.
2. Add the items that you require. For details, see Add Items to the Project Management

Table in a Project.

1. Select the check box beside each item that you want to claim. For details of item statuses in the project that determine which items you can mark for claiming, see Rules

for Changing Statuses.

1. For each item that you want to claim, select **Shared** or **Exclusive** as the claim mode. Note that if, in the Options Manager, **General Settings**, the **As-Built Claim** **Mode** option is set to **Exclusive**, the **Shared** claim mode is not available 5. Select the **Apply** command to claim the items.

The items are now available for editing in the project. When you have finished editing items, you can change their status to **Completed**. Items with status **Completed** are https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

125/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

ready for merging into As-Built.

Check the data under **Result Status** to make sure that there are no problems.

You cannot claim items in a project whose status has been set to **Completed** or **Merged**.

**Set Claim Mode**

This option allows you to set the required claim mode. The following claim modes are available:

**Exclusive** — Allows you to claim As-Built items in the current project only.

**Shared** — Allows users of different projects to claim the same As-Built items for their projects.

**Release Claim** — Allows you to cancel the claim of the selected items and then re-scope them in As-Built. Re-scoping the items will update the data in the project.

1. In a project, select **Window** > **New** > **Project Management**.
2. Add the items that you require. For details, see Add Items to the Project Management

Table in a Project.

1. Select the check box beside each required item. For details of item statuses in the

project, see Rules for Changing Statuses.

1. Select on the **Project Management** toolbar and then select **Exclusive**, **Shared**, or **Release Claim;** or right-click in the **Project Management** table and then on the shortcut menu, point to **Set Claim Mode** and then select **Exclusive**, **Shared**, or **Release Claim**.
2. Select the **Apply** command to claim the items.

The **Shared** claim mode is available only after making an appropriate setting in Options Manager. Also, if your plant is registered with SmartPlant Foundation, the **Shared** mode is not available, regardless of the setting you define in Options Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

126/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Release Claim in Smart Electrical**

1. In the **Project Management** table (for a project), select the check box beside each main items for which you want to release the claim.
2. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and select **Release Claim** on the shortcut menu.
3. Select to release the claim for the selected items.

To claim the items whose claim mode is **Release Claim**, right-click in the **Project** **Management** table and then select **Mark as Reclaimed**.

After setting the claim mode to **Release Claim**, the status of the items still remains exactly the same as the scoped items, as the software re-scopes them.

**Mark Items as Completed**

1. Open the required project.
2. Add the items that you require. For details, see Add Items to the Project Management

Table in a Project.

1. Select the check box beside each item that you want to mark as completed. For details

of item statuses in the project, see Rules for Changing Statuses.

1. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and then on the shortcut menu, select **Mark as Completed**.
2. Select the **Apply** command to claim the items.

The items marked as completed will not editable in the project and will be ready for merging into the As-Built.

**Clear Mark as Completed**

1. Open the required project.
2. Add the items that you require. For details, see Add Items to the Project Management

Table in a Project.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

127/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. Select the check box beside each required item. For details of item statuses in the

project, see Rules for Changing Statuses.

1. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and then on the shortcut menu, select **Clear Mark as Completed**.
2. Select the **Apply** command to claim the items.

The items whose status is **Clear Mark as Completed** become available for editing in the project.

**Change the Status of All Completed Items to Claimed** This feature allows you to revert the **Completed** status of all the project items to **Claimed**.

This is especially helpful when you want to use an existing plant as a source for similar plants by using the **Load plant as project** feature in Smart Engineering Manager. You can load this plant as a project into different plants, edit this project, and then merge it into your As-Built plant.

1. Open the project for which you want to change the item statuses.
2. On the **Project Management** toolbar, select to open the **Project Status** dialog.
3. Select the **Claim All Completed Items** button.
4. When prompted to confirm the action, select **Yes**.
5. On the **Project Status** dialog, select **Close**.

This command is available only for active projects. If your project is not active, prior to changing the item statuses, you need to select **Reactivate** in the **Project Status** dialog.

**Complete a Project**

Prior to merging all the project items into As-Built, you have to change the status of all the project items to **Completed**. Setting the project status to **Completed** automatically changes the status of all the project items to **Completed** and allows you to run a full merge of the current project into As-Built. For details about running a full merge, see Merge All Project

Items into As-Built (Full Merge).

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

128/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. In a project, select **Window** > **New** > **Project Management**.
2. On the **Project Management** toolbar, select .
3. On the **Project Status** dialog, select **Complete Project**.
4. Select **Close**.

A project can only be returned to an **Active** state from the **Completed** or **Merged** state. If a project has been set to **Canceled**, it cannot be changed back to **Active**.

**Canceled** is permanent state.

**Return a Project to the Active Status**

This procedure explains how to reactivate a project which has been merged or set as **Completed**.

1. In a project, select **Window** > **New** > **Project Management**.
2. On the **Project Management** toolbar, select .
3. On the **Project Status** dialog, select **Reactivate**.
4. Select **Close**.

**Release Items from Merge**

1. In a project, select **Window** > **New** > **Project Management**.
2. Right-click in the **Project Management** table and then select **Show Merged Items** .
3. Select the check box beside each item you want to release.
4. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and then select **Release from Merge**.
5. Select on the **Project Management** toolbar, or right-click in the **Project** **Management** table and then select **Apply**.

After releasing from merge, the status of the items in the project becomes **Scoped**, that is, the items will be scoped after you select **Apply** again.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

129/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

**Merging Items into As-Built**

Merging is the final stage of the project cycle. After you have edited items in your project, you can merge those items into As-Built. The merge operation completely overwrites existing data in As-Built with the data from the project. For this reason, after you have merged data, the changes are irreversible.

You can merge all the project items into As-Built or only some of the completed items that you select.

**Add Item**

If you add a new item in the project, after merging the item, the software creates it in As-Built.

**Modify Item**

If you modify data for an item in the project, after merging, the software overwrites the existing data for that item in As-Built.

**Delete Item**

If you delete an item in the project, after merging the item, the software deletes it in As-Built.

When merging an item that is connected in parallel with another equipment item, the software automatically merges all the items that are connected in parallel to the scoped item. For example, if you select Motor-1 that has been connected in parallel with Motor-2 and Motor-3, the software will also automatically merge Motor-2 and Motor-3 and their upstream items all the way to their power sources.

When merging a composite drawing, all the plant items that are associated with graphical elements on the drawing will be merged automatically on condition that they and their parent items have been completed or merged. If the status of at least one of the items or one of the parent items is not completed or merged, the software will not allow you to merge the composite drawing.

You can claim an item in a project and subsequently modify its data in As-Built. If you then want to transfer the item changes from As-Built to the project, you must update the item manually in the project. To assist you in doing this, it is recommended that you run a comparison report first. You can also run the **Release Claim** command in the project https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

130/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

to automatically re-scope the item with the updated data from As-Built, but in this case any changes you have made to the item in the project will be lost.

You can only edit data in As-Built if in Options Manager, **General Settings**, the **Allow** **Editing in As-Built** property is set to **Yes**.

For the rules that govern document revisions, see Rules Governing Revisions for

Documents Merged Back into As-Built.

**Compare a Document in a Project with a Document in As-Built** 1. In an As-Built plant, select **Window** > **New** > **Project Management**.

1. Select the required project. For details, see Select a Project.
2. From the **Electrical Index**, add the required documents to the **Project Management**

table. For details, see Add Items to the Project Management Table in As-Built.

1. In the **Electrical Index**, select a registered report, a schematic or an SLD that you want to compare.
2. In the **Project Management** table, select the check box next to the document that you want to compare.
3. Right-click in the **Project Management** table and then select **Compare Documents**.

For the rules that govern document revisions when merging documents into As-Built,

see Rules Governing Revisions for Documents Merged Back into As-Built.

In the drawing, the software displays clouds around the items that differ from the current data. The number of the revision selected for comparison is shown in a triangle beside https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

131/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

the cloud, for example:

For all document types, the software generates a tabular report in Excel showing the following information:

Report document type

Current drawing name

Compared revision

List of changed items displaying tag (where relevant), item type, property, current and previous property values, and change type (New, Updated, or Deleted) For SLDs, the report also indicates:

Current and previous revision numbers.

Attachment to a different document template.

Added or removed items, with an index number (Reference ID) for each item and the change type.

Changes in associations between items, with an index number (Reference ID) for each item, current and previous relation descriptions, and the change type.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

132/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

For schematic drawings, disconnected items are shown in the report as being deleted from the drawing and new connections appear as new items in the drawing. The following example of an Excel report is for a motor that was disconnected from a bus > circuit > cable hierarchy, and reconnected to a cabinet via a cable: For wiring diagrams, the report also indicates added or removed items with an index number (Reference ID) beside each deleted item and the change type for all items.

For cable block diagrams, the report also indicates: Current and previous revision numbers.

Added or removed items, with the change type.

Changes in associations between items, with an index number (Reference ID) for each item, current and previous relation descriptions, and the change type.

For registered reports, the software opens two Excel files. One of the Excel files displays changed data with a blue shading. The second file is a summary of all changes and it is called **Registered Comparison Report**. This report displays the previous and current data for each tag that has undergone a change. Note that you can compare a registered report only if this is a simple tabular report.

**Rules Governing Revisions for Documents Merged Back into As-https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456**
**
133/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Built

When merging a document from a project back into As-Built, the software manages the document revisions according to the following rules: The revision numbering of a document in a project is done manually. When merging a document into As-Built, and the revision number of the document in the project is lower than the one in As-Built, the software raises the revision number automatically.

If the revision number of the document in the project is higher than the one in As-Built, after merging the document back into As-Built, the software treats the revision number that was set in the project as the latest revision.

If a document has different revision methods in As-Built and a project, after merging such a document back into As-Built, the software inserts the revision as it was used in the project and treats this revision as the latest one. All consequent revisions of this document will use the new method as it was set in the project.

If the revision number of the document that you want to merge into As-Built is identical to the one in the project, the software can do one of the following according to the preference that you have set on the General Settings page in Options Manager.

Reject the document

The software will not merge the current document into As-Built and will add an appropriate note in the log file.

Increment the revision number

The software will raise the revision number in As-Built.

Use the existing number and overwrite the revision The software will retain the revision number in As-Built but will overwrite the revision information.

Run a Test Merge

1. In the Project Management table (for As-Built), select the required project.
2. On the Project Management table toolbar, select , or right-click in the Project Management table and then select Find Completed Items to see which items have https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

134/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

been completed in the project.

1. Right-click in the Project Management table and then select Test Merge.

The software generates a log file that shows any possible problems that might occur during the test merge. For details, see Generate Error Log Files in *Smart Electrical Help*.

Merge All Project Items into As-Built (Full Merge) The following procedure explains how to merge all the project items into As-Built.

Merging is the final stage of a project cycle. After you have edited items in your project, you can merge those items into As-Built. The merge operation completely overwrites existing data in As-Built with data from the project. For this reason, after you have committed to merge data, the changes are irreversible.

The software merges all the completed items into As-Built, including the child items. To run a full merge, the status of all the child items in the project must be Completed and the status of the project must be set to Completed. If the status of some of the child items is not set to Completed, full merge is not possible. See Complete a Project.

status of all the child items in the project must be Completed.

1. In an As-Built plant, select Window > New > Project Management.
2. Select the required project whose status has been set to Completed. See Select a

Project.

1. On the Project Management toolbar, select .
2. On the Project Status dialog, select Merge Project.
3. Select Close.

When merging a composite drawing, all the plant items that are associated with graphical elements on the drawing will be merged automatically on condition that they and their parent items have been completed or merged. If the status of at least one of the items or one of the parent items is not completed or merged, the software will not allow you to merge the composite drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

135/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

After a project has been merged, the software sets the status of the project and the status of all the items in the project to Merged. No further activities are possible in this project as all the items in the project are locked and cannot be edited. If you want to edit some of the items in a merged project, you must first reactivate the project. After reactivating a project, all the items in that project become scoped and you will have to claim the items that you want to edit.

Merge Selected Project Items into As-Built (Partial Merge) The software allows you to run a partial merge of the project items that have already been completed. You can instruct the software to find all the completed items in a project and add them to the Project Management table. You can then examine these items and select the ones that you want to merge into As-Built.

The merge operation completely overwrites existing data in As-Built with data from the project. For this reason, after you have committed to merge data, the changes are irreversible.

1. In an As-Built plant, select Window > New > Project Management.
2. Select the required project. For details, see Select a Project.
3. Right-click in the Project Management table and then select Find Completed Items or select on the Project Management toolbar.
4. On the Find dialog, select Find Now.
5. Under Results, select the items that you require and select OK.
6. In the Project Management table, select the check box next to a completed item that you want to merge into As-Built.
7. Right-click in the Project Management table and then select Merge or select on the Project Management toolbar.

You cannot merge items that have child items which are completed into As-Built. Also the main item, whose child items status is not set to Completed, cannot be merged.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

136/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

When merging a composite drawing, all the plant items that are associated with graphical elements on the drawing will be merged automatically on condition that they and their parent items have been completed or merged. If the status of at least one of the items or one of the parent items is not completed or merged, the software will not allow you to merge the composite drawing.

When merging an item that is connected in parallel with another equipment item, the software automatically merges all the items that are connected in parallel to the scoped item. For example, if you select Motor-1 that has been connected in parallel with Motor-2 and Motor-3, the software will also automatically merge Motor-2 and Motor-3 and their upstream items all the way to their power sources.

Plant Operating Cases in As-Built and Projects

When scoping As-Built items for a project, all the operating case data is copied together with the scoped items.

When creating a project, all the plant operating cases that exist in As-Built are created automatically in the new project.

Note the following information regarding plant operating cases when working with As-Built and projects.

Action

As-Built

Projects

Plant operating case

You can add, delete, and

You can add and rename cases

management

rename plant operating cases

as needed. You can delete only

as needed (performed in

those cases that exist in the

Options Manager).

selected project only and they

do not exist in As-Built.

If there are plant operating

case inconsistencies between

As-Built and an associated

project, you have to make sure

If the governing or active

that the names of the operating

case in a project is defined

cases in the projects are the

differently from As-Built,

same as in As-Built.

when merging data into

As-Built, the software

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

137/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

applies the governing or

active case functionality to

the operating case that is

defined as governing or

active in As-Built and not

to the case defined as

governing or active in the

project.

When scoping items for a

project whose governing

or active case is different

from As-Built, the software

applies the governing and

active case functionality to

the operating case that is

defined as governing and

active in As-Built and not

to the case in the project.

Adding or renaming cases

can cause inconsistencies

between the current

project and As-Built. You

will have to make sure that

the names of the operating

cases in the project are

the same as in As-Built.

Typically, you would add or

rename an operating case

to fix any existing

inconsistency that can be

caused by adding or

renaming an operating

case in As-Built.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

138/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Scoping

All plant operating case data of

the scoped items is

automatically copied to the

appropriate plant operating

case of the project after the

scoping is completed.

If the governing case defined in

a project is different from the

governing case in As-Built, the

governing case in the project

remains unchanged when

scoping items for that project.

Merging

All plant operating case data of

the merged items is

automatically copied to the

appropriate As-Built operating

case after the merging is

completed.

If the governing case defined in

a project is different from the

governing case in As-Built, the

governing case in the project

remains unchanged when

merging items for that project.

The software copies the item data to the appropriate operating case according to the ID

of the relevant operating case. So, even if an operating case has been renamed at one stage or another, the software will still copy the item data to the appropriate operating case.

If you attempt to merge data in an operating case that was created in the project and this case, does not exist in As-Built, the software stops the merge process and prompts https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

139/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

you to create an operating case in As-Built that has exactly the same name as in the project.

See Managing Plant Operating Cases and Synchronize Plant Operating Cases.

Synchronize Plant Operating Cases

The software checks for plant operating case inconsistencies when selecting a project in the As-Built or opening a project in Project Management.

If the software detects a case inconsistency between the As-Built and the selected project, you have to synchronize the plant operating cases that have been found as inconsistent. The names of these cases are shown by the software in the warning message that opens automatically after an inconsistency is detected. Inconsistencies can occur when adding, deleting, or renaming plant operating cases in the As-Built or one of the existing projects belonging to the As-Built. For example, if you add a plant operating case in a project, you will have to add the same case in the As-Built in order to merge the case data into the As-Built.

Synchronize Plant Operating Cases

1. In Options Manager, select Tools > Manage Plant Operating Cases.
2. On the Manage Plant Operating Cases dialog, add, delete, or rename the plant operating cases that have been detected as inconsistent.
3. In Smart Electrical, open Project Management and select the project that had inconsistent cases.
4. If no warning message appears, all the cases have been synchronized.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

140/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

About Security and Encryption

What techniques are used for Encryption?

Hexagon employs several encryption techniques to ensure that data is not exposed to unauthorized access. The following image details the standard encryption mechanisms: Enabling encryption on a system or device has negligible impact on performance of the system.

Database encryption

Transparent Data Encryption (TDE) is implemented on the standard database. TDE is where the database files on the server and any backups are encrypted. This ensures that external users cannot access or open files, backups, or hardware that could lead to the extraction of critical intellectual property data from the database without access to a decryption method.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

141/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

TDE provides an additional layer of security by securing how the Database Encryption Key (DEK) can be accessed. The DEK is stored in the database boot record and can be accessed in two ways:

Symmetrically by using a Certificate stored in the master database of the server.

Asymmetrically by using Extensible Key Management (EKM).

Communication encryption between application client and server

Hexagon products use the Hypertext Transfer Protocol Secure (HTTPS) and Transport Layer Security (TLS) 1.2 to support encrypted communication between the application client and the server. In addition, encryption is enforced on the server so unencrypted connections cannot be made by any client application.

Disk encryption

For hard disks and data on the computer drives, Hexagon employs Azure Disk Encryption (ADE) which encompasses multiple technologies to encrypt data at rest. All Hexagon software that is run in a Windows environment uses BitLocker to ensure that drives cannot be read without the proper decryption keys. These keys are held in the Azure Key Vault and provide access only to trusted users.

File share encryption

Files are protected as they are moved from the server to the client application using Server Message Block (SMB) Encryption, which is enabled on the server. SMB Encryption is the protocol supported by Windows as a way for two computers to transfer files and helps avoid unauthorized access to the data between them.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

142/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

For the latest support information for this product, connect to Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our

documentation web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To join in conversations about Smart P&ID, go to Technical User Forums

[https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf](https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf) and join the

Engineering & Schematics TUF group.

Hexagon Policy Against Software Piracy

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, or its affiliates, parents, subsidiaries retains ownership of the product. You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

143/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Copyright Notice

Copyright

Copyright © 1999-2025 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB and/or its subsidiaries and affiliates.

U.S. Government Restricted Rights Legend

Use, duplication, or disclosure by the government is subject to restrictions as set forth below.

For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014

and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division 305 Intergraph Way

Madison, AL 35758

Documentation

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

Other Documentation

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

144/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

Terms of Use

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

Disclaimer of Warranties

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

145/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL

EVALUATION AS TO THE USEFULNESS OF THE SOFTWARE IN HIS OWN

ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

Limitation of Damages

IN NO EVENT WILL HEXAGON BE LIABLE FOR ANY DIRECT, INDIRECT, CONSEQUENTIAL INCIDENTAL, SPECIAL, OR PUNITIVE DAMAGES, INCLUDING BUT

NOT LIMITED TO, LOSS OF USE OR PRODUCTION, LOSS OF REVENUE OR PROFIT, LOSS OF DATA, OR CLAIMS OF THIRD PARTIES, EVEN IF HEXAGON HAS BEEN

ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

UNDER NO CIRCUMSTANCES SHALL HEXAGON’S LIABILITY EXCEED THE AMOUNT

THAT HEXAGON HAS BEEN PAID BY LICENSEE UNDER THIS AGREEMENT AT THE

TIME THE CLAIM IS MADE. EXCEPT WHERE PROHIBITED BY APPLICABLE LAW, NO

CLAIM, REGARDLESS OF FORM, ARISING OUT OF OR IN CONNECTION WITH THE

SUBJECT MATTER OF THIS DOCUMENT MAY BE BROUGHT BY LICENSEE MORE THAN

TWO (2) YEARS AFTER THE EVENT GIVING RISE TO THE CAUSE OF ACTION HAS

OCCURRED.

IF UNDER THE LAW RULED APPLICABLE ANY PART OF THIS SECTION IS INVALID, THEN HEXAGON LIMITS ITS LIABILITY TO THE MAXIMUM EXTENT ALLOWED BY SAID

LAW.

Export Controls

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

146/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

1. To Cuba, Iran, North Korea, Syria, or the Crimean, “Donetsk People’s Republic”,

“Luhansk People’s Republic,” or Sevastopol regions of Ukraine, or any national of these countries or territories.

1. To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List. Visit www.export.gov for more information or follow this link for the screening tool:

https://legacy.export.gov/csl-search [https://legacy.export.gov/csl-search](https://legacy.export.gov/csl-search) .

1. To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Hexagon, its subsidiaries, or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.
2. To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.

Any questions regarding export/re-export of relevant Hexagon software product, customized software, Technical Data, and/or third-party software obtained from Hexagon, its subsidiaries, or distributors, should be addressed to Hexagon’s Export Compliance Department, 305

Intergraph Way, Madison, Alabama 35758 USA or at exportcompliance@hexagon.com.

Customer shall hold harmless and indemnify Hexagon and a Hexagon Group Company for any causes of action, claims, costs, expenses and/or damages resulting to Hexagon or a Hexagon Group Company from a breach by Customer.

Trademarks

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, Intergraph Smart® Cloud, PDS®, FrameWorks®Plus, I-Route, I-Export, Isogen®, Intergraph Spoolgen®, SupportManager®, SupportModeler®, SAPPHIRE®, TANK®, PV Elite®, CADWorx®, CADWorx DraftPro®, GT STRUDL®, CAESAR II® , and HxGN SDx®

are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners.

Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

147/148

3/19/25, 10:37 AM

Hexagon Documentation Site Export

Copyright

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/09a8a43f-35d1-4ca5-8c0d-80879207e456

148/148

- *