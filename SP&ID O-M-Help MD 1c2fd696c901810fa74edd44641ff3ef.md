# SP&ID O-M-Help MD

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Options Manager Help**

## **Hexagon Documentation**

Generated 03/13/2025

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 1/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Table of Contents**

Intergraph Smart® P&ID Options Manager

Upgrading from a Previous Version of the Software

Additional Documentation

Navigating in Smart P&ID Options Manager

Setting Symbology Options

Define Plant Symbology

Change Plant Symbology

Setting Gapping Options

Define Gapping Style

Change Gapping Style

Change Gapping Priority

Setting Heat Tracing Options

Create a New Heat Tracing Medium

Change the Default Placement of Heat Tracing for the Plant

Modify the Offset Distance of Heat Trace Lines

Setting Formatting Options

Change Default Formatting

Setting Distance Options

Place Two Inline Components an Arbitrary Distance Apart

Change Default Distances

Defining Reference Data Settings

Understanding Reference Data Settings

Change Reference Data Settings

Configure Piping Specification Settings

Connect to the Smart Reference Data Server

Open Dialog

Convert Existing Property Formats Command (Tools Menu)

Convert Existing Property Formats Dialog

Format Conversion Example

Importing and Deleting Linear Patterns and Styles

Linear Patterns and Styles

Linear Patterns Command (Tools Menu)

Linear Styles Command (Tools Menu)

Import a Linear Pattern

Delete a Linear Pattern

Pipe Jacket Nominal Diameter Command (Tools Menu)

Pipe Jacket Nominal Diameter Dialog

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 2/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Upgrading Reference Data

Upgrade Reference Data Command (Tools Menu)

Generating Symbol Images

Generate Symbol Images Command (Tools Menu)

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 3/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Intergraph Smart® P&ID Options Manager**

Intergraph Smart® P&ID Options Manager controls the look and feel of the design software and controls much of the data used throughout the life of a plant. For example, you can define how drawing items appear in drawings by selecting colors, line styles, gapping styles and heat tracing styles for the plant.

Using Smart P&ID Options Manager, you can identify the location of symbols, rules, and labels. You can also define symbology for graphics, default formats for data, and key distances that affect the behavior of the design software. Any changes you make using Options Manager apply to all drawings as well as projects in the plant.

You can customize several different options.

## **Symbology**

Controls the look of items.

## **Gapping**

Controls the style of gaps used.

## **Heat Tracing**

Defines the available display for heat tracing.

## **Formatting**

Specifies default formats used throughout the plant.

## **Default Distances**

Specifies basic distances used throughout the plant.

## **Default Reference Settings**

Controls where and how reference data is stored.

Usually, an administrator sets these options when a plant is created. The administrator can later modify these options when plant requirements dictate a change.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 4/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 12/31/2024 at 12:09 PM

**Upgrading from a Previous Version of the Software**

After upgrading to the latest version of Smart P&ID, opening Options Manager for the first time updates the RAD version for the ProjectStyles.spp file and as a result, changes the status of the Symbology for the drawings to ‘Out-of-Date’. For this reason, after upgrading Smart P&ID, you should open and close Options Manager once *before*  updating your drawings using Smart P&ID Drawing Manager.

## **Additional Documentation**

**Smart P&ID Options Manager Help Command (Help Menu)** Opens the Help viewer where you can read topics about commands, procedures, dialogs, and so forth.

**About Smart P&ID Options Manager Command (Help Menu)** Displays information about your copy of the software, including the version number and the copyright, legal, and licensing notices. The **About** dialog also links you to customer support websites.

**Navigating in Smart P&ID Options Manager**

Smart P&ID Options Manager is divided into six main functions, each of which is accessed by selecting a command button on the left side of the main window: Selecting one of these buttons opens a detailed view in the main window.

Commands on the **Edit** menu and on the toolbar are available depending on the current selection in the main window.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 5/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

For some cells in Smart P&ID Options Manager, a calculation button displays when the cell is selected. Selecting this button opens a dialog that enables you to specify the information required for that field. For instance, when you specify file locations in the **Settings** window, the Open Dialog displays so you can associate the correct file and path, or when you define

gapping, the **Select Filter** dialog opens.

The **File** menu also contains commands for saving changes to database definitions and closing a version of Smart P&ID Options Manager.

## **Connect to a Database**

1. Select **File** > Open Database. If the plant structure that you want appears in the **Available Plant Structures** list, you can select it in the **List** view on this dialog, and go to the last step.
2. On the Open Plant Structure Dialog, select **Site Server** to open the **Open Site server** dialog.
3. Choose the correct SmartPlantV4.ini file, and select **OK**.
4. Select **Open**.

The **Open** command checks to make sure you have the correct access privileges for the selected plant structure and passes you access information back to the software.

**Open Database Command (File Menu)**

Displays the Open Plant Structure Dialog so you can connect to the site and server that you

want to work with by choosing the appropriate SmartPlantV4.ini file. You can also view the plants to which you were recently connected. To use this command, your computer must be able to connect to the network where the server is located.

## **Open Plant Structure Dialog**

Sets options for connecting to a site and plant structure, and passes user access information to the application. This dialog opens when you select **File** > Open Database.

## **Available plant structures**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 6/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Lists those plant structures found on the network. You can select only one item from this list at a time.

## **Application Type**

Allows you to select an application for filtering the available plant structures that are associated with that application. If all the plants in the site are associated with one application only, the value is read-only.

## **Open**

Connects you to the selected database. The **Open** command also checks to make sure you have the correct access privileges for the selected plant structure and passes your access information back to Smart P&ID Options Manager.

## **Site Server**

Opens the **Open Site Server** dialog, allowing you to select a SmartPlantV4.ini file from local and network directories. Plant structures that correspond to the initialization file you choose appear in the list of available plant structures.

**Save Command (File Menu)**

Records any changes you have made to plant-wide options.

**Exit Command (File Menu)**

Closes the software after prompting you to save changes.

**Cut Command (Edit Menu)**

Moves the selected value to the Clipboard.

**Copy Command (Edit Menu)**

Duplicates the currently selected item and places the copy on the Clipboard.

**Copy a Value to the Clipboard**

1. Select the value you want to copy.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 7/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Select **Edit** > Copy to move a copy of the selected value to the Clipboard. The Copy

command is also available from the toolbar.

**Paste Command (Edit Menu)**

Inserts the contents of the Clipboard into the selected position. You use the Cut command

or the Copy command to place information on the Clipboard so you can paste the contents elsewhere.

**Move Up Command (Edit Menu)**

Moves the select list entry up one row in the editable grid. This command is only available for reference data that is editable.

**Move Down Command (Edit Menu)**

Moves the select list entry down one row in the editable grid. This command is only available for reference data that is editable.

**Insert Row Command (Edit Menu)**

Inserts a blank row into the editable grid so that you can create a new entry in a grid view.

This command is only available for reference data that is editable.

**Delete Row Command (Edit Menu)**

Deletes the selected row in the editable grid. This command is only available for reference data that is editable.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 8/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Setting Symbology Options**

Symbology provides graphical clarity to a drawing by differentiating among various items by their appearance. Symbology refers to the color, line width, and style associated with items in a particular filter.

You can use color to differentiate among the different types of drawing items, such as equipment, piping, or instruments, while the software uses line widths and styles to represent various properties of those items. For example, you can define symbology to represent existing lines, future lines, and new lines by using filters that correspond to these in Filter Manager. You can also define symbology to represent lines carrying different fluids or items supplied by different manufacturers, if those properties exist for items in the data model.

By default, the software offers a set of predefined symbology for the following items: instruments

nozzles

pipe runs

labels

equipment

duct runs

duct components

rooms

You can change the default symbology for any filter or define symbology for any other existing filters.

To change the appearance of graphics in the Smart P&ID design software for items with a particular attribute for package number, you can define a filter for items containing the property you want and then define symbology for that filter using the **Symbology** option. For example, if you want to customize the symbology of items with a particular piping materials class, you can define a filter containing items with the piping materials class, and then define https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 9/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

the specific symbology you want to see in the drawing. This behavior emulates the PDS 2D

**Context Display Domain** command.

The order of the options listed in the **Symbology** table indicates the priority, in descending order, when assigned to an item upon placement in a design. You can change the priority of symbology assignment by selecting the symbology row and using Move Item Up

or Move Item Down on the toolbar. You can select only one row at a time when changing symbology priority.

## **Define Plant Symbology**

1. Select **Symbology**

.

1. Select the **Plant Filter** column in the last row of the **Symbology** table.
2. Select to open the **Select Filter** dialog and choose a filter.
3. Select the filter or compound filter that represents the item for which you want to define plant symbology. If necessary, you can create a new filter. See Create a Simple Filter or Create a Compound Filter.
4. Select **OK**.
5. In the **Color**, **Width**, and **Pattern** boxes, select values for the symbology properties.

When you pause on an item in the **Pattern** list, a ToolTip displays the name of the pattern.

The order of the options listed in the **Symbology** table indicates the priority, in descending order, when assigned to an item upon placement in a design. You can change the priority of symbology assignment by selecting the symbology row and using Move Item Up

or Move Item Down on the toolbar. You can select only one row at a time when changing symbology priority.

## **Change Plant Symbology**

1. Select **Symbology**

.

1. Select the **Plant Filter** row you want to change.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 10/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. In the **Color**, **Width**, and **Pattern** boxes, select the new value for the symbology property.

When you pause on an item in the **Pattern** list, a ToolTip displays the name of the pattern.

You can change the color, width, or pattern for plant filters at any time. However, after you define a new plant filter, you cannot change its name. Nonetheless, you can delete that row from the table and redefine another plant filter. See Define Plant Symbology.

If you make changes to the symbology for a plant filter, the software prompts you to save your changes when you select one of the other options on the options bar.

If you make changes to the symbology after creating drawings, and you want those changes to be reflected in the drawings, you must run the appropriate update commands. See *Update Drawings Command* in the Drawing Manager’s Help and *Update Symbology Command* in the Smart P&ID * * Help.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 11/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Setting Gapping Options**

The **Gapping** options allow you to establish priorities and define symbols for displaying line intersections in drawings. In a drawing, when lines, hoses, capillaries, or other line routes intersect, you place gaps in the line with lower priority, while lines with higher priority remain unbroken.

You can define a priority list to handle such intersections. The placement of the connector type in the **Gapping** list indicates its gapping priority. For example, when you place two lines that appear to intersect in the drawing but do not intersect in the plant model, the design software automatically gaps the line that appears lower in the list. By default, piping lines gap signal lines, and primary lines gap secondary lines; however, an undefined gapping style receives the highest priority by default.

The gapping style dictates whether the software displays a jumper or a gap when two lines intersect in a drawing. When you define gapping options, you choose from the following gapping styles:

Plain Gap:

Jumper:

Gap with Break Marks:

Options set for gapping in Smart P&ID Options Manager apply only to automatically gapped lines. You can turn the automatic gapping of lines on and off with gapping commands in the design software.

## **Define Gapping Style**

1. Select **Gapping**

.

1. Select the **Line Type** box in the empty last row of the **Gapping** table.
2. Select to open the **Select Filter** dialog and select a filter.
3. Select the filter you want. If needed, you can create a new filter for your gapped item.

See Create a Simple Filter or Create a Compound Filter.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 12/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Select **OK**.
2. In the **Gapping Style** box of this row, select the symbol you want to use to indicate gaps for lines in the selected filter.

Options set for gapping in Smart P&ID Options Manager apply only to automatically gapped lines.

When you select a filter from the **Line Type** list, two filters appear in the **Gapping** table: one with vertical orientation and one with horizontal orientation. You can specify a gapping style for each.

You can change the priority with which these gaps are applied to lines in a design. See

Change Gapping Priority.

## **Change Gapping Style**

1. Select **Gapping**

.

1. Select the **Line Style** row for the gapping style you want to modify.
2. Select the corresponding **Gapping Style** box, and select from the list the symbol you want to use to indicate gaps in the selected line type.
3. Select Save .

Options set for gapping in Smart P&ID Options Manager apply only to automatically gapped lines.

You can change the gapping style for line types at any time. However, after you define a new line type, you cannot change its name, but you can delete that row from the table and redefine another line type.

If you change the gapping style after creating drawings, and you want that change to be reflected in the drawings, you must run the **Update Drawings** command. See *Update* *Drawings Command*  in the Drawing Manager Help.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 13/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Change Gapping Priority**

1. Select **Gapping**

.

1. Select the **Line Type** row with the priority you want to modify.
2. Select Move Item Up or Move Item Down to move the selected row.

The higher a line type is in the **Gapping** list, the higher its priority. When two lines intersect, the software makes a gap in the line type with the lower priority.

When changing the priority of gapping, you can move only one gap row at a time.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 14/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Setting Heat Tracing Options**

**Tracing** options allow you to specify the default appearance and location of heat tracing symbology in drawings for a plant. You can define a variety of line styles to designate lines with heat tracing or pipe jackets.

**Create a New Heat Tracing Medium**

1. Open Data Dictionary Manager and select **Select Entry**.
2. Select **Heat Trace Medium** from **Selected list**.
3. On the last row, enter information in the **Value** and **Short Value** columns.
4. Select Save to add a new entry in the select list. See Modify a Select List Entry for details about modifying a select list.
5. Open Options Manager and select **Tracing**

.

*The new heat tracing medium is now displayed in the **Tracing Media** list.*

1. From the **Tracing Media** list, locate the new media and select the **Style** box.
2. Select a new heat tracing style from the list.
3. Select Save .

To designate a heat tracing medium as a double heat trace or jacketed heat trace, select **Settings** in Options Manager and add the heat tracing media to one of the following:

Add heat tracing media designated as double to the **Heat Tracing Media - Double** **Heat Trace** row, with each value separated by a comma.

Add heat tracing media designated as jacketed to the **Heat Tracing Media -**

**Jacketed Pipe** row, with each value separated by a comma.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 15/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Any changes made to a heat trace medium in Options Manager are not reflected in any drawing in which that heat trace medium was already assigned to an item. For changes to be reflected in the drawings, you must run the **Update Drawings** command first. See Update Command in Drawing Manager Help.

**Change the Default Placement of Heat Tracing for the** **Plant**

1. Select **Tracing**

.

1. On the toolbar, select the default placement of heat tracing for both horizontal and vertical lines in the P&ID.

BottomLeft

Below horizontal lines and to the left of vertical lines.

BottomRight

Below horizontal lines and to the right of vertical lines.

TopLeft

Above horizontal lines and to the left of vertical lines.

TopRight

Above horizontal lines and to the right of vertical lines.

The default placement applies to all heat tracing media in the current plant, but only affects the display appearance in drawings for media that are designated as *single* heat trace media.

**Modify the Offset Distance of Heat Trace Lines**

The heat trace line offset is modified by setting the offset value in the line style properties for an individual heat trace. The offset value has to be modified for every heat trace line style for which the offset change is required. The workflow is as follows: https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 16/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Create a new symbol in Catalog Manager to be used to edit the line style and import the changes back into the ProjectStyles.spp file.
2. Reference the ProjectStyles.spp file.
3. Import line styles to be edited from the ProjectStyles.spp file into the symbol file and setting the offset to the needed value using Line Style Editor.
4. Import the updated line style from the symbol file back into the ProjectStyles.spp file in Options Manager.
5. Update drawings in Drawing Manager.

Unlike the default offset distance, a user-defined additional heat trace offset distance will not change dynamically as the zoom level changes in the Smart P&ID drawing view. It is recommended to turn on the **Display as printed** option (**Tools** > **Options** > **General**) in Smart P&ID to get a consistent look for the offset. This limitation will not affect the print-out results of the drawings.

This procedure has no impact on the heat trace line offset in translation output files (.dwg / .dxf / .dgn) created by the Smart P&ID **Save As** feature.

**Create symbol and line style definition**

1. Open Catalog Manager and create a new symbol.
2. Assign a meaningful name to the symbol, for example: HT_offset_modifier.sym.
3. Display the **Line Style Editor**.
4. Reference the ProjectStyles.spp file as follows:
5. Select **Format** > **Style** to display the **Style** dialog.
6. Select **Resources** to display the **Style Resources** dialog.
7. Select **Add t**o display the** Add Style Resource** dialog.
8. Browse to the active plant’s P&ID Reference Data folder and type **ProjectStyles.spp** in the **File name** field.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 17/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Select **Open**.
2. Select **OK** on the **Style Resources** dialog.
3. Select **Close o**n the **Style** dialog.
4. In the **Line Style Editor**, expand the **Linear Styles** node.
5. Right-click the heat trace line style that you want to modify (for example, Electric Heat Trace) and select **Import Style** on the shortcut menu.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 18/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

The line style name becomes bold, indicating that it has been imported into the symbol.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 19/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Right-click the style again and select **Properties** on the shortcut menu to display the **Linear Style Properties** dialog.
2. Enter the value in the **Offset** field. The base offset value for heat trace lines is 0.05 in.

As such, the actual offset value will be 0.05 in + the value entered in the **Offset** field.

1. Select a value that matches one of the Options Manager **Tracing** options in the **Crossover orientation** list. For example, select **Top right**.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 20/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Save the file in Catalog Manager and exit.

**Import line style changes back into ProjectStyles.spp** 1. Open Options Manager and select **Tools** > Linear Styles to open the Linear Styles

Dialog.

1. Select **Import**.
2. In the **Import Linear Styles From** window, browse to and select the symbol with the updated linear styles.
3. Select **Open** to open the Linear Styles Dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 21/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Select **Close**.
2. Save the changes and exit Options Manager.

## **Update drawings**

1. Open Drawing Manager and select the drawings that you want to update with the new heat trace style.
2. Select **File** > **Out-of-Date Drawings** > **Update**.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 22/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Setting Formatting Options**

The **Formats** option controls the default formats associated with various data types in the application database. Some examples of data types include length, area, volume, pressure, angular velocity, thermal expansion, signal intensity, integer, and string.

Data formats associated with data types control the length and type of specific information for the plant, such as text strings and numbers. Data formats also control the units associated with particular measurements in drawings and the placement of information in drawings. The formats assigned to these data types can change from plant to plant. You can use the delivered data type formats, or you can create new formats with Format Manager.

## **Change Default Formatting**

1. Select **Formats**

.

1. Select the **Format** box corresponding to the appropriate **Data Type** row.
2. Select the default format for the data type from the list.

The decimal places and units of measure for default distances are controlled by the default format selected for the Thickness data type.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 23/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Setting Distance Options**

Using the **Distance** option, you can define minimum distances between objects in drawings and define default lengths for various entities in drawings in a plant.

You can define default distances or lengths for each of these values: **Label offset**

Defines the default distance between a label and the component being labeled. When you create the label using Catalog Manager, you can change the values of the **Offset Source** and **Offset Distance** properties to override this value.

## **Minimum connector segment**

Defines the minimum length for connector segments (that is, the shortest length of pipe or signal run that can exist). However, the design software overrides this distance when you place piping components together. The line created between two touching piping components is zero-length. The greater of the **Minimum Connector Segment** and **Routing Self-Avoidance** settings governs the shortest line length when, for instance, routing a line from a nozzle.

**Routing self-avoidance**

Defines the distance between a line route and an object that the line is avoiding. This setting also governs how long a segment must be in order to place an inline component into it. When you place a line in your design, the self-avoidance setting is applied. If you later change this setting, the change affects only those lines created subsequent to the change. The original self-avoidance distance remains a characteristic of any line after it is created. You can use the delivered utility, ApplySettingsCmd.dll, to update existing lines with the next *value.*  See the Smart P&ID Installation Help.

**Place Two Inline Components an Arbitrary Distance Apart** 1. Place the first component in the line.

1. Place the second component into the line and connected to the connect point of the first component. You can see that the connect points are actually joined by the black rectangle in the **Drawing** view:

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 24/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. While holding down the ALT key, drag one component along the line away from the other leaving the desired distance between the two. If the components are already close to each other but not connected at coincident connect points, you must drag one component off of the segment to disconnect it and then move it back to get the connect points attached.

## **Change Default Distances**

1. Select **Distances**

.

1. Select the **Distance** box corresponding to the appropriate **Measured Entity** row.
2. Type a value.

The decimal places and units of measure for default distances are controlled by the default format selected for the Thickness data type.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 25/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Defining Reference Data Settings**

The Smart P&ID software requires that you specify various library, file, and path names for reference data. The reference data defines not only references to information used plant-wide but also where to find the data or where to store it. You must define the locations of most of these libraries, files, and directories for your plant before you can begin using Smart P&ID.

Smart Engineering Manager creates most of these initial definitions during site and plant creation.

For Smart P&ID, the following settings only are relevant: Catalog Explorer Root Path

Copy Transformation Program

Default Report Template Path

Delete Key Default Behavior

Display Undefined As

Drawing Properties - Optional

Drawing Properties - Required

Enable Plant Editing

Enable System Editing

EquipNextSeqNo

Export to CAD definition file

InstrLoopNextSeqNo

InstrNextSeqNo

OPCItemTag

PlantStyleFile

Rules Library

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 26/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

StockpileItems

Terminator Style

You can modify your default reference data settings for your plant using Smart P&ID Options Manager. You can define the settings for each of the following default files: rules library, default template, default piping symbol file, default duct symbol file, default signal line symbol file, format reference file, and default terminator style, as well as various locations for PDS 3D

files and passwords. You can define the following default styles and formats: default terminator style, pipeline name attributes, duct run name attributes, and signal name attributes.

You can define default paths for the following types of directories or drives: **Catalog Explorer** root directory, default P&ID template directory, default report template directory, and default drawing file directory.

Data locations for the default pipe, ducting, and signal run symbol files must be entered as a *relative* path based on the path defined for the **Catalog Explorer** **Root Path** setting. The data location for the default template file must be entered as a relative path based on the path defined for the P&ID template directory.

The path that is written to the database when you place an item in Smart P&ID and the data path in Smart P&ID Options Manager must be the same. If the paths are different, the software displays the symbol as an unintelligent graphic. If you run the **Update** **Drawings** report in Drawing Manager, this report indicates when the paths do not match. Also, the CheckFilePathsCMD.dll will also detect this and report in the log file when the paths do not match. The symbol path serves as a pointer in Smart P&ID

Options Manager and is written to the database after you place a symbol; whereas the data path is a general path to the reference data.

If Smart P&ID Options Manager is missing data for **Symbology**, **Gapping**, **Tracing**, and **Distances**, then the application association has not been created in Smart Engineering Manager. In other words, Smart P&ID needs to be associated with your plant. To fix this problem, connect to a plant database that has been associated with Smart P&ID using Smart Engineering Manager. See Connect to a Database.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 27/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

When you are using projects inside Smart P&ID, remember that the reference data belongs to the Plant and is used by projects of the Plant. You cannot change reference data, such as table layouts or formats or rules, at the project level.

## **Understanding Reference Data Settings**

The reference data settings are used to specify the location of particular types of data and various default settings used in creating P&IDs and sharing data with other applications such as PDS 3D.

## **Catalog Explorer Root Path**

Specifies the node or server where the symbols for this plant are stored. Select the ellipsis beside the **Setting** value to navigate to the required path.

To ensure that the **Symbols** node in **Catalog Explorer** can be expanded, if entering the path manually, do not use a trailing ‘\’ (backslash) character. For example, the path \\DBServer\SPPID\DevSite\DevPlant\P&ID Reference Data\Symbols is entered correctly, whereas the path \\DBServer\SPPID\DevSite\DevPlant\P&ID

Reference Data\Symbols\ is incorrect.

## **Claim Mode**

Identifies the claim mode for your plant:

## **Exclusive**

Claimed items are wholly owned by the claiming project.

## **Shared**

Items can be owned simultaneously by more than one project.

You can change the claim mode only if the Claim table is empty. If it is not empty, a message box appears. Additionally, if you are operating in a project, rather than the Plant, this option is always read-only. Only model items can be claimed. See the *<*  aProduct> Modeler Help.

## **Copy Transformation Program**

Specifies the transformation program to be used during the copying process. A transformation program is delivered with the software. You can copy this delivered code and then create your https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 28/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

own customized transformation program. See *Customizing the Sample Projects* in the Smart P&ID Programmer’s Help.

## **Default Assembly Path**

Specifies the default folder where assembly files are stored. If you want users to store new assemblies in the **Catalog Explorer** by default, enter the path for a directory in the **Catalog** **Explorer Root Path** field. Select the ellipsis beside the **Setting** value to navigate to the required path.

To save an assembly, you must have write permission for this folder. Additionally, if you do not choose a folder that is in the reference data folder, along with the other symbols, your assemblies are not displayed in nor available for placement from **Catalog Explorer**.

## **Default Duct Symbol File**

Specifies the default symbol used to represent ducting when two in-duct components are placed directly beside one another in a P&ID. For example, when two in-duct components, such as a duct nozzle and a flowmeter, are placed so that they touch, the software highlights the shared connect point. If you define a default ducting symbol, the two items are automatically connected with a ducting segment. If no default ducting symbol is defined, the software does not generate the connecting ducting segment. Select the ellipsis beside the **Setting** value to select the required file.

This value must be entered as a *relative* path based on the path defined for the **Catalog Explorer** **Root Path** setting, for example: Ducting\Routing\DuctRun.sym.

## **Default Pipe Symbol File**

Specifies the default symbol used to represent piping when two inline components are placed directly beside one another in a P&ID. For example, when two inline components, such as a nozzle and a valve, are placed so that they touch, the software highlights the shared connect point. If you define a default pipe symbol, the two items are automatically connected with a pipe segment. If no default pipe symbol is defined, the software does not generate the connecting pipe segment. Select the ellipsis beside the **Setting** value to select the required file.

This value must be entered as a *relative* path based on the path defined for the **Catalog Explorer** **Root Path** setting, for example: Piping\Routing\Process Lines\Primary Piping.sym.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 29/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Default Report Template Path**

Specifies the folder where default report templates for this plant are stored, including the blank Excel template used for creating new templates. When a report template is created and added to the plant reports, the new template is also stored at this location. Select the ellipsis beside the **Setting** value to navigate to the required path.

## **Default Signal Line Symbol File**

Specifies the default symbol used to represent signal lines when two offline instruments are placed directly beside one another in a drawing. By default, this setting is blank. If no default signal line symbol is defined, the software does not generate a connecting signal line segment. For example, when two offline instruments are placed so that they touch, the software highlights the shared connect point. If a default signal line symbol is defined in **Settings**, the two items are automatically connected with a signal line segment. Select the ellipsis beside the **Setting** value to select the required file.

You must enter this value as a *relative* path based on the path defined for the **Catalog Explorer** **Root Path** setting, for example: Instrumentation\Signal Line\Connect to Process.sym.

## **Delete Key Default Behavior**

Specifies the default behavior when you select drawing items and press the **Delete** key or select **Delete**

on the toolbar. he available options are:

## **Delete to Plant Stockpile**

Deletes the item from the drawing and sends it to the plant stockpile. This is the default setting when you create a new plant.

## **Delete to Drawing Stockpile**

Deletes the item from the drawing and sends it to the drawing stockpile.

## **Delete from Model**

Deletes the item from the drawing and from the database.

The **Delete to Plant Stockpile** and **Delete to Drawing Stockpile** options only take effect for item types that appear beside the **Stockpile Items** property.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 30/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Display Undefined As**

Specifies how a null value appears in the **Properties** window. When you select **Display Null** from the **Properties** window toolbar, you see this value for all properties that are null. Use the **Null** setting definition if you are using the PipeSpec Commodity Code Lookup utility.

**Drawing Properties - Optional**

Specifies the properties that appear on the **New Drawing** dialog as optional when you create a new drawing in the Smart P&ID Modeler. If a value already appears on the **Drawing** **properties - Required** list, you are prompted before assigning it as **Optional**. These fields are comma-delimited, for example: Version, Description.

**Drawing Properties - Required**

Specifies the properties that appear on the **New Drawing** dialog as required when you create a new drawing in the Smart P&ID Modeler. If a value already appears on the **Drawing** **properties - Optional** list, you are prompted before assigning it as **Required**. These fields are comma-delimited, for example: Version, Description.

## **DuctRun Name Attributes**

Specifies the common properties of ducts that belong to the same duct run. For example, if tag sequence number and fluid code are used to define a duct run, all connected ducts that have the same tag sequence number and fluid code belong to the duct run. To specify the properties used to define a duct run name, select the desired properties one-by-one from the list of properties in the **Setting** column. To remove a property from the duct run name, highlight that property including the preceding or following comma separator and on the keyboard, press **Delete**.

To enable deletion of duct runs to a stockpile, at least one property must be defined for this setting. Also, when deleting a particular duct run to the stockpile, at least one of those properties specified must be populated with a value in the drawing.

The duct run name attributes that you select affect the behavior of the **Delete to** **Stockpile** (**Plant** or **Drawing**) commands for duct runs. When using one of the **Delete** **to Stockpile** commands, if the duct run to be deleted has the same values as another duct run in the plant for all of the attributes selected as the duct run name definition, the software will delete that duct run from the model instead of moving it to the stockpile.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 31/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

For example, if **Tag Seq No** and **Duct Width** are specified as the duct run name attributes and in a drawing the duct run to be deleted has values **Tag Seq No** = **100** and **Duct Width** = **15 in**, then the **Delete to Stockpile** commands actually delete that duct run from the model if another duct run with these attribute values already exists in the plant.

## **DuctRunNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for duct runs. If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the duct run. As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for duct runs in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

**Enable “Keep Checked Out” on Check-In**

Allows you to check in a drawing but still keep the drawing checked out for further work. All claims are maintained.

When working with projects in an integrated environment, you must select **No** for this option.

## **Enable Piping Specification Validation**

Enables continuous service limits validation and automatic commodity code lookup if the **Use** **Piping Specification** setting is **PDS3D,**  **Smart 3D**, or **Smart Reference Data** and this setting is **Yes**. If the **Use Piping Specification** setting is **PDS3D,**  **Smart 3D**, or **Smart Reference** **Data** and this setting is **No**, *continuous* service limits validation and automatic commodity code lookup are not available. However, you can still manually select the **Calc** buttons to activate the **Commodity Code Lookup** dialog or the **Piping Materials Class** selection dialog. The **Calc** buttons are enabled for the **Piping Materials Class** and **Commodity Code** properties by assigning Calculation IDs in Data Dictionary Manager. See Enter Required ProgIDs.

## **Enable Plant Editing**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 32/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Specifies whether the **Engineering Data Editor** is enabled to manage data for all objects in the plant or only for objects in the active drawing and active drawing stockpile. If set to **Yes**, data values that you are allowed to change for objects that belong to a non-active drawing will be enabled for editing, provided that the drawing has not been opened by a user. If set to **No**, all data values for objects that belong to non-active drawings will be displayed as read-only.

For new or upgraded plants, the default value of this setting is **Yes**.

## **Enable System Editing**

Specifies if system wide changes in item values can be made automatically while editing. If set to **Yes**, when you change a value on an item, the new value is propagated to other connected items. These changes take place based on any existing rule settings.

## **EquipNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for equipment. If the tag sequence number property is left blank or a duplicate is entered, the software uses the value entered here as the tag sequence number for the piece of equipment.

As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for equipment in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

## **Export to CAD Definition File**

Specifies the Excel workbook used to associate filters in the design software with layer names in AutoCAD and level numbers in MicroStation. The software uses this definition file to tag items in a drawing with the layer name or level number on which the item should appear when the drawing is saved as an AutoCAD or MicroStation file. Select the ellipsis beside the **Setting** value to select the required file.

**Heat Tracing Media - Double Heat Trace**

Specifies a list of heat tracing media used to define which connectors are double heat traced.

If a value already appears on the **Heat Tracing Media - Jacketed pipe** list, you are prompted before assigning it as double heat traced. These fields are comma-delimited, for example, FAJ, FBJ. To un-assign a value, highlight the value in the field and press the **Delete** key.

**Heat Tracing Media - Jacketed Pipe**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 33/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Specifies a list of heat tracing media used to define which connectors are jacketed. If a value already appears on the **Heat Tracing Media - Double heat trace** list, you are prompted before assigning it as jacketed. These fields are comma-delimited, for example, FAJ, FBJ. To un-assign a value, highlight the value in the field and press the **Delete** key.

To define a heat tracing medium as a single heat trace, that medium should not be assigned either to **Heat Tracing Media - Double Heat Trace** or to **Heat Tracing Media**

- **Jacketed Pipe**.

If you apply a heat tracing medium designated as **Heat Tracing Media - Jacketed Pipe** to a drawing item other than a pipe run, the software displays graphics from the **Jacket** layer of the symbol defined in Catalog Manager. For a heat tracing medium designated as a single or double heat trace, software displays graphics from the **Heat Trace** layer of the symbol defined in Catalog Manager.

## **Import Map Path**

Defines where your map files reside on the system. An import map file is used to match attributes during the import process. Select the ellipsis beside the **Setting** value to navigate to the required path.

## **Import Transformation Program**

Specifies the transformation program to be used during the import process. This program controls the depth of the data transformation. A transformation program is delivered with the software. You can copy this delivered code and then create your own customized transformation program. See *Customizing the Sample Projects* in the Smart P&ID

Programmer’s Help.

## **InstrLoopNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for instrument loops. If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the instrument loop. As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for instrument loops in this plant. If you want to start with sequence numbers of https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 34/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

## **InstrNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for instruments. If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the instrument.

As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for instruments in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

**Max-Temperature Unit in PDS3D**

Specifies the units used for maximum temperature in PDS 3D. You can select **Deg-F**, **Deg-C**, **Deg-K**, or **Deg-R** from the list for this setting. The PipeSpec Commodity Code Lookup utility uses this setting.

## **OPCItemTag**

Specifies the next number used to automatically generate a unique tag sequence number for off-page connectors (OPCs). If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the OPC. As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for OPCs in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

**PDS Approved Reference Database Schema Name**

Type the user name created for the **ra** schema of the PDS 3D project.

**PDS Approved Reference Database Schema Password**

Type the password for the user created for the **ra** schema of the PDS 3D project.

## **PDS Database Name**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 35/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Type the name of the PDS database. This field is required for Microsoft SQL Server databases.

**PDS Database Server/Alias**

Type the name of the PDS server or an alias. This server name is required for Microsoft SQL

Server database. An **Alias** name on the client computer is required for an Oracle database.

## **PDS Database Type**

Select the type of database. Valid options include Oracle or Microsoft SQL Server.

**PDS Project Control Database Schema Name**

Type the user name created for the **pd** schema of the PDS 3D project.

**PDS Project Control Database Schema Password**

Type the password for the user created for the **pd** schema of the PDS 3D project. This user must have access privileges in both the **ra** and **pd** database schemas.

## **PID Template Path**

Specifies the storage location of templates used to create drawings in the design software.

When a new template is created, the template is also stored in this directory by default. Select the ellipsis beside the **Setting** value to navigate to the required path.

**Pipe Jacket Nominal Diameter Configuration File**

Specifies the name and path of the XML file used to store the spec showing the allowed jacket nominal pipe diameters available for each core pipe diameter. You define this information on the **Pipe Jacket Nominal Diameter** dialog. Select the ellipsis beside the **Setting** value to select the required file.

## **Pipeline Name Attributes**

Specifies the common properties of pipe runs that belong to the same pipeline. For example, if the tag sequence number and fluid code are used to define a pipeline, all connected runs that have the same tag sequence number and fluid code belong to the pipeline. The properties selected in this setting must be available in both Pipeline and Pipe Run item types.

Any property to be published as a Pipeline property must be included in this setting. To specify the properties used to define a pipeline name, select the desired properties one-by-https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 36/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

one from the list of properties in the **Setting** column. To remove a property from the pipeline name, highlight that property including the preceding or following comma separator and on the keyboard, press **Delete**.

To enable deletion of pipelines to a stockpile, at least one property must be defined for this setting. Also, when deleting a particular pipeline to the stockpile, at least one of those properties specified must be populated with a value in the drawing.

The pipeline name attributes that you select affect the behavior of the **Delete to** **Stockpile** (**Plant** or **Drawing**) commands for pipe runs. When using one of the **Delete** **to Stockpile** commands, if the pipe run to be deleted has the same values as another pipe run in the plant for all of the attributes selected as the pipeline name definition, the software will delete that pipe run from the model instead of moving it to the stockpile.

For example, if **Tag Seq No**, **Fluid Code**, and **Max Oper Temp** are specified as the pipeline name attributes and in a drawing the pipe run to be deleted has values **Tag Seq** **No** = **100**, **Fluid Code** = **D**, and **Max Oper Temp** = **250 F**, then the **Delete to Stockpile** commands actually delete that pipe run from the model if another pipe run with these attribute values already exists in the plant.

## **PipeRunNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for pipe runs. If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the pipe run. As tag sequence numbers are used, this value changes dynamically to the next consecutive number. This value also determines the first tag sequence number that you want to use for pipe runs in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

## **Plant Insulation Specification File**

Specifies the storage location for the file that contains all the available insulation information for this plant. The plant insulation file is an .isl file. Select the ellipsis beside the **Setting** value to select the required file.

## **Plant Style File**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 37/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Specifies the storage location for the file that contains all the available symbology for this plant, such as line patterns and styles. The plant style file is an .spp file. Select the ellipsis beside the **Setting** value to select the required file.

**Revision Management Software for Publishing Documents** In an integrated environment, allows you to select the software that will add new revisions to the documents that are intended to be published from the As-Built.

## **SmartPlant Foundation**

Instructs the software to add new revisions for the As-Built using SmartPlant Foundation revision management tools. This option is only available if the plant was registered with SmartPlant Foundation.

## **Smart PID**

Instructs the software to add new revisions for the As-Built using the Smart P&ID modeler revision management tools. If needed, you can select this option for a registered plant so that when publishing documents, the software sends Smart P&ID revisions to SmartPlant Foundation instead of using the SmartPlant Foundation revision feature. This option always applies for plants that are not registered with SmartPlant Foundation.

**Revision Management Software for Publishing Project Documents** In an integrated environment for a plant in which projects are enabled, allows you to select the software that will add new revisions to the documents that are intended to be published from your projects. This setting applies independently of the revision management software setting for the As-Built.

## **SmartPlant Foundation**

Instructs the software to add new revisions for projects using SmartPlant Foundation revision management tools. This option is only available if the plant was registered with SmartPlant Foundation.

## **Smart PID**

Instructs the software to add new revisions for projects using the Smart P&ID modeler revision management tools. If desired, you can select this option for a registered plant so that when publishing documents, the software sends Smart P&ID revisions to SmartPlant https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 38/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Foundation instead of using the SmartPlant Foundation revision feature. This option always applies for plants that are not registered with SmartPlant Foundation.

## **RoomNextSeqNo**

Specifies the next number used to automatically generate a unique tag sequence number for rooms. If the tag sequence number property is left blank or a duplicate is entered, the design software uses the value entered here as the tag sequence number for the room. As tag sequence numbers are used, this value changes dynamically to the next consecutive number.

This value also determines the first tag sequence number that you want to use for rooms in this plant. If you want to start with sequence numbers of more than three digits or with another value, you can modify the default value of 100 before you begin your design sessions.

## **Rules Library**

Specifies the location of the rules library for this plant. The rules library contains rules that customize the interaction of model items when you place or manipulate these items. You can define and modify rules in Rules Manager. The rules library is a .rul file. Select the ellipsis beside the **Setting** value to select the required file.

## **Signal Name Attributes**

Specifies the common properties, or attributes, of signal lines that belong to the same signal.

To specify the properties used to define a signal name, select the desired properties one-by-one from the list of properties in the **Setting** column. To remove a property from the signal name, highlight that property including the preceding or following comma separator and on the keyboard, press **Delete**.

To enable deletion of signal lines to a stockpile, at least one property must be defined for this setting. Also, when deleting a particular signal line to the stockpile, at least one of those properties specified must be populated with a value in the drawing.

The signal name attributes that you select affect the behavior of the **Delete to Stockpile** (**Plant** or **Drawing**) commands for signal lines. When using one of the **Delete to** **Stockpile** commands, if the signal line to be deleted has the same values as another signal line in the plant for all of the attributes selected as the signal name definition, the software will delete that signal line from the model instead of moving it to the stockpile.

For example, if **Tag Seq No** is specified as the signal line name attribute and in a https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 39/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

drawing the signal line to be deleted has a value **Tag Seq No** = **100**, then the **Delete to** **Stockpile** commands actually delete that signal line from the model if another signal line with this attribute value already exists in the plant.

## **Smart 3D Plant Name**

Specifies the name of the Smart 3D plant. The PipeSpec Commodity Code Lookup utility uses this setting if **Smart 3D** is specified in the **Use Piping Specification** option.

## **Smart 3D Server Name**

Specifies the name of the server that contains the Smart 3D database. The PipeSpec Commodity Code Lookup utility uses this setting if **Smart 3D** is specified in the **Use Piping** **Specification** option.

## **Smart Reference Data Server Details**

Specifies the details of the server and plant configured in the Smart Reference Data database. See Connect to the Smart Reference Data Server. The PipeSpec Commodity Code Lookup utility uses this setting when you select **Smart Reference Data** for the **Use Piping** **Specification** option.

In Smart P&ID, when assigning a piping materials class to a pipe run, the Smart P&ID Piping Specifications dialog displays only the piping specifications available for the specified plant in this setting.

If necessary, you can replace the name with a different plant name. For example, in the connection URL **https://[Host name]/SRDWEBAPI/srd/V2/Projects(“TRAINPROJ”)** replace **TRAINPROJ** with a different plant name that you want to work with.

You must enter the Smart Reference Data server name in this format: :/ *.*  For example: IN-SPMATDBSRV:1521/SDB2012

## **Smart Resource Path**

Specifies the path to the SPPIDDataMap.xml file for this plant or project. Select the ellipsis beside the **Setting** value to navigate to the required path.

**Smart Retrieve - Apply Default Formats**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 40/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

When retrieving data, this option allows you to specify to use either the units defined in the source or the units defined in the target. If set to **No**, the retrieved property’s preferred display UOM is mapped to the P&ID format. This value is used to reformat the retrieved UOM

property value for display as the new value in the **To Do List**. If set to **Yes**, the default format for the attribute is retrieved. This value is used to reformat the retrieved UOM property value for display as the new value in the **To Do List**.

## **StockpileItems**

Specifies the item types that can appear in the plant or drawing stockpiles when items of that type are deleted from a drawing. For example, if you want to allow only vessels, exchangers, and instruments to appear in a stockpile when deleted from a drawing, select **Vessel**, **Exchanger**, and **Instrument** from the **Setting** column.

When **PipeRun** is selected in the **Setting** column, only pipe runs that have an item tag can be deleted to a stockpile.

## **Terminator Style**

Specifies the type of terminator used at the terminal end of all leader lines, such as an arrow, solid dot, solid arrow, or none.

## **To Do List Placement Zone**

Controls the freestanding placement of items called when the **SmartPlant** > **To Do List** command in Smart P&ID modeler is selected. The items are placed in the area around the drawing border. Options include **Left**, **Right**, **Top**, **Bottom**, and **Pinwheel** (the default setting).

## **Use Piping Specification**

Lists the choices for using the PipeSpec Commodity Code Lookup utility.

## **No**

No type of calculation or validation for PipeSpec.

## **PDS3D**

Specifies the PDS 3D database for piping specification. When specified, Options Manager checks corresponding settings to make sure that the PDS 3D database connections are defined.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 41/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Smart 3D**

Smart 3D database is used for piping specification. Once specified, Options Manager checks corresponding settings to make sure that the server and plant name are defined.

## **Smart Reference Data**

Smart Reference Data database is used for piping specification. Once specified, Options Manager checks corresponding settings to make sure that the server and plant name are defined.

If **Enable Piping Specification Validation** is set to **Yes** and the value for this option is set to **PDS3D**, **Smart 3D**, or **Smart Reference Data**, continuous service limits validation and automatic commodity code lookup are invoked.

If the value for this option is set to **No**, continuous service limits validation and automatic commodity code lookup are not available. Also, the **Calc** buttons for the **Piping** **Materials Class** and **Commodity Code** properties are not functional.

The **Short Value** entries in the **Piping Component Type** select list in Data Dictionary Manager are populated from the contents of the

PDS3D_SP3D_ShortCode_Correlation.txt file (located in the ..\SmartPlant\P&ID

Workstation\bin folder) according to the **Use Piping Specification** setting as follows: **PDS3D -** The **Short Value** column is populated with data from the second column of the PDS3D_SP3D_ShortCode_Correlation.txt file (AABBCC code).

**Smart 3D** or **Smart Reference Data** - The **Short Value** column is populated with data from the third column of the PDS3D_SP3D_ShortCode_Correlation.txt file.

**No** - The data in the **Short Value** column is not updated and remains what it was previously.

## **Change Reference Data Settings**

1. Select **Settings**.
2. Select the **Setting** box in the **Reference Data** row you want to modify.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 42/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Specify the new storage path, resource file, or other information that you want the plant to use by default.

Data locations for the default pipe, ducting, and signal run symbol files must be entered as a *relative* path based on the path defined for the **Catalog Explorer** **Root Path** setting. The data location for the default template file must be entered as a relative path based on the path defined for the P&ID template directory.

The symbol path that is written to the database when you create an item in Catalog Manager and the data path in Smart P&ID Options Manager must be the same. If the paths are different, the software displays the symbol as an unintelligent graphic. The symbol path serves as a pointer in Smart P&ID Options Manager and is written to the database after you place a symbol; whereas the data path is a general path to the reference data.

## **Configure Piping Specification Settings**

1. Select **Settings** in Options Manager and follow steps 2 through 4 to enable continuous service limit validation and automatic commodity code lookup.
2. Select **Yes i**n the **Enable piping specification validation** field.
3. In the **Use piping specification** field, select the **PDS3D**, **Smart 3D**, or **Smart** **Reference Data** option, depending on the type of 3D database to which you are connected.
4. Enable the **Calc** buttons for the **Piping Materials Class** and **Commodity Code** properties by assigning Calculation IDs in Data Dictionary Manager. See Enter Required ProgIDs.

If the **Use piping specification** setting is **PDS3D**, **Smart 3D**, or **Smart Reference** **Data** *and* the **Enable piping specification validation** setting is **No**, *continuous* service limits validation and automatic commodity code lookup are not available.

However, you can still manually select the **Calc** buttons to activate the **Commodity Code Lookup** dialog or the **Piping Materials Class** selection dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 43/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

If the **Use piping specification** setting is **No**, continuous service limits validation and automatic commodity code lookup are not available. Also, the **Calc** buttons for the **Piping Materials Class** and **Commodity Code** properties are not functional.

When changing the **Use piping specification** setting from **No** to **PDS3D**, Smart 3D, or Smart Reference Data, validation occurs only for items modified *after* the change.

The **Short Value** entries in the **Piping Component Type** select list in Data Dictionary Manager are populated from the contents of the PDS3D_SP3D_ShortCode_Correlation.txt file (located in the ..\SmartPlant\P&ID

Workstation\bin folder) according to the **Use Piping Specification** setting as follows:

**PDS3D -** The **Short Value** column is populated with data from the second column of the PDS3D_SP3D_ShortCode_Correlation.txt file (AABBCC

code).

**Smart 3D** or **Smart Reference Data** - The **Short Value** column is populated with data from the third column of the

PDS3D_SP3D_ShortCode_Correlation.txt file.

**No** - The data in the **Short Value** column is not updated and remains what it was previously.

1. If you are connecting to a Smart 3D database, fill in the database information in the **Smart 3D Plant Name** and **Smart 3D Server Name** fields, and then skip the rest of this procedure.
2. If you are connecting to a Smart Reference Data database, fill in the database information in the **Smart Reference Data Server Details** field, and then skip the rest of this procedure.
3. If you are connecting to a PDS 3D database, select the database type from the **PDS**

**Database Type** list. Supported database types are **MSSQL** and **Oracle**.

1. Type the database name in the **PDS Database Name** field. The database name is not required for Oracle databases. The default value of a blank space, not a null, must be assigned for Oracle databases.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 44/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Type a value in the **PDS Database Server/Alias** field. This entry defines the server name for a Microsoft SQL Server database or the **Alias** name on the client computer for an Oracle database.
2. Type the user name and password of the **ra** schema of a PDS 3D project under **PDS**

**Approved Reference Database** **Schema Name** and **PDS Approved Reference** **Database Schema Password** respectively.

1. Type the user name and password of the **pd** schema of a PDS 3D project under **PDS**

**Project Control Database Schema Name** and **PDS Project Control Database** **Schema Password** respectively.

1. In the **Max-Temperature Unit in PDS3D** list, select the unit of measurement used in PDS 3D for the maximum temperature limit for piping components.

For more information about changing reference data settings, see Change Reference

Data Settings.

The **PipeSpec Commodity Code Lookup** utility uses these settings.

The **PipeSpec Commodity Code Lookup** utility does not run on specialty piping components. If the **IsspecialtyItem** value is **True**, then the utility ignores the piping component. If the value is **False**, then the utility processes the properties for the component as usual. The **IsspecialtyItem** property is specified in Catalog Manager.

**Connect to the Smart Reference Data Server**

Smart P&ID connects to Smart Reference Data (SRD) server using the SRD Web APIs.

The SRD Web APIs use Okta’s authentication service to verify secure user access to the SRD server. After successful authentication, a connection is established, and a token is generated to maintain the connection for a specified duration.

You can retrieve the following information from the SRD server: Pipe Specs

Commodity Code

Commodity Options

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 45/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Revisions

Allowable Nominal Diameter

Service Limits

To connect to the SRD server from Smart P&ID:

1. In Options Manager, click **Settings** .
2. In the **Smart Reference Data Server Details** box, select the ellipsis “…” button.
3. In the Smart Reference Data Server and Plant Details dialog, enter the SRD server

details.

1. Select **Connect**.
2. In the **Login** window, enter the **Username** and **Password**.
3. Select **Sign In**, ** **and then select** Send Push**.

*Okta sends a notification to the authenticated Administrator. After the Administrator* *accepts the notification, a connection to the SRD server is established.*

1. Upon successful connection, the **Smart Reference Data Server Details** box displays a connection URL.

**Smart Reference Data Server and Plant Details Dialog** Provides the SRD server and plant details in Smart P&ID. See Connect to the Smart

Reference Data Server.

## **Server Issuer URL**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 46/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Specifies the Okta server issuer URL.

## **Redirect URL**

Specifies the SRD server URL which Okta will redirect after successful authentication.

## **Client ID**

Specifies the Client ID received while registering with Okta.

## **Scope**

Specifies the Smart API Service ID/Scope from Okta.

## **Plant URL**

Specifies the path where the SRD plant is configured.

## **Connect**

Initiates a connection to the SRD server and displays the Okta Authentication dialog.

The **Server Issuer URL**, **Client ID**, and **Scope** are used to identify the Okta account.

## **Open Dialog**

This dialog opens when you select an ellipsis beside a path field in the **Settings** window to specify the path.

## **Look in**

Displays the folder structure for the selected drive or network path. Double-click a folder to display any sub-folders that it might contain.

## **Drives**

Select from the list of mapped drives or select **Network** to map another drive if not shown in the list.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 47/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Convert Existing Property Formats Command (Tools**

**Menu)**

Opens the Convert Existing Property Formats Dialog, from which you can specify conversion

of formats that are applied to existing properties in the plant.

The changes you make to existing property formats have no effect on the default formats specified under the **Formats** option.

Drawing item properties with null values are ignored when converting existing formats.

## **Convert Existing Property Formats Dialog**

Allows you to select specific formats that might be used for assigned properties of Smart P&ID drawing items and of Smart P&ID data throughout the plant and to convert those formats to a different format.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 48/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Format Category**

The format categories correspond to the main groupings that appear in the **Tree** view of Format Manager. The values are read-only.

**Current Forma**t

Select the format in the particular format category that you want to convert *from* for existing property values in the plant. By default, the default format as defined under the Options Manager **Formats** is displayed.

## **Convert to Format**

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 49/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

Select the format in the particular format category that you want to convert *to* for existing property values in the plant. By default, a blank value is displayed, indicating no change of format.

The lists in the **Current Format** and **Convert to Format** columns include all formats defined under the format category in Format Manager, including user-defined formats.

You can specify the conversion of only *one* current format for each format category each time you select **Apply**. You can convert additional formats under those format categories by selecting new values under the **Current Format** and **Convert to Format** columns.

## **Format Conversion Example**

When converting formats that apply to existing item properties, the conversion applies to Smart P&ID data, according to the software programs that are installed, in the entire plant.

This example demonstrates how conversion of the following formats affects item properties in a P&ID drawing.

**Format Category**

**Current Format**

## **Convert to Format**

### Pressure

Pressure-psi

Pressure-BarG

Temperature

Deg-F

Deg-C

Thickness

Thickness-in

Thickness-cm

Thickness

Thickness-in(symbol)

Thickness-cm

1. Place a pipe run in a drawing and assign the following property values and formats: https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 50/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

In this example, there are two properties (**Insulation Thk** and **Schedule Or Thk**) whose current formats belong to the same format category (Thickness) but which have different formats: *Thickness-in* and *Thickness-in(symbol)* respectively. The software only allows you to convert one format at a time per format category, therefore the procedure for implementing this conversion is as follows:

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 51/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Close all drawings in the plant for which you want to convert the property formats.
2. In Options Manager, select **Tools** > Convert Existing Property Formats to display the

Convert Existing Property Formats Dialog.

1. Select the format options as shown.
2. Select **Apply**.
3. Open the example drawing and view the **Properties** window to see the result of converting these property formats:

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 52/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Close the drawing.
2. To convert the second format, *Thickness-in(symbol),*  which affects the **Schedule Or** **Thk** property, select the format option as shown.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 53/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

1. Select **Apply**.
2. Reopen the example drawing to see the result of converting this property format: https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 54/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Importing and Deleting Linear Patterns and Styles**

You can import new linear patterns and styles to use in various ways in symbology and also delete patterns and styles that you do not use.

Linear patterns are imported from symbol files. When you import a pattern, point styles referenced by that file are also imported. To assign a newly imported pattern in the **Symbology** table or heat tracing style in the **Tracing** table, you must close Smart P&ID

Options Manager and re-open it.

You can also delete patterns from the list of available patterns. However, if a style or pattern is in use in Smart P&ID Options Manager, it cannot be deleted.

New linear patterns are created using the Line Style Editor, which is an add-on for Catalog Manager. Style resource documents can be any . *igr* document, . *spp*, or . *rsc* line style file that contains styles native to that document. The *projectstyles.spp* file contains the default symbology. Using Catalog Manager, you can add *projectstyles.spp* as a resource. When you open a new symbol file using the Line Style Editor, all styles are listed. Styles appearing in bold are currently available to you. You can modify any symbol file that appears (including styles that do not display in bold) and then you must save the symbol file. Refer to Catalog Manager Help for details about using the Line Style Editor.

Using Options Manager, you can import the symbol file. On the Linear Patterns Dialog, select **Import**. Be sure and save to your project style file. To use any imported symbols, you need to update. You can use the **File** > **Out-of- Date Drawings** > **Update Drawings** command in Drawing Manager or select **Tools** > **Update Symbology** in Smart P&ID. If you use **Tools** > **Update Symbology** in Smart P&ID, only the current drawing will update.

If you import a new pattern or style that has the same name as a pattern or style that is already listed on the Linear Patterns Dialog, the new information immediately overwrites

the older pattern or style.

If a linear pattern or style name exists in the *projectstyles.spp* file with the same name as a filter specified in the **Symbology** view, then the filter uses that particular linear pattern or style.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 55/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

As soon as you import linear patterns or styles, the new information is immediately written into the project styles file. There is no option to save the changes later.

You can also import linear styles, which incorporate linear patterns, for heat tracing symbology. The words *heat trace* must appear in the name of the style in order for Smart P&ID Options Manager to import the style.

You can chose a different linear pattern and style from the one specified with the filter, by using the **Color**, **Width**, and **Pattern** lists in the Symbology view.

## **Linear Patterns and Styles**

Linear patterns and linear styles are the basic graphical elements of your symbols. Using the **Symbology** view in Options Manager, you can choose a filter and a linear pattern and style to represent an item on your drawing. Smart P&ID Options Manager is supplied with a set of linear patterns and styles that can be found in the *projectstyles.spp* file. You can also create your own custom patterns and styles using the Line Style Editor, an add-in for Catalog Manager. See the Catalog Manager Help.

## **Linear Pattern**

Specifies the basic design of your line consisting of a series of dashes and gaps (strokes).

For example, **- /\ - /\ -** or **— … — … — …**  . You can use different patterns to represent different items on your drawings such as pipelines or cables.

## **Linear Style**

Defines the formatting, such as color and line width, which is applied to your linear pattern.

You can have the same linear pattern with different styles. The same pattern with different styles can be used to represent the same item type that have different uses. For example, gas- and liquid-carrying pipelines could both be represented on your drawing by the linear style **— … — … — …** , but with different line color and width to distinguish between a liquid-carrying pipeline and a gas-carrying pipeline.

**Linear Patterns Command (Tools Menu)**

Opens the Linear Patterns Dialog, which allows you to import or delete linear patterns.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 56/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

You can also import linear styles, which incorporate linear patterns, for heat tracing symbology. The words *heat trace* must appear in the name of the style in order for Smart P&ID Options Manager to import the style.

## **Linear Patterns Dialog**

Allows you to import or delete linear patterns. This dialog opens when you select **Tools** >

Linear Patterns on the menu bar.

## **Linear Patterns**

Lists all the available linear patterns. This list supports single entry selection only.

## **Import**

Opens the **Import Linear Patterns From** dialog, where you can browse to the file that is your linear style and import it. Linear patterns and styles are stored in symbol (.sym) files. When you import a linear pattern or heat tracing style, you must close the **Linear Patterns** dialog and re- open it to see the newly imported information.

## **Delete**

Deletes the pattern you have selected in the **Patterns** list. If a style is in use, it cannot be deleted.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 57/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Linear Styles Command (Tools Menu)**

Opens the Linear Styles Dialog, which allows you to import or delete linear styles for heat

tracing symbology.

The words *heat trace* must appear in the name of the style in order for Smart P&ID

Options Manager to import the style.

## **Linear Styles Dialog**

Allows you to import or delete linear styles. This dialog opens when you select **Tools** > Linear

Styles.

## **Linear Styles**

Lists all the available linear styles. This list supports single entry selection only.

## **Import**

Opens the **Import Linear Styles From** dialog, where you can browse to the file that is your linear style and import it. Linear patterns and styles are stored in symbol (.sym) files. When you import a linear pattern or heat tracing style, you must close the **Linear Styles** dialog and re-open it in order to see the newly imported information.

## **Delete**

Deletes the style you have selected in the **Linear Styles** list. If a style is in use, it cannot be deleted.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 58/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Import a Linear Pattern**

In this dialog you import linear patterns .sym files. You can also import linear styles, which incorporate linear patterns, for heat tracing symbology. The words *heat trace* must appear in the name of the style in order for Smart P&ID Options Manager to import the style. Importing a new pattern or style with the same name as an existing pattern in the dialog, overwrites the old information with the new imported information and is immediately written into the project styles file.

1. Select **Tools** > Linear Patterns** **to display the Linear Patterns Dialog.
2. Select **Import** to display the **Import Linear Patterns From** dialog.
3. Browse to the .sym file that contains your linear pattern.
4. Select **Open**.
5. Select **Close** on the **Linear Patterns** dialog to update the information. When you next open the **Linear Patterns** dialog the imported items are available for selection.

## **Delete a Linear Pattern**

1. Select **Tools** > Linear Patterns** **to display the Linear Patterns Dialog.
2. Select the pattern you want to delete. If you want to delete more than one pattern, you must do so one at a time.
3. Select **Delete**. If a style is in use, it cannot be deleted.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 59/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Pipe Jacket Nominal Diameter Command (Tools**

**Menu)**

Opens the Pipe Jacket Nominal Diameter Dialog, from which you can specify standard jacket diameters suitable for the nominal core diameter of each jacketed pipe.

## **Pipe Jacket Nominal Diameter Dialog**

Specifies pipe and standard jacket diameter. You can also add optional jacket diameters to a specific pipe.

## **Core NPD**

Specifies the core pipe diameter as set in Data Dictionary. Values in this column cannot be deleted.

## **Jacket NPD Min**

Specifies the minimum jacket diameter available for the core pipe. The value must always be greater than the corresponding core pipe value. Values in this column cannot be deleted.

**Jacket NPD 2**, **Jacket NPD 3**, and so forth Allows you to add optional jacket sizes for a specific pipe. Select on an empty cell in the specific pipe row to add an optional jacket size.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 60/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Add Row**

Adds a new row with a specific pipe diameter from the Data Dictionary. Select an empty cell for a list of available pipes. To delete a row, select a cell in the row you want to delete, and select **Delete Row**. You can also right-select, and select **Delete Row** on the shortcut menu.

## **Add Column**

Adds another column to the table. To delete a column, select a cell in the column you want to delete, and select **Delete Column**. You can also right-click a cell, and then select **Delete** **Column** on the shortcut menu.

## **Delete Row**

Deletes the row for the currently selected cell.

## **Delete Column**

Deletes the column for the currently selected cell.

## **Save**

Sorts the data values in ascending order in each row and column and saves any changes made to the table in the XML file defined as the value for the **Pipe Jacket Nominal Diameter** **Configuration File** in the Options Manager settings. See Understanding Reference Data

Settings.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 61/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Upgrading Reference Data**

Reference data often changes between versions of the software. These changes can include deletions and additions to reference data, as well as modifications to existing data formats and locations.

After you upgrade your plant data using the Smart Engineering Manager Upgrade Utility, you

can use the Upgrade Reference Data Command to automatically change the reference data to the correct information based on the plant and database settings that were entered when your plant was created and on the requirements for the new reference data.

Any changes made to the symbology in the Icon layer is updated in the reference data when you upgrade the reference data, allowing the Catalog Explorer to load the updated images for accurate information.

Before you can upgrade the reference data and drawings for an upgraded plant, you must define user access for the plant in Smart Engineering Manager. See the *Smart Engineering Manager*  Help.

Before you use the current version of Smart P&ID with an older plant version for the first time or whenever you create custom symbols in Catalog Manager, you must run this command to upgrade the symbols to the high-resolution 64 x 64 format.

After you upgrade reference data, you cannot view it in earlier versions of the software.

For information about changes made during the reference data upgrade, see the V4RefDataUpgrade.log file, which is saved in the reference data symbol path.

**Upgrade Reference Data Command (Tools Menu)**

Makes your reference data settings compatible with the latest version of the software. This should be done only after the site and plant data have been upgraded.

To run this command successfully, permissions for the reference data folder must be set to **Full Control**.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 62/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Upgrade Reference Data**

1. Select the site server and plant for which you want to upgrade reference data.
2. Select **Tools** > Upgrade Reference Data. The software displays a splash screen and then a message box to inform you of a successfully completed upgrade operation.
3. Select **OK**.

You must use this command before you can access reference data information from any plants created in an earlier version of the software.

Before you use the current version of Smart P&ID with an older plant version for the first time or whenever you create custom symbols in Catalog Manager, you must run this command to upgrade the symbols to the high-resolution 64 x 64 format.

Any changes made to the symbology in the Icon layer is updated in the reference data when you upgrade the reference data, allowing the Catalog Explorer to load the updated images for accurate information.

After you upgrade reference data, you cannot view it in earlier versions of the software.

For information about changes made during the reference data upgrade, see the V4RefDataUpgrade.log file, which is saved in the reference data symbol path.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 63/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Generating Symbol Images**

An administrator or a user with read/write access to the **Symbols** folder can generate images for the symbols so that when a user with read-only access opens a drawing for the first time, Catalog Explorer loads images for all symbols in a plant.

Symbol images are automatically generated when the reference data is upgraded, but when a new plant or symbol is created or when you make changes to the symbology in the Icon layer and you want those changes to be reflected in the symbol images, you must run the Generate

Symbol Images Command.

**Generate Symbol Images Command (Tools Menu)**

Generates JPEG images for all symbols in the **Symbols** folder, enabling Catalog Explorer to display updated images of all symbols of a plant. When you run this command, the CatalogExplorerSettings.bin file is created or updated for faster processing, reducing the time taken to load images in Catalog Explorer when multiple users are connected to the plant.

To run this command successfully, permissions for the reference data folder must be set to **Full Control**.

To generate images, select **Tools** > **Generate Symbol Images**.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 64/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our

documentation web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To join in conversations about Smart P&ID, go to Technical User Forums

[https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf](https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf) and join the

**Engineering & Schematics TUF** group.

## **Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, Intergraph, or its affiliates, parents, subsidiaries retains ownership of the product.

You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 65/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

**Copyright Notice**

## **Copyright**

Copyright © 1999-2024 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB and/or its subsidiaries and affiliates.

## **U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below.

For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014

and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division 305 Intergraph Way

Madison, AL 35758

## **Documentation**

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

## **Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 66/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

## **Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

## **Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 67/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL

EVALUATION AS TO THE USEFULNESS OF THE SOFTWARE IN HIS OWN

ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

## **Limitation of Damages**

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

## **Export Controls**

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 68/70

3/13/25, 10:44 AM

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

## **Trademarks**

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, Intergraph Smart® Cloud, PDS®, FrameWorks®Plus, I-Route, I-Export, Isogen®, Intergraph Spoolgen®, SupportManager®, SupportModeler®, SAPPHIRE®, TANK®, PV Elite®, CADWorx®, CADWorx DraftPro®, GT STRUDL®, CAESAR II® , and HxGN SDx®

are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners.

Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 69/70

3/13/25, 10:44 AM

Hexagon Documentation Site Export

## **Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/b47a4e2c-6862-492b-bcf7-c00eec96161c 70/70