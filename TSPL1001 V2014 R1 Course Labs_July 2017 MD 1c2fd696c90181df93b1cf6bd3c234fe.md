# TSPL1001 V2014 R1 Course Labs_July 2017 MD

SMARTPLANT® P&ID

SETUP AND CUSTOMIZATION COURSE LABS

Version 2014 R1

July 2017

DPID2-TP-100032A

- 
    - 

## **Copyright**

Copyright © 1999-2017 Hexagon PPM, a division of Intergraph Corporation. All rights reserved.

Including software, documentation, file formats, and audiovisual displays; may be used pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph and/or third parties which is protected by copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Intergraph Corporation.

## **U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below. For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS

252.227-7014 and the rights of the Government are as specified at DFARS 227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation

305 Intergraph Way

Madison, AL 35758

## **Documentation**

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

## **Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Intergraph Smart Support, SharePoint, or box.net, any documentation related to work processes, workflows, and best practices that is provided by Intergraph as guidance for using a software product.

## **Terms of Use**

1. 

Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation. If the Licensee has a valid signed license for this software product with Intergraph Corporation, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Intergraph Corporation gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.

1. 

For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Intergraph, Intergraph grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Intergraph Corporation gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Intergraph Corporation by giving written notice to Licensee.

## **Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Intergraph Corporation disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Intergraph believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Intergraph Corporation is not responsible for any error that may appear in this document.

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL

EVALUATION AS TO THE USEFULNESS OF THE SOFTWARE IN HIS OWN ENVIRONMENT.

- 
    - 

Intergraph is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data.

Users should verify for themselves that the data is accurate and suitable for their project work.

## **Limitation of Damages**

IN NO EVENT WILL INTERGRAPH CORPORATION BE LIABLE FOR ANY DIRECT, INDIRECT, CONSEQUENTIAL INCIDENTAL, SPECIAL, OR PUNITIVE DAMAGES, INCLUDING BUT NOT LIMITED TO, LOSS OF USE OR PRODUCTION, LOSS OF

REVENUE OR PROFIT, LOSS OF DATA, OR CLAIMS OF THIRD PARTIES, EVEN IF INTERGRAPH CORPORATION HAS BEEN

ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

UNDER NO CIRCUMSTANCES SHALL INTERGRAPH CORPORATION’S LIABILITY EXCEED THE AMOUNT THAT

INTERGRAPH CORPORATION HAS BEEN PAID BY LICENSEE UNDER THIS AGREEMENT AT THE TIME THE CLAIM IS

MADE. EXCEPT WHERE PROHIBITED BY APPLICABLE LAW, NO CLAIM, REGARDLESS OF FORM, ARISING OUT OF OR IN

CONNECTION WITH THE SUBJECT MATTER OF THIS DOCUMENT MAY BE BROUGHT BY LICENSEE MORE THAN TWO (2) YEARS AFTER THE EVENT GIVING RISE TO THE CAUSE OF ACTION HAS OCCURRED.

IF UNDER THE LAW RULED APPLICABLE ANY PART OF THIS SECTION IS INVALID, THEN INTERGRAPH LIMITS ITS

LIABILITY TO THE MAXIMUM EXTENT ALLOWED BY SAID LAW.

## **Export Controls**

Intergraph Corporation’s commercial-off-the-shelf software products, customized software and/or third-party software, including any technical data related thereto (“Technical Data”), obtained from Intergraph Corporation, its subsidiaries or distributors, is subject to the export control laws and regulations of the United States of America. Diversion contrary to U.S. law is prohibited. To the extent prohibited by United States or other applicable laws, Intergraph Corporation software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Intergraph Corporation, its subsidiaries or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: a.

To Cuba, Iran, North Korea, the Crimean region of Ukraine, or Syria, or any national of these countries or territories.

1. 

To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List (https://build.export.gov/main/ecr/eg_main_023148).

1. 

To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Intergraph Corporation, its subsidiaries or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.

1. 

To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.

Any questions regarding export/re-export of relevant Intergraph Corporation software product, customized software, Technical Data and/or third-party software obtained from Intergraph Corporation, its subsidiaries or distributors, should be addressed to PPM’s Export Compliance Department, 305 Intergraph Way, Madison, Alabama 35758 USA or at exportcompliance@intergraph.com.

Customer shall hold harmless and indemnify PPM and Hexagon Group Company for any causes of action, claims, costs, expenses and/or damages resulting to PPM or Hexagon Group Company from a breach by Customer.

## **Trademarks**

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine®, SmartSketch®, SmartPlant Cloud®, PDS®, FrameWorks®, I-Route, I-Export, Isogen®, SPOOLGEN, SupportManager®, SupportModeler®, SAPPHIRE®, TANK, PV Elite®, CADWorx®, CADWorx DraftPro®, GTSTRUDL®, and CAESAR II® are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

*SmartPlant P&ID Setup and Customization Course Labs* **Table of Contents**

**Preface …………………………………………………………………………………………………………………8**

**Lab 1 – Plant Group Types …………………………………………………………………………………..9**

Creating a New Plant Group Type ……………………………………………………………………..9

Entering Data Dictionary Manager for the Plant Group Types …………………………….10

Creating Another Plant Group Type …………………………………………………………………11

**Lab 2 – Hierarchy Templates ……………………………………………………………………………..12**

Creating a New Hierarchy Template Utilizing the New Plant Group Type ……………12

Adding a New Level to the TSPL1001E Hierarchy ……………………………………………13

**Lab 3 – Creating a New Site Server and Plant Structure ……………………………………..15**

Preliminary Setup ………………………………………………………………………………………….15

Creating a New Site Server ……………………………………………………………………………..16

Creating a New Plant Structure Using Hierarchy 7 …………………………………………….20

Associating the SmartPlant P&ID Application ………………………………………………….24

Assigning Roles to the New Plant Structure and Application ………………………………27

Creating Plant Groups for the New Plant Structure …………………………………………….27

Creating Drawings …………………………………………………………………………………………30

**Lab 4 – Working with Data Dictionary Templates ………………………………………………31**

Creating a Plant Data Dictionary Template ……………………………………………………….31

Creating a P&ID Application Data Dictionary Template …………………………………….32

Using the Data Dictionary Template Files ………………………………………………………..33

Preliminary Setup ………………………………………………………………………………………………. 33

Creating a Plant Structure ……………………………………………………………………………………. 33

Associating the SmartPlant P&ID Application ……………………………………………………….. 37

Assigning Roles to the New Plant Structure and Application …………………………………… 40

Creating Plant Groups for the New Plant Structure …………………………………………………. 40

Creating Drawings ……………………………………………………………………………………………… 43

**Lab 5 – Importing Drawings ……………………………………………………………………………….44**

Preliminary Setup for the Import Process ………………………………………………………….44

The Import Drawing Process …………………………………………………………………………..45

**Lab 6 – Creating a Border File and PID Template File ………………………………………..49**

Creating a Border File ……………………………………………………………………………………49

Creating a PID Template File ………………………………………………………………………….53

Creating a Drawing Using the New Template ……………………………………………………59

**Lab 7 – Migrating a SmartSketch Drawing (Optional Lab) …………………………………60**

4 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 8 – Cloning an Existing Symbol (TEMA) ……………………………………………………..63**

**Lab 9 – Cloning an Existing Symbol (Vessel) ……………………………………………………….66**

**Lab 10 – Creating a New Symbol (Piping Component) ………………………………………..68**

**Lab 11 – Creating Viewable Labels …………………………………………………………………….72**

**Lab 12 – Creating a Revision Label …………………………………………………………………….76**

**Lab 13 – Creating a Parametric Black Box ………………………………………………………….83**

Creating the Symbol in the Catalog ………………………………………………………………….83

Setting Drawing Options ………………………………………………………………………………..84

Drawing the New Symbol ………………………………………………………………………………85

Adding Dimensions to the Symbol …………………………………………………………………..86

Adding Variables and Equations to the Symbol …………………………………………………89

**Lab 14 – Creating a Parametric Pump (Optional Lab) ………………………………………..92**

Creating the Symbol in the Catalog ………………………………………………………………….92

Setting Drawing Options ………………………………………………………………………………..93

Drawing the New Symbol ………………………………………………………………………………94

Adding Dimensions to the Symbol …………………………………………………………………101

Adding Variables and Equations to the Symbol ……………………………………………….102

**Lab 15 – Creating a New Select List and Property …………………………………………….106**

Creating the Paint Code Select List ………………………………………………………………..106

Creating the Paint Code Property in the Equipment Table …………………………………107

Creating an Equipment Label Utilizing the Paint Code Property………………………..108

**Lab 16 – Working with Properties in Data Dictionary Manager …………………………110**

Turning Off the Display of a Property …………………………………………………………….110

Changing the Display Name of a Property ………………………………………………………110

Modifying Permissions of a Property ……………………………………………………………..111

Testing the Changes ……………………………………………………………………………………..111

Bonus Lab …………………………………………………………………………………………………..112

**Lab 17 – Adding Properties to Drawings and Plant Groups ……………………………….113**

Adding Properties to Drawings ……………………………………………………………………..113

Adding Properties to the Plant ……………………………………………………………………….115

**Lab 18 – Creating New Filters for Display Sets ………………………………………………….116**

**Lab 19 – Customizing Options Manager ……………………………………………………………119**

SmartPlant P&ID Setup and Customization Course Labs5 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

Bonus Lab …………………………………………………………………………………………………..121

**Lab 20 – Implementing Jacketed Pipe ……………………………………………………………….122**

Creating a Jacket for a Piping Component ………………………………………………………122

Enabling Jacketing ……………………………………………………………………………………….123

**Lab 21 – Creating New Rules ……………………………………………………………………………126**

**Lab 22 – Review of Existing Rules …………………………………………………………………….129**

**Lab 23 – Creating Buried Pipe ………………………………………………………………………….130**

Creating a Symbol for the New Line Style in Catalog Manager …………………………130

Installing the Line Style Editor …………………………………………………………………………… 131

Creating a Point Style ……………………………………………………………………………………….. 132

Defining the Point Style Graphics ………………………………………………………………………. 132

Creating a Linear Pattern …………………………………………………………………………………… 133

Creating a Linear Style ……………………………………………………………………………………… 134

Testing the Linear Style …………………………………………………………………………………….. 135

Importing the Linear Pattern and Linear Style in Options Manager ……………………136

Adding a New Pipe Run Type of Buried Pipe in the PID Data Dictionary …………..137

Defining the Symbology for Buried Pipe in Options Manager …………………………..138

Creating Buried Piping in Catalog Manager ……………………………………………………140

Routing Buried Piping in a P&ID Drawing ……………………………………………………..141

Editing the Process Pipe Run Rule in Rule Manager ………………………………………..142

Updating a Drawing and Reviewing Inconsistencies ………………………………………..143

**Lab 24 – Creating and Using a New Format ………………………………………………………145**

Creating a New Format …………………………………………………………………………………145

Creating a New Symbol Utilizing the New Format…………………………………………..146

Testing the Label …………………………………………………………………………………………147

Bonus Lab …………………………………………………………………………………………………..148

**Lab 25 – Creating and Using a New Insulation Specification ……………………………..149**

**Lab 26 – Importing Data …………………………………………………………………………………..154**

**Lab 27 – Creating New Reports ………………………………………………………………………..156**

**Lab 28 – Reporting from a Drawing and Excluding Drawing Stockpile Items …….159**

**Lab 29 – Reporting from the EDE …………………………………………………………………….160**

**Lab 30 – Editing a Report Template to Exclude Stockpile Items ………………………..161**

6 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 31 – Customizing the Report Header ………………………………………………………….163**

**Lab 32 – Creating Drawing Revisions ……………………………………………………………….166**

**Lab 33 – Versioning Drawings ………………………………………………………………………….167**

**Lab 34 – Fetching a Deleted Drawing ………………………………………………………………..168**

**Lab 35 – Backing Up and Restoring a Plant ………………………………………………………169**

Backup the Plant ………………………………………………………………………………………….169

Delete the Plant from the Site ………………………………………………………………………..170

Restore the Plant Backup to the Site……………………………………………………………….170

**Lab 36 – Running Reference Data Synchronization Manager …………………………….173**

**Lab 37 – Copying a Plant ………………………………………………………………………………….175**

Save Plant Structure ……………………………………………………………………………………..175

Load Plant Structure …………………………………………………………………………………….176

Finish Load Plant Structure Processing ……………………………………………………………….. 180

**Lab 38 – Running the Data Dictionary Template Comparison Utility …………………182**

SmartPlant P&ID Setup and Customization Course Labs7 *** ***

*SmartPlant P&ID Setup and Customization Course Labs* **Preface**

This document is a course guide for the various SmartPlant Engineering Manager and P&ID User Guides. The content is the similar as the online Help delivered as part of the software except for the Labs.

8 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 1 – Plant Group Types**

**Objective:**  To create new plant group types in SmartPlant Engineering Manager, and enter Data Dictionary Manager to view the new plant group types.

**Creating a New Plant Group Type**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> SmartPlant Engineering Manager**.

1. Select on the **+** sign to expand the **Plant Group Types**.
2. Select the **Plant Group Types** node.
3. Select **File** > **New**

SmartPlant P&ID Setup and Customization Course Labs9 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **OR**

Right-click on the **Plant Group Types** node, and select **New** **Type**.

1. On the **New Type** dialog box, enter the following property values, and then select **OK**.

**Note:**

- The * indicates a property value is required and must be defined.

**Entering Data Dictionary Manager for the Plant**

## **Group Types**

1. Select the **Plant Group Types** node.
2. Select **Tools** > **Data** **Dictionary** **Manager** 10 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

## **OR**

Right click on the **Plant Group Types** node, and select **Data** **Dictionary** **Manager**.

1. In the **Database Tables,**  notice the entry, **Building**, was created.
2. Select **Database Item Types**, and notice the Item Type, **SPMBldg**, for the Plant Group Type created.
3. Select **File** > **Exit** to exit **Data Dictionary Manager**.

## **Creating Another Plant Group Type**

1. Select the **Plant Group Types** node, and create another Plant Group Type.
2. In the **Plant Group Types** node, select the Plant Group Type** **just created.
3. Select **Edi**t > **Delete**

## **OR**

Right click and select **Delete**.

SmartPlant P&ID Setup and Customization Course Labs11 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 2 – Hierarchy Templates**

**Objective:**  To create a new hierarchy template using the new plant group type.

**Creating a New Hierarchy Template Utilizing the**

## **New Plant Group Type**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> SmartPlant Engineering Manager**

1. Select the + sign to expand the **Hierarchy Templates**.
2. Select the **Hierarchy Templates** node.
3. Select **File** > **New**.

## **OR**

12 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

Right-click on the **Hierarchy Templates** node, and select **New** **Hierarchy** **Template….**

1. On the **New Hierarchy Template** dialog box, enter the following property values, and then select **OK**.

**Note:**

- The name is limited to 80 characters, and spaces are permitted but no other special characters.

**Adding a New Level to the TSPL1001E Hierarchy**

1. Expand the **TSPL1001E** hierarchy by selecting the **+** sign.
2. Under the **TSPL1001E** hierarchy, select the **Plant** level.
3. Select **File** > **New**.

## **OR**

Right-click on the **Plant** level, and select **New** **Level.**

1. On the **New Level** dialog box, select the following property values from the drop-down menus, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs13 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Note:**

- **Depth** is automatically assigned, and is a read-only property.
1. The new **TSPL1001E** Hierarchy Template should be like the image below.

14 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 3 – Creating a New Site Server and Plant**

## **Structure**

**Objective:**  To create a new site server and plant structure, set up user access and create new plant groups and drawings.

**Preliminary Setup**

## **Important**

- It is understood that the Database is installed and configured prior to the following steps.
1. From **Windows** **Explorer**, select **New folder** and create a new folder named **PPM_Site** on the C: drive.
2. Right click on the **PPM_Site** folder, and select **Properties**.
3. On the **PPM_Site Properties** dialog box > **Sharing** tab, select the **Share** button.
4. On the **File Sharing** dialog box, select the **Share** button, and then select **Done**.
5. Double-click on the **PPM_Site** folder, select **New folder** and create the following subfolders.
- **501K**
- **Backups**
- **INI**
- **Role Templates**
1. Double-click on the **501K** folder, select **New folder**, and then create a subfolder named **Drawings**.
2. Browse to **C:\Program Files (x86)\SmartPlant** folder.
3. Select and **copy** the delivered **P&ID Reference Data** folder.
4. **Paste** the **P&ID Reference Data** folder into the **501K** folder.
5. Once complete, the folder structure should be like the image below.

SmartPlant P&ID Setup and Customization Course Labs15 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **Creating a New Site Server**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> SmartPlant Engineering Manager**.

1. Select the **Site Server** node.
2. Right-click on the **Site** **Server** node, and select **New** **Site** **Server…**

## **OR**

Select **File** > **New.**

1. On the New Site Server wizard dialog, select **Use default template**, and then select **Next.**
2. Enter the following Site server name and path information for the new site, and then select **Next**.

16 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Enter the following information to set the database type and server for the site schema, and then select** Next. **
2. For the** Group Filter**, select** Use local machine and domain groups**.
3. For the Site administrator user group…
4. Click the **Browse** button to display the **Select Group** dialog box, and in the **Enter the object name to select** field, key in **Administrators**.
5. Click the **Check Names** button, and then click **OK**.
6. Select the** Add the site administrator group to each plant created** checkbox, and then select **Next** to select the group that will have the site administrator privileges.

SmartPlant P&ID Setup and Customization Course Labs17 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the *defaults* to enter the database server and user information for the site schema, and then select **Next**.
2. Select the *defaults* to enter the database server and user information for site data dictionary, and then select **Next.**

18 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Review the settings for the site schema creation, and then select **Finish**.
2. When the **Site** creation process finishes, you will have a site server like the following image.

SmartPlant P&ID Setup and Customization Course Labs19 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Creating a New Plant Structure Using Hierarchy 7**

1. Select the **Plant** **Structures** node, right-click and select **New** **Plant** **Structure**.
2. For the **Data** **Dictionary** **Source** select **Use** **default** **template**, and then select **Next.**

---

1. In the **Hierarchy** pull-down menu, select **Hierarchy 7**, and then select **Next**.

---

20 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Enter the following Name and Description information for the new plant, and then select **Next**.

---

1. Enter the following Plant structure path and Backup location for the plant structure storage, and then select **Next**.

---

1. Enter the following information to set the database type and server for the plant schema, and then select **Next**.

SmartPlant P&ID Setup and Customization Course Labs21 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

---

1. Select the *defaults* to enter the database server and user information for the plant structure schema, and then select **Next**.

**Note:**

- The database username is the *plant name with a prefix of the letter ‘P’*

since a database username cannot begin with a number.

1. Select the *defaults* to enter the database server and user information for the plant structure data dictionary, and then select **Next**.

22 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Review the settings for the site schema creation, and then select **Finish**.

---

1. When the **Plant Structure** creation process finishes, you will have a plant structure like the following image. ** **

---

SmartPlant P&ID Setup and Customization Course Labs23 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Associating the SmartPlant P&ID Application**

1. Under the **501K** Plant, select the **Applications** node, right-click and select **Associate** **Applications**.
2. Enter the following information to select the Applications to associate and the reference data path, and then select** Next**.
3. Select **ANSI/IGR with Imperial Units** as the Data dictionary source, and then select **Next**.

24 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

---

1. Select the *defaults* to enter the database server and user information for the SmartPlant P&ID schema, and then select **Next**.
2. Select the *defaults* to enter the database server and user information for the SmartPlant P&ID data dictionary, and then select **Next**.

SmartPlant P&ID Setup and Customization Course Labs25 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

---

1. Review the settings for the application association, and then select **Finish**.

---

**7.** When the **Associate Application** process finishes, **SmartPlant P&ID** will be listed under **Applications** like the following image. ** **

26 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Assigning Roles to the New Plant Structure and**

## **Application**

1. Under the **501K** Plant, select the **Roles** node, right-click and select **New** **Role**.

**Note:**

- If you checked the option to **Add the site administrator group to each** **plant created** during the **Site** creation you will have a role automatically assigned to the new plant.

**Creating Plant Groups for the New Plant Structure**

1. Under the **501K** Plant, select the **Plant Groups** node, right-click and select **New** **Area**.
2. Enter the following information for the New Area, and then click **OK**.

SmartPlant P&ID Setup and Customization Course Labs27 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Under **501K > Plant Groups**, select **Area1**, right-click and select **New Unit**.
2. Enter the following information for the New Unit, and then click **OK**.
3. Under the **501K** Plant, select the **Plant Groups** node, right-click and select **New** **Area**.
4. Enter the following information for the New Area, and then click **OK**.

28 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Under **501K > Plant Groups**, select **Area2**, right-click and select **New Unit**.
2. Enter the following information for the New Unit, and then click **OK**.
3. Select **Area2** again, right-click and select **New Unit**.
4. Enter the following information for the New Unit, and then click **OK**.

SmartPlant P&ID Setup and Customization Course Labs29 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. After creating the Plant Groups, there will be Areas and Units like the following image.

## **Creating Drawings**

1. Open the **501K** Plant in Drawing Manager, and create drawings for each Unit (Unit1A, Unit2A, and Unit2B) using the **New Drawing** command.

30 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 4 – Working with Data Dictionary**

## **Templates**

**Objective:**  To generate new data dictionary templates (.ddt files) based on the selected plant and application schema, and use them to create a plant and associate an application.

**Creating a Plant Data Dictionary Template**

1. Open **SmartPlant Engineering Manager**.
2. Select the **501K** Plant, right-click and select **New Data Dictionary Template.**

## **OR**

Select **Tools** > **New Data Dictionary Template…**

1. On the **New Data Dictionary Template** dialog, select **OK** to accept the default template name and path.

SmartPlant P&ID Setup and Customization Course Labs31 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. After the successful creation of the plant data dictionary template, the following message will be displayed. Click **OK**.

**Creating a P&ID Application Data Dictionary**

## **Template**

1. Select the **501K > Applications** node and in the List View, right-click on **SmartPlant P&ID**, and select **New Data Dictionary Template.**
2. On the **New Data Dictionary Template** dialog, select **OK** to accept the default template name and path.
3. After the successful creation of the SmartPlant P&ID data dictionary template, the following message will be displayed. Click **OK**.

32 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Using the Data Dictionary Template Files**

## **Preliminary Setup**

1. From **Windows** **Explorer**, double-click on the **PPM_Site** folder, select **New** **folder** and create a subfolder named **Custom**.
2. Double-click on the **Custom** folder, select **New folder**, and then create a subfolder named **Drawings**.
3. Browse to **501K** folder.
4. Select and **copy** the **P&ID Reference Data** folder.
5. **Paste** the **P&ID Reference Data** folder into the **Custom** folder.
6. Once complete, the folder structure should be like the image below.

## **Creating a Plant Structure**

1. Select the **Plant** **Structures** node, right-click and select **New** **Plant** **Structure**.
2. For the **Data** **Dictionary** **Source**, select **Use** **custom template**, browse to the location of the plant data dictionary template, and then select **Next.**

SmartPlant P&ID Setup and Customization Course Labs33 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Note:**

- The** **status,**  Template is valid**, displays in the** **lower left** **corner.
1. Enter the following Name and Description information for the new plant, and then select **Next**.
2. Enter the following Plant structure path and Backup location for the plant structure storage, and then select **Next**.
3. Enter the following information to set the database type and server for the plant schema, and then select **Next**.

34 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

---

1. Select the *defaults* to enter the database server and user information for the plant structure schema, and then select **Next**.
2. Select the *defaults* to enter the database server and user information for the plant structure data dictionary, and then select **Next**.

SmartPlant P&ID Setup and Customization Course Labs35 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Review the settings for the site schema creation, and then select **Finish**.

---

1. When the **Plant Structure** creation process finishes, you will have a plant structure like the following image. ** **

---

36 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Associating the SmartPlant P&ID Application**

1. Under the **Custom** Plant, select the **Applications** node, right-click and select **Associate** **Applications**.

## **OR**

Select **Tools** > **Associate** **Applications**

1. Enter the following information to select the Applications to associate and the reference data path, and then select** Next**.
2. For the **Data** **Dictionary** **Source**, select **Use** **custom template**, browse to the location of the P&ID application data dictionary template, and then select **Next.**

SmartPlant P&ID Setup and Customization Course Labs37 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Note:**

- The** **status,**  Template is valid**, displays in the** **lower left** **corner.
1. Select the *defaults* to enter the database server and user information for the SmartPlant P&ID schema, and then select **Next**.
2. Select the *defaults* to enter the database server and user information for the SmartPlant P&ID data dictionary, and then select **Next**.

38 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Review the settings for the application association, and then select **Finish**.

**7.** When the **Associate Application** process finishes, **SmartPlant P&ID** will be listed under **Applications** like the following image. ** **

---

SmartPlant P&ID Setup and Customization Course Labs39 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Assigning Roles to the New Plant Structure and Application**

1. Under the **Custom** Plant, select the **Roles** node, right-click and select **New** **Role**.

**Note:**

- If you checked the option to **Add the site administrator group to each** **plant created** during the **Site** creation you will have a role automatically assigned to the new plant.

**Creating Plant Groups for the New Plant Structure**

1. Under the **Custom** Plant, select the **Plant Groups** node, right-click and select **New** **Area**.
2. Enter the following information for the New Area, and then click **OK**.
3. Under **Custom > Plant Groups**, select **Area1**, right-click and select **New Unit**.

40 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Enter the following information for the New Unit, and then click **OK**.
2. Under the **Custom** Plant, select the **Plant Groups** node, right-click and select **New** **Area**.
3. Enter the following information for the New Area, and then click **OK**.

SmartPlant P&ID Setup and Customization Course Labs41 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Under **Custom > Plant Groups**, select **Area2**, right-click and select **New Unit**.
2. Enter the following information for the New Unit, and then click **OK**.
3. Select **Area2** again, right-click and select **New Unit**.
4. Enter the following information for the New Unit, and then click **OK**.

42 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. After creating the Plant Groups, there will be Areas and Units like the following image.

## **Creating Drawings**

1. Open the **Custom** Plant in Drawing Manager.
2. Right-click on each Unit (Unit1A, Unit2A, and Unit2B) and create drawings using the **New Drawing** command.

SmartPlant P&ID Setup and Customization Course Labs43 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 5 – Importing Drawings**

**Objective:**  To import a drawing from the source plant (501K) to the target plant (Custom) in the same site.

**Preliminary Setup for the Import Process**

1. Open **Options** **Manager** > **Settings** for the **Custom** plant and verify that the **Import Map Path** is set.
2. From **Windows** **Explorer**, verify the **Import Map Files** folder is created as defined by the **Import Map Path** setting in Options Manager.
3. If the above criterion is not defined, the following message will occur during the import process. Click **OK**.
4. Open **Drawing Manager**, select the **Custom** plant, and then click **Open**.

44 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the Plant Group (Unit) that you will import a drawing into.

## **The Import Drawing Process**

1. Select **File > Import Drawings**.
2. The **Import Drawings Wizard** will display. Select **Next**.
3. For the Source plant name, select the ellipse button, select **501K**, and then click **Open**.
4. The following Source plant name will display. Select **Next**.
5. Under **501K > Area1**, select **Unit1A**, and in the List View, select **Drawing1A**, and then select **Next**.

SmartPlant P&ID Setup and Customization Course Labs45 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Review the Map Status column in the List View to resolve any status of Incomplete. Select **Next**.
2. Select the following Options to utilize during the import process, and then select **Custom Options**.

46 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the *defaults* on the **Transformation Programs** dialog, and then select **OK**.
2. Select **Next**.
3. Review the Summary, and then select **Finish**.
4. The following message will be displayed. Select **Yes**.

**Note:**

- The first time the Import process is ran, you will be prompted with this message. Subsequent imports may also prompt you with this message if changes to the Import Map file would be required.
1. After completion of the Import Drawings process, select **View Log**, and then select **Close**.

SmartPlant P&ID Setup and Customization Course Labs47 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. The imported drawing will appear in the List View.

**Note:**

- To rename the drawing, right-click on the drawing and select **Properties**.

48 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 6 – Creating a Border File and PID**

## **Template File**

**Objective:**  To use a MicroStation (.dgn) file to create a border file which will be inserted into the PID template file used to create drawings in the Custom plant.

## **Creating a Border File**

1. Select **Start > All Programs > Intergraph SmartSketch > SmartSketch** 2. Select **File** > **Properties** > **Summary** tab, and verify the **Normal.igr** template file was used.
2. Select the **Units** tab, specify the following Unit and Precision for each readout, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs49 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Sheet Setup**.
2. On the Sheet Setup dialog, select the **Size and Scale** tab.
3. For the Sheet size, select Standard, **E Wide(44in x 34in),**  and select **OK**.
4. Select **File > Open**.
5. On the **Open** dialog, browse to the **C:\ClassMaterials** folder, and select **MicroStation (*.dgn)** as the file type.

*9.*  Select** border1.dgn**, and then select** Open**. *The MicroStation file will open and* *display in SmartSketch as Document2.*

50 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Window** > ** Tile Horizontally **to display both files on the screen.
2. Select **Edit** > ** Select All** to select all the graphics in the MicroStation file.
3. Select **Edit** > ** Copy **to copy the graphics from the MicroStation file.
4. Select the SmartSketch **Document1** file to make it active.
5. Select **Edit** > ** Paste** to paste the graphics.

SmartPlant P&ID Setup and Customization Course Labs51 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Position the graphics on the sheet.

**Note:**

- The **Move/Copy** command on the **Change** Toolbar can be used to move the border file inside the Sheet.
1. Close the SmartSketch **Document2** file; MicroStation file.
2. Zoom in and place a fence around the **INTERGRAPH** logo to select the graphics, and then select **Delete**.
3. On the **Draw** Toolbar, select the **Text Box**

command and key in **CUSTOM**

**CLASS** to replace the logo.

1. Right-click on the text box, and select **Properties**.
2. On the **Paragraph** tab, use **Intergraph ANSI** font size **.50 in** or another font and size of your choice.
3. Select **File > Save**.
4. In the **Save As** dialog box, browse to **C:\PPM_Site\Custom\P&ID Reference** **Data\Template Files**, and in the File name field, key in **CustClassEsize**. Select **Save**. ** **

52 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File** > ** Exit** to exit the **SmartSketch** application.

**Note:**

- If prompted to save changes to Document2, select **No**.

## **Creating a PID Template File**

1. Select **Start > All Programs > Intergraph SmartPlant P&ID > SmartPlant** **P&ID**.
2. Select **File** > **New** **Template**.
3. Select **File** > **Page** **Setup**.
4. On the Page Setup dialog box, select **E (34in x 44in)** for the sheet size, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs53 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Properties**.
2. Select the **Units** tab, specify the following Unit and Precision for each readout, and then select **OK**.

**Note:**

- The Unit and Precision settings should match those of the .igr border file created in SmartSketch.

54 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Tools > Options**.
2. Select the **Files** tab, select **1:1** **in** for the Select scale, and then select **OK**.
3. Select **Edit** > **Insert** > **Object**.
4. On the **Insert Object** dialog box, uncheck the **Link** checkbox, and then select **Browse**.

SmartPlant P&ID Setup and Customization Course Labs55 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Browse to **C:\PPM_Site\Custom\P&ID Reference Data\Template Files**, select **CustClassEsize.igr**, and then select **Open**.
2. On the **Insert Object** dialog box, select **OK**.
3. Position the border (SmartFrame) in the center of the template.
4. Select the border (SmartFrame), right-click and select **Properties**.

56 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **SmartFrame Properties > Info** tab, select **DrawingBorder** for the Layer, uncheck the **Use photographic style scale** checkbox, and then select **OK**.
2. From **Catalog Explorer** > **Symbols** > **Design**, select the **Title Block Label – E**

**Size** symbol.

SmartPlant P&ID Setup and Customization Course Labs57 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Position and place the title block label, **Title Block Label – E Size**, into the template.
2. Select **File > Save**.
3. In the **Save As** dialog box, browse to **C:\PPM_Site\Custom\P&ID Reference** **Data\Template Files**, and in the File name field, key in **CustomClassEsize**.

Select **Save**. ** **

**Note:**

- You can configure additional settings in the template file, and whenever drawings are created utilizing this template, those drawings will have identical settings. For example, you can prevent selection of inserted objects using the **View > Properties > Display** tab, and configure grid settings using the **View > Properties > Grid** tab. ** **

---

58 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Exit**.

**Note:**

- If prompted to save changes to CustomClassEsize, select **Yes**.

**Creating a Drawing Using the New Template**

1. Select **Start > All Programs > Intergraph SmartPlant P&ID > Drawing** **Manager**.
2. Open the **Custom** plant, select **Area1 > Unit1A**.
3. Select **File > New Drawing**, enter the following information for the new drawing, and then click **OK**.

**Note:**

- Make sure to select the **CustomClassEsize** template just created.
1. Double-click on **TestDrawing1** to open, and then verify that the border displays and the title block label is updated with the drawing name and number.
2. Select **File > Exit** to close the drawing and Drawing Manager.

SmartPlant P&ID Setup and Customization Course Labs59 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 7 – Migrating a SmartSketch Drawing**

***(Optional Lab)***** **

**Objective:** To migrate a SmartSketch drawing into a SmartPlant P&ID drawing in the Custom plant.

1. Select **Start > All Programs > Intergraph SmartPlant P&ID > Drawing** **Manager**
2. Open the **Custom** plant, select **Area1 > Unit1A**.
3. Select **File > New Drawing**, enter the following information for the new drawing, and then click **OK**.
4. Double-click on **SSKtoSPPID** to open.
5. Select** File > Import > SmartSketch**.
6. On the SmartSketch to P&ID Migration Wizard, select **Next**.

60 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Generate Symbol Map** dialog box, select **Generate a new symbol map,** and then select** Next**.
2. On the **Select File To Migrate** dialog box, select **Browse** and browse to the **C:\ClassMaterials** folder, select **Migrator.igr**, and then select **Open**.
3. Verify the path to the SmartSketch file, and then select **Next**.

SmartPlant P&ID Setup and Customization Course Labs61 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Finish** to start the Migration process. *The software will create a temporary* *SmartSketch file called **GetSmart.igr** with the graphics to migrate.*
2. From Windows Explorer, browse to the **C:\Users\Admin\AppData\Local\Temp** folder, and open the **GetSmart.log** file. *Any errors during the migration process* *are written to this file.*
3. From Windows Explorer, browse to the **~\SmartPlant\P&ID Workstation\Bin** folder. * *
4. Open and review the **SymbolMap.csv** file in Microsoft Excel. * *
5. Open and review the **ConnectorMap.csv** file in Microsoft Excel. * *
6. Open and review the **RotationMap.csv** file in Microsoft Excel.
7. In SmartPlant P&ID, using the **Polygon Fence Locate**

> Polygon
> 

command, draw a fence around the entire graphics in the drawing.

1. Select **Move/Copy**, and move the graphics to the middle of the drawing.
2. Select **File > Exit** to close the drawing and SmartPlant P&ID.

62 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 8 – Cloning an Existing Symbol (TEMA)**

**Objective:** To create a new symbol in the Custom plant by cloning an existing symbol and modifying the graphics.

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols** > **Equipment > Heat Transfer Equipment**

**> TEMA Shell and Tube > Shells**, select the **TEMA Shell Type E** symbol in the List View.

1. With the **TEMA Shell Type E** symbol selected, right-click and select **Clone**.
2. Select the cloned symbol, **Clone of TEMA Shell Type E(1),**  right-click and select **Rename**.

SmartPlant P&ID Setup and Customization Course Labs63 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Rename the cloned symbol to **TEMA Shell Type E – Dashed**.
2. Double-click on **TEMA Shell Type E – Dashed** to open it.
3. Select the two lines on the inside of the symbol.
4. On the **Style** pull-down menu, select **Dashed** to change both lines to a dashed line style.
5. The modified, cloned symbol should be like the following image.
6. Select **File > Save** to save the symbol.
7. Select **File > Exit** to exit Catalog Manager.

64 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Open SmartPlant P&ID, and then open **TestDrawing1**.
2. Place the **TEMA Shell Type E – Dashed** symbol in the drawing.
3. From **Catalog Explorer** > **Symbols** > **Equipment > Heat Transfer Equipment**

**> TEMA Shell and Tube > Front Ends**, select the **Front End Type A** symbol and connect it to the front end of the shell.

1. From **Catalog Explorer** > **Symbols** > **Equipment > Heat Transfer Equipment**

**> TEMA Shell and Tube > Rear Ends**, select the **Rear End Type M** symbol and connect it to the front end of the shell.

1. The connected symbols should be like the following image.
2. Select **File > Exit** to close the drawing and SmartPlant P&ID.

SmartPlant P&ID Setup and Customization Course Labs65 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 9 – Cloning an Existing Symbol (Vessel)**

**Objective:** To create a new symbol in the Custom plant by cloning an existing symbol and modifying the properties and graphics.

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols** > **Equipment > Vessels > Vertical Drums**, select the **Short 1D1C 1to1** symbol in the List View.
3. With the **Short 1D1C 1to1** symbol selected, right-click and select **Clone**.
4. Select the cloned symbol, **Clone of Short 1D 1C 1to1(1)**, right-click and select **Rename**.
5. Rename the cloned symbol to **Short 1D 1C 1to1 with Base**.
6. Double-click on the cloned symbol to open it.
7. Select **Tools > Options > View** tab, modify the Grid spacing to **0.10 in**, and then select **OK**.
8. In the **Properties** Window, modify the **AABBCC Code** to **1B2G01**, and for the **Construction By** property, select **By Contractor**.
9. Select the **Graphics** tab.
10. Select the **bottom arc** on the vessel, and then select **Edit > Delete**.
11. From the **Draw** Toolbar, select the **Line**

command.

1. On the **Style** pull-down menu, select **Normal** and draw a skirt on the vessel like the following image.

**Note:**

- You may have to turn off the **Snap Grid** to place the lines.

66 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Icon** tab.

**Note:**

- After selecting the **Icon** tab, the graphics of the symbol are copied to represent the icon. You can also use the drawing tools to draw the icon you want to associate with the symbol. ** **
1. Select **File > Save** to save the symbol.
2. Select **File > Exit** to exit Catalog Manager.
3. Open SmartPlant P&ID, and then open **TestDrawing1**.
4. Place the **Short 1D 1C 1to1 with Base** symbol in the drawing, and then place some **Nozzles** and **Trays** on it.

SmartPlant P&ID Setup and Customization Course Labs67 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 10 – Creating a New Symbol (Piping**

**Component)**

**Objective:** To create a new piping component symbol in the Custom plant using the symbol guidelines.

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols** > **Piping > Valves > 4 Way**, right-click in the List View, and select **New Item**.
3. In the List View, select **New Item**, right-click and select **Rename**.
4. Rename the new symbol to **4-Way Piping Valve**.
5. From **Catalog Explorer**, select the **File** pull-down menu, and then select **Open**.
6. In the **Properties** Window, change the item type to **Piping Component**.

68 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. In the **Properties** Window, enter the required properties like the following image.
2. Select the **Graphics** tab, and then select **Tools > Options** > **View** tab.
3. Modify the Grid spacing to **0.10 in**, and then select **OK**.
4. From the **Draw** Toolbar, select the **Rectangle** command, and then draw the graphic in the following image.

SmartPlant P&ID Setup and Customization Course Labs69 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **View > Grid Snap**, and turn off the grid snap.
2. On the **Catalog Tools** Toolbar, select the **Place Point**  command.
3. From the **Place Point** **Ribbon**, select **Piping Point**.
4. Select the location (left side of the symbol) where the first connect point (piping point) will be created.
5. Orient the dashed line to represent the appropriate connection angle for the first piping point.

**Note:**

- The software displays a dynamic dashed line representing the connection of the new connect point. You can also type the exact angle value in the **Connect angle** field to define the connection angle.
1. After the connection angle is correct, click again to place the connect point.
2. Repeat steps 15-17 to continue adding the piping points in the order of Right, Top, and Bottom, and assign the appropriate connection angle to each piping point.

**Note:**

- The piping connect points must be collinear with the origin of the symbol to trim the pipe line properly when placed in a drawing.
1. Hold down the **Ctrl** key, and select the **Heat** **Trace** tab to view both the **Graphics** and **Heat** **Trace** tabs. Verify the **Heat** **Trace** tab is **Bold** (active).
2. From the **Draw** Toolbar, select the **Line/Arc Continuous** command, and then draw the heat tracing graphic in the following image.

70 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Icon** tab, and delete the connect points.
2. Select the **Graphics** tab.
3. Select **File > Save** to save the symbol.
4. Select **File > Exit** to exit Catalog Manager.
5. Open SmartPlant P&ID, and then open **TestDrawing1**.
6. Route a horizontal and a vertical pipe run (Primary Piping).
7. Place the **4-Way Piping Valve** on the horizontal pipe run.
8. Place the **4-Way Piping Valve** on the vertical pipe run.
9. Select the horizontal and vertical pipe runs, select **FA** for the **Heat Trace** **Medium**, and then verify the heat trace graphics’ location on the valve.
10. Select **File > Exit** to close the drawing and SmartPlant P&ID.

SmartPlant P&ID Setup and Customization Course Labs71 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 11 – Creating Viewable Labels**

**Objective:** To create a new description label for equipment in the Custom plant using the Smart Text Editor within Catalog Manager.

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols > Equipment > Labels – Equipment >** **Descriptions**, right-click in the List View, and select **New Item**.
3. In the List View, select **New Item**, right-click and select **Rename**.
4. Rename the new symbol to **Equipment Description**.
5. Select **Equipment Description**, and double-click to open.
6. In the **Properties** Window, change the item type to **Label: Catalog Item**.
7. On the **Catalog** **Tools** Toolbar, select the **Set Item Type** command.
8. On the **Set Item Type** dialog box, select **Equipment**, and then select **OK**.
9. In the **Properties** Window, enter the required properties like the following image.
10. Leave the **Graphics** tab empty (blank), except for the origin

; there will be

no graphics for the label.

72 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Hold down the **Ctrl** key, and select the **Label** tab to view both the **Graphics** and **Label** tabs. Verify the **Label** tab is **Bold** (active).
2. From the **Catalog** **Tools** Toolbar, select the **Smart Text Editor** command.
3. On the **Smart Text Editor** dialog box, define the values like the following image.
4. Select **Insert** **Field** to enter the Description property in the **Text** field.
5. To modify the text, select the **Text** in the **Text** field, and then select the **Text** **Font** button. Modify the text as desired, and then select **OK**.
6. Select the **NULL** text box, right-click and select **Properties**.

SmartPlant P&ID Setup and Customization Course Labs73 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Define the **Justification** and **Text** **Alignment** values like the following image, and then select **OK**.
2. Select **View > Grid Snap**, and turn off the grid snap.
3. **Move** the **Text** **Box** to the center of the origin.
4. Select the **Icon** tab, double-click on the **NULL** text, highlight the text, and then key in **DESC**.

74 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Save** to save the symbol.
2. Select **File > Exit** to exit Catalog Manager.
3. Open SmartPlant P&ID, and then open **TestDrawing1**.
4. Place an equipment vessel on the drawing, and then place the **Equipment** **Description** label on the vessel.
5. In the **Properties** Window, define a value for the description property.
6. Select **File > Exit** to close the drawing and SmartPlant P&ID.

SmartPlant P&ID Setup and Customization Course Labs75 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 12 – Creating a Revision Label**

**Objective:**  To create a label in the Custom plant which can be placed in a drawing template to display drawing revisions.

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols > Design**, right-click in the List View, and select **New Item**.
3. In the List View, select **New Item**, right-click and select **Rename**.
4. Rename the new symbol to **Title Block Revision Label**.
5. Select **Title Block Revision Label**, and double-click to open.
6. In the **Properties** Window, change the item type to **Label: Catalog Item**.
7. On the **Catalog** **Tools** Toolbar, select the **Set Item Type** command.
8. On the **Set Item Type** dialog box, select **Drawing**, and then select **OK**.

**Note:**

- In the **Properties** Window, the** Labeled Item Type **property is defined.
1. In the **Properties** Window, for the **Label Type**, select **Title Block**.

76 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Save**.
2. Select **View > Grid Snap**, and turn off the grid snap.
3. Select **Tools** > **Options** > **Reference** **Files** tab.
4. For the **Select scale** option, select **1:1 in**, and then select **OK**.
5. Select **Insert** > **Object**, browse to **C:\PPM_Site\Custom\P&ID Reference** **Data\Template Files**, select the **E-Wide.igr** file, and then select **Open**.
6. On the **Insert Object** dialog box, uncheck the **Link** checkbox, and select **OK**.
7. Move the **E-Wide.igr** file to the correct position, like the following image. *It is* *important to think about where the .igr file will be moved to with respect to the* *origin symbol.*

SmartPlant P&ID Setup and Customization Course Labs77 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Insert > Title Block Field** to display the **Place Label Ribbon** Bar.
2. On the **Place Label Ribbon** Bar, select the values in the following image to place a text box on the symbol sheet which displays the first **Major Revision Number**.

**Notes:**

- Select **Display** **Label** **Names**

to view the label names in the text box.

- Select **More**

to display more options to format the label.

1. Place the **Text Box** on the symbol. *The origin of the Text Box is Left Top.*

**Note:**

- To view or edit the XML text behind the label, select the label and click **Smart Text Editor**. If you edit the text, be careful not to change any of the XML code strings. ** **
1. Press the ESC key to cancel the command.
2. Select and move/resize the **Text Box** to fit within the **REV** field.
3. Select **Insert > Title Block Field** to display the **Place Label Ribbon** Bar.

78 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Place Label Ribbon** Bar, select the values in the following image to place a text box on the symbol sheet which displays the **Revision Date** of the first revision.
2. Place the **Text Box** on the symbol. *The origin of the Text Box is Left Top.*
3. Press the ESC key to cancel the command.
4. Select and move/resize the **Text Box** to fit within the **DATE** field.
5. Repeat steps 22 – 26 to continue building the first row of the Title Block Revision label. Select the values in the following images to place text boxes on the symbol sheet which displays **Created By**, **Checked By**, and **Description** for the first revision.
6. After completing the steps above, the first row of the symbol will be like the following image.
7. Repeat steps 22 – 26 to continue building the second row of the Title Block Revision label. Select the values in the following images to place text boxes on the symbol sheet (above the previous text boxes) which displays **Major Revision** **Number, Revision Date,**  **Created By**, **Checked By**, and **Description** for the next revision. *The Function Argument will be incremented by 1.*
8. After completing the steps above, the second row of the symbol will be like the following image.

SmartPlant P&ID Setup and Customization Course Labs79 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Note:**

- To adjust the text, select the **Text** **Box**, right click and select **Properties**, and then edit the **Text** **Alignment** fields.
1. Select the inserted **E-Wide.igr** border** **file, and then select** Delete**.
2. Select the **Icon** tab, and draw how the icon is to appear in the Catalog Explorer of SmartPlant P&ID and Catalog Manager.
3. Select **File > Save** to save the symbol.
4. Select **File > Exit** to exit Catalog Manager.
5. From Drawing Manager, select **TestDrawing1**.
6. Select **Revisions** > **New** **Revision**, enter information for the revision like the following image, and select **OK**.
7. Select **OK** again, and then select **Close**.
8. Repeat steps 36 – 38, and enter information to create 4 additional revisions.
9. Select **Revisions > Revision History**, select **Properties** to review and/or edit the revisions, and then select **Close**.

80 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Open SmartPlant P&ID, and then open **TestDrawing1**.
2. From Catalog Explorer, select the **Title** **Block** **Revision** **Label**, and place it in the appropriate position in the drawing.
3. Select **File > Close** to close the drawing.
4. Select **File > Open**, select **TestDrawing1**, and then select **OK**. *The **Title Block***

***Revision** **Label** is updated.*

- 
    - 
1. Select **File > Exit** to close the drawing and SmartPlant P&ID.
2. From **Windows Explorer**, browse to **C:\PPM_Site\Custom\P&ID Reference** **Data\Template Files**, and double-click on **E-Size.pid** file to open.
3. From **Catalog Explorer** > **Symbols > Design**, select the **Title** **Block** **Revision** **Label**, and place it in the appropriate position in the template.

SmartPlant P&ID Setup and Customization Course Labs81 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Save**.
2. Select **File > Exit**.
3. From Drawing Manager, open the **Custom** plant, and select **Area1 > Unit1A**.
4. Select **File > New Drawing**, enter the following information for the new drawing, and then click **OK**.
5. Select **TestDrawing2**, and select **Revisions > New Revision**, and enter information for the new revision.
6. Double-click on **TestDrawing2** to open.
7. Verify the information for the revision is displayed in the drawing.
8. Select **File > Exit** to close the drawing and SmartPlant P&ID.

82 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 13 – Creating a Parametric Black Box**

**Objective:** To create a new parametric Black Box in the Custom plant.

**Creating the Symbol in the Catalog**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols > Equipment > Black Box System**, right-click in the List View, and select **New Item**.
3. In the List View, select **New Item**, right-click and select **Rename**.
4. Rename the new symbol to **New Black Box**.
5. Select **New Black Box** and double-click to open.
6. In the **Properties** Window, change the item type to **Equipment: Other**.
7. In the **Properties** Window, enter the required properties like the following image.
8. Select **File > Save**.

SmartPlant P&ID Setup and Customization Course Labs83 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **Setting Drawing Options**

1. Select **Tools** > **Maintain** **Relationships**, and make sure that a check mark appears beside the command.
2. Select **Tools > SmartSketch…**
3. On the **SmartSketch Settings > Relationships** tab, check all the relationships, and then select **OK**.
4. Select** Tools **>**  Customize**.
5. On the **Toolbars** tab > **Categories**, select **Draw**.
6. Drag the **Point** button

to the right side of the Toolbar region.

1. Under **Categories**, select **Relations**.
2. Drag the **Lock** button

to the right side of the Toolbar region, and then click

**Close** to close the Customize dialog box.

1. Select **View** > ** Toolbars**, select the** Label** Toolbar, and then select **OK**.
2. Select **Tools > Layer Groups**.
3. Under **Layers**, key in **Construction**, and press **Enter**.
4. Under **Layers**, key in **Dimension**, press **Enter**, and then select **OK**.

84 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Tools** > ** Layers**, and then select the pull-down menu to verify both layers exist.

**Note:**

- These two layers allow you to work in the background to specify aspects of the parametric symbol. When the new symbol is complete, these layers will be turned off so the driving dimensions and construction objects of the symbol do not appear in the graphic or icon of the symbol. ** **
1. Select **File** > **Save**.

## **Drawing the New Symbol**

1. On the **Layers** Toolbar > **Layer** field, select **Default**.
2. Ensure the **Graphics** tab is active.
3. On the **Draw** Toolbar, select **Line/Arc Continuous**

.

1. Use the origin as the center, and draw four connected lines to form a square around the origin.

**Note:**

- The software will place horizontal and vertical relationship handles on each new line.
1. On the **Layers** Toolbar > **Layer** field, select **Construction**.

SmartPlant P&ID Setup and Customization Course Labs85 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Move the origin symbol

away from the symbol graphics.

**Notes:**

- Do not create dimensions off the origin symbol. The origin symbol is deleted during file save, and any dimensions created with respect to the origin symbol will be deleted as well.
- Delete or move the origin symbol temporarily, when you save the symbol the origin will embed itself.
1. On the **Draw** Toolbar, select **Line/Arc Continuous**

, and draw a line through

the center of the symbol.

1. Select the **Lock**

command.

1. Select the midpoint (center) of the line to lock it.
2. Select the **Esc** key to exit this command and switch to the **Select** tool.

**Note:**

- Locking the point that was added to the center of the symbol assures that the point will not move when the box is resized in SmartPlant P&ID, and the construction line is necessary for adding dimensions to the box later.
1. Select **File** > **Save**.

## **Adding Dimensions to the Symbol**

1. On the **Layers** Toolbar > **Layer** field, select **Dimension**.
2. On the **Label** Toolbar, select **Distance Between**

.

86 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the left vertical line at the **end** **point**

.

1. Select the construction line at the **mid**p**oint**

.

1. Move the pointer past the top of the symbol, and click to place the first dimension.

**Note:**

- As you move the pointer, the dimension dynamically follows your

movement.

1. On the **Label** Toolbar, select **Distance Between**

.

1. Select the construction line at the **midpoint**

.

1. Select the right vertical line at the **end** **point**

.

1. Move the pointer past the top of the symbol, and click to place the second dimension.

SmartPlant P&ID Setup and Customization Course Labs87 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Label** Toolbar, select **Distance Between**

.

1. Select the top horizontal line at the **end point**

.

1. Select the construction line at the **midpoint**

.

1. Move the pointer past the right of the symbol, and click to place the third dimension.

88 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Label** Toolbar, select **Distance Between**

.

1. Select the construction line at the **midpoint**

.

1. Select the** **bottom horizontal line of the symbol at the** end** **point**

.

1. Move the pointer past the right of the symbol, and click to place the fourth dimension.
2. Select **File** > **Save**.

**Adding Variables and Equations to the Symbol**

1. Ensure that no elements are currently selected, and select **Fit**

.

**Note:**

- If all the dimensions are not displayed when the Variable Table is displayed, you may not see all the dimensions in the Variable Table.
1. Select **Tools** > ** Variables** to display the Variable Table.

**Notes:**

- The dimensions, added to the symbol, will display in a tabular format.
- Moving the cursor over a **Dim** in the Variable Table will highlight the dimension on the symbol.

SmartPlant P&ID Setup and Customization Course Labs89 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. In the last row of the Variable Table, enter the **Name** and **Value** information in the following image to define 4 variables to tie to the dimension variables.
2. In the **Formula** column for each dimension, enter the information in the following image to define an equation to determine the behavior of that dimension in relation to the variables defined; create a relation between the **Dim** and **Var**.

**Note:**

- Adding a value of 0.1 to the variable for each dimension guarantees that the sides of the box cannot be resized to a value of 0.
1. To test the equations for the parametric symbol:
2. Change the **Value** for the **Bottom** variable to **.60**.
3. Change the **Value** for the **Top** variable to **.60**.
4. Change the **Value** for the **Right** variable to **.30**.
5. Change the **Value** for the **Left** variable to **.30**.
6. Select **Undo**

four times to return the dimensions to their original values.

1. Select **File > Save**.
2. On the **Variable Table**, select **Close**

.

1. **Move** the origin

to the center of the symbol.

1. Select **File > Save**.
2. On the **Layers** Toolbar > **Layer** field, select **Default**.

90 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Layers** Toolbar > **Layer** field, select **Layer Display**.
2. On the Layer Display dialog box, select **Construction** and **Dimension** to hide the layers, select **Apply**, and then select **Close**.

**Note:**

- If you do not turn off the display of the **Construction** and **Dimension** layers, the construction line and dimensions will appear as part of the parametric symbol graphic and icon in SmartPlant P&ID.
1. Select the **Icon** tab, and delete any relationship handles.
2. Select the **Graphics** tab to return to the symbol graphics.
3. Select **File > Save**.
4. Select **File > Exit**.
5. Select **Start > All Programs > Intergraph SmartPlant P&ID > Drawing** **Manager**.
6. Open the **Custom** plant, select **Area1 > Unit1A**, and open** TestDrawing1**.
7. Select and place the **New Black Box** symbol in the drawing, and stretch the symbol using the yellow parametric handles.

SmartPlant P&ID Setup and Customization Course Labs91 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 14 – Creating a Parametric Pump**

***(Optional Lab)***** **

**Objective:** To create a new parametric pump in the Custom plant.

**Creating the Symbol in the Catalog**

1. Select **Start > All Programs > Intergraph** **SmartPlant Engineering Manager**

> Catalog Manager.
> 
1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols > Equipment >Mechanical** > **Pumps**, right-click in the List View, and select **New Item**.
3. In the List View, select **New Item**, right-click and select **Rename**.
4. Rename the new symbol to **Parametric Pump**.
5. Select **Parametric Pump** and double-click to open.
6. In the **Properties** Window, change the item type to **Equipment:** **Mechanical**.
7. In the **Properties** Window, enter the required properties like the following image.
8. Select **File > Save**.

92 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

## **Setting Drawing Options**

1. Select **Tools** > **Maintain** **Relationships**, and make sure that a check mark appears beside the command.
2. Select **Tools > SmartSketch…**
3. On the **SmartSketch Settings > Relationships** tab, check all the relationships, and then select **OK**.
4. Select** Tools **>**  Customize**.
5. On the **Toolbars** tab > **Categories**, select **Relations**.
6. Drag the **Lock** button to the right side of the Toolbar region, and then click **Close** to close the Customize dialog box.
7. Select **View** > ** Toolbars**, select the** Label** and **Change** Toolbars, and then select **OK**.
8. Select **Tools > Layer Groups**.
9. Under **Layers**, key in **Construction**, and press **Enter**.
10. Under **Layers**, key in **Dimension**, press **Enter**, and then select **OK**.
11. Select **Tools** > ** Layers**, and then select the pull-down menu to verify both layers exist.

**Note:**

- These two layers allow you to work in the background to specify aspects of the parametric symbol. When the new symbol is complete, these layers will be turned off so the driving dimensions and construction objects of the symbol do not appear in the graphic or icon of the symbol. ** **
1. Select **File** > **Save**.

SmartPlant P&ID Setup and Customization Course Labs93 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **Drawing the New Symbol**

1. On the **Layers** Toolbar > **Layer** field, select **Default**.
2. Ensure the **Graphics** tab is active.
3. Move the origin symbol

away from the symbol graphics.

**Notes:**

- Do not create dimensions off the origin symbol. The origin symbol is deleted during file save, and any dimensions created with respect to the origin symbol will be deleted as well.
- Delete or move the origin symbol temporarily, when you save the symbol the origin will embed itself.
1. Select **View > Grid Snap** and turn grid snap on.
2. On the **Draw** Toolbar, select **Circle by Center Point**

, and draw a circle with a

**1.50 in** Radius.

**Note:**

- The origin of the circle is the original location of the origin. ** **
1. On the **Layers** Toolbar > **Layer** field, select **Construction**.
2. On the **Draw** Toolbar, select **Line/Arc Continuous**

, and then drag the cursor

over the circle to find the origin of the circle.

94 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Route the line from the center to the right.
2. Select the **Esc** key, and then route the line from the center to the left.
3. On the left side of the circle, **select** and **delete** the **Intersection** relationship.

SmartPlant P&ID Setup and Customization Course Labs95 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. From the **Change** Toolbar, place the **Equal**

and **Colinear**

relationships

on the two lines.

**Note:**

- Placing these relationships on the lines 90 degrees to the circle element will drive the diameter.
1. From the **Change** Toolbar, add the **Perpendicular**

relationship to the

construction line on the left.

1. On the **Draw** Toolbar, select **Line/Arc Continuous**

, pause the cursor over the

horizontal construction line until the **end** **point**

relationship displays, then

select the horizontal construction line and draw a vertical construction line from the center of the circle 0.75” at 270 degrees.

96 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. From the **Change** Toolbar, select the **Perpendicular**

relationship, select the

vertical construction line and then the right horizontal construction line.

1. On the **Draw** Toolbar, select **Line/Arc Continuous**

, pause the cursor over the

vertical construction line until the **end** **point**

relationship displays, then select

the vertical construction line and route the horizontal construction line to the left of the circle.

1. Using **Line/Arc Continuous**, pause the cursor over the vertical construction line until the **end** **point**

relationship displays, then select the vertical construction

line and route the horizontal construction line to the right of the circle.

1. On the right side of the circle, **select** and **delete** the **Intersection** relationship.

SmartPlant P&ID Setup and Customization Course Labs97 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. From the **Change** Toolbar, place the **Equal**

and **Colinear**

relationships

on the two bottom lines.

1. Select a **line**, right-click and select **Properties**, and then verify it is on the Construction layer.
2. Repeat step 19 and verify all lines inside the circle are on the Construction layer.
3. Make sure that no lines are selected, and on the **Layers** Toolbar > **Layer** field, select **Default**.
4. On the **Draw** Toolbar, select **Line/Arc Continuous**

, pause the cursor over the

lower left horizontal construction line until the **end** **point** relationship

displays, then select the lower left horizontal construction line and route a line 1.22” at 270 degrees.

1. Using **Line/Arc Continuous**, pause the cursor over the lower right horizontal construction line until the **end** **point**

relationship displays, then select the

lower right horizontal construction line and route a line 1.22” at 270 degrees.

98 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. From the **Change** Toolbar, select the **Perpendicular**

relationship, select the

left leg and then the lower left horizontal construction line.

1. Select the right leg and then the lower right horizontal construction line.

**Note:**

- Connecting the lines to the circle element forces the lines to follow the element shape.
1. From the **Change** Toolbar, place the **Equal**

relationship to the legs of the

pump.

SmartPlant P&ID Setup and Customization Course Labs99 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Draw** Toolbar, select **Line/Arc Continuous**

, pause the cursor over the

left vertical leg until the **end** **point**

relationship displays, then select the

vertical leg and route a line 0.25” at 0 degrees.

1. Using **Line/Arc Continuous**, pause the cursor over half of the foot that is already drawn until the **end** **point**

relationship displays, then select the half of the foot

and route a line 0.25” at 180 degrees.

1. From the **Change** Toolbar, place the **Connect**

relationship between the leg

and the second side of the foot. Be sure that you receive the **end** **point** relationship when you highlight the leg. (There is already a connect relationship with the first side because you paused for the end point indicator when routing.) 30. From the **Change** Toolbar, place the **Equal**

and **Colinear**

relationships

on the two halves of the left foot.

1. From the **Change** Toolbar, select the **Perpendicular**

relationship, select the

left leg and then the left half of the left foot. Select the left leg and then the right half of the left foot.

1. Repeat steps 27 through 31 to draw the foot on the right leg.

100 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. From the **Change** Toolbar, place the **Equal**

relationship to a segment of each

foot.

**Note:**

- This will keep all lines making up the feet equal since there is already an equal relationship on the two halves of each foot.

## **Adding Dimensions to the Symbol**

1. On the **Layers** Toolbar > **Layer** field, select **Dimension**.
2. On the **Label** Toolbar, select **Distance Between**

, select the vertical

construction line, and then select the horizontal construction line.

**Note:**

- Before selecting the vertical or horizontal construction line, remember to pause until you receive the **end** **point**

relationship.

1. On the **Label** Toolbar, select **Distance Between**

, select the lower horizontal

construction line, and then select the foot of the pump.

**Notes:**

- Before selecting the horizontal construction line or the leg, remember to pause until you receive the **end** **point**

relationship.

- This is the main driving dimension for the handle parameter – Bottom.
1. On the **Label** Toolbar, select **Distance Between**

, select the left end of the foot,

and then select the right end of the foot.

SmartPlant P&ID Setup and Customization Course Labs101 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Notes:**

- Before selecting either end of the foot, remember to pause until you receive the **end** **point**

relationship.

- A fixed dimension needs to be defined to prevent random alteration.

**Adding Variables and Equations to the Symbol**

1. Ensure that no elements are currently selected, and select **Fit**

.

**Note:**

- If all the dimensions are not displayed when the Variable Table is displayed, you may not see all the dimensions in the Variable Table.
1. Select **Tools** > ** Variables** to display the Variable Table.

**Notes:**

- The dimensions, added to the symbol, will display in a tabular format.

102 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

- Moving the cursor over a **Dim**, dimensional relationship, in the Variable Table will highlight the dimension on the symbol.
1. In the last row of the Variable Table, enter the **Name** and **Value** information in the following image to define 4 variables to tie to the dimension variables.
2. In the **Formula** column, enter the information in the following image to create a relation between the **Dim** and **Var**.
3. On the **Variable Table**, select **Close**

.

1. At the center of the circle, add a **Lock**  to the top end of the vertical line.

**Note:**

- The Lock relationship fixes all movement about this point.
1. Select **File > Save**.
2. **Move** the origin

to the center of the symbol.

SmartPlant P&ID Setup and Customization Course Labs103 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Layers** Toolbar > **Layer** field, select **Default**.
2. On the **Layers** Toolbar > **Layer** field, select **Layer Display**.
3. On the Layer Display dialog box, select **Construction** and **Dimension** to hide the layers, select **Apply**, and then select **Close**.
4. Select the **Icon** tab, and delete any relationship handles.
5. From the **Change** Toolbar, select **Relationship Handles**

to toggle the

relationship handles off.

104 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Graphics** tab to return to the symbol graphics.
2. Select **File > Save**.
3. Select **File > Exit**.
4. Select **Start > All Programs > Intergraph SmartPlant P&ID > Drawing** **Manager**.
5. Open the **Custom** plant, select **Area1 > Unit1A**, and open** TestDrawing1**.
6. Select and place the **Parametric Pump** symbol in the drawing, and stretch the symbol using the yellow parametric handle.

**Note:**

- For this example, the symbol must be adjusted in **Catalog** **Manager**. The circle element moves left or right but does not change size (diameter), as required. It is necessary to further specify the relationships between the elements using construction lines, dimensions, and the relationship

handles.

SmartPlant P&ID Setup and Customization Course Labs105 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 15 – Creating a New Select List and**

## **Property**

**Objective:**  To create a new select list property for paint code for ALL Equipment in the Custom plant using Data Dictionary Manager.

**Creating the Paint Code Select List**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Data Dictionary Manager**.

1. Open the **Custom** plant.
2. Select the **Select** **List** button.
3. Scroll down to the bottom of the select list, click in the **Name** field, and enter the information in the following image.
4. Select the **Select** **Entry**

button, click in the **Value** field, and enter the

information in the following image.

106 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Add** **Row**

button to add another row of data to the **Paint** **Code**

Select List, and enter the information in the following image.

1. Select **Sort**

, sort the values in **Ascending** order, and then select **OK**.

1. Select **File** > **Save**.

**Creating the Paint Code Property in the Equipment**

## **Table**

1. Select the** Database** **Tables** button.
2. Select** **the** Equipment** table, and then select **Edit** > **Add** **Property**.
3. In the **Add Property** dialog box, enter the information from the following image, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs107 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Save**.
2. Select **File > Exit**.

**Creating an Equipment Label Utilizing the Paint**

## **Code Property**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols > Equipment > Labels - Equipment**, select the **Cleaning Req** symbol** **in the List View.
3. With the **Cleaning Req** symbol selected, right-click and select **Clone**.
4. Select the cloned symbol, **Clone of Cleaning Req(1),**  right-click and select **Rename**.
5. Rename the cloned symbol to **Paint Code**.
6. Double-click on **Paint Code** to open it.
7. Select the **Label** tab, and then select the text, **CC1**.

108 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Smart Text Editor**.
2. On the **Smart Text Editor** dialog box, select and delete the text for the Cleaning Requirements.
3. In the **Property** field, select **PaintCode**, select **Insert Field**, and then select **OK**.
4. Select **File > Save**.
5. Select **File > Exit**.
6. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
7. Place three equipment vessels, and define a different **PaintCode** for each (**Blue**, **Green**, and **Orange**) in the **Properties** Window.
8. Place the **Paint** **Code** label on the equipment vessels to display the **PaintCode** property value.
9. Select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs109 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 16 – Working with Properties in Data**

## **Dictionary Manager**

**Objective:** To learn how to turn off the display of a property, change the display name of a property, and modify permissions of a property in the Custom plant.

**Turning Off the Display of a Property**

1. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
2. Route a **Pipe** **Run**, and in the **Properties** Window, note the **Estimated** **Length** and the **MOC Class** properties.
3. Exit **SmartPlant P&ID**.
4. Open **Data Dictionary Manager**.
5. Select the **Database Tables** button, and scroll down to the **Pipe Run** table.
6. Double-click the **EstimatedLength** property, select **No** for the **Display to User**, and then select **OK**.
7. Select **File** > **Save**.

**Changing the Display Name of a Property**

1. Select the **Database Item Types** button.
2. Select the **PipeRun** Item Type, and then select **Edit** > **Properties**.
3. On the **Modify PipeRun Properties** dialog box, select the

**MaterialOfConstClass** property.

1. In the** Display Name **column,**  **select** MOC Class** and key in** Material of** **Construction Class**, and then select **OK**.

110 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File >**  **Save**.

## **Modifying Permissions of a Property**

1. Double click the **Vessel** Item Type, and note the **EquipmentSubclass** property is **Write Catalog**.
2. Select **Cancel**.
3. Double click the **PipingComp** Item Type.
4. Modify the permissions on the **ConstructionStatus** property to **Read-Only Both**, and then select **OK**.
5. Select **File** > **Save**.
6. Select **File > Exit**.

## **Testing the Changes**

1. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
2. Select the **Pipe** **Run**, and verify the **Estimated Length** property does not display in the **Properties** Window, and the display value of MOC Class changed to **Material of Construction Class**.
3. Select the **Vessel** in the drawing, and verify the value for **Equip Subclass** cannot be changed.
4. Select **Tools > Options > Placement** tab, make sure the **Default construction** **status** is set to **New**, and select **OK**.
5. Place a Piping Valve on the drawing, verify the **Construction** **Status** property value is set to **New**, and verify the value cannot be changed.

SmartPlant P&ID Setup and Customization Course Labs111 *** ***

*SmartPlant P&ID Setup and Customization Course Labs* **Bonus Lab**

1. In **Data Dictionary Manager**, create a new category for the **Properties** Window by editing the **Property** **Category** Select List.
2. Change the **MaterialOfConstClass** property for **Pipe Runs** to the new Category.

112 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 17 – Adding Properties to Drawings and**

## **Plant Groups**

**Objective:** To add new properties to the Custom plant and to drawings.

## **Adding Properties to Drawings**

1. Open **Data Dictionary Manager**.
2. Select the **Database Tables** button, and then select **Drawing**.
3. Select **Edit** > ** Add Property**.
4. In the **Add Property** dialog box, enter the information in the following image, and then select **OK**.
5. Select **Edit** > ** Add Property**.
6. In the **Add Property** dialog box, enter the information in the following image, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs113 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **File > Save**.
2. Select **File > Exit**.
3. Open **Options Manager** > **Settings** view.
4. Add the **CheckedBy** and **CheckedDate** properties to **Drawing Properties –**

**Optional**.

1. Select **File > Save**.
2. Select **File > Exit**.
3. Open **Drawing Manager**, select **File > New Drawing**, enter the information in the following image, and then select **OK**.
4. In **Drawing Manager**, select **TestDrawing3**, and then select **Edit > Properties**.
5. On the **Properties** dialog box, verify the **Checked By** and **Checked Date** properties are optional drawing properties, and then select **Cancel**.

114 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

## **Adding Properties to the Plant**

1. Open **SmartPlant** **Engineering** **Manager**.
2. Select the **Custom** plant.
3. Select **Tools** > **Data** **Dictionary** **Manager**.
4. Select the **Database Tables** button, and then select **Plant**.
5. Select **Edit >Add Property**.
6. On the **Add Property** dialog box, enter the information in the following image, and then select **OK**.
7. Select **File > Save**.
8. Select **OK** to the following message about restarting SmartPlant Engineering Manager.
9. Select **File > Exit** to exit from Data Dictionary Manager.
10. From **SmartPlant** **Engineering** **Manager**, select **File > Open**.
11. Browse to the **C:\PPM_Site\INI** folder, select the **smartplantv4.ini** file, and then select **Open**.
12. Select the **Custom** plant, and then select **Edit > Properties**.
13. In the **Job Number** field, key in **1234**, and then select **OK**.
14. Select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs115 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 18 – Creating New Filters for Display Sets**

**Objective:** To create a new display filter that displays only pumps supplied By Owner in the Custom plant.

1. Open SmartPlant P&ID, and then open **TestDrawing1**.
2. From **Catalog Explorer > Symbols** > **Equipment** > **Mechanical** > **Pumps**, select **Pump** in the List View, and place it in the drawing.
3. From **Catalog Explorer > Symbols** > **Assemblies** > **Equipment**, select **Pump03.pid** in the List View, place it in the drawing, and then select **OK**.
4. Select **Pump03.pid** in the List View again, place it in the drawing, and then select **OK**.
5. Select the two pumps in the first assembly placed using the **Ctrl** key.
6. In the **Properties** Window, using a Select Set, select **By Owner** for the **Supply** **By** property.
7. Select the **Esc** key on the keyboard to de-select the pumps.
8. Select **View > Apply Display Set**.
9. Select the **Custom** folder.
10. Select the **Add Display Set**

command.

1. Highlight **New DisplaySet1**, and key in **Pumps By Owner**.

116 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Add Filter**

command.

1. From the **Plant Folders**, select **Display Filters**, right-click and select **Add** **Folder**, and then key in **Pumps**.
2. Select the **Pumps** folder, and then select **New**.
3. Select **Simple filter**, and then select **OK**.
4. On the **Add Filter** dialog box, enter the information in the following image, and then select **OK**.
5. On** **the** Select Filter** dialog box, select **OK**.
6. On the **Apply** **Display** **Set** dialog box, select Green for the color of the **Pumps By** **Owner**, ** **select Gray for the color of the** Background Items**, select** Apply**, and then select** OK**.

SmartPlant P&ID Setup and Customization Course Labs117 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Notice that only pumps with a **Supply** **By** of **By** **Owner** should be displayed in Green and all other items are displayed in Gray.
2. Select **View > Clear Display Set**.
3. Select **File > Exit** to close the drawing and SmartPlant P&ID.

118 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 19 – Customizing Options Manager**

**Objective:**  To customize symbology and gapping in Options Manager for the Custom plant, and then update the drawings.

1. Open **Options** **Manager**, and review the **Symbology** and **Gapping**.
2. Select **File > Exit**.
3. Open **Drawing Manager**, select **File > New Drawing**, enter the information in the following image, and then select **OK**.
4. In **Drawing Manager**, double-click **TestDrawing4** to open.
5. From **Catalog Explorer > Symbols** > **Equipment** > **Vessels** > **Vertical Drums**, select **1D1C 2to1** in the List View.
6. Place three equipment vessels, and define a different **Construction Status** for each (**New**, **Existing**, and **Future**) in the **Properties** Window.
7. Select **Tools > AutoGap**, and make sure that a check mark appears beside the command.
8. From **Catalog Explorer > Symbols** > **Piping** > **Routing** > **Process Lines**, select **Primary Piping** in the List View, and route several lines in the horizontal and vertical direction, and make sure to cross over the lines. * *

**Note:**

- The vertical Primary Piping will gap the horizontal Primary Piping as defined in **Options Manager > Gapping**.
1. Select **File > Exit**.
2. From **Drawing Manager**, select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs119 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Open **Options** **Manager** and change the color for **Equipment - New**, **Equipment**
- **Future**, and **Equipment - Existing**.
1. Change the **Gapping Style** for Primary Piping (Horizontal and Vertical).
2. Change the priority of when Horizontal Primary Piping crosses Vertical Primary Piping.
3. Select **File > Save**.
4. Select **File > Exit**.
5. Open **Drawing Manager.**
6. Select **View** > **Customize Current View**.
7. From the list of **Drawing** **properties**, scroll down and select **Out-of-Date** **Drawing Status**, select **Add**, and then select **OK**.

**Note:**

- If the drawing is Out-of-Date**,**  a symbol will be displayed in the List View next to the drawing.
1. Select **Tools** > **Out-of-Date Drawing Criteria**.
2. Select all the checkboxes, and then select **OK**.
3. Select Area1 > Unit1A, and then select **File** > ** Out-of-Date Drawings **>**  Report**.
4. Notice that an **X** is displayed in the **Gapping** and **Symbology** columns.
5. **Exit** the report, and then select **Don’t Save**.
6. Select the drawings in the List View using the **Shift** or **Ctrl** keys.
7. Select **File** > **Out-of-Date** **Drawings** > **Update**, review the dialog, resolve any missing symbols, and then select **OK**.

120 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Update Drawings** dialog box, select **View Log,** close the Update Drawings log file**,**  and then select **Close**.
2. Double-click on **TestDrawing4**, and notice that the items reflect the symbology and gapping changes made in **Options Manager**.

**Note:**

- Any new drawings created will read the latest changes in **Options** **Manager**, and **Update** will not be required on these drawings unless any changes are made after the drawings were created.
1. Select **File > Exit**.
2. From **Drawing Manager**, select **File > Exit**.

## **Bonus Lab**

1. In **Options** **Manager**, reset the values in **Symbology** and **Gapping** to their original values.
2. Run **Update** on ALL the drawings.

SmartPlant P&ID Setup and Customization Course Labs121 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 20 – Implementing Jacketed Pipe**

**Objective:**  To modify a piping component and configure Options Manager settings to implement Jacketed Pipe in the Custom plant.

**Creating a Jacket for a Piping Component**

1. Open **Catalog** **Manager**.
2. From **Catalog Explorer >**  **Symbols** > **Piping** > **Valves** > **2** **Way** **Other**, double-click **Blank Gate Valve** to open.
3. Select **Tools** > **Maintain** **Relationships**, and turn off Maintain Relationships.
4. Select **View > Grid Snap**, and turn off the grid snap.
5. Hold down the **Ctrl** key, and select the **Jacket** tab to view both the **Graphics** and **Jacket** tabs. Verify the **Jacket** tab is **Bold** (active).
6. From the **Draw** Toolbar, select the **Line/Arc Continuous** command, and draw a line on the bottom of the valve to represent the Jacket.

**Note:**

- The distance between the center of the valve and the Jacket = .12”
1. Select the **Jacket**, and then select the **Mirror/Copy** command on the **Change** Toolbar to copy and mirror the Jacket to the top of the valve.

122 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Graphics** tab to view both the **Graphics** and **Jacket** tabs. Verify the **Graphics** tab is **Bold** (active).
2. On the **Catalog Tools** Toolbar, select the **Place Point**  command.
3. From the **Place Point** **Ribbon**, select** Auxiliary Point**.
4. Select the left end of the top Jacket line where the first auxiliary point will be created.
5. Orient the dashed line upward to represent the appropriate connection angle for the first auxiliary point.
6. After the connection angle is correct, click again to place the connect point.
7. Repeat steps 11-13 to add the second auxiliary point to the right end of the top Jacket line.
8. Select the left end of the bottom Jacket line to add the third auxiliary point, orient the dashed line downward, and then click again to place the connect point.
9. Select the right end of the bottom Jacket line to add the fourth auxiliary point, orient the dashed line downward, and then click again to place the connect point.

**Note:**

- The Auxiliary Points will enable the placement of jacketed nozzles on the valve.
1. Select **File > Save**.
2. Select **File > Exit**.

## **Enabling Jacketing**

1. Open **Options** **Manager > Settings**, and for the **Heat Tracing Media - Jacketed** **Pipe** setting, select **SSJ**.
2. For the **Pipe Jacket Nominal Diameter Configuration File**, verify that the path and filename, **JacketNDCoreND.XML**, are specified.

SmartPlant P&ID Setup and Customization Course Labs123 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Tools** > **Pipe Jacket Nominal Diameter, select Add Row,** enter the information in the following image, select **Save**, and then select **Close**.
2. Select **File > Save**.
3. Select **File > Exit**.
4. Open **Drawing Manager**, and then double-click **TestDrawing1** to open.
5. Select the pipe run.
6. In the **Properties** Window, select **1”**  for **Nominal Diameter**, and select **SSJ** for **Heat Trace Medium**.

**Notes:**

- The pipe run will become jacketed, and the **Properties** Window will expose the **Piping Jacket** properties with a prefix of **J_**.
- You will no longer assign values to the regular insulation properties and specifications; you must assign those values to the properties with a prefix of **J_** which apply only to a jacketed pipe run.

124 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. From **Catalog Explorer >**  **Symbols** > **Piping** > **Valves** > **2** **Way** **Other**, select **Blank Gate Valve**, and place it on the jacketed pipe run.
2. From **Catalog Explorer >**  **Symbols** > **Piping** > ** Fittings** > **Flanges** **and** **Unions**, select **Jacket** **Nozzle (Valve)**, and then connect two of them to the top of the valve.
3. Select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs125 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 21 – Creating New Rules**

**Objective:** To work with Rule Manager using the Custom plant and gain an understanding of how the rules work.

1. Open **Rule Manager**, and edit an existing rule in **Plant** **Rules** > **Free** **Standing** to make it illegal to place piping components in space.
2. Select **File > Save**, and leave **Rule Manager** open.
3. Open **Drawing Manager**, and double-click on **TestDrawing1** to open.
4. From **Catalog Explorer > Symbols > Piping > Valves > 2 Way Common**, select **Ball Valve** and try to place it in the drawing.
5. Select **File > Exit**.
6. In **Rule Manager**, edit an existing rule in **Plant** **Rules** > **Relationship** > **Piping** to display an error when the **Piping** **Materials** **Class** changes at a branch.
7. Select **File > Save**, and leave **Rule Manager** open.
8. Open **Drawing Manager**, and double-click on **TestDrawing1** to open.
9. From **Catalog Explorer > Symbols > Piping > Routing > Process Lines**, select **Primary Piping**.
10. Route the **Primary Piping** horizontally, and then route a vertical branch off the horizontal pipe run.
11. Select the horizontal pipe run, and for the **Piping** **Materials** **Class**, key in 1C0031.

**Note:**

- Both the horizontal pipe run and the vertical branch will highlight indicating that both pipe runs will receive the value defined for the **Piping** **Materials Class**. For testing, you must turn off **System Editing**.
1. Select **Tools > System Editing**, and turn off **System Editing** for testing purposes.
2. Select the vertical pipe run (branch), and for the **Piping** **Materials** **Class**, key in 1C0033.

**Note:**

- Only the vertical pipe run (branch) highlights.

126 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Press enter on the Piping Materials Class field, and notice the inconsistency is displayed as an Error which is represented by an **X**.
2. Select **Tools > System Editing**, and turn ON **System Editing**.
3. Select **File > Exit**.
4. In **Rule Manager**, edit the **Process Pipe Run to Nozzle** rule in **Plant** **Rules** > **Relationship** > **Piping** to copy cleaning requirements from the nozzle to the pipe run, and display an error if this rule is violated. Remember that rules are invoked at placement time.
5. Select **File > Save**, and leave **Rule Manager** open.
6. Open **Drawing Manager**, and double-click on **TestDrawing1** to open.
7. From **Catalog Explorer > Symbols > Equipment > Vessels > Vertical Drums**, select **1D 1to1**, and place it in the drawing.
8. From **Catalog Explorer > Symbols > Equipment Components > Nozzles**, select **Flanged Nozzle**, and place it on the vertical drum.
9. Select the nozzle.
10. In the **Properties** Window, for **Cleaning Requirements**, select **CC1**.
11. Route **Primary Piping** from the nozzle, and verify that the **Cleaning** **Requirements** property value copies to the pipe run.
12. Select the pipe run.
13. In the **Properties** Window, for **Cleaning Requirements**, select **CC2**, and verify the inconsistency is displayed between the nozzle and pipe run as an Error which is represented by an **X**.

SmartPlant P&ID Setup and Customization Course Labs127 *** ***

*SmartPlant P&ID Setup and Customization Course Labs* 27. Select **File > Exit**.

1. In **Rule Manager**, reset all the changes made in this lab exercise.
2. Select **File > Save**.
3. Select **File > Exit**.
4. Open **Drawing** **Manager**.
5. Select ALL the drawings in the List View using the **Shift** or **Ctrl** keys.
6. Select **File** > **Out-of-Date** **Drawings** > **Update**, review the dialog, resolve any missing symbols, and then select **OK**.
7. On the **Update Drawings** dialog box, select **Close**.
8. Select **File > Exit**.

128 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs* **Lab 22 – Review of Existing Rules**

**Objective:** To review rules by selecting each tab in the Rule Manager interface to understand what is being defined.

1. Open **Rule Manager**, and then select and open the **Plant Rules >**  **Free** **Standing**

> No Freestanding Equip Comp rule.
> 
1. How does this rule prohibit placing equipment components in space?
2. Select and open the **Plant Rules >**  **Implied** **Items** > **Piping** **Vent/Drain** **Detail** **2**

rule.

1. How does the filter work for this item?
2. What symbols are implied by placing these Macro components in a drawing?
3. Select and open the **Plant Rules >**  **Label** **Placement** > **Equipment** **Label** rule.
4. What tab in this rule only allows Equipment Labels to be placed on Equipment?
5. Select and open the **Plant Rules >**  **Relationship** > **Equipment** **Component** > **Nozzle** **to** **Equipment** rule.
6. Why do nozzles orient themselves outside the geometry of the equipment?
7. Select and open the **Plant Rules >**  **Relationship** > **Piping** > **Piping** **Comp** **To** **Process** **Pipe** **Run** rule.
8. What tab controls the data that is copied from item to item at placement?

SmartPlant P&ID Setup and Customization Course Labs129 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 23 – Creating Buried Pipe**

**Objective:** To create a symbol for a new line style representing buried pipe which will be used to import the pattern and style into SmartPlant P&ID. Also, to create a new symbol for placement that utilizes the new line style.

**Creating a Symbol for the New Line Style in Catalog**

## **Manager**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer**, right-click on **Symbols**, and select **New** to create a new folder.
3. Right-click on **New Category**, select **Rename**, and key in **Linear Styles DO**

**NOT USE**.

1. Select the **Linear Styles DO NOT USE** folder.
2. In the List View, right-click and select **New Item**.

130 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Right-click **New Item**, select **Rename**, and then key in **B Linear Style Buried** **Pipe**.

**Note:**

- This symbol is **only** used to define the Point Style, Linear Pattern and Linear Style; it is not the symbol that will be placed in the drawing.
1. Select **B Linear Style Buried Pipe**, and** **double-click to open**. **
2. Select the **Graphics** tab.
3. From the **Draw** Toolbar, select the **Text Box**

command, and then select the

**Origin**.

1. Key in **B** for the value, and then press the **Esc** key.
2. Select the **B**, right-click and select **Properties.**
3. Select the Justification and Text alignment from the following image, and then select **OK**.

## **Installing the Line Style Editor**

1. Select **Tools > Add-Ins…**  (the **Add-in Manager** dialog will appear).
2. Select the **Browse** button and browse to the ~**\SmartPlant\Engineering** **Manager\bin** folder.
3. Select the **igrseaddin420.dll** file

SmartPlant P&ID Setup and Customization Course Labs131 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. The **Line Style Editor** will be added to the list of Available add-ins in the Add-in Manager dialog.
2. Select the checkbox next to Line Style Editor to place a checkmark in the box.
3. Select **OK**.
4. Select **View > Toolbars…**
5. In the Toolbars dialog under Toolbars, scroll to the bottom of the list.
6. Select the checkbox next to Line Style Editor to place an ‘X’ in the box.
7. The **Line Style Editor** will now display in **Catalog Manager**.

## **Creating a Point Style**

1. From the **Line Style Editor**, select **Point Styles**, and then select the **Create** **New** **Style**

command.

1. On the **Create New Point Style** dialog box, key in **B Point Style**, and then select **OK**.
2. On the **Point Style Properties** dialog box, key in **Point Style for Buried Pipe**, and then select **OK**.

## **Defining the Point Style Graphics**

1. From the **Line** **Style** **Editor > Point Styles**, select **B Point Style**.
2. In the Design Window, select the **B**.

132 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the **Define Point Style Graphics**

command.

1. Drag the target over the **B** and click.
2. The B Point Style will be displayed in the **Preview**.

## **Creating a Linear Pattern**

1. From the **Line Style Editor**, select **Linear Patterns**, and then select the **Create** **New Style** command.
2. On the **Create New Linear Pattern** dialog box, key in **B Linear Pattern**, and then select **OK**.
3. On the **Linear Pattern Properties** dialog box, enter the information in the following image for the first Stroke index.
4. The dashes will be displayed in the **Preview**.
5. On the same dialog box, select **2** for the **Stroke index**.
6. Enter the information in the following image for the second Stroke index, notice the **Preview**, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs133 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. The **B Linear Pattern** will be listed under **Linear Patterns**.

## **Creating a Linear Style**

1. From the **Line Style Editor**, select **Linear Styles**, and then select the **Create** **New Style** command.
2. On the **Create New Linear Style** dialog box, key in **Buried Pipe**, and then select **OK**.
3. On the **Linear Style Properties** dialog box, enter the information in the following image, notice the **Preview**, and then select **OK**.

134 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. The **Buried Pipe** will be listed under **Linear Styles**.

## **Testing the Linear Style**

1. From the **Draw** Toolbar, select the **Line** command.
2. On the **Ribbon** Toolbar, select **Buried Pipe** for the Style.
3. Route a line in the horizontal and vertical directions, and verify the style.

SmartPlant P&ID Setup and Customization Course Labs135 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select and delete the horizontal and vertical lines.
2. Select **File > Save**.
3. Select **File > Exit**.

**Note:**

- If prompted to save changes to **B Linear Style Buried Pipe.sym**, select **Yes**.

**Importing the Linear Pattern and Linear Style in**

## **Options Manager**

1. Select **Start > All Programs** > **Intergraph** **SmartPlant** **P&ID** > **Options** **Manager**.
2. Open the **Custom** plant.
3. Select **Tools** > **Linear Patterns**.
4. On the** Linear Patterns **dialog box, select** Import**.
5. Browse to the **C:\PPM_Site\Custom\P&ID Reference Data\Symbols\Linear** **Styles DO NOT USE** folder, select **B Linear Style Buried Pipe.sym**, and then select **Open**.
6. On the** Linear Patterns **dialog box, verify the B Linear Pattern was imported, and then select** Close**.

136 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Tools** > **Linear Styles**.
2. On the** Linear Styles **dialog box, select** Import**.
3. Browse to the **C:\PPM_Site\Custom\P&ID Reference Data\Symbols\Linear** **Styles DO NOT USE** folder, select **B Linear Style Buried Pipe.sym**, and then select **Open**.
4. On the** Linear Styles **dialog box, verify the Buried Pipe was imported, and then select** Close**.
5. Select **File** > **Save**.
6. Select **File** > **Exit**.

**Adding a New Pipe Run Type of Buried Pipe in the**

## **PID Data Dictionary**

1. Select **Start** **> All Programs** > **Intergraph** **SmartPlant** **Engineering** **Manager**

> Data Dictionary Manager.
> 
1. Open the **Custom** plant.
2. Select the **Select** **Entry** button.
3. From the **Selected list**, select **Line Type**.
4. Scroll down to the bottom of the Select List, click in the **Name** field, and key in **Buried Pipe**.
5. Click in the **Short Value** field, and key in **BP**.

**Note:**

- Adding this line type entry allows **Buried Pipe** to be filtered either through **Reports**, the **Design** **Window** or the **Engineering** **Data** **Editor**.
1. Select **File** > **Save**.
2. Select **File** > **Exi**t.

SmartPlant P&ID Setup and Customization Course Labs137 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Defining the Symbology for Buried Pipe in Options**

## **Manager**

1. Select **Start > All Programs** > **Intergraph** **SmartPlant** **P&ID** > **Options** **Manager**.
2. Open the **Custom** plant.
3. From **Symbology**, select the **Plant Filter** of **Hose – New**, and then select **Insert** **Row**.
4. In the blank row, select the **ellipsis** button to add a filter.
5. On the **Select** **Filter** dialog box, select the **Plant** **Folders > Symbology Filters** > **New** folder, and then select **New**.
6. On the **New** **Filter** dialog box, select **Simple filter**, and then select **OK**.
7. On the **Add Filter** dialog** **box, enter the information from the following image, and then select** OK**.

138 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Select** **Filter** dialog box, select **OK**.
2. For the **Color**, select **Blue**.
3. For the **Width**, select **0.35 mm**.
4. For the **Pattern**, select **B Linear Pattern**.
5. Select **File > Save**.
6. From **Symbology**, select the **Plant Filter** of **Hose – New**, and then select **Insert** **Row**.
7. In the blank row, select the **ellipsis** button to add a filter.
8. On the **Select** **Filter** dialog box, select the **Plant** **Folders > Symbology Filters** > **Future** folder, and then select **New**.
9. On the **New** **Filter** dialog box, select **Simple filter**, and then select **OK**.
10. On the **Add Filter** dialog** **box, enter the information from the following image, and then select** OK**.
11. On the **Select** **Filter** dialog box, select **OK**.
12. For the **Color**, select **Red**.
13. For the **Width**, select **0.18 mm**.
14. For the **Pattern**, select **B Linear Pattern**.
15. Select **File > Save**.
16. From **Symbology**, select the **Plant Filter** of **Hose – New**, and then select **Insert** **Row**.
17. In the blank row, select the **ellipsis** button to add a filter.
18. On the **Select** **Filter** dialog box, select the **Plant** **Folders > Symbology Filters** > **Existing** folder, and then select **New**.

SmartPlant P&ID Setup and Customization Course Labs139 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **New** **Filter** dialog box, select **Simple filter**, and then select **OK**.
2. On the **Add Filter** dialog** **box, enter the information from the following image, and then select** OK**.
3. On the **Select** **Filter** dialog box, select **OK**.
4. For the **Color**, select **Cyan**.
5. For the **Width**, select **0.18 mm**.
6. For the **Pattern**, select **B Linear Pattern**.
7. Verify the following three additional entries.

**Note:**

- Adding these entries will graphically depict **Buried Pipe** when placed in a drawing with the **Construction Status** of **New**, **Future** or **Existing**.
1. Select **File > Save**.
2. Select **File > Exit**.

**Creating Buried Piping in Catalog Manager**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Catalog Manager**.

1. Open the **Custom** plant.
2. From **Catalog Explorer** > **Symbols** > **Piping > Routing > Process Lines**, select the **Primary Piping** symbol in the List View.
3. With the **Primary Piping** symbol selected, right-click and select **Clone**.

140 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the cloned symbol, **Clone of Primary Piping** **(1)**, right-click and select **Rename**.
2. Rename the cloned symbol to **Buried Piping**.
3. Double-click on the cloned symbol to open it.
4. In the **Properties** Window, modify the **AABBCC Code** to **WM1B01**, and for the **Pipe Run Type** property, select **Buried Pipe**.
5. Select the **Icon** tab, and make any desired modifications.
6. Select **File > Save** to save the symbol.

**Note:**

- This symbol will be used when routing **Buried Pipe** in a P&ID drawing.
1. Select **File > Exit** to exit Catalog Manager.

**Routing Buried Piping in a P&ID Drawing**

1. Open **Drawing Manager**, and then double-click **TestDrawing1** to open.
2. From **Catalog Explorer > Piping > Routing > Process Lines**, select **Buried** **Piping**, and then route three individual pipe runs of Buried Piping.
3. Select each **Buried Piping**, and for the **Construction Status** property, select either **New**, **Existing** or **Future**.

**Note:**

- The **Default construction** **status** = **New**, and can be modified in the **Tools**

**> Options > Placement** tab.

1. From **Catalog Explorer > Piping > Labels – Piping Segments**, select **Construction Status** in the List View, and then place on each **Buried Piping**.
2. From **Catalog Explorer > Piping > Routing > Process Lines**, select **Primary** **Piping**, and then connect to each end of the **Buried Piping**.
3. Do you receive an inconsistency marker where the two pipe run types are connected? ( *Think of rules and filters.* )
4. Review the inconsistencies. ( *The connector endpoint is unattached*) 6. Exit the drawing, and then exit Drawing Manager.

SmartPlant P&ID Setup and Customization Course Labs141 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Editing the Process Pipe Run Rule in Rule Manager**

1. Open **Rule Manager** for the Custom plant.
2. From **Plant Rules** > **Relationship** > **Piping**, double-click on the** Process Pipe** **Run to Process Pipe Run** to open.
3. Select the **Items** tab, and notice the **Process Pipe Run** filter is being used.
4. Select **Browse**, and then select **Properties**.
5. On the **Filter Properties** dialog box, notice the **Ripe Run Type = Buried Pipe** is not listed in the **Definition** field.
6. Select **Add**, and from the **Edit Property** field, select the **Pipe Run Type =**

**Buried Pipe**, and then select **OK**.

1. Select **OK** again.
2. Select **Yes** to save your changes.
3. On the **Rule Properties** dialog box, select **OK**.
4. Select **File > Save**.
5. Select **File > Exit**.
6. Open **Rule Manager**, and notice the message, “**One or more rules did not load** **correctly.** ”

**Notes:**

- This message appears because other rules utilize the **Process Pipe Run** filter, and this filter was modified.
- If ALL the rules, which utilize this modified filter, are not addressed, the message, “**One or more rules did not load correctly**” will appear upon opening a drawing.
1. Select **OK**.
2. Select the **Plant Rules** folder, and then select **Edit > Approve All Rules**.
3. The message, “**Do you want to approve all rules?** ”, will appear.
4. Select **Yes** to approve and refresh all the rules which utilize the **Process Pipe** **Run** filter.

## **OR**

142 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **No** to individually review and approve each rule marked as disabled and indicated with a

.

1. Right-click on the disabled rule, and then select **Properties**.
2. On the **Rule Properties** dialog box, select the **Items** tab. ** **
3. Click in the **Name** field for the **Process Pipe Run** filter indicating **Filter** **has been modified**. ** **

---

1. Select **OK**. ** **
2. Repeat these steps for each disabled rule. ** **
3. Select **File > Save**.
4. Select **File > Exit**.

**Updating a Drawing and Reviewing Inconsistencies**

1. Open **Drawing Manager**.
2. Right-click on **TestDrawing1**, select **Out-of-Date Drawings > Update**, and then select **OK**.
3. On the **Update Drawings** dialog box, select **Close**.
4. Double-click on **TestDrawing1** to open.
5. Route **Primary Piping** on the opposite end of each **Buried Piping**.
6. Review and address the inconsistencies between the **Primary Piping** and the **Buried Piping** by implementing one of the following:
- **Approve** the inconsistency

## **OR**

SmartPlant P&ID Setup and Customization Course Labs143 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

- **Copy** the value from **Item** **1** to **Item** **2**

## **OR**

- **Copy** the value from **Item** **2** to **Item** **1**

## **OR**

- **Place** a **Construction Status** Segment Break Label
1. On the other end of each **Buried Piping**, disconnect the **Primary** **Piping** from the **Buried** **Piping** and reconnect.
2. Review and address the inconsistencies between the **Primary Piping** and the **Buried Piping**.
3. Select **File > Exit**.
4. Select **File > Exit** to exit Drawing Manager.

144 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 24 – Creating and Using a New Format**

**Objective:** To create a stream number label with leading zeros for pipe runs using the Custom plant.

## **Creating a New Format**

1. Select** Start > All Programs > Intergraph SmartPlant Engineering Manager **

**> Format Manager**.

1. Select **String**, and then select **Edit > Add Format**.
2. On the **Add Format** dialog box, for the **Name** field, key in **A10**.
3. Select** Insert Field**.
4. On the **Field Properties** dialog box, enter the information on the following image, and then select **OK**.
5. The** Add Format** dialog box, **Format mask** field will display 10 zeros.
6. Select **OK**.
7. Select **File** > ** Save**.
8. Select **File** > **Exit**.

SmartPlant P&ID Setup and Customization Course Labs145 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Creating a New Symbol Utilizing the New Format**

1. Select **Start > All** **Programs** > ** Intergraph SmartPlant Engineering Manager **

> ** Catalog Manager**.
> 
1. From **Catalog Explorer >**  **Symbols** > **Piping** > **Labels - Piping Segments**, select **Stream Number** in the List View.
2. Right-click on **Stream Number**, and select **Clone**.
3. Select the cloned symbol, **Clone of Stream Number** **(1)**, right-click and select **Rename**.
4. Rename the cloned symbol to **Stream Number A10**.
5. Double-click on the cloned symbol to open it.
6. In the **Properties** Window, for **Placement Type**, select **Two Point**.
7. Select **Tools** > **Options** > **View** tab, and set **Grid spacing** to **0.10 in**.
8. Select **Apply**, and then select **OK**.
9. Select the **Graphics** tab, delete the graphics, and then use the **rectangle** command on the **Draw** Toolbar to create the graphics shown in the following image.
10. Select the **Icon** tab, and create the graphics shown in the following image.
11. Select the **Label** tab.
12. Select the **Fit** command to fit the view.
13. In the **Design** **Window**, select the label.

146 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Smart Text Editor**, select the property in the Text field to edit the values, enter **A10** for the **Format**, select **Apply**, and then select **OK**.
2. In the **Design** **Window**, right-click on the label, and select **Properties**.
3. Define the desired Justification, Text alignment, Margins, etc., and then select **OK**.
4. With the **Label** tab selected, hold down the **Ctrl** key and select the **Graphics** tab.
5. Notice the label and the graphics of **Stream Number A10** are not aligned.
6. Move the label into the graphics.
7. Select **File** > ** Save**.
8. Select **File** > **Exit**.

## **Testing the Label**

1. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
2. Route **Primary Piping**, and then place the **Stream Number A10** Label on it.
3. Select the **Primary Piping**, and in the **Properties** Window, **Stream No** field, key in **123456**.
4. Select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs147 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **Bonus Lab**

**Objective:** To create a label to display both degrees, Fahrenheit and Celsius, for the Design Max Temperature property with the format of 150.00 F (65.56 C).

1. Open **Format Manager**, and add a new format, **Deg-FC**, for **Temperature**.
2. Select **Insert** **Field**, and enter **Precision = .01**, and **Primary = F**.
3. Select **Insert** **Text**, and enter “**(**“.
4. Select **Insert** **Field**, and enter **Precision = .01**, and **Primary = C**.
5. Select **Insert** **Text**, and enter “**)**”.
6. Save and Exit.
7. Open **Catalog** **Manager**, and create a new label for the **Design Max Temp** property using the new format.
8. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
9. Route Primary Piping, and key in **150** for the **Design Max Temp** property.
10. Place the label on the pipe run.
11. Exit the drawing.

148 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 25 – Creating and Using a New Insulation**

## **Specification**

**Objective:** To add entries to the Insulation Purpose Select List which will be used to create a new insulation specification in the Custom plant.

1. Select **Start > All** **Programs** > **Intergraph** **SmartPlant** **Engineering** **Manager**

> Data Dictionary Manager.
> 
1. Open the **Custom** plant.
2. Select the **Select List** button, and scroll down to the **Insulation Purpose** Select List.
3. Select the **Select Entry** button to open the **Insulation Purpose** Select List.
4. Scroll down to the bottom of the select list, click in the **Value** field, and enter the information in the following image.
5. Select **Add Row**
- ***from the Toolbar.
1. Click in the **Value** field, and enter the information in the following image.
2. Select **File > Save**.
3. Select **File > Exit**.
4. Select **Start > All Programs > Intergraph SmartPlant P&ID > Insulation** **Manager**.
5. Right-click on the **Urethane** folder, and select **Properties**.
6. For **Insulation density**, key in **10.0** lbm/ft^3, and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs149 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Right-click on the **Urethane** folder, and select **Add Specification**.
2. Select the **General** tab, and enter the information in the following image.
3. Select the **Piping** tab, and then select **Range Setup**.
4. On the **Piping** **Range** **Setup** dialog box, for **Nominal diameter**, select **1/8’’**, **2’’**, **4 ½’’**, **6’’**, **12’’**, **16’’** to get the **Resulting ranges** in the following image.
5. In the **Temperature** field, key in **100**, **250**, **350**, **450** and **600** pressing the Enter key after each entry to get the **Resulting ranges** in the following image.

150 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **OK**.
2. Enter the **Piping insulation thickness** information in the following image.
3. Select the **Equipment** tab, and then select **Range Setup**.
4. On the **Equipment** **Range** **Setup** dialog box, in the **Temperature** field, key in **100**, **250**, **350**, **450** and **600** pressing the Enter key after each entry to get the **Resulting ranges** in the following image.
5. Select **OK**.
6. Enter the **Equipment insulation thickness** information in the following image.

SmartPlant P&ID Setup and Customization Course Labs151 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **OK**.
2. Select **File > Save**.
3. Select **File > Exit**.
4. Open **SmartPlant P&ID**, and then open **TestDrawing1**.
5. Place any two equipment items, and route two pipe runs.
6. Place a valve on each pipe run.
7. Select one pipe run, and enter the following property values:
- **Nominal Diameter**: 4’’
- **Insulation Temp**: 300
- **Insulation Spec**: RS7188
1. Verify the insulation thickness, **Insulation Thk**, is set to **1’’**.
2. Select the other pipe run, and enter the following property values:
- **Nominal Diameter**: 4’’
- **Insulation Temp**: 700
- **Insulation Spec**: RS7188
1. Verify the message, “**The temperature or diameter value falls outside the** **range of the insulation specification. Please enter another value.** ”, appears.
2. Select **OK**, and notice the Insulation Spec property value is cleared.
3. Select one equipment, and enter the following property values:
- **Insulation Temp**: 300
- **Insulation Spec**: RS7188
1. Verify the insulation thickness, **Insulation Thk**, is set to **3’’**.

152 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select the other equipment, and enter the following property values:
- **Insulation Temp**: 400
- **Insulation Spec**: RS7188
1. Verify the insulation thickness, **Insulation Thk**, is set to **3’’**.
2. Select the **Insulation** **Thk** property, and enter **5”** .
3. Verify the property **Insulation** **Thk** **Source** changes from Software to **User**.
4. Select** File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs153 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 26 – Importing Data**

**Objective:** To import data from the Equipment List report into a SmartPlant P&ID

drawing in the Custom plant.

1. Open **SmartPlant P&ID**, and then open **TestDrawing3**.
2. Place any equipment vessel on the drawing.
3. Select the vessel, and enter the following property values:
- **Tag Prefix**: V
- **Tag Seq No**: 107
1. From **Catalog Explorer > Symbols >**  **Equipment > Labels - Equipment**, place the **Equipment ID** label on the vessel.
2. Place two **Generic 2 - Shell & Tube** heat exchangers on the drawing.
3. Select one heat exchanger, and enter the following property values:
- **Tag Prefix**: E
- **Tag Seq No**: 700
1. Select the other heat exchanger, and enter the following property values:
- **Tag Prefix**: E
- **Tag Seq No**: 800
1. Place the **Equipment ID** label on each heat exchanger.
2. Select **Reports > Plant Reports**, select **Equipment List**, and then select **OK**.
3. On the **Save Output As** dialog box, select **Save**.

**Note:**

- If prompted, select **Yes** to confirm replacing the Equipment List report. ** **
1. The **Equipment List** report opens in Excel.
2. Select Column **Q**, and then slide over to select Column **AD** simultaneously.

154 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Right-click and select **Unhide**.
2. Select Column **T** for each equipment, and verify that this relative path is valid for the plant. ( *The software will use this path to place the symbol if it does not exist* *in the database.* )
3. For each equipment, verify that the **Tag Prefix** in Column **Y** matches the prefix in Column **A** of the same row.
4. For each equipment, verify that the **Tag Seq No** in Column **Z** matches the sequence number in Column **A** of the same row.
5. If desired, select Columns **R** through **AC**, right-click and select **Hide**. ( *This is not* *a requirement for the import to work.* ) * *
6. For each equipment, enter a value for Column **G** (Materials of Construction), Column **I** (Piping Materials Class), and Column **K** (Heat Tracing Medium).
7. Save the changes and exit.
8. In **SmartPlant P&ID**, select **File > Import > Data File**, browse to the **C:\Users\Admin\My Reports\Output** folder, select **Equipment List.xlsm**, and then select **Open**.
9. In **Windows Explorer**, browse to the **C:\Users\Admin\AppData\Local\Temp** folder, open the **SPImport.log** and review for any errors.
10. In **SmartPlant P&ID**, select each equipment, and verify the imported data.

SmartPlant P&ID Setup and Customization Course Labs155 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 27 – Creating New Reports**

**Objective:** To create a new equipment list report for the Custom plant.

1. In **TestDrawing3**, select **Reports > New**, enter the information from the following image, and then select **OK**.
2. Select **Yes** to edit the report.
3. The report opens in **Excel**.
4. On the **Add-ins** tab, from the **SmartPlant Reports** Toolbar, select **Options**.
5. On the **Report Options** dialog box, define the various options for the report template, and then select **OK**.

---

1. For the header information, key in **Equipment List** for the title, and then key in the following column headings. ** **

**Equipment Number Equipment Name P&ID Number Material of Const** **Note:**

- The header information must be contained within the rows specified.

156 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. With the Excel functionality, define any cell formatting such as borders, text wrapping, etc.
2. On the **Add-ins** tab, from the **SmartPlant Reports** Toolbar, select **Define**.
3. On the **Define Report Contents** dialog box, select **Equipment**, and then select **Define**.
4. On the **Define Report Item > Properties** tab, for the **Selected properties**, select **Item Tag**, **Name**, and **Rep Drawing Name**.
5. Select the **Sort** tab, and for the **Sort properties**, select **Item Tag** and then select **OK**.

SmartPlant P&ID Setup and Customization Course Labs157 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Define Report Contents** dialog box, select **Close**.
2. In the Excel spreadsheet. select a cell under a column heading, and then from the **SmartPlant Reports** Toolbar, select **Map Properties**.
3. Map the appropriate properties (attributes) into the cells; selecting the appropriate property for each heading.

**Notes:**

- Map the properties below the rows defined as the header.
- The following headings and properties should be mapped:

o **Equipment Number** = Item Tag

o **Equipment** **Name** = Name

o **P&ID Number** = Rep Drawing Name

1. Select **File > Save**, and exit **Excel**.
2. In **TestDrawing3**, select **Reports > Plant Reports**, select **New Equipment List**, and then select **OK**.

158 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 28 – Reporting from a Drawing and**

## **Excluding Drawing Stockpile Items**

**Objective:** To run a report for a drawing and exclude items in the drawing stockpile using the Custom plant.

1. In **TestDrawing3**, select **Reports** > **Plant** **Reports** > **Equipment** **List**.
2. Uncheck the **Include items in drawing stockpile**, and select **OK**.
3. On the **Save Output As** dialog box, key in **Equipment List2.xlsm** for the **File** **name**, and then select **Save**.
4. Review the report, and then exit **Excel**.

SmartPlant P&ID Setup and Customization Course Labs159 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 29 – Reporting from the EDE**

**Objective:** To run a report from the Engineering Data Editor (EDE) using a drawing in the Custom plant.

1. In **TestDrawing3**, select** Equipment** in the **Engineering Data Editor**.
2. Select/activate the **Active Drawing**, **Active Drawing Stockpile**, **Stockpile**, and **Other Drawings** buttons.
3. From the EDE Toolbar, select the **View**

menu.

1. Select **Plant Reports**, select **Equipment List**, and then select **OK**.

**Note:**

- In the **EDE > Plant Reports** dialog box, there is not an option to include/exclude the stockpile items. To exclude the stockpile items, deselect/deactivate the **Stockpile** and **Drawing Stockpile** buttons.
1. Review the report, and then exit **Excel**.

160 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 30 – Editing a Report Template to Exclude**

## **Stockpile Items**

**Objective:** To edit a report template in the Custom plant to exclude the stockpile items.

1. In **TestDrawing3**, select** Reports **>**  Edit. **
2. Select **Equipment List**, and then select **Open**.
3. The report opens in **Excel**.
4. On the **Add-ins** tab, from the **SmartPlant Reports** Toolbar, select **Define**.
5. On the **Define Report Contents** dialog box, select **Equipment**, and then select **Define**.
6. On the **Define Report Item > Filter** tab, select **Browse**.

SmartPlant P&ID Setup and Customization Course Labs161 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Select Filter** dialog box, select **Properties**.
2. On the **Filter Properties** dialog box, select **Add**, select **Rep In Stockpile =**

**False**, and then select **OK**.

1. On the **Select Filter** dialog box, select **OK**.
2. On the **Define Report Item** dialog box, select **OK**.
3. On the **Define Report Contents** dialog box, select **Close**.
4. Select **File > Save**.
5. Exit the report, and then exit **Excel**.
6. Run the report from EDE, and verify that the items from the stockpile were excluded.

162 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 31 – Customizing the Report Header**

**Objective:** To edit a report template in the Custom plant, and add the Plant properties of Plant Name and Job Number to the Report Header.

1. In **TestDrawing3**, select** Reports **>**  Edit. **
2. Select **Equipment List**, and then select **Open**.
3. The report opens in **Excel**.
4. On the **Add-ins** tab, from the **SmartPlant Reports** Toolbar, select **Define**.
5. On the **Define Report Contents** dialog box, select **Equipment**, and then select **New**.
6. On the **New Items** dialog box, select **Plant Group**, and for the **Name**, key in **Plant Group Unit**.
7. Select **Apply**, and then select **Close**.
8. On the **Define Report Contents** dialog box, select **Plant Group Unit**, and then select **New**.
9. On the **New Items** dialog box, select **Plant Group**, and for the **Name**, key in **Plant Group Area**.
10. Select **Apply**, and then select **Close**.
11. On the **Define Report Contents** dialog box, select **Plant Group Area**, and then select **New**.
12. On the **New Items** dialog box, select **Plant Group**, and for the **Name**, key in **Plant Group Plant**.
13. Select **Apply**, and then select **Close**.

SmartPlant P&ID Setup and Customization Course Labs163 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the **Define Report Contents** dialog box, select **Plant Group Plant**, and then select **New**.
2. On the **New Items** dialog box, select **SubClass Plant**.
3. Select **Apply**, and then select **Close**.
4. The **Define Report Contents** dialog box will be like the following image.
5. On the **Define Report Contents** dialog box, select **Plant Group Plant**, and then select **Define**.
6. On the **Define Report Item > Properties** tab, for the **Selected properties**, select **Name**, and then select **OK**.
7. On the **Define Report Contents** dialog box, select **SubClass Plant**, and then select **Define**.
8. On the **Define Report Item > Properties** tab, for the **Selected properties**, select **Job Number**, and then select **OK**.
9. On the **Define Report Contents** dialog box, select **Close**.
10. Select **File > Save**.
11. Select **Cell A1**, and then from the **SmartPlant Reports** Toolbar, select **Map** **Properties**.
12. From **Equipment** > **Plant** **Group Unit** > **Plant Group Area > Plant Group** **Plant**, select **Name**.
13. Select **Cell A2**, and then from the **SmartPlant Reports** Toolbar, select **Map** **Properties**.
14. From **Equipment** > **Plant** **Group Unit** > **Plant Group Area > Plant Group** **Plant > SubClass Plant**, select **Job Number**.
15. Select **File > Save**.

164 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Exit the report, and then exit **Excel**.
2. In **TestDrawing3**, select** Reports **>**  Plant Reports. **
3. Select **Equipment List**, and then select **OK**.
4. On the **Save Output As** dialog box, key in **Equipment List4.xlsm** for the **File** **name**, and then select **Save**.
5. The report opens in **Excel**.
6. Review the report, verify that the Plant Name and Job Number displays, and then exit **Excel**.
7. In **TestDrawing3**, select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs165 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 32 – Creating Drawing Revisions**

**Objective:** To create revisions for a drawing in the Custom plant. ** **

1. Open **Drawing Manager**, and select **TestDrawing4**.
2. Select **Revisions > New Revision**.
3. On the **New Revision** dialog box, remove the time from **Revision Date**, enter the information in the following image, and then select **OK**.
4. Select **OK**, and then select **Close**.
5. Repeat steps 2 through 4 to create three additional revisions for the drawing. For each revision, assign values for the following:
- **Description**
- **Approved By**
- **Checked By**
- Remove the time from **Revision Date**
- **Major Revision**
- **Minor Revision**
- Check** Associate version **
1. Double-click **TestDrawing4** to open.
2. From **Catalog Explorer > Symbols** > **Design**, place **Drawing Revision Record**

**– D** in the drawing. ** **

1. **Exit** the drawing, **reopen** the drawing, and then verify the revision information.
2. Select **File > Exit**.

166 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 33 – Versioning Drawings**

**Objective:** To create and compare versions of a drawing using the Custom plant.

1. From **Drawing** **Manager**, double-click **TestDrawing4** to open.
2. Place an equipment vessel, and then **exit** the drawing.
3. Select **Revisions** > **New** **Version**.
4. On the **New Version** dialog box, key in **Added Vessel**, select **OK**, and then select **Close**.
5. Select **Revisions** > **Version** **History**.
6. On the **Version History** dialog box, select version 4, use the **Ctrl** key and select version 5, and then select **Compare**.
7. Become familiar with the commands on the **Compare** dialog box, and then **exit**.
8. On the **Version History** dialog box, select **Close**.

SmartPlant P&ID Setup and Customization Course Labs167 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 34 – Fetching a Deleted Drawing**

**Objective:** To delete a drawing in the Custom plant, and then fetch the deleted drawing.

1. Select and delete **TestDrawing4**, select **Yes** to confirm deletion, and then select **Close**.
2. Select **Custom**, and then select **Revisions > Fetch Deleted Drawing**.
3. Select **TestDrawing4**, select **OK**, and then select **Close**.
4. Select **Unit1A**, and verify that **TestDrawing4** was retrieved.

168 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 35 – Backing Up and Restoring a Plant**

**Objective**: To create a backup of the Custom plant, delete the plant structure, and then restore it to a site.

## **Backup the Plant**

1. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> SmartPlant Engineering Manager**.

1. Select the **Custom** plant.
2. Select **Tools > Backup**.
3. On the **Plant Structure Backup** wizard, verify that **Include Reference Data** is checked, and then select **Next**.
4. Select **Finish** to start the backup process.
5. Once complete, the message, “**The plant structure backup was successful.** ”, will appear.
6. Select **OK**.
7. From **Windows Explorer**, browse to **C:\PPM_Site\Backups**, double-click **Custom_p.zip** to view the files contained within the backup zip file.
8. Double-click **Export.log**, scroll to the end of the file, and notice the message,

“**Export terminated successfully without warnings.** ”.

1. **Exit** the file, and then exit **Windows Explorer**.

SmartPlant P&ID Setup and Customization Course Labs169 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Delete the Plant from the Site**

1. From** SmartPlant Engineering Manager**, select the** Custom** plant.
2. Select **Edit > Delete**.
3. On the **Delete Plant Structure** dialog box, select the information in the following image, and then select **OK**.
4. From **SmartPlant Engineering Manager**, verify the deletion of the **Custom** plant.

**Restore the Plant Backup to the Site**

1. From **SmartPlant Engineering Manager**, right-click on the **Plant Structures** node, and then select **Restore**.
2. In the **Restore Plant Structure** wizard, enter the information in the following image, and then select **Next**.

170 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. On the next dialog, keep the default selections, and then select **Next**.
2. On the next dialog, keep the default selections, and then select **Next**.
3. Review the information in the last dialog, and then select **Finish**.

SmartPlant P&ID Setup and Customization Course Labs171 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. After completion, the message, “**The restoration process was successful.** ”, will appear.
2. Select **OK**.
3. Exit **SmartPlant Engineering Manager**.
4. Open **Drawing Manager**, double-click **TestDrawing4**, and verify that a drawing can be opened in the restored plant.
5. **Exit** the drawing, and then exit **Drawing Manager**.

172 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 36 – Running Reference Data**

## **Synchronization Manager**

**Objective:** To synchronize reference data from the **Custom** Plant into the **501K**

Plant.

1. Select **Start** > **Programs** > **Intergraph** **SmartPlant** **Engineering** **Manager** > **Reference Data Synchronization Manager**.
2. Select **File > New Package**.
3. On the **New Package** dialog box, enter the information in the following image, and then select **OK**.
4. After completion, the message, “**The reference data package was created** **successfully.** ”, will appear.
5. Select **OK**.
6. In the **Source zipped package** field, select the RDS package created at the source plant.
7. For **Target plant name**, select the ellipsis button to navigate to the **SmartPlantv4.ini** file of the site that includes the relevant plant, and then from the **Target plant name** list, select the desired plant, **501K**.
8. Select **File** > **Compare**.

SmartPlant P&ID Setup and Customization Course Labs173 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. When the **Compare** is finished, review the compare results in the **Status and** **results** window.

## **Important**

- Create a plant backup from** SmartPlant Engineering Manager **before proceeding to the next steps.
1. Select **File** > **Synchronize**.
2. When the **Synchronize** is finished, review the synchronization results in the **Status and results** window.
3. Select **Tools** > **Create** **Report**.
4. **Exit** from **Reference Data Synchronization Manager**.

174 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 37 – Copying a Plant**

**Objective:** To copy the 501K plant and create a new plant utilizing the Copy Plant process which consists of Save Plant Structure, Load Plant Structure, and Finish Load Plant Structure Processing.

## **Save Plant Structure**

1. Open **SmartPlant Engineering Manager**, right-click the **501K** plant, and then select **Save Plant Structure**. ** **

---

1. In the **Save Plant Structure** dialog box, keep the default information, notice the location where the zip file will be saved, and then select **OK**.
2. After completion, the message, “**The plant structure was saved successfully.** ”, will appear. ** **

---

1. Select** OK**.**  **

SmartPlant P&ID Setup and Customization Course Labs175 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

## **Load Plant Structure**

1. Select the **Plant Structures** node, right-click and select **Load Plant Structure**.
2. In the **Load Plant Structure** wizard, browse to the location of the zip file created in the Save Plant Structure process, select **Open**, and then select **Next**.
3. Enter the information in the following image, and then select **Next**.
4. Keep the default selection of **SmartPlant P&ID** as the application to associate with the plant, and then select **Next**.

176 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. For the **Plant structure path**, key in

**\\SPPIDTRAINING\PPM_Site\502\Drawings**, and then select **Next**.

1. If the folder does not exist, a prompt will display. Select **Yes** to create the plant structure storage directory.
2. Keep the **Load Plant Structure** wizard open.
3. From **Windows Explorer**, open the **501K** folder, select the **P&ID Reference** **Data** folder, right-click and then select **Copy**.
4. Open the **502** folder, right-click and then select **Paste**.
5. **Close** Windows Explorer, and return to the **Load Plant Structure** wizard.

SmartPlant P&ID Setup and Customization Course Labs177 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. In the **Load Plant Structure** wizard, enter the information in the following image, and then select **Next**.
2. Keep the default username and tablespace information for the plant structure schema, and then select **Next**.
3. Keep the default username and tablespace information for the plant structure data dictionary schema, and then select **Next**.

178 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Keep the default username and tablespace information for the SmartPlant P&ID

schema, verify the **SmartPlant P&ID reference data path**, and then select **Next**.

1. Keep the default username and tablespace information for the SmartPlant P&ID

data dictionary schema, and then select **Next**.

1. Review the settings, select the Back button to make any corrections, and then select **Finish**.

SmartPlant P&ID Setup and Customization Course Labs179 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. After completion, the message, “**The plant structure has been loaded** **successfully.** ”, will appear. ** **

---

1. Select **OK**.
2. In **SmartPlant Engineering Manager**, expand the **502** plant, right-click the **Roles** node, and verify the role has Full Control privileges using the **Properties >** **Rights** tab. If this role does not exist, add one.
3. Select **File > Exit**.

## **Finish Load Plant Structure Processing**

1. Open **Drawing Manager**.
2. Select **File > Open Database**.
3. In the **Open Plant Structure** dialog, select **502**, and then select **Open**.
4. A **SmartPlant P&ID** dialog with the message, “**The plant has been locked as** **the result of running ‘Load Plant Structure’. An administrator with ’Full** **Control’ permissions in Options Manager must run the ’Finish Load Plant** **Structure Processing’ command in Drawing Manager to unlock this plant.** ”, will appear.

180 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **OK**.
2. Select **502** in the Tree View, and then select **Tools > Finish Load Plant** **Structure Processing**.
3. A **Drawing Manager** dialog with the message, “**This action is required to** **enable you to continue working with your drawings; however, the process** **may take some time. Do you want to perform the process now? If you** **choose Cancel, you will have to perform the process later.** ”, will appear.
4. Select **OK**.
5. The **Finish Load Plant Structure Processing** dialog displays green check marks next to each drawing as they are processed. Wait for the software to process the drawings that have been copied with this plant structure. The status “Process is completed.” appears in this dialog when it is finished. Select **Close**.
6. Open **Drawing1A** in SmartPlant P&ID, and verify it opens.
7. Select **File > Exit**.

SmartPlant P&ID Setup and Customization Course Labs181 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

**Lab 38 – Running the Data Dictionary**

## **Template Comparison Utility**

**Objective:** To create data dictionary templates from the Custom plant, and then compare the data dictionary templates with the 501K plant.

1. Open **SmartPlant Engineering Manager**.
2. Select Custom, and then select **Tools** > **New Data Dictionary Template**.
3. Notice the name, **Custom_SPAPLANT.ddt**, and the path of where the .ddt file will be saved, and then select **OK**.
4. The **SmartPlant Engineering Manager** dialog with the message, “**The plant** **data dictionary template was created successfully.** ”, will appear.
5. Select **OK**.
6. Expand **Custom**, select the **Applications** node, and in the List View, right-click **SmartPlant P&ID**, and then select **New Data Dictionary Template**.

182 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Notice the name, **Custom_SPPID.ddt**, and the path of where the .ddt file will be saved, and then select **OK**.
2. The **SmartPlant Engineering Manager** dialog with the message, “**The** **SmartPlant P&ID data dictionary template was created successfully.** ”, will appear.
3. Select **OK**.
4. Select **File > Exit**.
5. Select **Start > All Programs > Intergraph SmartPlant Engineering Manager**

**> Data Dictionary Template Comparison Utility**.

1. On the **Data Dictionary Template Comparison Utility** dialog, enter the information on the following image.
2. Select **Compare**.

SmartPlant P&ID Setup and Customization Course Labs183 *** ***

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Create Report**.
2. On the **Create Report** dialog, browse to **C:\Temp**, and then select **Save**.
3. Select **Yes** to view the report.
4. Review the report, and then select **File > Close**.
5. On the **Data Dictionary Template Comparison Utility** dialog, enter the information on the following image.

184 * SmartPlant P&ID Setup and Customization Course Labs *

*SmartPlant P&ID Setup and Customization Course Labs*

1. Select **Compare**.

**Note:**

- If the following message, “**Schema types do not match**

**(SPPID/SPAPLANT)**”, appears, select **OK**, and then reselect the plant name, **501K**, before selecting **Compare**.

1. Select **Create Report**.
2. On the **Create Report** dialog, browse to **C:\Temp**, key in **Book2.xls** for File name, and then select **Save**.
3. Select **Yes** to view the report.
4. Review the report, and then select **File > Close**.
5. **Exit** the **Data Dictionary Template Comparison Utility**.

SmartPlant P&ID Setup and Customization Course Labs185 *** ***