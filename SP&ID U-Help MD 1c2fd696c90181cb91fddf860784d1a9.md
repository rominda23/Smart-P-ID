# SP&ID U-Help MD

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Utilities Help**

## **Hexagon Documentation**

Generated 03/13/2025

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 1/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Table of Contents**

Intergraph Smart® P&ID Utilities

Analyze and repair drawings

Check Item Paths Utility

Check Symbols Utility

Clean Data Utility (DelOrpModItems.dl )

Duplicate Item Tag Report Utility

Local Model Item Lookup Table Utility

Update Labels Utility

Updating Symbology

Fixing Orphaned Drawing Symbols

Smart PID Analyzer

Piping Specification Utility

Update Zero Length Pipe Run Connectors Utility

Find Invalid Break Labels Utility

Log Files

Enable enhanced logs

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 2/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart® P&ID Utilities**

Intergraph Smart® P&ID delivers several utilities to help you manage your data.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 11/14/2024 at 1:19 PM

## **Analyze and repair drawings**

Use the Service Pids utility to analyze and repair drawings with bad relationship indicators. The utility processes all graphic connections on all the selected drawings of the active plant and reports on all relationships in the graphic file and in the database. During processing, the Service Pids utility generates a detailed log. You can access the log file in the Temp folder.

You cannot use or access the plant while the utility is processing drawings.

You cannot run the Service Pids utility if a drawing is open or in a recreate state. However, you can use the Relationship Indicator Repair Utility to repair and report an open drawing.

**Run the Service Pids utility manually in the user interface (UI)** The Service Pids utility processes drawings in the active plant only. To process a different plant, you must close the Service Pids utility and change the active plant in Smart P&ID.

1. In **Windows Explorer**, browse to the [Product Folder]\P&ID Workstation\bin folder, then and double-click **servicepidsexe.exe**.
2. On the **Service Pids** dialog, select **Show Drawings** to see a list of all the drawings associated with the active plant.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 3/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select the drawings to process.

If you want to select all the drawings, choose **Select All**. To clear the selection, choose **Select None**.

1. Choose what do you want to do next.

**To do this**

## **Choose this option**

### Analyze and generate a report

## **Report**

### on the selected drawings

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 4/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Analyze and repair broken

**Repair & Report**

relationships in the selected

drawings

The **Status** column shows the current status of each drawing:

- indicates that the drawing is being processed.
- indicates that the drawing was processed successfully.
- indicates that the drawing is either open or in a recreate state and could not be processed.
1. To see the report or repair details, select **View Logfile.**

You can save the log file as a text file and then print it.

1. To close the utility, select **Close**.

**Run the Service Pids utility automatically using the Windows Task** **Scheduler**

When you run the utility using the Windows Task Scheduler or the command prompt, you can repair and report drawings in projects from different sites. However, before running the utility, you must provide the necessary site, plant, and project details in an Excel file format.

For a plant with projects, such as an as-built plant, the plant and project names are different. If the plant does not have any projects, enter the plant name in the **plant** and **project** https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 5/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

columns.

**Where do I find the plant and project names?**

There are different ways to obtain the necessary plant and project names. In general, look for the corresponding icons in the **Plant Structures** hierarchy. Each icon represents a unique plant or project.

**Icon**

## **Indicates**

### Plant

Project

This node is visible only if the plant has projects.

## **Using Drawing Manager**

From the File menu, select Open database to see all the available plants and projects under the active site. In the list, the root node represents the plant. If the plant has projects, the sub-node represents a project.

## **Using Smart Engineering Manager**

If you are an administrator or if you have necessary access to Smart Engineering Manager, you can see a comprehensive list of plants and projects under the active site.

In the tree view, expand the **Plant Structures** node and look for the corresponding plant and project icons.

## **Create the Excel file**

1. Open Microsoft Excel on your computer.
2. In the first row, create the **INI file path**, **plant**, and **project** column headers.
3. In the Excel sheet, fill in the rows with the necessary details for each project that you want to analyze.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 6/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Save the Excel file in a location of your choice.

## **Schedule a recurring task**

1. Open Windows Task Scheduler.
2. In the **Task Scheduler** > **Actions** pane, select **Create Basic Task**.
3. Enter a name and description for the task, and then select **Next**.
4. For a recurring task, choose either **Daily**, **Weekly**, or **Monthly**, depending on how often you want to run the **Service Pids** utility.
5. Select **Next**.
6. Depending on your choice, configure specific settings such as the start time, frequency, and days of the week or month.
7. Select **Next**.
8. Choose **Start a program**, and then select **Next**.
9. Browse and select the **servicepidsexe.exe**.
10. In the **Add arguments (optional)** box, type **Command “[Excel file path]”** .

Replace [Excel file path] with the actual path. For example, **Command**

**“C:\Users\Documents\MyExcelFile.xlsx”** .

1. Select **Next**, ** **and then select** Finish**.

For information on repair and report process status, check the **ServicePids.log** file in your temporary folder.

**Run the Service Pids utility manually using the command prompt** When you run the utility using the Windows Task Scheduler or the command prompt, you can repair and report drawings in projects from different sites. However, before running the utility, you must provide the necessary site, plant, and project details in an Excel file format.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 7/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

For a plant with projects, such as an as-built plant, the plant and project names are different. If the plant does not have any projects, enter the plant name in the **plant** and **project** columns.

**Where do I find the plant and project names?**

There are different ways to obtain the necessary plant and project names. In general, look for the corresponding icons in the **Plant Structures** hierarchy. Each icon represents a unique plant or project.

**Icon**

## **Indicates**

### Plant

Project

This node is visible only if the plant has projects.

## **Using Drawing Manager**

From the File menu, select Open database to see all the available plants and projects under the active site. In the list, the root node represents the plant. If the plant has projects, the sub-node represents a project.

## **Using Smart Engineering Manager**

If you are an administrator or if you have necessary access to Smart Engineering Manager, you can see a comprehensive list of plants and projects under the active site.

In the tree view, expand the **Plant Structures** node and look for the corresponding plant and project icons.

## **Create the Excel file**

1. Open Microsoft Excel on your computer.
2. In the first row, create the **INI file path**, **plant**, and **project** column headers.
3. In the Excel sheet, fill in the rows with the necessary details for each project that you want to analyze.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 8/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Save the Excel file in a location of your choice.

## **Run the Service Pids utility**

1. Open a command prompt window.
2. Navigate to the drive where the **servicepidsexe.exe** executable is located.
3. Type the following command:

servicepidsexe.exe “[Excel file path]”

Replace [Excel file path] with the actual path. For example, servicepidsexe.exe

“C:\Users\Documents\MyExcelFile.xlsx”

1. Press ENTER.

For information on repair and report process status, check the **ServicePids.log** file in your temporary folder.

**Repair and report an open drawing**

Use the **Relationship Indicator Repair Utility** to report and repair bad relationship indicators in a specific drawing. The utility processes all graphic connections on the active drawing and verifies all relationships in the graphic file and in the database.

You cannot run the **Relationship Indicator Repair Utility** on a plant.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **repairrelindcmd.dll**.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 9/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Choose **Report** and select **OK** to evaluate the relationships indicators.
2. After the reporting process is complete, review the **RepairReport-RelIndicators.log** report to check for any relationship indicator errors.
3. If there are any errors, choose **Repair & Report** and select **OK**. Otherwise, skip to step 8.
4. After the repair process is complete, review the **RepairReport-RelIndicators.log** to check if the errors are resolved.
5. Close and reopen the drawing before making any further modifications.

## **Check Item Paths Utility**

The Check Item Paths utility (CheckFilePathCmd) checks the folder paths in the file names of all active plant items and reports paths that do not point to the current catalog. This macro details invalid paths in a log file named CheckFilePathsFor_ *YourPlant*.log in the Temp folder.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **CheckFilePathCmd.dll**.

## **Check Symbols Utility**

The Check Symbols utility (CheckSymbolsCmd.dll) checks the specified plant catalog for symbols for: Graphics other than: igArc2d, igBalloon, igBoundary2d, igBsplineCurve2d, igCircle2d, igDimension, igEllipse2d, igEllipticalArc2d, igLeader, igLine2d, igLineString2d, igTextBox, and igPoint2d

ConnectPoints with an incomplete connect point attribute set.

Duplicate Connect Point Keys.

Incorrectly ordered (not sequential) Connect Point Keys.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 10/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Piping / Signal / Ducting points (if the symbol is an OPC symbol).

Property ‘UsePhotographicStyleScale’ = True (this value is not valid for symbols in Smart P&ID) You should run this utility at least once on all plants. After running this initial check, run this utility each time symbols are edited in Catalog Manager. Results are written to the log file named CheckSymbolsFor_ *PlantName*.log in the Temp folder.

You must run the utility in the SPPIDAutomation.exe environment.The utility is delivered to the ..\SmartPlant\P&ID Workstation\bin folder.

## **Check Symbols in a Plant**

1. Start Drawing Manager and select **File** > **Open Database**.
2. Select the plant containing the reference data that you want to check. Doing this sets the **ActivePlant** value for the utility.
3. Close Drawing Manager.
4. Start the SPP&ID Automation application by double-selecting **SPPIDAutomation.exe** in the

..\SmartPlant\P&ID Workstation\bin folder.

1. If the SPP&ID Automation application does not open a document by default, complete the following steps before proceeding:
2. Select **File** > **New**.
3. Select **Document** in the **Create new** group.
4. Select **Normal.spp** from the list of templates.
5. Select **OK** to open a new document.
6. Select **Tools** > **Custom Commands** to display the **Custom Commands** dialog.
7. Browse to ..\SmartPlant\P&ID Workstation\bin and double-click **CheckSymbolsCmd.dll**.
8. Select **OK** or view the log file for detailed information.

## **Sample Check Symbol Log File**

The following sample log file contains five sets of detected errors. Below the graphic is a suggested solution for each numbered error set.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 11/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Suggested Solutions**

1. Delete symbol from existing drawings. Open the symbol in Catalog Manager, delete rectangles, and draw the graphics as lines instead of a rectangle. Place updated symbol on drawing.
2. Delete symbol from existing drawings. Open symbol in Catalog Manager, place a select set around the graphics, select **Ungroup** from the **Change** toolbar. Place symbol on drawing.
3. Delete symbol from existing drawings. Open symbol in Catalog Manager, delete connect points and add connect points. Place symbol on drawing.
4. Delete symbol from existing drawings. Open symbol in Catalog Manager, delete symbol and recreate symbol. Place symbol on drawing.
5. Delete symbol from existing drawings. From Catalog Manager, delete connect points and add Auxiliary points. Place symbol on drawing.

**Clean Data Utility (DelOrpModItems.dll)**

The Clean Data Utility (DelOrpModItems.dll), also referred to as Delete Orphan Model Items, allows you to check for problems in your database records and, if required, to run clean-ups on those records.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 12/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

You should run this utility prior to upgrading your drawings.

We recommend that you make regular back-ups of your database so that you can restore data in the event of database problems.

## **Database Report**

Generates a report, written to the **DBCleanup.txt** file in your Temp folder, that helps you decide whether a manual cleanup alternative exists before using the **Entire Database** command to delete the problems from the database. The report indicates the following problems: Broken database relationships, such as those between the Equipment and Plant Item tables, or between the Symbol and Symbol Representation tables.

Orphan model items of the item types listed below under **Model Items**.

## **Entire Database**

Runs the report and removes orphaned records from the plant database. This option includes all the clean-ups performed by the **Model Items**, **OPCs**, and **Gaps** options. Run this option *only* after running the **Database Report** option and examining the report.

## **Model Items**

Finds and deletes any model item in the database that does not have a corresponding entry in the T_Representation table. The utility works on an item type basis and repairs the following model item types: Vessel, Mechanical, Exchanger, Equipment: Other, Equipment Component, Instrument, Nozzle, Piping Component, Ducting Component, Pipe Run, Signal Run, Duct Run, OPC, Item Note, Area Break, Room, and Room Component. After the orphan model items for an item type are found, you can select any or all of the items and choose to delete them.

## **OPCs**

Finds and repairs off-page connectors (OPCs) that have lost their associations with the OPC with which they were originally paired. If one OPC has lost the identity of its mated OPC, but the mated OPC still has the identity of the first OPC, then the OPC is considered repairable. To repair the OPC, the utility updates the identity information for the first OPC. However, if both the OPC and its mated OPC have lost the identities of each other, then the OPCs are considered non-repairable, and you are given the option to delete them.

## **Gaps**

Repairs and updates gaps in the representation record with the proper item type. On rare occasions you will need to perform this operation if you have gapping problems in your drawings.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 13/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

We do not recommend using the **Gaps** command as part of your database constraint cleanup. If you find it necessary to run **Gaps**, you must be careful not to select **Yes** for a symbol that is not a gap. If you select **Yes** for any symbol other than a gap, your data set might get corrupted.

**Clean Data (Delete Orphan Model Items)**

The clean data utility allows you to check your database for broken database relationships or orphan drawing items and to clean up the database by deleting orphan model items.

You must run the Clean Data utility from within the Smart P&ID modeler.

For easy access to this utility, you can create a custom menu in the Smart P&ID interface to run the Clean Data utility. See *Create a New Menu* in the Smart P&ID Help.

Log messages generated when orphaned records are deleted from the plant database are written to the DBCleanup.txt file in the folder assigned to the TEMP environment variable.

Log messages are placed in SPDelOrpModItems.log file in the folder assigned to the TEMP

environment variable. The log file contains information about deleted items including the item type and SP_ID number.

## **Generate a Report**

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **DelOrpModItems.dll**.
4. On the **Clean Data** dialog, select **Database Report**. The results are written to the **DBCleanup.txt** file in your localTemp folder. This report helps you decide if a manual cleanup alternative exists before using the **Entire Database** command to automatically delete the problems from the database.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 14/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Perform Automatic Database Clean-Up**

Before starting the clean-up, ensure that all other users have logged out of the plant.

1. Select **Entire Database** to generate the report and automatically delete the problems from the plant database. This command results in the deletion of items where there are problems of referential integrity or non-unique records and includes all the clean-ups performed by the **Model** **Items**, **OPCs**, and **Gaps** options.

Running this option results in the deletion of many corrupted records in the database. To perform a less drastic set of clean-ups, skip this step and follow the rest of the steps in this procedure.

1. Select **Model Items**.
2. On the **Delete Orphan Model Items** dialog, select each model item type from **Item Type Names** list to see if any orphan items exist in the database. The following model item types are checked: Vessel, Mechanical, Exchanger, Equipment: Other, Equipment Component, Instrument, Nozzle, Piping Component, Ducting Component, Pipe Run, Signal Run, Duct Run, OPC, Item Note, Area Break, Room, and Room Component.
3. In the **List** view, select the model orphan items to delete, and select **Delete**. You can also select **Delete All** to select and delete all the items in the list view.
4. Select **Close** to return to the **Clean Data** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 15/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. On the **Clean Data** dialog, select **OPCs**.
2. On the **Repair OPCs** dialog, chose repairable or non-repairable from the **OPC Type** list.

Repairable OPC pairs retain one link out of two between the mates. Non-repairable OPC pairs retain neither link.

1. Choose the OPC pair you are interested in from the **OPC** list, and select **Fix** if it is a repairable pair or **Delete** if it is non-repairable.
2. Select **Close** to return to the **Clean Data** dialog.
3. On the **Clean Data** dialog, select **Gaps** to find and repair gaps that do not have the correct representation in the database.

We do not recommend using the **Gaps** command as part of your database constraint cleanup. If you find it necessary to run **Gaps**, you must be careful **not** to select Yes to a symbol that is not a gap. If you select Yes to any symbol other than a gap, you might corrupt your data set.

1. On the **Clean Data** dialog, select **Close** to return to the design software.

## **Duplicate Item Tag Report Utility**

The Duplicate Item Tag Report utility (Duplicate Tag Report.exe) helps you locate instruments, piping components and equipment that have the same item tag. The utility creates a Microsoft Excel spreadsheet in a temporary folder (usually C:\Temp) on your computer. The spreadsheet is named *PlantName*-DuplicateTags.xls, where *PlantName* is the name of the active plant.

1. Double-click **Duplicate Tag Report.exe** in the ..\SmartPlant\P&ID Workstation\bin folder.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 16/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **Connect to Active Plant**. The name of the active plant displays.
2. Select **Create Duplicate Item Tag Report**.
3. Select **Close**  to exit the utility.
4. Open the report spreadsheet from your local Temp folder.

**Local Model Item Lookup Table Utility**

Use the LocalModelItemLookupTable.sql utility if your connected Workshare satellite experiences performance problems when transferring piping data from Smart P&ID to PDS. This script converts a satellite database view (namely, the T_ModelItemLookup) that references a host table into a local table, allowing the data transfer to proceed without using a database link.

Smart P&ID uses the database link to fetch unique Long IDs from the Host when running from a connected Workshare satellite. If the performance of opening the PID file in PDS is an issue or if maintaining the correlation between Smart P&ID and PDS after the merge is not an issue, then you can run this script to change the lookup for the Long ID from a view to the host to a local query.

This utility is delivered as an SQL script to the ..\SmartPlant\P&ID Workstation\bin folder and can be executed using any Oracle user interface, such as SQLPlus.

Do not use this script if the transferred PDS data will be merged back into a host PDS database because the Long IDs will not be unique at the host.

For more information about Workshare and database links, see the Workshare Configuration and Reference Help.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 17/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

For more information about transferring piping data, see the Smart P&ID Piping Data Transfer Configuration and Reference Help.

## **Update Labels Utility**

The Update Labels utility updates item labels in drawings where the properties of the items were changed using automation. Without this utility, the labels on these items are not updated with the new information, and they display the old values in the drawing. Use the steps below to update labels in a drawing.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **UpdateLabelsCmd.dll**.

This utility does not update the label with modifications made in Catalog Manager. If modifications were made to the label in Catalog Manager, each instance of the label must be replaced in the drawings. Use **Edit** > **Replace** to find and correct these instances.

## **Updating Symbology**

You can force the software to redraw the graphic representation of your data, the drawing, by using the **Update Symbology** command in Smart P&ID. This command refreshes the graphic symbology (that is, line weight and color) of symbols in your drawing based on the current settings in Options Manager.

The ApplySettingsCmd macro (delivered to the ..\SmartPlant\P&ID Workstation\bin folder) also updates the line settings, Minimum Connector Segment, and Routing Self-Avoidance.

The symbology and other settings defined in Options Manager usually take effect only in those drawings created after those values are defined. Updating Options Manager settings enables you to force changes in your symbology definitions to be reflected in the current drawing, regardless of when it was created.

## **Use the Update Symbology Command**

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Update Symbology**.

**Update Line Styles Using the ApplySettingsCmd Macro** 1. Open a drawing in Smart P&ID.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 18/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **Tools** > **Custom Commands**.
2. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **ApplySettingsCmd.dll**.

Anyone can update drawings using these commands. However, check your permissions to find out if you can make changes to the plant-wide symbology in Options Manager. Permissions are assigned in Smart Engineering Manager .

After you load the current plant-wide symbology definitions into your drawing, you cannot revert to previous definitions. However, you can always override plant-wide symbology choices in your drawing by using drawing filters and choosing alternate symbology for items.

In Options Manager, two settings, **Minimum Connector Segment** and **Routing Self-Avoidance**, control the behavior of pipe and signal runs when they are placed in a drawing or when an inline component is placed on a run. You can change these settings in Options Manager, but the new values affect only lines placed after the change. The ApplySettingsCmd.dll macro applies the latest settings to all runs on the current drawing. You must run this macro for every drawing individually.

## **Fixing Orphaned Drawing Symbols**

In a drawing, if you select a symbol that is missing from the database, no properties appear in the **Properties** window. When such a symbol is identified and highlighted in a drawing, it is said to be *band-aided*. Because is not possible simply to delete orphaned symbols from a drawing, the following procedures describe how they can be highlighted and removed.

**Fix Orphaned Symbols Using the OrphanGraphics Macro** This option applies to orphaned symbols in a drawing that is not in a re-create state.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **OrphanGraphics.dll**. As an alternative to using this command, you can band aid symbols in a drawing using a custom validation with the BeforeDocumentClose event.
4. Close and then re-open the drawing.

*The orphaned symbols are now band-aided in the drawing.*

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 19/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Create a new version of the drawing.
2. Open the drawing.
3. Force a re-creation of the drawing.
4. Display the SmartPlantPID.log file. The log file reports on orphaned symbols by means of statements similar to the following:

OrphanGraphics has detected a problem: PipeRun with SP_ID =

FF038B6467F8429588B86A2FE38F5667 is missing from the database (A04501) and has been band aided.

1. To view the symbols that were fixed, open the Version History for the drawing. You can also compare the current drawing with the version you created.

Using custom validation, you can specify whether the software only reports on missing symbols in the SmartPlantPID.log file or whether they are reported on and band-aided. Two functions exist in the log file for handling orphan graphics by means of validation: **ReportOrphanGraphics** reports that symbols are missing from the database.

**BandAidOrphanGraphics** reports that symbols are missing from the database and have been band-aided.

**Fix Orphaned Symbols During Drawing Re-Creation**

1. Open the drawing.
2. When prompted to re-create the drawing, select **Cancel**. The software does not re-create the drawing. However symbols missing in the database are reported in the SmartPlantPID.log file.
3. Open the drawing using Automation. Using Automation to open the drawing ensures that the symbols are band-aided. A normal opening of the drawing re-creates the drawing and removes the orphaned symbols.
4. Open the drawing manually.
5. When prompted to re-create the drawing, select **OK**.

*The band-aided symbols are initially displayed and then removed from the drawing.*

1. Display the SmartPlantPID.log file. The log file reports on orphaned symbols by means of statements similar to the following:

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 20/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

OrphanGraphics has detected a problem: PipeRun with SP_ID =

FF038B6467F8429588B86A2FE38F5667 is missing from the database (A04501).

Using custom validation, you can specify whether the software only reports on orphaned symbols in the SmartPlantPID.log file or whether they are reported on and band-aided. Two functions exist in the log file for handling orphan graphics by means of validation: **ReportOrphanGraphics** reports that symbols are missing from the database.

**BandAidOrphanGraphics** reports that symbols are missing from the database and have been band-aided.

## **Smart PID Analyzer**

The Smart PID Analyzer provides optional checking to make users aware of various problems that can arise when the contents of a drawing are not in harmony with the database. When enabled, a macro, SmartPIDAnalyzer, which is built in to the Smart P&ID modeler, runs when a user opens or closes a drawing. The macro generates a report that informs the user of any problems found in the categories that were selected for checking.

To configure the system for checking:

1. Open Windows Registry.
2. Under HKEY_LOCAL_MACHINE, create the following registry key: SOFTWARE\Intergraph\Applications\SmartPlantPID.Application\AnalyzerOptions For a Windows 7 operating system, the registry key path is: SOFTWARE\Wow6432Node\Intergraph\Applications\SmartPlantPID.Application\AnalyzerOptions 3. Set the value of AnalyzerOptions as follows to check *one* of the following categories: Unnamed linear patterns in graphics = 1

Cross checking of RAD object and database object relationships = 2

Bad connectors = 4

To disable checking, set the value to 0; to check *all* the categories, set the value to 7

(1+2+4). For a combination of checks, set the value of AnalyzerOptions to the bit sum of the individual categories, for example, to check unnamed linear patterns and bad connectors, the value of AnalyzerOptions should be set to 5 (1+4), as shown in the example.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 21/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Open the drawing. If a problem is found under one or more selected categories, a message displays prompting you to view the log file. Select **Yes** to open the SmartpidAnalyzer.log file.

The log file is in your local Temp folder.

The log file is overwritten each time a drawing with an identified problem is opened.

## **Piping Specification Utility**

The Piping Specification Utility (PipeSpec) works with PDS 3D, Smart 3D, or Smart Reference Data to validate the piping materials class with the temperatures, pressures, and diameters assigned to the pipe run and to search commodity codes (in all product databases) and fabrication categories (in PDS

3D databases only) for inline piping components. The database tables and library files in the products provide source information for the validation and search. The service limits validation and automatic commodity code look-up can be disabled simultaneously using a switch in Options Manager. See

Configure Piping Specification Settings in the Options Manager Help..

For more information about using the Piping Specification Utility with Smart 3D, refer to the Smart P&ID Installation and Upgrade Help for details about installing **Smart 3D Piping Specification** **Remote Access Client**.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 22/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

In Data Dictionary Manager, the **ValidateNomDiam.ForeignCalc** program ID, which is assigned to the **Nominal Diameter** property, starts the Piping Specification Utility and triggers the commodity code and fabrication category look-ups when a nominal diameter is changed. See Enter Required ProgIDs.

To use the Piping Specification Utility with Smart 3D, you must install the Smart 3D Piping Specification Remote Access Client, which is available on the Smart P&ID product media under **Prerequisite Software**.

To use the Piping Specification Utility with Smart Reference Data, you must first enable .NET

Framework 3.5 under Windows Features.

**PDS 3D Files Used for PipeSpec**

**pd schema** — pdtable_102 table

**ra schema** — pdtable_201 and pdtable_202 tables **library files** — us_pjstb.l, us_pjstb.l.r, and us_pjstb.l.t (The library file locations are listed in pdtable_102.)

**.dll files** — PipeSpec.dll, pdpjs.dll, pdpjsx.dll, and ValidateServiceLimits.dll The Piping Specification utility allows separate logon for the **ra** and **pd** schemas in the PDS 3D

database.

All of the displayed text strings are maintained as Visual Basic resources in the **PipeSpec.dll** file.

These strings can be translated or modified as required using a resource file editor.

When performing piping materials class validations, commodity code lookup, or validation of nominal diameter for Smart 3D or Smart Reference Data, the Piping Specification Utility assigns the highest revision number from the Smart 3D or Smart Reference Data piping materials class to the **Pipe Spec Revision** property.

Error messages are placed in the PipeSpecError.log file in the folder assigned to the TEMP

environment variable. Error messages help you identify the cause of failure when the utility does not complete the tasks as expected. For example, if minimum requirements are not met for the look-up, the missing properties are listed in the log file.

The **ServiceLimits.log** file contains any errors encountered during the Service Limit Validation process, which runs as part of the Piping Specification Utility.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 23/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Enter Required ProgIDs**

1. Select **Start** > **SPEM** > **Data Dictionary Manager**.
2. Select **Database Tables**.
3. Select each database table listed in the following table.

**Database Table**

**Property**

**Calculation ID**

## **Validation ID**

### Case

Pressure

PipeSpec.Commodity

Process

CodeValidator

Case

Temperature

PipeSpec.Commodity

Process

CodeValidator

Inline Component

NominalDiamet

ValidateNomDiam.

er

ForeignCalc

Inline Component

CommodityCod PipeSpec.Commodity

e

CodeValidator

Pipe Run

PipingMaterials PipeSpec.PMCFinder

PipeSpec.Commodity

Class

CodeValidator

- Pipe Run

NominalDiamet PipeSpec.NPDFinder

ValidateNomDiam.

er

ForeignCalc

- Pipe Run

SP_PipeSpecR

PipeSpec.Commodity

evision

CodeValidator

- Piping Component

OptionCode

PipeSpec.OptionCode

PipeSpec.Commodity

Finder

CodeValidator

The Calculation IDs for **Nominal Diameter** and **SP_PipeSpecRevision** in the Pipe Run table and **Option Code** in the Piping Component table (items marked with an (*) asterisk) are available https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 24/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

only when the pipe specification source is Smart 3D or Smart Reference Data. These validations are not available when the piping specification source is PDS 3D.

1. Double-click each property to display the **Modify Property** dialog. An example of the dialog is shown below.
2. Type the information in the given fields as shown in the example above.
3. Select **OK** to save your changes and close the dialog.
4. Repeat steps 3 through 5 to update each database table.

## **Configure Piping Specification Settings**

1. Select **Settings** in Options Manager and follow steps 2 through 4 to enable continuous service limit validation and automatic commodity code lookup.
2. Select **Yes i**n the **Enable piping specification validation** field.
3. In the **Use piping specification** field, select the **PDS3D**, **Smart 3D**, or **Smart Reference Data** option, depending on the type of 3D database to which you are connected.
4. Enable the **Calc** buttons for the **Piping Materials Class** and **Commodity Code** properties by assigning Calculation IDs in Data Dictionary Manager. See Enter Required ProgIDs.

If the **Use piping specification** setting is **PDS3D**, **Smart 3D**, or **Smart Reference Data** *and* the **Enable piping specification validation** setting is **No**, *continuous* service limits validation and automatic commodity code lookup are not available. However, you can still manually select the **Calc** buttons to activate the **Commodity Code Lookup** dialog or the **Piping Materials Class** selection dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 25/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

If the **Use piping specification** setting is **No**, continuous service limits validation and automatic commodity code lookup are not available. Also, the **Calc** buttons for the **Piping** **Materials Class** and **Commodity Code** properties are not functional.

When changing the **Use piping specification** setting from **No** to **PDS3D**, Smart 3D, or Smart Reference Data, validation occurs only for items modified *after* the change.

The **Short Value** entries in the **Piping Component Type** select list in Data Dictionary Manager are populated from the contents of the PDS3D_SP3D_ShortCode_Correlation.txt file (located in the ..\SmartPlant\P&ID Workstation\bin folder) according to the **Use Piping** **Specification** setting as follows:

**PDS3D -** The **Short Value** column is populated with data from the second column of the PDS3D_SP3D_ShortCode_Correlation.txt file (AABBCC code).

**Smart 3D** or **Smart Reference Data** - The **Short Value** column is populated with data from the third column of the PDS3D_SP3D_ShortCode_Correlation.txt file.

**No** - The data in the **Short Value** column is not updated and remains what it was previously.

1. If you are connecting to a Smart 3D database, fill in the database information in the **Smart 3D**

**Plant Name** and **Smart 3D Server Name** fields, and then skip the rest of this procedure.

1. If you are connecting to a Smart Reference Data database, fill in the database information in the **Smart Reference Data Server Details** field, and then skip the rest of this procedure.
2. If you are connecting to a PDS 3D database, select the database type from the **PDS Database** **Type** list. Supported database types are **MSSQL** and **Oracle**.
3. Type the database name in the **PDS Database Name** field. The database name is not required for Oracle databases. The default value of a blank space, not a null, must be assigned for Oracle databases.
4. Type a value in the **PDS Database Server/Alias** field. This entry defines the server name for a Microsoft SQL Server database or the **Alias** name on the client computer for an Oracle database.
5. Type the user name and password of the **ra** schema of a PDS 3D project under **PDS Approved** **Reference Database** **Schema Name** and **PDS Approved Reference Database Schema** **Password** respectively.
6. Type the user name and password of the **pd** schema of a PDS 3D project under **PDS Project** **Control Database Schema Name** and **PDS Project Control Database Schema Password** respectively.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 26/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. In the **Max-Temperature Unit in PDS3D** list, select the unit of measurement used in PDS 3D for the maximum temperature limit for piping components.

## **Performing Service Limits Validation**

The Piping Specification Utility verifies that the temperatures and pressures assigned to a pipe run comply with the service limits associated with the selected Piping Materials Class. In continuous validation mode, which is activated by assigned settings in Options Manager, this verification occurs each time you modify either the Piping Materials Class or a temperature-pressure pair in the process case data of the pipe run. The Service Limits validation requires at least one complete temperature-pressure pair from among design, alternate design, operating, and alternate operating cases. If any temperature-pressure pair violates the service limits of the selected Piping Materials Class, a warning displays the appropriate pair. This warning appears in the design software by appending an error string (‘SERVICE LIMITS ERROR’) to the name of the Piping Materials Class.

In Smart 3D, for a particular temperature-pressure pair, the service limits might also specify an accepted range of nominal diameters for the pipe run. In such cases, if the nominal diameter lies outside this range or if no value is specified for the nominal diameter, the warning also displays.

**Performing Commodity Code and Fabrication Category Look Up** The Piping Specification Utility (PipeSpec) looks up the **Commodity Code** property (in all product databases) and the **Fabrication Category** property (in PDS 3D databases only) of inline piping components. In the continuous validation mode, this look-up occurs each time the **Piping Materials** **Class** or any of the case temperatures: **Design Max Temp**, **Design Min Temp**, **Operating Max Temp**, or **Operating Min Temp** are modified on the pipe run (for Smart Reference Data, only changes in the **Piping Materials Class** or **Design Max Temp** initiate the look-up). Validation also occurs each time the **Option Code** or **Nominal Diameter** of the component is modified. If the modification occurs on a property of a piping component, then the look-up is restricted to that particular component, but if the modification occurs on a property of a pipe run, then the look-up encompasses every piping component on that run.

The minimum requirements to cause a look-up are that the piping components must be in a pipe run and that the PMC and the nominal diameter of the pipe run must be specified. If temperatures do not comply with the service limits, then the **Commodity Code** property displays an error message.

The Piping Specification Utility uses process case temperatures of the run during the commodity code look-up only if the code for the component has a maximum temperature limit value in the Smart 3D or Smart Reference Data database. For example, in PDS 3D, a value of -9999 for maximum temperature in pdtable_202 indicates a null value and the process case temperatures on that pipe run are ignored for the look-up. If a maximum temperature limit exists for a component, then the look-up ensures that none of the relevant process case temperatures assigned in Smart P&ID to the pipe run in which the piping component resides exceed this limit.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 27/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The units for the PDS 3D maximum temperature are those specified in Options Manager.

If continuous validation is turned on for the PipeSpec utility, then a pipe run with temperature-pressure limits that do not agree with its PMC generates **Error in PMC** in the commodity code for an inline component.

If any temperature values for the pipe run are unspecified, then for Smart Reference Data or PDS 3D, a value of zero Deg-K is assumed for each of the unspecified temperatures. For Smart 3D, an unspecified temperature is interpreted as ‘undefined’.

Smart 3D can validate commodity codes using the four case temperatures listed earlier against Maximum Temperature ranges or Minimum Temperatures specified on piping components in the Smart 3D database.

Smart Reference Data can validate commodity codes using the pipe run’s Design Max Temp against Maximum Temperatures specified on piping components in the Smart Reference Data database. Other case maximum temperatures or minimum temperatures will not be used in the validation.

If the temperature falls within the allowable limits, the software will return a commodity code; otherwise, **Not in Spec** is returned.

Smart Reference Data supports a *single* maximum temperature only for each option code.

Smart Reference Data does not return a commodity code for reducers.

The **Fabrication Category** property of inline piping components is a select-listed property in Smart P&ID. A relationship between the fabrication category and the commodity name can be defined in the PDS 3D database. The **Commodity Name** is a unique name for every symbol. In PDS 3D, this unique name is the **AABBCC Code** property. In Smart P&ID, the commodity name corresponds to the **Short Value** entry of the **Piping Component Type** select list for the symbol defined in Data Dictionary Manager and it is this value of the commodity name that is used for the look-up. For a delivered symbol, the **Short Value** entry is equivalent to the symbol’s **AABBCC Code**, defined in Catalog Manager.

Similarly, the **Option Code** property is a select list of text values in Smart P&ID, while it is a set of code numbers or indices in Smart 3D. **Short Value** for the **Option Code** select list contains the Smart 3D indices corresponding to the appropriate **Option Code** text in Smart P&ID. The Piping Specification Utility uses the entries in the **Short Value** box of the **Option Code** list to obtain the Option Code used in the Smart 3D database tables.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 28/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Update Zero Length Pipe Run Connectors Utility**

This utility updates the property sp_connectorszerolength, which was added to the t_piperun table in Version 2007. This property is used to indicate a zero length pipe run when placing adjacent inline items such as a reducer and a valve. If you upgraded from an earlier version and have already run the Smart P&ID Upgrade Utility, this property is updated automatically and you should not need to perform any further action. However, if you did not perform the upgrade, or if you encounter problems with filtering or publishing zero length pipe runs, you can update the property independently by performing the procedure below. This utility finds all zero length pipe runs and assigns a value of **True** to this property for those pipe runs. After running the utility, you can filter out zero length pipe runs for viewing in the EDE and reports, and you can also exclude them from published data.

Do the following to update the sp_connectorszerolength property.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.
3. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **UpdtPiperunConnZeroLen.dll**.

## **Find Invalid Break Labels Utility**

The Find Invalid Break Labels Utility (FindInvalidBreakLabelsCmd.dll) identifies illegal break labels in a plant that has been upgraded from a version of Smart P&ID earlier than 2014. The utility identifies all break labels that have been placed at a location where there is no break in the pipe run. Two options are available: the utility can be run on the current drawing or on all drawings in the plant. When run on the current drawing, the utility band aids all invalid break labels in the drawing and generates a log with the number of items that were band-aided in the drawing. When run for the entire plant, the utility generates a log with a list of the drawings in which invalid break labels were found and the number of invalid break labels in each drawing (drawings that do not have any invalid break labels are not listed).

The log file is named InvalidBreaklLabels.log and is created in the default Temp folder. If the log file already exists, it is appended with any new information.

After running the utility on an individual drawing, you can repair invalid break labels by creating property breaks in the pipe runs where labels are located or you can delete the labels if not needed.

Fixing an invalid break label by creating a property break does not remove the band-aiding. To fix the band-aiding for an invalid break label, break the pipe run, delete the bad label, and place a new break label on the pipe run break. Alternatively, if the break is redundant, just delete the bad label.

1. Open a drawing in Smart P&ID.
2. Select **Tools** > **Custom Commands**.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 29/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. In the **Custom Commands** dialog, browse to the [Product Folder]\P&ID Workstation\bin folder, and then double-click **FindInvalidBreakLabelsCmd.dll**.
2. On the **Find Invalid Break Labels** dialog, select **Current drawing** to band aid invalid break labels in the current drawing and generates a log. To search all drawings in the plant, including the current drawing and generate a log of all drawings with invalid break labels, select **Entire** **plant**. With this option, any invalid break labels that exist in the current drawing are *not*  band-aided.

If any assemblies with break labels were created prior to upgrade, we recommend checking these assemblies for invalid break labels. To do this, create a new drawing, place the desired assemblies in the drawing, and then run the FindInvalidBreakLabelsCmd command on the current drawing. After upgrade it is also recommended to run this command on a drawing before creating any new assemblies from that drawing that include break labels.

During the search operation, it is not possible to perform any other activities in Smart P&ID. On completion of the search, a message displays indicating that the search is complete and allows you to view the log file if desired.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 30/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Log Files**

Log files provide insights into the system’s behavior and performance. They help diagnose and troubleshoot errors and system failures by providing detailed information about what caused an issue.

Smart P&ID provides info and debug logs on the status of the following drawing workflows. If you need

detailed information for debugging or troubleshooting, you can enable the enhanced logs and also

increase the log level.

**What drawing workflows are recorded in the enhanced logs?**

**Log Level**

## **Workflows**

### Info

Activate, open, save, fetch, check in, check

out, delete, and close a drawing.

Compare and refresh a drawing.

Fetch a drawing version.

Fetch a deleted drawing.

Place an assembly in a drawing.

Recreate and update a drawing.

Refresh template.

Scheduled drawing update.

Undo operation.

Debug

In addition to the Info level log information, the

following workflows are included:

Delete a drawing version and revision.

Delete a symbol while updating the drawing.

Delete graphics from a drawing.

Delete stockpile items.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 31/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Delete plan items and labels.

Remove a drawing and version from a project

during the check-in process.

Reserve a license.

Update out of date symbols in a drawing.

The following table lists the most common log files generated by Smart P&ID.

**Name**

**Location**

## **Related Functionality**

AssemblyFileNa %temp%

Assembly creation

me_CreAsm.log

AssemblyFileNa %temp%

Assembly placement

me_PlaAsm.log

Archive.log

Archive file path

Recovery

Retrieve.log

specified in Options

Manager

BuildDB.log

Generated when the Site and Plant databases are

created in Oracle

CheckFilePaths %temp%

Generated by the CheckFilePathsCmd.dll utility

For_PlantName.

log

CheckSymbolsF %temp%

Generated by the CheckSymbolsCmd.dll utility

or_PlantName.l

og

DBCleanup.txt

%temp%

Orphaned records deleted from the plant database using the Delete Orphan Model Item Utility are written to this https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 32/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

file.

GetSmart.log

%temp%

Migrating a SmartSketch drawing into Smart P&ID

InvalidBreakLab %temp%

Find Invalid Break Labels Utility

els.log

PIDAutomation.l %temp%

Using the PIDAutomation type library (PIDAuto.dll)

og

PipeSpecError.l %temp%

Piping Specification Utility

og

Publish.log

%temp%

PlantName is the name of the plant in which the Get

PlantName.log

Latest Version was invoked.

RADApplication. Desktop

Generated when you run Smart Engineering Manager

log

Recreate-

%temp%

Re-creating drawings

DrawingName.lo

g

RepairReport-

%temp%

Relationship Indicator Repair Utility

RelIndicators.lo

g

ServicePids.log %temp%

Service Pids utility

SmartPlantCatal Desktop

Generated when you run Catalog Manager

ogManager.log

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 33/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

SPID-

%localappdata%\SPIDL Overall system log files

[processname]- ogs

[processid]-

[yyyyMMdd].log

SpaBackups.log %temp%

Created when you back up a site and/or plant for the first time. Information from subsequent backups is appended to this file.

SyncSharedItem %temp%

Indicates status of synchronized shared items (off-page s.log

connectors, plant item groups) that cross Workshare site boundaries.

SPDelOrpModIt %temp%

Delete Orphan Model Item Utility

ems.log

ServiceLimits.lo %temp%

Piping Specification Utility

g

SymbolSource.l %temp%

Change Symbol Source

og

UpgradeV4_pla Plant path

Upgrade Utility

nt name.log

V4RefDataUpgr Catalog Explorer root

Upgrade Reference Data (Options Manager)

ade.log

path

V4UpgradePIDs %temp%

Upgrade drawings (Drawing Manager)

.log

Various

Archive file path

Generated during Workshare activities

Workshare-

specified Options

related log files Manager

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 34/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Enable enhanced logs**

When you install a hotfix, the Nlog.config file settings reset to default, so you must reconfigure the settings to enable the enhanced logs.

1. Go to [ *Product installation folder*]\SmartPlant\P&ID Workstation\bin folder and open the NLog.config file.
2. In the code, uncomment the AdvMainLog  element.

To uncomment, remove both the opening <!– and closing –> tags that surround the element.

1. Under rules section, uncomment the ADVMAIN
    
    element.
    

The next time you recreate or update the drawings, you can see more detailed information in the log file.

The application creates a log file per process in a session.

**Increase the log level to Debug**

Enabling Debug log level can affect the performance of the system and lead to increased resource usage and slower response times. Therefore, it is recommended to enable Debug level only when necessary and to disable it after troubleshooting or debugging activities are complete.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 35/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

In the ADVMAIN logger rule, change the minlevel value from “Info” to “Debug”.

**Can I customize the SPID logs filename and path?**

Yes, you can customize both the filename and path of the SPID log files.

For the main logs, in the MainLog  element, change the folder and default values for the fileName attribute.

For the enhanced logs, in the AdvMainLog  element, change the folder and default values for the fileName attribute.

**How do I disable the enhanced logs?**

1. Go to ..\SmartPlant\P&ID Workstation\bin folder and open the **NLog.config** file.
2. In the code, comment the AdvMainLog  element.

To comment, add both the opening <!– and closing –> tags surrounding the element.

1. Similarly, under rules section, comment the ADVMAIN
    
    element.
    

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 36/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to the Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our documentation web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To access the Technical User Forum, go to ALI TUF Link <https://hexagon.com/support-success/asset-

lifecycle-intelligence/tuf> .

## **Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, Intergraph, or its affiliates, parents, subsidiaries retains ownership of the product. You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

**Copyright Notice**

## **Copyright**

Copyright © 1999-2024 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 37/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB and/or its subsidiaries and affiliates.

## **U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below. For civilian agencies: This was developed at private expense and is “restricted computer software”

submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014 and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division 305 Intergraph Way

Madison, AL 35758

## **Documentation**

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

## **Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

## **Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 38/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.

1. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

## **Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE

USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL EVALUATION AS TO THE

USEFULNESS OF THE SOFTWARE IN HIS OWN ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

## **Limitation of Damages**

IN NO EVENT WILL HEXAGON BE LIABLE FOR ANY DIRECT, INDIRECT, CONSEQUENTIAL

INCIDENTAL, SPECIAL, OR PUNITIVE DAMAGES, INCLUDING BUT NOT LIMITED TO, LOSS OF

USE OR PRODUCTION, LOSS OF REVENUE OR PROFIT, LOSS OF DATA, OR CLAIMS OF THIRD

PARTIES, EVEN IF HEXAGON HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

UNDER NO CIRCUMSTANCES SHALL HEXAGON’S LIABILITY EXCEED THE AMOUNT THAT

HEXAGON HAS BEEN PAID BY LICENSEE UNDER THIS AGREEMENT AT THE TIME THE CLAIM

IS MADE. EXCEPT WHERE PROHIBITED BY APPLICABLE LAW, NO CLAIM, REGARDLESS OF

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 39/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

FORM, ARISING OUT OF OR IN CONNECTION WITH THE SUBJECT MATTER OF THIS

DOCUMENT MAY BE BROUGHT BY LICENSEE MORE THAN TWO (2) YEARS AFTER THE EVENT

GIVING RISE TO THE CAUSE OF ACTION HAS OCCURRED.

IF UNDER THE LAW RULED APPLICABLE ANY PART OF THIS SECTION IS INVALID, THEN

HEXAGON LIMITS ITS LIABILITY TO THE MAXIMUM EXTENT ALLOWED BY SAID LAW.

## **Export Controls**

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: a. To Cuba, Iran, North Korea, Syria, or the Crimean, “Donetsk People’s Republic”, “Luhansk People’s Republic,” or Sevastopol regions of Ukraine, or any national of these countries or territories.

1. To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List. Visit www.export.gov for more information or

follow this link for the screening tool: https://legacy.export.gov/csl-search

[https://legacy.export.gov/csl-search](https://legacy.export.gov/csl-search) .

1. To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Hexagon, its subsidiaries, or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.
2. To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.

Any questions regarding export/re-export of relevant Hexagon software product, customized software, Technical Data, and/or third-party software obtained from Hexagon, its subsidiaries, or distributors, should be addressed to Hexagon’s Export Compliance Department, 305 Intergraph Way, Madison, Alabama 35758 USA or at exportcompliance@hexagon.com. Customer shall hold harmless and indemnify Hexagon and a Hexagon Group Company for any causes of action, claims, costs, expenses and/or damages resulting to Hexagon or a Hexagon Group Company from a breach by Customer.

## **Trademarks**

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 40/41

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, SmartPlant Cloud®, PDS®, FrameWorks®, I-Route, I-Export, ISOGEN®, SPOOLGEN, SupportManager®, SupportModeler®, SAPPHIRE®, TANK, PV Elite®, CADWorx®, CADWorx DraftPro®, GTSTRUDL®, CAESAR II® , and HxGN SDx® are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners. Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

## **Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/f2a2f6c7-3185-4467-8030-01590cd8605a 41/41