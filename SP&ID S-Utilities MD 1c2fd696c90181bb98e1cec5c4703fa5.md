# SP&ID S-Utilities MD

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Support Utilities**

## **Hexagon Documentation**

Generated 03/13/2025

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

1/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Table of Contents**

Intergraph Smart® P&ID Support Utilities

Change Linked Document Source Utility

Limitations

Instructions

Error Log

Configure Item Tag Format Utility

Configuration

Limitations

Special Notes

Configuring Item Tag Formats

Configure an item tag’s format

Configure Item Tag Format for Equipment: Example 1

Configure Item Tag Format for Equipment: Example 2

Configure Item Tag Format Setup for PipeRun: Example

Configure Item Tag Dialog

Global Report Utility

Limitations

Instructions

Error Log

Global Symbol Replace Utility

Workflows

Known Problems

Error Log

Global Validation Utility

Instructions

Error Log

Highlight Loop Utility

Prerequisite

Instructions

Error Log

Show Loop Utility

Prerequisite

Instructions

Error Log

Smart Instrument Valve Utility

Limitations

Prerequisites

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

2/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Instructions

Symbol Report Utility

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

3/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart® P&ID Support Utilities**

Intergraph Smart® P&ID Support Utilities package includes the following utilities that are designed for use with Intergraph Smart® P&ID. These utilities facilitate the users perform various tasks with reduced time and effort.

Change Linked Document Source Utility - Globally modifies the source paths for

drawing attachments.

Configure Item Tag Format Utility - Facilitates the customization of Item tags.

Global Report Utility - Generates multiple reports from the set of drawings.

Global Symbol Replace Utility - Batch changes multiple symbols on multiple drawings.

Global Validation Utility - Validates the existing item tag, insulation specification, and 3D

pipe specifications.

Highlight Loop Utility - Identifies the items associated with a selected instrument loop.

Show Loop Utility - Identifies the items associated with a selected item’s instrument

loop.

Smart Instrument Valve Utility - Enables the user to place actuators with instrument

valves.

Symbol Report Utility - Generates a report of the symbols in the reference data.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 2003-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 1/10/2025 at 12:56 PM

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

4/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Change Linked Document Source Utility**

Smart P&ID provides functionality that allows drawings/documents to be attached to the P&ID

files. There are two methods available to accomplish this task. The objects can be embedded or linked depending on the philosophy of each individual customer. Currently, Smart P&ID

embeds the symbols placed in a drawing, and the border graphics in the template file. This allows the drawings to be transported to other sites without regard to the location of the attached file.

Customers intending to use Workshare functionality are advised to embed attachments because the attachments will not be moved with the drawing when published or if ownership is transferred. This utility is not intended for use in a Workshare environment.

When a customer restores a plant to a different location or wants to create a new plant from an existing plant, the source path of drawing attachments will need to be updated. Currently the delivered software requires the customer to open each drawing and modify the source file location of each attachment using the **Edit** > **Link** > **Change Source** command. The Change Linked Document Source utility has been developed to enable the customer to globally update the existing drawing attachment’s source path. The extent of the modification is dependent upon the philosophy used to store the original source attachments. This utility will open each drawing selected, update the attachment’s source path and then close the drawing.

## **Limitations**

This utility is *not* Workshare or Project enabled. It will not verify or detect the plant’s Workshare environment or ownership of drawings, nor it will detect the plant’s Project environment.

The user’s access rights are *not* validated against the roles set via Smart Engineering Manager.

## **Instructions**

1. Set the active plant as desired via Drawing Manager.
2. On the **Start** menu, select **Intergraph Smart P&ID Support Utilities** > **Change Linked** **Document Source** to start the utility.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

5/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The following form displays:

1. Expand the Plant tree in the **Plant hierarchy** pane to display the units.

Selecting a unit displays all the drawings of that unit in the **Drawing** pane. To view all the drawings of the selected plant group in the **Drawing** pane, select **Include** **Subnodes in ListView**.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

6/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Highlight all drawings that are to be processed and select the add (>) button. This adds the drawings to the **Drawing list** pane.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

7/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Drawings from multiple plant groups may be added to the **Drawing list** pane by highlighting the plant group at a level in the hierarchy that includes other desired plant groups in the **Plant hierarchy** pane and selecting the add (>) button.

All drawings from a plant item group (such as unit, area) or plant may be added to the **Drawing list** pane by highlighting the item in the **Plant hierarchy** pane and selecting the add (>) button, or use (>>) button.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

8/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Drawings can be removed from the drawing list by highlighting them in the **Drawing list** pane and selecting the remove (<) button.

1. After adding all the drawings to the **Drawing list**, enter the path to the point that will be replaced in the **Old Replace Path** field. Enter the path that will replace the value **Old** **Replace Path** in the **New Replace Path** field. The **Old Full Path** and **New Full Path** fields are read-only and identify to the user what linked paths will be modified.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

9/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The utility will test all drawings in the select set for their recreate state before the process begins. Drawings that are found in recreate state will not be processed.

They will be logged in the “SPAError.log” file and a message displays after all the processing is completed.

1. Select **Update** to begin processing the drawings. The utility will perform a find and replace on each linked attachment’s source path.

If the **Change Linked object to Embedded** is selected, the utility will break the links for all linked objects whose source files are located inside the old replace path and make these objects as embedded objects in Smart P&ID drawings.

The **Processing status** progress bar will be displayed during processing. When the utility completes processing the selected files, the following message displays: 7. Select **OK.**

1. Select **Cancel** to dismiss the utility form.

**Generate Report** provides an additional function of reporting information of all the linked/embedded objects in selected drawings. The report will be saved as LinkReport.xls file in the *TEMP* directory of your computer.

## **Error Log**

Records the results of the process in the SPAError.log file, located in the *TEMP*  directory. The log file is generated regardless of the process encountering an error.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

10/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Configure Item Tag Format Utility**

Provides an alternate philosophy for configuration of the Item Tag. The philosophy, as delivered in Smart P&ID, requires modification of the code used to generate the ItemTag.dll file for each plant that has unique tagging requirements. The ItemTag.dll file then needs to be managed so that it is installed on all workstations that are used to modify each plant’s data.

This could prove to be a very cumbersome task if a workstation is to be used to modify data on multiple plants.

This utility comprises two components. The first component is the GUI (graphical user interface) required to configure the item tag definition for Equipment, PipeRun, Instrument, InstrLoop, Nozzle, PipingComp, Room, DuctRun and DuctingComp. The item tag definitions can be configured differently for SpecialtyComp or ReliefDevice. The second component is the new ItemTag.dll, that dynamically reads the user-defined Item Tag format and generates the Item Tag based on that format. Implementation of this item tag configuration philosophy makes it possible for users to define and manage different ItemTag formats for different plants with only one ItemTag.dll without any change in the code.

When no configuration is made for the item tag format, the default item tag format is used. See Default Item Tag Configurations.

For the Project/As-Built configuration, two more versions of ItemTag.dll are delivered with the Configure Item Tag Format Utility. They are available in the AgainstAsBuilt and the AgainstAsBuiltAndProjects folders. See *ItemTag.dll Files*.

ItemTagRes.dll is available in the Resource folder.

ItemTagRes.resources.dll is available in the en-US folder.

## **ItemTag.dll Files**

1. Default ItemTag.dll available in the \SupportUtilities\ItemTag\ItemTag folder is used to check the Item Tag uniqueness within the configured active Greenfield Plant or Project only.
2. AgainstAsBuilt ItemTag.dll available in the

\SupportUtilities\ItemTag\AgainstAsBuilt\ItemTag folder is used to check the ItemTag https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

11/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

uniqueness against the As-Built Plant and configured active Project.

1. AgainstAsBuiltAndProjects ItemTag.dll available in the

\SupportUtilities\ItemTag\AgainstAsBuiltAndProjects\ItemTag folder is used to check the ItemTag uniqueness against the As-Built Plant and all Projects of the As-Built plant including the active one.

## **Configuration**

1. Rename the following dll files located in the folder paths mentioned below: ItemTag.dll in “…\Program Files (x86)\SmartPlant\P&ID

Workstation\Bin\Validation” folder.

ItemTagRes.dll in “…\Program Files (x86)\SmartPlant\P&ID

Workstation\Bin\Languages” folder.

ItemTagRes resources.dll in “…\Program Files (x86)\SmartPlant\P&ID

Workstation\Bin\Languages\en-US” folder.

If the above .dll files are to remain in their current folders, the renaming should be done to their extensions. For example, ItemTag.dll is renamed ItemTag.dll_orig. This is essential because the software will not work properly if the renamed files and the files to be copied to the same folder both have the .dll extension.

1. Copy the ItemTag.dll file from the ItemTag folder “…\Program Files (x86)\SmartPlant\P&ID Workstation\SupportUtilities\ItemTag” to the “…\Program Files (x86)\SmartPlant\P&ID Workstation\Bin\Validation” folder.

For the Project/As-Built configuration, extract the ItemTag.dll from the appropriate folder to achieve the desired results.

1. Copy the ItemTagRes.dll from the Resource folder “…\Program Files (x86)\SmartPlant\P&ID Workstation\SupportUtilities\ItemTag\Resource” to the “…

\Program Files (x86)\SmartPlant\P&ID Workstation\Bin\Languages” folder.

1. Copy the ItemTagRes.resources.dll from the en-US folder “…\Program Files (x86)\SmartPlant\P&ID Workstation\SupportUtilities\ItemTag\Resource\en-US” to the “…

\Program Files (x86)\SmartPlant\P&ID Workstation\Bin\Languages\en-US” folder.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

12/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. When the configuration is complete, invoke the utility to configure the Item Tag format for each ItemType, which gets saved in the *ItemTagFormat.xml* file under the plant’s P&ID Reference Data folder.

All client computers will need the new ItemTag.dll, ItemTagRes.dll, and ItemTagRes.resources.dll to use the new tagging configuration.

## **Limitations**

This utility will not verify or detect the plant’s Workshare or Project environment automatically; it is a manual configuration. For the Project/As-Built configuration, the appropriate ItemTag.dll must be used to achieve the desired results.

The user’s access rights are not being validated against the roles set via Smart Engineering Manager.

The TagSequenceNo property must be used as part of Item Tag definition. Because TagSequenceNo is not a delivered property for PipingComp (including SpecialtyComp and ReliefDevice), the user must add this new property for PipingComp only in order to use them.

The user cannot change the **Duplication Option** at this time for most item types. The default **Duplication Option** values are as follows: Equipment - **No duplicated ItemTag allowed** and **Check Child items against all** **Equipment items** enabled.

PipeRun - **Duplicated ItemTag allowed with AutoTagSeqNo**.

Instrument - **Duplicated ItemTag allowed with AutoTagSeqNo** and **No** **duplicated ItemTag allowed** enabled.

InstrLoop - **No duplicated ItemTag allowed**.

Nozzle - **Check Against Items Belonging to Same Parent**.

PipingComp - **Duplicated ItemTag allowed with AutoTagSeqNo**.

SpecialtyComp - **Duplicated ItemTag allowed with AutoTagSeqNo**.

ReliefDevice - **Duplicated ItemTag allowed with AutoTagSeqNo**.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

13/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Room - **No duplicated ItemTag allowed**.

DuctRun - **Duplicated ItemTag allowed with AutoTagSeqNo**.

DuctingComp - **Duplicated ItemTag allowed with AutoTagSeqNo**.

## **Special Notes**

1. A new item tag is created in the product only if the **TagSequenceNo** property is assigned a value.
2. Any attributes from plant groups, including new attributes added by users, are now available to be used for item tags. The attributes will be displayed as  … . For example, Plant…Name, Area … AreaNo, Unit…

UnitCode, and so forth. There is no limit to the levels in the hierarchy that is used.

1. If a user has previously added UnitNo, AreaNo, or Train_Number for a special case, the user should change this field to the new attribute that is available in the form of … as described in Special Note 2. When the user opens the Item Tag Configuration Utility, the user will not see those fields in the utility. Instead, sees a blank field that can be modified to use the new attribute.
2. To bulk update all the existing item tags in the plant with the new format, run the **Global** **Validation** command in Drawing Manager or the Global Validation Utility.
3. After modifying the item tag format, the new format will only apply to newly-created items or to items that have their tag properties edited in the Smart P&ID Test modeler or through Automation (LLAMA) after the format modification.

## **Configuring Item Tag Formats**

The **Item Tag Validation** functionality is saved as *ItemTag.dll* and performs calculations and validations in the current plant for unique tag checking, automatic tag generation, and tag reformatting. **ItemTag Validation** can generate unique **Item Tag** values and maintains consistency between the **Item Tag** value and the properties used in its calculation. Validation, in addition to checking for existing item tags, also checks for duplicate item tags according to the scope specified by the particular version of the *ItemTag.dll* file.

Also, for properties included in the item tag, any leading or trailing spaces are removed during validation.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

14/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

You can configure item tag formats without the need to make code changes and recompile the *ItemTag.dll* file. To do so, you must install the Configure Item Tag Utility, which is made up of the following components:

Executable file: *ConfigureItemTagFormat.exe*

*A* n appropriate customized version of the *ItemTag.dll* file After activating the customized *ItemTag.dll* file (for details, see below), you run the executable file and specify the item tag configuration for each required item type. You also have to update values for the **Validation ID** in Data Dictionary Manager of the properties you have chosen to include in the item tag configuration. For details, see step 11 of the topic Configure an item

tag’s format.

Details of the configurations are stored in the *ItemTagFormat.xml* file, which is read by the customized *ItemTag.dll* file. Data in the *ItemTagFormat.xml* file is then used to implement item tag validation. If the item tag for an item type has not been configured using the utility, the custom *ItemTag.dll* uses the default item tag configuration for that item type. For tables showing the default item tag configurations of supported item types for the installed product, see Default Item Tag Configurations.

The *ItemTag.dll* file validates item tag uniqueness for the following item types: equipment (other equipment, exchangers, mechanical equipment, and vessels), equipment components, instrument loops, instruments, pipe runs, duct runs, signal runs with a plant item type pipe run (hydraulic, connect to process, and so forth), rooms, and nozzles. All other item types are disregarded.

In addition to the default *ItemTag.dll* file, versions of the file for use with a Project / AsBuilt configuration are delivered with the utility. For details, see Item Tag Validation.

## **Activate the custom ItemTag.dll file**

1. Unregister the delivered *ItemTag.dll* file: a. Open a command prompt with admin privileges.

To do this, right-click the command prompt icon and on the shortcut menu, click **Run as administrator**.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

15/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. At the command prompt, type the following command with the appropriate path to the file, for example:

regsvr32 /u “c:\Program Files (x86)\SmartPlant\P&ID

Workstation\bin\Itemtag.dll”

1. Rename the delivered *ItemTag.dll* file located in the above folder path.
2. From the ..\Programmer’s Guide\Sample Source Code\Item Tag Validation folder on the Smart P&ID product media, copy the custom *ItemTag.dll* file to this folder path.
3. Register the custom *ItemTag.dll* file:
4. Open a command prompt with admin privileges.
5. At the command prompt, type the following command with the appropriate path to the file, for example:

regsvr32 “c:\Program Files (x86)\SmartPlant\P&ID

Workstation\bin\Itemtag.dll”

After running the *ConfigureItemTagFormat.exe* file for the first time, the *ItemTagFormat.xml* file is created in the location of the plant reference data rules file.

All client machines using the plant must unregister the old *ItemTag.dll* file and register the new *ItemTag.dll* file in order to use the new tagging configuration.

Any user can open and run the utility; that is, the user’s access rights for the Configure Item Tag Utility are not validated against the roles set via Smart Engineering Manager.

If a property included in an item tag’s definition is already associated with a validation program in Data Dictionary Manager, ** **the existing value of that property’s** Validation ID**

must be copied to the Configure Item Tag Utility’s **ProgID** field in order to be triggered, in addition to entering the value **ItemTag.ItemTagFunc** in the **Validation ID** field. For example, the existing Validation ID for the **Nominal Diameter** property of a pipe run is

“ValidateNomDiam.ForeignCalc”.

The utility cannot verify or detect a plant’s Workshare or project environment.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

16/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Configure an item tag’s format**

Before running the Configure Item Tag Format Utility, you must install and register the custom *ItemTag.dll* file for your work environment. For details, see Configuring Item Tag Formats.

1. Launch Drawing Manager and open the plant for which you want to configure item tag formats.
2. Double-click the *ConfigureItemTagFormat.exe* file.
3. In the dialog box that opens, under **Main Option**, do the following: a. From the **Item Type** list, choose the item type to be configured.

The available selections under **Duplication Option** depend on the item type selected. For Smart P&ID item types, the only available option for equipment is **No duplicated Item Tag allowed**, meaning that all equipment item tags must have unique values at the process engineering case level. If an item tag is found to be a duplicate, an error message is displayed to the user to change one or more properties that affect the item tag value. Process pipelines with duplicate values are allowed within the same case.

1. Beside **Field Number**, select a value between **2** and **12** for the number of properties to be used in the configuration.

The height of the dialog box changes to display the number of properties selected.

1. Select the properties to be used in configuring the item tag’s format.

The order of the properties in the list is the order in which they will appear in the item tag.

The **TagSequenceNo** property must *always* be used in the item tag.

1. Choose a separator to be displayed after each property where required. Select a value from the list or type your own value.
2. Choose values for fixed length strings where required. For each fixed length string, specify a padding character (selected from the list or typed) and the required alignment for the property value (**Left** or **Right**).

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

17/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Padding characters are displayed if the value for the property string has fewer characters than the specified fixed length. Padding characters appear to the right of left-aligned fields and to the left of right-aligned fields.

1. For every property that has a validation program associated with it in Data Dictionary Manager, copy that program’s ProgID from the Data Dictionary Manager **Validation ID**

field to the **ProgID** field in the Configure Item Tag Format Utility.

To view the **Validation ID** for a property in Data Dictionary Manager, see steps 12a - 12c below.

1. Click **OK** to save the configuration for the current item type.
2. Repeat steps 3-8 to configure the formats of other item types.
3. When done, click **Exit**.
4. Open Data Dictionary Manager.

You must have user access rights defined by Smart Engineering Manager to be able to complete this next part of the process.

1. Do the following to ensure that whenever the value of any property used in the item tag’s definition is changed, the item tag validation will be triggered for that property: a. Select the item type’s database table, for example: **Equipment**.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

18/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Find a property that appears in the item tag’s format (for example, **TagPrefix**) and double-click to open the **Modify Property** dialog box.
2. Beside **Validation ID**, add the value **ItemTag.ItemTagFunc**.

If a property included in an item tag’s definition is already associated with a validation program in Data Dictionary Manager, ** **the existing value of that property’s** Validation ID** must be copied to the Configure Item Tag Utility’s **ProgID**

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

19/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

field in order to be triggered, in addition to entering the value **ItemTag.ItemTagFunc** in the **Validation ID** field. For example, the existing Validation ID for the **Nominal Diameter** property of a process pipeline is

“ValidateNomDiam.ForeignCalc”.

1. Repeat steps b and c for each property included in the definition of the item type’s item tag.
2. Repeat steps a - d for each item type whose properties are included in the item tag definition.
3. When done, click **File** > **Save** to save your changes.
4. Close Data Dictionary Manager.

A new item tag is created in the product only if the **TagSequenceNo** property is assigned a value.

After modifying the item tag format, the new format will only apply to newly-created items or to items that have their tag properties edited in the Smart P&ID modeler or through Automation (LLAMA) after the format modification.

To bulk update all the existing item tags in the plant with the new format, run the **Global** **Validation** command in Drawing Manager or the GlobalValidationUpdate Utility from the Support Utilities pack.

**Configure Item Tag Format for Equipment: Example 1**

This example applies to Equipment objects with default **Duplication Option** of **No** **duplicated ItemTag allowed**, where **Check Child items against all Equipment items** is not selected.

Child Item Tag uniqueness is verified only against other children belonging to the same equipment parent.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

20/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Place Diaphragm Pump (Parent) with attached Air Motor (Child) and assign a **Tag Seq** **No** of **100** and a **Tag Prefix** of **P** (**Item Tag** = **P-100**) to the pump.
2. Assign a **Tag Seq No** of **100** and a **Tag Prefix** of **P** (**Item Tag** = **P-100**) to the Air Motor.

Duplicate Item Tags are allowed between the parent and one child item.

1. Place another Air Motor and assign a **Tag Seq No** of **100** and a **Tag Prefix** of **P** (**Item** **Tag** = **P-100**). The Item Tag Validation dialog is displayed with a ‘Duplicate Tag Found…’

message. Duplicate Item Tags are not allowed between child items belonging to the same parent.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

21/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Configure Item Tag Format for Equipment: Example 2**

This example applies to Equipment objects with default **Duplication Option** of **No** **duplicated ItemTag allowed**, where **Check Child items against all Equipment items** is selected.

Child Item Tag uniqueness is verified against all equipment items.

1. Place Diaphragm Pump (Parent) with attached Air Motor (Child) and assign a **Tag Seq** **No** of **100** and a **Tag Prefix** of **P** (**Item Tag** = **P-100**) to the pump.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

22/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Assign a **Tag Seq No** of **100** and a **Tag Prefix** of **P** (**Item Tag** = **P-100**) to the Air Motor.

The Item Tag Validation dialog is displayed with a ‘Duplicate Tag Found…’ message.

Duplicate Item Tags are not allowed between the parent and child items.

**Configure Item Tag Format Setup for PipeRun: Example** 1. Set the active plant as desired via Drawing Manager.

1. On the Start menu, select **Intergraph Smart P&ID Support Utilities** > **Configure Item** **Tag Utility** to start the utility.

For information about the fields in this form, see Configure Item Tag Dialog.

1. Select the **Item Type.** For example, **PipeRun.**
2. Set the **Field Number** to reflect the number of properties that will be displayed in the item tag (a value between 2 and 12).

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

23/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select properties to be displayed from the lists.

The order of the properties in the list is the order in which they will appear in the item tag.

The **TagSequenceNo** property should *always* be used in the item tag. If you are configuring the item tag for item type **PipingComp**, you must add **TagSequenceNo** as an attribute of this item type in Data Dictionary Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

24/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Enter the separator to be placed between the selected properties. The separator can be selected from the list or entered manually.
2. Enter a **Fixed length string** value for desired properties.
3. Enter the **Padding character** to be used for the **Fixed length string** fields. If the value for the string is less than the fixed length, this padding character will be used in each space to the left or right of the entered values for the desired property, depending on the alignment specified in next step.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

25/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Choose **Alignment** for the **Fixed length string** field.
2. If you have selected a property that already has a validation program associated with it in Data Dictionary Manager, copy that ProgID from the Data Dictionary Manager field to the **ProgID** field in the Configure Item Tag Format Utility. (In the example below, **NominalDiameter** is being used in the Item Tag for pipe runs. This field has a ProgID of **ValidateNomDiam.ForeignCalc** in Data Dictionary Manager. It has been copied to the utility’s **ProgID** field. The Item Tag function calls this **ValidateNomDiam.ForeignCalc** when it runs.)

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

26/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **OK** to save the format of the active Item Type.

*The following confirmation displays. Select **OK** to continue.*

1. Repeat steps 3 - 11 to configure each Item Type’s Item Tag.
2. Select **Exit** to dismiss the utility form.
3. Open Data Dictionary Manager (user must have access rights defined by Smart Engineering Manager) to complete the remaining steps of the process.
4. Under **Database Tables**, select the Item Type **Pipe Run**.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

27/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Right-click the **NominalDiameter** property and select the properties.

***Modify Property** window displays.*

1. Add the ProgID **ItemTag.ItemTagFunc** value to the **Validation ID** property.

If a property included in an item tag’s definition is already associated with a validation program in Data Dictionary Manager, ** **the existing value of that property’s** Validation ID** must be copied to the Configure Item Tag Utility’s **ProgID** field in order to be triggered, in addition to entering the value **ItemTag.ItemTagFunc** in the **Validation** **ID** field. For example, the existing Validation ID for the **Nominal Diameter** property of a pipe run is **ValidateNomDiam.ForeignCalc**.

1. Select **OK** to dismiss the **Modify Property** window.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

28/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Repeat steps 16, 17, and 18 for each property included in the definition of the Pipe Run’s item tag.
2. Repeat steps 15, 16, 17, and 18 for each set of Item Type properties.
3. Select **Save** and exit Data Dictionary Manager.

## **Configure Item Tag Dialog**

Allows you to specify the item tag configuration of available item types for the active plant.

## **Property**

Select the properties to be used in the item tag definition. The contents of the list depend on the selected **Item Type** value.

## **Separator**

If required, choose a character from the list or enter your own character to be used as a separator following the chosen property.

## **Fixed length string**

If required, choose a value between 2 and 9 for the maximum number of characters allowed for the property in the item tag.

## **Padding character**

For fixed length string fields, select from the list or enter a padding character to be displayed.

If the value for the property string has fewer characters than the specified fixed length, the padding characters display in the spaces to the left or to the right of the string, depending on the **Alignment** value specified for the property.

## **Alignment**

Select the value **Left** or **Right** for fixed length string fields. Padding characters display to the right of left-aligned fields and to the left of right-aligned fields.

## **ProgID**

If a selected property already has a validation program associated with it in Data Dictionary Manager, copy the **Validation ID** value for that property from the Data Dictionary Manager to https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

29/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

this field. For example, if you select **Nominal Diameter** as one of the properties used in the item tag and the **Validation ID** value is **ValidateNomDiam.ForeignCalc** for this property in Data Dictionary Manager, then that value should be copied to the **ProgID** field. The item tag function will then call ValidateNomDiam.ForeignCalc when it runs.

**Main Option**

## **Item Type**

Select the item type whose item tag you want to configure. Available item types depend on the application associated with the plant. The following item types are available for configuration in Smart P&ID:

Duct Run, Ducting Component, Equipment, Instrument, Instrument Loop, Nozzle, Pipe Run, Piping Component, Relief Device, Room, and Specialty Component.

Although defined in the software as piping components, relief devices, and specialty components have separate custom item tag definitions from those of other piping components. The following criteria are used to determine whether a particular piping component is treated as a piping component, a relief device, or a specialty component when configuring the item tag:

## **ReliefDevice**

All Piping Components where PipingCompSubclass = “Relief Device”.

## **SpecialtyComp**

All Piping Components where PipingCompSubclass = “In-Line Specialty Component”. The IsSpecialtyItem = “True” flag is ignored when defining a piping component as a specialty component.

## **PipingComp**

All Piping Components *except* those where PipingCompSubclass = “Relief Device” OR “In-Line Specialty Component”.

## **Field Number**

Specify the number of fields (properties) to be used in the item tag format. The selected value must be a number between 2 and 12.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

30/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Duplication Option**

Specifies how item tag uniqueness is validated by the *ItemTag.dll* file. The available options are as follows (not all these options may be available for some item types): **No duplicated Item Tag allowed**

All item tags must have unique values. If a new item tag is found to be a duplicate, the behavior depends on the item type:

## **Equipment**

The user is prompted to allow assignment of the next available tag sequence number. If the user selects **No** at the prompt, the tag sequence number is *not* incremented and the previous value is retained.

## **Instrument**

The next available tag sequence number is automatically assigned.

Selecting **Check Child items against all Equipment items** verifies child Item Tag uniqueness against all equipment items. When cleared, child Item Tag uniqueness is verified only against other children belonging to the same equipment parent.

**Duplicated Item Tag allowed with Auto TagSeqNo**

If a new item tag is found to be a duplicate, the user is prompted to allow assignment of the next available tag sequence number. If the user selects **No** at the prompt, the tag sequence number is *not* incremented and the duplicate item tag is retained.

**Duplicated Item Tag allowed w/o Auto TagSeqNo**

Not in use.

**Check Against Items Belonging to Same Parent**

Applies to item types such as equipment components placed on a piece of equipment, where uniqueness is validated only with respect to the particular equipment item.

**Duplicated Item Tag allowed without Check**

Not in use.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

31/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **OK**

Saves the changes you make to the item tag definition for the selected item type.

## **Exit**

Closes the **Configure Item Tag Utility** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

32/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Global Report Utility**

This utility enables the user to create multiple reports based on a select set of drawings.

Currently, the delivered software requires the user to open each drawing and generate one report at a time. This workflow can be very cumbersome when the user requires multiple reports from many drawings. The automation provided by this utility minimizes the time required to generate multiple reports on multiple drawings.

## **Limitations**

This utility is not Workshare or Project enabled. This utility will not verify or detect the plant’s Workshare environment or ownership of drawings nor it will detect the plant’s Project environment.

The user’s access rights are not validated against the roles set via Smart Engineering Manager.

## **Instructions**

1. Set the active plant as desired via Drawing Manager.
2. On the Start menu, select **Intergraph Smart P&ID Support Utilities** > **Global Report** **Utility**.

*The following form displays:*

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

33/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Expand the Plant tree in the **Plant hierarchy** pane to display the units. Selecting a unit displays the unit’s drawing list in the **Drawing** pane. Selecting the **Include Subnodes in** **ListView** checkbox lists all the drawings of the selected plant group in the **Drawing** pane.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

34/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Highlight all drawings that are to be processed and select the add (>) button.

*Selected drawings are added to the **Drawing list** pane.*

Drawings from multiple plant groups may be added to the **Drawing list** pane by highlighting the plant group at a level in the hierarchy that includes other desired plant https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

35/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

groups in the **Plant hierarchy** pane and selecting the add (>) button.

1. Select reports to be generated from the **Project Report & My Reports** list.
2. Select the **Include drawing stockpile** checkbox if you want to generate a report including items in the drawing stockpile. Select the **Individual Report per Drawing** https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

36/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

checkbox if you want to generate individual reports for each drawing. You may also select the **Include plant stockpile** checkbox if you want to include plant stockpile items in your report. However, if you include the plant stockpile, the option to generate an individual report per drawing will not be available.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

37/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **OK** to begin report generation.

*The utility confirms the reports to be generated by displaying a report name list in the*

***Selected Reports** form.*

1. Select **OK** to continue.

*The utility generates the reports selected from the list. When the report generation is* *complete, the following message displays:*

1. Select **OK**.

The default location of the reports generated by this utility is *C:\Users\{username}\My* *Reports\Output* folder.

The naming convention used for the reports generated by this utility is * {Report Name}-*

*{Drawing Name}.xls*.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

38/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Error Log**

This utility records the results of the process in the SPAError.log file, which is located the *TEMP*  directory. The log file is generated regardless of whether the process encounters an error.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

39/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Global Symbol Replace Utility**

In Smart P&ID, all symbols and labels are embedded instead of linked, which means if the symbol/label definition is modified, user need to replace the existing symbols/labels to update the changes. Find/Replace tool with delivered software requires user to open each drawing manually, and update only one symbol/label each time. The Global Symbol Replace Utility allows the P&ID user batch process multiple symbols/labels update for one or many drawings in an active project. User can select to update symbol/label with origin symbol file or with different symbol file, such as replace ball valve with gate valve. Utility opens each drawing selected, updates selected symbols/labels, and then closes the drawing.

## **Workflows**

1. On the Start menu, select **Intergraph Smart P&ID Support Utilities** > **Global Symbol** **Replace Utility**.

You can select one or many drawings. Drawings in the **Drawing list** pane will be

processed for symbol replacement. See Global Report Utility.

Any selected drawings in recreate state will not be processed. A message displays after the processing is completed. The skipped drawings information will be logged in the SPAError.log file.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

40/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **Select Symbol** to get a new form. In this case, the user has selected to update three equipment labels with origin symbol files.
2. Select to update ball valve with gate valve. It is required that: The checkbox **Use different symbol file for replacement** is selected.

Only one symbol is selected at a time.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

41/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Now user has symbols/labels selected and ready to update.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

42/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

User can select entire folder to be replaced. In this case all files under **Vessels** directory will be replaced.

The following screen shot shows the result after the entire **Vessels** directory was sent.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

43/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. To save the settings as an INI file, select **Save to file**.

Next time you run the report, you can load the settings from the file directly.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

44/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

In case where no symbol/label is selected, the utility runs in a mode that opens and closes each drawing, which may update drawing for following purposes: (1) data is updated through automation when drawing is closed, which might leave content in label outdated. (2) rule file is modified when drawing is closed. In this case, open and close drawing will make drawing graphic match data in database and latest rule file.

## **Known Problems**

If a problem symbol is updated, the drawing may corrupt and require a recreate.

Selecting a very large number of symbols is more likely to cause the update to fail.

The utility does not check user access and is not Workshare enabled.

You cannot replace the title block label, a pipe run, or a signal run.

## **Error Log**

An error log is maintained in the *TEMP*  directory in the *SPAError.log* file. Even if no runtime error occurs, some information will be written to the log file.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

45/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Global Validation Utility**

This utility enables the user to implement changes to a plant’s item tag configuration, 3D pipe specifications, or insulation specification, as well as changes the plant group association for items on a drawing. During the course of a project, it is common to have changes to the item tag configuration, and modification or additions to the 3D piping specifications and insulation specification. Using this utility, the changes to these items can be made without impacting P&ID production. The user will be able to select a drawing set and run the item tag validation for items such as Equipment, Pipe Runs, Instruments, Instrument Loops, Piping Components, and Signal Runs. It will also allow the user to optionally process items in the drawing stockpile. Pipe Specification and Insulation Specification validation can also be re-validated with this utility. Currently, this type of change would require the user to open each drawing and modify a property included in the item tag to update the Item Tag property. The user would also need to select the **Calculate** button on the Commodity Code property of each item to re-validate the 3D piping specifications. In addition, this utility will allow the user to change the plant group association for items on the selected drawing(s). This is useful if the user has moved drawings from one plant group to another.

## **Instructions**

1. Set the active plant.
2. On the **Start** menu, select **Intergraph Smart P&ID Support Utilities** > **Global** **Validation Utility**.

*The following form displays:*

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

46/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

You can select one or many drawings. Drawings in the **Drawing list** pane will be processed for global validation. See Global Report Utility.

1. After adding the drawings to the **Drawing list** pane, select the checkboxes for the Item Types that you want to update in the **Item Types** section of the form. Also, select the https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

47/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Item Tag Validation** checkbox in the **Validation Programs** section to allow item tag validation of the selected item types to be re-validated.

1. Select the **PipeSpec Validation** checkbox in the **Validation Programs** section to allow Piping Specification validation to be re-validated.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

48/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select the **InsulationSpec Validation** checkbox in the **Validation Programs** section to allow Insulation Specification validation to be re-validated.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

49/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **Enable** if you want to change the plant group association for items on the selected drawing(s).
2. Select the new plant group for association from the list.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

50/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Validation Programs and Item Types can be selected in any combination for processing.

1. Select the desired options in the **Options** section. You can use the **Include drawing** **stockpile** and **Include plant stockpile** options in any combination to process the items as required.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

51/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **OK** to begin re-validating the item tags, pipe specs, insulation specs and/or PlantGroup association.

The frame at the bottom of the **Smart P&ID Global Validation Utility** form is used to display the update status.

After the processing is completed, the following message displays: 10. Select **OK**.

## **Error Log**

This utility records the results of the item tag validation and insulation spec validation in the AutomationError.log file. The piping specification validation information will be recorded in the PipeSpecError.log file. The log files will be generated regardless of whether the process encounters an error and will be located in the *TEMP*  directory.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

52/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Highlight Loop Utility**

This utility allows the user to identify all items in the drawing that are associated to the selected instrument loop. It highlights the items and generates a select set of all items associated with the selected instrument loop.

## **Prerequisite**

You must add a new property to the Instrument Loop table via the Data Dictionary Manager as follows:

1. Set Active Plant.
2. Open the Data Dictionary Manager and select the Instrument Loop table.
3. Add a new property as follows:

The category can be changed to suit the user’s preference.

1. Select **OK**.
2. Select **Save** and exit the Data Dictionary Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

53/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Instructions**

1. Set the active plant as desired via Drawing Manager.
2. Open the desired drawing.
3. Open the Engineering Data Editor and select **Instrument Loop**.
4. Select an instrument loop from the list.
5. In the **Properties** window, select **Calculation**

.

*All instruments associated with this loop are highlighted and placed in a select set that* *can be used for possible modification.*

The following error message displays if more than one instrument loop is selected in the **Properties** window:

The following error message displays if the selected instrument loop is not associated with any items:

The following error message displays if the selected instrument loop is associated with items but none of those items are in the current drawing: https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

54/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Error Log**

This utility records the results of the process in the SPAError.log file, which is located in the *TEMP*  directory. The log file will be generated regardless of whether the process encounters an error.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

55/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Show Loop Utility**

This utility allows to identify all items in the drawing that are associated with the selected item’s instrument loop. It highlights the items and generates a select set of all items associated to the selected item’s instrument loop.

## **Prerequisite**

You must create a toolbar button as follows.

1. Open Smart P&ID.
2. Browse and add ShowLoopButton.dll to a toolbar:

## **Instructions**

1. Set the active plant as desired via Drawing Manager.
2. Open the desired drawing.
3. Select an instrument and then select the **Show Loop** on the toolbar.

*All instruments associated with this instrument’s loop will be highlighted and placed in a* *select set for possible modification.*

The following error message displays if more than one item is selected when the **Show** **Loop** is selected:

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

56/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The following error message displays f the item is not associated with an instrument loop or is not an instrument:

## **Error Log**

This utility records the results of the process in SPAError.log file, which is located in the *TEMP*

directory. The log file is generated regardless of whether the process encounters an error.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

57/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Smart Instrument Valve Utility**

This utility provides a more integrated relationship between the instrument valve and its associated actuator. When an instrument valve is placed the user can specify the type of actuator required. The software will then place the actuator automatically. When the actuator type of an instrument valve needs to be changed, the user can change the value of the instrument valve’s **Actuator Type** property and automatically update the graphics. If the user replaces the actuator (or deletes the actuator and places another one), the **Actuator Type** property of the instrument is updated automatically by the software.

## **Limitations**

1. When an actuator is replaced via the modification of the instrument valve’s **Actuator** **Type** property, the symbol will be replaced (if the appropriate symbol exists). However, there may be items that require clean up:
2. Any instrument signal lines connected to the original actuator will require manual re-attachment.
3. Any labels associated with the actuator will be deleted and require manual replacement.
4. Rotation of the actuator on placement of the instrument valve is governed by the placement method used when placing the individual instrument valve (that is, cursor above line will place the actuator on top of the valve).
5. If an instrument valve and its associated actuator are deleted from the model and processed in the same select set, the user will receive the following warning: Select **OK**, save the drawing and continue.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

58/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Prerequisites**

1. Copy the ActuatorTypeAndSymbolName.ini file to the folder specified in Options Manager > **Settings** > **Catalog Explorer Root Path**. Otherwise, the default symbol file is used.
2. In the Drawing Manager, open a site database and select a plant.
3. Open the Data Dictionary Manager and edit the database tables as mentioned in the steps below:
4. Select the Database Table for Inline Component.
5. Right-click **Actuator Type** property and select **Properties**.
6. Add the value **SmartInstrValveProgram.ValidationFunc** to the **Validation ID** field as follows:
7. Select **OK**.
8. Select the Database Item Type for Instrument.
9. In the **Validation Program** field, replace **PlantItemValidation.Validate** with **SmartInstrValveProgram.ValidationFunc** as follows: https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

59/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **OK**.
2. Select **Save** and exit Data Dictionary Manager.

## **Instructions**

1. Open a drawing.
2. Place an instrument valve.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

60/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

*A dialog displays prompting you to select the actuator to be placed on the instrument* *valve.*

1. Select the desired actuator from the list.

The actuator is placed on the instrument and the value of the instrument valve’s **Actuator Type** property is updated to match the actuator selected.

1. Select **OK** to continue placing the actuator.

The utility looks for the actuator symbol file of the selected actuator type based on mapping information in the INI file: *ActuatorTypeAndSymbolName.ini*. One actuator type could be mapped to multiple actuator symbol files.

If an actuator type is selected that does not have a matching symbol, the following error message displays and the instrument valve is placed without an actuator: When an instrument valve’s actuator type needs to be modified, update the value of the instrument valve’s **Actuator Type** property in the property grid.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

61/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The existing actuator symbol will be deleted and a new actuator will be placed according the actuator type that you select.

If an actuator type is selected that does not have matching graphics, the following error displays and the actuator will not be replaced:

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

62/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Symbol Report Utility**

Use the Smart P&ID Symbol Utility to generate Microsoft Excel reports containing a list of symbols available in the Smart P&ID Reference Data. You can generate either a general report or a focused report on a specific symbol category. The utility saves the reports in the

%temp% folder.

## **Prerequisites**

Ensure Smart P&ID is installed.

You must connect to a plant in Drawing Manager for the utility to open.

## **Generate a symbol report**

1. On the Windows **Start** menu, select **Intergraph Smart P&ID Support Utilities** > **Symbol Report Utility**.

*The **Smart PID Active Plant** and **Reference Data Root Path for the Active Plant***

*automatically display the active plant name and corresponding P&ID reference data* *path.*

1. Choose what do you want to do next.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

63/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Choose this option**

**To do this**

## **Select Symbol Folder**

### Specify a different source

path for the symbols.

To generate a focused

report on a specific symbol

type, browse the *Symbols*

folder and select a sub-folder.

For example, to generate a

report on all the available

equipment symbols, browse

and select the *Equipment*

folder.

## **Multiple Sheets**

### Categorize symbols into

separate sheets in the Excel

report. For example,

Assemblies, Equipment, etc.

## **Include Icons**

### Add symbol graphics to the

report.

1. Select **Write Symbols** to generate the report.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

64/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Sample report with multiple sheets and symbol graphics** https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

65/71

3/13/25, 10:45 AM

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

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, or its affiliates, parents, subsidiaries retains ownership of the product. You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

66/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Copyright Notice**

## **Copyright**

Copyright © 2003-2024 Hexagon AB and/or its subsidiaries and affiliates.

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

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

67/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

## **Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

## **Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

68/71

3/13/25, 10:45 AM

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

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

69/71

3/13/25, 10:45 AM

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

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

70/71

3/13/25, 10:45 AM

Hexagon Documentation Site Export

## **Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/6ed8d4fa-0fd3-4d81-80da-2b7652837882

71/71