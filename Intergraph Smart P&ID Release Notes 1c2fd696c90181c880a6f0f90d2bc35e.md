# Intergraph Smart P&ID Release Notes

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Release Notes**

**Hexagon Documentation**

Generated 03/19/2025

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

1/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Table of Contents**

What’s new in Intergraph Smart® P&ID

Version 12

Special Instructions

Internationalization

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

2/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**What’s new in Intergraph Smart® P&ID**

This document provides information on the latest features in the current release of Intergraph Smart® P&ID.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 1/3/2025 at 10:45 AM

**Version 12**

**Drawing Manager**

You can now modify properties of multiple drawings at once. This feature enhances user experience and productivity. See Modify Drawing Properties. (4212302) **P&ID Modeler/P&ID Engineering**

By default, the SPID error logs and enhanced logs are now stored at

%localappdata%\SPIDLogs instead of on the desktop. This migration aligns with best practices for file management. (4309498)

Smart P&ID now provides enhanced logs on the status of recreate and update drawing workflows. This improvement is crucial for better diagnostic capabilities and issue resolution. See Log Files. (4173231; 4188721)

You can now move auxiliary graphics without entering the auxiliary graphics mode. This enhancement streamlines the editing process, improves efficiency, and reduces the need to frequently switch between modes. See Edit auxiliary graphics. (4081945) For plants with projects, the Excel reports will now show plant name in !

format. For more information, see Generating Reports.

You can now choose between the classic and new progress bars. In addition to visual progress, the new progress bar includes a percentage completion indicator. See Customizing the Progress Bar. (4109964)

You must enable the Safe mode ActiveX setting in Excel for the reports to work properly.

See Creating and editing report templates. (3972492) https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

3/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Integration**

Smart P&ID Share Service is now included in the standard installation. See Installing the Software. (4063581)

The **SmartPlant** menu has been renamed to **Integration** menu. Also, added a new **Reshare** command, that allows you to reshare P&ID items with HxGN SDx2. See Reshare Command. (4334770, 4309362)

You must install both SmartPlant Client COM and SmartPlant Client.Net to create enhanced mapping for integration. (4207032)

We have improved and simplified the integration process between Smart P&ID and Smart Reference Data using the Options Manager settings. For details, see Connect to Smart Reference Data Server. (3423114, 3450879) When assigning a Piping Materials Class (PMC) for a pipe run, the Smart P&ID Piping Specifications dialog now displays only a list of piping specifications available for the plant specified in the Options Manager settings. This enhancement allows you to access only the piping specifications relevant to the plant you’re working with. (3729980) **Utilities**

You can now repair and report drawings using a command prompt without the need to open the Service Pids utility. This enhancement also enables you to schedule automatic repair and report jobs. For more information see, Analyze and repair drawings.

(4146612)

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

4/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Special Instructions**

**Assign User Rights for Scheduled Tasks on Windows 10**

On a Windows 10 operating system, users with standard User privileges must be granted special access to allow them to run scheduled tasks.

The changes described in this procedure can be made by a System Administrator only.

1. Log in using your administrator credentials.
2. Select the Windows icon and in the Search box, type Local Security Policy or Secpol.msc.
3. In the tree view, select to expand **Security Settings** > **Local Policies** > **User Rights** **Assignment**.
4. In the right pane, scroll down to the option **Log on as a batch job**.
5. Right-click this option and on the shortcut menu, select **Properties**.
6. Select the **Add User or Group** button.
7. In the **Select Users, Computers, Service Accounts, or Groups** dialog, enter **Users** (where **From this location** points to **Entire Directory**) or “specific user name” to run the scheduled tasks with all users or only with the specific user of the system respectively.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

5/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Internationalization**

Supporting internationalization in a homogeneous environment is one of the enhancements available in Hexagon’s products. A homogeneous environment uses elements from only a single locale. For example, a German customer running on a German operating system using only German characters and German cultural conventions is a fully supported homogeneous environment configuration.

**Homogeneous Environments**

When starting a new project, use extra care during installation and configuration to ensure the proper creation and maintenance of homogeneous environments: All the computers (servers and clients) within a Hexagon’s product implementation must have the same regional settings, and no one should change the regional settings after the project has started.

Do **not** cross the decimal locale boundary. This is the most common cause of numeric data corruption and calculation errors. Having users with different regional settings (such as with a period versus a comma for the decimal point) causes the software to interpret values unpredictably. For example, a pipe run with a pressure of 35.3 psi can be read by the software as 353 psi to the user with different regional settings. A cable length defined as 39 ft 11,21 inches has been interpreted as 121718910971323 meters when published to an XML file. These incorrect interpretations may be used in internal software calculations and can be impossible to backtrack or correct. Do not change the decimal point character to try to solve an issue. Doing so will only corrupt values in the database or in text files.

Do **not** cross the character-set locale boundary. For example, the character set boundary between Western (Latin-based) and Eastern Europe (Cyrillic-based), or between Eastern Europe and Japan.

Create Oracle databases using AL32UTF8 for the database character set and AL16UTF16 for the NLS character set.

Never modify the NLS_LANG registry entry on an Oracle client. Doing so causes the character data not to convert to Unicode.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

6/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

Create Microsoft SQL Server databases with locale-specific collation settings and ensure that all databases have the **same** setting.

Intergraph Smart Cloud delivers all solutions on English infrastructure. A homogeneous environment is available when customers deploy English clients.

**Heterogeneous Environments**

In contrast, a heterogeneous environment using elements from different, or even multiple locales, **is not supported**. Many customers are currently operating in unsupported heterogeneous environments and are often not aware of that fact. Examples of heterogeneous environments:

Entering or viewing Japanese data on a US/English operating system Using German Regional Settings (where the decimal point is a comma) on a US/English operating system

Using databases with different character encodings such as CL8MSWIN1251 or JA16SJIS

Using multiple languages in a project, **especially** when crossing language-group boundaries

Using an English server with different local language clients Intergraph Smart Cloud delivers all solutions on English infrastructure. Any clients configured to use non-English will result in a heterogeneous environment.

**International / Bi-lingual Projects**

International bi-lingual projects are possible; however, great care must be used when configuring these environments. Limitations exist and must be properly understood: Oracle and MS SQL Server databases can reside on any language operating system, as long as the databases have been created and configured with proper Unicode and collation settings.

All SQL Server databases must have the same collation setting and reflect the *master* language. Text is stored, sorted, indexed, and presented based on the collation setting.

You must determine which language will be used primarily to generate output (P&IDs, SLDs, reports, approval documents, and so forth.) If Russian and English text is https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

7/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

entered, and Russian is the target locale, choose the collation based on the Cyrillic character set.

All Microsoft operating systems (Japanese, Russian, German, and so forth) can enter English characters. The reverse, however, is not true in most cases.

Keyboard-locale can be changed as long as a character-set and code-page boundary is not crossed. For example, English, German, French, and Spanish characters can all be used in the same project because the same Windows® code-page (1252) is used.

However, Russian characters (code-page 1251) cannot be used in a US/English environment.

You must decide which language operating system is the master for bi-lingual projects.

The following is an example of a Russian-based project: Companies in the United States and the United Kingdom are working a project with a Russian company and the deliverables (drawings, reports, and so forth) must ultimately be provided in Russian. The companies in the U.S. and the U.K. are working the project using the *master* Russian operating systems (possibly using virtual Russian operating systems running on VMware Workstation). The U.S. and U.K. companies can install and use English Microsoft Office products on the Russian operating system because Office products are globally enabled. If a Russian interface exists for the Hexagon’s product application, then Russian users can use the Russian interface while the English-speaking users continue to use the US/English interface. English-speaking engineers can enter English characters. Russian-speaking engineers can enter Russian characters.

However, because the Russian locale uses different decimal and character-set locales, everyone (English and Russian engineers) **must** use the Russian decimal symbol which is a comma. For customization purposes, databases can be modified to accommodate new Russian-specific requirements (fields, properties, and so forth.) Using filters, display sets, and other software features, bi-lingual projects can be further customized. Graphic data, reports, and so forth can be created in either or both languages.

Do not change regional settings to reflect a U.S. environment in order to resolve problems in a non-US/English homogeneous configuration. Doing this creates a heterogeneous configuration that **will** cause other possibly hidden problems that cannot be corrected. Everyone working on a project must use the same regional settings and character set throughout the life of the project.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

8/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Citrix Virtual App Solutions for International Projects** Using Citrix Virtual App Solutions, you can define environments that isolate users from having to interact with non-native language operating systems while improving data integrity and minimizing opportunities for data corruption. However, users must enter data using master locale conventions for the project (decimal separator and date conventions, for example). You can create these environments using different combinations of languages, but some limitations exist. For example, you cannot use Russian and Chinese text together in a project.

In addition, special language characters (the German ä and ß for example) cannot be used if the master locale is outside the western Latin-based languages (the master locale is Russian, Chinese, Japanese, or Korean, for example).

**Questions and Assistance**

Please contact your support representative for assistance and answers to your questions: see

customer support <https://hexagon.com/support-success/asset-lifecycle-

intelligence/community> .

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

9/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . You can submit any documentation comments or suggestions you might have by logging on to our

documentation web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To join in conversations about Smart P&ID, go to Technical User Forums

[https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf](https://hexagon.com/support-success/asset-lifecycle-intelligence/tuf) and join the

**Engineering & Schematics TUF** group.

**Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, Intergraph, or its affiliates, parents, subsidiaries retains ownership of the product.

You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

10/15

3/19/25, 10:36 AM

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

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

11/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

**Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

**Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

12/15

3/19/25, 10:36 AM

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

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

13/15

3/19/25, 10:36 AM

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

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, Intergraph Smart® Cloud, PDS®, FrameWorks®Plus, I-Route, I-Export, Isogen®, Intergraph Spoolgen®, SupportManager®, SupportModeler®, SAPPHIRE®, TANK®, PV Elite®, CADWorx®, CADWorx DraftPro®, GT STRUDL®, CAESAR II® , and HxGN SDx®

are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners.

Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

14/15

3/19/25, 10:36 AM

Hexagon Documentation Site Export

**Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/f01395aa-4e78-41b8-8770-09d495041ed8

15/15