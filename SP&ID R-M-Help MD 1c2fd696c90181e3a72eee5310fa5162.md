# SP&ID R-M-Help MD

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Rule Manager Help**

**Hexagon Documentation**

Generated 03/13/2025

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

1/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Table of Contents**

Intergraph Smart® P&ID Rule Manager

Using Rules for Consistency Checking

Navigating in Rule Manager

Navigating in Smart P&ID Rule Manager

Open Command (File Menu)

Most Recently Used List Command (File Menu)

Open Database Command (File Menu)

Add Folder Command (Edit Menu)

Rename Command (Edit Menu)

Delete Command (Edit Menu)

Cut Command (Edit Menu)

Copy Command (Edit Menu)

Paste Command (Edit Menu)

Save Command (File Menu)

Save As Command (File Menu)

Exit Command (File Menu)

Printing a Rules Summary Report

Generate Report Command (File Menu)

Creating and Modifying Rules

Understanding Priority and Relationships

New Command (File Menu)

Add Rule Command (Edit Menu)

Rule Options Command (Edit Menu)

Properties Command (Edit Menu)

Approve Al Rules Command (Edit Menu)

Defining Items

Selecting Items

Using Implied Items

Using Filters

Understanding Placement Properties

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

2/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Intergraph Smart® P&ID Rule Manager**

Intergraph Smart® P&ID Rule Manager is the environment used to create, manipulate, and manage sets of rules, or rule bases. These rules define how items within the model act and interact. The default rule base for a plant or site is specified in theSmart P&ID Options Manager.

Rules are used in Smart P&ID for the following reasons:

Placement rules ensure that the correct relationships are created when you place a new item or move an item in a drawing.

Rules govern how properties are copied from one item to another in a relationship, how properties are designated at placement, or when the **Reapply Rules** command is used.

Rules check consistency.

Implied items are defined in rules.

Rules provide the capability to customize how model items behave during placement and manipulation within a drawing. A rule can identify two items and define the placement behavior and the relationship between these items. The items can be catalog items or specified using a filter. When you place or modify an item within the model, the software evaluates that placement using the rules in Smart P&ID Rule Manager.

The software tests applicable rules for the new or modified item against items located within the model. When a rule matches both items, the rule is carried out, and the software performs the associated actions. These actions can include the following: Geometric changes to the two items, such as moving a source item into place with respect to a target item.

Graphical connections between items, such as ownership, fitting, or gluepoint.

Creation of relationships between two items for the purpose of drawing consistency.

When an inconsistency is detected in the model, the software marks the location of the problem with an error or warning symbol. These inconsistencies are based on criteria defined in Smart P&ID Rule Manager, which must be taken into account when correcting the https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

3/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

inconsistencies. It is possible to override some rules while you are in the drawing software by approving inconsistencies.

By setting up typical or standard design rules that define the placement characteristics of items and how items interact with each other, you can quickly and easily place the required equipment, interconnecting piping, instrumentation, and other accessories and confirm that you are satisfying proper design criteria. All rules are applied while you create your drawing, not at some arbitrary later time.

You can generate a **Rules Summary Report** that displays a detailed list of your current rules.

You can view the report in you default Web browser.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 10/24/2024 at 2:44 PM

**Using Rules for Consistency Checking**

The Consistency Tab on the Rule Properties Dialog defines consistency check criteria and

specifies the copying guidelines for property values between items when you create relationships. Each row defines one pair of properties to copy and compare. You can enter as many rows as necessary.

Inconsistency indicators display the results of Consistency Checking. If the items do not satisfy one or more of the consistency criteria, the inconsistency indicator changes to either a warning or an error symbol.

The software copies property values only when you create a relationship. You create relationships when you place an item on another item or connect items in a drawing. You can place items from **Catalog Explorer**, the **Engineering Data Editor**, or by moving a placed item into a new position. The software also compares property values whenever you change any property. This validation process can happen many times during the lifetime of an item.

If you have already specified information on the Consistency Tab before

changing a filter on the Items tab, you lose all the information on the Consistency tab.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

4/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Navigating in Rule Manager**

**Navigating in Smart P&ID Rule Manager**

When you open the Smart P&ID Rule Manager software, the **Rule List** window displays all rule folders stored in your rule base. You can create folders in this window to help organize rules. Organizing rules into folders does not affect rule performance. The rules appear alphabetically in each folder and can be moved between folders using the Cut, Copy, and

Paste commands.

The symbol beside a rule indicates that the rule cannot be loaded.

You must have the appropriate privileges to create, edit, or delete rules. User roles are assigned in Smart Engineering Manager.

**Open Command (File Menu)**

Displays the **Open** dialog, from which you can access an existing rule base. The extension for a rule base file is *.rul*.

**Open an Existing Rule Base**

1. Select **File** > Open** **to display the** Open **dialog.
2. Select the folder that contains the rule base you want to open.
3. Type the name of the rule base or select it from the list of rule bases.

You can open one of the last rule bases that you worked on by selecting it from the list of recent files on the **File** menu.

In the **Open** dialog, you can double-click the rule base name to open it.

If you do not see the rule base you want to open, make sure the drive, directory, and type are correct. You can also change the database in which you are working. Se

Connect to a Database.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

5/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Most Recently Used List Command (File Menu)**

Displays a list of the last four rule bases that you opened and provides a shortcut to return to these rule bases. You can return only to rule bases that are in the database to which you are currently connected.

**Open Database Command (File Menu)**

Displays the Open Plant Structure Dialog allowing you to connect to the site and server that you want to work with by choosing the appropriate SmartPlantV4.ini file. You can also view the plants to which you were recently connected. In order to use this command, your computer must be able to connect to the network where the server is located.

**Open Plant Structure Dialog**

Sets options for connecting to a site and plant structure, and passes user access information to the application. This dialog opens when you select **File** > Open Database Command.

**Available plant structures**

Lists those plant structures found on the network. You can select only one item from this list at a time.

**Application Type**

Allows you to select an application for filtering the available plant structures that are associated with that application. If all the plants in the site are associated with one application only, the value is read-only.

**Open**

Connects you to the selected database. The Open command also checks to make sure you have the correct access privileges for the selected plant structure and passes your access information back to Smart P&ID Rule Manager.

**Site Server**

Opens the **Open Site Server** dialog so you can select a SmartPlantV4.ini file from local and network folders. Plant structures that correspond to the initialization file you choose display in the list of available plant structures.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

6/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Connect to a Database**

1. Select **File** > Open Database to open the Open Plant Structure Dialog. The **Open** **Database** command is also available on the toolbar.
2. Select **Site Server** to open the **Open Site Server** dialog.
3. Select the correct SmartPlantV4.ini file, and select **OK**.
4. Select **Open**.

The **Open** command checks to make sure that you have the correct access

privileges for the selected plant structure and passes your access information back to the software.

**Add Folder Command (Edit Menu)**

Inserts a new folder below the active folder, or as a sibling to the currently selected rule, in the rule list. If you select an open folder, the software creates the new folder inside the selected folder. The software is assigned a default name of **New Folder n**. The letter **n** represents the next unused, sequential number. For example, if the last folder that you added was 15, the next new folder is **New Folder 16**. The default folder name can be renamed.

**Create a Folder**

1. Select the rule or folder in which you want to add a new folder. If you select a rule, the new folder is added as a sibling to the rule.
2. Select **Edit** > Add Folder. The **Add Folder** command is also available on the toolbar

**Rename Command (Edit Menu)**

Allows you to change the name assigned to the active rule or folder. Type a new name into the edit box that appears. You can also select a rule or folder and select **F2** to rename it.

**Rename a Folder**

1. Select the folder you want to rename.
2. Select **Edit** > Rename.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

7/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Type the new folder name over the existing folder name.

**Rename a Rule**

1. Select the rule you want to rename.
2. Select **Edit** > Rename.
3. Type the new rule name over the existing rule name.

**Delete Command (Edit Menu)**

Removes the active rule or folder. If you delete a folder, all child folders and rules are also deleted. Deletions are permanent once you save your changes to the rule base.

**Delete a Folder**

1. Select the folder you want to delete.
2. Select Delete

on the toolbar.

If you delete a folder, all child folders and rules are also deleted.

**Delete a Rule**

1. Select the rule you want to delete.
2. Select Delete

on the toolbar.

1. Select **File** > Save to delete the rule from the database. If you decide you do not want to delete the rule, do not save your changes.

Deletions are permanent once you save your changes to the rule base.

**Cut Command (Edit Menu)**

Removes the selected rule from the **Tree** view, and copies the information to the Clipboard.

**Cut a Rule**

1. Select the rule you want to remove.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

8/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select **Edit** > Cut. The rule is placed in the Clipboard. The selected rule is now available to paste into a rule folder. This rule remains in the Clipboard until you cut or copy another rule or close the application.

**Copy Command (Edit Menu)**

Copies the active rule to the Clipboard.

**Copy a Rule**

1. Select the rule you want to copy.
2. Select **Edit** > Copy. A copy of the rule is placed on the Clipboard. You can now paste the rule to another location or folder.

**Paste Command (Edit Menu)**

Inserts the contents of the Clipboard into the rule list under the active folder. If a rule is currently selected, the software inserts the contents of the Clipboard as a sibling of the selected rule.

**Paste a Rule**

1. Select the location where you want to insert the rule. You can insert a rule into a folder or into a compound rule. If you select a simple rule in step one, the rule on the Clipboard is inserted as a sibling, on the same level as the selected rule.

To paste a rule, you must previously move a copy of a rule to the Clipboard by using either the Cut command or the Copy command.

1. Select **Edit** > Paste. The **Paste** command is also available on the toolbar

**Save Command (File Menu)**

Writes any changes for the rule base that is currently open to the *.rul* file.

**Save a Rule Base**

Select **File** > Save.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

9/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The software automatically prompts you to save the open rule base when you close the program.

**Save As Command (File Menu)**

Displays the **Save As** dialog so you can specify how and where to save the current rule base.

You can rename the rule base, but in order to open it in Smart P&ID Rule Manager, you must preserve the *.rul* extension.

**Save a Rule Base Under a Different Name**

1. Select **File** > Save As to pen the **Save As** dialog.
2. Browse to the location where you want to store the file.
3. Enter the file name and file type.

**Exit Command (File Menu)**

Closes the Smart P&ID Rule Manager application. If you have not saved all your changes to the open rule base, a message provides the option to cancel the **Exit** command.

**Close Smart P&ID Rule Manager**

Select **File** > Exit. If you have not saved all the changes you made to the open rule base, a message box appears with the option to cancel the Exit command.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

10/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Printing a Rules Summary Report**

**Generate Report Command (File Menu)**

Compiles a rules summary report of all rules. The report displays in your web browser. If you need a printed copy, select **Print** in your web browser.

**Print a Rules Summary Report**

1. Select a rule.
2. Select **File** > Generate Report. The **Rules Summary Report** displays in your default web browser.
3. From your browser, select the **Print** command.

You can also use the other functions of your browser to save or e-mail the report.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

11/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Creating and Modifying Rules**

In the course of your design work, you can create new rules to add to an existing rule base, or you can modify the rules delivered with Smart P&ID Rule Manager. You can do something as simple as add a description to a rule or something as complicated as creating an entirely new rule to govern a special relationship between two very specific items in the reference data.

You must have appropriate use access privileges to copy rules, create new rules, and modify rules extensively before you can create an entirely new rule base.

Use Add Rule** **

to create an entirely new rule, or use Properties

to modify an existing

rule.

If you are using a Workshare environment, do not create, modify, or delete rules at a satellite site.

**Understanding Priority and Relationships**

A rule’s priority setting determines the order in which rules are applied. To assign priority to a rule, select **Edit** > Properties and select the General Tab. If several rules apply to the source

and target items, the software selects the rule with the highest priority to control placement.

When you create a relationship, if several rules apply to the source and target items, the software instructs the highest priority rule to copy property values first. Then, each of the other applicable rules copies unpopulated property values in order of priority.

Additionally, you can prevent the software from creating a relationship that a rule describes.

For example, you can create an exception to a rule by specifying filters for **Item 1** and **Item 2**

on the Items Tab. Selecting the **Prohibit** check box on the General Tab prohibits a relationship between the two items that you defined. The **Prohibit** check box works for freestanding placement as well as placement on a target.

A nozzle cannot be set in a rule as the owner of another nozzle. Doing this causes a constraint violation and results in orphaned nozzle objects in the database.

**New Command (File Menu)**

Creates a new rule base. The new rule base folder appears in the **Rule** list. The file extension for a rule base is *.rul*.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

12/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Create a New Rule Base**

1. Select **File** > New.
2. Select the newly displayed folder name in order to rename it.
3. Create folders for your rules and add rules to the folders. See Create a Folder or Create

a Rule.

1. Select **File** > Save As to save your new rule base under its own name in the proper place in your directories.

**Add Rule Command (Edit Menu)**

Inserts a new rule below the active folder or as a sibling to the currently selected rule. If you select an open folder, the software creates the new rule in that folder.

Each rule must have a unique name because the software assigns a default name of **New** **Rule n** to each new rule. The letter **n** represents the next unused, sequential number. For example, if the last rule you added was 15, the next assignment is **New Rule 16**.

**Create a Rule**

1. Select the folder or rule in which you want to store your new rule. If you select a rule, the new rule appears as a sibling to the selected rule.
2. Select Add Rule

. The **Add Rule** command is also available from the **Edit** menu or from the shortcut menu accessed by right-clicking on a rule.

1. Enter a name and a description for the rule. The **Description** box can contain links to an Internet address so that a detailed description can be stored on a website and accessed using this option.
2. In the **Priority** box, enter a priority value.
3. On the Items Tab, select an item for **Item 1**.
4. Select a connect point type and a placement method for **Item 1**, if applicable.
5. Select an item for **Item 2** or leave **Item 2** freestanding, depending on the type of rule you are creating.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

13/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Define a connect point type and a placement method for **Item 2**, if applicable.
2. Set the **Comparison**, **Status**, **Severity**, and **Copy** options on the Consistency Tab.
3. On the Implied Items Tab, use the options to specify implied items, if applicable.
4. Select **OK**.
5. Select Save

on the toolbar to write the changes to the rule base.

**Example: Create a Rule to Copy Values From Piping to a Globe** **Valve**

1. Select **Edit >** Add Folder. Rename the folder if needed. See Rename a Folder.
2. Select the new folder, and then select **Edit >** Add Rule to open the** **Rule Properties

Dialog.

1. Enter a name and a description for the new rule. You can create an Internet link by typing a URL address in the **Description** box. This action allows for storage of additional information on a website.
2. In the **Priority** box, select a priority value, you can define a value from 1 to 100. One is the lowest priority, 100 the highest.
3. On the Items Tab, define **Item 1** by selecting the **Browse** button next to **Item 1**.
4. On the **Select Item 1** dialog, select **Catalog item**. In the **Item selection Tree** view, select a gate valve and select **OK**.
5. Set the connect point type for **Item 1** (Piping Point).
6. Set the placement method (Snap-on).
7. Select **Properties** next to **Placement method** for **Item 1**.
8. On the Snap-On Placement Properties Dialog, specify the gap distance and select **OK**.
9. Define **Item 2** by selecting the **Browse** button next to **Item 2**.
10. On the **Select Item 2** dialog, select **Catalog item**. In the **Item selection** **Tree** view, select **Nozzles** and then select **OK**.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

14/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Set the connect point type for **Item 2** (Piping Point). For this example, you do not need to define a placement method for **Item 2**.
2. On the Consistency Tab, set **Compare** to “=”.
3. Set **Status** option to **Warning**.
4. Set **Severity** level to **1**.
5. Set **Copy** to “<==” and select **OK**. Values are copied only if the destination values are **Null**.
6. Select **File >** Save to write the changes to the rule base.

**Example: Create a Rule to Copy Values From a Valve Upon**

**Placement**

1. Select **Edit** > Add Folder.
2. Select the new folder, and then select **Edit** > Add Rule** **to open the Rule Properties

Dialog.

1. Enter a name and a description for the new rule.
2. In the **Priority** box, select a priority value. You can define a value from 1 to 100. One is the lowest priority, 100 the highest.
3. On the Items Tab, define **Item 1** by selecting the **Browse** button next to **Item 1**.
4. On the **Select Item 1** dialog, select **Catalog Item**.
5. In the **Item selection** **Tree** view, select a gate valve, and then select **OK**.
6. Set the connect point type for **Item 1** (Piping Point).
7. Set the placement method (Snap-on).
8. Select **Properties** next to **Placement method** for **Item 1**.
9. On the Snap-On Placement Properties Dialog, set the gap distance, and select **OK**.
10. Define **Item 2** by selecting the **Browse** button next to **Item 2**.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

15/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. On the **Select Item 2** dialog, select **Catalog item**.
2. In the **Item selection** **Tree** view, select **Nozzles** and then select **OK**.
3. Set the connect point type for **Item 2** (Piping Point). For this example, you do not need to define a placement method for **Item 2**.
4. On the Consistency Tab, set **Compare** to “=”.
5. Set **Status** option to **Warning**.
6. Set **Severity** level to **1**.
7. Set **Copy** to “==>” and select **OK**. Values are copied only if the destination values are **Null**.
8. Select **File** > Save to write the changes to the rule base.

**Rule Options Command (Edit Menu)**

Opens the Rule Options Dialog, which allows you to define status and severity values for

inconsistencies in drawings. The software verifies in real-time if the composition of a drawing and the underlying data model satisfy rules defined in Rule Manager. Smart P&ID then alerts you if an inconsistency arises.

**Define Rule Options**

1. Select **Edit** > Rule Options.
2. Select the values from the **Status** and **Severity** lists to define the needed inconsistency type.

**Rule Options Dialog**

The **Rule Options** dialog shows the inconsistency error types. You can select from any one of the cells and change the value by selecting from the displayed list.

**Inconsistencies**

**Inconsistency Type**

There are six inconsistency types on the **Rule Options** dialog: https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

16/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Inconsistent property value**

When you add a new consistency criterion to a rule, the software uses the **Status** and **Severity** values you enter as defaults in the Consistency Tab (Rule Properties Dialog). You can then modify these default values as needed.

**Inconsistent flow direction**

Specifies the default **Status** and **Severity** where the software finds an inconsistency in the flow direction of the P&ID drawing. When you add the consistency criterion **Flow Direction** to a rule, the software uses these **Status** and **Severity** values as the defaults in the Consistency

Tab (Rule Properties Dialog). You can then modify these default values as needed.

**Unattached connect point**

Specifies the status and severity where the software finds an unconnected piping connect point on a piping component, instrument, or nozzle.

**Unattached connector**

Specifies the status and severity where the software finds an unconnected end of a pipe run, signal run, or duct run.

**No applicable rules**

Specifies the status and severity where the software finds two connected items for which there are no rules that allow the connection. This can happen, for example, when you work with two different plants that have two different sets of rules. When drawing data is copied from plant A to plant B, using **Assemblies** or **Import Drawings**, items that were legally connected in drawing A might not be legally connected in plant B. Also, such an inconsistency might be generated if you edit a plant rule after drawings have been created based on that rule. If the drawings contain connected items and the rules that supported those connections are deleted, the result is connections that have no applicable rules.

**Cannot evaluate consistency**

When a pipe run, signal run, or duct run is attached to an Off-Page Connector (OPC) but no corresponding run is attached to the mate OPC, the consistency cannot be evaluated. This can happen when working in a project environment. Two drawings that contain an OPC and its mate might be complete in the As-Built plant. If only one of the drawings is fetched into the https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

17/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

project, the consistency of the OPC connection cannot be evaluated because the other drawing does not exist in the project.

**Status**

This column has the following possible values:

**Warning**

The status is used to alert you of possible inconsistencies in your drawing. These inconsistencies are of a non-critical nature. When you select this option, a **Warning** symbol displays on the appropriate drawing object. You can double-click the symbol to open the **Consistency Check** dialog. On the **Consistency Check** dialog, you have the option to approve the inconsistency, and therefore leave it in your drawing, or you can correct the drawing and remove the inconsistency.

**Error**

This status is used to alert you of critical inconsistencies within your drawing. These errors must be fixed within the drawing for the inconsistency to be removed. When you select this option, an **Error** symbol

displays on the appropriate drawing object. You can double-click the symbol to open the **Consistency Check** dialog for a more detailed view of the inconsistency.

**Severity**

This column can have numeric values from 1 to 10, with 10 being the highest severity. The software can be configured to show only those inconsistencies above a specific value. See the **View Properties** dialog.

**Properties Command (Edit Menu)**

Displays the Rule Properties Dialog so you can define all of the properties for the selected rule. The different tabs that make up this dialog provide for general information, placement details, consistency checking, and defining implied items. The Rule Properties Dialog displays

automatically when you add a new rule.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

18/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Rule Properties Dialog**

Displays information about the active rule. This dialog opens when you select a rule and select **Edit** > Properties on the menu bar or when you create a new rule.

**General Tab (Rule Properties Dialog)**

Contains general information that controls the way you perform rule checking.

**Name**

Defines the name of the rule. If the name is blank, the software creates a new rule named **New Rule n**, where **n** is the next available number since the last new rule that you created. If you change the name of a rule, select **OK** and the new name appears in the **Rule** list.

**Description**

Identifies the purpose or function of your rule. Rule names must be unique. In addition, you can create an Internet link by entering a URL address, which provides another way to include detailed information about a rule.

**Priority**

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

19/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Determines which rule applies when rules conflict with each other. You can define a value from 1 to 100: 1 is the lowest priority. When you place items in a drawing, if several rules apply to the source and target items, the software selects the rule with the highest priority to control placement. When you create a relationship, if several rules apply to the source and target items, the highest priority rule copies property values first, and then each of the other applicable rules copies unpopulated property values in order. Assigning a priority is required.

**Prohibit**

Specifies whether to prohibit the relationship between the two items defined on the **Items** tab.

When you check the **Prohibit** box, the relationship this rule describes cannot be created. If you need to, you can create an exception to a broad rule by specifying more specific filters or by using catalog items for **Item 1** and **Item 2** and checking **Prohibit**. This option works for freestanding placement as well as placement on a target.

**Items Tab (Rule Properties Dialog)**

Defines items to which a rule applies, including connect point and placement information.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

20/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Item 1**

Displays the following options for the first item involved in this rule.

**Name (Item 1)**

Displays a filter or catalog item. For a new rule, the field initially appears as  ****. To choose an item name, select **Browse** and display the Select Item Dialog. **Name** is a required field.

**Connect point type (Item 1)**

Displays valid connect point types. This property defines the type of connect point to use when you connect one item with another. If the placement method is inline, only the connect point type for the item you are placing is valid. The **Label** and **Geometric** placement methods do not use connect point information.

**Placement method (Item 1)**

Defines the placement method to apply when placing an item to a target object.

**Browse (Item 1)**

Opens the Select Item Dialog. You can select a new item that is either defined by a filter or catalog item. You must specify this property for **Item 1**.

**Properties (Item 1)**

Displays the appropriate properties for your selected placement method. If a placement method does not have properties to specify, the **Properties** button is not available.

**Item 2**

Displays the following options for the second item involved in this rule. There can be no second item, in other words, this item can be defined as freestanding.

**Name (Item 2)**

Appears either as a filter, catalog item, or freestanding. To select an item name, select **Browse** to display the Select Item Dialog.

**Connect point type (Item 2)**

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

21/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Displays valid connect point types. This property defines the type of connect point to use when you connect one item with another. If the placement method is inline, only the connect point type for the item you are placing is valid. The **Label** and **Geometric** placement methods do not use connect point information, and this option is not available if you have not defined a second item.

**Placement method (Item 2**)

Defines the placement method to apply when placing an item to target object.

Rules can be bi-directional. If a placement method exists for both **Item 1** and **Item 2**, then both rules are invoked when establishing such a relationship in the drawing.

**Browse (Item 2)**

Opens the Select Item Dialog, allowing you to select a new item that is either a filter, catalog item, or freestanding. Item selection is not required for **Item 2**.

**Properties (Item 2)**

Displays the appropriate properties for your selected placement method. If a placement method does not have properties to specify or you did not define a second item, the **Properties** button is not available.

**Consistency Tab (Rule Properties Dialog)**

Defines the consistency criteria for a rule.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

22/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Consistency Criteria**

Lists the values for applying consistency criteria when items are placed in a drawing.

**(Property of Item 1)**

The header displays the Item 1 **Name** value as shown on the Items Tab. Each data row in the

column displays the name of the Item 1 property to be used for consistency checking and **System Editing**.

**Copy**

The copy action to be performed is displayed in this column. This column controls how the property value is propagated when **System Editing** is turned on. The following table describes the possible values and their meanings.

**Copy Action Symbol**

**Copy Action Name**

**Property Modification**

**< >**

Copy Bi-directional Always The value can be copied in

either direction during

propagation.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

23/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**<**

Copy Item2 to Item1

The value from Item 2 is copied

Always

to Item 1 during propagation.

**>**

Copy Item1 to Item2

The value from Item 1 is copied

Always

to Item 2 during propagation.

**< >**

Copy Bi-directional if Null

The value can be copied in

either direction during

propagation but only if the

current value on the target item

is Null.

**<**

Copy Item2 to Item1 if Null The value from Item 2 is copied

to Item 1 during propagation but

only if the current value on Item

1 is Null.

**>**

Copy Item1 to Item2 if Null The value from Item 1 is copied

to Item 2 during propagation but

only if the current value on Item

2 is Null.

**|**

None

The property is not propagated

across this relationship.

Property break

At the property break, the

property values of the

connected objects are not

copied or propagated. See

Consistency Checking and

System Editing.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

24/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Compare**

Displays how the property values from Items 1 and 2 are compared. The comparison occurs whenever any property on either item is changed. The following table describes the possible values and their meanings

**Comparison Operator**

**Meaning**

**|**

No comparison

**=**

Equal

**<**

Less than

**<=**

Less than or equal to

**>**

Greater than

**>=**

Greater than or equal to

**<>**

Not equal to

Property break

When applied to the **Process Pipe Run To Process Pipe Run** rule, the **Copy** and **Compare** operators determine the behavior of pipe runs joined by a collinear connection.

**(Property of Item 2)**

The header displays the Item 2 **Name** value as shown on the **Items** tab. Each data row in the column displays the name of the Item 2 property to be used for consistency checking and **System Editing**.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

25/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Status**

Defines the display status of the inconsistency marker when an inconsistency is generated. If this value is set to **Error**, the inconsistency marker appears as a red **X** in your drawing. If it is set to **Warning**, the marker displays a blue exclamation point. This list appears after you select the field.

**Severity**

Displays a list for you to specify the severity of the inconsistency. Severity displays as a number between 1 and 10.

The following columns display when both **Item 1** and **Item 2** are used. For example, **Nominal** **Diameter** is frequently different in a branch as compared to the main run it connects to.

Therefore you might want to set the value for **Non-colinear** to **None** for the **Nominal** **Diameter** property.

**Colinear Copy**

Defines the copy action to be used at a colinear connection. The values available for selection for this column are the same as those in the **Copy** column.

To specify the copy action at a colinear connection, you must set the value in the **Copy** column to be the same as the value for this column.

**Colinear Compare**

Defines the comparison operator to be used at a colinear connection. The values available for selection for this column are the same as those in the **Compare** column.

To specify the comparison action at a colinear connection, you must set the value in the **Compare** column to be the same as the value for this column.

**Non-colinear Copy**

Defines the copy action to be performed at a non-colinear connection. The values available for selection for this column are the same as those in the **Copy** column.

**Non-colinear Compare**

Defines the comparison operator to be used at a non-colinear connection. The values available for selection for this column are the same as those in the **Compare** column.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

26/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The following commands can be used to add and delete rows in the **Consistency Criteria** table.

**Add**

Adds a new row to the bottom of the list of consistency criteria. You must select the name of the Item 1 property from the drop-down list in the first column. Default values for the remaining columns are automatically displayed.

**Add All**

Fills in the table with default values for all matching properties of **Item 1** and **Item 2**. For each matching pair, the **Compare** field is set to “=” by default, and the **Copy** field is set to “|”

(None).

**Delete**

Removes the selected rows. It is enabled when one or more rows in the consistency criteria list are selected.

If no consistency criteria are defined for a particular property of an item, that property is not copied or included for comparison.

When joining pipe runs, **Copy** criteria are ignored for properties on pipe runs unless the value of the property is the same on both pipe runs prior to joining or if the property has a null value on the pipe run that is the target for the criterion.

For relationship rules where the Item 1 and item 2 are of the same item type, to determine which item is which, select one of the items in the drawing, right-click and on the shortcut menu, select **Consistency Check**. In the dialog that opens, select the **Highlight item 1** and **Highlight item 2** check boxes to highlight each item in the drawing.

To see the results of a changed **Copy** or **Compare** action after saving the rule, you must close and reopen the drawing.

When defining consistency criteria in a rule, and the property you select is a connect point (**Piping Point**, **Ducting Point** or **Signal Point**) property, you are not defining a specific connect point. The specific connect point is defined dynamically by the software https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

27/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

when the rule is applied to a specific relationship. Although the displayed property name in the **Rule Properties** dialog might display **End 1 Nom Diam**, it actually means the **Nominal Diameter** property on that connect point in this relationship.

It is possible that no matching properties can be found for the two items. If no match is found, defining consistency criteria for the two items is not possible.

You can highlight one or several rows by selecting the row tab at the far left side. A row marker is shown to indicate the current row. After a row or several rows are selected, you can delete the rows by pressing **Delete** or change the **Compare**, **Status**, **Severity**, and **Copy** values for selected rows by selecting on the appropriate heading and choosing from the list.

**Implied Items Tab (Rule Properties Dialog)**

Defines implied items for a rule.

**Owned by**

Defines the items that own the implied items you are defining.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

28/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Item 1**

Defines ownership of the implied item you are identifying.

**Item 2**

Defines ownership of the implied item you are identifying. If you have not defined a value for a second item, or defined it as freestanding, this option is not available.

**Implied items**

Displays a list of the implied items to claim. A thumbnail icon appears beside the symbol name.

**Add**

Displays the Add Implied Item Dialog allowing you to select a catalog item, and it appears in

the **Implied items** list.

**Delete**

Removes the selected implied item from the list.

**Select Item Dialog**

The **Select Item** dialog displays information about the **Item type** and **Item selection**.

Different options are available, depending on your selection of **Filter**, **Catalog item**, or **Freestanding**. This dialog displays when you select one of the **Browse** buttons on the Items

Tab (Rule Properties Dialog).

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

29/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Item type**

**Filter**

Defines the item as a filter.

**Catalog item**

Specifies that the item is a catalog item.

**Freestanding**

Defines the item as freestanding. This option is available only for **Item 2**.

**Item selection**

Displays three possible views:

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

30/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Filter Control** when the **Item type** is **Filter**.

**Catalog Explorer** when the **Item type** is **Catalog item**.

Blank when the **Item type** is **Freestanding**. This option is available only for **Item 2**.

**New**

Opens the **New Filter** dialog where you can create a new filter to define an item type. This button is available only when the **Item type** is **Filter**.

**Properties**

Opens the Filter Properties Dialog so you can view and edit properties for a selected filter.

This button is available only when the **Item type** is **Filter**.

**Add Implied Item Dialog**

Displays when you select **Add** on the Implied Items Tab (Rule Properties Dialog)) Use this

dialog to select your implied items. The dialog display is similar to **Catalog Explorer**: **Tree view**

Displays a tree view of catalog items.

**List view**

Displays a list view of implied items with their symbols.

**Display Rule Properties**

1. Select the individual rule for which you want to view the properties.
2. Select Properties

on the toolbar. The Properties command is also available from the

**Edit** menu or from the shortcut menu accessed by right-clicking on a rule.

1. On the Rule Properties Dialog, navigate to the information you need.

**Modify a Rule**

1. Select a rule to modify.
2. Select Properties

to display the Rule Properties Dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

31/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Make your modifications.
2. When finished, select **OK**.

**Approve All Rules Command (Edit Menu)**

Automatically approves all of the rules that are in a disabled state because of modifications to the filters on which they depend.

If you get a message stating **One or more rules did not load properly** when you open Rule Manager, this indicates that a filter used by a rule has been edited or deleted in Filter Manager. If this message box displays select **OK** to open Rule Manager. Then, expand the **Tree** views. Any rules that do not load properly display the **Disabled** icon.

If you are sure all the changes to the filters are acceptable, you can use the **Approve All** **Rules**. You can also review and approve each individual disabled rule using the Rule

Properties Dialog.

**Approve All Rules**

1. Select a folder in the **Tree** view.
2. Select **Edit** > Approve All Rules.
3. Select **Yes** to automatically approve all rules.
4. Select **File** > Save

to save the rule file changes.

If you want to review and approve each rule marked as disabled individually, select **No** to use the Rule Properties Dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

32/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Defining Items**

**Selecting Items**

The Items Tab on the Rule Properties Dialog allows you to define information about the items

to which a rule applies. You define **Item 1** and **Item 2** by selecting a filter or a catalog item for each. A filter allows you to specify an extensive class of items to which the rule applies. A catalog item allows you to specify a single, specific catalog item or symbol. For example, if you want a rule to apply between nozzles and vessels, define **Item 1** by using a filter for nozzles and **Item 2** by using a filter for vessels.

For each item, you can specify a connect point type. Some of the placement methods use connect points to calculate the placement geometry. For methods that use connect points, you must specify an appropriate **Connect point type**.

A rule can apply to a pair of items or a single item. For rules that apply to a single item, you must use **Item 1** to define the item and set **Item 2** to **Freestanding**. The software needs rules that apply to a single item to support placement of items in free space without relationships to other items. For example, if you want to place a vessel in free space, define **Item 1** by using a filter for vessels and **Item 2** as **Freestanding**.

For each item, you can specify a placement method that defines how to place the item relative to the other item. **Placement method** controls orientation of the geometry and relationships that the software creates when you place the item. For example, if you want to place nozzles on vessels, you can define a placement method for **Item 1**, the nozzle.

**Using Implied Items**

An implied item is an item in the database with no graphical representation in the drawing file.

You can establish implied items by the existence of a single item, or by the existence of a relationship between two items.

A common example of a symbol with implied items is a vent drain detail. In the drawing, the vent drain detail is represented graphically by only one symbol. However, when the symbol is placed, it represents a 1-inch secondary pipe, a 3/4-inch root valve, and a plug in the database.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

33/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Selecting **Edit** > Properties and selecting the Implied Items Tab on the Rule Properties Dialog

allows you to define the method for specifying implied items. The list shows all implied items for a rule. You can add or delete items by using the **Add** or **Delete** buttons beside the list.

If you associate implied items with a single item on the **Items** tab (**Item 2** is freestanding), then the software creates implied items for each instance of that item in the design. If you associate implied items with a pair of items, then the software creates implied items for each instance of the relationship between those two items.

When you delete an item, the software deletes all of the implied items that the item owns.

Because implied items are not graphical, you cannot see them in a drawing. However, you can display the items in the table view and in reports generated from the database.

**Using Filters**

You can use filters in many ways throughout the software and its standalone applications and utilities.

In Smart P&ID Rule Manager, you use filters to define items in individual rules. Provided you have the correct user access permissions, designated in Smart Engineering Manager, you have all the capabilities for handling filters in Smart P&ID Rule Manager that you have in Filter Manager itself. Therefore, you can create, modify, and reorganize filters. You cannot create a compound filter(s) in Smart P&ID Rule Manager, but you can view the properties of compound filters.

Compound filters cannot be used to define items for individual rules, but you can use the simple filters inside compound filters to define items for rules.

If you are using a Workshare environment, Project Filters should not be created at a satellite site. However, you can always create My Filters in the Filter Manager interface.

**Display Filter Properties**

1. On the Rule Properties Dialog** **>**  **Items Tab, select the** Browse** button beside the item whose filter properties you want to view.
2. On the Select Item Dialog , choose **Filter** in the **Item type** list.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

34/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Select the filter for which you want to view properties.
2. Select **Properties**.

If you have the Select Item Dialog open and are creating or modifying a filter, do not open Filter Manager and make changes to filters in that utility at the same time.

**Filter Properties Dialog**

Specifies properties of a filter, including the name, description, and the other properties for which you want to filter. Each item type owns a set of properties. Examples of item types are **Equipment**, and **Instrument**, and examples of properties for these item types are **Equipment Type**, **InstrLoop Part Number**, and **Estimated Length** respectively.

**Name**

Specifies the filter name. The name can be any combination of characters and any length.

Filter names within a plant must be unique. This name displays as the filter name in the Filter Manager interface.

**Set as asking filter**

Defines the filter as an asking filter.

**Description**

Specifies a phrase or sentence about the filter. The description can be any combination of characters and any length. The description appears as a ToolTip when you point to the filter name in the Filter Manager interface.

**Filter for**

Contains the top-level items from the Data Dictionary. This area allows you to specify available properties in the **Definition** grid.

**Definition**

Displays all defined criteria associated with a filter. To add to or modify the definition list, you must select a line in the list and then define or edit the property in the **Edit** group.

**Match all**

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

35/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Specifies that only items matching ALL of the filtering criteria pass through the filter.

**Match any**

Specifies that items matching any one or more of the filtering criteria pass through the filter.

**Match any** is the default matching method.

**Add**

Places a new entry at the end of the existing definition list and enables the options in the **Edit** group so you can edit the new entry.

**Delete**

Removes the selected criterion from the definition list. This button is available only when you select a criterion in the definition list.

**Edit**

Allows you to define or edit a single line of filter definition criteria.

**Property**

Displays a list of all properties for a certain item type. Examples of properties include **Equipment Type**, **Instrument Loop Item Tag**, and **Estimated Length**. You define or modify filtering criteria by selecting a property, an operator, and a value.

**Operator**

Specifies the relationship between the property and its value. Examples of relationships include greater than (>), equal to (=), and not equal to (<>).

If a string property is being filtered or a wildcard character is being used, only the

‘equal to’ (=) operator is valid as a selection. When a wildcard character is used, the ‘equal to’

operator actually behaves as a ‘like’ operator.

**Value**

Lists appropriate values for the property specified in the **Property** list. If a list of attributes is not already associated with the **Value** box, you must type a value, which can be free text, or choose null. You can use a percent sign (**%**) as a wildcard character to find multiple https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

36/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

characters or an underscore (_) as a wildcard character for a single character. Do not use an asterisk (*****) in the **Value** box.

**Add Filter Dialog**

Specifies properties of a filter, including the name, description, and the other properties for which you want to filter. Each item type owns a set of properties. Examples of item types are **Equipment**, **Instrument**, and **Pipe Run**, and examples of properties for these item types are **Equipment Type**, **Instr. Loop Item Tag**, and **Estimated Length** respectively.

**Name**

Specifies the filter name. The name can be any combination of characters and any length.

Filter names within a plant must be unique. This name appears as the filter name in the Filter Manager interface.

**Description**

Specifies a phrase or sentence about the filter. The description can be any combination of characters and any length. The description appears as a ToolTip when you point to the filter name in the Filter Manager interface.

**Filter for**

Contains the top-level items from the data dictionary. This area allows you to specify available properties in the **Definition** grid.

**Definition**

Displays all defined criteria associated with a filter. To add to or modify the definition list, you must select a line in the list and then define or edit the property in the **Edit** group.

**Match all**

Specifies that only items matching ALL of the filtering criteria pass through the filter.

**Match any**

Specifies that items matching any one or more of the filtering criteria pass through the filter.

**Match any** is the default matching method.

**Add**

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

37/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Places a new entry at the end of the existing definition list and enables the options in the **Edit** group so you can edit the new entry.

**Delete**

Removes the selected criterion from the definition list. This button is available only when you select a criterion in the definition list.

**Edit**

Allows you to define or edit a single line of filter definition criteria.

**Property**

Displays a list of all properties for a certain item type. Examples of properties include Equipment Type, Instrument Loop Item Tag, and Estimated Length. You define or modify filtering criteria by selecting a property, an operator, and a value.

**Operator**

Specifies the relationship between the property and its value. Examples of relationships include greater than (>), equal to (=), and not equal to (< >).

**Value**

Lists appropriate values for the property specified in the **Property** list. If a list of attributes is not already associated with the **Value** box, you must type a value, which can be free text, or choose null. You can type a percent sign (**%**) as a wildcard character to find multiple characters or an underscore (_) as a wildcard character for a single character. Do not use an asterisk (*****) in the **Value** box.

**Create a Simple Filter**

1. On the Rule Properties Dialog > Items Tab, select the **Browse** button beside the item whose filter you want to view.
2. Open the Select Item Dialog.
3. Select the folder in which you want to add the filter, and select **New** to open the Add

Filter Dialog.

1. Enter a name for the new filter.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

38/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

1. Enter a description in the **Description** box.
2. Select the **Filter for** list, and specify the item type for the new filter. The selection in the **Filter for** box determines which properties are available in the **Edit** group.
3. In the **Definition** area, select either **Match all** or **Match any**.

**Match all** means that only those items matching ALL of the filtering criteria pass through the filter. **Match any** means that items matching any one or more of the filtering criteria pass.

1. In the **Edit** group, select the filter property, operator, and corresponding value for the first filter criterion.
2. Select **Add** to add a line for another filter definition, if needed, and repeat the previous step.

If you select a date-formatted property, you can specify a date for that property. Select near **Value** in the **Edit** group and select a date on the Calendar Dialog.

If you have the Select Item Dialog open and are creating or modifying a filter, do not open Filter Manager and make changes to filters in that utility at the same time.

**Calendar Dialog**

Specifies a date in the **Value** box on the Filter Properties Dialog. For example, you might want

to filter for pumps that have a date value defined. A date **Value** is available only for those properties that are date formatted as specified in Data Dictionary Manager. Select the date you want and select **OK**.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

39/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Month**

Allows you to choose the correct month.

**Year**

Allows you to choose the correct year.

**Dates**

Allows you to specify the date of the month.

**Compound Filter Properties Dialog**

A compound filter consists of more than one simple filter. Simple filters are added to the compound filter by dragging the simple filter to the compound filter folder or by creating new simple filters under the compound filter in the filter hierarchy. Compound filters apply only to homogeneous item types. This dialog specifies the properties of a compound filter, including the name, description, and whether to match all or any of the simple filter criteria.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

40/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Name**

Specifies the filter name. The name can be any combination of characters and has no length limit. Filter names within a plant must be unique. This name appears as the filter name in the

Select Item Dialog.

**Description**

Specifies a phrase or sentence about the filter. The description can be any combination of characters and has no length limit. The description appears as a ToolTip when you point to

the filter name in the Select Item Dialog.

**Filter method**

Allows you to decide whether items must meet all or only one criterion to pass through the filter.

**Match all**

Specifies that items matching ALL of the filtering criteria pass through the filter.

**Match any**

Specifies that items matching any one or more of the filtering criteria pass through the filter.

**Match any** is the default matching method.

**Understanding Placement Properties**

Under different circumstances with different catalog items, you want to control how that item is placed in a design and how it relates to other items nearby. Placement properties allow you to specify how items appear in the drawing and how they are related to other items.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

41/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

You choose the type of placement in a rule when you choose the items involved in that rule.

On the Items Tab (Rule Properties Dialog), you can specify the placement type and options

for the placement type that you choose.

The following placement type options are available:

**None**

Use this option for freestanding or non-existent items or for rules that do not pertain to the placement of an item. For example, a rule that prohibits the placement of an item can naturally use **None** for the placement type.

**Geometric**

This placement type is frequently used for equipment and equipment components. You can specify rotation and mirroring with this placement type, making it the appropriate way to control how, for example, a nozzle behaves when you place it inside or outside of a piece of equipment. You can select **Properties** to define the options for this placement type on the

Geometric Placement Properties Dialog.

**In-Line**

Use this option to control how an item is placed in relationship to a signal or pipe run. This placement type is used for inline piping and instrument components. Select **Properties** to define the options for this placement type on the In-Line Placement Properties Dialog.

**Label**

Specify this placement type for rules governing the placement of a label on its target.

**Snap-On**

Use this option to connect items without the geometric implications of the geometric placement type. It is used, for example, to connect an instrument to an instrument. Select **Properties** to define the options for this placement type on the Snap-On Placement

Properties Dialog.

**Line Run**

Use this placement type for rules governing the placement of line or signal runs.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

42/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Choose a Placement Method**

1. Select the rule you want to modify, and select **Edit** > Properties to display the Rule

Properties Dialog.

1. Select the Items Tab.
2. In the **Placement method** list for **Item 1**, choose a placement type.
3. Select **Properties** next to the **Placement method** list in order to further specify options for the placement type you have chosen.

If you select a placement method that does not have further options to specify, the **Properties** button is not available.

1. If you have specified an **Item 2** for this rule, choose a placement type for **Item 2** and then specify the placement method properties.

Occasionally, you might want to specify a placement method for both items. For example, if you have a rule that applies to valves and pipes and want to place valves on pipes and also connect pipes to valves, you should specify a placement method for each item. You are not required to select a placement method for both items.

You select a placement method for an item only if you can place that item on another item. In the nozzle example, you do not select a placement method for the vessel because you do not want to place a vessel on an existing nozzle.

You do not need to select any placement method at all. If a rule does not have a placement method associated with it, the rule does not participate in placement. You can use this type of rule for consistency checking or implied items.

**Using Geometric Placement**

The Geometric placement method is designed to support placement of one item, the source, as a freestanding item or relative to an existing item, the target. The method assumes that the source item is a symbol and does not use connect points. You do not need to specify connect point types on the Items Tab (Rule Properties Dialog).

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

43/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

This placement method allows you to snap to the target, rotate perpendicular to the target, and mirror to the inside or the outside of the target.

Use this placement method to place freestanding items, such as equipment, and to place equipment components, such as nozzles and trays.

**Geometric Placement Properties Dialog**

Defines placement methods according to the geometry of the items that you are placing. You can select options that allow you to define snap placement (using connect points), orthogonal placement, mirroring, assign ownership of items, and so forth. Distances can be defined for items you are placing inside other items.

After selecting **Geometric** on the Items Tab (Rule Properties Dialog), the **Geometric** **Placement Properties** dialog opens when you select the **Properties** button next to the **Placement type** list .

**Action**

**Position**

Defines the action to take when positioning the target item. Choose from the following options:

**None**

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

44/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

Allows you to place an item without it actually touching the item on which it is being placed.

**Snap**

Allows you to actually place an item that automatically attaches to the geometry of the item on which you are placing it.

**Rotation**

Defines the action to take when rotating an item that you are placing. Choose from the following options:

**None**

Indicates that no rotation applies.

**Align**

Rotates the item that you are placing perpendicular to the geometry of the item on which you are placing it. You can place the item at any angle.

**Orthogonal**

Sets the rotation to 90 degrees using the north, south, east, and west positions.

**Mirror**

Defines an action to take when mirroring an item. Choose from the following options: **Mirror to Cursor**

Mirrors the item according to location of the pointer. If the pointer is outside the item, then you can mirror and place your item there. If the pointer is inside the item, then you can mirror the item and place it.

**Mirror to Outside**

Mirrors the item that you are placing outside of the geometry of the item already placed.

**Mirror to Inside**

Mirrors the item that you are placing inside of the geometry of the item that you already placed.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

45/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**None**

Does not allow mirroring of the item you are placing.

**Owner**

Defines the item that owns the item that you are placing. For example, if you are placing a nozzle on a pump, then the pump is defined as the owner of the nozzle. If the pump is moved later, then the nozzle moves with the pump. Choose from the following options: **None**

Implies items that you are placing are not associated and do not move with the item already placed.

**Glue to Target**

Establishes an association with the item you are placing and the item already placed. If one of these items is moved, all associated items move also.

**Reach**

Allows you to place an item inside another item without touching the geometry of the item already placed.

**Reach distance**

Defines the effective distance between the source and target items for associated actions to exhibit their behavior. This distance is measured in meters.

**Using Inline Placement**

Inline placement is designed to support placement of one item, the source, relative to an existing item, the target. The method assumes that the source item is a symbol and the target item is a line run. Inline placement uses connect point information in the source item and calculates placement configurations with the geometry of the target line run. When you use this placement method, you specify the connect point type for the source item, but you do not specify connect point type for the target item.

You specify options for inline placement on the In-Line Placement Properties Dialog. This placement method works in two ways:

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

46/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

If te **Rotate and mirror to fit** is **True**, the software explores all possible combinations of rotation and mirroring to find the ways that the source can fit on the target geometry.

The software can generate multiple configurations and display them by using the configuration tool in the design software.

If **Rotate and mirror to fit** is **False**, the software finds the connect points on the source that match the target geometry. If a match is found, the software generates a single configuration with zero rotation.

Placement is available for both the endpoints and at any internal points within a line. If you place an item at an internal point, the line is broken into two runs, and the new item is inserted.

Use this placement method primarily to place instruments and piping components into pipes and signal lines. You can place off-page and utility connectors on end-points by using this method, too.

**In-Line Placement Properties Dialog**

Defines inline component placement methods. After selecting **In-Line** on the Items tab (Rule

Properties Dialog), the **In-Line Placement Properties** dialog opens when you select the **Properties** button next to the **Placement type** list .

**Action**

**Rotate and mirror to fit**

Enables mirroring and rotating to fit options.

**Place only at end point**

Allows for inline placement only at an endpoint.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

47/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Add to line run**

Allows you to add items to a run. If you do not choose **Place only at end point**, this option is not available.

**Using Label Placement**

Use the **Label** placement type for rules that relate labels to their targets. Look in the delivered **Label Placement** folder in Smart P&ID Rule Manager for some examples.

**Using Snap-On Placement**

Snap-On placement supports placement of one item, the source, relative to an existing item, the target. The method assumes that symbols represent both the source and target items.

Snap-on placement relies on connect points in both the source and target to define the placement configurations. When you use this placement method for an item, you specify the connect point types for both items.

You can use this placement method to place actuators on valves, TEMA ends on TEMA shells, and instrument functions on instruments. You can also use this method to place inline components, such as valves, directly on nozzles and other inline components.

This placement method works in two ways:

If **Rotate To Fit** is **True**, the software generates a configuration for each connect point in the source. Each configuration rotates the source by an angle to allow the source and target connect points to match.

If **Rotate To Fit** is **False**, the software finds the one connect point on the source that matches with the target connect point. The software generates a single configuration with zero rotation.

**Snap-On Placement Properties Dialog**

Specifies placement options for the snap-on method. You can define the mirroring options, an owner for the item being placed, and a gap distance that defines the placement distance between items. After selecting **Snap-On** on the Items tab (Rule Properties Dialog), the **Snap-On Placement Properties** dialog opens when you select the **Properties** button next to the **Placement type** list .

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

48/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Action**

**Rotate to fit**

Rotates the item being placed so that the connect points fit together. If not selected, the software locates the connect points and no rotation is applied.

**Mirror**

Allows you to choose to mirror, or flip, the orientation of an item. For example, set this option if you want nozzles to always point out from the geometry of equipment.

**Owner**

Defines how the item being placed is related to the target item. Choose from the following options:

**Glue To Target**

Implies items are kept together during a move. For example, when you move equipment, all components attached to it also move.

**Connect to Target**

Implies the item being placed is connected to the target item by means of a pipe run or a signal run.

**None**

Implies items you are placing are not associated and do not move with the item already placed.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

49/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Gap distance**

Defines the distance between your items. This distance is in meters.

**Using Line Run Placement**

Line Run placement supports placement of one item, the source, relative to an existing item, the target. The method assumes that the source item is a line run and the target item is a symbol. Line run placement uses connect point information in the target item to calculate the placement configurations. When you use this placement method, you specify the connect point type for the target item. Do not specify connect point types for the source item.

The **Line Run Placement** method uses this placement method to attach piping and signal lines to instruments and piping components.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

50/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to the Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our

documentation web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To access the Technical User Forum, go to ALI TUF Link <https://hexagon.com/support-

success/asset-lifecycle-intelligence/tuf> .

**Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, Intergraph, or its affiliates, parents, subsidiaries retains ownership of the product.

You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

51/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Copyright Notice**

**Copyright**

Copyright © 1999-2024 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB and/or its subsidiaries and affiliates.

**U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below.

For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014

and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division 305 Intergraph Way

Madison, AL 35758

**Documentation**

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

**Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

52/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

**Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

**Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

53/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL

EVALUATION AS TO THE USEFULNESS OF THE SOFTWARE IN HIS OWN

ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

**Limitation of Damages**

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

**Export Controls**

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

54/56

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

**Trademarks**

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, SmartPlant Cloud®, PDS®, FrameWorks®, I-Route, I-Export, ISOGEN®, SPOOLGEN, SupportManager®, SupportModeler®, SAPPHIRE®, TANK, PV Elite®, CADWorx®, CADWorx DraftPro®, GTSTRUDL®, CAESAR II® , and HxGN SDx® are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners.

Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

55/56

3/13/25, 10:45 AM

Hexagon Documentation Site Export

**Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/6bc8a067-06e0-411d-8abd-bca97e3bb615

56/56