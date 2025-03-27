# SP&ID D-Manager MD

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Drawing Manager**

**Hexagon Documentation**

Generated 03/13/2025

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

1/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Table of Contents**

Intergraph Smart® P&ID Drawing Manager

Navigating in Drawing Manager

Understanding the Drawing Icons

Open Database Command (File Menu)

Customize Current View Command (View Menu)

Include Subnodes Command (View Menu)

Select Al Command (Edit Menu)

Filter Command (View Menu)

Clear Filter Command (View Menu)

Properties Command (Edit Menu)

Exit Command (File Menu)

Working with Drawings

Finish Load Plant Structure Processing Command (Tools Menu)

Create a New Drawing

New Drawing Command (File Menu)

New Drawing Dialog

Open a Drawing

Open Drawing Command (File Menu)

Viewing Drawings

Updating Drawings

Importing Drawings

Global Validation Command (File Menu)

Upgrade Drawings Command (File Menu)

Copy Command (Edit Menu)

Paste Command (Edit Menu)

Delete Command (Edit Menu)

Unlock Plant After Group Rename Command (Tools Menu)

Working with Projects

Working with Off-Site Projects

Working with Drawings within a Project

Sample Project Workflows

Working with Drawing Versions and Revisions

Using Drawing Versions

Creating a New Version of a Drawing

Recovering Drawings

Comparing Drawing Versions

Revising Drawings

Saving Drawings

Save Drawings in Other Formats

Enable Save As XML

Configuration File Settings for AutoCAD Translation

Configuration File Settings for MicroStation Translation

Save As Command (File Menu)

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

2/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Save As Dialog

Save As Dialog Box (Multiple Drawings Selected)

PDF Settings Dialog

Printing Multiple Drawings

Print Dialog

Apply Display Set Dialog

Display Set Legend

Print Command (File Menu)

Define a Display Set

Working with Auto Display Sets

Print Preview Dialog

Settings Dialog

Print Status Dialog

Print Multiple Drawings

Using Workshare

Using Workshare in an Integrated Environment

Workshare Common Tasks

Using Workshare with Projects

Sample Workshare with Projects Workflows

Publishing and Assigning Ownership

Getting Latest Versions of Drawings

Synchronizing Reference Data

Synchronizing Shared Items

Scheduling Workshare Tasks

Integration

Registering Tools

Integration with HxGN SDx2

Integration with SmartPlant Foundation

Upgrade Schema Command

Scheduling Wizard

Scheduling Tasks

Schedule Task Wizard

Assign User Rights for Scheduled Tasks on Windows 10

Schedule a Task

Troubleshooting

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

Glossary

active placement point

alias

annotations

archive

attribute

backup

batch processing

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

3/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Boolean operator

branch point

break label

cache

catalog

check in

class

client

client/server database

code list

col aboration

column

commodity code

commodity item

commodity option

component

concentric

configuration files

connect point

connectivity

connector

data dictionary

data model

database

database administrator

database link

database table

design file

design-wide break

display-only annotation

drawing file

drawing, P&ID, PFD

driving label

easting

edge-edge model

enumerated list

equipment components

equipment group

exclusive database relationship

exit elevation

filter

fixed point

flow rate

flow time

ful path name

gap

glyphs

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

4/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

hierarchical

hierarchy

horizontal angle

horizontal distance

host

implied piping component

inline

inline instruments

instance

instrument loops

instruments

interference checking

isometric

item

item type

keypoint

label

line route

line style

loop

macro

mirror

mirror handle

model

model file

MTO

net service alias

net service name

network

node name

northing

nozzle

offline

offline instruments

Oracle Net

Oracle Net Manager

ORACLE_HOME

orientation by system

orientation by user

orientation fixed

orthogonal view

P&ID

parameter

parametric item

path name

peak flow

PFD

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

5/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

pipe run

pipeline

Piping and Instrumentation Diagram (P&ID)

piping components

Piping Materials Class (PMC)

piping network

piping segment

plant

plant group items

plant structure

project

projection lines

property

publish

publishing method

reference data

reference file

Relational Database Management System (RDBMS)

relationship

relative mode

relative path name

report template

required item

revision cloud

revision triangle

rule

satel ite

satel ite slot

schema

schema file

schematic file

search criteria

segment

select list

server

signal lines

signal run

site

site server .ini file

SP_IDs

Standard Query Language (SQL)

static Oracle port

stockpile

style

subnet

subnet mask

subscribe

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

6/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

subscribe access

symbology

table

template

time stamping

transaction

UNC path

unit

user name

validation

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

7/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Intergraph Smart® P&ID Drawing Manager**

Intergraph Smart® P&ID Drawing Manager handles functionality having to do with the drawing files in Smart P&ID. You do not modify the designs themselves in Drawing Manager, but you do create, open, modify, and delete drawings and drawing properties. Drawing Manager is also the interface for printing multiple drawings and for upgrading drawings to the current version of Smart P&ID.

Drawing Manager includes version tools for creating, comparing, and recovering deleted drawing versions. These operations are carried out with commands on the **Revisions** menu.

The Workshare capability of Smart P&ID is carried out in Drawing Manager. These commands are on the **Workshare** menu in Drawing Manager. The actual host and satellite sites are specified and configured in Smart Engineering Manager.

**Smart P&ID Installation and**

**Drawing Management**

**Creating and Editing Drawings**

**Configuration**

Installing Smart P&ID

Navigating in Drawing Manager

Creating P&IDs in Smart P&ID

Hardware and Software

Working with Drawings

Creating D&IDs in Smart P&ID

Recommendations

Working with Drawing Versions

Comparing and Refreshing

Upgrading Smart P&ID

and Revisions

Versions

Saving Drawings

Printing Multiple Drawings

**Working with Smart P&ID Data**

**Printing and Reports**

**Smart P&ID Reference Data**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

8/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Modifying Item Properties

Printing Drawings

Understanding Reference Data

Settings

Navigating in the Engineering Data Generating Reports

Editor

Customizing Your Reference Data

System Editing

Upgrading Reference Data

Plant Editing

Consistency Checking

Importing Drawing Data

**Projects, Workshare, and**

**Tools and Utilities**

**Additional Features**

**Integration**

Smart P&ID Project Management

Duplicate Item Tag Report Utility Using Auxiliary Graphics

Using Workshare

Insulation Specification Manager Smart P&ID Symbol Libraries

Working with SmartPlant

Options Manager

Comparison of Smart P&ID with

Integration

PDS 2D

Rule Manager

Integration with Smart Completions

Smart P&ID to PDS Piping Data

Smart P&ID Utilities

Transfer

**Troubleshooting**

General Smart P&ID

Troubleshooting

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

9/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Copy and Paste EDE Data -

Troubleshooting

Smart P&ID to PDS Piping Data

Transfer - Troubleshooting

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2025 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 2/28/2025 at 12:54 PM

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

10/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Navigating in Drawing Manager**

The main Drawing Manager interface is split into two main panes: the **Tree** view, where plant groups are arranged in nodes, and the **List** view, where lists of drawings appear.

You can control the display in the **List** view in many ways: add a filter so that only drawings that match specific criteria are displayed, display all drawings that reside under the selected node in the **Tree** view, and specify which and in what order drawing properties appear in the **List** view. The following commands are needed to carry out these activities.

**Open Database**

Used to open a site so that you can access a plant or project and its related drawings. For more information,

see Open Database Command (File Menu).

**Customize Current View**

Allows you to specify the drawing properties that you want to appear in the **List** view. For more information,

see Customize Current View Command (View Menu).

**Include Subnodes**

Controls the depth of display in the **List** view. For more information, see Include Subnodes Command (View

Menu).

**Select All**

Selects all of the drawings in the **List** view. For more information, see Select All Command (Edit Menu).

**Filter**

Allows you to filter out drawings that you do not want displayed in the **List** view. For more information, see

Filter Command (View Menu).

**Clear Filter**

Used to clear any filters applied to the **List** view. For more information, see Clear Filter Command (View

Menu).

**Properties**

Displays properties related to the selected plant group or drawing. For more information, see Properties

Command (Edit Menu).

**Exit**

Used to close Drawing Manager. For more information, see Exit Command (File Menu).

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

11/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You can drag-and-drop drawings from one plant group to another plant group, providing the drawings are in the same plant structure and the **Allow P&ID Drawings** option has been enabled in Smart Engineering Manager.

**Understanding the Drawing Icons**

In the Drawing Manager **List** view, each drawing is accompanied by an icon that indicates the drawing status and ownership.

New drawing in the Plant, not checked out to a project.

New drawing in a project of the Plant, belonging to that project.

New drawing that belongs to a different project as viewed from the Plant or as viewed from your project.

Drawing that has been fetched AND is owned by your project.

Drawing that has been fetched with read/write permissions AND is not owned by your project.

Drawing that has been fetched with read-only permissions OR is not owned by your project.

Drawing that has been checked out AND is owned by your project or non-Workshare plant or project.

Drawing that has been checked out AND is not owned by your project.

On the **Check Out** dialog in the Plant, fewer drawing states are needed.

Drawing that is not checked out.

Drawing that is checked out to a project.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

12/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

The software indicates out-of-date drawings by displaying the icon in the **Out-of-Date Drawing Status** column. To display this column, do the following:

1. Select **View** > **Customize Current View**.
2. On the **Customize Current View** dialog, from the **Drawing properties** list, select **Out-of-Date** **Drawing Status**.
3. Select **Add** to copy this property to the **Selected properties** list.

**Open Database Command (File Menu)**

Opens the **Open Plant Structure** dialog, allowing you to connect to the site server containing the drawings that you want to work with. Choosing the appropriate SmartPlantV4.ini file connects you to that site. You can also view the plants to which you have recently been connected.

In order to use this command, your computer must be able to connect to the network where the server is located.

**Open Plant Structure Dialog**

Sets options for connecting to a site and plant structure and passes user access information to the application. This dialog opens when you select **File** > **Open Database**.

**Available plant structures**

Lists those plant structures found on the network. You can select only one item from this list at a time.

**Application Type**

Allows you to select an application for filtering the available plant structures that are associated with that application. If all the plants in the site are associated with one application only, the value is read-only.

**Open**

Connects you to the selected plant or project database. The **Open** command also checks to make sure you have the correct access privileges for the selected database and passes your access information back to Drawing Manager.

**Site Server**

Opens the **Open Site Server** dialog, allowing you to select the SmartPlantV4.ini file for the site you want to access. Plant structures contained in the site you selected display in the **Available plant structures** list.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

13/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Connect to a Database**

1. Select **File** > **Open Database**.
2. On the **Open Plant Structure** dialog, select **Site Server**.
3. On the **Open Site Server** dialog, select the correct SmartPlantV4.ini file and select **OK**.
4. Select **Open**.

If the site server .ini file that you need appears on the **File** menu in the list of recently opened items, you can select it and open that database immediately.

**Customize Current View Command (View Menu)**

Opens the **Customize Current View** dialog, allowing you to specify the drawing properties that you want to appear in the **List** view.

**Customize Current View Dialog**

Sets options for the information that is displayed in the **List** view of Drawing Manager. This dialog opens when you select **View** > **Customize Current View** on the main menu bar.

If you are working in a Project, you can also select the **Custom View** button on the **Fetch** dialog.

**Drawing properties**

Lists the drawing properties that are available for display in the **List** view. Select a property from this list and select **Add** in order to move it to the **Selected properties** list.

**Selected properties**

List the properties that will display in the **List** view.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

14/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Add**

Moves the property into the **Selected properties** list so that the selected information is displayed in the **List** view.

**Remove**

Moves the selected property back into the **Drawing properties** list. That information will no longer display in the **List** view.

**Move Up**

Moves the property you select in the **Selected properties** list up one position. Use this button to further customize the way the columns in the **List** view are displayed.

**Move Down**

Moves the property you select in the **Selected Properties** list down one position. Use this button to further customize the way the columns in the **List** view are displayed.

**Customize the List View**

1. Select **View** > **Customize Current View**.
2. On the **Customize Current View** dialog, move the drawing properties that you want to appear in the **List** view to the **Selected properties** list by selecting the property in the **Drawing properties** list and selecting **Add**.
3. Rearrange the display order of the properties in the **Selected properties** list by selecting **Move Up** or **Move Down**.
4. Select **OK**.

Use Filter the List View to control which drawings are displayed in the **List** view.

To display all drawings in the selected plant hierarchy node, use the **View** > **Include Subnodes**

command. For more information, see Display Subnodes in the List View.

You can drag-and-drop drawings from one plant structure to another, provided P&IDs are allowed in the target plant structure.

You can sort drawings in the list view by a chosen drawing property. For more information, see Sort

Drawings in the List View.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

15/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Sort Drawings in the List View**

Select the column header of the drawing property you want to use for sorting. Select the header again to toggle between ascending and descending order.

When updating out-of-date drawings, the order in which the drawings appear in the **Update Drawings** dialog corresponds to the sort order.

When the **Include Subnodes** command is activated, the drawings are sorted independently in each subnode by the selected property.

**Include Subnodes Command (View Menu)**

Displays in the **List** view all of the drawings that reside under the selected plant in the **Tree** view, not only those drawings that reside directly under the selected node.

If you select a plant in the **Tree** view and then select **View** > **Include Subnodes**, the entire plant hierarchy is displayed in the **List** view. This command provides an easy way of viewing the plant hierarchy without having to open every unit.

**Display Subnodes in the List View**

Select **View** > **Include Subnodes** or select the **View Subnodes** button on the main toolbar.

After activating this command, when sorting drawings by a selected property, the drawings are sorted independently in each subnode.

**Select All Command (Edit Menu)**

Selects all the drawings displayed in the **List** view.

**Filter Command (View Menu)**

Opens the **Filter** dialog, which allows you to customize the **List** view. You can display only drawings having particular properties if you want.

Any previously-applied filter settings are retained the next time you open the Drawing Manager in the current plant.

**Filter Dialog**

Sets options for the display of drawings in the **List** view. This dialog opens when you select **View** > **Filter** or by selecting **Filter**

on the **Fetch** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

16/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Definition**

Displays all defined criteria associated with a filter. To add to or modify the definition list, you must select a line in the list and then define or edit the property in the **Edit** group.

**Match all**

Specifies the items matching ALL of the filtering criteria pass through the filter.

**Match any**

(Default) Specifies the items matching any one or more of the filtering criteria pass through the filter.

**Add**

Places a new entry at the end of the existing definition list and enables the options in the **Edit** group so that you can edit the new entry.

**Delete**

Removes the selected criterion from the definition list. This button is available only when you select a criterion in the definition list.

**Edit**

Allows you to define or edit a single line of filter definition criteria.

**Property**

Displays a list of all properties for a certain item type. Examples of properties include revision number and name. You define or modify filtering criteria by selecting a property, an operator, and a value.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

17/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Operator**

Specifies the relationship between the property and its value. These relationships include greater than, >; equal to, =; not equal to, <>; and so forth.

**Value**

Lists appropriate values for the property specified in the **Property** list. If a list of attributes is not already associated with the **Value** box, you must choose null or type a value, which can be free text. You can type a percent sign (**%**) as a wildcard character to find multiple characters or an underscore (_) as a wildcard character for a single character. Do not use an asterisk (*****) in the **Value** box.

**Filter the List View**

1. Select **View** > **Filter**.
2. On the **Filter** dialog, specify the details of the drawings that you want to displayin the **List** view. For instance, if you want to display only drawings with revision number of 1, define *Revision = 1* in the **Edit** box.
3. To add more filter criteria, select **Add** and specify further details of the drawings that you want to see in the **List** view. Be sure to select **Match All** or **Match Any**, depending on the appropriate choice for your display.
4. Select **OK**.

Filter criteria are case-sensitive.

View filters in Drawing Manager are strictly established only for the specific case at hand and are retained the next time you open Drawing Manager in the current plant.

If you select a different plant, the filter is cleared.

You cannot save individual filter settings.

Select **View** > **Clear Filter** to remove an applied filter. If you have not applied a filter to the view, the **Clear Filter** command is not available.

When using the **<** , **<>** , and **>**  operators in a filter item, null values are not included in the filtered results. To include null values, the operator **=** and the value **Null** have to be added to the **Filter** **Definition**. For example, if all drawings that do not have a **Title Block Revision** value equal to **R1** are to be filtered, then the filter definition is set to **Match any** and the following criteria used in the **Filter** **Definition**:

Title Block Revision <> R1

Title Block Revision = Null.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

18/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Clear Filter Command (View Menu)**

Removes a filter from the view and displays all drawings. This command is available only if you have applied a filter to the view.

**Properties Command (Edit Menu)**

Opens the **Properties** dialog, which displays the plant group properties or drawing properties based on the item selected in the **Tree** or **List** view.

Plant group properties are read-only. You can modify some of the drawing properties, such as the name, version, title, description, and so forth.

You can rename and renumber drawings, but be aware of possible naming conflicts when retrieving a drawing using an older name or number. In a plant, you cannot retrieve a version of a renamed or deleted drawing if the current drawing shares the same name or number.

**Displaying Plant Group Properties**

If you select a plant group in the **Tree** view, you can open the **Plant Group Properties** dialog to view the description for the selected plant group.

**Display Plant Group Properties**

1. In the **Tree** view, select the plant group whose properties you want to view.
2. Select **Edit** > **Properties**.

**Modify Drawing Properties**

1. In the **List** view, select a drawing whose properties you want to modify.
2. Select **Edit** > Properties.
3. In the Properties dialog, review or change the property values as necessary.

You can rename and renumber drawings, but be aware of possible naming conflicts when retrieving a drawing using an older name or number. In a plant, you cannot retrieve a version of a renamed or deleted drawing if the current drawing shares the same name or number.

When a drawing (Drawing A) becomes out-of-date for modifying its properties, then all the partner OPCs of Drawing A will also be shown as out-of-date with respect to Out-of-date model items.

Therefore, update Drawing A first, to update the partner OPCs. See Updating Drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

19/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You cannot modify unique and read-only drawing properties after the drawing is created. For instance, the **Template** property value remains unchanged.

**Modify properties of multiple drawings**

1. In the **List** view, select multiple drawings whose properties you want to modify.

To select multiple drawings, press and hold CTRL key or fence select.

1. Select **Edit** > Properties.
2. In the Edit Bulk Properties dialog, make the necessary changes that apply to all the selected drawings.

To modify a value, you can either directly edit the value or select from the list.

To delete a value, you can either select empty value from the list or press the BACKSPACE key.

**Null** value indicates that the property has no value or multiple values from the selected drawings.

Expand the list to see all the values.

The **Edit Bulk Properties** dialog displays only the editable drawing properties.

**How do I add new properties to a drawing?**

Only an administrator or someone with necessary access permissions can add new properties using the Data Dictionary Manager.

**Properties Dialog**

Displays properties of the item selected in the **Tree** or **List** view. This dialog opens when you select **Edit** > **Properties** on the main menu bar or when you select **Properties** on the **Select Drawings** page toolbar

of the Import Drawings Wizard.

**Alphabetical**

Displays properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Category**

Displays properties categorically. Categories are defined and assigned in Data Dictionary Manager. This button acts as a toggle and is available when properties are displayed alphabetically.

**Properties**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

20/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Displays the properties for the selected item. All properties except the plant group properties can be modified. Plant group properties are read-only and are defined during the plant group creation in Smart Engineering Manager.

You can rename and renumber drawings, but be aware of possible naming conflicts when retrieving a drawing using an older name or number. In a plant, you cannot retrieve a version of a renamed or deleted drawing if the current drawing shares the same name or number.

If the property format is set to **a1**, **a2**, or **a3**, the property value displays only 1, 2, or 3 characters, respectively. The number following *a* indicates the character display limit. To display the full value, select formats such as **Variable Length** or **a255**. To change the format, see Add/Modify Property Dialog Box.

**Edit Bulk Properties Dialog**

Displays editable properties of the selected drawings in the List view. This dialog opens when you select multiple drawings and then select **Edit** > Properties.

**Alphabetical**

Displays properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Category**

Displays properties categorically. Categories are defined and assigned in Data Dictionary Manager. This button acts as a toggle and is available when properties are displayed alphabetically.

**Properties**

Displays only the editable properties of selected drawings. Unique and read-only drawing properties are not displayed.

**Null** value indicates that the property has no value or multiple values from the selected drawings.

Expand the list to see all the values.

**Exit Command (File Menu)**

Quits Drawing Manager. If you have customized the **List** view, that layout is retained and any filters you have applied will be retained as long as you are working within the same plant.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

21/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Working with Drawings**

Drawing Manager enables you to manage your process and instrumentation drawings by allowing you to create new drawings in your plant structure, open and view drawings, and delete drawings. The following commands are needed to carry out these activities.

**New**

Used to create a new drawing. For more information, see New Drawing Command (File Menu).

**Open**

Opens a drawing in Smart P&ID. Drawing Manager checks to make sure that you have the appropriate

permissions for opening or modifying drawings. For more information, see Open Drawing Command (File

Menu).

**Copy**

Used to copy one or more drawings from within the same plant or same project. The copied drawing(s) can then be placed using the **Paste** command. To copy a drawing from one plant to another plant, refer to the **Import Drawing** command. Any graphics that have been repaired should be deleted and replaced prior to using this command.

**Paste**

Places a copy of a drawing in the selected plant or project. Any graphics that have been repaired should be deleted and replaced prior to using this command.

**Revision History**

Displays the revision history of a drawing. For more information, see Revision History Command (Revisions

Menu).

**Version History**

Displays the version history of a drawing, provides access to the **Compare** and **Compare With** commands for viewing changes between drawing versions, and the **View** command, which allows you to view a

drawing as read-only without opening Smart P&ID. For more information, see Version History Command

(Revisions Menu).

**Delete**

Used to remove drawings from the plant. For more information, see Delete Command (Edit Menu).

You must have the appropriate permissions, which are assigned in Smart Engineering Manager, in order to carry out these operations.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

22/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Finish Load Plant Structure Processing Command (Tools Menu)** Renames all item IDs, of all the drawings, of the plant that you have copied and loaded using the Load Plant Structure Wizard in Smart Engineering Manager.

This operation can only be carried out by an administrator with Full Control Permissions to Options Manager.

Opening the copied plant structure in Smart P&ID or Drawing Manager before completing this process is not possible.

When loading a plant for which the **Keep unique identifiers from source** check box on the **Associate Applications** page of the Load Plant Structure Wizard was selected, and where the name of the loaded plant is the same as the source plant name, this command is not required and is therefore disabled.

**Create a New Drawing**

1. In the **Tree** view, select the plant in which you want to create a new drawing.

The **New Drawing** command is not available if the node you choose does not permit drawings to be created under it. Permissions for drawings in a given node are set in the hierarchy templates in Smart Engineering Manager.

1. Select **File** > **New Drawing**.
2. On the **New Drawing** dialog, fill in the information that describes your new drawing.

If you are using a utility that communicates data from an authoring tool to PDS, remember that there can be no spaces in the path to a drawing, therefore you should name your drawings accordingly.

For the **Document Type** property, you must select **P&IDs** or **D&IDs** according to the desired designation of the drawing.

1. Select **Create** to generate the new drawing and add it to the plant node; the **New Drawing** dialog remains open so that you can create more drawings under this node.
2. Select **OK** to create the new drawing, close the dialog, and return to the main Drawing Manager interface.

You can modify the drawing properties that appear in the **New Drawing** dialog by modifying them in **Database Tables** in Data Dictionary Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

23/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You can specify whether certain drawing properties are required or optional in Options Manager. The **Document Type**, **Drawing Number**, **Name**, **Path**, and **Template** properties are always required for being able to view the drawing.

The properties - **Drawing Number** and **Name,** should be unique within each plant.

For the **Name** property, the following characters are not allowed: / \ : * ’ ? ” < > |. For the **Drawing** **Number** property, the single quote (’) character is not allowed.

Several standard templates are delivered with Smart P&ID, and you can create new templates in Smart P&ID. If you want to create custom border files for your drawing templates, use Intergraph SmartSketch. You can then embed your border file in the new templates you create in Smart P&ID.

After you embed a border file into a drawing template and a drawing is created in Drawing Manager using that template, any changes to the border file are not reflected in drawings created prior to the change.

**New Drawing Command (File Menu)**

Opens the **New Drawing** dialog where you specify properties for a new drawing. The drawing is created under the currently selected plant group node in the **Tree** view.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to be able to create drawings.

**New Drawing Dialog**

Sets options for the new drawing that will be created under the plant group node that you select in the **Tree** view. This dialog opens when you select **File** > **New Drawing**.

The properties - **Drawing Number** and **Name,** should be unique within each plant.

For the **Document Type** property, you must select **P&IDs** or **D&IDs** according to the desired designation of the drawing.

The **Drawing Number**, **Name**, and **Template** properties on a drawing are always considered as Read/Write by **Drawing Manager** even when set to Read Only within the **Data Dictionary Manager**.

This is because these properties must be set when creating a drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

24/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Alphabetical**

Displays drawing properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Category**

Displays drawing properties in categories. This button acts as a toggle and is available when properties are displayed alphabetically.

**OK**

Creates the new drawing, adds it to the selected plant node, and closes the **New Drawing** dialog.

**Cancel**

Closes the **New Drawing** dialog without creating a new drawing.

**Create**

Creates a new drawing and adds it to the selected plant node. This button is available only after you enter values for the **Required Fields** in the list of drawing properties.

**Open a Drawing**

1. In the **Tree** view, select the node in which the drawing resides.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

25/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. In the **List** view, select the drawing that you want to open.
2. Select **Open**

on the main toolbar.

1. View or modify your drawing in Smart P&ID.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to view or modify drawings.

If you only want to quickly view a read-only version of the drawing, you can do so inside Drawing Manager, without opening Smart P&ID. For more information, see View a Drawing in Drawing

Manager.

**Open Drawing Command (File Menu)**

Opens the selected drawings in Smart P&ID.

**Viewing Drawings**

You can open a read-only display of a drawing using commands in Drawing Manager without having to open the full-blown design software. Although you cannot edit the drawing from Drawing Manager, you can view the graphics and properties assigned to drawing items. In some cases, this capability can save you time and effort.

For details of how to view a drawing, see View a Drawing in Drawing Manager.

You can use this viewing functionality on the current drawing in the database or on any of the saved versions for a drawing, too. However, a version, either current or saved, must exist in order to use this viewing capability. Versions are automatically created once the drawing is opened and changed for the first time; otherwise, the **New Version** command can be used to save a version.

Most of the commands to manipulate the view are also available. That is, you can zoom in on an area in the drawing, fit the drawing to the display space, pan across a drawing, and so forth. You can also use buttons on the **Properties** window toolbar to manipulate the display of properties for a selected drawing item or items.

**View a Drawing in Drawing Manager**

1. In the **List** view, select the drawing you want to view.
2. Select **Version History** on the main toolbar.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

26/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. In the **History** list on the **Version History** dialog, select the current drawing or a saved version in the list.
2. Select **View**.
3. On the **View** dialog, manipulate the view or select an item and review its properties.
4. Select **Close**.

Viewing a drawing or version in Drawing Manager is always limited to read-only permissions. If you want to edit a drawing, you must do so in Smart P&ID.

A version of a drawing must exist before you can open the **View** dialog and display the drawing. For

more information about creating versions, see Save a Version of a Drawing.

**Updating Drawings**

Changes are often made to the Smart P&ID Reference Data while work is being managed on the P&IDs.

When these changes are made, they apply to all drawing items after the time of change, but do not apply to existing drawing items. The Update Drawings functionality (provided by the set of **Out-of-Date Drawings** commands) allows you to manage which drawings are updated with the latest reference data changes by defining values that define out-of-date drawings criteria and by resolving any symbols that have been deleted, moved, or renamed.

Be sure to back up your work or create a version prior to using these commands.

These updates do not apply to assemblies.

To establish criteria for defining out-of-date drawings, use the Out-of-Date Drawing Criteria command.

You can also create reports for out-of-date drawings and schedule update operations. See Report

Command (Out-of-Date Drawings) and Schedule Update Command (Out-of-Date Drawings).

Using the Update Drawings functionality is not required as part of the upgrade process, but it is strongly recommended.

After upgrading to the latest version of Smart P&ID, opening Options Manager for the first time updates the RAD version for the ProjectStyles.spp file and as a result, changes the status of the Symbology for the drawings to ‘Out-of-Date’. For this reason, after upgrading Smart P&ID, you should open and close Options Manager once *before*  updating your drawings using Smart P&ID Drawing Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

27/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

After upgrading Smart P&ID from a version earlier than 2014, you should open and close Rule Manager once **before** updating your drawings using Smart P&ID Drawing Manager. This ensures that the Rules.rul file is updated with the new rules. The following rules were added in SmartPlant P&ID

## 2014:

### Connect To Process To Duct Run

Duct Run

Duct Run Label

Duct Run OPC To Duct Run

Duct Run To Duct Run

Duct Run To Nozzle

Ducting Components

Ducting Component Label

Ducting Comp To Duct Run

Ducting Comp To Ducting Comp

Ducting Comp To Instrument Inline

Ducting Comp To Nozzle

Ducting Comp To Signal Pipe Run

Instrument Inline To Duct Run

Internal Nozzle To Room

Nozzle To Room

Process Pipe Run to Ducting Comp

Room

Room Component

Room Component Label

Room Comp to Room

Room Comp to Room Comp

Room Label

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

28/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If an existing rule has the same name as one of the new rules, a numeric suffix is added to the name of the new rule, for example: ‘Duct Run_1’

When you submit a selection of P&IDs to the **Out-of-Date Drawings** > **Update** command, Drawing Manager analyzes the drawing for changes to the following:

Data Dictionary (select lists)

Formats

Symbols (moved and missing symbols, and changes to the .sym file) Rules Manager

Options Manager (heat tracing, gapping, and symbology)

Model Items (via Llama)

OPCs (moved)

Drawings in a **Re-create** state

Drawing Properties

After this analysis process, a summary displays, listing the number of drawings selected, the number of out-of-date drawings, and the number of drawings with missing symbols. You must manually resolve the missing symbols using the **Resolve Missing Symbols** dialog, which lists the symbols in question and allows you to define the new location of each symbol.

In addition to the interactive approach of updating drawings, you can schedule the entire update process, except for the resolution of missing symbols, which is a manual process as described above.

The reporting capability provides a summary of the selected drawings and the out-of-date criteria detected during the analyze step. This report format is non-configurable.

**Out-of-Date Drawings Command (File Menu)**

These commands allow reference data changes to be applied to existing drawings. Available commands are:

Update Command

Report Command

Schedule Update Command

Refresh Template Command

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

29/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

To establish criteria for defining out-of-date drawings, use the **Out-of-Date Drawing Criteria** command on

the **Tools** menu.

**Update Command**

When you select this command, the selected drawings are analyzed based on the out-of-date criteria and

the results are displayed in the Update Drawings Dialog.

Intergraph recommends that you backup your work or create a version of your work prior to using this command.

If you need to reapply template settings on a drawing or to update inserted or embedded drawing

items after a version upgrade, see Refresh Template Command.

Update does not update any symbol whose definition has been changed into a break component. This situation occurs when you have a catalog item that has been placed in a drawing and then you change its definition to be a break component. The Smart P&ID **Replace** command does not allow a non-breaking component to be replaced with a break component. The **Update** command relies on the Smart P&ID **Replace** command to replace symbols that are out-of-date.

If an item type property has **Write Modeler** or **Write Both** permissions in Data Dictionary Manager and a symbol belonging to the item type is changed in Catalog Manager, running the **Update** command will NOT overwrite values assigned to this property with any default that may have been pre-defined in Catalog Manager. If the property permissions are **Write Catalog** in Data Dictionary Manager, **Update** will restore any default property values defined in Catalog Manager.

Certain symbol properties, such as the item’s **Type**, are hardcoded to be set at the Catalog level. These properties should not be changed at the Modeler level, as this can result in unexpected symbol behavior.

If a default value has been set for a property in Data Dictionary Manager, running the **Update** command will overwrite null values of this property in out-of-date symbols with the default value. If a symbol has a property value other than null, this value will not be overwritten.

If the path to your Rules.rul file is set incorrectly in Smart P&ID Options Manager, the **Update** command will not work. For example, if the path is invalid, then all drawings in the project are in an out-of-date state but the software cannot update them. This error also occurs if the **Catalog Explorer** **Root Path** specified in Smart P&ID Options Manager is invalid. An error message displays and the report displays **Drawings with a ? in the criteria column have missing or incorrect reference** **data**.

You can enable enhanced logs for the status of recreate and update drawing workflows to diagnose, troubleshoot, and resolve any issue. See, Log Files.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

30/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Update Drawings Dialog**

This dialog opens when you run the **Update** command or the **Refresh Template** command.

**Total drawings selected**

Displays the number of drawings selected.

**Report**

Generates a Microsoft Excel report describing the details of out-of-date drawing(s).

**Out-of-date drawings**

Displays the number of drawings that are out-of-date based on the criteria selected using the **Out-of-Date** **Drawing Criteria** dialog.

**Resolve**

Displays the **Resolve Missing Symbols** dialog. Use this button to resolve any missing symbols.

**Drawings with missing symbols**

Displays the number of out-of-date drawings containing symbols that do not exist in the catalog. Select **Resolve** to fix this issue in the drawings affected.

**Resolve Missing Symbols Dialog**

This dialog provides a way for you to define any symbols that have been deleted, moved, or renamed. It appears when you select the **Resolve** command in the **Update Drawings** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

31/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

In order to resolve any missing symbols, you must have an existing symbol in the catalog to define as the replacement for the missing symbol.

You cannot resolve missing symbols for offline instruments of a different class using this command.

**Old Path**

Displays the relative path of the missing symbol.

**New Path**

Displays possible options for defining correct locations for the missing symbol(s).

**Drawings**

Displays the list of drawings that contain the missing symbol(s).

**Report Command**

Displays detailed information about out-of-date drawings. Criteria that can be checked includes select list values, formats, out-of-date symbols, missing symbols, rules, heat tracing, gapping, symbology, OPCs, and so forth.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

32/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You must select one or more drawings prior to selecting this command. The information displays in Microsoft Excel and is based on options selected using the **Out-of-Date Drawing Criteria** command. If all drawings are up-to-date, a message box displays stating that all selected drawings are up-to-date.

When upgrading a plant, drawings may be out of date for any of the out‑of‑date criteria.

In order to use this command, you must be assigned the user right **Update P&ID** on the **Role** **Properties** dialog in Smart Engineering Manager. Also, you are required to have **Full Control** assigned on **P&ID Objects**.

**Schedule Update Command**

Displays the **Schedule Task Wizard**. Use this wizard to schedule the update operations for any out-of-date drawings. For information about using this wizard, refer to Schedule Task Wizard.

In order to use this command, you must be assigned the user right **Update P&ID** on the **Role** **Properties** dialog in Smart Engineering Manager. Also, you are required to have **Full Control** assigned on **P&ID Objects**.

If you are logged in as a standard user on a Windows 10 operating system, your System Administrator

must assign you special user rights to be able to run scheduled tasks. For details, see Assign User

Rights for Scheduled Tasks on Windows 10.

Any changes made to the out-of-date drawing settings after the task is scheduled will not affect the scheduled task.

If update drawings processing is scheduled for a hierarchy item, select in the Tree view, at the scheduled time all the drawings under it are analyzed and only the out-of-date drawings are updated.

If update drawings processing is scheduled for drawings, selected in the List view, at the scheduled time only the selected drawings are analyzed and the out-of-date drawings are updated.

Drawings with missing symbols are logged but not updated. Drawings that do not require an update are logged with a message that the drawing is up-to-date.

**Refresh Template Command**

This command reapplies the current template settings to the selected drawings and cancels any changes made directly in the drawings such as moving or deleting a SmartFrame or a logo that originates from the template. After running this command, the selected drawings are left in a recreate state and the Update

Drawings Dialog Box box opens to allow you to recreate the drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

33/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Intergraph recommends that you backup your work or create a version of your work prior to using this command.

Running this command skips drawings that are already in a recreate state. Details appear in the smartpid.log file. You must first recreate these drawings before refreshing the template.

The following examples represent situations where it is recommended to run this command: When corrupted template objects or new objects appear in drawings, especially after upgrading the Smart P&ID plant and then recreating the drawing.

When you change a drawing template and you want the changes to be implemented in existing drawings associated with that template.

If a logo or picture that comes from the template became corrupted or was deleted by mistake.

If a Smart Frame was moved unintentionally and you want to restore its original position in the drawing.

**Out-of-Date Drawing Criteria Command (Tools Menu)**

Displays the Out-of-Date Drawing Criteria Dialog, from which you can define the criteria used to search for

out-of-date values when you use the **File** > **Out-of-Date Drawings** commands.

**Out-of-Date Drawing Criteria Dialog**

Allows you to define the criteria used to search for out-of-date values when you use the **File** > **Out-of-Date** **Drawings** commands.

**Select out-of-date drawing criteria**

**Select List Changes**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

34/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Data Dictionary Select List GUID on the drawing item is not equivalent to select list GUID in Data Dictionary.

PID Select List GUID on the drawing item is not equivalent to the select list GUID in PID schema.

**Format Changes**

Formats GUID on the drawing item is not equivalent to Formats GUID from the database. Default Formats GUID on the drawing item is not equivalent to Default Formats GUID in Options Manager setting.

**Out-of-Date Symbols**

File Last Modified Time Stamp on at least one representation in the drawing is not equivalent to the File Last Modified Time Stamp on the corresponding symbol definition file.

**Missing Symbols**

Filename specified for at least one representation in the drawing does not have the corresponding symbol definition file available in the current catalog.

**Rule Changes**

Rules GUID on the drawing item is not equivalent to the GUID from the Rules file.

**Heat Trace Changes**

Heat Trace GUID on the drawing is not equivalent to the Heat Trace GUID in Options Manager Setting.

**Gapping Changes**

Gapping GUID on the drawing item is not equivalent to the Gapping GUID in Options Manager Setting.

**Symbology Changes**

Symbology GUID on the drawing item is not equivalent to the Symbology GUID in Options Manager Setting.

**Out-of-Date Model Items**

SP_ModelItemTimeStamp for at least one representation in the drawing is not equivalent to the TimeStamp on the History Item of its Model Item. This criterion covers model items updated via Llama (outside the drawing).

**Moved OPCs**

MatingOPCPath (will have Drawing ID of its mate) on the OPC is not equivalent to the SP_DrawingId of its mate OPC. The OPC label is in a to-be-updated state as its mate has been moved.

**Recreate State**

The drawing is in a re-create state.

**Drawing Property Changes**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

35/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Property Changes GUID on the drawing item is not equivalent to Drawing Property Changes GUID on the drawing item. Drawing Property Changes GUID is set when drawing properties are modified from Drawing Manager.

**Importing Drawings**

The **Import Drawings** command allows you to copy drawings from another plant in the same site or a different site. An import map file is used to match attributes. The software uses a delivered map file to map any customized attributes, select list entries, and symbols between the target and source plants. Using the wizard, you can create and save your own map files. In order to be able to edit the import map file, you must have permission as assigned in Smart Engineering Manager. Using the **Roles Properties** dialog and the **Rights** tab, you must select the **Drawing Management** option **Edit Import Map** in order to be able to edit a map file.

There are several import drawing options also available in Options Manager. The **Import Map Path** setting defines where your map files will reside on the system. The **Import Transformation Program** controls the depth of the data transformation. A transformation program is delivered with the software but you can copy and edit the program to fit your requirements. For example, you could edit the program to clean individual property values, categories of values, or you can flag values that are set during the copy process.

Any graphics that have been band-aided should be deleted and replaced prior to using this command.

If your target plant uses a shorter data string value than the source plant, the string will be truncated.

For example, if the source plant has a maximum character value of 80 set for a field, and the target plant has a maximum character value of 40 set for the same field, only the first 40 characters of the field will be mapped.

If your source drawings and target database use different languages, you are required to use a database created using the UTF-8 character set for unrestricted multilingual support. For example, if the source drawing name contains German characters, they will be converted to English during the import. When you try to open the drawing, the physical file will not be found and the product will try to re-create the drawing.

When importing a symbol’s representation properties, the representation properties are a pure copy of the source symbol.

If the import of drawings fails, the reason will be recorded in the import log file and those drawings will not be included in the re-create process.

When you import a drawing that contains ABE items, the **Source Tag** property will not be copied.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

36/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Drawings Command (File Menu)**

Allows you to copy drawings from another plant in the same site or a different site by using the Import Drawings Wizard.

**Import Drawings Wizard - Welcome**

This screen provides an introduction to the **Import Drawings Wizard**. The wizard screens prompt you for details about your source and target drawings.

**Import Drawings Wizard - Select Source Plant**

Allows you to select the plant that contains the drawings you want to import. Select and use the **Open**

**Plant Structure** dialog to define the system location of the drawings.

**Open Plant Structure Dialog**

Sets options for connecting to a site and plant structure and passes user access information to the application. This dialog opens when you select **File** > **Open Database**.

**Available plant structures**

Lists those plant structures found on the network. You can select only one item from this list at a time.

**Application Type**

Allows you to select an application for filtering the available plant structures that are associated with that application. If all the plants in the site are associated with one application only, the value is read-only.

**Open**

Connects you to the selected plant or project database. The **Open** command also checks to make sure you have the correct access privileges for the selected database and passes your access information back to Drawing Manager.

**Site Server**

Opens the **Open Site Server** dialog, allowing you to select the SmartPlantV4.ini file for the site you want to access. Plant structures contained in the site you selected display in the **Available plant structures** list.

**Import Drawings Wizard - Select Drawings**

Displays a list of drawings available for importing and allows you to select the drawings to be imported.

**Filter**

Opens the **Filter** dialog, which allows you to specify criteria for filtering the drawings that are displayed in the List view.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

37/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Clear Filter**

Deactivates any filter you have applied to the list of drawings that appears in the List view.

**Include Subnodes**

Displays all the drawings and node names that reside in the currently selected node.

**Details**

Displays a detailed view of the drawing properties specified using the **Customize View** option. You can sort by the listed properties. By default, this view shows the **Name** property only, so it will appear the same as the **List** view unless you specify additional properties to display.

**List**

Displays a list of the drawings. One property per drawing is displayed.

**Properties**

Displays the properties for the selected item. These values display in the **Properties** dialog.

**Customize View**

Opens the **Customize Current View** dialog, which allows you to specify the information about each drawing that is displayed.

**Import Drawings Wizard - Missing Symbols Dialog**

Displays a list of missing symbols from the Source Catalog that have been placed on the drawing(s) you are importing. After you select your drawing(s) for import, the software performs an analysis of in-use data. If there are any missing symbols, this dialog displays automatically.

Symbol maps are created for missing symbols but since the symbol is not found in the catalog, the information normally obtained from the symbol (Item Type, Type Value, Connect Point, and so forth) cannot be determined. Symbol maps for missing symbols are marked as **In Use**. The map status is set to **Incomplete**.

You must replace the missing symbol to resolve the error. To replace the missing symbol, locate a saved version of the missing symbol and copy it to the exact location of the missing symbol. When the symbol is replaced, you can use the **Update from Source** command in the **Import Drawings Wizard**. For more information, refer to Import Drawings Wizard - Complete Import Map.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

38/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Source catalog path**

Displays the catalog root path where your symbols are installed.

**Symbols**

Displays an alphabetical list of any missing symbols.

**Import Drawings Wizard - Complete Import Map**

Displays the import map and allows you to define how data from the source plant is to be mapped into data in the target plant.

Smart P&ID allows you to customize a plant in various ways. You can add new properties, select lists and select list values with the Data Dictionary Manager. You can also add new catalog items (symbols) with the Catalog Manager. Because you can customize different plants in different ways, you must be able to define how to map the data before you can import drawings from one plant to another. The import map provides the solution to this problem.

The Import Drawings wizard supports two different approaches to mapping. They are Just-In-Time Mapping and Proactive Mapping. Each of these approaches is valuable in different contexts. The approach you choose to adopt will depend on your needs and your own personal preferences.

With the just-in-time approach, you only define the mapping for the minimum number of items that are required to import the selected drawings. The software automatically identifies all of the properties, select lists and symbols that are used by the selected drawings. The filter commands (**Show in Use** and **Show** **Incomplete**) are turned on to help you to focus on the items that remain to be mapped before the drawings can be imported. The just-in-time approach is the default approach to mapping.

With the proactive approach, you can define a complete mapping of all select list values, symbols, and so forth. After a complete map is created, drawings can be imported at any time without any mapping activity https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

39/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

required at all. The filter commands (**Show in Use** and **Show Incomplete**) can be turned off to allow the full map to be viewed. The **Update from Source** command can be used to fully populate the import map. The **Auto Complete** command can be used along with interactive mapping to complete the map. The proactive approach is an alternative approach to mapping.

All of the import map files for a plant are saved in the import map folder defined using Options Manager.

This folder is normally setup on a server that is accessible to all client computers. One import map file is created for each source plant from which drawings are imported. The wizard automatically opens the import map file for the selected source plant. If you have imported drawings from a different source plant, you can copy that import map file using the **Open** command. The **Save** command always saves the current import map file to the standard name in the standard location.

The import map is displayed in a familiar Explorer view with a Tree view on the left and a list view on the right. You can select the nodes of the Tree view and see the related data in the list view. The **Map Status** column in the list view can have a value of **Complete** or **Incomplete**. A value of **Complete** indicates this item and all of the items below it have been mapped. A value of **Incomplete** indicates this value is not mapped or some value below it has not been mapped. You must expand the Tree view to find the item that needs to be mapped. When you select the top-most node in the Tree view and the **Map Status** field displays **Complete** for all three of its children, then you know that the import map is complete.

You must have the same size symbols available when importing. Imported parametric symbols will use existing parametric parameters.

**New**

Creates a new import map file. If there are any unsaved changes in the current map file, you are prompted to save those changes if needed. The new map file is automatically updated with existing values that are in use by the selected drawing.

**Open**

Opens a new import map file. If there are any unsaved changes in the current map file, you are prompted to save those changes if needed. The import map file is validated against both the source and target plants.

Map entries for items that do not exist in the current source and target plants are deleted. The map is automatically updated with the existing values in use by the selected drawings.

**Save**

Writes the current import map file to the disk using the standard naming convention.

**Show in Use**

If selected, this command filters the display to show only the items being used by the selected drawing. By default, this option is selected. If not selected, the display is based on all items in the map.

**Show Incomplete**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

40/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If selected, this command filters the display to show only the items displaying an incomplete map status. By default, this option is selected. If not selected, all items display.

**Update from Source**

Reads data from the source plant and then populates the import map file. The import map is updated using the source plant data dictionary and catalog definitions. If you have the top node in the **Tree** selected, a complete update is performed. If any lower level node in the **Tree** is selected, a partial update is performed.

This option fills in the source value for each created map object and automatically completes the mapping process by filling in the target value for certain objects. Properties in the source plant that match with identically named properties in the target plant are automatically mapped. Select list values and symbols are not automatically mapped. If you are doing a partial update (a lower level node in the **Tree** view is selected when using this command), select lists should be updated before item types or symbols. This will help to create the proper relationships between the items.

**Auto Complete**

Automatically maps source objects to the corresponding target objects where possible. If the target value is already defined, the target value is not changed. If you have the top node in the Tree selected, a full operation is performed. If any lower level node in the Tree is selected, a partial operation is performed.

When applied to properties, the target property name and data type must match the source for it to be automatically mapped. When applied to select list values, you can use the** Select List Options** dialog to match by text, match by index or match by text and index. When applied to symbols, the item type and the mapped type property must match for the symbol to be automatically mapped.

Piping components, instruments, nozzles, and OPCs can contain connect points. For symbols that contain connect points, the number and type of connect points in the target symbol must match those of the source symbol. For labels, the Label Type and the Labeled Item Type properties must match the values of the source symbol. If a single symbol is found in the target catalog that matches the source properties, it is used. If multiple matching symbols are found, and one of those has the same name as the source symbol, then it is used. Mapping of symbols depends on the catalog index.

Interactive mapping of select lists is not supported. Mapping of select lists is always done through **Auto** **Complete** and is always driven by the mapping of the attributes that use them. To map a select list that is not in-use, you must first map an attribute that references it. Select Piping Component under Item Type Maps and invoke the **Update from Source** command. This brings in all of the attributes for Piping Component and internally calls **Auto Complete**. All of the attributes are mapped and the select lists that are referenced by those attributes are also mapped. Now, you can select **Action** under **Select List Maps** and run **Auto Complete**. This will complete the mapping of the select list values.

**Clean Up Map File**

Cleans up the map file by removing items in the map file that have no relationship with the current import.

All items on drawings to be imported must be mapped. If you have the top node in the tree view selected, a https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

41/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

full operation is performed. If any lower level node in the tree view is selected, a partial operation is performed.

**Update Catalog Index**

Updates the catalog index to include the latest information about all symbols in the target catalog. The mapping of symbols depends on the catalog index. The catalog index should be updated after any changes are made to the symbols in the catalog. The catalog index is saved in the file named CatalogIndex.xml in the top level folder of the catalog.

**Import Drawings Wizard - Select List Options Dialog**

Defines an option for resolving select list matching between the source and target plant. This dialog displays when you select **Auto Complete**

on the **Complete Import Map** wizard page.

**Match index**

Matches index, or number, associated with each select list item. For example, you would use this option if your source plant contains English text values and the target plant contains German values. The values would be assigned according to the select list index (its numeric value).

**Match text**

Matches the text, or string, associated with each select list item. For example, use this option if you have added entries to your select list. This option matches the text values and ignores the numeric values.

**Match text and index**

Matches the index and text associated with each select list item.

**Map Source and Target Symbols**

1. From the **Complete Import Map** wizard page, in the **Import Map File** pane, expand **Symbol Maps** and select the desired symbol class.
2. In the **Target Symbol** column, select the ellipsis button

.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

42/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. On the **Target Symbols** dialog, select the symbol you would like to use.

For details of how the software determines which symbols are available as target symbols, see

Criteria for Available Target Symbols.

1. Select **OK**.

**Target Symbols Dialog**

The **Target Symbols** dialog allows you to select a target symbol file for mapping with a source symbol where the software cannot find a suitable target symbol automatically.

**Available symbols**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

43/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Displays a list of symbols that meet the criteria determined by the software for mapping to the source symbol. For details of how the software determines which symbols are available as target symbols, see

Criteria for Available Target Symbols.

**Criteria for Available Target Symbols**

The software searches for available symbols in the target catalog. A source symbol is available for mapping to the target if the Item Type and the ‘Type’ property are the same.

For **instrument symbols**, the software applies the following criteria to determine whether symbols are able to be mapped:

Both the source and target instruments must be inline or offline. An inline instrument cannot be replaced by an offline instrument, nor can an offline instrument be replaced by an inline instrument.

If both the source and target instruments are inline instruments, they must belong to the same instrument class. Examples of inline instrument classes are ‘control valves and regulators’, ‘other inline instruments’.

In addition, depending on the type of symbol, the software will match the source and target symbols using the following criteria:

**Connect points**

Piping components, instruments, nozzles and OPCs can contain connect points. For symbols that contain connect points, the number and type of connect points in the target symbol must match those of the source symbol.

The software can map source and target *offline instruments* even if they have a different number of connect points.

**Label symbol properties**

A label symbol in the target catalog is considered to be available for mapping if the **Label Type** and the **Labeled Item Type** properties match those of the source symbol.

**Gap symbols**

Any symbol defined as a gap symbol in the target may match any gap symbol in the source.

Using the above criteria, the software determines whether a target symbol that can be mapped exists. If there is exactly one available symbol, the source symbol is mapped to that one target symbol. If there are multiple available symbols and one of them has the same name as the source symbol, the source symbol is mapped to that target symbol. In all other cases, the software leaves the source symbol unmapped.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

44/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Drawings Wizard - Options**

Allows you to select a template size for your drawing. You can also define a program that you want to use during the transformation process. This program could contain any special instructions you want applied during the import. A transformation program is delivered with the software. You can use the delivered program as an example to create your own transformation programs.

**Use source templates**

Select to use the template associated with each drawing that you import from the source plant.

**Target template**

Allows you to select the template that defines the sheet size for all drawings imported into the target plant.

This option is not available if you select **Use source templates**.

**Apply default formats**

When selected, the software reformats property values from the source database using the default format for each property in the target database. This applies to all properties but is most important for Unit of Measure (UOM) properties such as temperatures and pressures. If a drawing is being imported from a source plant that shares the same locale as the target plant, typically this option should be turned off to prevent any loss of formatting during the import operation. For example, if pressure values are expressed in several different units of measure for different properties, these would all be imported exactly as they are in the source database. If a drawing is being imported from a source plant in one locale into a target plant in a different locale, typically this option should be turned on. This ensures that locale-dependent formatting is applied to all values. For example, if importing from a plant where the decimal symbol is a comma (,) to a plant where the decimal symbol is a period (.), property values should be reformatted using the default formats.

**Import revisions**

Select to include with the import all drawing revisions that were made in the source plant.

**Use source drawing name and number**

Select to keep the original name and number of the drawings without the addition of any prefix. Clear to specify new drawing names and numbers. When cleared, the software adds a prefix to the drawing name indicating the name of the source plant.

**Do not recreate drawings**

Select to skip re-creation of the graphical drawings when importing the drawing data. This improves performance when you are importing a large number of drawings. If you select this option, you are prompted to re-create a drawing when you open it.

**Transformation program**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

45/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

This option displays the name of the transformation program defined by the Options Manager setting **Import Transformation Program**. You can copy the delivered code and then create your own customized transformation program. Then, you can use this field to enter the name of your transformation program. The delivered import transformation program is CopyTransformation.Import. You are not required to use a transformation program. For more information about creating a transformation program, see Customizing the Sample Projects in the *Smart P&ID Programmer’s Guide*.

**Custom Options**

If a *transformation program* is defined, this command displays the **Transformation Programs** dialog. It is used to define options for modifying property values during the import process. The options that appear on the **Transformation Programs** dialog depend on the transformation program defined by the Options Manager setting **Import Transformation Program**. You can copy the delivered code and then create your own customized transformation program. The delivered transformation program used for importing drawings is CopyTransformation.Import.

**Transformation Programs Dialog**

This dialog is used to define options for modifying property values during the import process. If the delivered import transformation program (CopyTransformation.Import) is used, the options described below are available:

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

46/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Sequence numbers**

**Generate new**

Selecting the option causes existing tag sequence numbers to be set to null for any item that has the property **TagSequenceNo**. The null sequence number triggers the creation of new sequence numbers during normal item tag validation.

**Add value to the beginning of all sequence numbers**

When you select this option, you can use the box to type the values you want to display at the beginning of all your sequence numbers.

**Keep existing if unique**

If the sequence number for an imported item is unique, it will be left as it was, but if the software detects a duplicate item tag in the plant for an item type where duplicate item tags are not allowed, the tag sequence number will be incremented to the next available value.

**Add value to the beginning of the sequence numbers** and **Keep existing if unique** options do not apply to OPCs (Off-Page Connectors). When you import or copy a drawing, each OPC is assigned a new unique tag number, and the **OPC Tag** number gets incremented to the next available value.

Duplicate item tags are allowed in the plant for the following item types only: pipe runs, duct runs, and signal runs of Plant Item Type **Pipe Runs**.

When importing a drawing that has a loop associated with one or more instruments, the sequence number that the newly-created loop receives is in accordance with the selected option; however, the instrument / loop associations will correspond to those in the source drawing and the instruments will retain the original values for their **Tag Seq No** and **Item Tag** properties. This may result in a mismatch between the loop and instrument sequence numbers. To resolve this situation, you must update the related instrument tags on the **Update Associated Instruments with Loop Properties** dialog box in Smart P&ID.

Item tag values follow the behavior set by the *ItemTag.dll* file. For more details, see Default Item Tag Configurations.

**Clear piping material classification**

Select to remove any defined piping materials class.

**Clear process data**

Select to remove any values in the **Process** category.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

47/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drawing and plant item associations**

Allows you to specify the behavior of the plant item associations when importing the drawing, determined by the combination of selections that you make under the **Associate drawings** and **Associate plant items** sections.

**Associate drawings**

**By current plant group**

When performing the import, the software re- associates all drawings in the selected source plant group with the target plant group selected when Import Drawing was initiated.

**By mapping (multiple plant groups)**

When performing the import, the software re-associates the drawings in each plant group with the target plant groups chosen in the **Mapping** dialog. For the current source and target plant groups, the mapping overrides the selection made at the initiation of Import Drawing.

**Associate plant items**

**By drawing plant group associations**

All plant items in each plant group, regardless of their drawing associations in the source, are re-associated with the target plant group specified for the drawing.

**By mapping**

All plant items in each plant group, regardless of their drawing associations in the source, are re-associated according to the definitions made in the **Mapping** dialog.

**Re-associate items depending on original associations**

Those plant items that belong to the plant group of the drawing itself follow the mapping for the drawing.

Other plant items follow the plant item mapping.

The following table describes the resulting behavior for each of the settings: **Associate drawings**

**Associate plant items**

**Resulting behavior for the imported drawing**

By current plant group

By drawing plant group

The drawing and all of its plant items are re-

associations

associated with the current plant group. For details,

see Import Options - Example 1.

By current plant group

By mapping

The drawing is re-associated with the current plant

group and the plant items are re-associated according

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

48/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

to the mapping. For details, see Import Options -

Example 2.

By current plant group

Depending on original

The drawing and those plant items that were

associations

associated with the same plant group as the drawing

are re-associated with the current plant group. Other

plant items follow the plant item mapping. For details,

see Import Options - Example 3.

By mapping (multiple

By drawing plant group

The drawing is re-associated according to the

plant groups)

associations

mapping. All plant items in a particular drawing are re-

associated with the target plant group specified for

that drawing in the mapping. For details, see Import

Options - Example 4.

By mapping (multiple

By mapping

The drawing and the plant items follow the mapping.

plant groups)

For details, see Import Options - Example 5.

By mapping (multiple

Depending on original

The drawing and those plant items that were

plant groups)

associations

associated with the same plant group as the drawing

follow the mapping for the drawing. Other plant items

follow the plant item mapping. Note that the end result

is the same as for the previous combination of

settings. For details, see Import Options - Example 6.

**‘In use’ plant group data only**

Filters the plant groups available for mapping so that only those plant groups that have associated plant items and drawings will be available on the **Mapping** dialog.

**Mapping**

Opens the **Mapping** dialog to allow you to define the associations between the target and source plant groups for the drawings and / or the plant items depending on the settings you choose. This button is only enabled when you make appropriate selections under **Import options**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

49/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 1**

**Selected Options**

**Associate drawings**: By current plant group

**Associate plant items**: By drawing plant group associations **Import Results**

The drawing and all of its plant items are re-associated with the current plant group.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

50/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 2**

**Selected Options**

**Associate drawings**: By current plant group

**Associate plant items**: By mapping

**Mapping**

**Source Plant Group**

**Target Plant Group**

P1\U1

P2\U4

P1\U2

P2\U2

P1\U3

P2\Unit3

**Import Results**

The drawing is re-associated with the current plant group and the plant items are re-associated according to the mapping.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

51/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 3**

**Selected Options**

**Associate drawings**: By current plant group

**Associate plant items**: Depending on original associations **Mapping**

**Source Plant Group**

**Target Plant Group**

P1\U1

P2\U4

P1\U2

P2\U2

P1\U3

P2\Unit3

**Import Results**

The drawing and those plant items that were associated with the same plant group as the drawing are re-associated with the current plant group. Other plant items follow the plant item mapping.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

52/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 4**

**Selected Options**

**Associate drawings**: By mapping (multiple plant groups) **Associate plant items**: By drawing plant group associations https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

53/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Mapping**

**Source Plant Group**

**Target Plant Group**

**P1\U1**

**P2\U4**

**P1\U2**

**P2\U2**

**P1\U3**

**P2\Unit3**

**Import Results**

The drawing is re-associated according to the mapping. All plant items in a particular drawing are re-associated with the target plant group specified for that drawing in the mapping.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

54/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 5**

**Selected Options**

**Associate drawings**: By mapping (multiple plant groups) **Associate plant items**: By mapping

**Mapping**

**Source Plant Group**

**Target Plant Group**

**P1\U1**

**P2\U4**

**P1\U2**

**P2\U2**

**P1\U3**

**P2\Unit3**

**Import Results**

The drawing and the plant items follow the mapping.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

55/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Import Options - Example 6**

**Selected Options**

**Associate drawings**: By mapping (multiple plant groups) **Associate plant items**: Depending on original associations https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

56/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Mapping**

**Source Plant Group**

**Target Plant Group**

**P1\U1**

**P2\U4**

**P1\U2**

**P2\U2**

**P1\U3**

**P2\Unit3**

**Import Results**

The drawing and those plant items that were associated with the same plant group as the drawing follow the mapping for the drawing. Other plant items follow the plant item mapping.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

57/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Mapping Dialog**

Allows you to define mapping between source and target plant groups when importing drawings. Depending on the options that you select on the **Transformation Programs** dialog, the mapping can apply to drawings, plant items, or both.

The following screen capture shows an example of mapping between two plants.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

58/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Source**

Shows the source plant hierarchy.

**Target**

Shows the hierarchy for the target plant. From this window, you can select a plant group at any level for mapping, but note that if there is a restriction on associating a drawing with a particular plant group, an error message will appear.

**Map**

Copies the selected plant group item in the target plant hierarchy to the selected **Target Path** row. In this way the mapping is defined to the corresponding plant group in the **Source Path** row.

**Remove Mapping**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

59/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Removes the selected target plant group item from the Plant Group mapping, allowing you to redefine the mapping target for the specified source.

**Plant group mapping**

Displays the mapping assignments and paths between the source and target plant groups.

**Source Path**

Shows the paths of all the plant groups in the plant. If you selected the **‘In use’ plant group data only** check box on the **Transformation Programs** dialog, only the paths of those plant groups that have associated drawings or plant items appear.

**Target Path**

Displays the paths of the plant groups that you have chosen as the target. All of the rows must contain values.

You can assign plant groups at any level of the hierarchy as the target; for example, an Area.

If you use the mapping to associate both the drawing and the plant items to the target plant group, and you do not have appropriate permissions for the drawing association, a message appears and only the plant items are re-associated according to the mapping. In this case, the software associates the drawing with the current plant group.

**Define Plant Group Mapping for Import**

1. On the **Transformation Programs** dialog, under **Drawing and plant item associations**, select the settings you want.

The software responds according to the combination of options that you select under the **Associate drawings** and **Associate plant items** group boxes. For details of the options and

examples of the resulting behavior for each of the combinations, see Transformation Programs Dialog.

1. If desired, select **‘In use’ plant group data only** to filter the plant groups available for mapping so that only those plant groups that have associated plant items and drawings are available in the source path on the **Mapping** dialog.
2. Select **Mapping**.
3. On the **Mapping** dialog, under the **Source** tree view, navigate to the source plant group that you want to map.

As you select a source plant item in the tree that can be mapped, the corresponding row in the **Plant group mapping** window is highlighted.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

60/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Under the **Target** tree view, navigate to the target plant group that you want to map.

You can assign plant groups at any level of the hierarchy as the target; for example, an Area.

1. In the **Plant group mapping** window, select the desired row under the **Target Path** column beside the source plant group that you want to map to, and do one of the following: Select **Map**.

Drag the plant group from the target hierarchy to the desired row.

You must map ALL of the rows that appear in the source path to a target path.

You can clear the mapping for a particular row by selecting that row and selecting **Remove Mapping**.

**Import Drawings Wizard - Summary**

Displays a summary of information about the imported drawing(s). You must select **Finish** to complete the import process.

**Global Validation Command (File Menu)**

Opens the **Global Validation** dialog, from which you can implement changes to the plant’s item tag configuration, 3D pipe specifications, or insulation specifications for the selected drawings.

**Global Validation Dialog**

Allows you to implement changes to the plant’s item tag configuration, 3D pipe specifications, or insulation specifications for the selected drawings. You can open this dialog by selecting one or more drawings and then selecting **File** > **Global Validation**.

**Item types**

Allows you to select the following item types for validation in the selected drawings: **Equipment**

**Pipe run**

**Instrument**

**Instrument loop**

**Piping component**

**Room**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

61/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Duct run**

**Ducting component**

**Validation programs**

Allows you to select the following programs for validation in the selected drawings: **Item tag validation**

Validates changes in item tag configuration. These changes may be the result of renaming the plant hierarchy item name where this name is a part of the item tag.

**Pipe spec validation**

Validates pipe spec data that was changed in Smart 3D or PDS 3D databases. Not available in this version; however, you can run this option using the Global Validation Utility.

**Insulation spec validation**

Validates insulation spec data that was changed in Insulation Manager. Not available in this version; however, you can run this option using the Global Validation Utility.

**Options**

Allows you to include items in either or both of the stockpiles for validation in the selected drawings: **Include drawing stockpile**

**Include plant stockpile**

**Run**

Runs the validation for the selected drawings.

**Upgrade Drawings Command (File Menu)**

This command is currently not in use.

**Copy Command (Edit Menu)**

Copies the selected drawing(s) in Drawing Manager.

To avoid database lockup during pasting of a group of drawings, ensure that the workstation performing the operation has at least 4 GB of memory. Also ensure that the size of the redo log files of the database instance is at least 500 MB.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

62/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Copy a Drawing**

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to copy drawings.

1. In the **Tree** view, select the node in which the drawing resides.
2. In the **List** view, select the drawing that you want to copy. Use the SHIFT or CTRL key to select more than one drawing.
3. Select **Copy** on the main toolbar.

You can hold CTRL, select a drawing, and drag it to a new location to make a copy. You can also drag it to the current list view to make a copy. When copying a drawing, the software displays the **Transformation Programs** dialog. If you drag and drop the drawing to another unit, you will need to select the contents of the drawing using Smart P&ID and set the **Plant Group Name** value in the **Properties** window.

A multi-rep model item is created at the target only once if the drawings that contain all the representations for it are selected for copy in one session. If the drawings are copied in separate sessions, the model item is re-created at the target for that session.

Paired OPCs in a drawing that are not copied (for example, not in a Select Set) are placed in the plant stockpile. Paired OPCs in a copied drawing have their relationships maintained by the copy. Paired OPCs are not moved from the plant stockpile to a drawing by a subsequent copy session.

A plant item group is created at the target only once if the drawings that contain all of its members are selected for copy in one session. If the member drawings are copied in separate sessions, the plant item group is re-created at the target for each session.

When you copy a drawing that contains ABE items, the **Source Tag** property will not be copied.

**Move a Drawing**

1. In the Tree view, select the node in which the drawing resides.
2. In the List view, select the drawing that you want to move.
3. Drag and drop the selected drawing to the new location.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to copy drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

63/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If you move the drawing to another plant group, the associated plant groups for the items in the drawing are not automatically updated to reflect the new plant group. You will have to update the plant groups manually from within Smart P&ID.

**Paste Command (Edit Menu)**

Pastes the selected drawing(s) in Drawing Manager. When implementing this command, the software displays the **Transformation Programs** dialog.

To avoid database lockup during pasting of a group of drawings, ensure that the workstation performing the operation has at least 4 GB of memory. Also ensure that the size of the redo log files of the database instance is at least 500 MB.

The options that appear on the **Transformation Programs** dialog depend on the transformation program defined by the Options Manager setting **Copy Transformation Program**. You can copy the delivered code and then create your own customized transformation program. The delivered transformation program used for copying drawings is CopyTransformation.Transform.

You can change the name of a pasted drawing by selecting the drawing and then select **Edit** > **Properties**. On the **Properties** dialog, in the **Name** field, enter the new name.

**Transformation Programs Dialog**

This dialog is used to define options for modifying property values during the copy process. If the delivered copy transformation program (CopyTransformation.Transform) is used, the options described below are available:

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

64/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Sequence numbers**

**Generate new**

Selecting the option causes existing tag sequence numbers to be set to null for any item that has the property **TagSequenceNo**. The null sequence number triggers the creation of new sequence numbers during normal item tag validation.

**Add value to the beginning of all sequence numbers**

When you select this option, you can use the box to type the values you want to display at the beginning of all your sequence numbers.

**Keep existing if unique**

If the item tag for a copied item is unique, it will be left as it was, but if the software detects a duplicate item tag in the plant for an item type where duplicate item tags are not allowed, the tag sequence number will be incremented to the next available value.

Duplicate item tags are allowed in the plant for the following item types only: pipe runs, duct runs, and signal runs of Plant Item Type **Pipe Runs**.

When copying a drawing that has a loop associated with one or more instruments, the sequence number that the newly-created loop receives is in accordance with the selected option; however, the instrument / loop associations will correspond to those in the source drawing and the instruments will retain the original values for their **Tag Seq No** and **Item Tag** properties. This may result in a mismatch between the loop and instrument sequence numbers. To resolve this situation, you must update the https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

65/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

related instrument tags on the **Update Associated Instruments with Loop Properties** dialog box in Smart P&ID.

Item tag values follow the behavior set by the *ItemTag.dll* file. For more details, see Default Item Tag Configurations.

**Clear piping material classification**

Select to remove any defined piping materials class.

**Clear process data**

Select to remove any values in the **Process** category.

**Plant item associations**

Allows you to specify the behavior of the plant item associations when copying the drawing.

**Re-associate all plant items with the target**

All plant items, regardless of their plant group associations in the source, are associated with the target plant group of the copied drawing.

**Retain existing plant item associations**

All plant items retain the same plant group associations that they had in the source. No changes are made to the associations.

**Re-associate items depending on original associations**

Those plant items that belong to the plant group of the drawing itself in the source are reassigned to the target plant group. Those plant items that were assigned to a different plant group from that of the drawing source plant group retain their existing override associations.

**Paste a Drawing**

1. In the **Tree** view, select the node where the copy of the drawing will reside.
2. In the **List** view, select the location where you want to paste the copy of the drawing.
3. Select **Paste** on the main toolbar.

*The software displays the **Transformation Programs** dialog.*

The options that appear on the **Transformation Programs** dialog depend on the transformation program defined by the Options Manager setting **Copy Transformation Program**. You can copy the delivered code and then create your own customized transformation program. The delivered transformation program used for copying drawings is CopyTransformation.Transform.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

66/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select one of the following options:

**Generate new sequence numbers** option if you would like new sequence numbers to be created. Selecting the option causes existing tag sequence numbers to be set to null for any item that has the property **TagSequenceNo**. The null sequence number triggers the creation of new sequence numbers during normal item tag validation.

**Add value to the beginning of all sequence numbers** to define a string to be added at the beginning of the tag sequence numbers in the copied items. Select in the provided field and enter the values you want to display at the beginning of all your sequence numbers.

**Keep existing if unique** to leave the same item tag for the copied item. If the item tag for the copied item is unique, it will be left as it was, but if the software detects a duplicate item tag in the plant for an item type where duplicate item tags are not allowed, the tag sequence number will be incremented to the next available value.

1. Select the **Clear piping material classification** check box to remove any defined piping materials class.
2. Select the **Clear process data** check box to remove any values in the **Process** category.
3. Under **Plant item associations**, select the required option.
4. Select **OK**.

*The software displays the **Paste Drawings** dialog.*

1. When the processes are complete, select **View Log** to view the report or select **Close** to dismiss the **Paste Drawings** dialog.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to paste drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

67/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

For more information about creating a transformation program, see *Customizing the Sample Projects* in the Smart P&ID * Programmer’s Guide*.

**Delete Command (Edit Menu)**

Allows you to delete drawings from the **List** view and from the plant structure. Because a new version of the drawing is automatically created when you delete a drawing, you can recover the drawing after you have deleted it, but there are many drawing recovery Recovering Drawings.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to delete drawings.

**Deleting Drawings Dialog Box**

Opens when you choose **Yes** on the confirmation message that appears when you select a drawing and select **Edit** > **Delete** on the main menu bar. This dialog displays the progress of drawing deletions currently underway.

**Drawings**

Lists the drawings that are being deleted, and shows the status of that operation.

**View Log**

Opens the log file, DeleteDrawing.log, which is created when you delete a drawing.

**Delete a Drawing**

1. In the **List** view, select the drawing that you want to delete.
2. Select **Delete** .
3. To confirm the drawing deletion, select **Yes** on the message box.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

68/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If you have not saved a version of the drawing, you will not be able to retrieve the drawing after deleting it.

1. Select **View Log** on the **Deleting Drawings** dialog to review notes from the drawing deletion process.

You must have the appropriate permissions, specified in Smart Engineering Manager, in order to delete drawings.

If you have a saved version of a deleted drawing, you can retrieve the drawing as it was when you saved it. For more information, see Recover a Version of a Deleted Drawing.

If a plant group has no drawings or plant items belonging to it, you can delete that hierarchy item in Smart Engineering Manager. Keep in mind, though, that if you have associated a plant item with a hierarchy item by using the **Properties** window in Smart P&ID, then even though it can look as if no drawings are associated with that plant group, you cannot delete that hierarchy item in Smart Engineering Manager.

You can also delete saved versions of a drawing, without deleting the drawing itself. For more

information, see Show the Version History of a Drawing.

**Unlock Plant After Group Rename Command (Tools Menu)**

If a plant group name is used for validation or is part of an item tag name, and that plant group is renamed in Smart Engineering Manager, it will affect the drawing. This command can be run to unlock the drawings so that the properties containing the new plant group name are updated.

This command operates on a per-user basis, provided that the particular user has Full Control access to Options Manager for the selected plant.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

69/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Working with Projects**

Plants, after designed and built, are often modified throughout their lifecycles. During these modifications, information assets of the “As-Built” state must be maintained. Using projects in your plant allows you to maintain this information while allowing multiple projects, possibly overlapping and running concurrently, to be designed, approved, constructed, and/or canceled.

Before creating a project in a plant, you must enable that plant for projects. When enabled for projects, the plant structure becomes the Plant, sometimes referred to as the Master or As-Built plant. In a Task/Master scenario, the Plant is the Master and the projects are the individual Tasks.

**Database Configuration**

To allow work on projects to proceed without affecting the Plant, separate schemas are created for each project. In other words, all projects must be located in the same database instance as the Plant, with each project contained within a separate schema (separate database user names).

The Plant shares reference data with its projects. Changes to the reference data can be made only in the Plant. In other words, you can use Catalog Manager, Data Dictionary Manager, Filter Manager, and Format Manager in a project, but you have read-only permissions and are not allowed to modify any of the data from within these managers.

**Fetching and Checking Out Drawings**

After projects are enabled in Smart Engineering Manager, the As-Built can no longer create drawings; drawings are created inside projects. However, any drawings that might have existed in the plant before projects were enabled remain in the As-Built. All drawing versions in the As-Built are read-only drawings when projects are enabled, but these drawings can still be deleted in the As-Built, unless the drawing is either fetched or checked out to a project. If the plant is registered in SmartPlant Foundation, drawings can be created and edited in the As-Built, except for drawings that are checked out to a project.

**Projects and Claiming**

One of the main capabilities associated with using projects in an integrated environment is the ability for a project to *claim* a drawing object. When a project claims an object, the project controls modifications to that object. A project cannot modify objects it has not claimed. All the modifications and claiming of objects is carried out in the design software, but the claim states of objects inside drawings do have ramifications for drawing manipulation and for completing projects. You do not need to check out a drawing to claim items on it; you can claim items on a fetched drawing.

Projects claim objects in either Exclusive (default) or Shared mode. If you plan to use the project in an integrated environment, Exclusive mode is mandatory. Use the **Settings** view in Options Manager to set the Claim Mode before creating a project.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

70/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When publishing from a project, an instruction container, which contains all the claimed objects, is created within the tombstone file.

You can change the Claim Mode to Shared at any time. However, you can change the mode to Exclusive only when there are no claims in any project in the Plant.

**Using Workshare with Projects**

Workshare functions the same whether using projects or not. The only difference is that when using projects, only a project can function as a Workshare host. The Plant cannot be a host or a satellite when projects are enabled.

**Working with Off-Site Projects**

To implement off-site projects in Smart P&ID, you use standalone workshare functionality. See the following help topics:

Using Workshare

Using Workshare with Projects

Configuring Workshare

Managing a Workshare Collaboration

Publishing and Assigning Ownership

Getting Latest Versions of Drawings

Synchronizing Reference Data

Synchronizing Shared Items

**Working with Drawings within a Project**

After enabling and creating projects in Smart Engineering Manager for Smart P&ID, use Drawing Manager to manipulate the drawings. Actual design work is still accomplished in Smart P&ID; however, managing and setting out that work is largely controlled from the Drawing Manager interface. Only the project can use the commands on the **Project** menu in Drawing Manager to fetch, check in, and check out drawings.

After projects are enabled in Smart Engineering Manager, the As-Built can no longer create drawings; drawings are created inside projects. However, any drawings that might have existed in the plant before projects were enabled remain in the As-Built. All drawing versions in the As-Built are read-only drawings when projects are enabled, but these drawings can still be deleted in the As-Built, unless the drawing is either fetched or checked out to a project. If the plant is registered in SmartPlant Foundation, drawings can be created and edited in the As-Built, except for drawings that are checked out to a project.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

71/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When you are using projects inside Smart P&ID, remember that the reference data belongs to the Plant and is used by projects of the As-Built. You cannot change reference data, such as table layouts or formats or rules, at the project level.

**Claiming**

Claiming Items on a drawing is one of the main features of using projects in an integrated environment.

When a project claims an object on a drawing, the project controls modifications to that object. A project cannot modify objects that it has not claimed.

Projects claim objects in either Exclusive (default) or Shared claim mode. If you plan to use the project in an integrated environment, Exclusive mode is mandatory. Use the **Settings** view in Options Manager to set the **Claim Mode** value before creating a project.

You can change the claim mode to Shared at any time. However, you can change the claim mode to Exclusive only when there are no claims in any project in the Plant.

All the modifications and claiming of objects is carried out in the design software, but the claim states of objects inside drawings do have ramifications for drawing manipulation and for completing projects. You do not need to check out a drawing to claim items on it; you can claim items on a fetched drawing.

**Smart P&ID Project Statuses**

You can review the status of the active project using the **Project Status** command in Drawing Manager. The **Project Status** dialog shows the status of the active project and tells you where the project is in its lifecycle.

See Modify Project Status in Smart P&ID.

A **project** status shows the stage of the project life-cycle. Possible project statuses are: **Active**

The initial state of a project right after its creation.

**Completed**

Indicates that all the work on the project items has been completed and that the items are ready to be merged back into the As-Built. You cannot claim items in a project whose status has been set to **Completed** or **Merged**.

In a project, when searching for completed items in the **Project Management** window, it is possible to select the related items which have not been completed yet and to change their status to **Completed**.

**Merged**

Indicates that all the project items have been merged back into the As-Built.

**Canceled**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

72/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Indicates that the project has been canceled and it can be deleted. Selecting this project status changes the status of the items in the project from **Claimed** to **Scoped**.

**Project Status Command (Project Menu)**

Opens the **Project Status** dialog, which allows you to update, modify, and verify the status of your project with respect to the Plant and/or SmartPlant Foundation. Possible statuses include **Active**, **Completed**, **Merged**, and **Canceled**. This command is not available if you are currently in the Plant; it is only available if your current database is a project database.

After a project enters the **Completed** state, all the commands are disabled and design work is no longer possible within that project. If you later determine that the project is really not done, use the **Return to** **Active** button on the **Project Status** dialog. This command resets the project status to **Active**, allowing work to continue in the project. This command is only enabled when the project is in the **Completed** state.

**Project Status Dialog**

Displays the current project status, both with respect to SmartPlant Foundation and the plant and allows you to update or modify those statuses. This dialog opens when you select **Project** > **Project Status** on the main menu bar.

A project can only be returned to an **Active** state from the **Completed** state. If a project has been set to **Merged** or **Canceled**, it cannot be changed back to **Active**. **Merged** and **Canceled** are permanent states.

**SmartPlant project status**

Displays information about the status of the active project with respect to SmartPlant Foundation. This area is not active if the plant is not registered with SmartPlant Foundation.

**Refresh Status**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

73/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Searches for and displays the status of this project in SmartPlant Foundation and updates this information in SmartPlant Foundation if appropriate. This button is not available if the plant is not registered with SmartPlant Foundation.

**Smart P&ID project status**

Indicates whether the project is **Active**, **Completed**, **Merged**, or **Canceled**. If your project status is** Merged** or **Canceled**, then no further actions are available on this dialog.

**Return to Active**

Returns the project status to **Active**. This command is available only when the initial project status is **Completed** and the **SmartPlant project status**, if applicable, is **Active**.

**Complete Project**

Sets the project status to **Completed**. This command is available only when the initial project status and the **SmartPlant project status** are both **Active**. When you select **Complete Project**, a confirmation message appears.

**Merge Project**

Sets the project status to **Merged**. This command is available only when the initial project status and the **SmartPlant project status** are both **Completed**. When you select **Merge Project**, a confirmation message appears.

**Cancel Project**

Clears all claims on all objects and sets the project status to **Canceled**. This command is available only when the initial project status is **Active**. If the Plant is not registered, then the project is simply canceled out of Drawing Manager.

**Modify Project Status in Smart P&ID**

1. In Drawing Manager, open the project for which you want to view the status.
2. Select **Project** > **Project Status**.
3. In the **Smart P&ID project status** area, ascertain the current status of your project with respect to the plant.

A check mark denotes the current status. Possible statuses include **Active**, **Completed**, **Merged**, and **Canceled**.

1. Do any of the following to change the status of your project: To change an active project to completed, select **Complete Project**. This command is available only when the initial project status is **Active**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

74/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When you change the project status to **Completed**, all the drawings in the project are verified for checking into the plant. You can verify each drawing separately if you want to. See Verify a

Drawing for Checkin.

To change a completed project back to active, select **Return to Active**. This command is available only when the initial project status is **Completed**.

To merge a completed project into the plant, select **Merge Project**. This command is available only when the initial project status is **Completed**.

To cancel an active project, select **Cancel Project**.

If the plant is registered, select **Refresh Status** on the **Project Status** dialog to update the **SmartPlant project status** display.

In SmartPlant Foundation, the **Complete Project**, **Return to Active**, and **Merge Project** options are not available unless the **SmartPlant project status** is also **Active**. The **Cancel Project** option is not available unless the **SmartPlant project status** is also **Canceled**.

**Fetching a Drawing to an Active Project**

Fetching a drawing from the Plant places a copy of the drawing in the project. Only one project at a time can check out a drawing, but numerous projects can *fetch* the same drawing.

Fetched drawings can have read-only or read/write permissions. If you want to save changes to a read/write fetched drawing into the Plant, you must check the drawing out first, apply your changes, and then check it back into the Plant.

If you are working with projects but are not connected to SmartPlant Foundation, all claims on items in that drawing are automatically released when you delete a fetched drawing from your project database.

A Workshare satellite can only fetch drawing versions from its own database by using the **Fetch** command in the **Version History** dialog. If you want a drawing version from another project or the Plant, it must be fetched into the host project and then the satellite can use the **Get Latest Version** commands on the **Workshare** menu.

**Fetch Command (Project Menu)**

Displays the **Fetch** dialog, which provides options for fetching a drawing version from the Plant or another project. You can fetch a drawing with read/write permissions or with read-only permissions.

The **Fetch** command is not available if you are currently working in the Plant. You cannot fetch a deleted drawing, but a deleted drawing can be retrieved if a version of it is saved, and then you can fetch it.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

75/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Fetch Dialog**

Displays the active Plant hierarchy and lists its drawings, allowing you to fetch a drawing from a specified database. This dialog appears when you select **Project** > **Fetch** or the **Fetch**  command.

**Open Database**

Opens the **Projects** dialog, which allows you to specify a different project or the Plant.

**Filter**

Opens the **Filter** dialog, which allows you to specify the drawings that are displayed in the **List** view.

**Cancel Filter**

Deactivates any ad hoc filter you have applied to the **List** view.

**Include Subnodes**

Displays all the drawings and node names that reside in the currently selected node.

**List**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

76/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Displays the **List** view. The **List** view displays only one property for each drawing. To specify which property displays, select **Customize View** . The first item in the **Selected Properties** list is the property that appears in the **List** view.

**Details**

Displays the **Detail** view, which contains all the properties specified in the **Selected Properties** list on the **Customize Current View** dialog. Using the **Detail** view allows you to view and sort drawings by several attributes.

**Customize View**

Opens the **Customize Current View** dialog, which allows you to specify the information about each drawing that is displayed in the **List** view.

**Options**

Displays options specific to this fetch operation.

**Create New Version**

Saves a new version of the drawing before overwriting the existing version. This option is not enabled if the current drawing is not already fetched or checked out to the project.

**Read-only**

Fetches a read-only version of the drawing so that your project can examine the drawing but not alter it.

**Comments**

Allows you to enter comments pertinent to this fetch operation.

**History**

Opens an abbreviated version of the **Version History** dialog, which allows you to choose a saved version of the drawing you select in the **Fetch** dialog **List** view.

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions, when you select the same drawing to fetch, the **OK** button on this dialog is not available.

**Projects Dialog**

Allows you to choose the Plant or a project that you want to fetch a drawing version from. You can fetch a version from a different project only if that project is part of the same plant in which you are working. This dialog opens when you select the **Open Database** button on the **Fetch** dialog toolbar.

**Available databases**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

77/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Lists the active Plant and the projects associated with it, other than the project in which you are currently working. Choosing from this list changes the plant hierarchy and the drawings displayed in the **Tree** and **List** views.

**Fetching Drawings Dialog**

Displays the progress of the version fetching operation currently under way. This dialog opens when you select **OK** on the **Fetch** dialog.

**Drawings**

Lists the drawings that are being fetched, and shows the status of that operation.

**View Log**

Opens the log file, Fetch.log, which is created when you fetch a drawing version.

**Fetch a Drawing**

1. Select **Fetch** .
2. On the **Fetch** dialog, select the pertinent node in the **Tree** view if it is not already selected.
3. In the **List** view, select the drawing that you want to fetch.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

78/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select **History** if you need to fetch a version of this drawing other than the current version.
2. On the **Version History** dialog, select the version that you want to fetch, and then select **OK**.
3. Select the **Read-only** option if you want to fetch a version of the drawing for review only.
4. (Optional) Enter appropriate comments in the **Comments** box.
5. Select **OK**. You can follow the progress of the fetch operation on the **Fetching Drawings** dialog.

Select **View Log** if you want to examine notes from the fetch operation.

If you want to fetch a drawing version from another project and not from the Plant, select **Open** **Database** on the **Fetch** dialog toolbar. On the **Projects** dialog, select the Plant or a project from the **Available databases** list, and then select **OK**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

79/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You can open a read-only version of the drawing for review by selecting **View**. For more information

about viewing drawing versions without fetching or checking them out, see Show the Version History

of a Drawing.

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions when you check the drawing out, the fetched version remains intact and only its status changes to checked-out. That is, you cannot replace the fetched version with the version in the Plant.

**Checking a Drawing Out to an Active Project**

Checking out a drawing places that drawing under the control of the project. No other project can check out the same drawing while your project has it checked out. The advantage of checking out rather than fetching a drawing is that only checked out drawings can have their changes reflected back in the Plant.

The software notifies you if you try to fetch a version of a drawing that you have already checked out.

When working with projects in an integrated environment, you must select **No** for the **Enable**

**“Keep Checked Out” on Check-In** option in Options Manager.

After you check out a drawing to a project, the drawing will be read only in the As-Built and the following actions are not allowed:

Modifying drawing properties

Modifying the drawing or any drawing items or properties

Deleting the drawing

Updating the drawing using Drawing Manager

Updating the drawing using automation

You cannot check out a drawing to a project if it is open in the As-Built.

The software cannot validate a drawing in the As-Built using the Global Validation functionality if you have checked out that drawing to a project.

**Check Out Command (Project Menu)**

Displays the **Check Out** dialog, allowing you to check drawings out from the Plant and into your current project. This command checks user permissions, assigned in Smart Engineering Manager, before it allows you to check out a drawing.

You can check out drawings that you have already fetched to your project, too. The **Check Out** command is available only inside a project of the Plant; that is, you cannot check a drawing out from a project and into the Plant. After a drawing is checked out to a project, the drawing icon changes to reflect the new status.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

80/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You do not have to check out a drawing to claim items on that drawing.

If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions, when you check the drawing out, the fetched version remains intact and only its status changes to checked-out. That is, you cannot replace the fetched version with the version in the Plant.

**Check Out a Drawing**

Select **Check Out** .

1. On the **Check Out** dialog, select the drawing that you want to check out from the Plant hierarchy.
2. If you already have a fetched version of the drawing in your project and you want to replace it with the version that you check out, select the **Replace existing P&ID** option.

If you do not replace the existing P&ID, your previously fetched version remains, but its status changes to **Checked-out**.

1. (Optional) Enter comments in the **Comments** area.
2. Select **OK**. If you want to review notes about this operation after it is completed, select **View Log** on the **Checking Out Drawings** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

81/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

To undo the checkout, see Undo a Drawing Checkout.

**Check Out Dialog**

Displays the active Plant hierarchy and lists its drawings, allowing you to fetch a drawing from the specified database. This dialog appears when you select **Project** > **Check Out** or the **Check Out** button .

**Open Database**

Opens the **Projects** dialog, which allows you to specify a different project or the Plant.

**Filter**

Opens the **Filter** dialog, which allows you to specify the drawings that are displayed in the **List** view.

**Cancel Filter**

Deactivates any ad hoc filter you have applied to the **List** view.

**Include Subnodes**

Displays all the drawings and node names that reside in the currently selected node.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

82/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**List**

Displays the **List** view. The **List** view displays only one property for each drawing. To specify which property displays, select **Customize View** . The first item in the **Selected Properties** list is the property that appears in the **List** view.

**Details**

Displays the **Detail** view, which contains all the properties specified in the **Selected Properties** list on the **Customize Current View** dialog. Using the **Detail** view allows you to view and sort drawings by several attributes.

**Customize View**

Opens the **Customize Current View** dialog, which allows you to specify the information about each drawing that is displayed in the **List** view.

**Options**

Displays options specific to this check-out operation.

**Replace existing P&ID**

Overwrites the existing P&ID in the project if you have previously fetched a version of this drawing. If you have more than one drawing selected, at least one of them must exist in the project as a fetched drawing for this option to be available. If you are connected to SmartPlant Foundation and you have already fetched the drawing with read/write permissions, when you check the drawing out, the fetched version remains intact and only its status changes to checked-out.

**Create New Version**

Saves a new version of the drawing before overwriting the existing version. This option is not enabled if the current drawing does not already exist in the project. Also, if the drawing being checked out is already fetched to the project, you must first select **Replace existing P&ID** to enable the option.

**Comments**

Allows you to enter comments pertinent to this check-out operation.

**Checking Out Drawings Dialog**

Displays the progress of the version checking out operation currently underway. This dialog opens when you select **OK** on the **Check Out** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

83/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that are being checked out, and shows the status of that operation.

**View Log**

Opens the log file, CheckOut.log, which is created when you check out a drawing version.

**Undo Checkout Command (Project Menu)**

Opens the **Undo Checkout** dialog, which enables you to return the drawing to the status of not being checked out without going through the process of checking the drawing in. This command is available only when you are working in the project that has the drawing in question checked out. You must select the checked-out drawing in the **List** view in order to use this command.

If you do not choose to remove the drawing from the project when you undo the checkout, the drawing remains in the project as a fetched drawing with read/write permissions.

If the project has claimed items on the checked-out drawing, then selecting **Undo Checkout** and using the **Remove from project** option, the software reminds you to release all claims prior to undoing the check out.

**Undo a Drawing Checkout**

1. In the **List** view in the project, select the checked-out drawing that you want to return to the Plant.
2. Select **Project** > **Undo Checkout**.
3. On the **Undo Checkout** dialog, choose an option for either retaining or completely removing the drawing from the project database.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

84/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Undo Checkout Dialog**

Allows you to return the selected drawing to the Plant without going through the process of checking the drawing in. With the options on this dialog, you can choose to leave a fetched version of the checked-out drawing in the active project or to delete the drawing from the project database altogether. This dialog opens when you select **Project** > **Undo Checkout** on the main menu bar.

**Remove from project**

Returns the drawing to the Plant and deletes it from the project. If the project has claimed items on the checked-out drawing, you must release all claimed items before you can undo checkout.

**Leave in project**

Returns the drawing to the Plant while leaving a fetched drawing with read/write permissions in the project.

**Editing Drawing Items Within a Project**

New items can be created in a project drawing using Smart P&ID. As these items are added to the drawing, they are automatically claimed by the project. If your edits to an item cause related items to be modified, those related items must be claimed also. Moving items and adding labels, for example, can be accomplished without claiming.

When an existing drawing is fetched or checked out to a project, none of the items are claimed. You will not be able to modify or delete any items until they are claimed. Use the **Claim** command to define the scope for your project. Claim modes include Exclusive and Shared. Exclusive mode allows only a single project to claim an item. Using Shared mode, multiple projects can claim the same item at the same time.

You can compare your current drawing with a previous version to locate any differences. These differences display as change groups. The change group contains a list of changes that can be made in the current drawing and still maintain consistency. You can then choose to accept the changes, if needed. Each change group is marked if it affects items you have claimed. You should accept, or refresh, all of the changes that do not involve items claimed by you because these items represent changes checked in by other projects.

See Comparing and Refreshing Versions

Items must be claimed before you can delete them. If deleting an item results in changes to related items, then those related items must be claimed also.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

85/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Returning a Drawing to the Plant Using Check In**

Checking in a drawing writes all of the changes made to the drawing by the project into the drawing stored in the Plant. When a drawing is checked in, all versions of that drawing are deleted from the project.

**Verification Processes Performed During Check In**

All objects that exist in the project but don’t exist in the Plant must be claimed.

All objects that exist in the Plant but don’t exist in the project (they were deleted) must have been claimed.

All objects that exist in both the Plant and the project must be identical if not claimed.

The claim state must be valid for the project.

If any claim on an object on this drawing is invalid, then check in cannot occur.

The timestamp on all objects that exist in the project must be earlier than or equal to the timestamp on the drawing.

Last Publish Date > Drawing date.

Check in is not allowed if drawing is in a **Re-create** state.

The **Verify for Checkin** command for new drawings should ensure that all items on the drawing have been claimed.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for** **Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Check In Command (Project Menu)**

Enables you to check drawings into the Plant. This command is available only when drawings are selected in the **List** view and when those drawings are checked out to the current project. Drawings created in a project automatically belong to that project and can be selected and checked in. This command is not available from within the Plant.

You must have the correct permissions, assigned in Smart Engineering Manager, before you can check drawings in or out.

You cannot check a drawing in if any of the objects that belong to that drawing were modified after the latest version of a drawing was created. For more information about creating versions, see Save a

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

86/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Version of a Drawing.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for** **Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Check In a Drawing**

1. In the **List** view, select the drawings that you want to check into the Plant.
2. Select **Project** > **Check In** or select on the main toolbar.
3. On the **Check In** dialog, select either **Keep checked out and maintain claims, Remove from** **project** or **Leave in project**. If you leave the drawing in the project, it becomes a fetched drawing with read/write permissions.
4. (Optional) Enter comments in the **Comments** box.
5. Select the **Compare** button if you want to compare the version you have selected to check in with

other versions of the drawing. See Comparing Drawing Versions.

1. On the **Checking In Drawings** dialog, follow the progress of the operation. Select **View Log** if you want to review notes about this drawing check-in.

You cannot check in a fetched drawing. In order to check a drawing in, it must be checked out. For

more information about checking out drawings, see Check Out a Drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

87/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If your current active database is the Plant database, you cannot check in drawings. See *Connect to a*

*Database* in the *Smart P&ID Drawing Manager Help*.

When you check a drawing into the Plant, any claims on objects on that drawing are automatically released. See Claiming Items.

When you check a drawing into the Plant, your version of the drawing becomes the current version in the Plant. However, the version that was in the Plant already is automatically saved as the previous version.

You can select a checked out drawing and use the **Verify for Checkin** command to make sure claims

and conflicts are resolved before you try to check in a drawing. See Verify a Drawing for Checkin.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for** **Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Related Drawings Dialog**

This dialog opens when you run the **Check In** command after selecting a drawing for check-in that is related to other drawings that were not selected. You must check in all related drawings together. To enable checkin of the selected drawing, close this dialog and select all the related drawings before running the **Check In** command.

**Check In Dialog**

Allows you to return ownership of drawings to the Plant. This dialog opens when you select **Project** > **Check In** on the main menu bar.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

88/291

3/13/25, 10:36 AM

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

**Minor revision**

Displays the new minor revision for the selected drawings, if added.

**New Revision**

Opens the **New Revision** dialog and allows you to add a revision for the drawings prior to check-in. The values that you enter appear in the **Major revision** and **Minor revision** boxes.

**Compare**

Performs a comparison between the latest versions of the drawings in the active project and As-Built. The **Compare** button is not available when you have selected more than one drawing for check-in or if no drawing version exists in As-Built for the selected drawings.

**Checking In Drawings Dialog**

Displays the status of the check-in operation and allows you to review notes on the task. This dialog opens when you select **OK** on the **Check In** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

89/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that you selected to check into the Plant and displays the progress of the process through the list.

**View Log**

Allows you to review the log file for the check-in operation when the task is finished.

**Verify a Drawing for Checkin**

1. Select the project in the **Tree** view.
2. In the **List** view, select the checked-out drawings that you want to check into the Plant.
3. Select **Project** > **Verify for Checkin**.
4. On the **Verifying Drawings for Checkin** dialog, observe the progress of the verification operations.

Select **View Log** if you want to examine notes on the operation.

After verifying the drawing for checkin, check the drawing into the Plant as soon as possible because the verification process does not freeze the drawing state and the changes can be made to the

drawing during any interim time between verification and actual check in. See Check In a Drawing.

You cannot check in a fetched drawing, it must be checked out first. You can, however, check in a new drawing created in the project. See Check Out a Drawing.

Verifying a drawing for checkin checks exactly the same drawing conditions as the **Check In** command, but without actually checking the drawing into the Plant.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for** **Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

90/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Verification Processes Performed During Check In**

All objects that exist in the project but don’t exist in the Plant must be claimed.

All objects that exist in the Plant but don’t exist in the project (that is, they were deleted) must have been claimed.

All objects that exist in both the Plant and the project must be identical if not claimed.

The claim state must be valid for the project.

If any claim on an object on this drawing is invalid then check in cannot occur.

The timestamp on all objects that exist in the project must be earlier than or equal to the timestamp on the drawing.

Last Publish Date > Drawing date.

Check In not allowed if Drawing is in a **Re-create** state.

The Verify for Checkin for new drawings should ensure that all items on the drawing have been claimed.

**Verify for Checkin Command (Project Menu)**

Checks the selected drawing to see if there are any conditions that would keep it from successfully being checked into the Plant. For a list of items or issues checked during the verification process, see Returning a

Drawing to the Plant Using Check In.

If the drawing fails this verification, select the **View Log** button on the **Verifying Drawings for Checkin** dialog and review the items listed there.

Even though a drawing passes verification, the state of the drawing is not then frozen. Subsequent actions can cause a drawing not to be ready for checking in. If your drawing is verified and you do want to check it into the Plant, then you should do so as soon as possible after verifying it for checkin.

If an invalid claim is found but the item in question matches the item in the Plant, run **Verify for Checkin** to resolve this situation. This process automatically sets the claim to valid and allows the check in to occur.

**Verifying Drawings for Checkin Dialog**

Displays the progress of the version verification operation currently underway. This dialog opens when you select **Project** > **Verify for Checkin**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

91/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that are being verified for checkin, and shows the status of that operation.

**View Log**

Opens the log file that is created by the verification process.

**Reviewing the Drawing Status**

Checking the drawing status allows you to see which projects that have fetched or checked out the selected drawings.

**Drawing Status Command (Project Menu)**

Displays the projects that have fetched or checked out the selected drawing. This command is available in the Plant and in any of its projects. You can select more than one drawing and display their statuses at the same time.

The **Drawing Status** dialog displays information about the project and the user who changed the status, the time of the change, and any comments that were added during the status change. These comments can be entered during any status-changing operations, such as fetching, checking out, checking in, and undoing a checkout.

**Drawing Status Dialog**

Displays information about the project and user that changed the drawing status, the time the status was changed, and any comments that were added when the status was changed. Status changing operations include checking out, checking in, fetching a drawing, and undoing a checkout. This dialog opens when you select drawings in the **Tree** view and then select **Project** > **Drawing Status**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

92/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**History**

Displays the pertinent information about the selected drawings.

**Check Drawing Status**

1. In the **List** view, select a drawing.
2. Select **Project** > **Drawing Status** or select on the toolbar.
3. Review the information on the **Drawing Status** dialog.

**Sample Project Workflows**

The following scenarios provide workflows for using projects in various configurations. You must perform the activities below before executing the workflows.

1. In Smart Engineering Manager, do the following:
2. Create a site.
3. Create a plant.
4. Associate the Smart P&ID Modeler application.
5. Create plant groups that allow drawings.
6. In Smart P&ID Drawing Manager, create new drawings A - E and G, as shown.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

93/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. In Smart P&ID Modeler, do the following:
2. Open Drawing A.
3. Create Assembly A-1 and assign the item tags as shown.

Choose vessel type **Equipment** > **Vessels** > **Vertical Drums** > **Short 1D 1C 1to1**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

94/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Place both OPC partners in the Plant Stockpile.

1. Make the assembly available in Catalog Explorer by opening Options Manager and running the **Tools** > **Generate Symbol Images** command.
2. Open Drawings B, C, D, and G and place Assembly A-1 in each of the drawings.

*The software assigns unique item tags to the vessel, pipe runs, and OPCs in each drawing.*

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
4. Find and replace Vessel V-100 with a 1 to 1 Parametric V Drum.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

95/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Exit Drawing A.

*Drawing A becomes Drawing A’.*

1. In Project 2, fetch Drawing A’ from Project 1.
2. In Project 1, execute the **Undo Checkout** command on Drawing A’, leaving Drawing A’ in Project 1.
3. In Project 2, open Drawing A’.
4. Claim Nozzle N1.
5. Change the Tag Sequence Number of the nozzle to 4.
6. Exit Drawing A’.

*Drawing A’ becomes Drawing A’’.*

1. Check out Drawing A from the Plant to Project 2 *without replacing the existing P&ID*.

*Drawing A becomes Drawing A’’.*

1. In Project 2, attempt to check in Drawing A’’.
2. View the check in log file.

*Unclaimed changes prevent check in.*

1. Open Drawing A’’.
2. Claim Vessel V-100.
3. Exit Drawing A’’.

*Drawing A’’ becomes Drawing A’’’.*

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

96/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Check in Drawing A’’’ with removal of the drawing from the project.

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an arrow**

**indicates changes to the drawing or to drawing**

**item data)**

---

**Check in drawing**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

97/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Check-in unsuccessful**

**Undo drawing check-out**

**Refresh: Modify a Drawing Concurrently in Two Projects**

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing B from the Plant.
2. Open Drawing B.
3. Fence select all items and claim the selected items.
4. Exit Drawing B.
5. In Project 2, fetch Drawing B from the Plant.
6. Open Drawing B.
7. Fence select all items except both OPCs and claim the selected items.

*The claim status for the items indicates that they have already been claimed by another project.*

1. Change the Tag Sequence Number for the vessel to **110**.
2. Change the Construction Status of the vessel from **New** to **Existing**.
3. Exit Drawing B.

*Drawing B becomes Drawing B’.*

1. In Project 1, open Drawing B.
2. Place an Area Break around the vessel and Nozzle N1.
3. Place an Alt Dgn Press-Temp Equipment Label on the Area Break.
4. Select the Area Break, right-click, and on the shortcut menu, select **Select Contents**.
5. In the **Properties** window, if you cannot see the pressure and temperature properties, select **Show** **Case Data** for the Select Set to display those properties.
6. Assign **Alt Dgn Max Press** of **100 psi**.
7. Assign **Alt Dgn Max Temp** of **101 F**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

98/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Exit Drawing B.

*Drawing B becomes Drawing B’’.*

1. In Project 1, check in Drawing B’’ with removal of the drawing from the project.
2. Select **Project** > **Project Status**.
3. Select **Complete Project**.
4. Select **Merge Project** to merge Project 1 into the Plant.

If you complete and merge Project 1, you will not be able to use it for the other workflows unless you delete and re-create Project 1. If you want to continue without deleting and recreating the project, you should skip both the Complete and Merge operations until you have completed all of the workflows.

1. In Project 2, check out Drawing B’’ *without replacing the existing P&ID*.

*Drawing B’’ becomes Drawing B’ in Project 2.*

1. In Project 2, attempt to check in Drawing B’.

*Invalid Claim prevents check-in.*

1. In Project 2, open Drawing B’ and compare it with the drawing in the Plant.
2. Do the following:
3. Refresh Drawing B’ for the Area Break and label and all other differences that result in invalid claims (see Compare and Refresh Drawing Versions).
4. Place a Revision Cloud around the Control Valve (FV-…) and the Actuator (ACT-…).
5. Place a Revision Triangle on the Revision Cloud. Label the Revision Triangle RT- 1.
6. Exit Drawing B’.

*Drawing B’ becomes Drawing B’’’.*

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

99/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Check in Drawing B’’’.

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an arrow**

**indicates changes to the drawing or to drawing**

**item data)**

---

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

100/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

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
2. In Project 2, check out Drawing C from the Plant *without replacing the existing P&ID*.
3. In Project 3, fetch Drawing C’’ from Project 2.
4. Open Drawing C’’.
5. Add a Generic Tray to the vessel.
6. Exit Drawing C’’.

*Drawing C’’ becomes Drawing C’’’.*

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

101/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

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
4. Perform Compare and Refresh for the generic vessel tray.
5. Exit Drawing C’.
6. Check in Drawing C’.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

102/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

103/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Fetch drawing**

**Continuity between procedure steps (an arrow**

**indicates changes to the drawing or to drawing**

**item data)**

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
6. Exit Drawing D.

*Drawing D becomes Drawing D’.*

1. In Project 1, create Drawing F.
2. Open Drawing F.
3. Place the instrument OPC that was placed in the Plant Stockpile after being deleted from Drawing D.
4. Place a Multiple Representation of the vessel.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

104/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Add an Equipment Name label to the vessel.
2. Exit Drawing F.

*Drawing F becomes Drawing F’.*

1. Attempt to check in Drawing F’.

*Related Drawings error prevents check in.*

1. Check in Drawings D’ and F’ together.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

105/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

**Fetch drawing**

**Continuity between procedure steps (an arrow**

**indicates changes to the drawing or to drawing**

**item data)**

---

**Check in drawing**

**Check-in unsuccessful**

**Fetch Older Drawing Versions and OPCs**

Before performing this scenario, ensure that you have completed all the prerequisite activities described in Sample Project Workflows.

1. In Project 1, check out Drawing G.
2. Open Drawing G.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

106/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Claim the vessel, Nozzle N1, and the pipe run connected to the nozzle.
2. Delete the vessel and Nozzle N1 from the model.
3. Exit Drawing G.

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
3. In Project 3, open Drawing I’.
4. Claim OPC2 (in Drawing I stockpile).
5. Use the Delete to Stockpile command to remove OPC2 from Drawing I’.
6. Use the Move to Different Stockpile command to place OPC2 into Project 3 Plant stockpile.
7. Exit Drawing I’.

*Drawing I’ becomes Drawing I’’.*

1. In Project 1, check in Drawing G’.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

107/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. In Project 3, fetch Version 1 of Drawing G’ from As-Built.

To fetch the correct version of Drawing G’, select **History** on the Fetch dialog and Version 1 on the **Version History** dialog.

1. From Project 2, check in Drawing H’ and then check it out to Project 3.
2. Open Drawing H’.
3. Claim OPC1, OPC2, and OPC3.
4. Exit Drawing H’.

*Drawing H’ becomes Drawing H’’.*

1. Check in Drawing I’ and Drawing H’ from Project 3 into As-Built.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

108/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Key**

**Check out drawing**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

109/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Fetch drawing**

**Continuity between procedure steps (an arrow**

**indicates changes to the drawing or to drawing**

**item data)**

---

**Check in drawing**

**Check-in unsuccessful**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

110/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Working with Drawing Versions and Revisions**

You can create revisions for drawings consisting of major and minor revisions and include the revision information in the drawing title block if desired. You can also associate a version with the latest revision if you need to archive drawings for viewing or comparing. You can compare two archived drawings or you can compare an archived drawing with the current drawing.

**Using Drawing Versions**

Drawing versions allows you to create, compare, and recover versions of your drawings. Using drawing versioning is helpful in the following situations.

Restoring a drawing after it has been deleted

Restoring a drawing after items have been deleted from the drawing Restoring a drawing after making design errors

Archiving a drawing before making major design changes

When a drawing is checked in, all versions in the project are deleted.

**Creating a New Version of a Drawing**

The current state of a drawing and all associated data can be saved using the New Version command.

Previously saved drawing versions are available to be viewed, compared, and fetched, if necessary. If drawing versions are saved on a regular basis, the sequence of drawing versions in a project becomes a sort of archive that shows the development of the drawing over the life of the project.

Each time a drawing is checked into the Plant database, a new version of the drawing is automatically created in the Plant and all versions of that drawing are deleted from the project. The drawing versions in the Plant show the changes to the drawing over the life of the Plant.

**New Version Command (Revisions Menu)**

Saves a new version of the selected drawing. The **New Version** dialog opens, allowing you to add comments to the version as you create it.

Previously saved drawing versions are available to be viewed, compared, and fetched, if necessary. If drawing versions are saved on a regular basis, the sequence of drawing versions in a project becomes a sort of archive that shows the development of the drawing over the life of the project.

Each time a drawing is checked into the Plant database, a new version of the drawing is automatically created in the Plant and all versions of that drawing are deleted from the project. The drawing versions in https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

111/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

the Plant show the changes to the drawing over the life of the Plant.

**New Version Dialog**

Allows you to enter notes pertaining to the creation of this new version. This dialog opens when you select a drawing and select **Revisions** > **New Version**. When you select **OK**, the **Creating Version of Drawings** dialog opens and you can follow the version creation process.

**Comments**

Enter notes pertaining to the creation of this new version. These notes can be viewed by other projects and the Plant when they check the history of a drawing.

**Schedule**

Opens the Schedule Task Wizard, which allows you to schedule version creation for a later time or at a regular interval. For details, see Scheduling Tasks.

**Creating Version of Drawings Dialog**

Displays the progress of your version creation. This dialog appears when you select **OK** on the **New** **Version** dialog.

**Drawings**

Lists the versions that are being created and shows the status of version creation process.

**View Log**

Opens the log file that is created when you save a new version.

**Save a Version of a Drawing**

1. In the **List** view, select a drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

112/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select **Revisions** > **New Version** or select **New Version** .
2. On the **New Version** dialog, enter any comments that you want to attach to the new version.
3. Select **OK** to create the version.

Select **View Log** on the **Creating Version of Drawings** dialog to open the log file and review notes on the version creation operation.

**New Version** skips open drawings, notes them in the log, and then continues.

If no changes have been made to the drawing since the last version was created, no new version is created.

When a drawing is checked in to the Plant, all versions are deleted from the project.

When a drawing version is created, it is stored in a database segment named LOBSEGMENT. This space is not reclaimed when drawing versions are deleted. However, if you delete the older version of a drawing before creating a new version, then the database size will not increase rapidly. Deleting older version will create free space in LOBSEGMENT (without decreasing the total LOBSEGMENT

size) which will be available for storing future drawing versions.

Use the **Schedule** button to create a task for creating drawing versions at a later time or on a regular interval. Follow the instructions on the Schedule Task Wizard (for details, see Scheduling Tasks).

**Incremental New Versions Command (Revisions Menu)**

Opens the Schedule Task Wizard, allowing you to create a task to save all drawings in a plant or site whose time stamp shows that changes have been made since the last version was saved. For details, see

Scheduling Tasks.

**Save Versions of All Drawings**

1. In the **Tree** view, select the site, plant, or project containing the drawings you want to save versions of.
2. Select **Revisions** > **Incremental New Versions**.
3. Follow the steps and directions on the **Schedule Task Wizard**, and select **Finish** to schedule the operation at another time or on a regular interval.

When saving versions of all drawings in a Plant that has projects, new versions of the drawings belonging to those projects are created also.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

113/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

This procedure saves new versions of only those drawings whose time stamp shows that they have changed since the last version was saved.

Instead of creating versions of a set of drawings, you can create a version of a single drawing. For more information, see Save a Version of a Drawing.

**Version History Command (Revisions Menu)**

Opens the **Version History** dialog, which displays a record of the versions of the selected drawing and allows you to view the drawing or compare the drawing with other versions of the drawing.

**Version History Dialog**

Lists all available versions of a drawing. You can compare two versions of the drawing, or view a version of the drawing without opening Smart P&ID, or fetch a version from the list. You can open this dialog by selecting **Revisions** > **Version History** or by selecting the **History** command on the **Fetch** dialog.

**History**

Lists all the versions of the drawing in the current plant or project.

**Compare**

Opens the **Compare** dialog, allowing you to compare two versions in the **History** list. This command is not available unless two versions are selected in the list or if you open this dialog by selecting **History** on the **Fetch** dialog. Use the **Compare With** command to compare one version in the active project to a version in another project or the Plant.

**Compare With**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

114/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Opens the **Compare With** dialog, allowing you to find a drawing version in a different project or in the Plant to compare to the drawing version you select in the **History** list. This command is not available unless you are in a project or if you open this dialog by selecting **History** on the **Fetch** dialog.

**View**

Opens the** View** dialog, which displays a read-only view of the selected drawing version without opening Smart P&ID. You can manipulate the view or select drawing items and review their properties.

**Fetch**

Opens the **Fetch Comments** dialog. This command is available only if you have selected one, and only one, version in the **History** list and that drawing is not the current version. The **Fetch** command is not available if you open this dialog by selecting **History** on the **Fetch** dialog.

**Delete**

Removes the selected drawing version. You must have the appropriate permissions, assigned in Smart Engineering Manager, to delete versions. You cannot delete the current version of a drawing by using this command. However, you can delete the current version of a drawing by using the **Delete** command on the **Edit** menu on the main menu bar. If the selected version is one that was created especially for the last revision using the **Associate Version** command, then you cannot delete the version unless you first delete the revision.

**View Dialog**

Opens when you select the **View** button on the **Version History** dialog, allowing you to quickly view a read-only display of the selected drawing version without opening Smart P&ID.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

115/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Print**

Opens the **Print** dialog where you can specify options for printing your drawings.

**Zoom Area**

Enlarges the display of items in the active window.

**Zoom In**

Enlarges the display of items around a specified point in the active window.

**Zoom Out**

Reduces the display of items around a specified point in the active window.

**Fit**

Fits all visible items in the active view.

**Pan**

Allows you to move the display in any direction from a specific point in a drawing to see other areas of the drawing by dragging the pointer across the view.

**Select Tool**

Changes the pointer to the arrow-shaped selection pointer so that you can select items. The circle at the end of the pointer arrow is the locate zone.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

116/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Help**

Displays contents for the Help topics that include step-by-step instructions for using Drawing Manager.

**Drawing View**

Displays the graphical view of the selected drawing version.

**Properties Window**

Displays the properties associated with a drawing item that you select in the **Drawing** view.

**Selected Items List**

Itemizes all of the selected objects individually and as a select set.

**Alphabetic Button**

Displays item properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Categorized Button**

Displays item properties categorically. Categories are defined and assigned in Data Dictionary Manager.

This button acts as a toggle and is available when properties are displayed alphabetically.

**Fetch Comments Dialog**

Opens when you select **Fetch** on the **Version History** dialog and provides a way to enter comments about the operation.

**Comments**

Allows you to enter text pertaining to this fetch operation.

**Show the Version History of a Drawing**

1. In the **List** view, select the drawing whose history you want to view.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

117/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select **Version History** .
2. On the **Version History** dialog, review the versions in the **History** list.

Use the **Compare** command to compare two drawing versions selected in the **History** list. For more

information, see Compare Drawing Versions.

If the drawing exists in other projects, use the **Compare With** command to compare this version to a

version in another project or in the Plant. For more information, see Compare Drawing Versions for

As-Built and Projects.

Use the **Delete** command to delete a selected drawing version. You cannot delete the current drawing version.

Use the **View** command to open a read-only display of a selected drawing version. For more

information, see *View a Drawing in Drawing Manager*.

**Recovering Drawings**

The following areas require special consideration with regard to saving new drawing versions and how retrieving a drawing effects the actions that can occur in the Plant between saving a version and retrieving it. These actions have serious implications when recovering (using the **Fetch Deleted Drawing** command) a drawing. In all drawing recovery activities, a log file is created in which you can review notes on any recovery activity that you are undertaking.

**Multiple Representations**

After a drawing is recovered, there are situations where multiple representations of piping and equipment items can spontaneously occur. For example, you place a piece of equipment on drawing A and then you save a version of drawing A. After creating a version of drawing A, you move the equipment from drawing A to the Plant Stockpile and then to drawing B. When drawing A is retrieved, the following message is added to the log file:

Item (item tag *ItemTag*, internal ID *SP_ID*) is being restored as a multiple representation because another representation of the same item was found in drawing < *Drawing Name*>.

Encountering this situation does not cause the retrieval to fail; the retrieval process continues as normal.

If an equipment item already exists as a multiple representation in another drawing, the following message is added to the log file:

Restoring multi representation item (item tag *ItemTag*, internal ID *SP_ID*).

Encountering this situation does not cause the retrieval to fail; the retrieval process continues as normal.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

118/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If other valid stockpile items are moved from drawing A to drawing B, the following message is added to the log file:

Error ! Item (item tag *ItemTag*, internal ID *SP_ID*) has been moved to drawing < *Drawing Name*>.

To resolve this conflict, you must either delete the indicated item or restore the indicated drawing first. If you delete the item, then the item can either be deleted to the Plant Stockpile or deleted from the model. This error message is created for each moved item, and the retrieval process quits without restoring the archive.

**Off-Page Connectors (OPCs)**

If you save a new version of a drawing that includes an OPC, and its mate is deleted from the database afterward, both OPCs are restored to the drawing or drawing stockpile, as appropriate, when the drawing is retrieved.

For example, an OPC is placed on a drawing A, its mate is placed on drawing B, and both drawings saved in versions. When drawing A is retrieved, the OPC is restored to drawing A, and the mate is placed in the Plant Stockpile. The mated OPC has the same item tag as the OPC restored to drawing A. After drawing B

is retrieved, the OPC mate of the OPC in drawing A is placed in drawing B and removed from the Plant Stockpile.

**Pipe and Signal Lines**

If all the line runs belonging to a line are deleted from the model after a drawing version is saved, the line is restored back to the database after the drawing is recovered.

To restore a deleted line, Drawing Manager searches the database for a line that has the same key property values as the line that is being restored. If such a line is found, it is used as the line for the restored runs. If a suitable line is not found one is created for the restored runs.

**Plant Group Joins**

Plant Group Joins, which relate items in plant groups, are restored from a version only if the plant group, such as the unit or area, exist in the current database.

For example, a piece of equipment belongs to a plant group and a drawing version is saved. If the plant group is deleted and then the drawing is recovered, the equipment is restored, but because the plant group does not exist, the Plant Group Join is not restored.

If the plant item group is found in the archived drawing, but the Plant Group Join does not exist in the current database, Drawing Manager restores the Plant Group Join.

**Plant Item Groups**

Plant Item Groups placed in the drawing stockpile are considered part of the drawing; therefore, Drawing Manager restores them to the drawing stockpile when the drawing is recovered.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

119/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Plant Item Groups that are moved to the Plant Stockpile after a drawing version has been saved are restored back to the drawing stockpile when the drawing is recovered. The software searches for the corresponding Plant Item Group in the saved stockpiles, and if it is not found there, searches in the active database for the same.

**Plant Item Group Joins**

A Plant Item Group Join is a relationship created when a plant item, such as an instrument or a piece of equipment, is linked to a Plant Item Group, such as an instrument loop, a package, or the like. Plant Item Group Joins are saved as part of the drawing version.

During a drawing recovery, if a Plant Item Group Join exists in the saved drawing version, the software searches for the corresponding Plant Item Group in the archived stockpiles. If the corresponding Plant Item Group is not found in those stockpiles, the database is also searched.

If the Plant Item Group is found in the saved version, and the Plant Item Group Join is not found in the database, then the Plant Item Group Join is restored. If the Plant Item Group is not found in the saved stockpiles, the Plant Item Group and the Plant Item Group Join are restored to the Plant Stockpile. If the Plant Item Group exists in the current drawing stockpile, Drawing Manager updates the database to reflect the archived Plant Item Group Join.

For example: An instrument is associated with a Loop, LP1, in the drawing stockpile and a version is saved.

Afterward, a new Loop, LP2, is placed in the drawing stockpile and the instrument is associated with LP2.

When the drawing is restored, the Plant Item Group Join indicates a relationship between the instrument and LP1. If LP1 has since been deleted from the drawing stockpile, it is restored to the drawing stockpile. If LP2 exists in the current Plant Stockpile at the time of drawing recovery, LP2 is left as is. However, if LP2 is in the drawing stockpile, Loop LP2 is deleted from the database along with any other corresponding representations and histories of Loop LP2.

**Miscellaneous**

If a drawing is deleted after a version is saved and a new drawing is created using the same name and drawing number as the deleted drawing, retrieval of the deleted drawing fails. Changing drawing properties, such as name, number, and so forth, after saving a version of a drawing results in the original values being restored when the drawing is recovered. If this situation occurs, the following message is added to the log file:

Warning! Drawing < *Drawing Name1*> has been renamed to *new drawing name2*.

Drawing Manager changes the drawing back to its original name, *drawing name1*, in the database. The original .pid file *pathname\drawing name1* is also replaced. You must delete the .pid file for *pathname\*

< *Drawing Name2*>.

You must have either site administrator or modify privileges to save versions or recover drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

120/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You cannot restore hierarchy items by using drawing recovery. For example, if a unit is deleted, an archived drawing belonging to that unit can never be retrieved.

**Recover a Version of a Drawing**

Be sure you are familiar with the ramifications of drawing recovery before you undertake the

operation. For more information, see Recovering Drawings.

1. In the **List** view, select the drawing that you want to recover.
2. Select **Revisions** > **Version History** or select the **Version History** button .
3. On the **Version History** dialog, select the version of the drawing you want to recall.
4. Select **Fetch** and enter comments on the **Fetch Comments** dialog.
5. On the message box, select **Yes** to confirm that you want to overwrite the current version with the saved version you have selected.
6. Select **View Log** on the **Fetching Drawings** dialog if you want to see notes about this operation.

You can also recover a version of a drawing by selecting **Fetch** . Using the **Fetch** command is particularly useful if you want to recover a version of your drawing that resides at the Plant or another project. For more information, see Fetch a Drawing.

**Fetch Deleted Drawing Command (Revisions Menu)**

Allows you to recover drawings that have been deleted from the plant structure; whenever you delete a drawing, a version is automatically saved. The **Fetch Deleted Drawing** dialog opens so that you can specify the drawing versions you want to recover. You must select an appropriate plant structure in the **Tree** view in order to be able to use this command.

Be sure you are familiar with the ramifications of drawing recovery before you undertake the

operation. For more information, see Recovering Drawings.

**Fetch Deleted Drawing Dialog**

Lists the drawings that are deleted, allowing you to select which drawings to retrieve. This dialog opens when you select **Revisions** > **Fetch Deleted Drawing**. The plant structure where the deleted drawings were must be active in the **Tree** view before this command is made available.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

121/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Deleted drawings**

Lists deleted drawings.

**Delete permanently**

Permanently deletes selected drawings from the database. Permanent deletion of drawings is an irreversible action.

It is not possible to permanently delete drawings that have been checked out or fetched by other projects.

**Schedule**

Opens the Schedule Task Wizard. Follow the directions in the wizard to schedule retrieval at a later time or

on a regular interval. For details, see Scheduling Tasks.

**Fetching Deleted Drawings Dialog**

Opens when you select **OK** on the **Fetch Deleted Drawing** dialog, and displays the progress of your recovery operation.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

122/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drawings**

Lists the drawings that are being retrieved, and shows the status of that operation.

**View Log**

Opens the log file that is created when you perform a drawing recovery operation.

**Delete Drawings Permanently**

1. Select the appropriate plant level in the **Tree** view, and select **Revisions** > **Fetch Deleted Drawing**.
2. On the **Fetch Deleted Drawing** dialog, select the drawings you want to delete.
3. Select **Delete Permanently**.
4. At the prompt, select **Yes** to confirm deletion of the selected drawings from the database.

This action is irreversible; drawings cannot be recovered after being deleted permanently.

It is not possible to permanently delete drawings that have been checked out or fetched by other projects.

**Recover a Version of a Deleted Drawing**

1. Select the appropriate plant level in the **Tree** view, and select **Revisions** > **Fetch Deleted Drawing**.
2. On the **Fetch Deleted Drawing** dialog, select the drawing you want to retrieve.
3. Select **OK** to retrieve the drawing now or select **Schedule** to open the Schedule Task Wizard, which allows you to schedule retrieval at a later time or on a regular interval. For details, see Scheduling

Tasks.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

123/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. On the **Fetching Deleted Drawings** dialog, select **View Log** to review notes about this retrieval process.

All the saved versions of the selected drawing are retrieved. You can view the various versions by selecting the drawing in the **List** view and selecting **Revisions** > **Version History**.

If you retrieve a drawing that was new to your Plant or project, then the drawing icon for a new drawing will be applied; otherwise, the drawing icon for a fetched drawing is used in the **List** view.

**Comparing Drawing Versions**

When more than one version of a drawing exists, the **Compare** command on the **Version History** dialog allows you to view two versions side-by-side and examine their differences. You can compare two versions from inside your own Plant or project database, or you can compare a version in your database to a version in the Plant or another project database. Keep in mind that you can only compare a drawing against a version of itself; that is, you cannot compare one drawing to another drawing.

Differences between drawing versions are assigned to logical “change” groups, which are listed on the **Compare** dialog.

Differences also belong to one of three possible categories: **Data**

Refers to a mismatch in the properties assigned to an item that exists in both drawings, namely a change, addition, or deletion of a property in the **Properties** window, in the **Engineering Data Editor** in Smart P&ID, or through automation.

**Graphic**

Refers to an item that has changed only in its graphical representation in the design (for example, the item is moved or otherwise graphically manipulated in the drawing).

The following differences are ignored: claim status, select list strings, linked or embedded objects, symbology, and inconsistency indicators.

Adding or deleting an item is also a connectivity change because the relationship between the item and the drawing has changed. Every change grouping and every changed item is assigned a category, and if more than one category applies (for instance, if you move an item and change one of its properties) then the highest priority category is displayed. The order of priority, from high to low, for the categories is connectivity then data then graphic.

The two versions are displayed in two **Drawing** views, described only as left and right. The relationship between the two views depends on whether you are comparing two versions in your own database or comparing your version to a version in another database.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

124/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If the two versions are in the active database, then the left-hand view is the older version, and the right-hand view is the newer version. That is, they are displayed in time-order from left to right.

If the two versions exist in different databases, you cannot be assured that time-order is the logical order to display the versions; therefore, the right-hand view is reserved for the version in your active Plant or project database, and the left-hand view belongs to the version in another database.

You can also compare the differences between the typicals of either drawing. Using the select list situated in the drawing name bar of each view, you can display the primary, typical, or both views of the selected version.

The **Compare** dialog in Drawing Manager is useful reviewing differences between versions only. If you want to reconcile anything about the two versions you review, then you must do so inside Smart P&ID modeler.

The **Compare and Refresh** command in Smart P&ID modeler exists for this purpose. If you started with the left-hand drawing version and applied every change listed on the **Compare** dialog, then you would end with a drawing that is identical to the right drawing version. For more information about reconciling two versions, see *Smart P&ID Modeler Help.*

**Compare Drawing Versions**

1. In the **List** view, select the drawing.
2. Select **Version History** .
3. In the drawing list on the **Version History** dialog, select two versions of the drawing.
4. Select **Compare**. If you want to compare your drawing to a version in a different project or the Plant,

see Compare Drawing Versions for As-Built and Projects.

1. On the **Compare** dialog, you can view the differences between the two versions, but you cannot make changes to the designs. To change the design, you must use the Smart P&ID Modeler. For more information about using the compare-and-refresh capabilities, see *Smart P&ID Modeler Help*.

You can manipulate the views and navigate through the listed changes by using the commands on the **Compare** dialog toolbar. Each **Drawing** view also has its own shortcut menu, which includes manipulation commands that apply only to that view.

You can select an item in either **Drawing** view. The item is then located in the appropriate group in the **Change details** list. If you select an item in the **Change details** list, then you can use the **Find in** **Drawings** button on the toolbar to locate the item in one or both **Drawing** views.

You can select an item in the **Drawing** view or in the **Change details** list. Properties for that item appear in the **Properties** window. Selecting multiple items is not possible on the **Compare** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

125/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

The following differences are ignored: claim status, select list strings, linked or embedded objects, symbology, and inconsistency indicators.

You can only compare a drawing against a version of itself; that is, you cannot compare one drawing to another drawing.

You can also compare versions when you are checking in a drawing. For more information, see Check

In a Drawing.

If at any point you attempt to compare two versions that are actually identical to each other, the **Compare** dialog does not open and a confirmation message alerts you as to why.

**Compare Dialog**

This dialog opens when you select **Compare** on the **Version History** dialog, displaying two versions of the same drawing and indicating the differences between them.

You cannot do anything else in Drawing Manager while this dialog is open.

**Toolbar Commands**

The toolbar commands apply to the **Drawing** views. For icons that display a drop down-arrow, you can apply the command to either the right or left view.

**Compare Options**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

126/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Opens the **Compare Options** dialog, which allows you to customize the colors that the various comparison states are displayed in. That color coding is then displayed in the status bar as a static reminder.

**Print**

Prints the **Drawing** view or views.

**Generate Report**

Opens Microsoft Excel and creates a report of the information contained in this comparison session. This report lists the same information that is displayed in the **Change groups** and **Change details** lists (change groups, item types, claim statuses, and so forth).

**Find in List**

Zooms to the **Change details** list entry that corresponds to an item you select in either **Drawing** view. In general, if you select a drawing item that exists in the list, then the list display automatically zooms to that entry.

**Find in Drawings**

Manipulates the **Drawing** views so that the selected element is listed in the **Change details** and the **Change groups** list is centered in the appropriate **Drawing** view. You must first select an item in either the **Change groups** or **Change details** area.

**Zoom Area**

Enlarges the selected area in one or both **Drawing** views by allowing you to draw a fence around the area.

**Zoom In**

Enlarges the selected area where you click.

**Zoom Out**

Reduces the display of the selected area where you click.

**Fit**

Fits all the drawing elements into the visible viewing area of the active drawing. Selecting part of the drawing and clicking **Fit** fits the selected area into the visible viewing area of the active drawing.

**Pan**

Allows you to move the display in any direction from a specific point in one or both **Drawing** views in order to see other areas of the view by dragging the pointer across the display.

**Select**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

127/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Changes the pointer to an arrow allowing you to select an item.

**Help**

Opens the Online Help.

**Drawing Views**

The left and right drawing views display the two versions of your drawing being compared. The display above the drawing view shows the drawing name and the version. The select list in the display allows you to choose the drawing layers to be compared and can be selected individually for each version. Possible select list values are **Primary**, **Typical**, or **Both**.

If you compare two versions from different projects, the version that belongs to the other project appears in the left **Drawing** view and the version that belongs to your active Drawing Manager project appears in the right **Drawing** view. If you compare two versions from your active project, then the latest version appears in the right **Drawing** view.

At the top of each **Drawing** view, the Plant or project, the name of the drawing, and the version is displayed explicitly. You can move the bars between the different views according to your needs. If you double-click on the divider between the left and right **Drawing** views, then the software automatically adjusts the two views to be the same-size.

**Properties Window**

Displays two columns of properties for an item selected in a **Drawing** view or in the **Change details** list.

The left-hand and right-hand columns correspond to the left and right **Drawing** views. If a deleted item is selected (the item exists in left view, but not the right view), the properties for that item are listed in the left-hand column and the right-hand column is empty. If a modified item is selected, values from both versions show in their respective columns in the **Properties** window. If a new item is selected, that is, the item exists in right view, but not the left view, the properties for that item are listed in the right-hand column and the left-hand column is empty.

**Properties Commands**

Allows you to customize the properties that are displayed in the **Properties** window.

**Alphabetic**

Lists properties in alphabetical order. This button acts as a toggle and is available when properties are displayed categorically.

**Categorized**

Displays properties grouped by specific categories. Categories are defined and properties are assigned to those categories in Data Dictionary Manager. This button acts as a toggle and is available when properties are displayed alphabetically.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

128/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Show Modified**

Toggles the display of only those properties of the selected drawing item that are different in the versions.

This button applies only to modified items that exist in both versions. For added and deleted items, all properties are listed.

**Change groups**

Lists the changed items in groups. A listed item contains all the items this change effects. You can sort the list be clicking the column headings.

**Check box** column

Displays colors in the drawings as defined using **Compare Options**. If not selected, the **Default items** color displays.

**Number**

Displays an arbitrary number that is assigned to a logical change group when this dialog is opened. The number has no intrinsic meaning and might apply to a different group the next time you open this dialog.

**Identifier**

Lists item tags for the principal member of the change group, if an item tag is assigned to that object. For instance, if a change group centers around data differences for a vessel and its nozzles, then the item tag for the vessel is displayed in this column.

**Category**

Displays the category of the change, listed in order of highest to lowest priority. Options include: **Data**

Indicates that a property value has changed (for example, a property value for a vessel).

**Graphic**

Indicates that a change has been made to an item in the drawing (for example, a vessel has been moved).

**Claimed**

Displays an overview of the claim status of the individual items in the group. Possible values are **All**, **Some**, or **None**.

**Valid Claim**

Indicates that the claimed item is a valid claim.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

129/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Change details**

Lists all the individual items that belong to the group that you select from the **Change groups** list. You can sort this list by clicking on any of the column headings.

**Result**

Displays one of three possible values: **Left-Only**, **Right-Only**, and **Different**.

**Left-Only**

Denotes an item that exists in the left-hand version only, implying that the item is deleted from the right-hand version.

**Right-Only**

Denotes an item that exists in the right-hand version only, implying that the item was added to the right-hand version.

**Different**

Denotes a difference between the properties or graphical elements of an item that exists in both versions.

**Item Type**

Describes the item type, such as **Equipment** or **Instrument**.

**Specific Item Type**

Displays the specific type of item, such as **3-Way Ball Valve**, **Piping**, or **Flange Orifice**.

**Item Tag**

Displays the item tag of the individual item in question if a tag has been assigned to the item.

**Category**

Displays the highest priority category of change that applies. Possible categories are: **Data**

Indicates that a property value has changed (for example, a property value for a vessel).

**Graphic**

Indicates that a change has been made to an item in the drawing (for example, a vessel has been moved).

**Claimed**

Displays the claim status of the object:

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

130/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Valid claim

Invalid claim

Not claimed

**Stockpile**  or

Denotes whether the selected item is stored in the stockpile.

**View**

Displays the status of the selected item in relation to its placement in the primary or typical view, and between the selected versions. The following statuses are displayed: Added to Primary

Added to Typical

Moved to Typical

Moved to Primary

Removed from Typical

No Change in Typical

Removed from Primary

No Change in Primary

**Status bar**

Displays the currently defined colors for illustrating comparison status. You can change the color scheme by clicking the **Compare Options** button on the toolbar and defining options on the **Compare Options** dialog.

**Compare Options Dialog**

Opens when you select **Compare Options**  on the **Compare** dialog toolbar and allows you to customize the colors that the various comparison states are displayed in. The active color scheme is displayed in the **Compare** dialog status bar.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

131/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Left-only items**

Allows you to choose a color for displaying objects that exist only in the left-hand Drawing view. Dark green is the default color for this option.

**Right-only items**

Allows you to choose a color for displaying objects that exist only in the right-hand Drawing view. Red is the default color for this option.

**Different items**

Allows you to choose a color for displaying items that exist in both views but differ from each other for any number of reasons (for example, modified properties, changed connectivity, and so forth). Blue is the default color for this option.

**Default items**

Allows you to choose a color for displaying drawing items that are identical in the two views. Black is the default color for this option.

**Highlight items**

Allows you to choose a color to denote that a drawing object is highlighted, for instance, when an item is within your locate zone.

**Selected items**

Allows you to choose a color to denote items that are selected in one or both of the **Drawing** views.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

132/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Compare Drawing Versions for As-Built and Projects**

1. In the **List** view, select the drawing.
2. Select **Version History** .
3. In the drawing list on the **Version History** dialog, select the version in the active project that you want to compare against a version elsewhere.
4. Select **Compare With**.
5. On the **Compare With** dialog, select the correct target project or the Plant database from the **Available Databases** list.
6. In the **History** list, choose the version of the drawing that you want to compare against your version and select **OK**.
7. On the **Compare** dialog, you can view the differences between the two versions, but you cannot make changes to the designs. To change the design, you must use Smart P&ID. For more information about using the compare-and-refresh capabilities inside Smart P&ID, see Comparing and Refreshing Versions in *Smart P&ID Help*.

You can manipulate the views and navigate through the listed changes by using the commands on the **Compare** dialog toolbar. Each **Drawing** view also has its own shortcut menu, which includes manipulation commands that apply only to that view.

You can select an item in either **Drawing** view. The item is then located in the appropriate group in the **Change details** list. If you select an item in the **Change details** list, then you can use the **Find in** **Drawings** button on the toolbar to locate the item in one or both **Drawing** views.

You can select an item in the **Drawing** view or in the **Change details** list. Properties for that item appear in the **Properties** window. Selecting multiple items is not possible on the **Compare** dialog.

The following differences are ignored: claim status, select list strings, linked or embedded objects, symbology, and inconsistency indicators.

You can only compare a drawing against a version of itself; that is, you cannot compare one drawing to another drawing.

You can also compare versions when you are checking in a drawing. See Check In a Drawing.

If you attempt to compare two versions that are actually identical to each other, the **Compare** dialog does not open and a confirmation message alerts you as to why.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

133/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Compare With Dialog**

Opens when you select **Compare With** on the **Version History** dialog and allows you to select a drawing version from a database other than the current active database to compare against the version you choose on the **Version History** dialog in the active database.

**Available Databases**

Lists all the different databases that currently have a version of the drawing you chose on the **Version** **History** dialog.

**History**

Lists all the versions of the chosen drawing in the database you selected in the **Available Databases** list.

**Print Dialog**

Controls how a drawing is printed. This dialog opens when you select to print when viewing or comparing a drawing version.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

134/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Name**

Specifies the printer that you want to use. You can select from a list of all the available configured printers.

The information below the **Name** box applies to the selected printer. The printer that you select in the **Name** box is the default printer for the rest of the current design session until you specify a different printer.

**Properties**

Opens the **Printer Document Properties** dialog, which allows you to specify page setup and other printer settings specific to the selected printer.

**Status**

Describes the state of the selected printer, for example, busy or idle. This area is read-only.

**Type**

Displays the type of printer currently selected. This area is read-only.

**Where**

Identifies the printer path, printer port, queue name, or physical location of the currently selected printer.

This area is read-only.

**Print range**

Allows you to select the following options:

**Drawing**

Prints the entire drawing based on the defined page size.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

135/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**View**

Prints the portion of the drawing that is actually visible in the **Print Preview** window.

**Number of copies**

Allows you to specify the number of copies of the drawing to be printed.

**Collate**

When the number of copies is more than 1, selecting this check box collates the output by printing all the pages consecutively for each copy. Clearing the check box causes the same page of each copy to be printed together for the number of copies specified.

**Settings**

Opens the **Settings** dialog, which allows you to view and edit the scale and origin of your print area.

**Revising Drawings**

The software implements drawing revisions in different ways depending on your work environment. If you are working in an integrated environment, when you select the **Revisions** > **New Revision** command in Drawing Manager, the software opens either the SmartPlant Foundation **Revise** dialog or the **New** **Revision** dialog, depending on the option selected in Options Manager for the **Revision Management** **Software for Publishing Documents** setting. If you want to associate a version with a new revision in an integrated environment, you must select the drawing and run the **Revisions** > ** Associate Version** command after creating the revision.

The document revision process is separate from the publishing process, making it possible to revise a document locally and in SmartPlant Foundation and save the revision values to the tool database without re-publishing the document.

Revising a document creates a revision for the document with major and minor revision values set, depending on the revision schema selected. When revising a document, you can modify the major and minor revision data on the document.

You can change the revision scheme after a document has been published, skip revision numbers, and manually add a revision number, then have it validated against the revision scheme. It is not required to assign a minor revision number. Also, revision data from tools is supported even if the document has previously been revised in SmartPlant Foundation.

You can revise a document by using any previous revisions that are available from the last published revision.

**Example**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

136/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

If you revise a new document using the revision scheme RevAlpha (A, B, C, D…) and revision C, then SmartPlant Foundation reserves revision number C for the document. Revising the same document with RevAlpha, you can now revise with any previous revision numbers, such as A or B. However, if the document is published to SmartPlant Foundation with revision number C, you are not allowed to go back to the previous revision numbers.

The following table contains the available revision numbers based on the document revision state in SmartPlant Foundation:

**Document revision state**

**Next available revision number**

Working (C)

C and up

Current (C)

D and up

The combination of the major and minor revision values must be unique in the plant, or when working with As-Built, in the project.

When you check out or fetch a drawing from the As-Built into a project, only the last revision record is displayed in the **Revision History** dialog, regardless of whether that revision is associated with a version or not.

Deletion of revisions is allowed in a non-integrated environment. Deletion of revisions is also allowed in an integrated environment where revisions are managed by Smart P&ID, provided the revised drawing has not yet been published and regardless of any permission settings. Revision deletion is performed in the **Revision History** dialog.

**Revise Drawings Using Smart P&ID Revisions**

1. Select one or more drawings for revision.
2. Select **Revisions** > **New Revision**.

*The **New Revision** dialog displays.*

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

137/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. In the **Status** section, select a major revision number and if desired, a minor revision number.

After creation of the revisions, the drawings remain selected.

**New Revision Command (Revisions Menu)**

Opens the **New Revision** dialog, allowing you to create a new revision for the selected drawings and to enter values for the revision properties. You can also associate a version with a new revision.

If you are working in an integrated environment, when you select the **Revisions** > **New Revision** command in Drawing Manager, the software opens either the SmartPlant Foundation **Revise** dialog or the **New Revision** dialog, depending on the option selected in Options Manager for the **Revision Management** **Software for Publishing Documents** setting.

**New Revision Dialog**

Allows you to enter values of properties pertaining to the creation of a new revision that applies to one or more drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

138/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Alphabetical**

Displays drawing properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Category**

Displays drawing properties in categories. This button acts as a toggle and is available when properties are displayed alphabetically.

**(Properties and Values List**)

Displays a list of shipped properties used for the revision. You can specify additional properties for display on this dialog by defining them in the Data Dictionary Manager. Note that **Major Revision** is a mandatory property and that the combination of the **Major Revision** and **Minor Revision** values must be unique in the plant or project.

**Associate version**

Check to associate drawings. When you select **OK**, the **New Version** dialog opens, which allows you to create a new version and associate it with the revision.

**OK**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

139/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Generates the new revision, and if specified, an associated version. This command only becomes available when you enter a value for **Major Revision**.

**Revision Properties Command (Revisions Menu)**

Opens the **Revision Properties** dialog, allowing you to view and edit drawing revision properties.

**Revision Properties Dialog**

Allows you to view and edit revision properties for a drawing. This dialog opens when you select a drawing and select **Revisions** > **Revision Properties**.

**Alphabetical**

Displays drawing properties alphabetically. This button acts as a toggle and is available when properties are displayed categorically.

**Category**

Displays drawing properties in categories. This button acts as a toggle and is available when properties are displayed alphabetically.

**(Properties and Values List**)

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

140/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Displays a list of shipped properties used for the revision. You can specify additional properties for display on this dialog by defining them in the Data Dictionary Manager. Note that **Major Revision** is a mandatory property and that the combination of the **Major Revision** and **Minor Revision** values must be unique in the plant or project.

**Associate version**

This option is not available on this dialog.

**Associate Version Command**

Opens the **New Version** dialog, which allows you to associate a version with the last revision of the selected drawings. After you associate this version, it can only be deleted at the same time as you delete the revision.

**Revision History Command (Revisions Menu)**

Opens the **Revision History** dialog, which displays the revisions of the selected drawing.

**Revision History Dialog**

Lists all available revisions of a drawing.

**History**

Lists all the revisions of the drawing in the current plant or project. Note that when you check out or fetch a drawing from As-Built into a project, only the last revision record is displayed on this dialog, regardless of whether that revision is associated with a version or not.

**Major Revision**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

141/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Indicates the number or other designation of the major revision. This is a required property, so a value will always appear in this column.

**Minor Revision**

Indicates the number or other designation of the minor revision. This is not a required property, so a value may or may not appear in this column.

**Revision Date**

Shows the date on which the revision was created.

**Approved By**

Shows the name of the person who approved the revision.

**Created By**

Shows the name of the user who created the revision.

**Checked By**

Shows the name of the person who checked the revision.

**Properties**

Opens the **Revision Properties** dialog, allowing you to view or edit all of the revision properties.

**Associate Version**

Opens the **New Version** dialog, allowing you to create and associate a new version with this revision. This option is only available for the last revision.

**Delete**

Removes the selected drawing revision. To be able to delete revisions, you must have appropriate permissions assigned in Smart Engineering Manager.

Deletion of revisions is allowed in a non-integrated environment. Deletion of revisions is also allowed in an integrated environment where revisions are managed by Smart P&ID, provided the revised drawing has not yet been published and regardless of any permission settings; once the drawing is published, this command is disabled.

If the revision has an associated version, the software deletes the version together with the revision.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

142/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Saving Drawings**

You can save drawings in the following formats:

AutoCAD (*.dwg and *.dxf)

MicroStation (*.dgn)

PDF (*.pdf)

ISO 15926 (*.xml)

Smart P&ID uses the ExportLayer.xlsx file to map drawing item types to the layers that they will be assigned to. Filters are used to define the scope of the item type, for example ‘Equipment - New’. The file then specifies the layer to which the scoped item type will be assigned. If a symbol’s item type does not match any of the filter definitions and if that symbol is in the Primary drawing layer (the only active layer when saving from Drawing Manager), the symbol is saved in the Default layer. If a display set is assigned to the drawing and the **Color** value of filtered or background items is **None**, the software ignores the ExportLayer.xlsx file and those items go to the hidden layer in AutoCAD or MicroStation. If the **Color** value of filtered or background items is not **None**, filtered items go to the layer specified by the filter and background items go to the default layer unless a filter exists in the ExportLayer.xlsx file for a particular item or set of items, in which case the settings in the ExportLayer.xlsx file override the display set settings for those background items.

For details of the supported versions of AutoCAD and MicroStation for these formats, refer to the Smart P&ID * Installation and Upgrade Guide*,* Hardware and Software Recommendations* under the section Smart P&ID * Workstation* > *Optional Software*. The PDF printer that the current version of the software supports is Amyuni 5.5 PDF Converter.

The ISO 15926 (*.xml) format is available only if you have a valid license ID and you have run a

procedure that activates this option. For details, see Enable Save As XML.

Text boxes on drawings that are saved as AutoCAD drawings display a border if the fill color **Blank** is selected in the **Text Block Properties**. To remove the border around text boxes in translated AutoCAD drawings, modify the P&ID symbol in Catalog Manager and set the **Text Block Properties** fill color to **None**.

**Save Drawings in Other Formats**

1. Under **Name** containing the list of drawings, select one or more drawings. Use the SHIFT or CTRL key to select multiple drawings.
2. Select **File** > **Save As**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

143/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. On the **Save As** dialog, do one of the following:

For a single drawing, in the **File path** field, type the path where you want to save the files, or select **Browse** to open the **File Name and Path** window to navigate to the desired path.

For multiple drawings, in the **Folder path** field, type the path to an existing folder where you want to save the files, or select **Browse** to open the **Browse for Folder** dialog to navigate to the desired folder.

1. From the **Save as type** list, select one of the following formats: AutoCAD (*.dwg and *.dxf)

MicroStation (*.dgn)

PDF (*.pdf)

ISO 15926 (*.xml)

The value of the **Override Layers on Export** attribute in the pidacad.ini file affects the output when saving a file as AutoCAD. If symbols are exported as blocks (when the value of the **Dissolve Symbol** **to Groups** attribute is set to 0), you must specify a value of 2 or 3 for the **Override Layers on Export** attribute to ensure that the blocks are exported to the correct AutoCAD layer. For full details of the **Override Layers on Export** attribute, see Configuration File Settings for AutoCAD Translation.

The ISO 15926 (*.xml) format is available only if you have a valid license ID and you have run a

procedure that activates this option. For details, see Enable Save As XML.

Text boxes on drawings that are saved as AutoCAD drawings display a border if the fill color **Blank** is selected in the **Text Block Properties**. To remove the border around text boxes in translated AutoCAD drawings, modify the P&ID symbol in Catalog Manager and set the **Text Block Properties** fill color to **None**.

When you save a drawing in .dwg format, the text labels appear in low-resolution due to the changes made to the text width factor in RAD.

When saving a drawing to AutoCAD with SmartFrame objects such as auxiliary graphics, you must do the following to prevent a border showing around such objects: 1. In the Smart P&ID installation folder path *..\Program Files (x86)\SmartPlant\P&ID*

*Workstation\bin*, select the pidacad.dwg seed file and copy it to a location where you have write permissions.

1. Launch AutoCAD and open the copied pidacad.dwg file.
2. Under **System Variables**, set the value of the **FRAME** variable to **0**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

144/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Save the change to update the pidacad.dwg file.
2. Copy the pidacad.dwg file back to the bin folder in the Smart P&ID installation path.

When saving to AutoCAD or MicroStation, to use a display set to filter the layers to which the drawing items are sent, do the following:

1. Under **Save filter**, select **Apply display set**.
2. Beside the **Active display set** field, select **Browse** to open the **Apply Display Set** dialog.
3. Select a display set.

When saving to AutoCAD or MicroStation, the software checks the ExportLayer.xlsx file and if it finds a reference to a filter that does not exist in the reference data, a **Filters Not Found** dialog is displayed showing a list of missing filters. When you select **Exit** to dismiss the dialog, the save as process stops.

When saving to AutoCAD or MicroStation using a display set, the software uses the ExportLayer.xlsx file only for filtering items that do not meet any of the display set filter criteria and for which the **Color** value of filtered or background items is not **None**.

The dependent behavior of drawing items on the color value of display sets is as follows: **Color Value**

**Effect on Filtered Items**

**Effect on Background Items**

Specific color

Layer is created with name of

Items are mapped according to filters in the

display set filter and filtered items go ExportLayer.xlsx file. Colors specified by to that layer with the color specified the display set filter are ignored for items by the display set filter. If **Override**

mapped to layers that appear in

**Layers on Export** = **2** in the

ExportLayer.xlsx, and the colors of those

pidacad.ini or pidmstn.ini file, the

items are assigned according to the

color from the seed file overrides the **Override Layers on Export** setting. Items display set filter color for the

sent to the Default layer are assigned the

particular layer.

background items color from the display

set.

Default

Layer is created with name of

Items are mapped according to filters in the

display set filter and filtered items go ExportLayer.xlsx file. Color is assigned to that layer with the default color

according to **Override Layers on Export**

specified in Options Manager. If

setting.

**Override Layers on Export** = **2**, the

color from the seed file overrides the

default color for the particular layer.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

145/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

None

Items are sent to the HiddenObjects Items are sent to the HiddenObjects layer layer and the ExportLayer.xlsx file

and the ExportLayer.xlsx file settings are

settings are ignored.

ignored.

When saving to AutoCAD, extra layers such as ConsistencyChecks, HeatTrace, HiddenObjects, Labels, and others may be created on your AutoCAD drawing. To delete one of these layers, you must add a row to the ExportLayer.xlsx file and enter the name of the layer in the **Filter** column and the value **-9999** in the **Layer** column as shown:

For a display set that contains one or more asking filters, on clicking **OK** in the **Save As** dialog box, the **Asking Filters** dialog box opens with the default values for each asking filter, allowing you to change the operators and values of each asking filter’s attributes for the selected drawings, if desired.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

146/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When saving a drawing as PDF, update the out-of-date drawings to save the latest changes in the PDF.

When saving as PDF, select **PDF Settings** to open the **PDF Settings** dialog, where you can specify the resolution, color mode, JPEG compression, and whether or not to include inconsistency markers in the output

**Enable Save As XML**

This procedure explains how to enable the **ISO 15926 (*.xml)** option on the list of formats when using the **Save As** command in Drawing Manager.

You must have a valid license ID to perform this procedure successfully. To obtain a license and receive the license ID for the Smart P&ID ISO 15926 Export Utility, contact your local Intergraph Sales Representative.

The file PlantConfig.xml must be located in the Smart P&ID Reference Data folder. This file contains the mapping of the symbology and Heat Trace media line types between Smart P&ID and ISO 15926.

If a line style is undefined in the mapping, Smart P&ID lines appear by default in the ISO output as

‘solid’. To change the mapping default for an undefined line style, edit the following line in the file:

1. At the command prompt, type the full path of the Drawing Manager executable file, for example: c:\Program Files (x86)\SmartPlant\P&ID

Workstation\bin\DrawingManagerEXE.exe.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

147/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Add a space after the path and copy the license ID provided to you after the space.
2. Run the command to open Drawing Manager. The ‘Save as’ formats will include the **ISO 15926 (*.xml)** option as enabled.

To enable this option whenever Drawing Manager is opened, create a shortcut that includes the full path to the executable file and the license ID, and use this shortcut to start Drawing Manager.

**Configuration File Settings for AutoCAD Translation**

The configuration file, pidacad.ini, is used by translators and provides the capability for customizing the process of translation between the software and an AutoCAD document. The options shown here should be changed only by experienced users at their own risk.

Text boxes on drawings that are saved as AutoCAD drawings display a border if the fill color **Blank** is selected in the **Text Block Properties**. To remove the border around text boxes in translated AutoCAD

drawings, modify the P&ID symbol in Catalog Manager and set the **Text Block Properties** fill color to **None**.

**Options**

**Name of Setting**

**Description**

**Import**

**Export**

**Default Value**

**Accepted Values**

**Seed File**

Name of a seed file used

No

Yes

pidacad.dwg

Filename

for export (not

mandatory).

**Enable Logging**

If set, a log file wil be

Yes

Yes

0

0 = Logging is turned OFF

created in the directory

that the file was opened

1 = Logging is turned ON

from and wil have the

same name as the file

that was opened.

**Read Default Units**

Sets the default units for

Yes

No

64

59=m; 61=mm; 62=cm; 63=km;

foreign format. Because

64=in; 65=ft; 66=yd; 67=miles

.dwg is a unit-less file

format, the **Read Default**

**Units** setting is used to

determine the unit

settings.

**Template File**

Sets the document that

Yes

No

TransAcad.igr

Filename

wil be used as a template

when importing foreign

(If this file is required, it can

be taken from the

data for setting up

hatching and patterns.

SmartSketch folder)

**Symbol Template File**

Sets the symbol file that

Yes

No

Filename

wil be used as a template

when importing foreign

data.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

148/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Override Layers on Export**

Determines which

No

Yes

3

0 – Translation honors seed file

settings AutoCAD

settings and sends blocks to the

translation honors to

Default layer. ByLayer=7 is needed

include visibility, locks,

to display the colors correctly.

color, linetype, and

lineweight for duplicate

1 – Translation honors Smart P&ID

layers.

settings and sends blocks to the

Default layer.

Any layer specified in the

seed file wil be

2 – Translation honors seed file

generated in the

settings and sends blocks to the

AutoCAD drawing

specified layer. ByLayer=7 is needed

regardless of this setting

to display the colors correctly.

or whether the layer

3 – Translation honors Smart P&ID

contains any objects.

settings and sends blocks to the

specified layer.

**ByLayer**

Used with **Override**

No

Yes

7

7

**Layers on Export** setting

for values 0 and 2.

**Ignore Sheet Scale**

Determines whether to

Yes

No

1

0 = Do not fit the graphics to the

scale the sheet to fit the

sheet

graphics during a

translation import.

1 = Fit the graphics to the sheet

**Attribute Sets**

Controls the import /

Yes

Yes

TranslationSettings

String consisting of attribute names

export of attribute

delimited by semicolons, or the ALL

information on objects

keyword

during translation.

**Read Block Options**

Sets how the blocks

Yes

No

Shared Embeds

Shared Embeds - Preserves blocks

imported from AutoCAD

Rigid Groups - Translates blocks into

are handled.

groups

**Write Version**

Sets the version of the

No

Yes

2018

2000; 2002; 2004; 2005; 2006;

foreign file format that is

2007; 2008; 2009; 2012; 2018

created on export.

**Read Reference Options**

Specifies options to

Yes

No

Translate; Link; Merge

process reference files

during translation.

**Read Default Width**

Sets the width to be

Yes

No

## 0.25 mm

### mil imeters

assigned to al AutoCAD

entities that do not have

width or color to width

mapping.

**Write Polyline Width Threshold**

Sets the width to

No

Yes

## 10.000000

### determine when polylines

with width must be

created.

**Dissolve Symbol to Groups**

Controls the export of

No

Yes

0

0 = Symbols are exported as blocks

SmartSketch symbols to

blocks or to groups of

1 = Symbols are dissolved into their

individual objects.

individual components

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

149/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Export All Graphics to**

Displays reference data

No

Yes

2

0 = Al graphic objects are exported

**PaperSpace**

contained in SmartSketch

to Model space. SmartFrames with

SmartFrames on the

clipping boundaries do not display

AutoCAD PaperSpace

properly and detail views are

sheet during a translation

ignored.

export.

1 = Al graphic objects are exported

into the Paper space. SmartFrames

with clipping boundaries display

properly. Detail views are ignored.

2 = Al graphic objects are exported

to Modelspace and Paper space is

populated so that the original

SmartSketch sheet is re-created.

**Process Multiple Orientation in**

Indicates whether to

Yes

No

0

0 = OFF

**Viewports**

handle multiple

orientations in viewports.

1 = ON

**Max. Nesting Depth**

Refers to the depth that

Yes

No

0

- 1 = Process ALL nested reference

reference files (inserted

files

via the **Insert** > **Object**

menu command) wil be

0 = Process NO nested reference

processed for displaying

files

and locating. This setting

n = Process nested reference files

does not apply to

up to n levels deep, where n is an

reference files in foreign

integer between 1 and 9

data files that are

translated in via the **File** >

**Open** command or to

reference files in

SmartSketch drawings

that are translated to a

foreign format via the **File**

> Save As command.
> 

**Application Text Type**

Determines whether text

Yes

Yes

1

0= Text origin always in upper left

origin and justification are

corner

preserved.

1= Origin preserved

**Single Text Alignment**

Determines the horizontal Yes

No

0

0 = Horizontal text alignment is set

alignment of text.

to **Horizontal Justification**

1 = Horizontal text alignment is set

to **Left**

**Process Non- Displayable**

Determines whether non- Yes

Yes

1

0 = OFF

**Reference Files**

displayable reference

files are translated.

1 = ON

**Attributes as Smart Text**

Determines whether

Yes

No

0

0 = Attributes are created as text

attributes are created as

boxes

simple text boxes or

SmartLabels during

1 = Attributes are created as

translation import.

SmartLabels

**AutoCAD Extended Data**

Sets the XData to be

Yes

No

ACADASE

String consisting of XData names

imported.

delimited by semi- colons

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

150/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Stroke Reference**

Determines whether

No

Yes

0 = OFF

attached reference files

are stroked on export.

1 = ON

**Stroke Text**

Determines whether text

No

Yes

0

0 = OFF

is stroked on export.

1 = ON

**Stroke Dimension**

If set, the dimension

No

Yes

1

0 = OFF

objects are stroked on

export.

1 = ON

**Disk-based Symbols**

Controls whether to leave Yes

No

0

0 = Do not leave symbols on the disk

symbol files that are

created for AutoCAD

1 = Leave symbols on the disk

blocks on the disk when

performing a translation

import.

**Ignore Non-Displayable Symbols** Controls whether to

Yes

Yes

0

0 = Do not include non-displayable

include non-displayable

objects

objects on import or

export.

1 = Include non-displayable objects

**Preserve Layers on Dissolved**

Controls the export of

No

Yes

0

0 = Do not translate objects in

**Symbols**

elements contained by a

symbols when the objects’ layers are

Symbol whose layer is

not displayed

turned off. If the setting is

ON, then al objects in a

1 = Translate al objects in symbols

symbol wil be translated

whether or not layers are displayed

whether their layer

display is turned on or

not. This can result in

non-WYSIWYG

translation. This setting is

relevant only if the value

of the **Dissolve Symbol**

**to Groups** setting is 1.

**Push Owner Attributes to its**

If set to 1, RAD dynamic

No

Yes

0 = Attributes are NOT created on

**Children**

attributes are moved from

children of owner objects

a group (symbol) to its

members.

1 = Attributes are created

**Metafile to Raster DPI**

Sets the dpi resolution for No

Yes

350

dpi resolution (1 through 1200)

**Resolution**

raster metadata during

export.

**Stroking Tolerance**

Determines the accuracy

No

Yes

## 0.1 mm

### mil imeters

used when objects are

stroked during export.

**Hatch Supported Complexity**

Supported Hatch

No

Yes

3

1 (only supports a single

complexity of output

independent hatch line with dashes

format.

and gaps)

**Need Hatch Description and**

If true, then stroke hatch

No

Yes

1

0/1

**Stroke**

even when hatch name

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

151/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

and description are

included in symbology.

**Delete Symbol Definitions**

Controls what happens to Yes

No

1

0 = Do not delete symbol definitions

the symbol definitions

after translation.

1 = Delete symbol definitions

**Process PaperSpace**

Controls whether to

Yes

No

1

0 = Processing PaperSpace is

process the PaperSpace

turned OFF regardless of the last

sheet in an AutoCAD file

saved space in the AutoCAD file

if the file was last saved

with a PaperSpace layout

1 = Processing PaperSpace is

as the active tab.

turned ON

This setting

has no effect if the model

space tab was the active

tab when the AutoCAD

file was last saved.

**Bigfont Name**

Name of the AutoCAD

No

Yes

Filename

font file with Asian

characters.

**Write DXF Precision**

Controls the number of

No

Yes

6

1 through 16

decimal places that are

used during a translate

DXF export.

**Export Internal Attributes**

Controls whether attribute No

Yes

1

0 = Do not export attribute sets

sets wil be exported.

This setting takes

1 = Export attribute sets

precedence over the

**Attribute Sets** setting.

**Merge References**

Controls whether files of

No

Yes

2

0 = Save inserted igr, .dwg, .dgn,

type .igr, .dwg, .dgn, and

and .dxf files as separate .dwg files

.dxf that were inserted

into a drawing are

1 = Merge inserted files using BIND.

merged into the main

Creates a duplicate set of styles for

.dwg file when saving to

each block reference.

AutoCAD. Inserted Office

2 = Merge inserted files using

documents are translated

INSERT. Creates a single set of

to .tiff file format.

unique styles for the main drawing

Regardless of the setting

and al block references.

value, objects with .tiff or

.jpg format are not

merged and need to be

kept in the same folder as

the .dwg file in order to

display correctly.

Note that for a main

drawing saved as a .dxf

file with objects in .tiff

format, when the files are

copied to a new location,

AutoCAD cannot find

them due to the reference

to an exact location, even

if they are in the same

location as the .dxf file. To

rectify this, the path to the

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

152/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

.tiff file needs to be

updated manual y in the

.dxf file.

**Clipping Boundary Growth**

Extends the boundary of

No

Yes

## 0.1

### Numeric values

SmartFrames (including

drawing template

borders) by the quantity

shown to avoid clipping

when graphics are on the

boundary. The units of

measure are taken from

the **Unit** value under

**Length readout** on the

**Units** tab of the drawing

properties which are

accessed using the **File** >

**Properties** command in

Smart P&ID.

**Write Linestyles**

Many of the default linestyles in your document are pre-mapped to the most equivalent AutoCAD linestyles.

Other linestyles are mapped as continuous. If the _default_ = _stroke_ setting is used, all linestyles are stroked regardless of their mapping. The _default_ = _stroke_ setting is commented out by default to disable it.

The number values are used in the linestyle table to map linestyle definitions in the current document to AutoCAD line types.

**Number**

**Definition**

**9**

CONTINUOUS

**10**

HIDDEN2

**11**

DOT2

**12**

DASHDOT2

**13**

DIVIDE2

**18**

CENTER2

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

153/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**19**

CENTER

**20**

PHANTOM2

**21**

BORDER2

**23**

CONTINUOUS

The following table shows the Signal Run linestyles as they appear in the software and in AutoCAD.

**Software**

**AutoCAD**

Capillary

=

CAPILLARY

Electric

=

ELECTRIC

Electric Binary

=

ELECTRIC_BINARY

Guided Electromagnetic

=

ELECTROMAGNETIC

Hydraulic

=

HYDRAULIC

Connect To Process

=

CONTINUOUS

Mechanical Link

=

MECHANICAL_LINK

Pneumatic

=

PNEUMATIC

Pneumatic Binary

=

PNEUMATIC_BINARY

Software

=

SOFTWARE_LINK

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

154/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Data Link

=

SOFTWARE_LINK

Undefined

=

UNDEFINED

Unguided Electromagnetic

=

UNGUIDED_ELECTROMAGNETIC

_default_

=

_stroke_

The following table shows the revision cloud linestyles as they appear in the software and in AutoCAD.

**Software**

**AutoCAD**

Cloud Large

=

CLOUDLARGE

Cloud Small

=

CLOUDSMALL

**Configuration File Settings for MicroStation Translation** The configuration file, pidmstn.ini, is used by translators and provides the capability for customizing the process of translation between the software and a MicroStation document. The options shown here should be changed only by experienced users at their own risk.

**Options**

**Name of Setting**

**Description**

**Import**

**Export**

**Default Value**

**Accepted Values**

**Seed File**

The Working Units of the

No

Yes

pidmstn.dgn

Filename

seed file that is specified

by this setting determines

the Working Units of the

resulting DGN file. If the

Master Units of the

specified seed file are not

a standard recognized

unit, then the Length

Readout Unit of the IGR

file (specified on the **File**

**Properties** dialog) is

used for the Master Units

of the resulting DGN file.

If the Length Readout

Unit contains Sub Units,

such as ft – in, the Sub

Units wil also be taken

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

155/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

from the Length Readout

Unit. If the Length

Readout Unit does not

contain Sub Units, the

Sub Units wil be taken

from the specified seed

file.

This setting is optional for

the current MicroStation

version.

**Enable Logging**

If set, a log file wil be

Yes

Yes

0

0 = Logging is turned OFF

created in the directory

that the file was opened

1 = Logging is turned ON

from and wil have the

same name as the file

that was opened.

**Read Default Units**

If the MicroStation file

Yes

No

64

59=m; 61=mm; 62=cm; 63=km;

being imported does not

64=in; 65=ft; 66=yd; 67=miles

have a master unit setting

that matches one of the

default SmartSketch unit

settings, then this setting

is used to specify the

units being imported. If

the MicroStation file being

imported does have a

valid master unit setting

that matches a default

SmartSketch unit setting,

then this setting is

ignored.

**Template File**

Sets the document that

Yes

No

TransMstn.igr

Filename

wil be used as a template

when importing foreign

(If this file is required, it can

data for setting up

be taken from the

hatching and patterns.

SmartSketch folder)

**Symbol Template File**

Sets the symbol file that

Yes

No

Filename

wil be used as a template

when importing foreign

data.

**Ignore Sheet Scale**

Determines whether to

Yes

No

1

0 = Do not fit the graphics to the

scale the sheet to fit the

sheet

graphics during a

translation import.

1 = Fit the graphics to the sheet

**Attribute Sets**

Controls the import /

Yes

Yes

TranslationSettings;

String consisting of attribute names

export of attribute

_SymInst

delimited by semicolons, or the ALL

information on objects

keyword

during translation.

**Write Version**

Sets the version of the

No

Yes

## 8.0

### 7.0; 8.0

foreign file format that is

created on export.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

156/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Read Reference Options**

Specifies options to

Yes

No

Translate; Link; Merge

process reference files

during translation.

**Write Polyline Width Threshold**

Sets the width to

No

Yes

## 10.000000

### determine when polylines

with width must be

created.

**Dissolve Symbol to Groups**

Controls the export of

No

Yes

0

0 = Symbols are exported as shared

SmartSketch symbols to

cel s

cel s or to groups of

individual objects.

1 = Symbols are exported as type 2

cel s to control the graphics level

To implement this

behavior, you must also assign to

the **Attribute Sets** option the value

‘TranslationSettings; _SymInst’;

otherwise, when the value of

**Dissolve Symbol to Groups** is set

to 1, symbols are exported as

individual objects

**Override Background Color**

Overrides the background No

Yes

1

0 = Override is turned OFF

color specified in the

MicroStation seed file

1 = Override is turned ON

during a translation

export, by using the

SmartSketch sheet color.

**Process Multiple Orientation in**

Indicates whether to

Yes

No

0

0 = OFF

**Viewports**

handle multiple

orientations in viewports.

1 = ON

**Max. Nesting Depth**

Refers to the depth that

Yes

No

0

- 1 = Process ALL nested reference

reference files (inserted

files

via the **Insert** > **Object**

menu command) wil be

0 = Process NO nested reference

files

processed for displaying

and locating. This setting

n = Process nested reference files

does not apply to

up to n levels deep, where n is an

reference files in foreign

integer between 1 and 9

data files that are

translated in via the **File** >

**Open** command or to

reference files in

SmartSketch drawings

that are translated to a

foreign format via the **File**

> Save As command.
> 

**Application Text Type**

Determines whether text

Yes

Yes

1

0= Text origin always in upper left

origin and justification are

corner

preserved.

1= Origin preserved

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

157/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Single Text Alignment**

Determines the horizontal Yes

No

0

0 = Horizontal text alignment is set

alignment of text.

to **Horizontal Justification**

1 = Horizontal text alignment is set

to **Left**

**Process Non- Displayable**

Determines whether non- Yes

Yes

1

0 = OFF

**Reference Files**

displayable reference

1 = ON

files are translated.

**Process Construction Elements**

Determines whether

Yes

No

0

0 = Do not translate elements

elements on a

MicroStation construction

1 = Translate elements

layer are translated.

**Attributes as Smart Text**

Determines whether

Yes

No

0

0 = Attributes are created as text

attributes are created as

boxes

simple text boxes or

SmartLabels during

1 = Attributes are created as

SmartLabels

translation import.

**Stroke Reference**

Determines whether

No

Yes

0 = OFF

attached reference files

are stroked on export.

1 = ON

**Stroke Text**

Determines whether text

No

Yes

0

0 = OFF

is stroked on export.

1 = ON

**Stroke Dimension**

If set, the dimension

No

Yes

1

0 = OFF

objects are stroked on

export.

1 = ON

**Disk-based Symbols**

Controls whether to leave Yes

No

0

0 = Do not leave symbols on the disk

symbol files that are

created for MicroStation

1 = Leave symbols on the disk

cel s on the disk when

performing a translation

import.

**Ignore Non-Displayable Symbols** Controls whether to

Yes

Yes

0

0 = Do not include non-displayable

include non-displayable

objects

objects on import or

export.

1 = Include non-displayable objects

**Preserve Layers on Dissolved**

Controls the export of

No

Yes

0

0 = Do not translate objects in

**Symbols**

elements contained by a

symbols when the objects’ layers are

Symbol whose layer is

not displayed

turned off. If the setting is

ON, then al objects in a

1 = Translate al objects in symbols

symbol wil be translated

whether or not layers are displayed

whether their layer

display is turned on or

not. This can result in

non-WYSIWYG

translation. This setting is

relevant only if the value

of the **Dissolve Symbols**

**to Group** setting is 1.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

158/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Preserve MSTN UDLS Styles**

Determines whether to

No

Yes

0 = User-defined linestyles are

preserve user-defined

stroked

linestyles.

1 = User-defined linestyles are

preserved

**Push Owner Attributes to its**

If set to 1, RAD dynamic

No

Yes

0 = Attributes are NOT created on

**Children**

attributes are moved from

children of owner objects

a group (symbol) to its

members.

1 = Attributes are created

**Metafile to Raster DPI**

Sets the dpi resolution for No

Yes

350

dpi resolution (1 through 1200)

**Resolution**

raster metadata during

export.

**Stroking Tolerance**

Determines the accuracy

No

Yes

## 0.1 mm

### mil imeters

used when objects are

stroked during export.

**Hatch Supported Complexity**

Supported Hatch

No

Yes

3

1 (only supports a single

complexity of output

independent hatch line with dashes

format.

and gaps)

**Need Hatch Description and**

If true, then stroke hatch

No

Yes

1

0/1

**Stroke**

even when hatch name

and description are

included in symbology.

**Delete Symbol Definitions**

Controls what happens to Yes

No

1

0 = Do not delete symbol definitions

the symbol definitions

after translation.

1 = Delete symbol definitions

**Export Internal Attributes**

Controls whether attribute No

Yes

1

0 = Do not export attribute sets

sets wil be exported.

This setting takes

1 = Export attribute sets

precedence over the

**Attribute Sets** setting.

**Read Cell Options**

Sets how the shared

Yes

No

Shared Embeds

Shared Embeds - Preserves shared

(type 34/35) cel s

cel s

imported from

MicroStation are handled.

Rigid Groups - Translates shared

cel s into groups

**Sub Units Per Master Units**

Sets the values to

Yes

No

10

Numeric

determine the size of

units for a MicroStation

cel .

**Pos Units Per Sub Units**

Sets the values to

Yes

No

1000

Numeric

determine the size of

units for a MicroStation

cel file

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

159/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Always Shift GO to Center**

Controls whether to set

No

Yes

0

0 = Do NOT shift the Global Origin of

**Drawing**

the Global Origin of .dgn

the resulting .dgn file

files in case the drawing

objects fal outside the

1 = Shift the Global Origin of the

maximum design plane

resulting .dgn file

as defined by

MicroStation.

**EDF as Smart Text**

Determines whether the

Yes

No

0

0 = Tags are created as text boxes

values of tags are created

as simple text boxes or

1 = Tags are created as SmartLabels

as SmartLabels during

translation import.

**Write Linestyles**

The default linestyles in your document are pre-mapped to the most equivalent MicroStation linestyles.

Linestyles other than the default linestyles or any complex linestyles containing shapes are mapped to continuous unless they are specifically mapped on the Linestyle tab. Linestyles that are not mapped on export are stroked to give them a more correct appearance. The default length of the stroking line is 0.1

millimeters (mm).

The number values are used in the linestyle table to map linestyle definitions in the current document to MicroStation line types.

**Number**

**Definition**

**9**

0

**10**

2

**11**

1

**12**

4

**13**

6

**18**

7

**20**

6

The following table shows the Signal Run linestyles as they appear in the software and in MicroStation.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

160/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Software**

**MicroStation**

Capillary

=

Capillary

Electric

=

Electric

Electric Binary

=

Electric_binary

Guided electromag/sonic

=

Guided Electromag/Sonic

Hydraulic

=

Hydraulic

Connect To Process

=

Connect To Process

Mechanical Link

=

Mechanical Link

Pneumatic

=

Pneumatic

Pneumatic Binary

=

Pneumatic Binary

Software Link

=

Software Link

Undefined

=

Undefined

Unguided Electromagnetic

=

Electromag/Sonic

_default_

=

_stroke_

The following table shows the revision cloud linestyles as they appear in the software and in MicroStation.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

161/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Software**

**MicroStation**

Cloud Large

=

CLOUDLARGE

Cloud Small

=

CLOUDSMALL

In addition to the above mapping, the PIDLineStylesV8.rsc file, delivered in the folder path *..\Program Files* *(x86)\SmartPlant\P&ID Workstation\bin*, must be copied to the MicroStation installation folder: *C:\ProgramData\Bentley\WorkSpace\System\Symb*.

The following table shows the Tracing Media linestyles as they appear in the software and in MicroStation.

**Software**

**MicroStation**

NT

=

NT

E

=

E

FA

=

FA

FB

=

FB

FC

=

FC

I

=

I

MI

=

MI

SKE

=

SKE

SH

=

SH

SL

=

SL

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

162/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

SM

SM

SN

=

SN

SS

=

SS

ST

=

ST

**Save As Command (File Menu)**

Allows you to save the selected drawings in a specified file format. You can select a single drawing or multiple drawings (by holding the SHIFT or CTRL key) before running this command.

**Save As Dialog**

Allows you to save the selected drawing in a specified file format. See Save Drawings in Other Formats.

AutoCAD (*.dwg and *.dxf)

MicroStation (*.dgn)

PDF (*.pdf)

ISO 15926 (*.xml)

For details of the supported versions of AutoCAD and MicroStation for these formats, refer to the Smart P&ID * Installation and Upgrade Guide*,* Hardware and Software Recommendations* under the section Smart P&ID * Workstation* > *Optional Software*. The PDF printer that the current version of the software supports is Amyuni 5.5 PDF Converter.

When you save a drawing in .dwg format, the text labels appear in low-resolution due to the changes made to the text width factor in RAD.

When saving a drawing as PDF, update the out-of-date drawings to save the latest changes in the PDF.

The ISO 15926 (*.xml) format is available only if you have a valid license ID and you have run a

procedure that activates this option. For details, see Enable Save As XML.

**PDF Settings**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

163/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

(Available only when **PDF** is selected in the **Save as type** list.) Opens the **PDF Settings** dialog to specify settings for the PDF output.

**Save filter**

**Apply display set**

Select this check box to enable selection of a display set to specify the layers to which drawing items go when saving to AutoCAD or MicroStation formats. Clear the check box to ignore display set settings.

**Active display set**

This field becomes active when you select **Apply display set**. Click **Browse** to open the **Apply Display** **Set** dialog box from which you choose the desired display set.

If an active display set is already selected for the drawing, this dialog opens with the **Apply display** **set** check box selected and the relevant display set appears in the **Active display set** field.

**About ISO 15926**

(Available only when **ISO 15926 (*.xml)** is selected in the **Save as type** list.) Opens an **About** dialog that displays version and licensing information for the Smart P&ID Modeler ISO 15926 Export Utility.

**Save As Dialog Box (Multiple Drawings Selected)**

Allows you to save a batch of selected drawings in a specified file format.

**Save options**

**Folder path**

Allows you to type the path to an existing folder where you want to save the drawings. You can also select **Browse** to navigate to the desired folder.

**Save as type**

Allows you to select a file format for the drawings you want to save (see Save Drawings in Other Formats).

The following formats are available:

AutoCAD (*.dwg and *.dxf)

MicroStation (*.dgn)

PDF (*.pdf)

ISO 15926 (*.xml)

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

164/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

For details of the supported versions of AutoCAD and MicroStation for these formats, refer to the Smart P&ID * Installation and Upgrade Guide*,* Hardware and Software Recommendations* under the section Smart P&ID * Workstation* > *Optional Software*. The PDF printer that the current version of the software supports is Amyuni 5.5 PDF Converter.

When saving a drawing as PDF, update the out-of-date drawings to save the latest changes in the PDF.

The ISO 15926 (*.xml) format is available only if you have a valid license ID and you have run a

procedure that activates this option. For details, see Enable Save As XML.

**PDF Settings**

(Available only when **PDF** is selected in the **Save as type** list.) Opens the **PDF Settings** dialog to specify settings for the PDF output.

**Save filter**

**Apply display set**

Select this check box to enable selection of a display set to specify the layers to which drawing items go when saving to AutoCAD or MicroStation formats. Clear the check box to ignore display set settings.

**Active display set**

This field becomes active when you select **Apply display set**. Click **Browse** to open the **Apply Display** **Set** dialog box from which you choose the desired display set.

The display set chosen from the **Active display set** field is the one used to specify the layers for all selected drawings and this overrides any active display sets that were selected for individual drawings.

**About ISO 15926**

(Available only when **ISO 15926 (*.xml)** is selected in the **Save as type** list.) Opens an **About** dialog that displays version and licensing information for the Smart P&ID Modeler ISO 15926 Export Utility.

**PDF Settings Dialog**

Defines the output settings when saving drawings to PDF documents.

**Resolution**

Modifies the dots per inch, or “dpi”. The greater the dpi, the better the clarity. Increasing the resolution setting increases the file size and can slightly increase the time required to process some files.

**Color options**

**Color**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

165/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Creates a PDF using the colors available in the document. You can only create a color PDF from a color drawing sheet.

**Grayscale**

Creates a PDF using a 256-color grayscale.

**Pure black and white**

Creates a PDF that has no color or grayscale. Anything that is not pure white is drawn as black.

**JPEG compression**

Compresses images embedded in your document according to the compression level you define. If your drawing contains a lot of images, compression settings are very important for achieving good image quality at a manageable file size. Use the pull-down menu to set the compression level. Compression levels in the **High quality** range do not noticeably affect image quality, and produce larger file sizes than settings in the **Low quality** range. However, using a mid-range compression level usually strikes the best balance in creating a compact file while still maintaining enough information to produce high-quality images.

**Include inconsistency markers**

When selected, includes inconsistency symbols that appear on the drawing in the PDF output.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

166/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Printing Multiple Drawings**

Rather than printing drawings one-by-one from within Smart P&ID, Drawing Manager allows you to print more than one drawing at a time. You can select drawings from multiple plant groups for printing and you can specify for the entire group of selected drawings printing options such as whether to display a watermark, whether to print inconsistency markers, and drawing orientation. In Drawing Manager, you also have the capability to schedule batch printing for a later time or at regular intervals by using the **Schedule** option on the **Print** dialog.

While it is possible to print just one drawing at a time from Drawing Manager, the Drawing Manager **Print** command does not have all the single-print capabilities of the **Print** command in the Smart P&ID Modeler.

For instance, Drawing Manager only prints an entire drawing; whereas, in the Smart P&ID Modeler, you may choose to print only a selection or a view inside a drawing.

When filtering by typicals or display sets to determine which drawings are to be printed, you can specify whether to include or exclude in the printout drawings that do not contain filtered items.

In the Smart P&ID Modeler, you can control the display and print output of the drawing using the settings under the **Select** section on the **Display** tab of the **View Properties** dialog. The check box options affect the way that inserted objects are printed from the Smart P&ID Modeler and also from Drawing Manager. When **Prevent selection of inserted objects** is selected on its own, inserted objects and Auxiliary Graphics are printed in gray. If **Retain Auxiliary Graphics colors** is selected, any Auxiliary Graphics included in the drawing are printed in color. If **Print inserted objects in color** is selected, any inserted or linked objects and Auxiliary Graphics are printed in color. If **Print inserted** **objects in color** is not selected then the inserted objects print as displayed in the drawing.

**Print Dialog**

Controls how a drawing is printed. This dialog opens when you select **File** > **Print**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

167/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Printer**

**Name**

Specifies the printer that you want to use. You can select from a list of all the available configured printers.

The information below the **Name** box applies to the selected printer. The printer that you select in the **Name** box is the default printer for the rest of the current design session until you specify a different printer.

**Properties**

Opens the **Printer Document Properties** dialog, which allows you to specify page setup and other printer settings specific to the selected printer.

**Status**

Describes the state of the selected printer, for example, busy or idle. This area is read-only.

**Types**

Displays the type of printer currently selected. This area is read-only.

**Where**

Identifies the printer path, printer port, queue name, or physical location of the currently selected printer.

This area is read-only.

**Print filter**

Filters the selected drawings that are to be printed according to the specified criteria. If none of the check boxes in this section are selected, all selected drawings are printed.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

168/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Typicals only**

Prints only the typical items as they appear in the typical view.

**Apply display set**

Associates symbols to a display set filter that defines which symbols to print. If not selected, then no filtering is applied to the drawing and the entire drawing prints. Because single and multiple drawings can be printed with the display set applied and the legend selected, following is the print criteria defined for each case: **Number of drawings Display set**

**Display of**

**’Print all selected drawings in**

**Documents**

**selected for print**

**applied?**

**legend**

**a single document’ selected?**

**printed**

**selected?**

Single

Yes

Yes

No

Two

documents -

one with the

drawing and

the other with

the legend.

Multiple

Yes

Yes

No

One document

for each

drawing and

one for the

legend.

Example: If you

print four

drawings, five

documents will

be printed, one

each for each

drawing and

one for the

legend.

Multiple

Yes

Yes

Yes

Single

document

including all the

drawings with

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

169/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

the legend on

the last sheet.

Example: If you

print four

drawings, all

the drawings

will be printed

in a single

document with

the legend on

the last sheet.

**Print a Drawing with Display Set - Single**

**Print Drawings with Display Set - Multiple**

When specifying line widths for display sets, you can set label graphics and leader lines to appear in the default width of the labels regardless of the line width value specified for model items. This option is specified by using a key ‘IgnoreDisplaySetWidthOnLabels’ under the ‘Options’ section of the Smart P&ID.ini file (located in the users\ folder) as shown:

[options]

WaterMarkWhileWorking=True

WaterMarkWhilePrinting=True

undosteps=0

autogapping=False

ConsistencyChecks=True

.

.

.

IgnoreDisplaySetWidthOnLabels=1

The following table shows how the values assigned in the SmartPlantPID.ini file affect the output.

**Key Value**

**Resultant Behavior when Applying Display Set**

IgnoreDisplaySet

Label line widths are independent of model item line widths; label line widths are set to WidthOnLabels=1 default value for labels.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

170/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Label line widths are independent of model item line widths; line widths of label graphics and leader lines are set to the default value for labels.

IgnoreDisplaySet

Label line widths, including graphics and leader lines, are the same as the model item WidthOnLabels=0 line widths.

No key

Label line widths, including graphics and leader lines, are the same as the model item line widths.

**Active display set**

Displays the selected display set. You can select **Browse** to select a defined display set.

**Print all selected drawings**

This option is only available when either or both check boxes - **Typicals only** and **Apply display set** - are selected. When the **Print all selected drawings** check box is cleared, those drawings that do not contain filtered items as a result of applying these filters are excluded from the print output. Selecting the check box results in the printing of all selected drawings, including drawings that do not contain such filtered items.

**Options**

**Fit to page**

Prints your entire drawing on one page. This option is selected by default.

**Print black and white**

Prints the drawing in black and white. This option is selected by default.

**Print claim status**

Allows for the printed copy to include the status of claims. This check box is only enabled if you are in a Project.

**Print watermark**

Prints a faint graphic in the drawing background.

**Print inconsistency markers**

Causes inconsistency markers in the graphic to appear on the printed copy.

**Print all selected drawings in single document**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

171/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Prints all the selected drawings in a single document. If the **Legend Box** check box is selected in **Apply** **Display Set** dialog, then the legend for all the selected drawings is also printed on the last page of the printed document. For more information, refer to Display Set Legend.

This option appears only when multiple drawings are selected for printing.

**Settings**

Opens the **Settings** dialog, which allows you to view and edit the scale and origin of your print area.

**Preview**

Allows you to see how the image will look when printed. The image displays on your monitor.

**Schedule**

Opens the Schedule Task Wizard, which allows you to specify options for printing the selected drawings at a later time or on a regular interval. For details, see Scheduling Tasks.

This option is disabled if ‘Print to PDF’ or a converter option (such as Amyuni) is selected in the **Name** box.

**Apply Display Set Dialog**

You use this dialog to select a display set to apply to drawings before printing or saving them.

**Add Folder**

Adds an empty folder to the Tree. You can use **Rename** to define a name for the folder. These folders can be used to organize display sets.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

172/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Add Display Set**

Creates a new display set. You can use **Rename** to define a name for the new display set.

**Create Auto Display Set**

Automatically creates a display set for the plant or the selected drawings along with filters. Filters are automatically created for the Plant Item properties you select. For more information, refer to Working with

Auto Display Sets.

**Add Filter**

Displays the **Select Filter** dialog. Select any displayed filter to add it to the current display set.

**Save**

Saves the selected display set.

**Cut**

Removes the selected display set and places it in memory.

**Copy**

Copies the selected display set into memory.

**Paste**

Pastes any values that are currently stored in memory.

**Delete**

Deletes the selected item.

**Rename**

Allows you to select on an item in the Tree and rename it.

**Move Up**

Allows you to move the selected filter name up in the list.

**Move Down**

Allows you to move the selected filter name down in the list.

**Properties**

Displays the properties of the filter.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

173/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Filter Name**

Lists filter names for the selected display set. For display sets you create, you can define filters using **Add** **Filter** command. For auto display sets, filters are automatically created with a defined naming format.

**Color**

For manually created filters, this column shows the selected display color of the items in the selected filter.

For automatic filters, it shows the color auto assigned to the filters. You can click in the **Color** field to display a color palette and then select any color to define a new color for any selected item(s). The default color square is defined with the crosshatch pattern. **Default** is the color value specified in Options Manager for the item type’s symbology.

**Width**

For manually created filters, this column shows the selected display width of items defined in the selected filter. For automatic filters, it displays the default width defined for the filters. A wider display width would cause the item to be more visible. **Default** is the width value specified in Options Manager for the item type’s symbology. **Legend Box**

Selecting this checkbox prints a legend of the filters of a display set applied on the drawing(s). For more information, refer to Display Set Legend.

From Drawing Manager, you can select multiple drawings to apply a display set.

The automatically created display sets and filters function in the same way as the display sets and filters created manually.

**Display Set Legend**

Creates a legend for the filters in a display set when the **Legend Box** checkbox is selected in the **Apply** **Display Set** dialog, when applying a display set to a drawing. The legend includes the colors, names and descriptions of the filters in a defined format.

From the Modeler or Drawing Manager, when you print a drawing that has a display set applied and the **Legend Box** selected, the legend is also printed. The criteria for printing the legend is defined in the **Print** dialog.

If no display set is applied, then no legend is created.

When the **Legend Box** checkbox is selected, the legend pops up every time you open the drawing until you clear the display set applied on it.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

174/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Print Command (File Menu)**

Opens the **Print** dialog where you can specify options for printing your drawings.

**Define a Display Set**

1. Select **View** > **Apply Display Set**.
2. Select the **My Display Sets** folder or the plant folder, and on the toolbar, select **Add Display Set**

.

1. Type a name for the display set.
2. Right-click the display set and on the shortcut menu, select **Add Filter** to display the **Select Filter** dialog.
3. Browse to an existing filter and select **OK** to add that filter to the display set.
4. If you want to create a new filter, browse to the appropriate folder, select **New.**
5. On the **New Filter** dialog, select whether to create a simple or compound filter. See *Create a New* *Simple Filter* and *Create a New Compound Filter*  in the Filter Manager Help.
6. Create the filter with the required properties.
7. Select **OK** to close the **Add Filter** dialog for each simple filter that you create.
8. Select **OK** to close the **Select Filter** dialog and return to the **Apply Display Set** dialog with the selected filter added to the display set.
9. For each filter in the display set, select the desired color and width of the drawing item lines to be applied by that filter. To hide an item on the drawing sheet, select **None** for the color.

Filtering behavior for label colors depends on the value of the **Filter for** property in the label filter and the **Do not show labels for filtered items** check box setting on the **View Properties** dialog **Display** tab (the **Labels** check box must always be selected to enable the **Do not show labels for filtered items** check box). The following table summarizes the behavior.

**‘Filter for’ value**

**‘Do not show labels…’ setting**

**Resultant Behavior when Applying Display Set**

**Label: Model**

Selected

Label colors are independent of model item colors;

**Item**

labels are hidden when model items are hidden.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

175/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Label: Model**

Cleared

Label colors are independent of model item colors;

**Item**

labels display when model items are hidden.

**Label: Catalog**

Selected or cleared

Label colors are the same as the model item colors;

**Item** (optional)

labels are hidden when model items are hidden.

**Working with Auto Display Sets**

1. Open a drawing.
2. Select **View** > Apply Display Set.
3. In the Apply Display Set dialog, select Create Auto Display Set Command** **

.

1. In the Create Auto Display Set dialog, type a name for the automatic display set.
2. For **Scope**, choose **Plant** or **Drawing**.

To create automatic display filters for all the drawings in the plant, select **Plant**.

To create automatic display filters for the drawing, select **Drawing**.

1. Choose and add the necessary properties for which you want to create automatic display set.
2. Select **Create**.
3. In the **Apply Display Set** dialog, select **Save** .

*The software creates a filter for each property set in a drawing.*

1. If necessary, modify the color and line width in a filter.

To hide an item on the drawing sheet, select **None** for the color.

**Create Auto Display Set Command**

Automatically creates a display set along with filters for a plant or a drawing. The filters are automatically created for the properties of Plant Items you select.

The automatically created display sets are shown in the **AutoDisplaySet** folder that appears in the plant’s folder in **Apply Display Set** dialog. Each filter appears with a name, color, and width, that you can modify as required. These filters are listed in the **Auto Filters** folder in the **Plant Folders** in the **Select Filter** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

176/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

The naming convention of the automatic filter is unique and follows the format

_Filter.

The automatically created display sets and filters function in the same way as the display sets and filters created manually.

**Create Auto Display Set Dialog**

Allows you to specify a name for the auto display set, select scope and properties for creating automatic filters.

**Name**

Allows you to type in a name limited to 39 characters for the auto display set.

**Scope**

Defines if the filters for the auto display set should be created for the plant or a drawing. If the scope is selected as Plant, automatic filters are created for the values of Plant Item properties of all the drawings in a plant. If selected as Drawing, automatic filters are created for the values of Plant Item properties of a drawing.

**Available Properties**

Lists all the properties available for the Plant Items.

**Selected Properties**

Displays the properties you select for creating automatic filters.

**Add**

Adds properties to **Selected Properties** for creating filters.

**Remove**

Removes properties from the **Selected Properties** list.

**Create**

Creates a display set with automatic filters.

When you select multiple drawings for applying display set and set the scope to Drawing, the auto filters will be created for the values of Plant Item properties available for all the drawings selected.

**Apply a Display Set**

1. Open a drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

177/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select **View** > **Apply Display Set** to display the **Apply Display Set** dialog.
2. Under the **My Display Sets** folder or the plant folder or the Auto Display Sets folder, select the display set.

If needed, change the color and width of the drawing item lines to be applied by the filters in the display set. To hide an item on the drawing sheet, select **None** for the color.

1. Select **OK**.

Filtering behavior for label colors depends on the value of the **Filter for** property in the label filter and the **Do not show labels for filtered items** check box setting on the **View Properties** dialog **Display** tab (the **Labels** check box must always be selected to enable the **Do not show labels for filtered** **items** check box). The following table summarizes the behavior.

**‘Filter for’ value ‘Do not show labels…’ setting Resultant Behavior when Applying Display Set** **Label: Model**

Selected

Label colors are independent of model item

**Item**

colors; labels are hidden when model items are

hidden.

**Label: Model**

Cleared

Label colors are independent of model item

**Item**

colors; labels display when model items are

hidden.

**Label: Catalog** Selected or cleared

Label colors are the same as the model item

**Item** (optional)

colors; labels are hidden when model items are

hidden.

When specifying line widths for display sets, you can set label graphics and leader lines to appear in the default width of the labels regardless of the line width value specified for model items. This option is specified by using a key ‘IgnoreDisplaySetWidthOnLabels’ under the ‘Options’ section of the Smart P&ID.ini file (located in the users\ folder) as shown:

[options]

WaterMarkWhileWorking=True

WaterMarkWhilePrinting=True

undosteps=0

autogapping=False

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

178/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

ConsistencyChecks=True

.

.

.

IgnoreDisplaySetWidthOnLabels=1

The following table shows how the values assigned in the SmartPlantPID.ini file affect the output.

**Key Value**

**Resultant Behavior when Applying Display Set**

IgnoreDisplaySet Label line widths are independent of model item line widths; label line widths are WidthOnLabels= set to default value for labels.

1

Label line widths are independent of model item line widths; line widths of label graphics and leader lines are set to the default value for labels.

IgnoreDisplaySet Label line widths, including graphics and leader lines, are the same as the model WidthOnLabels= item line widths.

0

No key

Label line widths, including graphics and leader lines, are the same as the model item line widths.

For a display set that contains one or more asking filters, on selecting **Apply**, the **Asking Filters** dialog opens with the default values for each asking filter, allowing you to change the operators and values of each asking filter’s attributes, if desired. The attribute values you selected are used when saving or printing the drawing and those values are retained until the display set is cleared for that drawing. This applies on a per drawing basis; therefore if the same display set is applied to more than one drawing, you can enter different attribute values for each asking filter and those values are retained independently for each drawing.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

179/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Print Preview Dialog**

Allows you to see how the image will look when printed. The image displays on your monitor. If more than one drawing is selected for printing, you can select **Next** or **Back** to view the other selected drawings.

Select **OK** to return to the **Print** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

180/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Settings Dialog**

Specifies the print layout for the drawings to be printed. These settings apply to all drawings you have selected to print. This dialog opens when you select **Settings** on the **Print** dialog.

**Scale**

Controls the scale applied to the print area in a document.

**Best fit**

Scales the selected drawing sheets or print area to fit the printer paper for the configured device.

**Manual scale**

Specifies the scale value to apply to the print range during printing. For example, if the print range is a rectangle at 12 cm by 12 cm and you set a manual scale of 1:12, then the printed range appears to be 1 cm by 1 cm on the printer paper. If you want a 1:1 drawing of the current sheet scale, you can set the **Paper** **length** option to 1 and the **Design length** option to 1.

**Paper length**

Specifies the paper length for the document you want to print with respect to the **Design length** option.

**Design length**

Specifies a design length (size of the printed graphic) with respect to the **Paper length** option.

**Origin**

Adjusts the origin of the graphic area, thereby changing the location of the effective print area on the paper.

**Center**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

181/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Positions the print area center to the center of the printer paper. If you do not set this option, then the paper positions at bottom left to bottom left.

**X origin**

Sets a shift in the x-direction from the origin.

**Y origin**

Sets a shift in the y-direction from the origin.

**Preview**

Displays dynamically how the graphic prints on the sheet as you change other options on the dialog.

For many of the options on this dialog such as, ** Design length**,** Paper length**,** X**,** Y**, and so forth, when you change an option, the red, blue, and black boxes in the** Preview** area change to reflect your new values. Therefore, you have a dynamic representation of how your graphic fills the printed sheet.

**Print Status Dialog**

Displays the progress of your print job. This dialog opens automatically when you select **OK** on the **Print** dialog.

**Drawings**

Lists the drawings to be queued to the printer. When each drawing is queued, a check mark is displayed next to that drawing name.

**View Log**

Opens the log file with details of the print jobs.

**Close**

Closes the dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

182/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Print Multiple Drawings**

1. In the **Tree** view, select the drawings you want to print. Use the SHIFT or CTRL key to select multiple drawings or use **Edit** > **Select All**. Also, if you need to print all drawings in the Plant, select **View** > **Include Subnodes**. Then, select **Edit** > **Select All**.
2. Select **File** > **Print**.
3. Set your printing options on the **Print** dialog and select **OK**.

When filtering by typicals or display sets to determine which drawings are to be printed, you can specify whether to include or exclude in the printout drawings that do not contain filtered items.

To print a drawing with the latest changes, update the out-of-date drawings.

For a display set that contains one or more asking filters, on clicking **OK** in the **Print** dialog box, the **Asking Filters** dialog box opens with the default values for each asking filter, allowing you to change the operators and values of each asking filter’s attributes for the selected drawings, if desired.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

183/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Using Workshare**

Workshare functions allow you to share Smart P&ID data within one plant structure with remote sites.

Designed for companies running plants from multiple sites, EPCs or Owner/Operators, or for multiple companies that are working on a single plant, Workshare provides tools to manage changes as if they were created at the same site.

**Hosts and Satellites**

Workshare functions use a host/satellite model for sharing Smart P&ID data among multiple locations. The host, using Smart P&ID, creates satellite slots that include the entire Smart P&ID system and grants access to P&ID data by allowing the satellite sites to subscribe to an available satellite slot.

The satellite sites, after using Smart P&ID to subscribe to a satellite slot at the host site, use Smart P&ID

Drawing Manager to create, view, or modify the drawings.

Drawing ownership is controlled at the site where they are created. When ready, the owner of a drawing can grant ownership to the host or to other satellites. Throughout this sharing process, synchronization tools in Smart P&ID Drawing Manager allow the host and the satellites to make sure they are working with the latest data.

**Workshare Modes**

Workshare can be configured in two modes:

**Connected**

Uses a database link established between the database servers at the host and satellite sites. In other words, satellites are distributed databases linked to a host database. In connected Workshare, both the host and satellite must be using Oracle. If you plan to use Workshare in an integrated environment, we recommend using connected Workshare to ensure smooth claiming.

**Standalone**

Shares files and data without having a database link. Files are manually transmitted between host and satellites.

Any given site can host both connected and standalone satellites. In other words, the host can use Oracle and the satellite can use SQL Server, or any combination thereof. However, a site must use Oracle to host a connected Workshare collaboration.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

184/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Configurations**

There are numerous configuration possibilities for implementing Workshare. For example, you can use Workshare to simulate the PDS 2D Task/Master configuration by using the Workshare host as the Task environment and the satellite as the Master. You could then publish drawings for sharing from the host to the satellite. By limiting user access at the satellite site to Read Only for Smart P&ID objects, the satellite becomes an issued drawing database.

You can also use standalone Workshare in a mixed database environment where the host can be using Oracle and the satellite can be using SQL Server, or vice-versa. This configuration is useful when multiple companies using different database standards are working on the same plant.

Standalone Workshare provides a means of implementing off-site projects.

Workshare can be used in an integrated environment. See Using Workshare in an Integrated Environment.

Another possible configuration involves using Workshare at the project level within an As-Built plant

scenario. See Using Workshare with Projects.

**Automation**

Several of the Workshare commands are available in the Smart P&ID automation layer. For more information about using these Workshare automation commands, see the *Smart P&ID* Programmer’s Help.

**Using Workshare in an Integrated Environment**

The following rules apply to using the Workshare functionality in an integrated environment: You can enable and disable Workshare before or after registering a Greenfield plant.

You can create satellites and connect to them after registering.

You cannot register a satellite or a project host.

You cannot retrieve a PBS document when Workshare is enabled.

Satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

185/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Using the Smart P&ID SmartPlant Menu Commands Within a Workshare Collaboration** The Workshare host can perform actions using the following commands from within Smart P&ID when registered in an integrated environment:

**Publish**

Any drawing can be published.

**Retrieve**

Any document can be retrieved.

**Correlate**

Available to review correlations only if the drawing is read-only with respect to Workshare. No other correlation activity is allowed for read-only drawings. If the drawing is owned with respect to the Workshare site, then all correlation activities are available.

**To Do List**

Only available at the Workshare Host for drawings opened with read-write privileges. For drawings opened in read-only mode, commands that modify a drawing, such as the **Run To Do List** task, are not available.

To Do List tasks can be reviewed on drawings for which the host does not have ownership, but these tasks cannot be executed unless ownership is assigned to the Host. The To Do List is not available at the Satellite.

**Workshare Common Tasks**

After configuring Workshare at the host and satellite sites, the following tasks are used frequently when using Workshare in Smart P&ID. Most of these procedures can also be scheduled for a later time or at regular intervals.

**Publishing a Drawing**

To share a drawing with another site, you must first publish that drawing. Publishing the drawing does not grant access to the drawing: it only freezes a copy of the drawing in anticipation of ownership being transferred. Between the publication of a drawing and the transfer of ownership, the publishing site still owns the drawing and is free to modify it. Granting subscription access to the drawing gives another site read-only access to the published copy of the drawing. Assigning ownership to the drawing allows the new owner to claim ownership of the drawing and obtain the published copy of the drawing.

**Granting Access to a Drawing**

After you publish a drawing, you can grant access to that drawing by using the **Subscribe Access** command. For connected Workshare, the designated satellite site will be able to open and view the published drawing, but will not be able to modify it. For standalone Workshare, the drawing will be writeable https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

186/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

at the satellite site. You can grant write access to a drawing, too, by using the **Assign Ownership** command. The designated site will then not only be able to open the drawing but also to edit it.

As soon as you use the **Assign Ownership** command, the selected drawing is automatically published.

**Getting the Latest Version of a Drawing**

After a site has been granted access to a published drawing, that site must subscribe to the latest version in order to open or edit that drawing. Normally you get the latest version over a Workshare connection from the owner site by using the commands for remote access. You can also get the latest version from a local folder - for instance, if the site has sent you the latest version on CD.

Drawings are never dynamically linked between sites. That is, the version you view is only the latest version you subscribed to or only the latest version left on your site. If another site has modified the drawing since then, you do not see those changes.

**Synchronizing Reference Data**

Because only the host site can change the reference data, satellite sites need to synchronize the reference data from the host site each time it changes. Synchronizing the reference data involves making sure both the host and satellites are using the same plant schema and data dictionary, plant structure, Smart P&ID

schema and data dictionary, and various options settings. Synchronization also involves making sure various data files at the satellite site remain up to date with the files at the host. These files include the rules file, insulation specification file, report and drawing templates, symbology settings, CAD definition file, and so forth.

You can synchronize this data either with the host site or with a copy of the reference data on your local computer or network using the **Synchronize Reference Data** commands.

Reference data at the satellite site must be synchronized with the host reference data before drawings and shared items can be synchronized or transferred.

We recommend scheduling synchronization for a time when no users are working in the data.

**Synchronizing Shared Items**

Some drawing items, such as off-page connectors, instrument loops, and utility connectors, require special handling when using Workshare. Because these items can be shared by more than one drawing, any modifications made to a drawing at another site can have ramifications for the shared items contained in that drawing.

Several Workshare commands are available in the Smart P&ID automation layer. See the *Smart* *P&ID*  Programmer’s Help.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

187/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Using Workshare with Projects**

Workshare functions the same whether using projects or not. The only difference is that when using projects, only a project can function as a Workshare host. The Plant cannot be a host or a satellite when projects are enabled.

In a Workshare collaboration, new plant groups cannot be created by standalone satellite sites or by the satellite sites in a project.

Connected Workshare is available only for sites using Oracle databases. If your plants and projects are using a SQL Server database, you cannot use connected Workshare.

Standalone Workshare allows you to mix the type of databases used in a Workshare collaboration.

When a project is used as a Workshare host, the satellites synchronize their reference data with the Plant reference data.

When transferring ownership of a drawing to another Workshare site, the corresponding versions are not transferred. Only the current version of the drawing is transferred.

New plant groups (plants, areas, units, and so forth) cannot be created by satellites hosted by a project.

**Using Projects in an Existing Workshare Collaboration**

You must discontinue all Workshare collaboration in a plant before you can create projects in the plant. In other words, if the plant structure contains active **Satellites**, the **Enable Projects** command remains unavailable. We recommend completing the following tasks before enabling the plant for projects.

1. Transfer all drawings to the host.
2. Delete all satellites.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

188/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Disable the plant for Workshare.
2. Enable the plant for projects.
3. Create a project to serve as the host.
4. Enable the project for Workshare.
5. Create satellite slots in the project host.
6. Create satellites.
7. Check out or fetch drawings at the host, then re-distribute drawings back out to the satellites.

**Projects vs. Workshare**

The following comparisons can be useful when making the decision about whether to use projects or Workshare or both.

**Category**

**Projects**

**Workshare**

Topology

Each plant can have many

Each Workshare host can have many

projects. Each project belongs satellites. Each satellite belongs to to exactly one plant.

exactly one host.

Identity

Objects that are transferred

Objects that are transferred between a

between a plant and a project host and a satellite maintain their maintain their identity.

identity.

Reference Data

One set of reference data is

The reference data must be the same

used for a plant and all its

for a host and its satellites. Changes

projects. Changes can be

can be made only through the host.

made only through the Plant.

Changes are propagated to the

Because all projects use the

satellites by means of the synchronize

same reference data as the

reference data commands in Drawing

Plant, all projects immediately Manager.

see changes to the reference

data.

Physical Separation

A plant and all its projects

Connected Workshare allows data to

must exist on the same server be distributed to multiple database https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

189/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

and within the same database instances on separate servers that instance.

might be remote from the host server.

Standalone Workshare allows data to

be distributed between separate

database types.

Organization

Projects are suited to dividing Workshare is suitable for dividing up up work that will be done

work among multiple organizations.

within a single organization.

Work Off-Site at a Satellite Site?

No. In a projects/Workshare

Yes, in a connected Workshare

scenario, claim records are

configuration (without projects), work

stored in the P&ID schema at

can continue when the database link

the host site. If the database

goes down. Standalone Workshare

link goes down, claimed items does not require any database at the satellite site will not

connections.

recognize the claim status.

However, the claim status of

newly placed items will be

recognized when the database

link is re-established.

When to Use?

When the work to be done

When the work to be done must be

must be divided into subsets,

divided into subsets and assigned to

but it is all done by the same

different organizations.

organization and can use the

same server.

When the subsets of work must be

done on servers that are physically

When an As-Built facility model separated.

is to be built and the changes

to that model need to be

managed.

When a master database is to

be used for the approved

design and a task database is

to be used for the ongoing

design work.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

190/291

3/13/25, 10:36 AM

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

Project 1 assigns ownership of Drawing A to Satellite

1.1.

**2**

Project 2 fetches Drawing A from Project 1.

**3**

Project 2 assigns ownership of Drawing A to Satellite

2.1.

**4**

Satellite 2.1 opens, claims items, and modifies

Drawing A.

Drawing A becomes Drawing A’.

Satellite 2.1 exits Drawing A’.

**5**

Satellite 2.1 assigns ownership of Drawing A’ to

Project 2.

**6**

Satellite 1.1 opens, claims items, and modifies

Drawing A.

Drawing A becomes Drawing A’’.

Satellite 1.1 releases claims and exits Drawing A’’.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

191/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**7**

Satellite 1.1 assigns ownership of Drawing A’’ to

Project 1.

**8**

Project 1 checks Drawing A’’ into the Plant.

**9**

Project 2 checks out Drawing A’’ (without replacing

Drawing A’).

**10**

Project 2 compares Drawing A’’ (modified in Project

1) with its own Drawing A’.

**11**

Project 2 refreshes Drawing A’ with differences from

Drawing A’’.

Drawing A’ becomes Drawing A’’’.

**12**

Project 2 checks Drawing A’’’ in to the Plant.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

192/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Scenario 2: Loops**

The following workflow demonstrates using shared items in a connected Workshare collaboration using projects.

**1**

The Plant creates Drawing A and places 3 DCS

instruments.

**2**

Project 1 checks out Drawing A and creates the

following loops:

P-100 in the drawing stockpile

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

193/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

P-101 in plant stockpile (shared = False)

P-102 in plant stockpile (shared = True)

Project 1 verifies via the EDE that there are 3 DCS

instruments and 3 loops in the drawing.

**3**

Project 1 closes Drawing A.

Drawing A becomes Drawing A’.

**4**

Project 2 fetches (with read/write permissions)

Drawing A’ from Project 1.

Project 2 opens Drawing A’ and verifies via the EDE

that P-100 is in the drawing stockpile and that there

are 3 DCS instruments, then closes Drawing A’.

Project 2 assigns ownership of Drawing A’ to

Satellite 2.1 and synchronizes shared items.

**5**

Satellite 2.1 executes Get Latest Version from

Remote command and synchronizes shared items.

Satellite 2.1 opens Drawing A’ and verifies via the

EDE that P-100 is in the drawing stockpile and that

there are 3 DCS instruments, then closes Drawing

A’.

**6**

Project 1 assigns ownership of Drawing A’ to

Satellite 1.1 and synchronizes shared items.

Satellite 1.1 executes Get Latest Version from

Remote command and synchronizes shared items.

Satellite 1.1 opens Drawing A’ and verifies via the

EDE that P-100 is in the drawing stockpile and that

there are 3 DCS instruments, then closes Drawing

A’.

**7**

Satellite 1.1 creates Drawing B and places an

instrument. Drawing B becomes Drawing B’.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

194/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**8**

Satellite 1.1 opens Drawing B’, verifies via the EDE

that only the P102 loop tag is available for

assignment (confirming that synchronizing shared

items brought the loop over to the satellite), then

closes Drawing B’.

**9**

Satellite 2.1 creates Drawing C and places an

instrument. Drawing C becomes Drawing C’.

**10**

Satellite 2.1 opens Drawing C’, verifies via the EDE

that only the P102 loop tag is available for

assignment (confirming that synchronizing shared

items brought the loop over to the satellite), then

closes Drawing C’.

**11**

Satellite 1.1 assigns ownership of Drawing A’ to

Project 1 and synchronizes shared items.

**12**

Project 1 executes Get Latest Version from Remote

command and synchronizes shared items.

Project 1 opens Drawing A’ and verifies the following

via the EDE:

P-100 in the drawing stockpile

P-101 in plant stockpile (shared = False)

P-102 in plant stockpile (shared = True)

3 DCS instruments

Project 1 closes Drawing A’ and then checks

Drawing A’ into the Plant.

**13**

The Plant opens Drawing A’ as read-only and

verifies via the EDE that P-100 is in the drawing

stockpile and that there are 3 DCS instruments.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

195/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Scenario 3: OPCs**

The following workflow demonstrates handling OPCs in a connected Workshare collaboration using projects.

**1**

Project 1 checks out Drawing A from the Plant.

**2**

Project 1 checks out Drawing B from the Plant.

**3**

Project 1 assigns ownership of Drawing B to Satellite

1.1.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

196/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**4**

Project 1 checks out Drawing C from the Plant.

**5**

Project 1 assigns ownership of Drawing C to

Satellite 1.1.

**6**

Project 1 opens Drawing A, places OPC-100, sends

the partner OPC-100 to Drawing B, and closes the

drawing.

Drawing A becomes Drawing A’.

**7**

Project 1 synchronizes shared items with Satellite

1.1.

**8**

Satellite 1.1 synchronizes shared items.

**9**

Satellite 1.1 opens Drawing B, places partner OPC-

100 from the drawing stockpile, and closes the

drawing.

**10**

Project 1 synchronizes shared items with Satellite

1.1, then opens Drawing A’ and verifies that “to

drawing” name in the OPC label is updated with

information from Drawing B.

Drawing A’ becomes Drawing A’’.

**11**

Project 2 fetches Drawing A’’ and assigns

subscription access to Satellite 2.1.

**12**

Satellite 2.1 opens drawing A’’ and verifies that the

OPC label is updated with information from Drawing

B, then closes Drawing A’’.

**13**

Project 1 assigns ownership of Drawing A’’ to

Satellite 1.1 and synchronizes shared items.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

197/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Satellite 1.1 gets latest version of Drawing A’’ and

synchronizes shared items.

Satellite 1.1 opens Drawing A’’ and verifies that the

“to drawing” name of OPC-100 is updated, then

closes Drawing A’’.

**14**

Satellite 1.1 opens Drawing B, deletes OPC-100 to

the Plant stockpile, then closes the drawing.

**15**

Satellite 1.1 opens Drawing C, places OPC-100 from

the Plant stockpile, then closes the drawing.

**16**

Satellite 1.1 assigns ownership of Drawing A’’ to

Project 1 and synchronizes shared items.

**17**

Project 1 gets latest version from remote and

synchronizes shared items.

Drawing A’’ becomes Drawing A’’’.

**18**

Project 1 opens Drawing A’’’ and verifies that the

graphical label in OPC-100 contains the correct

information and that the data relating to OPC-100

and its partner is correct in the EDE, then closes the

drawing.

**19**

Project 2 fetches Drawing A’’’ from Project 1.

Project 2 opens Drawing A’’’ and verifies that the

graphical label in OPC-100 contains the correct

information and that the data relating to OPC-100

and its partner is correct in the EDE, then closes the

drawing.

Project 2 publishes and assigns subscription access

for Drawing A’’’ to Satellite 2.1, then synchronizes

shared items.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

198/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**20**

Satellite 2.1 gets latest version, subscribes to the

updated Drawing A’’’, and synchronizes shared

items.

Satellite 2.1 opens Drawing A’’’ and verifies that the

graphical label in OPC-100 contains the correct

information and that the data relating to OPC-100

and its partner is correct in the EDE, then closes the

drawing.

In a standalone Workshare collaboration, the satellite site needs only to be given subscribe access to a drawing in order to access items (for example, OPCs) in the Plant stockpile.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

199/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Publishing and Assigning Ownership**

To share a drawing with another site, you must first publish that drawing. Publishing the drawing does not grant access: it only freezes a copy of the drawing in anticipation of ownership being transferred. Between the publication of a drawing and the transfer of ownership, the publishing site still owns the drawing and is free to modify it.

Granting subscription access to the drawing gives another site access to the published copy of the drawing; for standalone Workshare, the drawing will be writable at the satellite site, while for connected Workshare, the drawing will be read-only. Assigning ownership, on the other hand, allows the site to claim ownership of the drawing and to obtain the published copy of the drawing for either Workshare mode.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

200/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

In a standalone Workshare collaboration, drawing ownership controls from which site the host receives a published file of a given drawing. In other words, if a published file did not originate from the site with ownership, the host will ignore it when receiving the latest version of drawings. Only the host can assign ownership, which means that the host can “take back” or revoke ownership of a drawing at any time.

Hosts and satellites can create drawings in either Workshare mode. However, uniqueness of drawing names and numbers is not enforced across a standalone Workshare collaboration.

In connected Workshare collaborations, published files are stored in the database at the publishing site and the Oracle database link is used to transfer published files between sites. In standalone Workshare collaborations, published files are stored in the WSPublish folder at the publishing site and must be manually transmitted to the other sites by e-mail, CD, network share, or other means.

**Publish Command (Workshare Menu)**

Publishes the selected drawing or drawings. The **Publish** dialog displays the status of the operation.

The act of publishing a drawing actually bundles the drawing and its related data and places it as a “blob”

object in the host database.

In a connected Workshare collaboration, when the satellite uses the **Get Latest Version from Remote** command, the published “blob” is copied from the host database to the satellite site database. At the satellite site, the “blob” is then unpacked and the drawing is placed in the local file system while its related data is placed in the local Smart P&ID database.

In a standalone Workshare collaboration, the published “blob” is automatically extracted into a published zip file. The **Publish** command derives which sites have been given subscribe access to the drawings being published and places the published zip files in the target WSPublish folder in individual folders corresponding to each subscribing site, allowing you to more easily determine which published zip files to transmit to a given site. The receiving site then uses the **Get Latest Version from Local** command to unpack the zip file, placing the drawing in the local file system and the related data into the local Smart P&ID database.

For mixed Workshare collaborations, the publishing process detects the types of satellites involved and performs the appropriate actions. For example, when a drawing is published for both a standalone and a connected satellite, the **Publish** command creates the published zip file in the WSPublish folder and places the corresponding “blob” in the database.

For standalone Workshare collaborations, before the connected satellite site can access the published drawing, you must grant subscription access to or assign ownership of the drawing to the satellite site.

For standalone Workshare collaborations, if you do not grant subscription access to or assign ownership of a drawing before you publish it, the published drawing zip file will not be created in the https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

201/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

WSPublish folder.

Satellite-to-satellite data transfer is not supported in standalone Workshare.

Published zip files in the WSPublish folder are overwritten without warning as needed by subsequent publishes.

When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.

**Publish Dialog**

Displays the status of your publishing operation. This status dialog opens when you publish drawings or when you assign ownership to drawings.

**Drawings**

Lists the drawings that are being published, and shows the status of that operation.

**View Log**

Opens the log file that is created when you perform a Workshare operation.

**Publish a Drawing**

1. In the **List** view, select the drawings that you want to publish.
2. Grant access to the drawings by using either the **Subscribe Access** or **Assign Ownership** commands.
3. Select **Workshare** > **Publish**. If you used the **Assign Ownership** command in the previous step, the Publish process is launched automatically.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

202/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. On the **Publish** dialog, you can select **View Log** to see the history of the Workshare operation just completed.
2. If you are using connected Workshare, drawings need to be extracted if the files need to be transmitted manually in a case where the default publishing method is through the database. For

details, see Extract Published Drawings.

1. If you are using standalone Workshare and changes have been made to the reference data, be sure to use the **Publish Standalone Package** command in Smart Engineering Manager to bundle the database reference data for synchronization with the satellite.

For standalone Workshare, you must run the **Subscribe Access** command before you publish, whereas for connected Workshare, the order of these actions is unimportant.

Linked or embedded files are not transferred by Workshare. Those files must be transferred manually.

We do not recommend using linked files in a Workshare collaboration.

You can schedule the selected drawings for publishing at a later time or on a regular interval by using the **Schedule Publish** command in Drawing Manager and following the prompts on the Schedule

Task Wizard.

When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.

**Extract Published Drawings Command (Workshare Menu)**

Extracts all plant-wide published drawing and related data from the database into zip files (one zip file per drawing) so that the data can be manually transmitted to a satellite. The satellite then unpacks the zip file using the **Get Latest Version from Local** command, which places the drawing in the local file system and the related data into the local Smart P&ID database.

This command is available only in connected Workshare collaborations.

**Extract Published Drawings Dialog**

Allows you to specify the location, on a local or network drive, where the extracted data will be placed into a new folder named using the day, date, and time of the publishing operation.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

203/291

3/13/25, 10:36 AM

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

Quits the process if the publishing operation is underway. If the extraction is complete, **Close** simply dismisses the dialog.

**Extract Published Drawings**

1. In Drawing Manager, select the plant structure in the **Tree** view.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

204/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select **Workshare** > **Extract Published Drawings**.
2. On the **Extract Published Drawings** dialog, browse to the directory to which you want your drawings published.
3. Select **OK**.

A new folder is created in this directory and named using the day, date, and time of the publishing operation. This folder contains the results of the extraction operation. The folder could be on a local or network drive.

Extracting published drawings is later used with the **Get Latest Version from Local** command.

This command is available only in connected Workshare collaborations.

**Subscribe Access Command (Workshare Menu)**

Designates which sites should receive a published drawing and grants access to those sites.

In standalone Workshare mode, only the host can set subscribe access and the access to the drawings is read-write. In connected Workshare mode, this command is available to the host and the connected satellites and the access to the drawings is read-only.

In a mixed-mode Workshare collaboration, the following limitations apply: For drawings owned by the host, subscribe access can be given by the host to any standalone or connected satellite.

For drawings owned by a standalone satellite, subscribe access can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer subscription access to a drawing from one satellite to another, the host must first transfer the access back to itself before granting subscription access to the other satellite.

For drawings owned by a connected satellite, subscribe access cannot be set by the host.

**Subscribe Access Dialog**

Allows you to specify the sites that have subscribe access to drawings that you publish.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

205/291

3/13/25, 10:36 AM

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

**Set Subscription Access for a Drawing**

1. In Drawing Manager, select the drawings for which you want to set the subscription access.
2. Select **Workshare** > **Subscribe Access**.
3. On the **Subscribe Access** dialog, select the site that you want to grant access to from the **Available** **Sites** list.
4. Select **Add** to move that site into the **Selected Sites** list.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

206/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You can remove read access from these permissions by using the **Remove** button to move a site out of the **Selected Sites** list.

You must have published a drawing before you can assign access to another site.

When assigning subscription access, drawings in standalone Workshare mode are writable, whereas drawings in connected Workshare mode are read-only.

If a drawing in standalone Workshare mode is modified at the satellite site and then published and sent back to the host, it will not be available for selection at the host when the **Get Latest Version** **from Local** command is run. To grant read/write permission for the drawing at the host site, use the

Assign Ownership option. For details, see Assign Ownership to a Drawing.

When the other site gets a copy of a drawing to which they have read access, they do not see updates to that drawing after the point when they receive that version. That is, the two instances of the drawing are not linked dynamically. For more information about getting the latest version of a drawing, see

Getting Latest Versions of Drawings.

**Assign Ownership Command (Workshare Menu)**

Opens the **Assign Ownership** dialog, where you can specify which Workshare sites have read/write permission for published drawings. Drawing ownership is used to control, for a given drawing, which satellite’s published data the host receives during a Get Latest Version operation.

In a mixed-mode Workshare collaboration, the following limitations apply.

For drawings owned by the host, ownership can be given by the host to any standalone or connected satellite.

For drawings owned by a standalone satellite, ownership can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer ownership to a drawing from one satellite to another, the host must first transfer ownership back to itself before granting ownership to the other satellite.

For drawings owned by a connected satellite, ownership cannot be set by the host.

When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.

When the host, in standalone mode, is functioning as a project, all items on the selected drawings are automatically claimed when the drawing ownership is assigned to a satellite site. If exclusive claiming is https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

207/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

being used and one or more items have already been claimed by another project, assigning ownership is not allowed.

Assigning ownership of a drawing automatically publishes the drawing.

When transferring ownership of a drawing, the corresponding drawing versions are not transferred.

Only the current version of the drawing is transferred.

If the site to which ownership has been assigned has subscription access, the subscription access will be removed.

**Assign Ownership Dialog**

Allows you to specify the site to which you want to grant ownership of the selected drawing.

**Available Workshare sites**

Lists the sites that are currently linked to your site and available to take ownership of the selected drawing.

**OK**

Assigns ownership of the drawing to the specified site and publishes the selected drawing.

**Assign Ownership to a Drawing**

1. In the List view, select the drawings to which you want to grant write access.
2. Select **Workshare** > **Assign Ownership**.
3. On the **Assign Ownership** dialog, choose the appropriate site from the list.
4. Select **OK**.

*The drawings are immediately published.*

The sites available on the **Assign Ownership** dialog are specified automatically according to the sites currently participating in the Workshare collaboration. These Workshare sites are set up in Smart Engineering Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

208/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Assigning ownership of a drawing also publishes the drawing.

If you want to grant read access only, see Set Subscription Access for a Drawing.

For drawings owned by the host, ownership can be given by the host to any standalone or connected satellite.

For drawings owned by a standalone satellite, ownership can be given by the host to any other standalone or connected satellite or the host itself. For the host to transfer ownership to a drawing from one satellite to another, the host must first transfer ownership back to itself before granting ownership to the other satellite.

For drawings owned by a connected satellite, ownership cannot be set by the host.

When transferring ownership of a drawing, the corresponding drawing versions are not transferred.

Only the current version of the drawing is transferred.

When using Workshare in an integrated environment, satellites must transfer drawing ownership back to the host in order for the host to publish the drawings and in order for retrieved documents to have tasks updated within the satellite drawings.

**Getting Latest Versions of Drawings**

After a site has been granted access to a published drawing, that site must subscribe to the latest version of the drawing in order to open or edit that drawing. In a connected Workshare collaboration, you get the latest version from the owner site over a database connection by using the commands for remote access. In a standalone Workshare collaboration or a connected collaboration where the satellite does not have remote access to the host, you get the latest version from the owner site by getting the latest version from a local directory after the published files have been extracted into a zip file and manually transmitted to the satellite site via e-mail, CD, network share, or so forth.

Drawings are never dynamically linked between sites. That is, the version you view is only the latest version to which you subscribed or the latest version left on your site. If another site has modified the drawing since you retrieved the latest version of a published drawing, you do not see those changes. At sites that have a copy of a drawing but do not own the drawing, a red lock on the drawing icon appears in the **List** view.

This icon indicates that your version of the drawing may not be the most current.

**Get Latest Version from Remote Command (Workshare Menu)**

Typically used only in a connected Workshare collaboration, this command opens the **Get Latest Version** **from Remote** dialog, which allows you to specify the site from which you want to receive the latest versions of published drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

209/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When you get the latest version of a drawing, you do not see updates to that drawing after the point in time when you got that version. That is, the two versions of the drawing are not linked dynamically.

Before you can get the latest version of a drawing, that drawing must first be published and assigned to you with the appropriate permissions, and you must have a network or database connection to the Workshare site where the published drawing currently resides.

The latest version of a drawing replaces any versions of that drawing currently at your site; therefore, use caution when subscribing to the latest versions.

**Get Latest Version from Remote Dialog**

Allows you to specify the remote site from which you want to receive the latest versions of drawings.

**Available Workshare Sites**

Lists the sites in your Workshare collaboration that have published drawings available to you. If the site you are looking for is not in the list, check to see if that site has published any drawings and, if so, has it assigned access to you.

**Get Latest Version from Remote Dialog (status)**

Displays the status of the Get Latest Version operation.

**Drawings**

Lists the drawings that are being updated and shows the status of that operation.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

210/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**View Log**

Opens the log file that is created during this procedure.

**Get the Latest Version of a Drawing from a Remote Site**

1. In the **Tree** view in Drawing Manager, select the plant structure to accept the latest versions of drawings.

This site must have either subscription access or ownership of the latest versions of drawings.

1. Select **Workshare** > **Get Latest Version from Remote**.
2. On the **Get Latest Version from Remote Site** dialog, select the location from which you want to get the latest versions of drawings, and then select **OK**. The **Get Latest Version from Remote** dialog opens and displays the status of the operation.

You must have a network connection or DBLink with the remote site to use this command. If you received the published drawings from the remote site via a CD or e-email and have stored those files locally, use the **Get Latest Version from Local** command to access those files.

1. Select **View Log** to see the history of the subscription operation just completed.

The locations available in the list in the **Get Latest Version from Remote Site** dialog are specified automatically according to the satellites connected to the host.

When you get a version of a drawing, you do not see updates to that drawing after the point in time when you subscribed to it. That is, the two versions of the drawing are not linked dynamically.

Linked files are not transferred by Workshare. Those files must be transferred manually. We do not recommend using linked files in a Workshare collaboration.

You can select **Workshare** > **Schedule Get Latest Version from Remote** to open the Schedule Task

Wizard and defer the subscription to a later time or on a regular interval. You must still complete the next step in this procedure.

**Get Latest Version from Local Command (Workshare Menu)**

Typically used in a standalone Workshare collaboration, this command opens the **Get Latest Version from** **Local** dialog, which allows you to browse to the published zip file you received from another site and to select the drawings you want to receive. The **Get Latest Version from Local** command detects if the incoming published files originated from the expected host site. If they did not, the files are skipped and an entry is written in the log file.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

211/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When you get the latest version of a drawing, you do not see updates to that drawing after the point in time when you got that version. That is, the two versions of the drawing are not linked dynamically. In a connected Workshare collaboration, the latest version of a drawing replaces the version of a drawing that you currently have on your computer. In a standalone collaboration, a version is created for each replaced drawing.

When a new drawing created at a satellite is obtained by the host, the drawing ownership at the host is set to the originating site. For projects, when new objects created by a satellite site are obtained by the host, new claim records are created at the host.

Before you can get the latest version of a drawing, that drawing must first be published and assigned to you with the appropriate permissions, and you must have placed the zip file containing the extracted published files on your local computer or a network share to which you have access.

**Get Latest Version from Local Dialog**

Allows you to open the zip file containing the extracted published drawings you received from another site.

After opening the zip file, you can view a drawing or compare it with an existing version at your site prior to actually obtaining the drawing and writing it to your local database.

**Published files**

Displays the drawings included in the published zip file. In the following situations, certain published drawings are excluded from this list:

At a connected satellite, excludes published files for drawings owned by that site and drawings from a site not collaborating with the same host.

At the host, excludes published drawings not owned by the originating site and drawings from a site not collaborating with the same host.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

212/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

At a standalone satellite, excludes published files for drawings from a site not collaborating with the same host.

Drawings that already have assigned ownership at the current site are displayed in grey.

**Browse**

Opens the **Select Publish Folder** dialog, which allows you to browse to the location where you saved the

zip file containing the Extract Published Drawings.

**View**

Opens the **View** dialog, which displays a read-only view of the selected drawing version without opening Smart P&ID. You can manipulate the view or select drawing items and review their properties.

**Compare With**

Opens the **Compare With** dialog, allowing you to compare the current drawing version at your site with the incoming data. You cannot compare incoming data to a previous version of the drawing.

**Select All**

Marks all drawings in the **Published files** list to be extracted from the zip file and written to your local plant database.

**Clear All**

Clears all drawings in the **Published files** list.

**Schedule**

Opens the Schedule Task Wizard, which allows you to schedule the get latest from local process for a later time.

**Select Publish Folder Dialog**

Allows you to locate the folder in which the zip file containing the extracted published drawing is stored.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

213/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Look in**

Lists the available folders.

**Drives**

Displays the currently active drive. To change to another drive, select **Network** or select a drive from the list.

**Network**

Opens the Microsoft standard **Map Network Drive** dialog, allowing you to specify a new active drive.

**OK**

Opens the zip file containing the extracted published drawings and lists the drawings in the **Get Latest** **Version from Local** dialog.

**Get the Latest Version of a Drawing from the Local Computer** 1. In the **Tree** view in Drawing Manager, select the plant structure to accept the latest versions of drawings. This plant must have either subscription access or ownership of the latest versions of drawings.

1. Select **Workshare** > **Get Latest Version from Local**.
2. On the **Get Latest Version from Local** dialog, select **Browse**.
3. On the **Select Publish Folder** dialog, browse to the folder that contains the zip file containing the extracted files associated with the latest drawing version.
4. Select **OK**.

*The **Get Latest Version from Local Status** dialog opens and displays the status of the operation.*

1. Select **View Log** if you want to read notes from this process.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

214/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Be sure to synchronize reference data before trying to open the newly obtained drawings. For details,

see Synchronizing Reference Data.

You can schedule this process for a later time by using the Schedule Task Wizard.

If you are using a connected Workshare collaboration and have an active network connection to the remote site, you can get the latest version from there, too. For more information, see Get the Latest

Version of a Drawing from a Remote Site.

**Get Latest Version from Local Dialog (status)**

Displays the status of the **Get Latest Version from Local** process.

**Drawings**

Lists the drawings that are being updated and shows the status of that operation.

**View Log**

Opens the log file.

**Synchronizing Reference Data**

Because only the host site may change the reference data, satellite sites need to synchronize the reference data from the host site each time it changes.

Synchronizing the reference data (RDB) involves making sure both the host and satellites are using the same plant schema and data dictionary, plant structure, Smart P&ID schema and data dictionary, and various options settings. Synchronization also involves making sure various data files at the satellite site remain up to date with the files at the host. These files include the rules file, insulation specifications, report and drawing templates, symbology settings, CAD definition file, and so forth.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

215/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Changes made to a data dictionary require reference data synchronization before any publishing or subscription activity. Because the data dictionary can be modified only at the host site, the host administrator should inform the satellite administrators when any data dictionary at the host is modified.

Reference data stored in the data dictionary that can be changed or updated includes, but is not limited to, new properties or changes to existing properties (such as display name, category) Validation or Calculation IDs, filters, and **Engineering Data Editor** layouts.

You can synchronize reference data either directly with the host site over a network connection or with a copy of the reference data on your local computer (or network share) using the **Synchronize Reference** **Data** commands.

There are two synchronization stages:

**Database, Schema, and Data Dictionary Synchronization**

Involves synchronizing the database-related data listed below. In connected Workshare collaborations, synchronizing this portion of the reference data is accomplished automatically over the DBLink using the **Synchronize Reference Data** command. For standalone Workshare collaborations, the host uses the **Publish Standalone Package** command in Smart Engineering Manager to bundle this information into a zip file (plantname_sync.zip) for the satellite site to access in the **Published standalone package file** field on the **Synchronize Reference Data from Copy** dialog.

Plant schema and data dictionary

Plant structure

Plant replication schema, if using connected Workshare

Smart P&ID schema and data dictionary

Formats

Options settings

**File Synchronization**

Involves the host site manually transmitting the following data files to the satellite site for access using either of the **Synchronize Reference Data** commands.

Rules file (rules.rul)

Insulation specification file (InsulationSpec.isl)

Report and drawing templates (border files are synchronized only if they are in the same location as the drawing templates)

Symbology settings (ProjectStyles.spp)

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

216/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

CAD definition file (Exportlayer.xlsx)

Templates

Path to the symbol catalog

Plant Configuration file for ‘Save as XML’ (PlantConfig.xml) For connected Workshare collaborations across domains, the satellite site can use the **Synchronize** **Reference Data** command to synchronize the database part of the reference data only if it has no access to the reference data shared folder at the host. If file synchronization is also needed, then the satellite should use the **Synchronize Reference Data from Copy** command.

During the synchronization process, a log file, SynchRefData.log or SynchRefDataFromCopy.log is created in the user’s temp folder (%temp%). This log file contains a list similar to the list that is displayed in the **Synchronize Reference Data** dialog.

Customizations should be done at the host. For example, Plant Filters should not be created at a satellite site because when you synchronize reference data with the host, you lose that information.

However, you can always create My Filters in the Filter Manager environment.

Automation programs (for example, DLL and OCX files) are not synchronized. For more information about automation, see *Smart P&ID Programmer’s Guide*.

Reference data at the satellite site must be synchronized with the host reference data before any drawings and shared items can be synchronized or transferred.

Border files are synchronized only if they are in the same location as the drawing templates.

We recommend scheduling synchronization for a time when no users are working in the data.

**Synchronize Reference Data Command (Workshare Menu)**

Typically used in a connected Workshare collaboration, this command uses the DBLink or network connection between host and satellite to synchronize the data. The **Synchronize** dialog displays the progress of synchronizing your reference data with the host reference data.

**Synchronize Reference Data Dialog**

Displays the progress of synchronizing reference data.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

217/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Tasks**

Lists the individual parts of the reference data and displays their status in the synchronization process.

**View Log**

Opens the log file that is created when you perform a Workshare operation.

**Synchronize Reference Data from Host**

1. In Drawing Manager, select **Workshare** > **Synchronize Reference Data**.
2. When the synchronization process finishes, select **Close**.
3. Exit, then re-open Drawing Manager. You can now publish or get the latest version of drawings.

In order to synchronize the databases, the DBLink or other network connection between host and satellite must be active.

You can view the progress of the synchronization process on the **Synchronize** dialog.

If a satellite does not synchronize reference data, the satellite can neither publish nor get the latest version of a drawing.

For information about synchronizing reference data without a remote connection to the host, see

Synchronize Reference Data from a Copy.

**Synchronize Reference Data from Copy Command (Workshare Menu)** Typically used in a standalone Workshare collaboration, this command allows you to synchronize the reference data with a copy of the data as opposed to over a network connection. The **Synchronize** **Reference Data from Copy** dialog allows you to specify the directories or files that contain the copies of the reference data.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

218/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Synchronize Reference Data from Copy Dialog**

Specifies the paths to the copies of the specific reference data with which you want to synchronize your data.

**Rules library**

Allows you to specify the path to the rules file (Rules.rul) in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.

The path you specify for the rules library is also used to determine the path for the PlantConfig.xml file.

**Insulation specifications file**

Allows you to specify the insulation specification file (InsulationSpec.isl) in the copied reference data. By default, this file is located in the SmartPlant\P&ID Reference Data folder on your computer.

**Default report template path**

Allows you to specify the path to the default report templates folder in the copied reference data. This path typically points to the Report Files folder in the SmartPlant\P&ID Reference Data folder on your computer.

**Plant style file**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

219/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

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

**Browse**

Allows you to browse to the appropriate file or folder for the pertinent reference data.

**Schedule**

Opens the Schedule Task Wizard, which allows you to defer synchronizing data to a later time or to schedule it on a regular interval.

**Default Report Template Path Dialog**

Allows you to search for a folder on your computer or the local network. This dialog opens only when you are browsing for the **Default report template path** on the **Synchronize Reference Data from Copy** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

220/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Look in**

Lists the available directories. Choose a folder and select **OK**.

**Drives**

Displays the currently active drive. To change to another drive select **Network**.

**Network**

Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.

**P&ID Template Path Dialog**

Allows you to search on your computer or the local network for a folder. This dialog opens only when you are browsing for the **P&ID template path** on the **Synchronize Reference Data from Copy** dialog.

**Look in**

Lists the available directories. Choose a folder and select **OK**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

221/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Drives**

Displays the currently active drive. To change to another drive select **Network**.

**Network**

Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.

**Catalog Explorer Root Path Dialog**

Allows you to search for a folder on your computer or the local network. This dialog opens only when you are browsing for the **Catalog Explorer root path** on the **Synchronize Reference Data from Copy** dialog.

**Look in**

Lists the available directories. Choose a folder and select **OK**.

**Drives**

Displays the currently active drive. To change to another drive, select **Network**.

**Network**

Opens the Microsoft standard **Map Network Drive** dialog where you can specify a new active drive.

**Synchronize Reference Data from a Copy**

1. Select **Workshare** > **Synchronize Reference Data from Copy**.
2. On the **Synchronize Reference Data from Copy** dialog, select each **Browse** button and specify the paths to the copies of the reference data files.

You must have a live network connection to these files if they are not on your local computer.

1. Specify a path for every file listed on this dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

222/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Until every path is specified, the **OK** command is not available.

The path you specify for the rules library is also used to determine the path for the PlantConfig.xml file.

*The **Synchronize Reference Data** dialog opens and displays the progress of the synchronization* *operation.*

1. You can select **View Log** if you want to read notes on the synchronization operation.
2. Exit and then re-open Drawing Manager. You can now publish or get latest version of drawings.

If a satellite does not synchronize reference data, the satellite cannot publish or get the latest version of a drawing.

If you are using a Workshare environment in the Smart P&ID Modeler and you are at a satellite site, you should not store custom layouts for the **Engineering Data Editor** or Plant Filters because when you synchronize reference data, you lose that information.

You can select **Schedule** to defer this task to a later time or schedule it on a regular interval. When the Schedule Task Wizard opens, follow directions in the wizard to complete the scheduling of this

synchronizing operation.

**Synchronizing Shared Items**

Some drawing items, such as off-page connectors, instrument loops, and utility connectors, require special handling when using Workshare. Because these items can be shared by more than one drawing, any modifications made to a drawing at another site may have ramifications for the shared items contained in that drawing. Consequently you must synchronize these shared items.

**Connectors** (OPCs such as off-unit connector, off-page connector, and utility connector) To be sure that OPCs synchronize properly, when placing a connector in a drawing at your site, use the **Move Partner OPC** command in the Smart P&ID Modeler to specify the drawing at another site on which the partner OPC should be placed. After synchronizing shared items at both sites, the partner OPC is transferred to the drawing stockpile for the specified drawing at the other site.

**Plant Item Groups** (instrument loop, package, safety class, and test system) These items can be placed only in the stockpile. To share these items with another site, first place them in the stockpile in Smart P&ID and then set the **IsShared** property in the **Properties** window to **True**. After synchronizing shared items at both sites, this plant item group appears in the stockpile at the other site and can now be associated with items at that site, but can only be modified by the originating site.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

223/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Synchronize Shared Items Command (Workshare Menu)**

Opens the **Synchronizing Shared Items** dialog, which allows you to start and monitor the synchronization operation.

Run this command at the host and then at the satellite site.

**Synchronizing Shared Items Dialog**

Displays the progress of the synchronization operation.

**View Log**

Opens the log file that is created when you perform a synchronizing operation.

**Synchronize Shared Items**

1. Select **Workshare** > **Synchronize Shared Items**.
2. On the **Synchronizing Shared Items** dialog, select **View Log** to see the record of this synchronization operation.

If you want to defer this activity, or schedule it on a regular interval, you can select **Workshare** > **Schedule Synchronize Shared Items**. Follow the instructions on the Schedule Task Wizard.

**Sample Synchronize Shared Items Workflow**

Synchronizing shared items is an automated process in a connected Workshare collaboration but is unsupported in standalone Workshare. Shared items must be manually synchronized in standalone Workshare collaborations as shown in the sample workflow below.

1. Host creates Dwg1 and assigns to Site1 and creates Dwg2 and assigns to Site2.
2. Host publishes these two drawings and sends the resulting .zip files to their respective sites.
3. Site1 and Site2 perform a Get Latest Version from Local to receive their drawings.
4. Site1 places an OPC on Dwg1.
5. Site1 creates a new drawing, Dwg3.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

224/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Site1 moves the partner OPC from Dwg1 into the drawing stockpile of Dwg3.
2. Site1 publishes Dwg1 and Dwg3 and sends the resulting .zip files to the Host.
3. Host performs a Get Latest Version from Local on both drawings.
4. Host publishes Dwg1 and Dwg3 and sends the resulting .zip files to Site2.
5. Site2 performs a Get Latest Version from Local on both drawings.
6. Site2 moves the partner OPC from Dwg3 to the drawing stockpile of Dwg2.
7. Site2 places the OPC in Dwg2.
8. Site2 publishes Dwg2 and sends the resulting .zip file to the Host.
9. Host performs a Get Latest Version from Local on Dwg2. (The Host receives a moved items error condition and must move the OPC currently in Dwg3 to the plant stockpile before the **Get Latest** **Version from Local** command can succeed.)
10. Host publishes Dwg2 and sends to Site1.
11. Site1 performs a Get Latest Version from Local on Dwg 2. (Site1 receives a moved items error condition and must move the OPC currently in the Dwg3 stockpile to the plant stockpile before the **Get** **Latest Version from Local** command can succeed.)
12. Site1 opens Dwg 1 to cause the OPC label to refresh.

**Scheduling Workshare Tasks**

**Schedule Publish Command (Workshare Menu)**

Opens the Schedule Task Wizard, which allows you to schedule publishing the selected drawing or drawings at a later time or on a regular interval.

**Schedule Get Latest Version from Remote Command (Workshare Menu)** Opens the **Schedule Get Latest Version from Remote** dialog, which allows you to schedule getting a remote version of a drawing at a later time or on a regular interval. When you select **OK**, the Schedule Task

Wizard opens. Follow the prompts on the wizard to complete scheduling the subscription operation.

**Schedule Get Latest Version from Remote Dialog**

Specifies the site where the latest drawing versions reside. Selecting **OK** on this dialog opens the Schedule

Task Wizard.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

225/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Available Workshare Sites**

Lists the sites in your Workshare collaboration that have published drawings available to you. If the site you are looking for is not in the list, check to see if that site has published any drawings and, if so, has it assigned access to you.

**Schedule Synchronize Reference Data Command (Workshare Menu)** Opens the **Schedule Task Wizard**, which allows you to schedule synchronizing with the host reference data at a later time or on a regular interval.

**Schedule Synchronize Shared Items Command (Workshare Menu)**

Opens the Schedule Task Wizard, which allows you to schedule the synchronizing of shared items at a later time or on a regular interval.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

226/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Integration**

Smart P&ID can exchange design data with the following applications: Integration with Aspen Basic Engineering™

Integration with HxGN SDx2

Integration with SmartPlant Foundation

Integration with Smart Completions

**Registering Tools**

Before you can publish and retrieve documents from any of the other authoring tools, such as Smart Instrumentation or Smart Electrical, you must register each plant in Smart P&ID with a SmartPlant Foundation database (for Integration 1.0), HxGN SDx2 database (for Integration 2.0), or an Aspen Basic Engineering™ (ABE) database. On registering your plant, the connection allows Smart P&ID to use the **Integration** menu commands. Registration is performed by the System Administrator in Smart Engineering Manager and each plant must be registered only once in an authoring tool.

The software maps a plant and its relevant projects for SPF to a unique integration tool URL, which connects to a single integration tool plant database and its projects. When you use the **Register** command in any of the authoring tools, you are registering an authoring tool plant with the integration tool URL and plant that you specify.

In Smart Engineering Manager, you can register a plant with either SmartPlant Foundation or HxGN

SDx2, but not both. After the plant is registered with one of these integration tools, the option to register with the other tool becomes unavailable on the **Integration** menu.

A plant that is registered with SmartPlant Foundation or HxGN SDx2 can also be registered with ABE, and vice versa.

In Smart P&ID and Drawing Manager, the **Integration** menu is available only when you register a plant with an integration tool.

If a plant is registered with HxGN SDx2, only the Reshare command is available on the **Integration** menu. However, if the plant’s tool schema is older than the Smart P&ID schema version, only the

Upgrade Schema command is available. For plants registered with SmartPlant Foundation or ABE, the **Reshare** command is not available.

If a plant is registered only with ABE, only the **To Do List** command is available on the **Integration** menu. If you subsequently register an ABE plant with another integration tool, other relevant commands on the **Integration** menu become available.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

227/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Integration with HxGN SDx2**

Integrating Smart P&ID’s Project items with HxGN SDx2 optimizes the efficiency of digital technology. One of the challenges an organization faces when making any kind of design change is how to maintain the accuracy of the essential information (design, planning, engineering, maintenance, and operations). This accuracy is vital for safe and efficient operations.

To standardize and improve the data exchange of Smart P&ID’s asset information, HxGN SDx2 uses a simplified Common Schema. This Common Schema enables all tools to communicate in a single schema format. HxGN SDx2 stores this digital asset information in a centralized location.

Smart P&ID facilitates the sharing of items along with their associated documents with HxGN SDx2 for communication among the various authoring tools. The data sharing process with HxGN SDx2 is data driven and scheduler based. Smart P&ID employs a new service that runs automatically in the background.

The service monitors incremental changes in its database on a scheduled basis and compares data to HxGN SDx2’s database. Setting up the automated sharing service is a one-time task. As you work on your project, the sharing happens seamlessly. Furthermore, any changes made to items since the last comparison are shared with HxGN SDx2 and can then be used by other authoring tools.

These capabilities enable changes to an existing plant while ensuring strict change control and providing operations access to current information for running the plant safely and efficiently.

**Prerequisites**

Integration with HxGN SDx2 includes two services that must be installed and configured: Intergraph Schematics Scheduler Service

Smart P&ID Share Service

**Smart P&ID Share Service and Intergraph Schematic Scheduler Service** **Overview**

The** Intergraph Schematic Scheduler Service** is a separate software utility that monitors changes to plant items. Once you setup and start the scheduler service, the service synchronizes the changes with HxGN SDx2. Changes are then flagged for new, modified, or deleted plant items. Updates can then be shared with other Hexagon applications.

The **Intergraph Schematic Scheduler Service** needs to be configured using the **Schematic** **Scheduler Configuration Utility**. Before you setup a site using the **Configuration Utility**, make sure that **Smart P&ID Share Service** is installed.

The **Smart P&ID Share Service** enables integration with HxGN SDx2 and runs in the background. It is available with Smart P&ID as a separate feature and is located in the **Select Features to Install** section of the **Smart P&ID** installation DVD. You can also install the Share Service using the **Windows Control Panel > Programs > Programs and Features**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

228/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Here are the basic steps to setup and configure the services: 1. Ensure Smart P&ID Share Service is installed. See Install or modify Smart P&ID Select Features.

1. Install the Intergraph Schematic Scheduler.
2. Install Intergraph SmartPlant (.NET).
3. Configure the Intergraph Schematic Scheduler.
4. Start the Intergraph Schematic Scheduler Service.

The Smart P&ID Share Service, Intergraph Schematic Scheduler, and Intergraph SmartPlant (.NET) must be installed on the same workstation where Smart P&ID is installed.

To create enhanced mapping for integration, you must install Intergraph SmartPlant (COM) along with SmartPlant (.NET).

To use the Share Service with an Oracle client, you must install Oracle 64-bit client. The 64-bit Oracle client can coexist with the 32-bit client on the same host.

When an item is moved from the drawing to the plant stockpile and categorized under a plant group type - “Plant”, no relation will be established.

**Registering plants with HxGN SDx2**

Before you can share data between authoring tools and organizations using HxGN SDx2, you must register the plant in the authoring tool with the plant in HxGN SDx2. The relationship you create during this registration includes a tool signature or design component, which tracks where the data is coming from when shared. Each authoring tool can share with HxGN SDx2 and receive a unique tool signature. A new set of tables is created in the database as part of registration with the signature name. This allows HxGN

SDx2 to segregate data from different sources.

A system administrator typically configures the plant registration.

Depending on your organization’s policy and procedure, the plant and projects could have already been created in the HxGN SDx2 environment.

HxGN SDx2 supports SAM and Okta authentication.

The HxGN SDx2 login must have HxGN SDx2 **System Administration** and **Business Administrator** roles on the plant to which you are registering.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

229/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Prerequisites**

Before registering Smart P&ID with HxGN SDx2, ensure that the following prerequisites are configured in HxGN SDx2.

1. Sign in to HxGN SDx2. Your system administrator typically provides the URL and sign-in credentials.
2. Ensure the user exists in HxGN SDx2 and belongs to the respective organization. See Update a user.
3. Ensure the user has at least **Business Administrator** and **System Administration** roles assigned.

See Assign roles to a user in a configuration.

1. Make sure the HxGN SDx2 project has a work area and work package.

Create a work area

Create a work package from work area

**Register a plant with HxGN SDx2**

1. Obtain the **Server Url** and **Client ID** from your HxGN SDx2 administrator.
2. Register the plant in Smart Engineering Manager. See Registering a plant with HxGN SDx2.

You must register each plant in Smart Engineering Manager once.

**Prerequisites for registering with HxGN SDx2 (SPID)**

Before registering Smart P&ID with HxGN SDx2, ensure that the following prerequisites are configured in HxGN SDx2.

1. Sign in to HxGN SDx2. Your system administrator typically provides the URL and sign-in credentials.
2. Ensure the user exists in HxGN SDx2 and belongs to the respective organization. See Update a user.
3. Ensure the user has at least **Business Administrator** and **System Administration** roles assigned.

See Assign roles to a user in a configuration.

1. Make sure the HxGN SDx2 project has a work area and work package.

Create a work area

Create a work package from work area

**Share data and documents with HxGN SDx2**

Smart P&ID can continuously share data and documents with HxGN SDx2 using the Schematic Scheduler Service. The sharing process occurs on a set schedule as configured in the Schematic Scheduler Service.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

230/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Functional Considerations**

The Schematic Scheduler Service does not share a drawing if it is open in the Smart P&ID Modeler.

Share from projects is not supported.

The service does not support sharing duct runs and certain ducting components.

The service does not support sharing relations between the following item types and PBS items: Pipe runs

Piping components

When an item is moved from a drawing to a stockpile, the system removes all its relationships with the PBS. HxGN SDx2 automatically assigns the item to a Work Area (WA).

**Reshare data and documents with HxGN SDx2**

Ensure the plant is registered with HxGN SDx2.

**Reshare plant items**

1. In the **Engineering Data Editor**, select **Push Plant Item** or **Push Plant Group** from the select list.
2. Select one or more items to reshare with HxGN SDx2.

In the **Reshare** column, notice that the status of selected items is **False**.

1. On the main menu, select **Integration** > Reshare.

*The software changes the **Reshare** status of the selected items to **True**. After the next sharing cycle* *completes, the **Last Publish Time** gets updated, and the **Reshare** status of the selected items* *changes back to **False**.*

**Reshare drawings**

1. In the **Engineering Data Editor**, add **Drawing Name** column to the view.
2. On the **SDx Class Def** column, select **Filter** , and then apply **[Empty]** data filter.
3. Select **Push Plant Item** or **Push Plant Group** from the select list.
4. Select one or more drawings to reshare with HxGN SDx2.

In the **Reshare** column, notice that the status of selected drawings is **False**.

1. On the main menu, select **Integration** > Reshare.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

231/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

*The software changes the **Reshare** status of the selected drawings to **True**. After the next sharing* *cycle completes, the **Last Publish Time** gets updated, and the **Reshare** status of the selected* *drawings changes back to **False**.*

**What do True and False reshare statuses mean?**

**True** indicates that you have explicitly marked the item to be reshared with HxGN SDx2, overriding the default sharing behavior. All of the mapped properties of the item are pushed to HxGN SDx2 in the next sharing cycle, as configured in the Schematic Scheduler.

**False** indicates that the software determines if the item needs to be shared with HxGN SDx2, based on the default sharing behavior.

The **Start Publish Time** column is currently not supported.

**Reshare Command**

The **Integration** > **Reshare** command allows you to explicitly share P&ID items and drawings with HxGN

SDx2 in the next sharing cycle. By default, the software shares an item with HxGN SDx2 only if any of its properties have changed since it was last shared. However, it does not automatically share the newly mapped properties if their values have not changed.

This command is available only if the P&ID plant is registered with HxGN SDx2.

**Integration with SmartPlant Foundation**

Integration standardizes and improves the communication among the various authoring tools you use in the course of designing, constructing, and operating a plant. Integration manages data exchange among these authoring tools, which enables sharing and re-use of plant information throughout the plant life-cycle.

SmartPlant Foundation acts as a repository for data and a medium through which information is shared among other tools, such as Smart Instrumentation, Smart Electrical, and Smart 3D.

Most integration commands are available on the menu in Smart P&ID and Smart P&ID Drawing Manager.

The following graphic displays what Smart P&ID publishes and retrieves and shows the flow of data and the different types of data.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

232/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Smart P&ID interacts with SmartPlant Foundation by correlating items between the plant database and the SmartPlant Foundation database by retrieving documents from SmartPlant Foundation. Also, Smart P&ID

creates a set of tasks in the To Do List that you can run to update the plant database. In Smart P&ID, you can also use the commands on the menu to publish documents and retrieve data, access SmartPlant Foundation to browse data, and subscribe to change notifications and compare documents.

You can only use the menu commands after your plant is registered. See Registering Tools.

**Tool Requirements for Integrating Smart P&ID**

This topic describes rules and settings that allow Smart P&ID data to be shared correctly with Aspen Basic Engineering, Smart Instrumentation, Smart 3D, and the other tools that are part of an integrated environment. Other tools that are not listed here have no known Smart P&ID/integration issues.

**General Integration Requirements**

The following is a list of *best practice* scenarios for using Smart P&ID so that data will migrate correctly to other tools:

In general, when modifying P&IDs that have been published, avoid unnecessarily deleting items in order to move them inside the active drawing or moving them to other drawings. Deleting and replacing items (with the same tag), causes additional work in applications retrieving the P&IDs that might negate the time-saving benefits of the P&ID changes.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

233/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

When working with Projects and As-Built, all instruments to be published must be placed on a P&ID

drawing or in the active drawing stockpile. This is because the plant stockpile is not communicated back and forth between Projects and As-Built.

To enable publishing from a project, you must create a project in SmartPlant Foundation with the same name (case-sensitive) as the P&ID project.

When creating symbols, connection points (piping, signal, and auxiliary) must be added in the correct sequence. See the Important note at the end of Place Point Ribbon (Smart P&ID) in Catalog Manager Help.

Signal points and piping points are not supported for Equipment and Equipment Components when publishing to SmartPlant Foundation.

When creating formats for use with Smart P&ID publishing, the formats must be added and mapped in SPPIDDataMap.xml using Schema Editor. The UID string of the custom SPMapUOMDef map file must be of the form *SPMU__* , where ‘NN’ represents the SPMapUOMListDef ID

for the format type (for example Temperature = 5; Pressure = 27). Because spaces or restricted characters are not allowed in the UID string, custom format names must not include spaces or restricted characters.

If you intend to publish select lists (enum lists) to SmartPlant Foundation, make sure that you review the SmartPlant Adapter for Smart P&ID Help to understand the requirements (see under *Data* *Transformation Logic* > *Publish/Retrieve*).

If the Smart P&ID item tag validation allows for duplicate tags, this might have an impact on downstream tools such as Smart Instrumentation, which does not allow duplicates. In such cases, allowing duplicates in Smart P&ID can cause problems in the retrieving tool.

By default, Smart P&ID item tag validation does not allow duplicate item tags for loops or instruments.

**Integration with Smart Instrumentation**

**Retrieving Documents**

If a Smart P&ID drawing that includes items with a flow direction is to be retrieved by Smart Instrumentation, a flow direction of **End 1 Upstream** or **End 1 Downstream** must be defined in Smart P&ID. Bi-directional flow is not supported.

**Connect to Process Lines**

**Connect to Process** lines are required for connecting instruments to equipment nozzles and pipe runs in Smart P&ID.

All non-piped offline equipment instruments must be connected to vessels through non-electric signal lines and nozzles in Smart P&ID. This enables Smart Instrumentation to recognize that instruments are https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

234/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

connected to vessels.

If Smart P&ID assigns an object to an intermediate level in the hierarchy and publishes, Smart Instrumentation assigns the object to the level in the hierarchy in Smart Instrumentation determined by their logic. Because instruments belong to units in Smart Instrumentation, an instrument assigned to the intermediate level in Smart P&ID will be assigned to the unit in Smart Instrumentation. Panels will be assigned to the plant. Smart P&ID might get an update on retrieve to move the object to another level in the hierarchy than where it was published based on the move done automatically by Smart Instrumentation.

Panels will move to the top level; instruments will move to the bottom.

**Deleting and Adding Items**

When you are working in a Projects environment, and items are correlated using the SmartPlant integration tools, you should minimize deleting and re-adding any items. Smart P&ID reuses tag numbers in the numbering scheme when you delete and re-add items. Smart Instrumentation tracks tag numbers claimed in a project, and this tracking does not work if tag numbers are reused after correlation. If you must delete an item in this situation, you can delete the item to the Smart P&ID Stockpile.

**Instrument Expansion**

A Smart P&ID instrument or loop tag does not always have a 1:1 relationship with instruments in Smart Instrumentation. In some cases, a single item tag in a P&ID corresponding to an instrument or loop needs to be expanded to create several instruments when publishing the data for Smart Instrumentation. For this purpose, the **Expansion Type** property in Smart P&ID specifies the expansion behavior when publishing an instrument or loop. Each value of the property corresponds to a Smart Instrumentation rule that determines which instrument types and numbers are to be created in Smart Instrumentation when the Smart P&ID tag is expanded and retrieved.

When retrieving data back to Smart P&ID, the behavior of a particular instrument created by expansion is determined by Smart Instrumentation parameters. For an expanded instrument, the state of the IRetrievableExpansion interface determines whether that instrument will be retrieved by Smart P&ID: if the IRetrievableExpansion interface is realized, the instrument is retrieved, whereas if the IRetrievableExpansion interface is *not* realized, the instrument is not retrieved. The ‘parent’ item tag is *always* retrieved, regardless of the realization state of the IRetrievableExpansion interface.

**Ports**

Smart Instrumentation uses physical ports, while Smart P&ID uses logical ports. Smart Instrumentation publishes the physical ports with the Dimensional Data Sheets and not the Instrument Index. Smart P&ID

retrieves the Instrument Index and does not retrieve the Dimensional Data Sheets.

When the workflow goes from Smart P&ID to Smart Instrumentation, followed by Smart Instrumentation publishing the Dimensional Datasheet, a Same As relationship is created between the ports in the SmartPlant Foundation database. That Same As relationship is required by Smart 3D to correctly match the design basis ports to the 3D representation of the ports.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

235/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

However, when the workflow goes from Smart Instrumentation to Smart P&ID, a Same As relationship is not created in the SmartPlant Foundation database. Without the Same As relationship created in the SmartPlant Foundation database, the result might be additional ports in Smart 3D. To obtain the Same As relationship on the ports requires that Smart P&ID publish the P&ID with the instrument, this P&ID be retrieved by Smart Instrumentation and then having Smart Instrumentation publish the Dimensional Data Sheet.

**Integration with Smart 3D**

**General**

In Options Manager, ensure that under **Settings**, the **Use Piping Specification** setting value is **Smart 3D**

even if the P&ID plant is not validating piping specifications. This is to ensure that the required Piping Component Select List entries are properly set to match the PIP short codes expected by Smart 3D. See *Configure Piping Specification Settings* in Smart P&ID * * Options Manager User’s Help.

**Drawing Items**

For Smart 3D to properly determine flow direction in a process run, that process run must be connected to at least 2 items.

Some items that can be represented as single objects in Smart P&ID, such as Vent Detail, are modeled in Smart 3D as a set of separate objects. For full correlation to be established between the two tools, ensure that these objects are modeled in Smart P&ID with the same configuration used to represent them in Smart 3D.

**Properties**

Smart 3D handles temperature and pressure properties in pairs and does not support having a temperature (for example, Normal Operating Temperature) without defining the matching pressure (in this case, Normal Operating Pressure). While this is a valid condition for Smart P&ID, it should be a consideration when publishing for retrieval into Smart 3D. Without the Pressure / Temperature pair of values defined, the Smart 3D user will be required to enter a value that was not defined in Smart P&ID.

**Integration with Aspen Basic Engineering**

**Retrieving Documents**

Basic Engineering data sheets can contain multiple objects and can be formatted in a traditional data sheet view or list view (for example, as an equipment list). Data sheets retrieved from Basic Engineering might include stream data, specialty piping data, or relief valve data as required by business practices.

**Using the Catalog Index in Smart P&ID and SmartPlant Integration** When you select the **Retrieve** command, the software accesses the CatalogIndex.mdb and the system performs the following actions:

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

236/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Using the retrieved document, the object type and classification of the retrieved item is determined.
2. Using the Smart P&ID Map file, the ItemTypeName (Equipment, PipeRun, PipingComp, Loops, and so forth), and codelist indices for Class, Sub-Class, and Type are determined.

**Catalog Index Lookup**

The Catalog Index file is used to find a symbol in the catalog with type properties that match the given values. The lookup is performed using the most specific information first. If a match is found, that symbol is used. However, if there is no match, the more generic type information is used for additional searches. In this way, a generic symbol will be returned if no specific symbol is available in the catalog.

**Search Based on Type Value**

Searches the catalog index for all rows with matching ItemTypeName and Type values and IsDefaultForType = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software performs the search based on Subclass.

**Search Based on Subclass Value**

Searches the catalog index for all rows with matching ItemTypeName and SubClass values and IsDefaultForSubclass = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software performs the search based on Class.

**Search Based on Class Value**

Searches the catalog index for all rows with matching ItemTypeName and Class values and IsDefaultForClass = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software returns an empty string.

**Accessing the SmartPlant Foundation Web Client**

The SmartPlant Foundation Web Client provides a web-based user interface that allows you to interact with SmartPlant Foundation. From this interface you can perform a number of tasks, such as browse data and documents that have been published, use the SmartPlant Foundation To Do List to complete workflow tasks, compare document revisions and published documents with tool data, and subscribe to documents to receive notification of document changes.

**Access the SmartPlant Foundation Web Client from Drawing Manager** Select **SmartPlant** > **Browser**.

This functionality is available only if you have registered the active plant using the SmartPlant Registration Wizard. For more information, see Register from Smart Engineering Manager in the *Smart Engineering Manager Help*.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

237/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

From the SmartPlant Foundation Web Client, you can perform a number of tasks, such as publishing or retrieving documents, comparing documents, subscribing to document changes, and so forth. Many of these tasks can be performed from the authoring tools, such as Smart P&ID or Smart Electrical, but the Web Client provides unique access to other features such as the Web Client To Do List and search capabilities.

**Browser Command (SmartPlant Menu)**

Opens the SmartPlant Foundation Web Client, from which you can perform a number of tasks, such as browsing for documents that have been published, using the SmartPlant Foundation To Do List to complete tasks, comparing documents in the SmartPlant Foundation database with the data in your authoring tool, and subscribing to documents to receive notification of changes to the documents.

This command is available only if you have registered the active plant using the SmartPlant Registration Wizard.

**Revising Documents**

The software implements drawing revisions in different ways depending on your work environment. If you are working in an integrated environment, when you select the **Revisions** > **New Revision** command in Drawing Manager, the software opens either the SmartPlant Foundation **Revise** dialog or the **New** **Revision** dialog, depending on the option selected in Options Manager for the **Revision Management** **Software for Publishing Documents** setting. If you want to associate a version with a new revision in an integrated environment, you must select the drawing and run the **Revisions** > ** Associate Version** command after creating the revision.

The document revision process is separate from the publishing process, making it possible to revise a document locally and in SmartPlant Foundation and save the revision values to the tool database without re-publishing the document.

Revising a document creates a revision for the document with major and minor revision values set, depending on the revision schema selected. When revising a document, you can modify the major and minor revision data on the document.

You can change the revision scheme after a document has been published, skip revision numbers, and manually add a revision number, then have it validated against the revision scheme. It is not required to assign a minor revision number. Also, revision data from tools is supported even if the document has previously been revised in SmartPlant Foundation.

You can revise a document by using any previous revisions that are available from the last published revision.

**Example**

If you revise a new document using the revision scheme RevAlpha (A, B, C, D…) and revision C, then SmartPlant Foundation reserves revision number C for the document. Revising the same document with https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

238/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

RevAlpha, you can now revise with any previous revision numbers, such as A or B. However, if the document is published to SmartPlant Foundation with revision number C, you are not allowed to go back to the previous revision numbers.

The following table contains the available revision numbers based on the document revision state in SmartPlant Foundation:

**Document revision state**

**Next available revision number**

Working (C)

C and up

Current (C)

D and up

The combination of the major and minor revision values must be unique in the plant, or when working with As-Built, in the project.

When you check out or fetch a drawing from the As-Built into a project, only the last revision record is displayed in the **Revision History** dialog, regardless of whether that revision is associated with a version or not.

Deletion of revisions is allowed in a non-integrated environment. Deletion of revisions is also allowed in an integrated environment where revisions are managed by Smart P&ID, provided the revised drawing has not yet been published and regardless of any permission settings. Revision deletion is performed in the **Revision History** dialog.

**Revise Drawings Using SmartPlant Foundation Revisions**

1. Select one or more drawings for revision.
2. Click **Revisions** > **New Revision**. The Revise Dialog displays.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

239/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

This command is available only if you have registered the active plant using the SmartPlant Registration Wizard and if the authoring tool has implemented the SmartPlant Foundation revision functionality.

You can revise documents in an integrated environment from the **Publish** dialog box. For more information, see Revisable and Locked Documents for COM environments or Revisable and Locked Documents .NET * * for .NET environments.

1. For a new document or a document that does not yet have a defined revision scheme, select the revision scheme you want to use from the **Revision Scheme Name** list.

Only revision schemes that are applicable to the configuration (plant) or classification (document type) are available in the shortcut menu. The revision schemes related to a configuration or classification are not available for any other configurations or classifications. If none of the revision schemes are related to the configuration or classification, then all revision schemes are available unless they are related to any other configuration or classification. See Configure different revision scheme strategies.

Any revision scheme that was previously assigned to a document can be changed even if the document has been published or retrieved. For example, if the original revision scheme for a document was set as Rev01A, you can change the revision scheme to Rev1A at any time.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

240/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Revision schemes can be set at any level of the document hierarchy.

You can revise a document that has been previously signed off and it can be re-published into SmartPlant Foundation.

1. In the **Revise in Tool** section, select the next available major and minor revision values.

The current revisions of the tool will not be available in the **Major** and **Minor** list. You can select the current revisions of the tool only if they are not active.

If the **Allow skipping revisions** option is set to **False** on the **Manage Integration Options** dialog box in SmartPlant Foundation Desktop Client, you are limited to which revisions you can select.

1. Click **OK**. The document currently available for retrieval by other authoring tools is not updated until you publish this revised document.

After creation of the revisions, the drawings remain selected.

**Use Minor Revisions from SmartPlant Foundation in Smart P&ID**

The following example explains how Smart P&ID supports minor revisions. This example creates a revision from a new P&ID document.

1. Select **Revisions** > **New Revision**.

If you logged on to the authoring tool with a user name that is not defined in the integrated environment, you are prompted to log on when you use this command.

1. On the **Revise** dialog, select the revision scheme you want to use from the **Revision Scheme** list. In this example, **Rev1A** is the revision scheme.
2. In the **Major** list under **Revise in Tool,**  select **1**. This is the first available major revision number.
3. In the **Minor** list under **Revise in Tool**, select **A**. This is the first available minor revision number.
4. Revise the document and keep the **Major** revision number as **1**.

*The minor revision number is automatically incremented and becomes **B**.*

1. Revise the document and change the **Major** revision number to **2**.

*The minor revision number begins again at **A**.*

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

241/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Scenarios for Revision Scheme Behavior**

In an integrated environment, you can use SmartPlant Foundation revisions. You can change revision schemes, skip revisions, and switch between using and not using minor revisions. A number of dependencies, such as a tool revision scheme or whether a document has other revisions, influence the behavior of a document when a revision is created in SmartPlant Foundation.

1. Click **Revisions** > **New Revision**. The Revise Dialog displays.

This command is available only if you have registered the active plant using the SmartPlant Registration Wizard and if the authoring tool has implemented the SmartPlant Foundation revision functionality.

You can revise documents in an integrated environment from the **Publish** dialog box. For more information, see Revisable and Locked Documents for COM environments or Revisable and Locked Documents .NET * * for .NET environments.

1. In the **Revision Scheme** list, select** RevA01**.
2. In the **Revise in Tool** > **Major** list, select **B** as the major revision for the document.
3. Click **OK**. The revised document is saved to the authoring tool database. The document currently available for retrieval by other authoring tools is not updated until you publish this revised document.
4. Revise the document again. In the **Revise in Tool** > **Major** list, change the major revision to **C**.
5. Click **OK**.
6. Publish the document.

The document is revised in a tool to make additional changes. The tool manages its own revision schemes and sets the revision of the document to **5**. Rather than selecting a revision scheme to match the tool revision scheme, you choose a new revision scheme.

1. Click **Revisions** > **New Revision**. The Revise Dialog displays.
2. In the **Revision Scheme** list, select** RevA01**.

In the **Revise in Tool** > **Major** list, the first major revision is **A**. **A** is the first available revision because the document has not been previously published in SmartPlant Foundation.

**Revise Dialog**

Allows you to revise a document in the authoring tool without publishing it.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

242/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Boxes with a shaded background are read-only and cannot be edited.

An asterisk appears in a box if more than one document is selected or the documents have different values for what is displayed.

**Engineering Tool**

Displays an authoring tool-specific dialog that allows you to select documents to add to the tree view list.

**Delete**

Allows you to remove a document from the tree view list.

**Documents list**

Displays a list of the documents selected to be revised (see Revise a Document). You populate this list by selecting documents before activating the **Revise** command. You can select the **Delete** button to remove documents from this list.

**Revision Scheme > Name**

Choose the revision scheme to be applied from the list of available options. Only revision schemes that are applicable to the configuration (plant) or classification (document type) are available in the drop-down menu.

If none of the revision schemes are related to the configuration or classification, then all revision schemes are available. For more information on revision schema configuration, see Configure different revision scheme strategies.

**Revision Scheme > Major Type**

For the selected revision scheme, this box displays the type of the major revision value sequence in read-only format.

**Revision Scheme > Minor Type**

For the selected revision scheme, this box displays the type of the minor revision value sequence in read-only format if the revision scheme contains a minor revision scheme.

**Current Revision in Tool** > **Major**

For existing documents, this box displays the current major revision of the document, as defined in the authoring tool, in a read-only format. For new documents, this box is empty.

**Current Revision in Tool** > **Minor**

For existing documents, this box displays the current minor revision of the document, as defined in the authoring tool, in a read-only format. If the revision scheme does not use minor revision, or if the selected document has not yet been revised, this box is empty.

**Revise in Tool** > **Major**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

243/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

From this list box, choose the major revision value for the document to revise it locally and to reserve the revision in SmartPlant Foundation.

**Revise in Tool** > **Minor**

From this list box, if you want a minor revision value, choose a minor revision value for the document to revise it locally and to reserve the revision in SmartPlant Foundation.

An Administrator can disable the skipping of revision numbers using the** Manage Integration** **Options** in the SmartPlant Foundation Desktop Client. For more information, see Configure Allow skipping revisions.

**Publishing Documents**

In an integrated environment, you must publish documents containing the drawing data and relationships before the authoring tools can share this information. The publishing process involves selecting a document to publish, assigning it to a workflow (if necessary), and specifying a revision and version of the document if specified in SmartPlant Foundation. For most documents, the associated data is included in the publishing process.

The authoring tools publish data in XML format. The software then places the .XML file in the appropriate SmartPlant Foundation vault and loads the data from the .XML files to the SmartPlant Foundation database.

After the document is published, users can retrieve the data from the .XML file in the SmartPlant Foundation vault into other authoring tools.

When you publish documents, the software does the following things: Creates a new master document and the first revision in SmartPlant Foundation the first time you publish a particular document. From that point on, the software creates new versions and revisions when the document is subsequently published. The software relates revisions to the master document. You can publish subsequent revisions into a workflow, which can be a different workflow than assigned in the original publish. Changes in the document status of a related revision change the status of the subsequently published versions and revisions of the document.

Publishes a visual representation of the document that you can view without the authoring tool. For many applications, this is an Intergraph proprietary file, called a RAD file. The viewable file can also be an Excel spreadsheet or another viewable file type, such as .pdf or .doc. You can review and mark up the visual representation of the document, which is attached to the document revision, using SmartPlant Markup.

Publishes associated data, depending on workflow approval. If the data is approved and loaded, it is used for reporting and subsequent retrieval by downstream applications when the tools retrieve latest data. The software publishes only meaningful engineering data. The published data is not enough to re-create the document in the originating tool.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

244/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Places the published .XML file and any view files in the appropriate SmartPlant Foundation vault. This

.XML file can be retrieved when users in the authoring tools retrieve as-published data.

Sends notification to the publishing tool.

For more information about revisions and versions, see Revisions and versions.

**Reasons to Publish**

You can publish documents and associated data for several reasons: To exchange and enhance data among tools, to avoid creating data multiple times in multiple authoring tools

To report on common data originating in multiple tools

To provide enterprise-wide accessibility to published documents To manage change, including workflow history and document revision management You can also publish documents to share information with users in other tools without going through a formal workflow. To share data, you can publish a document to a “for sharing” workflow that has only a load step, so that the data in loaded into SmartPlant Foundation as soon as you publish the document.

You can also publish a document by not assigning the document to a workflow, but rather by using the default workflow from SmartPlant Foundation. When you do not select a workflow for a document during publishing, the SmartPlant Loader Manager loads the document into SmartPlant Foundation as soon as it reaches the top of the Loader queue.

**Publishing Documents**

Each authoring tool publishes different documents and data. The following list contains each authoring tool that is part of integration, the document types that each tool publishes, and information about whether data is also published with each document type.

**Aspen Basic Engineering**

Process Flow Diagrams (PFD)

Equipment Datasheets — documents and data

Equipment Lists (published as Equipment Datasheets) — documents and data Stream Datasheets (published as Equipment Datasheets) — documents and data **Smart P&ID**

Piping and Instrumentation Diagram (P&ID) — documents and data https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

245/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Smart Electrical**

Electrical I/O Lists — documents and data

Electrical Power Elements — documents and data

Cable Schedules — documents and data

**Smart Instrumentation**

Instrument Index — documents and data (limited)

Instrument Specification Sheets — documents

Dimensional Data Sheets (DDP) — documents

Instrument Process Data Sheets (IPD) — documents

Instrument Loop Drawings

I/O Assignments — documents

Electrical Signal Lists

Browsers (viewable file with links to data) — documents and data **Smart Engineering Manager**

Does not publish

**Smart 3D**

3D Model Data (Smart Review File Type)

3D Cable Data (Smart Review File Type)

Orthographic Drawings — viewable file with links to data

Isometric Drawings — viewable file with links to data

Reports — viewable file with links to data

**PDS**

Model

Orthographic Drawings

Isometric Drawings

Reports

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

246/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**SmartPlant Foundation**

Plant Breakdown Structures (PBS)

Project Breakdown Structure

Project Definition Documents

Project Lists

Instrument Process Datasheets (IPD)

Equipment Lists

Instrument Master Lists

The PBS document published by SmartPlant Foundation contains information about the physical plant with a structure consisting of plants, areas, and units. The default structure is plant/area/unit, but you can define a custom hierarchy in the Schema Editor. When a PBS document is published from SmartPlant Foundation, the authoring tools are notified about the plant, areas, and units that need to be created in each authoring tool.

The project breakdown structure, project definition document, and project list contain information about projects and their statuses. When these documents are published from SmartPlant Foundation, the authoring tools are notified of projects and contracts that need to be created in the authoring tools.

The project breakdown structure contains a single project and the hierarchy of contracts under that project in a plant/project structure. The project definition document contains information for a single project that needs to be created in the authoring tool. The project list contains a list of all projects in a plant, and it is used by those authoring tools that create all projects at one time.

The plant breakdown structure and project breakdown structure used in the authoring tools must match the structure in SmartPlant Foundation for publishing from the authoring tools and object correlation to work correctly.

When you publish data from an authoring tool, you might not be able view all the properties that you published in the SmartPlant Foundation client. You can customize view definitions to allow you to see additional properties. For more information about defining view definitions in the SmartPlant schema, see Working with View Definitions and Create a View Definition in the Schema Editor User’s Guide.

For further assistance with visualizing data in SmartPlant Foundation, contact Intergraph Support Services.

When publishing from a project, an instruction container, which contains all the claimed objects, is created within the tombstone file.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

247/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Publishing Files without Data**

You can also browse to and publish other file types, such as Microsoft Word, Microsoft Excel, or SmartSketch files. These documents are always published without data. The primary reason to publish documents without data is so that you can manage document changes and reviews using workflows and view the document electronically using the SmartPlant Foundation Change Management functionality.

**Publishing from Smart P&ID Drawing Manager - Work Process**

- This step applies to a plant that is configured to use SmartPlant Foundation revisions. If your plant is configured to use Smart P&ID revisions, a new revision is added in the Smart P&ID **Revise** dialog.

**Publish Documents from Smart P&ID Drawing Manager**

Before you can publish a document for the first time, at least one revision of that document must exist. The software finds only those documents that have revisions. If a document has several revisions, the software finds the most recent revision of that document.

This functionality is available only if you have registered the active plant using the SmartPlant Registration Wizard. See Register from Smart Engineering Manager.

If you logged on to the authoring tool with a user name that is not defined in the integrated environment, you are prompted to log on when you use this command.

1. Select the drawings you want to publish.
2. Select **SmartPlant** > **Publish**.

A plug-in can be created that will allow user intervention to modify, add, or remove information from data to be published before it gets transmitted to SmartPlant Foundation. See Pre-Publishing Automation from Smart P&ID.

1. Select **Engineering Tool** in the **Share** dialog to open the **Find** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

248/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Opens the **Publish from Engineering Tool** dialog for selecting documents.

**File System**

Opens a standard Microsoft dialog that allows you to select files. When you select a file with this **Select File** dialog, the **Document Properties** dialog displays, allowing you to specify information about the file, such as whether it is a new file; the category, type, and subtype of the document; and the name, description, and title of the document.

**Find**

Opens the **Find Documents to Publish** dialog, which allows you to search for documents. These are documents that have at least one revision and that were not published after creation of the last revision.

See Find Documents to Publish Dialog.

The documents that display in the **Selected documents** list in the **Publish** dialog when it first opens are publishable documents that were selected within the authoring tool before you selected the **Publish** command.

Edit properties as required for the selected documents. When multiple documents are selected, only property values shared by all the selected documents appear in the grid. Changing a value in the grid changes that value for all the selected documents. If you must remove an entry (or node) from the **Selected documents** list, select the node in the tree, and then select **Delete**

.

1. From the **Operations** list, choose a publish method. Select **Publish** to start the publishing process.

Publishing starts as soon as you select **OK**.

Select **Background** **publish** to publish the selected documents immediately as a separate process, allowing you to perform other tasks at the same time. When you use this feature, an e-mail message alerts you when the process is complete.

If the authoring tool supports scheduled batch publishing, select the **Scheduled publish** option to indicate that the publish process should be run in batch mode.

1. Select **OK** to complete the procedure.

During publishing, an information dialog appears with a progress bar. Select **Show Details** to view details of the operation showing steps completed successfully, the current step that is running, and steps yet to run. You can select **Hide Details** to hide this section of the dialog. If the **View Log** button is enabled, it provides operation messages including errors, warnings, and information. Select **View** **Log** to view these messages.

The SmartPlant Schema file must be checked into SmartPlant Foundation when you publish. If the publish operation fails, contact your SmartPlant Foundation system administrator to make sure the https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

249/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

SmartPlant Schema is checked into SmartPlant Foundation.

**Issue Request Documents from Smart P&ID Drawing Manager** Before you can publish a document for the first time, at least one revision of that document must exist. The software finds only those documents that have revisions. If a document has several revisions, the software finds the most recent revision of that document.

1. Select the drawings you want to issue requests for.

This functionality is available only if you have registered the active plant using the SmartPlant Registration Wizard. See Register from Smart Engineering Manager.

If you logged on to the authoring tool with a user name that is not defined in the integrated environment, you are prompted to log on when you use this command.

1. Select **Integration** > **Publish**.
2. In the **Publish** dialog, click the **Issue Request** tab.
3. In the **Issue to** box, select the contract to which you want to assign the document or documents.
4. Under **Selected documents**, select the documents you want to associate with the specified contract.
5. Select **Engineering Tool** in the **Share** dialog to open the **Find** dialog.

Opens the **Publish from Engineering Tool** dialog for selecting documents.

**File System**

Opens a standard Microsoft dialog that allows you to select files. When you select a file with this **Select File** dialog, the **Document Properties** dialog displays, allowing you to specify information about the file, such as whether it is a new file; the category, type, and subtype of the document; and the name, description, and title of the document.

**Find**

Opens the **Find Documents to Publish** dialog, which allows you to search for documents. These are documents that have at least one revision and that were not published after creation of the last revision.

See Find Documents to Publish Dialog.

The documents that display in the **Selected documents** list in the **Publish** dialog when it first opens are publishable documents that were selected within the authoring tool before you selected the **Publish** command. To remove documents from the list, select them and then click the **Delete** toolbar

button.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

250/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Click **OK** to issue the contract request for the selected documents to the integrated environment.
2. Start SmartPlant Foundation Desktop Client on your computer and search for the published document to verify the publishing process.
3. Right-click the document in the Desktop Client tree view and on the shortcut menu, click **Refresh**.
4. Update the document. For more information, see the *SmartPlant Foundation Desktop Client User’s* *Guide*.
5. Review the issue properties by right-clicking the document and on the shortcut menu, clicking **Properties**, and then clicking the **Issue Request** tab to see the issue information. You can also open the document to see the issue information in the title block.
6. Publish the document with the updated issue information.

**Publish Command (SmartPlant Menu)**

Opens the Publish dialog to allow you to send the information of the selected documents for retrieval by

other tools.

**Publish Dialog**

Provides a list of documents selected to publish.

**Selected documents**

Displays a list of the documents selected for publishing. You must populate this list by selecting documents before you use the **Publish** command or by using the buttons in the **Add** section of this dialog. For each document, this list displays the name, the type of document, the workflow from which the document was last published, the revision and version numbers, the revision scheme, and the date when the document was last published.

**Engineering Tool**

Displays a tool-specific dialog that allows you to add documents from authoring tools, such as P&IDs or PFDs, to the **Selected documents** list.

**File System**

Opens the standard **Select File** dialog that allows you to select documents, such as Microsoft Word documents or Microsoft Excel workbooks, to add to the **Selected documents** list. When you select a file using this dialog, the **Document Properties** dialog opens, allowing you to specify information about the file, such as whether it is a new file or was previously published; the category, type, and subtype of the document; and the name, description, and title of the document.

**Find**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

251/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Opens the **Find Documents to Publish** dialog, which allows you to search for documents to add to the **Selected documents** list.

**Advanced**

Opens the **Advanced Publish Options** dialog, which allows you to search for files that are of a specific type and that have been updated since they were last published.

**Remove**

Removes the selected file or files from the **Selected documents** list.

**Contract**

Opens the **Contract** dialog, if applicable. This command is available only if it is defined by your project implementation team.

**Batch publish**

Indicates that the system publishes the selected documents in batch mode (that is, in the background). You are notified by e-mail when the operation is complete. If this option is not selected, the documents begin to be published as soon as you select **OK**.

You can select rows that are in white on this dialog. Rows that are gray are provided for viewing purposes only and cannot be selected.

**Publish Tab (Publish Dialog)**

Displays properties of the selected document or documents. If only one document is selected in the tree view, the properties displayed on this tab are the properties of that one document. If multiple documents are selected, only the properties with the same value for all documents are displayed. Any properties with varying values across the documents appear as blank values in these fields.

You can change some of the values assigned to one or more documents by changing the values displayed in the table. The values you enter here will override any existing values for all selected documents.

**Last Published**

Indicates the date on which the document or documents were last published.

**Name**

Displays the name of the document.

**Source**

Indicates the authoring tool in which the document was created.

**Type**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

252/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Displays the type of document or documents selected.

**Comment**

Allows you to enter information about the selected publishable documents.

**Issue Only**

Allows you to issue request documents without, necessarily, republishing them. Use this option when no changes were made to a document, but you want to add the document to a transmittal.

Even with the **Issue Only** option set, documents can still be published. Any documents that have never been published must be published, regardless of this setting.

You will receive an error message if you select multiple documents and activate this option when one or more of the selected documents cannot be changed. For example, if a selected set of documents includes new documents (for which this field can be set only to **No**) and current or locked documents (for which this field can be set only to **Yes**), the error message prompts you to select a smaller set of documents.

**Owning Group**

Select an owning group from the drop-down list to which the document belongs.

By default, the owning group selected for the previous version, if any, is shown.

All the owning groups configured in SmartPlant Foundation are listed.

**Revision**

Displays the current revision number of the selected document or documents.

You will receive an error message if you attempt to change the value in this box when you have selected one or more documents that have conflicting revision schemes or different possible revisions. The error message prompts you to select a smaller set of documents.

**Revision Scheme**

Displays the revision scheme applied to the selected document or documents.

Only revision schemes that are applicable to the configuration (plant) or classification (document type) are available in the shortcut menu. The revision schemes related to a configuration or classification are not available for any other configurations or classifications. If none of the revision schemes are related to the configuration or classification, then all revision schemes are available unless they are related to any other configuration or classification. See Configure different revision scheme strategies.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

253/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

You will receive an error message indicating that this field cannot be edited if one or more of the documents you have selected are not new or will have a revision scheme supplied by the authoring tool.

The error message prompts you to select a smaller set of documents.

**Version**

Indicates the current version of the document or documents.

**Workflow**

Indicates to which workflow the selected document or documents were assigned.

You will receive an error message indicating that this field cannot be edited if one or more of the documents you have selected have conflicting sets of possible workflows. The error message prompts you to select a smaller set of documents.

**Check and publish released claims for previously deleted items** Select this check box to resolve issues where deleted items were restored from an earlier version and the claim on them was released. This check will take additional time and should only be used when deleted items have been restored.

**Operation**

Select the operation you want to perform on the selected documents. Choose from the following options: **Publish now**

Selected documents are published immediately.

**Background publish**

Selected documents are published immediately as a separate process, allowing you to perform other tasks at the same time.

**Scheduled publish**

Selected documents are published in batch mode by the authoring tool. This option is available only for tools that support it and if processed by the authoring tool, not the SmartPlant Client. The documents are not published immediately. Instead, the selected documents are scheduled for publish at a later time and might be scheduled as a recurring operation.

**Custom**

If applicable, opens the **Custom** dialog. This functionality is available only if defined by your project implementation team.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

254/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Issue Request Tab (Publish Dialog)**

This tab allows you to view the documents associated with a specific issue request and add documents to or remove documents from a request.

**Issue to**

Contains a list of all objects (contracts) that can support issue requests. When you select an item from this list, the names of any documents associated with that object appear in the table below.

**Add**

Creates a new item in the table for any documents highlighted in the **Selected documents** tree view.

**Remove**

Deletes a selected document from the table.

**Document Name**

Displays the names of all documents associated with the object in the **Issue to** box.

**Advanced Publish Options Dialog**

Allows you to specify the type of files that you want to search for when you look for documents to publish.

This dialog opens when you select **Advanced** on the **Publish** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

255/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Document type**

Indicates the types of documents the software considers when selecting the documents to publish.

**Find Documents to Publish from Smart P&ID Drawing Manager** 1. Select **SmartPlant** > **Find Documents to Publish**.

This feature is also available by clicking **Find** on the** Publish** dialog.

This command is available only if you have registered the active plant using the SmartPlant Registration Wizard.

The **Find Documents to Publish** command determines which documents need to be published or re-published and displays the results on the **Find Documents to Publish** dialog.

1. From the **Select documents to publish** list on the **Find Documents to Publish** dialog, select the check boxes beside the documents that you want to publish.

You can quickly select the entire list by selecting **Select All**, or you can clear the entire list by selecting **Clear All**.

1. Select **OK** to accept the selections. The documents you selected to publish now appear in the **Documents to Publish** list on the **Publish** dialog, and are ready to be published.

The lists displayed on the **Find Documents to Publish** dialog are compiled at the time indicated in the **Last search performed** box. You can update the lists by selecting **Update**, but this process can be time consuming, depending on whether you are running the applications in *synchronous* or *asynchronous* mode.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

256/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Find Documents to Publish Command**

Opens the **Find Documents to Publish** dialog, which helps you select the documents that you want to publish and specifies those documents that have never been published or have been modified and need to be published again, or have been deleted since the last publish. This list is specific to the authoring tool from which you are working.

**Compare with Published Version Command**

Allows you to compare the current document with a previous revision and version of that document that was published.

**Find Documents to Publish Dialog**

Allows you to search for documents that have been updated since they were last published. Additionally, you can use this dialog to terminate documents that were previously published but no longer exist in the authoring tool.

**Last search performed**

This option is not used.

**Update**

This option is not used.

**Document types searched**

Indicates what types of files were considered when the last search was conducted.

**Select documents to publish**

Displays a list of files that were either updated since they were last published or files that have not yet been published. For each file, this list displays the file name and type, and the date on which the document was last published. If the file has not been published, the **Last Published** box for the document is **New**.

**Select documents to terminate**

Displays a list of all the files that were previously published but have been removed from the project. For each file, this list box displays the file name, type, and the date on which the document was last published.

**Select All**

Selects all the files in the associated list of documents.

**Clear All**

Clears any selected documents in the associated list.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

257/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Check for deleted objects no longer on documents** option will be checked and disabled if **Automatic process of moved objects** option is set to **TRUE** on the **Manage Integration Options** dialog in the SmartPlant Foundation Desktop Client.See Configure Automatic process of moved objects.

The status bar contains four separate areas of information.

The first column displays information about the current SmartPlant Foundation connection.

The second column indicates whether SmartPlant Integrator has been installed.

The third column indicates whether File Mode is on or off.

The last column displays whether debug logging is enabled, and to what level. If this section is blank, debug is not enabled.See Debug and Error Logging in SmartPlant Integration for COM

environments or Debug and Logging in SmartPlant Integration for .NET environments.

To terminate a document published to a project at the plant level, you need to first terminate the document at the project level. After the project level document has been terminated, the plant level revisions can be terminated.

**Find Documents to Publish dialog - Document Types**

Allows you to specify the types of documents to find for publication.

**Document types**

Indicates the types of documents the software should consider when deciding which documents should be published.

**Retrieving Documents**

When you retrieve documents into an authoring tool, you are retrieving the document data that was published by another authoring tool. For example, in Smart Instrumentation, you can retrieve engineering information from a published P&ID into the Smart Instrumentation database.

The authoring tools provide commands that let you select a document and retrieve it into that tool. You can use either the **Integration** > **Retrieve** command to open a wizard that assists you in retrieving applicable documents, or with some authoring tools, you can configure an automatic retrieval feature.

When you publish a 3D model, you must now enable the **Scheduler** and **Loader** in SmartPlant Foundation to make the 3D model data document retrievable. The load, consolidate, and merge tasks must complete successfully before the 3D model document can be retrieved.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

258/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

The software trims all leading and trailing spaces from all strings and from all values without units of measure. These spaces do not appear in the retrieved data file.

Additionally, you can access the Web Client through the **Integration** > **Browser** command. This allows you to select the document or documents that you want to retrieve from your Web Client To Do List, the tree view, or by using the Web Client search functionality. After you select the documents that you want to retrieve, you can use the **Retrieve** command on the Web Client **Integration** menu to start the retrieval process.

The **Retrieve** command provided in the authoring tools is slightly different from the **Retrieve** command available in the SmartPlant Foundation Web Client. The Web Client presents a list of documents from which you can select those you want to retrieve. However, when you use the command from an authoring tool without first selecting documents, the software searches the SmartPlant Foundation project for documents to retrieve, and these are presented in a list on the **Retrieve** dialog.

You can retrieve a document in two ways:

**As published**

Retrieves only the data the authoring tool originally published with the selected revision and version of the document. Retrieving as-published data retrieves the .XML file the authoring tool published from the appropriate SmartPlant Foundation vault.

**With the latest data**

Retrieves the latest data associated with the selected document in the SmartPlant Foundation database. If another, more-recently published document contains updates to objects in the selected document, the software retrieves the most current data in the SmartPlant Foundation database for those shared objects.

When you retrieve the latest data, SmartPlant Foundation generates an .XML file containing the published data.

**Document Types for Retrieval**

The types of documents that you can retrieve depend on the authoring tool you are using. The following lists include the documents that each authoring tool can retrieve: **Aspen Basic Engineering**

Equipment Data Sheets

P&IDs

Process Flow Diagrams (PFDs)

Plant Breakdown Structure (PBS)

Project Lists

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

259/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Summary Sheet documents and data

**Smart P&ID**

Equipment Data Sheets

Equipment Lists

Instrument Index documents

Instrument I/O Assignment documents

Instrument Master Lists

Process Flow Diagrams (PFDs)

Stream Data Sheets (published as Equipment Data Sheets)

**Smart Electrical**

P&IDs

Smart Instrumentation Electrical Signal Lists

Smart Instrumentation Electrical Power Elements

3D Cable Data (Smart Review File Type)

**Smart Engineering Manager**

PBS

Project Definition Documents

**Smart Instrumentation**

Instrument Index documents

Instrument Process Data Sheets (IPD)

P&IDs

Plant Breakdown Structure (PBS)

Project Definition Documents

Smart Electrical I/O Lists

Smart Electrical Power Elements

**Smart 3D**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

260/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

P&IDs

Cable Schedules

Dimensional Datasheets (DDPs)

Plant Breakdown Structure (PBS)

Project Breakdown Structure

Project Lists

**PDS**

Does not retrieve

**All Authoring Tools**

From the authoring tools, you can retrieve the plant breakdown structure (PBS) and project documents. The PBS and project documents, created in SmartPlant Foundation and published, are retrieved by authoring tools to provide information about the plants, areas, units, projects, and contracts that need to be created in the authoring tool so that the information is consistent across all authoring tools.

The PBS document published by SmartPlant Foundation contains information about the physical plant with a structure consisting of plants, areas, and units. The default structure is plant/area/unit, but you can define a custom hierarchy in the Schema Editor. The project breakdown structure, project list, and project definition document contain information about the project or projects and their statuses in a plant/project structure.

Retrieving the project breakdown documents and the PBS into Smart Engineering Manager creates the appropriate structures automatically.

When using Smart Instrumentation, you must create the plant hierarchy according to the PBS

information in SmartPlant Foundation before you retrieve either the PBS or the project definition document. You must create a plant hierarchy with at least three levels with a minimum of one unit before you can retrieve the PBS and project definition document.

When working in a project, retrieval is not available.

For certain document types, the tool schema definition can specify that To Do List tasks (Create, Update, or Delete) will not be generated for those document types. See Suppress Generation of Tasks on Retrieve.

**Data Handling After Retrieval**

The authoring tool that you use also determines how the system deals with changes in downstream data when you retrieve a document. Smart P&ID, Smart Instrumentation, Smart Electrical, and Aspen Basic https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

261/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Engineering analyze the impact of the newly retrieved data on the existing database, and then place tasks on the authoring tool’s To Do List that allows you to modify items at the appropriate time in the design process. The To Do list gives you the opportunity to view and understand potential changes before accepting your changes. In Smart 3D, you can view the P&ID using the **View** > **P&ID** command to pull in the data and correlate items.

**Design Basis**

Objects that tools retrieve from other authoring tool documents can become the design basis for objects in downstream documents. Objects that become the design basis for other objects can be specific objects that get richer as they move through the life-cycle or can be schematic or logical objects in one application that evolve into more detailed objects downstream.

Design basis is implicit based on retrieval; you do not have to define it. For example, a pump retrieved from a PFD becomes the design basis for a pump in the P&ID. When you change common properties for the pump and retrieve the changes into Smart P&ID, tasks to update property values automatically appear in the To Do List. The same process works for logical items that are a design basis for other items, such as a stream in Aspen Basic Engineering that results in multiple pipe runs in Smart P&ID, or a P&ID tag in Smart P&ID can evolve into a control loop with associated tag numbers in Smart Instrumentation.

**Retrieving to Smart P&ID Drawing Manager - Work Process** **Retrieve Documents to Smart P&ID Drawing Manager**

This functionality is available only if you have registered the active plant using the SmartPlant Registration Wizard. See Register from Smart Engineering Manager.

If you logged on to the authoring tool with a user name that is not defined in the integrated environment, you are prompted to log on when you use this command.

1. Select **SmartPlant** > **Retrieve**. The **Retrieve** dialog appears.
2. In the **Document type** list box, specify the type of document to be retrieved. The default option is **All**.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

262/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

1. Select additional filtering options in the **Show** area of the dialog.

Select **New documents** to only display documents that have not been retrieved previously.

Select **New versions of retrieved documents** to only display documents that are a new version of a previously retrieved document.

Select **Unchanged documents** to display documents that have not been modified since the last retrieval process.

1. Select **Documents of all owning groups** to display all documents.
2. In the **Documents to retrieve** list, select the check box beside each document you want to retrieve.

To help identify the documents, review the details in the **Type**, **Revision**, **Version**, and **Last** **Retrieved** columns. To quickly select the entire list, select **Select All**. To quickly cancel the selections, select **Clear All**.

1. For each document you selected, use the **Retrieve Option** column to specify whether you want to retrieve the document with the latest data or retrieve it as published.
2. Select **OK** to retrieve the specified documents.

Select the **Batch retrieve** option if you want the retrieve process to run in batch mode. If you select this option, an e-mail message will alert you when the process is complete. Otherwise, the retrieval process begins when you select **OK**.

The Deleted and Unclaimed Objects document is retrieved automatically every time you retrieve, if there is a newer version of this document since the last retrieval. The document is not included in the list, but it is retrieved automatically, when necessary, to ensure that the applicable information is updated.

During retrieval, an information dialog appears with a progress bar. If the **View Log** button on the dialog is enabled, messages are available concerning the operation. These messages can include errors or warnings or even informational messages. Select **View Log** to see these messages.

**Retrieve Command**

Searches the SmartPlant Foundation plant for documents that are ready to be retrieved into the authoring tool. This list is displayed on the Retrieve Dialog, from which you can select the documents you want to retrieve, bringing the information from the SmartPlant Foundation database into the authoring tool.

**Retrieve Dialog**

Allows you to retrieve information published by other authoring tools.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

263/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Document type**

Lists the types of documents that you can retrieve. Selecting a document type changes the list view to show only that document type.

**Show**

Indicates which documents you want to see in the list. Choose from the following options: **Documents to be retrieved only**

Provides a list of only those documents that need to be retrieved. In other words, the list will display the documents that have newer versions published since they were last retrieved.

**New documents only**

Provides a list of only the new documents that have not yet been retrieved.

**All documents**

Provides a list of all the documents available for retrieval, including both new and previously retrieved documents.

**Documents to retrieve**

Displays a list of the documents available for retrieval. For each document, this list provides the name, type, revision and version numbers, status, date of the last retrieval, and revision option. Select the check box beside each document you want to retrieve and then use the **Retrieve Option** column to specify whether you want to retrieve the document with the **Latest Data** or retrieve it **As published**.

**Select All**

Selects all the files in the **Documents to retrieve** list.

**Clear All**

Cancels the selection of documents in the **Documents to retrieve** list.

**Batch retrieve**

Indicates that the system will retrieve the selected documents in batch mode, in other words, in the background. When you use this feature, an e-mail message alerts you when the process is complete.

Otherwise, the retrieval process begins as soon as you select **OK**.

Work Breakdown Structure (WBS) documents, such as the Project List, Project Definition, and Project Breakdown, and Plant Breakdown Structure (PBS) documents are considered Administrative documents by the software and must be retrieved by all tools that subscribed to these types of documents.

So, even when these documents are new to the tools (have not been retrieved by the tool before), they are still listed in the **Documents to be retrieved only** list because they must be retrieved.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

264/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Upgrade Schema Command**

Upgrades the existing SmartPlant schema associated with the active plant to a newer version.

The software upgrades the SPPIDDataMap.xml file, including user customizations, with the latest version data from the files in the ..\SmartPlant\P&ID Workstation\bin folder path and registers the schema version at the beginning of the .xml file.

When using Integration 2.0 share service, the upgraded file will be SPPIDSIODataMap.xml, and upgrade status feedback will be recorded in the shared data log file.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

265/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Scheduling Wizard**

**Scheduling Tasks**

Drawing Manager has the capability to let you schedule tasks to complete at a later time or on a regular interval. For example, you can schedule drawings to print at a time when the print queue is not in high demand, or you can schedule a drawing to publish at a specific time every day. Tasks that can be scheduled are either associated with a schedule command on the main menus or with a **Schedule** button on a dialog.

Selecting either one of those opens the **Schedule Task Wizard**, and you can progress through screens that are appropriate to your task and specify options for that task.

**Schedule Task Wizard**

Allows you to specify options for scheduling a task, such as printing, archiving, publishing, and so forth.

Follow the directions on the wizard as you choose options. Selecting **Next** advances you to the next appropriate screen in the wizard where you further specify options for the task that you are scheduling. On the final screen, selecting **Finish** completes the schedule and closes the wizard.

If you are logged in as a standard user on a Windows 10 operating system, your System Administrator

must assign you special user rights to be able to run scheduled tasks. For details, see Assign User

Rights for Scheduled Tasks on Windows 10.

After setting up the schedule, the wizard relinquishes control over the schedule to your Windows operating system. The only way to modify or delete a task schedule is to use the **Control Panel** > **Scheduled Tasks** utility.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

266/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Assign User Rights for Scheduled Tasks on Windows 10**

On a Windows 10 operating system, users with standard User privileges must be granted special access to allow them to run scheduled tasks.

The changes described in this procedure can be made by a System Administrator only.

1. Log in using your administrator credentials.
2. Select the Windows icon and in the Search box, type Local Security Policy or Secpol.msc.
3. In the tree view, select to expand **Security Settings** > **Local Policies** > **User Rights Assignment**.
4. In the right pane, scroll down to the option **Log on as a batch job**.
5. Right-click this option and on the shortcut menu, select **Properties**.
6. Select the **Add User or Group** button.
7. In the **Select Users, Computers, Service Accounts, or Groups** dialog, enter **Users** (where **From** **this location** points to **Entire Directory**) or “specific user name” to run the scheduled tasks with all users or only with the specific user of the system respectively.

**Schedule a Task**

1. If you choose to schedule a task, such as printing, archiving, or publishing, by selecting a schedule command or selecting **Schedule** on a dialog, the **Schedule Task Wizard** opens.
2. Follow the directions, fill out options, and select **Next** on the wizard to complete the schedule.
3. Select **Finish** on the last wizard screen in order to exit the wizard.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

267/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Troubleshooting**

**Problem**: The application fails to launch or stops working when the user launches it.

**Reasons**: The application might fail to launch due to damage in any of the following areas: Cached data

Database connection or database client

Database server, site, or plant

Smart P&ID client software

Smart P&ID client USER information

**Solution**: We recommend that you perform each of the following steps in the order shown and after each step try to launch the application. If the application still fails to launch, proceed to the next step: 1. Open Task Manager and terminate the draft.exe process.

1. Reboot the computer.
2. Clean up temporary cached data (.tmp and .temp files) in the client’s user profile. These files are usually located in the path C:\Documents and Settings\ *username*\Local Settings\Temp\.
3. Check the database connection using the appropriate database tools.
4. Delete the SmartPlantManager.ini and Smart P&ID.ini files. These files are usually located in the path C:\Documents and Settings\ *username*\
5. Uninstall the software client and do the following:
6. Clean up the current USER registry information:

HKEY_CURRENT_USER\Software\Intergraph\Applications\SmartPlantPID.Application b. Ensure that the following registry settings have been removed: HKEY_LOCAL_MACHINE\SOFTWARE\Intergraph\Applications\SmartPlantPID.Application HKEY_LOCAL_MACHINE\SOFTWARE\Intergraph\SmartPlantPID

1. Clean up any left-over files and the following folders:

Smart P&ID installation folder ..\SmartPlant\P&ID Workstation\.

Any subfolders in the Windows\Downloaded Installations\ folder that contain Smart P&ID.msi files.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

268/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

Deletion of the SmartPlantManager.ini file and the current user’s registry environment will clear the user’s recent activities and customized menu look-up.

1. Reinstall the software client.

If, after performing all of the above troubleshooting steps, the application still fails to launch, contact Intergraph Customer Support.

**Problem:** The software is unable to print to PDF.

**Reasons:** Missing the .pdf extension from the documents name.

**Solution:** Check that the .pdf extension is included in the documents name in the **Print to File** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

269/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our documentation web site at

https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To join in conversations about Smart P&ID, go to Technical User Forums <https://hexagon.com/support-

success/asset-lifecycle-intelligence/tuf> and join the **Engineering & Schematics TUF** group.

**Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, or its affiliates, parents, subsidiaries retains ownership of the product. You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

**Copyright Notice**

**Copyright**

Copyright © 1999-2025 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

270/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB

and/or its subsidiaries and affiliates.

**U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below. For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software -

Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014 and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division 305 Intergraph Way

Madison, AL 35758

**Documentation**

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

**Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

**Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

271/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

**Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE

SOFTWARE IS EXPECTED TO MAKE THE FINAL EVALUATION AS TO THE USEFULNESS OF THE

SOFTWARE IN HIS OWN ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

**Limitation of Damages**

IN NO EVENT WILL HEXAGON BE LIABLE FOR ANY DIRECT, INDIRECT, CONSEQUENTIAL

INCIDENTAL, SPECIAL, OR PUNITIVE DAMAGES, INCLUDING BUT NOT LIMITED TO, LOSS OF USE

OR PRODUCTION, LOSS OF REVENUE OR PROFIT, LOSS OF DATA, OR CLAIMS OF THIRD PARTIES, EVEN IF HEXAGON HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

UNDER NO CIRCUMSTANCES SHALL HEXAGON’S LIABILITY EXCEED THE AMOUNT THAT

HEXAGON HAS BEEN PAID BY LICENSEE UNDER THIS AGREEMENT AT THE TIME THE CLAIM IS

MADE. EXCEPT WHERE PROHIBITED BY APPLICABLE LAW, NO CLAIM, REGARDLESS OF FORM, ARISING OUT OF OR IN CONNECTION WITH THE SUBJECT MATTER OF THIS DOCUMENT MAY BE

BROUGHT BY LICENSEE MORE THAN TWO (2) YEARS AFTER THE EVENT GIVING RISE TO THE

CAUSE OF ACTION HAS OCCURRED.

IF UNDER THE LAW RULED APPLICABLE ANY PART OF THIS SECTION IS INVALID, THEN HEXAGON

LIMITS ITS LIABILITY TO THE MAXIMUM EXTENT ALLOWED BY SAID LAW.

**Export Controls**

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

272/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: a. To Cuba, Iran, North Korea, Syria, or the Crimean, “Donetsk People’s Republic”, “Luhansk People’s Republic,” or Sevastopol regions of Ukraine, or any national of these countries or territories.

1. To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List. Visit www.export.gov for more information or follow this link for the screening tool: https://legacy.export.gov/csl-search [https://legacy.export.gov/csl-search](https://legacy.export.gov/csl-search) .
2. To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Hexagon, its subsidiaries, or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.
3. To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.

Any questions regarding export/re-export of relevant Hexagon software product, customized software, Technical Data, and/or third-party software obtained from Hexagon, its subsidiaries, or distributors, should be addressed to Hexagon’s Export Compliance Department, 305 Intergraph Way, Madison, Alabama 35758

USA or at exportcompliance@hexagon.com. Customer shall hold harmless and indemnify Hexagon and a Hexagon Group Company for any causes of action, claims, costs, expenses and/or damages resulting to Hexagon or a Hexagon Group Company from a breach by Customer.

**Trademarks**

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, Intergraph Smart® Cloud, PDS®, FrameWorks®Plus, I-Route, I-Export, Isogen®, Intergraph Spoolgen®, SupportManager®, SupportModeler®, SAPPHIRE®, TANK®, PV Elite®, CADWorx®, CADWorx DraftPro®, GT STRUDL®, CAESAR II® , and HxGN SDx® are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners. Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

273/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**Glossary**

**active placement point**

Coordinates that define the point where you place piping and instrumentation.

**alias**

An alternative name for an object, such as a variable, file, device, or database instance.

**annotations**

Dimensions, notes, symbols, or reports that are used in a drawing to provide information or comments.

**archive**

To copy a file to a specified storage location and then delete the file from the current location.

**attribute**

1. A property or characteristic of a component.
2. A characteristic that all members of a class possess. Each property has an associated value that defines its current state. Most databases represent an attribute by a column in a table.

**backup**

To copy a file to a specified storage location while retaining the file in the current location.

**batch processing**

A method of processing data that collects a series of operations into a group and runs the group in a continuous stream without user intervention.

**Boolean operator**

Syntax that defines logical relationships between expressions like **AND** (both), **OR** (either), and **NOT** (other than).

**branch point**

A point on a pipe run that separates piping segments for assignments with different segment parameters.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

274/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**break label**

A graphic label placed at a point in a piping line at which any property can change value.

**cache**

Memory that stores recently-accessed data so that subsequent requests to access the same data can be processed quickly.

**catalog**

A collection of catalog items, which are blueprints or templates for creating an item within the model.

**check in**

The process of moving a file from a user location to a storage location and recording that location in the database.

**class**

A blueprint for creating an item. The class defines the properties and behaviors that an item can show.

**client**

A user, software application, or computer that requests the services, data, or processing of another application or computer. The client is the user process. In a network environment, the client is the local user process and the server may be local or remote. All network operations among two or more nodes establish a client/server relationship.

**client/server database**

A database system in which the database engine and database applications reside on separate, intelligent computers that communicate with each other through a network. In this system, the processing power is split between the two CPUs. The workstation for the user is the client, and the database runs on the server.

**code list**

See *select list*.

**collaboration**

Working jointly. In Workshare, satellite sites work together with the host site to share the creation and maintenance duties for P&ID drawings and related data.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

275/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**column**

An attribute of a database table. A group of columns defines a table in the database.

**commodity code**

A code you define that provides an index to material descriptions.

**commodity item**

A standard component that you can find in a manufacturer catalog.

**commodity option**

A pre-defined exception to the default settings for a component definition in the Piping Job Specification.

**component**

A catalog item that represents a part of the drawing. A component has database information associated with it.

**concentric**

Having a common center or origin point with varying radii.

**configuration files**

Files that are used to identify and characterize the components of a network. Configuration is largely a process of naming network components and identifying relationships among those components.

**connect point**

An active point item that is specially designated in a component. A connect point is a location at which lines, labels, and other components connect to one another. Also, a location for applying a relationship.

**connectivity**

Linkage between items that relate because of their graphics, like a valve and a pipe run. Proper connectivity must exist to confirm valid data integrity.

**connector**

Item with multiple vertices; behavior of a connector relies on the two items that it connects.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

276/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**data dictionary**

The underlying data model of a plant, consisting of database entries and select lists. Data Dictionary Manager maintains this information.

**data model**

Application items that populate a project. Typical items in a data model are components, lines, and labels.

**database**

Collection of files of comprehensive information that have predefined structure and organization; a specific program can communicate, interpret, or process these files.

**database administrator**

The technical support person who assigns user IDs and data access permissions, creates new databases, removes databases no longer in use, and monitors disk storage usage of the database and performance.

**database link**

A pointer that defines a one-way communication path from an Oracle database server to another database server. This pointer is stored in the local database and identifies the remote database, a communication path to that database, and optionally, a user name and password. In connected Workshare, the database link is used to access the remote database, providing the satellite a view into the plant schema at the host site.

**database table**

Part of the database consisting of rows and columns and containing information about the project and design elements.

**design file**

File containing graphics and text data, also called a drawing file.

**design-wide break**

A region of the drawing within which a single property value is defined for all the included components.

Indicating the region, a closed shape exists, along with an accompanying label that shows the property value.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

277/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**display-only annotation**

Feature that allows you to generate temporary annotation graphics for review without placing the graphics in a design file.

**drawing file**

File that contains graphical items; also called a design file.

**drawing, P&ID, PFD**

Graphics file that contains data about one unit. Each drawing has a unique drawing number within the unit to which the drawing belongs.

**driving label**

Graphics, text, or both with their own properties that are placed on the drawing to define property values of the components and groups to which they apply.

**easting**

Term used in plane surveying that describes an east, or positive, difference in longitude.

**edge-edge model**

A model that represents connectivity entirely by edges.

**enumerated list**

See *select list*.

**equipment components**

Items associated with pieces of equipment, such as nozzles and trays. As you place equipment components, the software automatically creates a group relationship between the equipment and the component. As a group, the components move along with the equipment.

**equipment group**

A single-name equipment body and any items within or attached to the body, such as a tray or nozzle.

**exclusive database relationship**

Relationship that exists between any given item and the parent item to which it belongs, for example, an instrument can belong only to one loop at a time.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

278/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**exit elevation**

Lowest downstream elevation point on the internal diameter of a pipe.

**filter**

Function that creates a subset of items. This subset meets criteria that property values define.

**fixed point**

A control point that usually is a locally known monument with known coordinates.

**flow rate**

Quantity of fluid that flows per unit of time.

**flow time**

Required time for the flow, from the start of the piped system, to reach a downstream point.

**full path name**

Name of the entire path or directory hierarchy to a file, including the filename. See also *relative path name* and *UNC path*.

**gap**

Condition that exists when two lines intersect graphically on the P&ID but not physically in the plant.

**glyphs**

1. Icons attached to the pointer that provide feedback as you draw. For Smart P&ID, glyphs identify the relationships that you are creating.
2. Icons that show the perpendicular or parallel relationships with other items in the drawing as you point over items in the drawing.

**hierarchical**

An ordered relationship from greatest to least; refers to the relationships among groups, components, and labels.

**hierarchy**

A classified structure with superiors, or roots, and subordinates, or dependents, for grouping files or commands.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

279/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**horizontal angle**

Angle measured in the horizontal plane. Horizontal angles are the basic measurements needed to determine bearings and azimuths.

**horizontal distance**

Distance between two points computed using only the northing and easting coordinates of the points.

**host**

A computer that acts as the controlling source of information. In Smart P&ID Workshare, a site that controls satellites.

**implied piping component**

Piping components that the software creates in the alphanumeric database; these components are not represented graphically.

**inline**

Term used to refer to those piping or instrument components that have been inserted in a piping segment.

**inline instruments**

Components that have been inserted in a piping segment. Inline instruments include instrument valves, such as butterfly valves and temperature regulator valves, and other instrument components, such as orifice plates and flow controllers.

**instance**

A single allocation of an item class.

**instrument loops**

A group of one or more instruments or control functions arranged so that signals can pass from one function to the next for the purpose of measuring and controlling a process variable. In Smart P&ID, you can create instrument loops containing any combination of inline and offline instruments.

**instruments**

Devices that directly or indirectly measure or control a variable in a plant process, such as flow or temperature. Instruments can be devices such as final control elements, computing devices, or electrical switches. Two types of instruments exist: inline instruments and offline instruments.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

280/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**interference checking**

Process that identifies possible collisions or insufficient clearance between items in a drawing.

**isometric**

Relating to or concerning a drafting system characterized by three equal axes at right angles; a view in which the horizontal lines of an item are drawn at an angle to the horizontal and all verticals are projected at an angle from the base.

**item**

Unit of storage within a larger unit, such as a file in a catalog; a single member in a drawing.

**item type**

Distinct objects that users can manipulate in Smart P&ID, such as equipment, events, and safety classes.

**keypoint**

A point on an item, including vertices, which is used to connect to the item.

**label**

A graphic representation that reflects the status or condition of an associated item.

**line route**

Collection of ordered line runs, gaps, and components that all share the same attribution. A line route contains line runs, components, gaps, and properties; however, a line route does not contain any branches.

**line style**

Collection of formats or properties that you name and store as a group to apply as a style of a line.

**loop**

Software structure that allows a specified sequence of instructions to run repeatedly, if the stated conditions remain constant.

**macro**

1. **Smart Piping and Instrumentation Diagram**, **Smart Engineering Manager** - A sequence of actions or commands that can be named and stored. When you run the macro, the software performs the actions or runs the commands. You can create the macros in Visual Basic or other OLE-aware https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

281/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

programming applications. Some of the OLE-aware programming applications are VBA, Visual C++

Delphi, Visual Basic, and so forth.

1. **Smart Electrical** - A string attached to a graphic block that represents the item type and one of its properties. You can assign one or more macros to a block. When you generate a schematic drawing, the software reads and resolves the macros so that it can retrieve the value of the property from the database and display it in the drawing.

**mirror**

To create the reverse image of a display set through a plane or around a defined axis.

**mirror handle**

Reflects an image about the horizontal and vertical axes. Point to the manipulation handle on upper corner of an item to display the mirror handle.

**model**

A representation of graphics or a schema; collection of all items and their relationships to create a coherent description of a process plant.

**model file**

A design file or database file that defines the 2-D or 3-D geometry and connectivity of a structure.

**MTO**

Material take-off; also called a Bill of Materials.

**net service alias**

(Oracle) An alternative name for a directory naming object in a directory server. A directory server stores net service aliases for any defined net service name or database service.

**net service name**

(Oracle) A simple name for a service that resolves to a connect descriptor. Users initiate a connect request by passing a username and password along with a net service name in a connect string for the service to which they want to connect: *CONNECT username/password@net_service_name*.

**network**

Interconnection of host computers and workstations that allows them to share data and control. The term has a dual meaning:** network** can refer to the devices that connect the system, or **network** can refer to the connected system.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

282/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**node name**

A name or alias that you can assign to the node address of a device on a network.

**northing**

Term used to describe a north coordinate location in the plant coordinate system.

**nozzle**

A special equipment item that contains the connection point to piping.

**offline**

Term that refers to those instrument components that are not inserted in a pipe run.

**offline instruments**

Components that are not inserted in a piping segment. Typically, these components are the instruments that monitor and control inline instruments. Offline instruments include temperature regulators, level gauges, and system functions, such as digital control stations (DCS) or computers.

**Oracle Net**

Communication software that enables a network session from a client application to an Oracle database server. After a network session is established, Oracle Net acts as a data courier for the client application and the database server. It is responsible for establishing and maintaining the connection between the client application and database server, as well as exchanging messages between them. Oracle Net is able to perform these jobs because it is located on each computer in the network.

**Oracle Net Manager**

A graphical user interface tool that provides an integrated environment for configuring and managing Oracle Net Services.

**ORACLE_HOME**

An alternate name for the top directory in the Oracle directory hierarchy on some directory-based operating systems.

**orientation by system**

A type of orientation in which the software places items in the same orientation that you created them, if you place the items in free space or in a horizontal line. For example, if you placed the item in a vertical line, the https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

283/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

software automatically rotates the item 90 degrees counterclockwise from the orientation in which you created it. See also *orientation by user*.

**orientation by user**

A type of orientation in which you define the orientation of an item when you place it. The default orientation of this item is identical to items that the software orients. You can change the default orientation at placement time. See also *orientation by system* and *orientation fixed*.

**orientation fixed**

A type of orientation in which the software places items in the same orientation in which you created them, regardless of the method or location that you used for placement. You cannot change the orientation at placement time. See also *orientation by system* and *orientation by user*.

**orthogonal view**

A view that is a projection of the drawing onto a plane along lines that are orthogonal to the plane.

**P&ID**

See *Piping and Instrumentation Diagram*.

**parameter**

A property with a value that determines the characteristics or behavior of an item.

**parametric item**

Item that contains geometry constrained together using relationships, with driving dimensions that are defined as adjustable parameters.

**path name**

Sequence of directories leading to a file. See also *relative path name*.

**peak flow**

Maximum flow rate of water through a specific size pipe.

**PFD**

Process Flow Diagram; a drawing that serves as a start for a P&ID.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

284/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**pipe run**

A line run that has piping properties. Also, a contiguous set of pipe run segments separated only by inline components, branch points and gap components. A pipe run has a beginning and an end. It does not branch or contain spaces between components. A pipe run segment may have identical properties as a pipe run from which it branches but is not considered part of the pipe run.

**pipeline**

Set of connected piping segments and their associated piping items. Also, the collection of pipe runs from all drawings in a project whose project-defined line property values are identical.

**Piping and Instrumentation Diagram (P&ID)**

A primary drawing for maintaining a plant. The P&ID includes three primary groups of items: equipment, piping, and instrumentation. The drawing relates critical process-related information, such as process conditions for temperatures and pressures, and identifies physical components in the plant. The P&ID is the basis for both the construction of the physical plant and further specification of instrumentation components.

**piping components**

Graphic elements that represent processes or functions within a particular piping segment. Piping components include valves, flanges, reducers, strainers, and safety components. In drawings, piping components are connected with multiple line segments.

**Piping Materials Class (PMC)**

Classification of components by service or specification - for example, a 150-pound carbon steel specification.

**piping network**

Series of connected pipe runs and inline components. A network terminates at a nozzle, off-page connector, utility connector, or one-point piping component - for example, a pipe cap.

**piping segment**

A line string with two or more vertices that defines the centerline geometry of the pipe run and contains the non-graphic data associated with the pipe run.

**plant**

A group of facilities and equipment that performs one or more material processing functions within a given geographical area. One company can have several plants located at different geographical locations.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

285/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**plant group items**

The building blocks, such as site, plant, unit, area, and level, used to create plant breakdown structures or plant structure hierarchies.

**plant structure**

Represents the business structure or physical hierarchy of a plant.

**project**

1. A directory file created in an application environment that contains design files and subprojects. A project is not necessarily specific to an application; the project may contain design files from multiple applications.
2. Term used for convenient grouping of either all or part of the items that constitute a plant. Several projects can be under design at one time, probably in separate geographical locations and having limited communication among them.

**projection lines**

Witness lines; lines extending from the boundaries of an item and between which dimensioning data for the area marked by the projection lines is placed.

**property**

A unique characteristic of an object, item, symbol, or document.

The properties of an item can include display properties and properties stored with the item. For example, the properties of a valve symbol can include display properties such as color, line style, and width. Other properties stored with the valve symbol can include the manufacturer, cost, or material. Properties stored with the valve symbol are displayed in the Properties window when the valve symbol is selected.

**publish**

To release a P&ID drawing for subscription or distribution.

**publishing method**

To publish a P&ID drawing using either the database link or the file sharing means of transferring data.

**reference data**

A collection of information containing facts relative to industry design codes, catalog data of vendors, job specifications, commodity libraries, graphics symbology, label descriptions, report formats, and other information of a similar theme.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

286/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**reference file**

A drawing file attached to another drawing file for reviewing reference; a graphic representation attached to a drawing view.

**Relational Database Management System (RDBMS)**

A database management system that uses Structured Query Language (SQL) to implement and query data in relational tables.

**relationship**

A condition that exists between items indicating some form of communication of behavior or state. You can establish relationships as you place new items or between items already on the drawing sheet.

**relative mode**

A placement mode in which symbols respond to their orientation definition at creation time, whether they are defined in the application’s reference data as orientation fixed, orientation by system or orientation by user, and to the orientation of any graphic item to which they are attached at placement time. Relative placement mode is more flexible then absolute, but much more difficult to predict.

**relative path name**

Sequence of directories leading from the current directory to a particular file. See also *path name*.

**report template**

An online outline for a new report that you need to define. You can select a user-level or a project-level template to create a new report template.

**required item**

Item that the plant model needs. An item is required if the **Tag Required Flag** property is set to **True** for the item in the **Properties** window of Catalog Manager. If you delete a required item from a drawing, it appears in the stockpile for later placement.

**revision cloud**

A set or arcs used to enclose changes that have occurred since the last revision.

**revision triangle**

A numbered triangle placed in the drawing to indicate the drawing revision when the change occurred.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

287/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**rule**

Standard mechanism for creating relationships. A rule defines a valid context for two items to communicate their behavior or state.

**satellite**

A server located remotely from the host server. In Smart P&ID Workshare, a remote server connected to a satellite slot at the host server.

**satellite slot**

The host’s side of a Workshare connection. Satellites connect to the satellite slots made available by the host at the host site.

**schema**

Description of the overall structure of the rulebase or database.

**schema file**

File that outlines the overall logical structure of a rulebase or database.

**schematic file**

Schematic drawing or diagram of a particular item in the plant.

**search criteria**

Set of values used to scan a database or object library.

**segment**

Contiguous piping and piping components between two points in the network at which properties change value. Segments terminate by property break labels, branches, nozzles, off-pace and utility connectors, and by the terminal ends of piping lines.

**select list**

List of related values that Data Dictionary Manager uses to specify various aspects of the data model. For example, select lists allow you to select from a list of values for specific properties when creating drawings, filters, and symbols. A select list for the fluid code property, for example, allows you to select from a set of standard entries: such as P for process or MMA for methyl alcohol.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

288/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**server**

1. In network operations, the node that maintains common data or performs a common task that clients need. All network operations between two or more nodes establish a client/server relationship.

**signal lines**

1. Intelligent line strings that connect offline instruments, inline instruments, and piping.
2. An ordered collection of connectors, and inline components with an equal set of core properties: typically, items that share the same line number. Specifically, a representation of the wiring used for transferring electrical or software signals.
3. A collection of signal runs from all drawings in a project whose project-defined line property values are identical.

**signal run**

A line run with signal properties. See also *pipe run*.

**site**

A group of plants. A site can contain one or more plants.

**site server .ini file**

A text file (SmartPlantV4.ini) containing the database type, connection alias, data dictionary, and schema information for the site. Used to connect to a site.

**SP_IDs**

Unique identification numbers assigned by the software to all items created in the database.

**Standard Query Language (SQL)**

Language developed by IBM for creating, modifying, and querying relational databases.

**static Oracle port**

A network configuration that forces an Oracle database link to always connect via a fixed path to a fixed port number.

**stockpile**

View of the data model, displaying items that have not yet been placed in the graphic model.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

289/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

**style**

1. The appearance of geometry and annotations on the drawing sheet. For example, color and line weight of an element, the font used in a text box, and so forth.
2. A collection of formats or properties that you name and store as a group. When you apply a style to a selected item, the software applies all the formats or properties in the style to the element. The style types include: fill, dimension, line, and text.

**subnet**

A division of a network into an interconnected, but independent, segment, or domain, in order to improve performance and security.

**subnet mask**

The technique used by the IP protocol to filter messages into a particular network segment. The subnet mask is a binary pattern that is stored in the client computer, server, or router and is matched up with the incoming IP address to determine whether to accept or reject the packet.

**subscribe**

To sign up for a service. In Smart P&ID Workshare, to connect a satellite site with a satellite slot at the host.

**subscribe access**

Read-only access to published P&ID drawings.

**symbology**

1. Display style of an item, including color, pattern, style, and width.
2. In Options Manager, symbology provides graphical clarity to a drawing by differentiating among various items by their appearance. Symbology refers to the color, line weight, and style associated with items in a particular filter.

**table**

Collection of data for quick reference, either stored in sequential locations in memory or printed as an array of rows and columns of data items of the same type.

**template**

A document or file having a preset format, used as a starting point or blueprint for a particular application so that the format does not have to be re-created each time it is used. In Smart P&ID, a file used to create a drawing with a set of default parameters; a template serves as an outline or blueprint for you to create a https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

290/291

3/13/25, 10:36 AM

Hexagon Documentation Site Export

new drawing. In Smart Engineering Manager, a file used to create roles, data dictionaries or other database schemas.

**time stamping**

A process that prompts the software to generate a record when you change a property.

**transaction**

A non-graphic record of any additions, deletions, and changes that you request during job posting activities.

**UNC path**

Universal Naming Convention. The full name of a resource on a network. It conforms to the

\\ *servername*\ *sharename* syntax, where *servername* is the name of the server and *sharename* is the name of the shared resource. UNC names of directories or files can also include the directory path under the share name, with the following syntax: \\servername\sharename\directory\filename.

**unit**

Group of parts of the schematic and individual worlds of a plant that together perform a given process function. The identifying number of the unit is unique within the project and within the plant. Most companies, but not all, use the concept of unit.

**user name**

Name that provides access to an account on the system. Same as username.

**validation**

A process or program that verifies data integrity in the database.

**Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/f0c37e2c-8d48-435e-bdf7-aa33a6c177e0

291/291