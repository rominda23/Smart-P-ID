# Intergraph Smart P&ID Installation and Upgrade

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Intergraph Smart P&ID Installation and Upgrade**

## **Hexagon Documentation**

Generated 03/19/2025

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

1/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Table of Contents**

Instal ing the Software for Intergraph Smart® P&ID

Smart P&ID Program Group

Internationalization

Hardware and Software Recommendations

Smart P&ID Database Server

Smart P&ID Workstation

Smart P&ID Project Hardware Sizing Recommendations

Before You Instal

Loading Smart P&ID Prerequisite Software

Oracle Instal ation and Configuration

Instal ing Oracle Client

Register Oracle .NET assemblies

Enable pipe spec validation with Smart Reference Data

Instal ing the Software

Grant Permissions to Write to a Registry Key

Uninstal a Previous Version of Smart P&ID

Instal Smart P&ID

Instal Intergraph Smart® 3D S3DPIDClient

Modify or Uninstal the Latest Version of Smart P&ID

Instal ing Smart P&ID in Silent Mode

Working in Thin Client Mode

Instal ing and Configuring Smart P&ID for Integration with Aspen Basic Engineering™

Configuring Reference Data for Smart P&ID

Instal Smart P&ID Reference Data

Upgrading Smart P&ID

Correcting Database Constraint Violations for Smart P&ID

Post-Upgrade Tasks

Upgrading Reference Data

Upgrading Existing Automation Projects

Updating Drawings

User Access

Smart P&ID User Rights

Customizing Your Reference Data

Customize Reference Data Options

Establishing Design Rules

Working with Filters

Working with Formats

Working with Symbols and Labels

Modifying Data Model Properties

Configuring Border Templates

Customizing the Progress Bar

Integration with SmartPlant Foundation

Integration with HxGN SDx2

Integration with SPF

About Security and Encryption

What techniques are used for Encryption?

Database encryption

Communication encryption between application client and server

Disk encryption

File share encryption

Support, Copyright, and Legal Information

Customer Support and Technical User Forum

Hexagon Policy Against Software Piracy

Copyright Notice

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

2/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Installing the Software for Intergraph Smart® P&ID**

The following information is specific to the product being installed on-premises.

Intergraph Smart® P&ID creates intelligent P&IDs by populating the database with relevant plant data. This method provides valuable information throughout the plant life cycle. As a data-centric, rule-based solution for the P&ID life cycle, Smart P&ID helps users improve design quality, data consistency, and standards compliance. With quick access to supporting engineering data, Smart P&ID significantly cuts design and modification time and increases accuracy with its exclusive data-centric approach and use of design rules, automatic checks, and drag-and-drop capabilities.

Smart P&ID is vastly different from graphic-driven P&ID solutions of today. All data from the P&ID is stored in the plant database and adheres to plant standards. The graphical representation of the P&ID is a view or a report of the data. The strong data import and export facilities of Smart P&ID allow users to populate the system with relevant plant data, such as process data from process simulation databases based on Aspen Basic Engineering from Aspen Technologies, Inc. or equipment and line lists. The Import can be used to either update data on existing items in the plant database or to create new items in the Smart P&ID Stockpile to use for designing the P&ID.

The rule-based and automation capabilities of Smart P&ID also differentiate it from other P&ID systems. Smart P&ID features a comprehensive, user-definable rule-based system that assists the engineer during the design phase of the plant and subsequent life cycle phases. Data is entered directly into the database; rules are executed; and feedback is immediate. The design rule-base confirms data consistency and compliance with plant and engineering standards, allowing faster, more efficient design with less iteration.

Smart P&ID incorporates the latest Microsoft technologies, such as OLE automation, to provide integration with existing data and other systems. Running on various Microsoft Windows operating system platforms, Smart P&ID does not require a traditional, expensive CAD

engine for P&ID creation. The open architecture of Smart P&ID permits integration with other systems, such as Smart 3D, Smart Instrumentation, and Aspen Basic Engineering, all of which allow users to share data with third-party software.

Customer Support

Hexagon Policy Against Software Piracy

Copyright 1999-2024 Hexagon AB <https://hexagon.com/company/divisions/asset-lifecycle-intel igence> and/or its subsidiaries and affiliates Version 12

Published 12/23/2024 at 6:46 AM

**Smart P&ID Program Group**

Smart P&ID provides multiple views of a central, unified data structure that represents the plant model. A view is a visual presentation of the data in the plant model and can be a schematic drawing or a table. The plant model is the computer representation of the conceptual design, including all plant components and their relationships. By manipulating model views, you can organize the information within the plant model to better understand and maintain the data.

Smart P&ID has several programs and utilities for running and managing your plant data.

**Smart P&ID** provides the design environment for Smart P&ID

drawings.

**Drawing Manager** allows you to create and delete drawings,

manage drawing versions, and print multiple drawings.

**Insulation Specification Manager** allows you to create and modify

lookup tables for insulation specifications and thicknesses.

**Options Manager** defines plant-wide graphic standards for

symbology, gapping, heat tracing, and formats. Options Manager

also defines paths to Smart P&ID files and directories.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

3/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Rule Manager** defines rules for placement and property copying on

placement.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

4/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Internationalization**

Supporting internationalization in a homogeneous environment is one of the enhancements available in Hexagon’s products. A homogeneous environment uses elements from only a single locale. For example, a German customer running on a German operating system using only German characters and German cultural conventions is a fully supported homogeneous environment configuration.

## **Homogeneous Environments**

When starting a new project, use extra care during installation and configuration to ensure the proper creation and maintenance of homogeneous environments:

All the computers (servers and clients) within a Hexagon’s product implementation must have the same regional settings, and no one should change the regional settings after the project has started.

Do **not** cross the decimal locale boundary. This is the most common cause of numeric data corruption and calculation errors. Having users with different regional settings (such as with a period versus a comma for the decimal point) causes the software to interpret values unpredictably. For example, a pipe run with a pressure of 35.3 psi can be read by the software as 353 psi to the user with different regional settings. A cable length defined as 39 ft 11,21 inches has been interpreted as 121718910971323 meters when published to an XML file. These incorrect interpretations may be used in internal software calculations and can be impossible to backtrack or correct. Do not change the decimal point character to try to solve an issue. Doing so will only corrupt values in the database or in text files.

Do **not** cross the character-set locale boundary. For example, the character set boundary between Western (Latin-based) and Eastern Europe (Cyrillic-based), or between Eastern Europe and Japan.

Create Oracle databases using AL32UTF8 for the database character set and AL16UTF16 for the NLS character set.

Never modify the NLS_LANG registry entry on an Oracle client. Doing so causes the character data not to convert to Unicode.

Create Microsoft SQL Server databases with locale-specific collation settings and ensure that all databases have the **same** setting.

Intergraph Smart Cloud delivers all solutions on English infrastructure. A homogeneous environment is available when customers deploy English clients.

## **Heterogeneous Environments**

In contrast, a heterogeneous environment using elements from different, or even multiple locales, **is not supported**. Many customers are currently operating in unsupported heterogeneous environments and are often not aware of that fact. Examples of heterogeneous environments:

Entering or viewing Japanese data on a US/English operating system

Using German Regional Settings (where the decimal point is a comma) on a US/English operating system Using databases with different character encodings such as CL8MSWIN1251 or JA16SJIS

Using multiple languages in a project, **especially** when crossing language-group boundaries Using an English server with different local language clients

Intergraph Smart Cloud delivers all solutions on English infrastructure. Any clients configured to use non-English will result in a heterogeneous environment.

**International / Bi-lingual Projects**

International bi-lingual projects are possible; however, great care must be used when configuring these environments. Limitations exist and must be properly understood:

Oracle and MS SQL Server databases can reside on any language operating system, as long as the databases have been created and configured with proper Unicode and collation settings.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

5/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

All SQL Server databases must have the same collation setting and reflect the *master* language. Text is stored, sorted, indexed, and presented based on the collation setting. You must determine which language will be used primarily to generate output (P&IDs, SLDs, reports, approval documents, and so forth.) If Russian and English text is entered, and Russian is the target locale, choose the collation based on the Cyrillic character set.

All Microsoft operating systems (Japanese, Russian, German, and so forth) can enter English characters. The reverse, however, is not true in most cases.

Keyboard-locale can be changed as long as a character-set and code-page boundary is not crossed. For example, English, German, French, and Spanish characters can all be used in the same project because the same Windows® code-page (1252) is used. However, Russian characters (code-page 1251) cannot be used in a US/English environment.

You must decide which language operating system is the master for bi-lingual projects.

The following is an example of a Russian-based project:

Companies in the United States and the United Kingdom are working a project with a Russian company and the deliverables (drawings, reports, and so forth) must ultimately be provided in Russian. The companies in the U.S. and the U.K. are working the project using the *master*  Russian operating systems (possibly using virtual Russian operating systems running on VMware Workstation). The U.S. and U.K.

companies can install and use English Microsoft Office products on the Russian operating system because Office products are globally enabled. If a Russian interface exists for the Hexagon’s product application, then Russian users can use the Russian interface while the English-speaking users continue to use the US/English interface. English-speaking engineers can enter English characters. Russian-speaking engineers can enter Russian characters.

However, because the Russian locale uses different decimal and character-set locales, everyone (English and Russian engineers) **must** use the Russian decimal symbol which is a comma. For customization purposes, databases can be modified to accommodate new Russian-specific requirements (fields, properties, and so forth.) Using filters, display sets, and other software features, bi-lingual projects can be further customized. Graphic data, reports, and so forth can be created in either or both languages.

Do not change regional settings to reflect a U.S. environment in order to resolve problems in a non-US/English homogeneous configuration. Doing this creates a heterogeneous configuration that **will** cause other possibly hidden problems that cannot be corrected.

Everyone working on a project must use the same regional settings and character set throughout the life of the project.

**Citrix Virtual App Solutions for International Projects**

Using Citrix Virtual App Solutions, you can define environments that isolate users from having to interact with non-native language operating systems while improving data integrity and minimizing opportunities for data corruption. However, users must enter data using master locale conventions for the project (decimal separator and date conventions, for example). You can create these environments using different combinations of languages, but some limitations exist. For example, you cannot use Russian and Chinese text together in a project. In addition, special language characters (the German ä and ß for example) cannot be used if the master locale is outside the western Latin-based languages (the master locale is Russian, Chinese, Japanese, or Korean, for example).

## **Questions and Assistance**

Please contact your support representative for assistance and answers to your questions: see customer support

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) .

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

6/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Hardware and Software Recommendations**

Before beginning an installation of your engineering software, verify that your servers meet the requirements in this section.

For optimum display of Smart P&ID UI elements, it is recommended to set your computer’s display with **Change the size of text, apps** **and other items** at 100% and **Display resolution** of 1920 x 1080.

**Smart P&ID Database Server**

## **Hardware Recommendations**

For details of the recommended hardware configuration for the Smart P&ID database server, see Smart P&ID Project Hardware Sizing

Recommendations. For additional details regarding platform support, please review the latest compatibility matrix available on Smart

Community [https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . If you cannot access the compatibility matrix,

contact customer support [https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) .

## **Supported Operating Systems**

Microsoft Windows Server 2019 Standard or Enterprise Server

Microsoft Windows Server 2022 Standard or Enterprise Server

Linux 9 Update 2

## **Remote Client Server Operating System**

Microsoft Windows Server 2022 Standard or Enterprise Server

## **Supported Database Servers**

Oracle 19.3 Standard Edition or Enterprise Edition

Oracle for Linux 19.3.0.*

Microsoft SQL Server 2019 Standard Edition or Enterprise Edition

Microsoft SQL Server 2022 Standard Edition or Enterprise Edition

Beginning with Windows 10 and Oracle 12.1.0.2, Microsoft and Oracle will enforce the Internet Host Table Specification RFC

952 which mandates that component hostname labels can contain only alphanumeric characters. Host names using underscores (‘_’) are not allowed. Refer to Oracle Support Articles 1603775.1 and 1957895.1 and Microsoft KB 101785.

The following editions of Oracle Database Server are available:

**Standard Edition**: For department or workgroup level applications, or for small-to-medium sized enterprises (SMEs). It is engineered to provide core relational database management services and options. If you select this installation type, you must purchase additional licenses if you want to install extra Enterprise Edition options.

**Enterprise Edition**:** **For enterprise-level applications. It is engineered for mission-critical, high-security online transaction processing (OLTP) and data warehousing environments. If you select this installation type, all separately licensable Enterprise Edition options are installed.

If working with Smart P&ID connected workshare configuration, the Standard Edition of Oracle will suffice. If Smart 3D workshare will also be implemented on this database server, then the Enterprise Edition is required.

**Smart P&ID Workstation**

## **Hardware Recommendations**

The recommended hardware configuration for the Smart P&ID workstation is as follows: 16 GB RAM for Microsoft SQL Server or Oracle

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

7/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

64-bit Bus Size, OS, and Database

## **Network Requirements**

1 GbE or higher network speed, latency must be less than 1 ms between the client and database server.

## **Recommended Disk Space**

Oracle Client: 1.0 GB

Full installation of Smart P&ID: 0.4 GB

Additional disk space is required for software prerequisites and optional software that you install.

## **Supported Operating Systems**

Microsoft Windows 10 (build 22H2 or later) Professional or Enterprise Edition (64-bit) Microsoft Windows 11 (build 22H2 or later) Professional or Enterprise Edition (64-bit) Smart P&ID is certified on Windows with UAC ‘On’ at Level 3 (Default) **Supported Database Clients**

Oracle Database 19.3.0.*.* Client, 32-bit

Microsoft .NET Framework 4.8 must be installed as a prerequisite for the installation of Oracle Client.

The client database software must be the same version as the server database software.

Oracle 32-bit Client is required for both 32-bit and 64-bit Oracle databases.

Do not use Oracle ‘light client’ as it does not include some of the required .dll files.

Beginning with Windows 10 and Oracle 12.1.0.2, Microsoft and Oracle will enforce the Internet Host Table Specification RFC 952 which mandates that component hostname labels can contain only alphanumeric characters. Host names using underscores (‘_’) are not allowed. Refer to Oracle Support Articles 1603775.1 and 1957895.1 and Microsoft KB 101785.

## **Licensing Requirements**

Smart P&ID 12 requires Intergraph Smart® Licensing Client 14.02 or latest update.

A license is required to do any of the following for drawings in Smart P&ID Drawing Manager: Open a drawing in Smart P&ID (includes opening the drawings in overlapping view) Update

Batch update

Refresh template

Import

Copy/paste

Print (either from Drawing Manager or Smart P&ID)

A separate license is required for the following activities:

Schedule update

Schedule print

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

8/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Therefore, at the time when a scheduled update or print is set to run, single license users will need to ensure that any other Drawing Manager activity that requires a license is not running.

All other Drawing Manager features do not require a license; these include: creating a new drawing, deleting a drawing, filtering the view, all revision and version activities, Projects, Workshare, Integration, and report activities.

## **Software Prerequisites**

Microsoft .NET Framework 4.8

Microsoft .NET Core 2.2.

Google Chrome or Microsoft Internet Explorer or Microsoft Edge, required for viewing the Online documentation delivered with the software and the report generated from Rule Manager.

Microsoft Office 2022 or Microsoft Office 365 (32-bit), required for working with report templates, importing and generating reports, importing from SmartSketch, and saving drawings as MicroStation or AutoCAD.

Microsoft XML Core Services (MSXML) 6.0 Service Pack 1 or 6.0 Service Pack 3.

Microsoft Visual C++ 2017 or 2019 for automation.

## **Optional Software**

Apart from SmartSketch, Smart Engineering Manager, Intergraph Smart® 3D S3DPIDClient, and BricsCAD® Pro, the following software programs are not Hexagon software and are owned by third parties. It is the responsibility of the customer to select at its sole discretion the applicable third-party software the customer desires to use to generate reports and Hexagon makes no recommendation as to the choice of said third-party software. The customer is responsible for obtaining a valid license to use said third-party software from the owner of said third-party software and to pay any license fees to the owner of said third-party software for the use of said third-party software. HEXAGON DISCLAIMS AND MAKES NO WARRANTY EITHER EXPRESS OR IMPLIED, INCLUDING THE WARRANTIES OF

MERCHANTABILITY OR THE WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE IN REGARD TO SAID THIRD-PARTY

SOFTWARE.

For administrative functions, Smart Engineering Manager 13 or a latest update.

To use Smart 3D specifications in Smart P&ID Piping Specification Utility, you must install the Intergraph Smart 3D S3DPIDClient. See

Install Intergraph Smart® 3D S3DPIDClient.

Citrix Virtual App 7 2203 on Windows Server 2022 (Standard or Enterprise).

One of the following compatible drawing software programs (for viewing files generated using the ‘Save As’ feature): SmartSketch 11 or a later hot fix

Autodesk AutoCAD 2022

Bentley MicroStation V8

BricsCAD Pro 24

For additional details regarding platform support, please review the latest compatibility matrix available on Smart Community

[https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) . If you cannot access the compatibility matrix, contact

Customer Support [https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) .

**Smart P&ID Project Hardware Sizing Recommendations**

Use these guidelines and examples in sizing Smart P&ID hardware configurations, including Connected Workshare.

Hardware sizing, especially for servers, depends on many factors such as: The number of concurrent users per site

The number of sites (for Connected Workshare)

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

9/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

The size of the project (which translates into the size of the databases) Other software that is running on the computer

For best performance in medium to large workshare configurations, we recommend using 64-bit hardware and operating system. Smart P&ID was tested in workshare environments for sites on Oracle databases (Connected or Standalone Workshare) and Microsoft SQL Server databases (Standalone Workshare only) running 64-bit hardware and operating system.

## **Concurrent Users**

The size of the system depends partly on the number of concurrent users, that is, users actively working at the same time. For Connected Workshare, it is probable that work will be done at several sites in a non-concurrent way. In this case, there is less impact on performance.

For example, if you have two sites with 60 users at each site but the users at the two sites do not work at the same time, you could consider the user load to be 60 users.

In a Connected Workshare configuration when users are working concurrently at several sites, the work done at one site will impact each site as the data is pushed to the other sites. In a hub and spokes configuration, the data is first pushed to the hub then the hub pushes it to the other sites. We estimate that the equivalent user load (the number of effective users) for each server to be the users on that server plus 25%

of the total concurrent users of all the other sites. For example, in a configuration with 6 sites and 40 users at 5 sites, and 5 users at 1 site: When 3 sites (with 40 users) are working concurrently, the equivalent number of users at each site is: 40 (concurrent users for this site)

+ (0.25 * (2 * 40)) (users for the 2 other sites) = 60 users.

When all 6 sites are working concurrently:

1. The equivalent number of users at each of the 40-user sites is: 40 + (0.25 * (165)) = 81 users b. The equivalent number of users at the 5-user site is: 5 + (0.25 * (200)) = 55 users.

## **Project Size Estimates**

Use the following estimates to help define project size. The model database is an important factor in determining project size.

The number of users for each project size below (small, medium, and large) is the **effective** *number connected to a single server*. The **effective** number of users should be calculated by taking into consideration: 1. Connected Workshare Setup - use the 25% formula above

1. Drawing Batch server - add 3 users
2. Remote IFC - add 1 user

## **One small project**

1 to 15 **effective** users on one database server

Database up to 10 GB

Up to 500 drawings

4 processor cores

32 GB RAM for Microsoft SQL Server or Oracle

64-bit Bus Size, OS, and Database

## **One medium project**

16 to 50 **effective** users on one database server

Database 10 GB to 30 GB

501 to 1000 drawings

4-8 processor cores

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

10/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

64 GB RAM for Microsoft SQL Server or Oracle

64-bit Bus Size, OS, and Database

## **One large project**

51 to 100 **effective** users on one database server (contact Customer Support if you plan to have more than 100 **effective** users on one database server)

Database 30 GB or more

1001 or more drawings

8 or more processor cores

128+ GB RAM for Microsoft SQL Server or Oracle

64-bit Bus Size, OS, and Database

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

11/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Before You Install**

Before you begin installing the software, verify that the computers on which the software components will be installed meet the requirements

described in the Hardware and Software Recommendations.

**Loading Smart P&ID Prerequisite Software**

Install any required prerequisite software which is not yet installed on your computer. The following software is required: Intergraph Smart® Licensing

Microsoft .NET Core

If Microsoft .NET Framework is not installed on your computer, you must download and install it before you can proceed with the Smart P&ID installation.

Microsoft Visual C++ for automation.

Requirements might vary depending on your particular configuration. See Hardware and Software Recommendations.

If working on an Oracle platform, you must register the Oracle DataAccess dlls to the Global Assembly Cache (GAC). See Register

Oracle .NET assemblies.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

12/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Oracle Installation and Configuration**

For Smart P&ID, when working on an Oracle database, the Oracle client installation only is required. You install Oracle client after the Oracle database server installation has been completed. See Installing Oracle Database Server.

## **Oracle Instances**

If one server hosts the databases of several products, it is recommended that each product’s database be a separate instance, each of which can host multiple plants.

The advantage of placing each product’s database in its own instance is that only the affected application will be off-line during backup, performance tuning, and other database maintenance activities. Additionally, global tuning parameters that apply to one instance can be tailored to the specific product requirements.

According to Oracle documentation, the only limit to the number of instances you can have on any computer is the availability of resources.

However, the number of instances on one database server should be minimized, because each additional instance places additional load on the server.

Each instance adds redundant tablespaces, rollback segments, background processes, and memory requirements for each SGA (System Global Area). For this reason, you should start by putting the database of one product for several plants into a single instance. Then, when the number of plants increases, or a plant becomes very large, consider separating the database into new instances, adding server memory, or even adding database servers.

## **Installing Oracle Client**

The Oracle client provides Smart P&ID with the means to interface with the Oracle database server. You install the Oracle client after you have completed the Oracle database server installation. You can install the Oracle client either on a file server or on the local station. If you install the Oracle client on a station, make sure you have the appropriate access rights to the Oracle database server.

Make sure that a compatible Oracle server version is installed. Set up your client Windows regional and language options as you require.

You can only set up these options before the client installation. If you want to change the regional and language options after the installation, you will have to reinstall the Oracle client for the changes to take effect.

When running the Oracle client installation, choose the required installation type as follows: **Administrator**

For users who need Administrator functions, such as the ability to create tablespaces and restore backups using Smart Engineering Manager.

## **Runtime**

For all other users.

## **Register Oracle .NET assemblies**

After installing both Oracle Server and Client, you must run the following Command Line commands from the Command Line or Power Shell.

This registers specific DLLs that were not registered in the Global Assembly Cache (GAC) when installing Oracle but are required for Smart P&ID to function with Oracle.

The following procedure describes the four commands that you need to action to register the appropriate DLLs to the GAC and complete the Oracle connection to Smart P&ID.

You must register these DLLs each time you apply a patch.

1. Open the Windows CMD Interface as Administrator.
2. Run the following four commands in the CMD window.

CMD: <Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\bin\4\OraProvCfg.exe /action:gac /providerpath:

<Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\bin\4\Oracle.DataAccess.dll https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

13/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

CMD: <Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\bin\4\OraProvCfg.exe /action:gac /providerpath:

<Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\PublisherPolicy\4\Policy.4.112.Oracle.DataAccess.dll CMD: <Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\bin\4\OraProvCfg.exe /action:gac /providerpath:

<Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\PublisherPolicy\4\Policy.4.121.Oracle.DataAccess.dll CMD: <Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\bin\4\OraProvCfg.exe /action:gac /providerpath:

<Oracle_Installation_Folder>\product\xx.x.x\client_1\ODP.NET\PublisherPolicy\4\Policy.4.122.Oracle.DataAccess.dll The screen shot below shows an example of successful registration of all the dlls.

For additional information, refer to:

Oracle Support article: 12.2 Installation Does Not Register Oracle Data Provider for .Net in the GAC (Doc ID 2272241.1)’.

Oracle Central Designer software Help topic: ‘Registering .NET assemblies’.

**Enable pipe spec validation with Smart Reference Data**

To enable pipe spec validation with Smart Reference Data, you need to run the following gacutil.exe commands: gacutil.exe /I “\product\xx.x.x\client_1\ODP.NET\bin\2.x\Oracle.DataAccess.dll”

gacutil.exe /I “\product\xx.x.x\client_1\ODP.NET\PublisherPolicy\2.x\Policy.2.112.Oracle.DataAccess.dll”

The gacutil.exe command comes with the Windows 10 SDK (https://developer.microsoft.com/windows/downloads/windows-10-sdk).

If the file is available, it is not necessary to install the SDK; just copy gacutil.exe and gacutil.exe.config and that will allow you to install the dlls into the GAC.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

14/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Installing the Software**

This section describes how to install Smart P&ID and supporting software. Before you begin installing the software, verify that the computers

on which the software components will be installed meet the requirements described in the Hardware and Software Recommendations.

The Open Database functionality, incorporated into all parts of the SmartPlant® software, allows you to install pieces of the software on several different workstations. You do not have to maintain a server for just Smart Engineering Manager. For example, you can install Smart Engineering Manager and its related managers on one workstation, Smart P&ID and its related managers on a different workstation, and the reference data on yet another workstation or file server.

During installation of the software, you have the option of installing the fully functional Smart P&ID or Smart P&ID Engineering.

Smart P&ID Engineering allows data editing but does not allow placement, moving, or deleting items on the drawing sheet.

**Grant Permissions to Write to a Registry Key**

During the installation process, you might receive an error stating that setup does not have permission to modify one or more registry keys.

This procedure explains how to grant write permissions to the registry keys.

1. Select **Start** > **Run**.
2. Enter **regedit.exe**, and then select **OK**.
3. In the left pane of the **Registry Editor** window, select the appropriate registry key: For a 32-bit computer, select the **HKEY_LOCAL_MACHINE**\**Software**\**Intergraph**\**Applications** registry key.

For a 64-bit computer, select the **HKEY_LOCAL_MACHINE**\**SOFTWARE**\**Wow6432Node**\**Intergraph**\**Applications** registry key.

1. Right-click, and then select **Permissions** on the shortcut menu to open the **Permissions for Applications** dialog.
2. Select **Advanced**.
3. At the bottom of the **Advanced Security Settings for Applications** dialog, clear the **Include inheritable permissions from this** **object’s parent** option.
4. To verify your change, select **Remove** on the security dialog that displays.
5. Reselect the **Include inheritable permissions from this object’s parent** check box.
6. Select the **Replace all child object permissions with inheritable permissions from this object** check box.
7. Select **OK** and at the prompt, select **OK** again.
8. Select **OK**.

**Uninstall a Previous Version of Smart P&ID**

1. Open **Control Panel**, and select **Programs and Features** > **Uninstall a Program**.
2. Select **Intergraph Smart P&ID** and then select **Uninstall**.

To uninstall a previous Service Pack, select the appropriate row in the list of installed programs.

1. At the message prompt that displays, select **Yes** to confirm removal of the software.
2. Select **Finish** on the** Maintenance Complete** page.

**Install Smart P&ID**

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

15/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Licensing software is required for concurrent licensing for both the core Smart P&ID product and for each feature, therefore you must install and configure Intergraph Smart Licensing on your workstation before installing Smart P&ID. This licensing software is delivered on its own media. For more information about using and configuring concurrent licensing, refer to the licensing software documentation.

If you previously uninstalled a SmartPlant P&ID 2009 SPx Hot Fix, you must run the CleanUp Utility before installing the current version of Smart P&ID. To download and run this utility, go to Smart Community <https://hexagon.com/support-success/asset-lifecycle-

intelligence/community> , type **20488** under **Find the answer to your question**, and follow the instructions.

1. Navigate to the Smart P&ID DVD layout folder. Double-click **setup.exe** in the main folder.
2. On the **Welcome** page, select the **Additional Software** link to perform any of the following installations:

Smart P&ID Reference Data

Intergraph Smart Engineering Manager

Intergraph Schematic Scheduler

Intergraph SmartPlant (.NET)

Intergraph SmartPlant (COM)

Make sure you have administrator privileges on the workstation to install the additional software.

1. After installing additional software and closing the setup, select **Back** on the **Additional Software** page, to continue with the installation of Smart P&ID.
2. To install Smart P&ID, select **Start Setup**.
3. On the **Details and Features** page, enter your user name and company details. By default, the user name and company name are obtained from the registry. You can change the values, but you cannot leave these fields blank.

For an evaluation copy of the software, these fields are mandatory.

1. Enter your product serial number.
2. Under **Select Features to Install**, choose whether to install Smart P&ID, Smart P&ID Engineering, or Smart P&ID Share Service.

The Drawing Manager is always installed with Smart P&ID or Smart P&ID Engineering.

The Smart P&ID Share Service enables integration with HxGN SDx2. It is not necessary to install Smart P&ID and Share Service simultaneously. You can install the Share Service later. See Integration with HxGN SDx2.

1. In the **Install Path** field, accept the default installation path or specify a different path, and then select **Next**.
2. On the **License Agreement** page, select your country or region from the list to view the license agreement in your language, and then select **I agree to the license agreement and conditions**.
3. Select **Install**.
4. When installation completes, select **View Readme** to open the Readme file.
5. Select **Finish** to close the installation wizard.

If you try to install Smart P&ID software when you do not have write permissions to the registry on the computer on which you are installing, a warning message appears. See Grant Permissions to Write to a Registry Key in the Smart P&ID Installation and Upgrade

Help.

The driver used for printing the PDF files, Amyuni 6.0.3 PDF Converter, is included in the Smart P&ID installation. This printer is used for PDF generation and should not be removed or used for any other purpose. If you are unable to generate PDF files because this https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

16/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

driver is missing, restore the driver by running the executable file *InstallPDFConverter.exe*, which is installed by default in the software installation folder path ..\SmartPlant\P&ID Workstation\bin.

**Install or modify Smart P&ID Select Features**

You can install these **Select Features** at any time if they were not installed during the Smart P&ID initial installation: **Insulation Manager**

**Options Manager**

## **Rule Manager**

**Smart P&ID Share Service**

## **To Install**

1. Go to the Windows

**Start** button.

1. Open the **Control Panel > Programs > Programs and Features**.
2. Select **Smart P&ID** from the list and then select **Change**.
3. Select **Modify** on the Setup **Modify** page.
4. Select **Add or Remove Features** on the **Modify/Uninstall** page and then select **Next**.
5. From the **Select Features to Add or Remove** section, select any or all of the features to install, and then select **Update**.
6. Select **Yes** on the **User Account Control** dialog.
7. When the process completes, select **Finish**.

**Install Intergraph Smart® 3D S3DPIDClient**

To use the Piping Specification Utility with Smart 3D, you must install Intergraph Smart® 3D S3DPIDClient.

Before installing Smart 3D S3DPIDClient.exe, you must uninstall any previous installation of this software.

1. Go to the Smart Community [https://hexagon.com/support-success/asset-lifecycle-intelligence/community](https://hexagon.com/support-success/asset-lifecycle-intelligence/community) site, and download the

install files and start the installation.

Ensure that S3DPIDClient.exe version is same as that of Smart 3D.

1. On the **Welcome** page, select the the **Additional Software** link to open the **Additional Software** page.
2. Select **Intergraph Smart 3D S3DPIDClient** to open the installation wizard.
3. Select **Next** on the **Welcome** page.
4. Choose your country from the list on the **Software License Agreement** page.
5. View and read the license agreement and then close the **Software License Agreement** window.
6. Select **Yes** to accept the license agreement.
7. On the **Destination Folder** page, accept the default installation path or specify a different path, and then select **Next**.
8. Select **Install** on the **Ready to Install Intergraph Smart 3D S3DPIDClient** page.
9. When installation completes, select **Finish** to close the installation wizard.

**Modify or Uninstall the Latest Version of Smart P&ID**

1. Select **Control Panel > Programs and Features**.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

17/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

1. From the list of installed programs, select **Intergraph Smart P&ID 12** and then select **Change**.
2. Select **Modify** on the page that displays.
3. On the **Modify / Uninstall** page, select one of the following options: **Add or Remove Features**

**Repair**

## **Uninstall**

1. Select **Next**.

If you select **Repair** or **Uninstall**, a wizard page opens with progress bars for the overall process and individual details.

1. If you select **Add or Remove Features**, select the check boxes beside those features to add, and clear the check boxes beside those features to remove.
2. Select **Update**.

The **Add or Remove Features** option only adds or removes the additional features; it does not remove Drawing Manager or Smart P&ID / Smart P&ID Engineering.

1. Select **Finish** when the process completes.

**Installing Smart P&ID in Silent Mode**

Silent mode installation involves running a command at the command prompt with arguments specifying the license activation, product serial number, and installation path. In addition, you can specify which individual software features to install and the path of the log file.

## **Prerequisites**

Smart P&ID installation requires licensing software for concurrent licensing. Install the licensing software on your workstation and on every other workstation before installing Smart P&ID in silent mode. For more information about installing and configuring licensing software, see Intergraph Smart Licensing Installation and Setup.

Ensure there is sufficient disk space on each workstation for the installation. See Smart P&ID Workstation.

Before installing a new release, uninstall all previous versions of Smart P&ID.

Ensure no folder with the same name exists where Smart P&ID will be installed.

Close all the applications.

**Install Smart P&ID in Silent Mode**

## **General Command Syntax**

At each workstation where you want to install the software, open **Command Prompt** as an administrator and enter the command according to the following syntax:

“\SPID_setup.exe” {/install | /modify | /repair | /uninstall} /silent

[INSTALLFOLDER=“”] [/log “.log”] SLAACCEPT=YES [ADDLOCAL=“”] [REMOVE=“”] SERIALNUM=“” [USERNAME=“”]

[COMPANYNAME=“”] [PIDMODE=]

Command line arguments and their values are case-sensitive.

Ensure the command line includes spaces before and after the arguments, as shown in the syntax and examples.

Restart the workstation after installation.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

18/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

The setup stops and logs an error if a mandatory argument is missing or incorrect. After installation, check the log file to ensure that the installation proceeded without errors. If the silent installation is successful, the log file ends with: Exit code: 0x0

**What are the available features?**

**Basic features or the default features**

Drawing Manager

Smart P&ID or Smart P&ID Engineering

## **Optional features**

### Options Manager

Insulation Specifications Manager

Rule Manager

Smart P&ID Share Service

**Argument**

**Mandatory**

## **Description**

\SPID_setup.exe

{/install | /modify | /repair |

No

Choose one of the arguments.

/uninstall}

If you skip this argument, the default

action is to install.

/silent

Yes

Runs the process in silent mode without the user

interface.

INSTALLFOLDER=“”

No

Specifies the installation folder. If you do not

specify, the setup installs the software at the

default location.

/log “<log file path and

No

Specifies the path and the name of the log file.

name>.log”

SLAACCEPT

Yes

Automatically accepts the software license

agreement.

Accepted value: YES

ADDLOCAL=“”

No

Specifies which features to install or modify. Use

it with /install or /modify arguments.

Accepted values: ALL, SPPID,

INSULATIONMGR, OPTIONSMGR, RULEMGR,

SPIDShareService

You can list one or more features separated by

commas. For example, ADDLOCAL=“Feature1,

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

19/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Feature2”

ALL installs basic and optional features.

If you skip this argument, by default the

setup installs Drawing Manager and Smart

P&ID or Smart P&ID Engineering

depending on PIDMODE.

SERIALNUM=“”

installation.

USERNAME=“”

No

Specifies the username. This argument is

mandatory when installing an evaluation version.

COMPANYNAME=“<name of the

No

Specifies the company name. This argument is

company>”

mandatory when installing an evaluation version.

PIDMODE=

No

Specifies the installation mode.

Accepted values: 0 or 1

0 installs Smart P&ID

1** **installs Smart P&ID Engineering

If you skip this argument, by default the

setup installs Drawing Manager and Smart P&ID.

REMOVE=“”

No

Specifies which optional features to skip or

remove when modifying an installation. Use it

with the /modify argument.

Accepted values: INSULATIONMGR,

OPTIONSMGR, RULEMGR, SPIDShareService

You can list one or more features separated by

commas. For example, REMOVE=“Feature1,

Feature2”

## **Silent Mode Installation Example Scripts**

You can prefix the arguments with a hyphen (-) or a forward slash (/) where required. For example, use /install or -install.

You can use %temp% in the log file path to create the log file in the active user’s local **Temp** folder.

You can add pause at the end of your command or script. This is useful for confirming that a process has completed successfully before proceeding to the next step.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

20/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Install Smart P&ID with all available features**

“\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “%temp%\Install.log” SLAACCEPT=YES ADDLOCAL=“ALL” SERIALNUM=“0123456789”

PIDMODE=0

pause

**Install Smart P&ID**

\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “C:\Install.log” SLAACCEPT=YES ADDLOCAL=“SPPID” SERIALNUM=“0123456789” PIDMODE=0

pause

**Install Smart P&ID Engineering with all available features**

\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “%temp%\Install.log” SLAACCEPT=YES ADDLOCAL=“ALL” SERIALNUM=“0123456789”

PIDMODE=1

pause

**Install Smart P&ID Engineering**

\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “%temp%\Install.log” SLAACCEPT=YES ADDLOCAL=“SPPID” SERIALNUM=“0123456789”

PIDMODE=1

pause

## **Install specific features**

\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “C:\Install.log” SLAACCEPT=YES ADDLOCAL=“OPTIONSMGR,RULEMGR”

SERIALNUM=“0123456789” PIDMODE=0

pause

## **Install evaluation version**

\\Smart P&ID\Setup Files\SPID_setup.exe” /install /silent INSTALLFOLDER=“C:\Program Files (x86)\SmartPlant” /log “%temp%\Install.log” SLAACCEPT=YES ADDLOCAL=“ALL” SERIALNUM=“0123456789”

USERNAME=“RisingStar42” COMPANYNAME=“Intergraph” PIDMODE=0

pause

## **Modify product features**

\\Smart P&ID\Setup Files\SPID_setup.exe” /modify /silent /log “%temp%\Install.log” ADDLOCAL=“OPTIONSMGR”

REMOVE=“RULEMGR”

pause

## **Repair the product**

\\Smart P&ID\Setup Files\SPID_setup.exe” /repair /silent /log “%temp%\Install.log”

pause

## **Uninstall the product**

\\Smart P&ID\Setup Files\SPID_setup.exe” /uninstall /silent /log “C:\Uninstall.log”

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

21/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Pause

## **Working in Thin Client Mode**

You can use Smart P&ID in thin client mode, which supports Citrix. When you access the Smart P&ID application via Citrix, it is recommended that you do not perform any administration activities that run automatically for a long time on a client computer. When you execute administration activities via Citrix client, the software actually performs these activities on the server side, while the client remains idle, and the connection to Citrix is lost, possibly resulting in corruption of data. Examples of these types of administration activities are: upgrading the database to a new version. or importing a large number of drawings.

As a workaround, it is recommended that you perform these kinds of activities on a computer where Smart P&ID is installed or on a remote client computer using a configuration other than Citrix.

When using thin client mode, all users share a common database, resulting in intellectual property being shared between all sites.

**Comparison of Thin Client Mode and Smart P&ID Workshare**

For data sharing between sites, you can use Smart P&ID Workshare functionality or you can run Smart P&ID in thin client mode using Citrix XenApp.

**Using Smart P&ID Workshare**

Users on the host and on each satellite work in separate databases. This means that it is possible to segregate intellectual property between sites by transferring only the data that needs to be shared. When using Workshare, it is necessary to update reference data at remote locations and to move data between sites.

## **Using Thin Client Mode**

All users share a common database, so that there is no need to update reference data at remote locations or to move data between sites.

**Tuning the Software for Use in Thin Client Mode**

The following procedures describe special instructions for the installation of Smart P&ID when working in thin client mode on a Citrix computer. Tuning Smart P&ID involves performing the following operations: Installing Smart P&ID on Citrix.

Creating Global Objects.

Publishing the Smart P&ID program to enable it to be viewed on a web page or in a published Citrix application list.

## **Create Global Objects**

To run Smart P&ID via Citrix using Oracle, users or groups that will be using Smart P&ID are required to be included in the “Create Global Objects” policy security setting.

1. Open **Control Panel**, select** Administrative Tools**, and then double-click** Local Security Policy**.
2. In the left pane of the **Local Security Policy** window, expand **Local Policies** **> User Rights Assignment**.
3. In the right pane, double-click **Create global objects** to open the **Create global objects Properties** dialog.
4. Select **Add User or Group**.
5. On the** Select Users, Computers, Service Accounts, or Groups** dialog, add the users or groups that will be using Smart P&ID.

## **Publish Applications Using XenApp RDS**

You need to publish the application to allow you to view the data using a web page.

You must perform this procedure for each executable file for which you want to view data; for example, the Smart P&ID

Modeler (SmartPlantPID.exe), Drawing Manager (DrawingManagerEXE.exe), Options Manager (Options Manager.exe), Rule Manager (Rule Manager.exe), and so forth.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

22/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Smart P&ID and Smart P&ID Engineering cannot co-exist on the same computer, therefore they cannot both be published on the same Citrix server.

1. Select **Start** > **All Programs** > **Citrix** > **Citrix Studio**.
2. In the left pane, select **Delivery Groups**.
3. In the main window,

Select the **Delivery Groups** tab, select the groups, and then select **Create Application** in the **Actions** pane.

OR

Select the **Applications** tab, and then select **Add Applications** in the **Actions** pane 4. Select **Next** on the **Introduction** wizard page.

1. On the **Applications** page, select the check box beside each application you want to add and select **Next**.

If you want to add an application from a location other than the local computer, select **Add applications manually**, and then enter the required information in the **Add Applications Manually** dialog.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

23/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

1. Select **Finish** on the **Summary** page. When the publish operation successfully completes, the application displays under **Applications**.
2. Repeat the above steps for each application you want to publish.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

24/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Installing and Configuring Smart P&ID for Integration with Aspen Basic** **Engineering™**

For installation and configuration details to enable Smart P&ID 12 to work with ABE Integration, see Configuring Smart P&ID for Integration with Aspen Basic Engineering™.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

25/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Configuring Reference Data for Smart P&ID**

Smart P&ID Reference Data contains the symbols, rules, labels, styles, templates, insulation specification and other information that you use to create a P&ID. The default location for the reference data is ..\SmartPlant\P&ID Reference Data.

If the reference data is located elsewhere, use Smart P&ID Options Manager to identify the location of symbols, rules, labels, and other reference data for the application. You can also define symbology for graphics, default formats for data, and key distances that affect the behavior of the application. Usually, a project manager sets these options at the beginning of a project. The project manager seldom modifies these options except on rare occasions when project requirements dictate a change. See Customizing Your Reference Data.

If you are upgrading from a previous version of the software, you might also need to upgrade your reference data. See Upgrading Reference Data.

You do not need to set the default data locations in Options Manager before creating a P&ID in Drawing Manager. These locations are set at the time of plant structure creation. The drawing template path should be set to the correct node name and share name so that

the software can locate the templates for P&ID creation. See Install Smart P&ID Reference Data.

For a configuration in an integrated environment, be sure the **Smart Resource Path** setting in Options Manager points to the

..\SmartPlant Resources\ folder installed with the Smart P&ID reference data.

From Smart P&ID 2019 HF8, if you copied existing Smart P&ID reference data from another location; for example, when creating a new plant and P&ID application from custom templates, the CatalogExplorerSettings.bin file in the reference data folder must be deleted before any drawings are opened. This ensures that when a drawing is opened, the software creates a new CatalogExplorerSettings.bin file with updated file paths so that **Catalog Explorer** opens properly.

**Install Smart P&ID Reference Data**

1. Insert the Smart P&ID DVD into the drive. If the installation does not start automatically, double-click the product …_setup.exe file in the main folder.
2. On the **Welcome** page, select **Additional Software** to display the **Additional Software** page.
3. Select **Smart P&ID Reference Data** to open the Smart P&ID Reference Data Setup Wizard **Welcome** page.
4. Select **Start Setup** to start the reference data setup wizard.
5. On the **Details and Features** page, make sure that **Smart P&ID Reference Data** is selected under **Select Features to Install**.
6. Select the Smart P&ID Reference Data header text to display more options.
7. In the **Install Path** field, accept the default installation path or specify a different path.
8. Under **Optional Features**, select or clear the check boxes for the items as required and then select **Next**.
9. On the **License Agreement** page, select your country or region from the list to view the license agreement in your language, and then select **I agree to the license agreement and conditions**.
10. Select **Install**.
11. When installation completes, select **View Readme** to open the Readme file.
12. Select **Finish** to close the installation wizard.
13. After you install the reference data, share the folder that contains the reference data. Make sure that you grant all users Read permission to this share. Write permission to the share is required to make changes to the symbols, rules, templates, and other reference data.

We recommend that you make a copy of the reference data and store it with your plant files. This will help you with future service pack installations, data recovery, and so forth.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

26/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Upgrading Smart P&ID**

Most of the upgrade procedures are performed using the Smart Engineering Manager Upgrade Utility. This section deals with details of the procedures that apply to Smart P&ID only. For full details of the upgrade process, including actions required for Smart P&ID, refer to Upgrading the Database in the *Smart Engineering Manager Installation and Upgrade Help*.

When upgrading Smart P&ID to the latest version, you must have a compatible version of your database platform; therefore, if you have an older version of Oracle or SQL Server, you must upgrade it before upgrading Smart P&ID. For Oracle, both the server and the client must be upgraded.

Upgrade Prerequisites

1. Identify database constraint violations using the Database Constraint Report.exe delivered with the current version of Smart P&ID.
2. If your site database is Out-of-Date, upgrade it using Smart Engineering Manager and then if the application database is out of date, upgrade it using the Smart Engineering Manager Upgrade Utility. If you are using Workshare and have a satellite plant, upgrade that plant too.
3. Open and then close Smart P&ID Options Manager without running any commands. This action updates the RAD version for the ProjectStyles.spp file and as a result, changes the status of the Symbology for the drawings to ‘Out-of-Date’.
4. Update drawings as needed using Smart P&ID Drawing Manager.

To open an insulation spec (*.isl) from **File > Recent File List** after upgrading to Smart P&ID Version 12, clear the **Recent File List** of Smart P&ID Insulation Specification Manager from the **Registry Editor *:***

Computer\HKEY_CURRENT_USER\SOFTWARE\Intergraph\Applications\SmartPlantPID.application\InsulationMana File List

**Correcting Database Constraint Violations for Smart P&ID**

The** Database Constraint Report.exe** reporting utility delivered with your current version of Smart P&ID is used to help you identify whether the Smart P&ID data stored in your database is compliant with the database constraints. You must run this utility before you begin upgrading Smart P&ID.

## **Tasks for correcting constraint violations**

1. Make a complete backup of the data you are upgrading.
2. Generate a Database Constraint Exceptions Report. See Generate a Database Constraint Exceptions Report.
3. Clean up the database by removing orphan model items. See Clean Data Utility (DelOrpModItems.dll) in the *Smart P&ID Utilities* *Guide*.
4. Resolve constraint violations. See Using Constraint Utilities.
5. Generate a database constraint exceptions report again.
6. Run the appropriate constraint utilities again if any exceptions still exist.
7. Continue running the database constraint report and the constraint utilities until no exceptions are reported.
8. Make a complete backup of the now compliant data.

For additional information on resolving discrepancies listed in the database constraint report, contact your Customer Service representative.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

27/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Generate a Database Constraint Exceptions Report**

Use Smart P&ID or one of its manager applications to connect to the plant on which you want to run the **Database Constraint Exception** **Report** utility. If you use Smart P&ID to connect to the plant, be sure to close all drawings before proceeding. Microsoft Excel must be installed on any workstation from which you run the **Database Constraint Exception Report** utility.

1. In the ..\SmartPlant\P&ID Workstation\bin folder, double-click the **Database Constraint Report.exe** file to open the **Database** **Constraint Exception Report Utility** dialog.
2. Select **Connect to Active Plant**.

The utility runs the report on the active plant that you are connected to at the time. To run a report on another plant, connect to that plant using Smart P&ID or one of its manager applications.

1. After connecting to the database, select **Create Database Constraint Report**. This process can take several minutes, depending on the amount of data you have in your plant.
2. When complete, the utility automatically saves a copy of the report in the temp directory under your user profile and displays the file name (**plant name - ConstraintExceptions.xlsx**) in the list on the right side of the **Database Constraint Exception Report Utility** dialog.
3. Exit the **Database Constraint Exception Report** utility.
4. Open the report using Microsoft Excel and save a copy of the report to another location other than the Temp folder.
5. Review the completed report for discrepancies that must be resolved before you can upgrade to the new version of Smart P&ID. It is recommended to run this utility again until no discrepancies are reported.

## **Database Constraint Report Results**

The Database Constraint Report file is a Microsoft Excel file containing several worksheets.

The first sheet in the report is the **Report Progress Messages**, which contains a list of the constraint checks made and the number of violations detected for each constraint check. Each violation type displays on its own worksheet, with the name of the constraint violation displayed on the **Worksheet** tab.

Each worksheet also contains a list of drawings containing constraint exceptions, along with the name of the recommended constraint utility (usually in cell B1) to use in resolving the violation.

All constraint utilities, including the **Clean Data** utility (DelOrpModItems.dll), are run on an open drawing inside Smart P&ID. However, unlike all the other constraint utilities that run on a drawing-by-drawing basis, the **Clean Data** utility runs on the entire plant data set. If** Clean Data** is used to resolve any particular constraint violation, a particular drawing will not be specified in the report for this constraint violation nor will a utility name be listed at the top of the worksheet.

## **Using Constraint Utilities**

Before running any of the constraint utilities recommended by the database constraint report, run the **Clean Data** utility inside a blank drawing, then run the **Database Constraint Report.exe** again. Running **Clean Data** first decreases the number of exceptions listed in the report and lessens the amount of further manual data cleanup required. See Clean Data Utility (DelOrpModItems.dll) in the *Smart P&ID*

*Utilities Help*.

The remaining constraint utilities must be run from within specific drawings. These utilities are located in the ..\SmartPlant\P&ID

Workstation\bin folder, along with the **Clean Data** (DelOrpModItems.dll) utility.

Each plant might require a different set of utilities. Open each drawing listed in the** Database Constraint Report** and run the recommended macros on the drawing. You need to run only the macros listed in the report for that particular drawing.

## **Constraint Utilities**

Delivered with Smart P&ID, the following constraint utilities help you correct any database constraint exceptions reported in the **Database** **Constraint Exception Report**.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

28/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

In general, each utility attempts to repair the constraint violation. However, in some cases the violation cannot be cleaned up by the utility and the item is band-aided in the drawing. This situation is noted and logged in each utility’s corresponding log file. See Constraint Utilities Log

Files.

You must manually fix any band-aided item in a drawing by deleting the item and replacing it. If you have difficulty finding the band-aided items, select **Tools** > **Options** in Smart P&ID, then select the **Display as Printed** option on the **Options** > **General** tab.

## **cmdnotconnectedcomps.dll**

Repairs items that have a relationship to a pipe run or signal run (sp_piperunid or sp_signalrunid are not null), but are not referenced by a corresponding connector. If the relationship cannot be repaired, you must delete it and replace it.

## **cmdLPCheck.dll**

Checks for LabelPersist records pointing to a representation that does not exist. If the graphical label is watching a graphic, the database is updated to match, thus repairing the LabelPersist. If the label cannot be repaired, the utility band-aids it. You should delete and replace these band-aided items.

## **ConnectorItem12.dll**

Checks for connector records pointing to a symbol that does not exist. If the graphical connector is connected to a symbol, the utility repairs the connector by updating the database to match. If the connector cannot be repaired, the utility band-aids it. You should delete and replace these band-aided items.

## **OPCFK.dll**

Checks for OPC records with a partner that does not exist. If the graphical OPC exists, fix it. You should delete these items.

## **PointIndexCheck.dll**

Checks for piping point records and signal point records with non-unique indices or point numbers, then repairs the item by deleting from the database whichever one of the duplicate points is not loaded into the cache.

## **RepairBadConnector.dll**

Checks for connectors with the same start and end objects and connectors with the wrong number of vertices. The utility band-aids the graphical connector, which you should delete.

## **RepairNullFileNameCmd.dll**

Checks for LabelPersist records with a null file name value.

If the number of LabelPersist records equals the number of SmartLabel objects locked to the watched symbol, the utility repairs the LabelPersist record by updating the filename value for the LabelPersist.

If the number of LabelPersist records does not equal the number of SmartLabel objects locked to the watched symbol, then the utility band-aids the watched symbol. You should delete band-aided items.

For the remaining LabelPersist records with a null filename, if the graphic exists, the utility band-aids it. You should delete band-aided items. If the graphic does not exist, the utility deletes the representation from the database.

## **RepairOrphanedNozzleCmd.dll**

### Checks for the following situations:

## **Nozzle records without a Parent**

If the Nozzle graphic is not in the drawing, the utility repairs the nozzle by setting the Instockpile flag = True. If the Nozzle graphic is in the drawing, the utility tries to set either the SP_EquipmentID or SP_PartOfID based on the graphic relationship. The graphic parent must be an equipment or equipment component for the relationship to be re-established. If the relationship cannot be re-established, the utility band-aids it. You should delete band-aided items.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

29/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Nozzles associated via SP_EquipmentID to a Parent in the stockpile**

If the Nozzle graphic is not in the drawing, the utility repairs the Nozzle by setting the Instockpile flag = True. If the Nozzle graphic is in the drawing, the utility band-aids it. You should delete band-aided items.

**Nozzles associated via SP_PartOfID to a Parent in the stockpile**

If the Nozzle graphic is not in the drawing, the utility repairs the Nozzle by setting Instockpile flag = True. If the Nozzle graphic is in the drawing, the utility band-aids it. You should delete band-aided items.

**Nozzles that are a Part of a Run**

The utility clears the SP_PartOfID attribute. If the Nozzle graphic is not in the drawing, the utility repairs the Nozzle by setting the Instockpile flag = True. If the Nozzle graphic is in the drawing, the utility band-aids it. You should delete band-aided items.

## **Constraint Utilities Log Files**

Each constraint utility generates a log file, which records each action taken to correct the constraint violation. Log files are located at the path specified in your TEMP environment variable.

**Constraint Utility**

## **Log File**

cmdnotconnectedcomps.dll

RepairNotConnectedComps.log

cmdLPCheck.dll

RepairBadEmbLabelCmd.log

ConnectorItem12.dll

ConnectorItem12_Check.log

DelOrpModItems.dll (CleanDB)

SPDelOrpModItems.log

DBCleanup.txt

OPCFK.dll

OPC_OPC_FK.log

PointIndexCheck.dll

PointIndexConstraint_check.log

RepairBadConnector.dll

RepairBadConnector.log

RepairOrphanedNozzleCmd.dll

RepairOrphanedNozzles_.pid.log

RepairNullFileNameCmd.dll

RepairNullFileNameCmd.log

**Post-Upgrade Tasks**

After you complete all the upgrade tasks for a plant, make a full backup of the upgraded databases.

Some or all of the following post-upgrade tasks might also be required:

Back Up Each Upgraded Plant

Preserve Software Customizations

Update Symbology Definitions in Smart P&ID Options Manager https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

30/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Make Additional Changes for Smart P&ID

Upgrade SmartFrames in Smart P&ID Options Manager

The requirement to upgrade SmartFrames applies if your plant was upgraded from 2014 R1 (or earlier). The **Upgrade SmartFrames** command is available in Smart P&ID 2019 HF16 and later and in Smart P&ID 10 HF5 and later. The instructions for enabling and executing **Upgrade SmartFrames** command display in the *Upgrade SmartFrames Command - DM-PB-253661.pdf*  document in the **Additional Files** folder of the hot fix package.

## **Back Up Each Upgraded Plant**

After you have completed the upgrade process for each plant, you should do the following: 1. Set the backup location for the plant in Smart Engineering Manager and perform a full backup. See Backing Up and Restoring Your Data in *Smart Engineering Manager*  Help.

1. Perform a complete database backup.
2. Perform a file system backup to archive the drawings, reference data, and other files.

## **Preserve Software Customizations**

The Upgrade Utility does not make changes that might overwrite user customization of display names, property formats, calculation programs, validation programs, or layouts. A data dictionary change made during an upgrade can cause layouts that use PipingPoint properties to have an incorrect caption or column heading. None of the default layouts delivered during installation include PipingPoint properties. However, if you added these properties to one of the default layouts or created a new layout with PipingPoint properties, you can manually revise the captions for any layouts that use PipingPoint properties after you upgrade by doing the following: 1. Open Smart P&ID.

1. In the list on the **Engineering Data Editor** toolbar, select the saved view that contains PipingPoint properties.
2. In the **Engineering Data Editor**, select **View** > **Edit View** to open the **Table Properties** dialog.
3. Select **Advanced**.
4. Select the **Layout** tab.
5. In the **Display Property** list, select the **PipingPoint** property.

PipingPoint properties start with the word *End*, such as **End**, **End 2**, **End 3**, and **End 4**.

1. Confirm that the caption is appropriate for the property.
2. If you need to modify the caption, make changes in the **Caption** box at the bottom of the **Advanced Table Properties** dialog.

## **Update Symbology Definitions**

In a plant that was upgraded from a version earlier than SmartPlant P&ID 2014, the new Ducting Symbology options appear at the bottom of the list and are assigned default color, width, and line pattern properties. The following procedure ensures that the new item types will receive the correct symbology properties.

1. Select **Start** > **Programs** > **Smart P&ID** > **Options Manager**.
2. Select the site and plant for which you want to update the symbology definitions.
3. Move the symbology definitions of the 3 ducting nozzle entries above the general nozzle symbology definitions.
4. Assign color, width, and line pattern properties as desired to all new ducting and room symbology definitions.

**Make Additional Changes for Smart P&ID**

After running the **Upgrade Utility**, you must still perform the following changes manually for the current version of Smart P&ID: https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

31/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Open and save the rules file so that the new rule options are added to the Rules.rul file.

Copy any new or modified symbols from ..\SmartPlant\P&ID Reference Data to the plant’s reference data, making sure that you do not overwrite any customizations.

## **Upgrading Reference Data**

Reference data often changes between versions of the software. These changes can include deletions and additions to reference data, as well as modifications to existing data formats and locations. After you upgrade your plant data using the Smart Engineering Manager Upgrade Utility, you can use the **Upgrade Reference Data** command in Smart P&ID Options Manager to upgrade styles, template files, symbols, and assemblies.

## **User Access**

Before you can upgrade the reference data and drawings for an upgraded plant, you must define user access for the plant in Smart Engineering Manager.See the *Smart Engineering Manager*  Help.

After you upgrade reference data, you cannot view it in earlier versions of the software.

For information about changes made during the reference data upgrade, see the **V4RefDataUpgrade.log** file. This log file is saved in the folder where the symbols are stored. See the Smart P&ID Options Manager Help.

To use Smart P&ID Share Service, ensure that **SPPIDSIODataMap.xml is** located under Smart Resource Path, See the Smart P&ID

Options Manager Help. This XML file is available as part of the Smart P&ID reference data installation.

## **Upgrade Reference Data**

1. Select **Start** > **Programs** > **Smart P&ID** > **Options Manager**.
2. Choose the site and plant for which you want to upgrade reference data.
3. Select **Tools** > **Upgrade Reference Data**. A splash screen displays. When the upgrade operation successfully completes, the software displays a message.
4. Select **OK**.

After you upgrade reference data, you should not view it in earlier versions of the software.

For information about changes made during the reference data upgrade, see the **V4RefDataUpgrade.log** file. This log file is saved in the folder where the symbols are stored.

For more information about upgrading reference data, see Smart P&ID Options Manager Help.

## **Upgrading Existing Automation Projects**

This section helps in creating or maintaining custom software for your company. As the specifics of custom software vary for each company, information in this section should be used for common tasks related to assessing impacts and making changes to custom software.

If your company uses custom software that relies on .NET APIs, then this upgrade might make the software inoperable.

Review the following topics to determine whether your custom software will be impacted, and if it is, the changes that need to be made to https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

32/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

keep it working.

**Handling Impact to Upgrade Existing Projects**

P&ID now contains changes to validation, calculation, and standalone applications depicted in the following flowchart: For continued COM support of validation and calculation technology in custom applications: Re-reference relevant COM-visible API components.

Rebuild COM components.

Make changes from Interop for COM components.

Create .NET wrappers that implement new Managed Extensibility Framework (MEF) approach for lightweight extensible applications and will be proxy for interops.

All the .NET API functionality (Llama, Plaice, PIDAuto, LMAutomationUtil) components are COM-visible. ProgIDs and GUIDs of those components are preserved. This approach provides minimum impact to clients already using P&ID Automation capabilities with the VB6

version of the product.

## **Upgrading Legacy COM Technology**

VB6 validation and calculation components are no longer supported and must be migrated to .NET.

No impact to Excel report templates - not required to reopen. Template references will automatically get a new reference to Llama.tlb, instead of Llama.dll.

Third-party applications that are using SPPID Automation components should be reopened and recompiled to the product installation path.

**Upgrading Interop .NET Components or .NET Third-Party Technology**

## **Validation and Calculation**

Replace references for Interops to use new component (InteropLlama.dll->Llama.dll).

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

33/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Replace Namespaces, accordingly.

Validation implements at least one of the following interfaces: ILMForeignCalc, IPrintValidation, or ITransformUI. Add attributes to all validation projects:

[PartCreationPolicy(CreationPolicy.NonShared)]

[Export(typeof(ILMForeignCalc.ILMForeignCalc))]

[Export(typeof(ILMForeignCalc.IPrintValidation))]

[Export(typeof(ILMForeignCalc.ITransformUI))]

[ProgIDsExport(ILMForeignCalcProgID = “ItemTag.ItemTagFunc”, IPrintValidationProgID = ““, ITransformUIProgID =”“)]

The [ProgIDsExport] attribute will contain the ProgID for each interface that was implemented in the class; otherwise, it will remain empty.

Compile DLL to installationPath\Validation folder.

**Out-of-Process Applications**

Replace references for Interops to use new component (InteropLlama.dll->Llama.dll).

Replace Namespaces, accordingly.

Compile executable to installationPath folder.

Reference other files: InteropigrWrapperHelper.dll, InteropISPClientData3V2.dll, and SPPIDLateBind.dll.

**External Client Programs (.exe)**

Client applications cannot use core product components.

Out-of-process functionality is no longer supported, for example, as previously implemented for making changes to drawings, such as placing symbols. Now, external standalone customized programs must be updated to use PIDAuto.dll first to open P&ID.

## **Upgrading Automation**

Using SPID (RAD) commands in automation is not supported. Previously-created automation that includes SPID commands must be modified to use only SPID API components. We cannot assist you with problems that stem from the use of SPID commands in automation. This includes not only problems with the automation itself, but also problems with your company’s SmartPlant P&ID

implementation or data. The results of continuing to use the SPID commands can be catastrophic, including irretrievable data loss.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

34/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Updating Drawings**

Changes are often made to the Smart P&ID Reference Data while work is being managed on the P&IDs. When these changes are made, they apply to all drawing items after the time of change, but do not apply to existing drawing items. The Update Drawings functionality (provided by the set of Out-of-Date Drawings commands in Drawing Manager) allows you to manage which drawings are updated with the latest reference data changes by defining values that define out-of-date drawings criteria and by resolving any symbols that have been deleted, moved, or renamed.

You can also schedule these update operations and create reports. See Updating Drawings in *Drawing Manager Help*.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

35/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **User Access**

User access identifies the users allowed to work at specified access levels within the site and related plant structures. With user access, administrators can control access to data and thereby ensure the security of their project data.

Smart Engineering Manager incorporates user access as an integral product feature by using roles to define and maintain user privileges and rights at the plant structure level, where each application has its own set of rights. Roles are the primary focus, with each role associated to a single Windows user group. Each role is then assigned specific rights for each engineering application and for Smart Engineering Manager.

To see the roles currently defined for a plant, select the **Roles** node under the plant node in the **Tree** view.

To view the rights settings for a particular role, right-click the role in the **List** view and select **Properties**.

**Mutually-Exclusive Rights**

User rights can vary from one plant to another in the same site. These rights are defined by categories. Categories with radio button options indicate that the rights contained within are mutually exclusive, meaning you can choose only one right in that category to apply to the role. In other categories, you can choose multiple rights, as denoted by check boxes.

## **None**

The user is not allowed to execute the application or utility for this plant structure.

**Read-Only**

The user can execute the application or utility for this plant structure to view the data held within it.

## **Modify Settings**

The user can execute the application or utility for this plant structure to view the data held within it and to modify any custom settings.

## **Full Control**

The user can execute the application or utility for this plant structure and perform all commands and modifications. This right is not available to a satellite site when operating in the Workshare mode because the reference data must be controlled by the host site.

Smart Engineering Manager provides roles templates to help you easily create new roles. Because the most labor-intensive part of a role creation is setting the values for the rights, you can create templates for specific roles and then use those templates multiple times. This feature is useful for defining a role template in one site and then reusing that same role template throughout all your sites.

**Smart P&ID User Rights**

If you modify properties on the **Rights** tab, you must execute the **Refresh Users** command to properly update the site administrator group and plant structure roles.

**Category**

## **Options and Descriptions**

### Catalog

**None** prevents users from accessing Catalog Manager.

**Read-Only** allows users to view symbols in Catalog Manager, but not make changes.

**Full Control** allows users to create new symbols and edit existing symbols.

**Full Control** is disabled for Workshare satellites and projects.

Plant Filters

**None** prevents users from accessing Filter Manager.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

36/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Read-Only** allows users to view existing filter definitions, but not make changes.

**Full Control** allows users to create new filters and edit existing filters.

**Full Control** is disabled for Workshare satellites and projects.

Display Sets

Controls the ability to view, edit, and define plant display sets.

**None** prevents users from accessing display sets.

**Read-Only** allows users to view and apply existing display sets, but not make changes. This option also allows users to copy plant display sets to the **My Display Sets** folder.

**Full Control** allows users to apply, create, edit, and delete plant display sets.

The options affect plant display sets only. There are no restrictions for display sets under the **My Display Sets** folder, regardless of the option selected.

**None** allows users to clear a previously-applied plant display set.

**Full Control** is disabled for Workshare satellites.

Default Views

Controls the ability to specify default filters and layouts for item types. Also controls setting the Brief/Bulk Lists associated with item types.

**None** allows users to view existing default filters, layouts, and Brief/Bulk Lists definitions, but not make changes to the layout. Users can define and apply ad-hoc filters.

**Read-Only** allows users the same rights as the **None** option.

**Full Control** allows users to create, edit, and delete default filters, layouts, and Brief/Bulk Lists definitions.

**Full Control** is disabled for Workshare satellites and projects.

Plant Reports

**None** prevents users from accessing the plant reports.

**Read-Only** allows users to view existing report definitions, but not make changes.

**Full Control** allows users to create new plant reports and edit existing reports.

**Full Control** is disabled for Workshare satellites and projects.

Rules

**None** prevents users from accessing Rule Manager.

**Read-Only** allows users to view existing rule definitions, but not make changes.

**Full Control** allows users to create new rules and edit existing rule definitions.

**Full Control** is disabled for Workshare satellites and projects.

Data Dictionary

**None** prevents users from accessing Data Dictionary Manager.

**Read-Only** allows users to view settings in the data dictionary, but not make any changes.

**Modify Select Entry** allows users to edit select lists. **Modify Select Entry** is disabled for Workshare satellites and for projects.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

37/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Full Control** allows users to add items and edit existing items in the data dictionary.

**Full Control** is disabled for Workshare satellites and for projects.

Options

**None** prevents users from accessing Options Manager.

**Read-Only** allows users to view option settings, but not make any changes.

**Modify Settings** allows users to change reference data pointers. Users must have at least **Modify** **Settings** level privileges to be able to use Workshare.

**Full Control** allows users to add options and edit existing options.

**Full Control** is disabled for Workshare satellites and for projects.

Insulation Specifications

**None** prevents users from accessing Insulation Specification Manager.

**Read-Only** allows users to view insulation settings, but not make any changes.

**Full Control** allows users to add settings and edit existing insulation settings.

**Full Control** is disabled for Workshare satellites and for projects.

Drawing Management

**Create P&ID** allows users to execute the **New Drawing** command in Drawing Manager.

**Delete P&ID** allows users to execute the **Delete** command in Drawing Manager.

**Refresh P&ID** allows users to execute the **Compare and Refresh** and **Validate** commands in Smart P&ID. Users must also have Full Control permission for P&ID Objects before they can refresh a drawing.

**Create Version** allows users to execute the **Create Version** command in Drawing Manager.

**Delete Version** allows users to execute the **Delete Version** command in Drawing Manager.

**Fetch Version** allows users to execute the **Fetch Version** command in Drawing Manager.

**Edit Import Map** allows users to execute the **Edit Import Map** command in Drawing Manager.

**Update P&ID** allows users to execute the **Update** command in Drawing Manager to update existing drawings.

**Create Revision** allows the user to create revision properties, modify revision properties, and associate revision properties with the revised drawing. For this option to work, **Create P&ID** must also be selected.

**Delete Revision** allows the user to delete a revision and its associated version.

P&ID Objects

**None** prevents users from creating, opening, printing, or performing other actions on drawings or drawing objects in the Smart P&ID environment.

**Read-Only** allows users to view drawings in the Smart P&ID environment, but not make any changes. With this setting, users are allowed to apply plant display sets and filters but not create or modify them.

**Modify Properties** allows users to make changes to plant item properties in the **Properties** grid or the EDE but not to place, delete or manipulate plant items. This setting also allows import of properties; for example, by importing a report.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

38/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Full Control** allows users to perform all actions related to drawings and drawing objects. This setting is required to enable users to refresh drawings.

Workshare

**Publish** allows users to publish drawings to other satellites or back to the host.

**Get Latest Version** allows users to obtain the latest published drawing from the host or satellite site.

**Assign Drawing Ownership** allows users to specify which Workshare sites have read/write permission for published drawings.

**Synchronize Reference Data** allows users to update their reference data with the reference data at the host.

**Synchronize Shared Items** allows users to update their shared items with the shared items at the host.

Projects

**Check Out** allows users to execute the **Check Out** and **Undo Check Out** commands in Drawing Manager.

**Check In** allows users to execute the **Check In** command in Drawing Manager.

**Fetch** allows users to execute the **Fetch** command in Drawing Manager.

**Change Status** allows users to interact with the **Project Status** dialog in Drawing Manager. If you are not granted this right, you can only view the project status, but cannot modify it.

**Claim** allows users to execute the **Claim** and **Release Claim** commands in Smart P&ID.

Integration

**Publish** enables or disables document publishing. Select to enable; clear to disable.

**Retrieve** enables or disables document retrieval. Select to enable; clear to disable.

**Smart P&ID User Rights Examples**

The following examples are suggestions for granting rights to common groups of users. These examples are a great starting place for defining custom Smart P&ID role templates.

## **Plant Administrators**

This user group has full control over all aspects of the plant structure for drawings, administrative tasks, and reference data. The users should have the capability to create plant groups, add applications and roles, create projects, enable Workshare, and create satellites, but should not see the hierarchy templates or plant group types.

## **Plant Users**

This group has full control on all drawings, can set personal filters, set up personal display sets, set up My Reports, create drawings, and archive drawings (needed for personal use in case there are big changes to the drawing design).

## **Engineers**

This group has access to drawings to view and modify data reports but not graphics. They can set up personal filters, set up personal display sets, and create My Reports. They should not be able to modify any project reference data or perform any administrative tasks with respect to drawing management, projects, or Workshare activities.

## **Managers**

This group needs only view data access. They can set up personal filters, set up personal display sets, and create My Reports. They should not be able to modify any project reference data or perform any administrative tasks with respect to drawing management or Workshare activities.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

39/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Category**

**Administrators**

**Users**

**Engineers**

## **Managers**

### SEM Plant Structure

Full Control

Read-Only

Read-Only

Read-Only

Access

Catalog

Full Control

None

None

None

Plant Filters

Full Control

Read-Only

Read-Only

Read-Only

Display Sets

Full Control

Full Control

Full Control

Full Control

Default Views

Full Control

Read-Only

Read-Only

None

Formats

Full Control

None

None

None

Plant Reports

Full Control

Read-Only

Read-Only

None

Rules

Full Control

None

None

None

Data Dictionary

Full Control

None

None

None

Options

Full Control

None

None

None

Insulation Specifications Full Control

None

None

None

Drawing Management

Create P&ID, Delete P&ID

Create P&ID

Undefined (do not choose

Undefined (do not choose

anything)

anything)

P&ID Objects

Full Control

Full Control

Modify Properties

Read-Only

Workshare

Publish, Get Latest Version, Assign

Undefined (do

Undefined (do not choose

Undefined (do not choose

Drawing Ownership,

not choose

anything)

anything)

Synchronize Reference Data,

anything)

Synchronize Shared Items

Integration

Publish, Retrieve

Undefined (do

Undefined (do not choose

Undefined (do not choose

not choose

anything)

anything)

anything)

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

40/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Customizing Your Reference Data**

Several tools are delivered with Smart P&ID or with Smart Engineering Manager that allow you to customize your reference data.

## **Customize Reference Data Options**

Reference data options control the look and feel of the product and controls much of the data used throughout the life of a project. See the *Smart P&ID Options Manager Help*.

Use Smart P&ID Options Manager to define how you want particular P&ID items to appear in drawings by selecting colors, line styles, gapping styles, and heat tracing styles for the project.

1. Select **Start** > **Programs** > **Smart P&ID** > **Options Manager**.
2. Define the symbology, gapping, heat tracing, formatting, and distances as needed.
3. Select **Settings**.
4. Verify that all \\node\share entries are set to the shares defined during reference data installation.
5. Select **File** > **Save**.

## **Establishing Design Rules**

By defining typical or standard design rules, you can quickly and easily place required equipment, interconnecting piping, instrumentation, and other accessories on a drawing. hese rules define the placement characteristics of items and how items interact with each other. Using rules, you also confirm that you meet proper design criteria.

The Rule Manager provides the tools for creating and editing rules.

## **Working with Filters**

Filter Manager, delivered with Smart Engineering Manager, allows you to select the items to display in the engineering application. You can use this feature to clear the view of other items to display one class of items. See the Filter Manager help.

## **Working with Formats**

Format Manager, delivered with Smart Engineering Manager, allows you to define the characteristics and formats for labels, report data and formatted properties. You can also create and edit formats. See the Introduction to Format Manager help.

## **Working with Symbols and Labels**

Symbols include a graphic representation of the item as well as the properties associated with that item. Catalog Manager, delivered with Smart Engineering Manager, allows you to create and edit these symbols.

Some of the characteristics of a symbol include the graphic representation of the item, labels, heat tracing, the icon that represents the item in the Catalog Explorer, and the properties associated with the item.

Two types of labels display important information about drawing items:

## **Driving**

Sets the property in the model, for example, a dimension that changes the size of the object.

## **Driven**

Reports the property in the model, for example, a pressure label that takes its pressure value from the associated pump.

For more information about working with symbols and labels, see the Catalog Manager Help.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

41/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Modifying Data Model Properties**

Data Dictionary Manager, delivered with Smart Engineering Manager, allows you to modify the data model properties, including the database entries, select lists, and item types that form the underlying data structure. See the Data Dictionary Manager help.

With Data Dictionary Manager, you can perform the following tasks:

Add and change properties for specific database tables

Create select lists and add entries to them

Associate validation programs with various item types

Because your changes can affect the database for the entire project, only system administrators and project managers typically customize the database with Data Dictionary Manager.

## **Configuring Border Templates**

The delivered borders are embedded in the delivered template files. Before you can see modifications made to the drawing border during the course of a project, you must edit the delivered templates. If you do not modify the delivered template files, the borders of the drawings created with these templates are not modifiable on a global level. In other words, changes to border files do not show up in drawings that are using the embedded border template files. This means that you can change the border of drawings only on a drawing-by-drawing basis.

**Smart P&ID Delivered Templates**

Smart P&ID delivers the following border templates.

**Metric Templates**

**Template File**

**Border File**

## **Page Size**

A0-Size.pid

A0border.igr

A0 Wide (1189mm x 841mm)

A1-Size.pid

A1border.igr

A1 Wide (841mm x 594mm)

A1-Wide(Metric).pid

A1-Wide(Metric).igr

A1 Wide (841mm x 594mm)

A1-Wide Note Area.pid

A1-Wide Note Area.igr

A1 Wide (841mm x 594mm)

A2-Size.pid

A2border.igr

A2 Wide (594mm x 420mm)

A2-Wide(Metric).pid

A2-Wide(Metric).igr

A2 Wide (594mm x 420mm)

A2-Wide Note Area.pid

A2-Wide Note Area.igr

A2 Wide (594mm x 420mm)

A3-Size.pid

A3border.igr

A3 Wide (420mm x 297mm)

A3-Wide (Metric).pid

A3-Wide (Metric).igr

A3 Wide (420mm x 297mm)

A4-Size.pid

A4border.igr

A4 Wide (297mm x 210mm)

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

42/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

A4-Wide (Metric).pid

A4-Wide (Metric).igr

A4 Wide (297mm x 210mm)

A5-Size.pid

A5border.igr

A5 Wide (210mm x 148mm)

**English Templates**

**Template File**

**Border File**

## **Page Size**

A-Size.pid

A-Wide.igr

A Wide (11in x 8.5in)

A-Wide (Imperial).pid

A-Wide (Imperial).igr

A Wide (11in x 8.5in)

B-Size.pid

B-Wide.igr

B Wide (17in x 11in)

B-Wide (Imperial).pid

B-Wide (Imperial).igr

B Wide (17in x 11in)

C-Size.pid

C-Wide.igr

C Wide (22in x 17in)

C-Wide (Imperial).pid

C-Wide (Imperial).igr

C Wide (22in x 17in)

C-Wide Note Area (Imperial).pid

C-Wide Note Area (Imperial).igr

C Wide (22in x 17in)

D-Size.pid

D-Wide.igr

D Wide (34in x 22in)

D-Wide (Imperial).pid

D-Wide (Imperial).igr

D Wide (34in x 22in)

D-Wide Note Area (Imperial).pid

D-Wide Note Area (Imperial).igr

D Wide (34in x 22in)

E-Size.pid

E-Wide.igr

E Wide (44in x 34in)

## **Edit Delivered Templates**

Before editing the delivered templates, verify that the correct plant structure has been selected and that no drawings are open.

1. In **Windows Explorer**, browse to the default templates location defined in Options Manager or the location of the reference data of your plant.
2. Select the template that matches the system of units and page size requirements for the drawing and double-click the template file to open it in the Smart P&ID Modeler. Refer to the previous chart to determine the appropriate template and border files.

You also can drag the template file into the application window to open the template file.

1. Select the existing border file and press **Delete**.
2. Select **Edit** > **Insert** > **Object**.
3. Clear the **Link** check box. This ensures that the item will be embedded.
4. Select **Browse** and locate the border file to use. You can use the delivered border or choose another border.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

43/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

1. Select **Open**.
2. Select **OK** on the **Insert Object** dialog.
3. Position the border file in the template.
4. Select **File** > **Exit**.

## **Create a Border Template**

1. Open Smart P&ID.
2. Verify that the correct plant structure is selected.
3. Select **File** > **New Template**.
4. Select **File** > **Page Setup**.
5. Choose the sheet size in the **Standard** option and then select **OK**.
6. Select **File** > **Properties**.
7. On the **Units** tab, select a unit in the **Length**, **Angle**, and/or **Area Readout** boxes to specify the default units of measure, and then select **OK**.
8. Select **Edit** > **Insert** > **Object**.
9. Verify that **Link** is selected if you want the border file linked, or clear the **Link** check box if you want to embed the file.
10. Select the border to use, select **Open**, and then select **OK**.
11. Select **File** > **Save**.
12. Type the name for the template in the **File Name** box.
13. Save the template border in the default templates location defined in Options Manager.
14. Select **Save**.
15. Select **File** > **Exit**.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

44/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Customizing the Progress Bar**

You can customize the progress bar if you are an administrator or have the necessary permissions.

When you install a hotfix, the progress bar resets to classic. You must re-enable the new progress bar after installing the hotfix.

In Smart P&ID, you can choose between the classic and new progress bars.

The classic progress bar shows visual progress, whereas the new progress bar provides more comprehensive information by displaying the current operation or task being executed. In addition to visual progress, it includes a percentage completion indicator.

## **Enable the new progress bar**

1. Go to ..\SmartPlant\P&ID Workstation\bin folder and
2. Copy the **igrProgressBar412C.dll.config** file to your desktop or another location.
3. Open the config file using a text editor.
4. Change the value attribute from 0 to 1.
5. Copy the modified file back to the ..\SmartPlant\P&ID Workstation\bin folder.
6. Restart the application.

To switch to classic progress bar, change the value attribute back to 0.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

45/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Integration with SmartPlant Foundation**

Integration standardizes and improves the communication among the various authoring tools you use in the course of designing, constructing, and operating a plant. Integration manages data exchange among these authoring tools, which enables sharing and re-use of plant information throughout the plant life-cycle. SmartPlant Foundation acts as a repository for data and a medium through which information is shared among other tools, such as Smart Instrumentation, Smart Electrical, and Smart 3D.

Most integration commands are available on the **SmartPlant** menu in Smart P&ID Drawing Manager and **Integration** menu in Smart P&ID.

The following graphic displays what Smart P&ID publishes and retrieves and shows the flow of data and the different types of data.

Smart P&ID interacts with SmartPlant Foundation by correlating items between the plant database and the SmartPlant Foundation database by retrieving documents from SmartPlant Foundation. Also, Smart P&ID creates a set of tasks in the To Do List that you can run to update the plant database. In Smart P&ID, you can also use the commands on the **Integration** menu to publish documents and retrieve data, access SmartPlant Foundation to browse data, and subscribe to change notifications and compare documents.

You can only use the **Integration** menu commands after your plant is registered. See Registering Tools.

## **Integration with HxGN SDx2**

Integration with HxGN SDx2 includes two services that must be installed and configured: Intergraph Schematics Scheduler Service

Smart P&ID Share Service

**Smart P&ID Share Service and Intergraph Schematic Scheduler Service Overview** The** Intergraph Schematic Scheduler Service** is a separate software utility that monitors changes to plant items. Once you setup and start the scheduler service, the service synchronizes the changes with HxGN SDx2. Changes are then flagged for new, modified, or deleted plant items. Updates can then be shared with other Hexagon applications.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

46/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

The **Intergraph Schematic Scheduler Service** needs to be configured using the **Schematic Scheduler Configuration Utility**. Before you setup a site using the **Configuration Utility**, make sure that **Smart P&ID Share Service** is installed.

The **Smart P&ID Share Service** enables integration with HxGN SDx2 and runs in the background. It is available with Smart P&ID as a separate feature and is located in the **Select Features to Install** section of the **Smart P&ID** installation DVD. You can also install the Share Service using the **Windows Control Panel > Programs > Programs and Features**.

Here are the basic steps to setup and configure the services:

1. Ensure Smart P&ID Share Service is installed. See Install or modify Smart P&ID Select Features.
2. Install the Intergraph Schematic Scheduler.
3. Install Intergraph SmartPlant (.NET).
4. Configure the Intergraph Schematic Scheduler.
5. Start the Intergraph Schematic Scheduler Service.

The Smart P&ID Share Service, Intergraph Schematic Scheduler, and Intergraph SmartPlant (.NET) must be installed on the same workstation where Smart P&ID is installed.

To create enhanced mapping for integration, you must install Intergraph SmartPlant (COM) along with SmartPlant (.NET).

To use the Share Service with an Oracle client, you must install Oracle 64-bit client. The 64-bit Oracle client can coexist with the 32-bit client on the same host.

When an item is moved from the drawing to the plant stockpile and categorized under a plant group type - “Plant”, no relation will be established.

## **Install the Intergraph Schematic Scheduler**

Intergraph Schematic Scheduler and Smart P&ID must be installed on the same workstation.

1. Select **Intergraph Schematic Scheduler** to open the installation wizard.
2. On the **Welcome** page, select **Start Setup**.
3. Enter **User Name** and **Company**.
4. Under **Select Features to Install** section, select **All Features**.
5. If necessary, specify a different installation path.
6. Select **Next**, ** **and then select** I agree to the license agreement and conditions**.
7. Select **Install**, ** **and then select** Finish**.

**Install Intergraph SmartPlant (.NET)**

To use the Smart P&ID Share Service, you must install Intergraph SmartPlant (.NET).

1. On the **Welcome** page, select the **Additional Software** link to open the **Additional Software** page.
2. Select **Intergraph SmartPlant (.NET)** to open the installation wizard.
3. On the **Welcome** page, select **Start Setup**.
4. Ensure all the options are selected.
5. Select **Next**, ** **and then select** Finish**.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

47/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Configure the Intergraph Schematic Scheduler**

The** Intergraph Schematic Scheduler **contains the** Intergraph Schematic Scheduler Configuration Utility**.

Configuration of the Intergraph Schematic Scheduler is intended for IT administrators who manage the system’s hardware and software.

1. Go to the **Start**

menu on the Windows taskbar and scroll to** Intergraph Schematic Scheduler **folder**. **

1. Right-click **Configuration Utility**
- ***and select **Run as administrator**.
1. Select the **Product** tab, and then the required product:: **P&ID**, **SI**, or **SEL**.
2. Select **Add** from the **Product** tab on the bottom left panel.
3. In the **Open File** dialog, locate the Site’s connection **.ini** file. Select the file then select **Open.**
4. Enter the **Site Name** in the **Add New Site** dialog, and then select **Add**.
5. The . **INI Path** gets populated on the next page. For example, the path in Smart Electrical and Smart P&ID is:

” **\\Site_Server_Name\Shared_Sites\Site_Name\smartplantv4.ini**” and in Smart Instrumentation: ” **[drive]: \Program Files** **(x86)\SmartPlant\Instrumentation\Intools.ini**”.

The site you select must contain plants that are registered with HxGN SDx2.

1. On the **Synchronization to SDx** page, review the .INI** **file name that displays in the** INI Path** field.
2. Select **min** or **hr** in the **Interval** section and enter a numerical value in the box.

Minimum interval time is one hour and maximum interval time is 24 hours. Specify the default timing for querying the database for modifications.

1. Select

from the** Structure Provider Path. **

1. In the **Open File** dialog, navigate to the Share Service, which is located in the path where the Shared Service was installed. For example, [drive]: **\Program Files (x86)\SmartPlant\SPID** **Workstation\bin** folder. Select **HxGN.Schematic.I2.SPID.SiteInfoProvider.exe**.
2. Select **Save**.

## **Remove a Site**

1. Select from the **Product** tab in the bottom left panel.
2. Select **Remove,** in the **Alert** notification that opens.
3. Select **Save**.

## **Configure the Server tab**

Specify the following parameters for the server on which you are running the Smart P&ID Share Service.

1. Select the **Server** tab.
2. From the **Refresh Scheduler** section, choose the frequency from the **Schedule** box, as follows: Select **Monthly**, and then select a number from the **Time** box.

Select **Weekly**, and then select a day from **Day** box and a number from the **Time** box**.**

Select **Daily**, and then select a number from the **Time** box.

Selecting **None** disables the refresh schedule.

1. From the **Share Configuration** section, select a number from the **Max Number of Parallel Processes** box.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

48/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

The value you enter must not exceed the maximum number of core processors available on the server. To maintain optimal server performance, consider a plant for each process. In addition, take into account the value you enter in the **Data Chunk** size and **Document Chunk** size boxes, as well as the value in the **Max Number of Parallel Processes per Plant** box.

1. Select a number from the **Max Number of Parallel Batches** box.

The number of simultaneous batches that comprise web requests, which can be sent to the HxGN SDx2 server.

1. Enter a number for the **Max Number of Parallel Processes per Plant** box.

The number of simultaneous parts that a Plant scope (of documents and/or of Plant data) can process.

1. Enter a number for the **Max Batch Size** box.

Determines the size of batch, based on the Document/Data Chunk sizes.

1. Enter a number for the **Document Chunk Size** box.

Determines the number of documents to be published.

1. Enter a number for the **Data Chunk Size** box.

Determines the number of plant items to be published.

1. Select **Save**.

**Start the Intergraph Schematic Scheduler Service**

This service is turned off by default. It can be turned on or off.

1. Go to the Windows

**Start** button.

1. Open the **Control Panel > Administrative Tools > Services.**
2. Scroll to the** Intergraph Schematic Scheduler. **
3. Right-click and select **Properties** and from the **General** tab, set the **Startup type** to **Automatic (Delayed Start)**.
4. Select **Start** from the **Service status** section, and then select **OK**.

The Intergraph Schematic Scheduler service refresh frequency is run automatically once you start the service for the first time. This eliminates the need for manual start/stop actions. Any changes made to the JSON configuration file such as adding new sites, or updating server configurations will automatically trigger the scheduler to refresh and apply the new settings.

**Install Intergraph SmartPlant (COM)**

To create enhanced mapping for integration, you must install Intergraph SmartPlant (COM) along with Intergraph SmartPlant (.NET).

1. On the **Welcome** page, select the **Additional Software** link to open the **Additional Software** page.
2. Select **Intergraph SmartPlant (COM)** to open the installation wizard.
3. On the **Welcome** page, select **Start Setup**.
4. Ensure all the options are selected.
5. Select **Next**, ** **and then select** Finish**.

**Integration with SPF**

## **Prepare the Integrated Environment**

To enable Smart P&ID or Smart Electrical to work in an integrated environment, you must do the following: https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

49/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

1. Install SmartPlantClient.NET and Schema Component.NET, bundled and delivered with SmartPlant Foundation, on each Smart Engineering Manager and engineering application workstation. See Install Schema Component.NET.

Before you run **SmartPlant Client.NET and Schema Component.NET setup**, be sure to install the software prerequisites described in SmartPlant Foundation Desktop Client platform recommendations.

1. To create enhanced mapping for integration, you must install SmartPlant Client COM.
2. Use a hierarchy that contains a minimum of three levels when you create your plant in Smart Engineering Manager. In addition to requiring a minimum of three-levels in hierarchies, Integration configurations also require that the names of hierarchy items must not be

changed after they are created and that the hierarchy structure must not be modified after you create the project. See Using Custom

Hierarchies in an Integrated Environment.

1. Associate applications with and assign user access rights to your plant. When Smart P&ID and Smart Electrical are both enabled for a plant, they are both enabled for all projects in that plant. If a project requires only one of these applications, create separate plants for each application, then enable Smart P&ID for one plant and Smart Electrical for the other.
2. Edit the **Smart Resource Path** setting in Options Manager to point to the ..\SmartPlant Resources folder installed with the application’s reference data. The path specified in Options Manager must contain the tool schema .xml file to enable publish and retrieve operations between the tool and SmartPlant Foundation to work properly.
3. Register your plant with SmartPlant Foundation, as described in Register from Smart Engineering Manager in the *Smart Engineering* *Manager Help*.

When you register your plant, you must specify the location of the Smart Engineering Manager schema map file (SPEMDataMap.xml). See Specify Map File Dialog in the *Smart Engineering Manager*  help.

If only one application is associated with the plant at the time it is registered, only that application is registered. If another application is later associated with the plant, the **Register** command is enabled so that you can register the new application with the plant.

**Tool Requirements for Integrating Smart P&ID**

This topic describes rules and settings that allow Smart P&ID data to be shared correctly with Aspen Basic Engineering, Smart Instrumentation, Smart 3D, and the other tools that are part of an integrated environment. Other tools that are not listed here have no known Smart P&ID/integration issues.

## **General Integration Requirements**

The following is a list of *best practice* scenarios for using Smart P&ID so that data will migrate correctly to other tools: In general, when modifying P&IDs that have been published, avoid unnecessarily deleting items in order to move them inside the active drawing or moving them to other drawings. Deleting and replacing items (with the same tag), causes additional work in applications retrieving the P&IDs that might negate the time-saving benefits of the P&ID changes.

When working with Projects and As-Built, all instruments to be published must be placed on a P&ID drawing or in the active drawing stockpile. This is because the plant stockpile is not communicated back and forth between Projects and As-Built.

To enable publishing from a project, you must create a project in SmartPlant Foundation with the same name (case-sensitive) as the P&ID project.

When creating symbols, connection points (piping, signal, and auxiliary) must be added in the correct sequence. See the Important note at the end of Place Point Ribbon (Smart P&ID) in Catalog Manager Help.

Signal points and piping points are not supported for Equipment and Equipment Components when publishing to SmartPlant Foundation.

When creating formats for use with Smart P&ID publishing, the formats must be added and mapped in SPPIDDataMap.xml using Schema Editor. The UID string of the custom SPMapUOMDef map file must be of the form *SPMU__* , where ‘NN’

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

50/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

represents the SPMapUOMListDef ID for the format type (for example Temperature = 5; Pressure = 27). Because spaces or restricted characters are not allowed in the UID string, custom format names must not include spaces or restricted characters.

If you intend to publish select lists (enum lists) to SmartPlant Foundation, make sure that you review the SmartPlant Adapter for Smart P&ID Help to understand the requirements (see under *Data Transformation Logic* > *Publish/Retrieve*).

If the Smart P&ID item tag validation allows for duplicate tags, this might have an impact on downstream tools such as Smart Instrumentation, which does not allow duplicates. In such cases, allowing duplicates in Smart P&ID can cause problems in the retrieving tool.

By default, Smart P&ID item tag validation does not allow duplicate item tags for loops or instruments.

**Integration with Smart Instrumentation**

## **Retrieving Documents**

If a Smart P&ID drawing that includes items with a flow direction is to be retrieved by Smart Instrumentation, a flow direction of **End 1**

**Upstream** or **End 1 Downstream** must be defined in Smart P&ID. Bi-directional flow is not supported.

## **Connect to Process Lines**

**Connect to Process** lines are required for connecting instruments to equipment nozzles and pipe runs in Smart P&ID.

All non-piped offline equipment instruments must be connected to vessels through non-electric signal lines and nozzles in Smart P&ID. This enables Smart Instrumentation to recognize that instruments are connected to vessels.

If Smart P&ID assigns an object to an intermediate level in the hierarchy and publishes, Smart Instrumentation assigns the object to the level in the hierarchy in Smart Instrumentation determined by their logic. Because instruments belong to units in Smart Instrumentation, an instrument assigned to the intermediate level in Smart P&ID will be assigned to the unit in Smart Instrumentation. Panels will be assigned to the plant. Smart P&ID might get an update on retrieve to move the object to another level in the hierarchy than where it was published based on the move done automatically by Smart Instrumentation. Panels will move to the top level; instruments will move to the bottom.

## **Deleting and Adding Items**

When you are working in a Projects environment, and items are correlated using the SmartPlant integration tools, you should minimize deleting and re-adding any items. Smart P&ID reuses tag numbers in the numbering scheme when you delete and re-add items. Smart Instrumentation tracks tag numbers claimed in a project, and this tracking does not work if tag numbers are reused after correlation. If you must delete an item in this situation, you can delete the item to the Smart P&ID Stockpile.

## **Instrument Expansion**

A Smart P&ID instrument or loop tag does not always have a 1:1 relationship with instruments in Smart Instrumentation. In some cases, a single item tag in a P&ID corresponding to an instrument or loop needs to be expanded to create several instruments when publishing the data for Smart Instrumentation. For this purpose, the **Expansion Type** property in Smart P&ID specifies the expansion behavior when publishing an instrument or loop. Each value of the property corresponds to a Smart Instrumentation rule that determines which instrument types and numbers are to be created in Smart Instrumentation when the Smart P&ID tag is expanded and retrieved.

When retrieving data back to Smart P&ID, the behavior of a particular instrument created by expansion is determined by Smart Instrumentation parameters. For an expanded instrument, the state of the IRetrievableExpansion interface determines whether that instrument will be retrieved by Smart P&ID: if the IRetrievableExpansion interface is realized, the instrument is retrieved, whereas if the IRetrievableExpansion interface is *not* realized, the instrument is not retrieved. The ‘parent’ item tag is *always* retrieved, regardless of the realization state of the IRetrievableExpansion interface.

## **Ports**

Smart Instrumentation uses physical ports, while Smart P&ID uses logical ports. Smart Instrumentation publishes the physical ports with the Dimensional Data Sheets and not the Instrument Index. Smart P&ID retrieves the Instrument Index and does not retrieve the Dimensional Data Sheets.

When the workflow goes from Smart P&ID to Smart Instrumentation, followed by Smart Instrumentation publishing the Dimensional Datasheet, a Same As relationship is created between the ports in the SmartPlant Foundation database. That Same As relationship is required by Smart 3D to correctly match the design basis ports to the 3D representation of the ports.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

51/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

However, when the workflow goes from Smart Instrumentation to Smart P&ID, a Same As relationship is not created in the SmartPlant Foundation database. Without the Same As relationship created in the SmartPlant Foundation database, the result might be additional ports in Smart 3D. To obtain the Same As relationship on the ports requires that Smart P&ID publish the P&ID with the instrument, this P&ID be retrieved by Smart Instrumentation and then having Smart Instrumentation publish the Dimensional Data Sheet.

**Integration with Smart 3D**

## **General**

In Options Manager, ensure that under **Settings**, the **Use Piping Specification** setting value is **Smart 3D** even if the P&ID plant is not validating piping specifications. This is to ensure that the required Piping Component Select List entries are properly set to match the PIP

short codes expected by Smart 3D. See *Configure Piping Specification Settings* in Smart P&ID * * Options Manager User’s Help.

## **Drawing Items**

For Smart 3D to properly determine flow direction in a process run, that process run must be connected to at least 2 items.

Some items that can be represented as single objects in Smart P&ID, such as Vent Detail, are modeled in Smart 3D as a set of separate objects. For full correlation to be established between the two tools, ensure that these objects are modeled in Smart P&ID with the same configuration used to represent them in Smart 3D.

## **Properties**

Smart 3D handles temperature and pressure properties in pairs and does not support having a temperature (for example, Normal Operating Temperature) without defining the matching pressure (in this case, Normal Operating Pressure). While this is a valid condition for Smart P&ID, it should be a consideration when publishing for retrieval into Smart 3D. Without the Pressure / Temperature pair of values defined, the Smart 3D user will be required to enter a value that was not defined in Smart P&ID.

**Integration with Aspen Basic Engineering**

## **Retrieving Documents**

Basic Engineering data sheets can contain multiple objects and can be formatted in a traditional data sheet view or list view (for example, as an equipment list). Data sheets retrieved from Basic Engineering might include stream data, specialty piping data, or relief valve data as required by business practices.

**Using the Catalog Index in Smart P&ID and SmartPlant Integration**

When you select the **Retrieve** command, the software accesses the CatalogIndex.mdb and the system performs the following actions: 1. Using the retrieved document, the object type and classification of the retrieved item is determined.

1. Using the Smart P&ID Map file, the ItemTypeName (Equipment, PipeRun, PipingComp, Loops, and so forth), and codelist indices for Class, Sub-Class, and Type are determined.

## **Catalog Index Lookup**

The Catalog Index file is used to find a symbol in the catalog with type properties that match the given values. The lookup is performed using the most specific information first. If a match is found, that symbol is used. However, if there is no match, the more generic type information is used for additional searches. In this way, a generic symbol will be returned if no specific symbol is available in the catalog.

## **Search Based on Type Value**

Searches the catalog index for all rows with matching ItemTypeName and Type values and IsDefaultForType = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software performs the search based on Subclass.

## **Search Based on Subclass Value**

Searches the catalog index for all rows with matching ItemTypeName and SubClass values and IsDefaultForSubclass = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software performs the search based on Class.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

52/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **Search Based on Class Value**

Searches the catalog index for all rows with matching ItemTypeName and Class values and IsDefaultForClass = True. If one or more rows are found, the software uses the CatalogItemName from the first one. If no match is found, the software returns an empty string.

## **Mapping for SmartPlant Integration**

If you customize the plant database items or attributes in your Smart Engineering Manager plant, you must define the mapping between these customized plant attributes and the properties in the SmartPlant schema.

1. Open the plant data dictionary by right-clicking the plant in the Tree view in Smart Engineering Manager and selecting the Data Dictionary Manager Command.
2. Add or modify the attributes in Data Dictionary Manager for each level in your hierarchy. See Add a Property to Database Tables.
3. Open the plant SPEMDataMap.xml schema map file in the Schema Editor and map the plant database items between the tool schema (SPEMDataMap.xml) and the SmartPlant schema. See the Schema Editor Help.

If you add an enumerated list attribute to the plant data dictionary, see Hierarchical Enumerated Lists for information about mapping these complex data types.

The default SPEMdatamap.xml file contains the EF_SPAPlant attributes (CompanyName, SiteName, SiteLocation, DivisionName, and DivisionLocation). This file is delivered to the ..\Engineering Manager\SmartPlant Resources folder.

**Using Custom Hierarchies in an Integrated Environment**

Integration supports custom hierarchies, as long as they contain a minimum of three levels. By default, the delivered SPEMdatamap.xml file is compatible with the standard Plant > Area > Unit hierarchy.

After registering, Smart Engineering Manager cannot retrieve the PBS document if the plant and SmartPlant hierarchies are not compatible. To be compatible with the SmartPlant hierarchy, your plant hierarchy can contain less than or equal, but not more than the number of levels in the SmartPlant hierarchy.

Smart Engineering Manager retrieves from the SmartPlant hierarchy only the hierarchy levels it needs. For example, if your plant hierarchy contains 4 levels and the SmartPlant hierarchy contains 8 levels, only the top 4 levels of the SmartPlant hierarchy are retrieved.

All Smart Engineering Manager hierarchy item names (plant group names) below the plant (top level) must match the names in the SmartPlant Foundation plant hierarchy that are at the same level. The names are case-sensitive and therefore the cases must also match. The plant names do not have to match.

In addition to requiring a minimum of three-levels in hierarchies, Integration also requires that the names of hierarchy items must not be changed after they are created and that the hierarchy structure must not be modified after you create the project.

## **Register Command**

Registers a plant database, along with its associated applications, with an instance of SmartPlant Foundation. Each database must be registered before you can connect to SmartPlant Foundation to perform any specific tasks, such as publishing or retrieving files. You can register each plant database only once.

During registration, the software maps the plant database, all of its projects, and all of its associated applications to a single SmartPlant Foundation URL, which points to one SmartPlant Foundation plant database, and returns a unique signature for the tool/plant combination being registered.

You must install Intergraph SmartPlant (Schema Component and the SmartPlant Client), delivered with SmartPlant Foundation, on your Smart Engineering Manager workstation before you can register your plant.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

53/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

If only one application is associated with the plant at the time it is registered, only that application is registered. If another application is later associated with the plant, you must also register the new application with the plant.

After the plant is registered, the **SmartPlant** tab is added to the **Plant Structure Properties** dialog. The **SmartPlant** tab displays the SmartPlant Foundation URL, the SmartPlant Foundation plant database, and the unique application identifiers returned by the registration process.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

54/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

## **About Security and Encryption**

**What techniques are used for Encryption?**

Hexagon employs several encryption techniques to ensure that data is not exposed to unauthorized access. The following image details the standard encryption mechanisms:

Enabling encryption on a system or device has negligible impact on performance of the system.

## **Database encryption**

Transparent Data Encryption (TDE) is implemented on the standard database. TDE is where the database files on the server and any backups are encrypted. This ensures that external users cannot access or open files, backups, or hardware that could lead to the extraction of critical intellectual property data from the database without access to a decryption method.

TDE provides an additional layer of security by securing how the Database Encryption Key (DEK) can be accessed. The DEK is stored in the database boot record and can be accessed in two ways:

**Symmetrically** by using a Certificate stored in the master database of the server.

**Asymmetrically** by using Extensible Key Management (EKM).

**Communication encryption between application client and server**

Hexagon products use the Hypertext Transfer Protocol Secure (HTTPS) and Transport Layer Security (TLS) 1.2 to support encrypted communication between the application client and the server. In addition, encryption is enforced on the server so unencrypted connections https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

55/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

cannot be made by any client application.

## **Disk encryption**

For hard disks and data on the computer drives, Hexagon employs Azure Disk Encryption (ADE) which encompasses multiple technologies to encrypt data at rest. All Hexagon software that is run in a Windows environment uses BitLocker to ensure that drives cannot be read without the proper decryption keys. These keys are held in the Azure Key Vault and provide access only to trusted users.

## **File share encryption**

Files are protected as they are moved from the server to the client application using Server Message Block (SMB) Encryption, which is enabled on the server. SMB Encryption is the protocol supported by Windows as a way for two computers to transfer files and helps avoid unauthorized access to the data between them.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

56/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

**Support, Copyright, and Legal Information**

**Customer Support and Technical User Forum**

For the latest support information for this product, connect to Smart Community <https://hexagon.com/support-success/asset-lifecycle-

intelligence/community> . You can submit any documentation comments or suggestions you might have by logging on to our documentation

web site at https://docs.hexagonali.com [https://docs.hexagonali.com](https://docs.hexagonali.com/) .

To join in conversations about Smart P&ID, go to Technical User Forums <https://hexagon.com/support-success/asset-lifecycle-

intelligence/tuf> and join the **Engineering & Schematics TUF** group.

## **Hexagon Policy Against Software Piracy**

When you purchase or lease Hexagon’s Asset Lifecycle Intelligence division software, Hexagon, Intergraph, or its affiliates, parents, subsidiaries retains ownership of the product. You become the licensee of the product and obtain the right to use the product solely in accordance with the terms of the Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement and applicable United States and/or international copyright laws.

You must have a valid license for each working copy of the product. You may also make one archival copy of the software to protect from inadvertent destruction of the original software, but you are not permitted to use the archival copy for any other purpose. An upgrade replaces the original license. Any use of working copies of the product for which there is no valid Intergraph Corporation, doing business as Hexagon’s Asset Lifecycle Intelligence division, Software License Agreement constitutes Software Piracy for which there are very severe penalties. All Hexagon software products are protected by copyright laws and international treaty.

If you have questions regarding software piracy or the legal use of Hexagon software products, please call the Legal Department at 256-730-2362 in the U.S.

Updated June 2022

Document No. DDGL562C0

**Copyright Notice**

## **Copyright**

Copyright © 1999-2024 Hexagon AB and/or its subsidiaries and affiliates.

This computer program, including software, icons, graphic symbols, documentation, file formats, and audio-visual displays; may be used only as pursuant to applicable software license agreement; contains confidential and proprietary information of Intergraph Corporation or a Hexagon Group Company and/or third parties which is protected by patent, trademark, copyright law, trade secret law, and international treaty, and may not be provided or otherwise made available without proper authorization from Hexagon AB and/or its subsidiaries and affiliates.

## **U.S. Government Restricted Rights Legend**

Use, duplication, or disclosure by the government is subject to restrictions as set forth below. For civilian agencies: This was developed at private expense and is “restricted computer software” submitted with restricted rights in accordance with subparagraphs (a) through (d) of the Commercial Computer Software - Restricted Rights clause at 52.227-19 of the Federal Acquisition Regulations (“FAR”) and its successors, and is unpublished and all rights are reserved under the copyright laws of the United States. For units of the Department of Defense (“DoD”): This is “commercial computer software” as defined at DFARS 252.227-7014 and the rights of the Government are as specified at DFARS

227.7202-3.

Unpublished - rights reserved under the copyright laws of the United States.

Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division

305 Intergraph Way

Madison, AL 35758

## **Documentation**

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

57/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

Documentation shall mean, whether in electronic or printed form, User’s Guides, Installation Guides, Reference Guides, Administrator’s Guides, Customization Guides, Programmer’s Guides, Configuration Guides and Help Guides delivered with a particular software product.

## **Other Documentation**

Other Documentation shall mean, whether in electronic or printed form and delivered with software or on Smart Community, SharePoint, box.net, or the Hexagon documentation web site, any documentation related to work processes, workflows, and best practices that is provided by Hexagon as guidance for using a software product.

## **Terms of Use**

1. Use of a software product and Documentation is subject to the Software License Agreement (“SLA”) delivered with the software product unless the Licensee has a valid signed license for this software product with Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence Division (“Hexagon”), a Hexagon Group Company. If the Licensee has a valid signed license for this software product with Hexagon, the valid signed license shall take precedence and govern the use of this software product and Documentation. Subject to the terms contained within the applicable license agreement, Hexagon gives Licensee permission to print a reasonable number of copies of the Documentation as defined in the applicable license agreement and delivered with the software product for Licensee’s internal, non-commercial use. The Documentation may not be printed for resale or redistribution.
2. For use of Documentation or Other Documentation where end user does not receive a SLA or does not have a valid license agreement with Hexagon, Hexagon grants the Licensee a non-exclusive license to use the Documentation or Other Documentation for Licensee’s internal non-commercial use. Hexagon gives Licensee permission to print a reasonable number of copies of Other Documentation for Licensee’s internal, non-commercial use. The Other Documentation may not be printed for resale or redistribution. This license contained in this subsection b) may be terminated at any time and for any reason by Hexagon by giving written notice to Licensee.

## **Disclaimer of Warranties**

Except for any express warranties as may be stated in the SLA or separate license or separate terms and conditions, Hexagon disclaims any and all express or implied warranties including, but not limited to the implied warranties of merchantability and fitness for a particular purpose and nothing stated in, or implied by, this document or its contents shall be considered or deemed a modification or amendment of such disclaimer. Hexagon believes the information in this publication is accurate as of its publication date.

The information and the software discussed in this document are subject to change without notice and are subject to applicable technical product descriptions. Hexagon is not responsible for any error that may appear in this document.

The software, Documentation and Other Documentation discussed in this document are furnished under a license and may be used or copied only in accordance with the terms of this license. THE USER OF THE SOFTWARE IS EXPECTED TO MAKE THE FINAL

EVALUATION AS TO THE USEFULNESS OF THE SOFTWARE IN HIS OWN ENVIRONMENT.

Hexagon is not responsible for the accuracy of delivered data including, but not limited to, catalog, reference and symbol data. Users should verify for themselves that the data is accurate and suitable for their project work.

## **Limitation of Damages**

IN NO EVENT WILL HEXAGON BE LIABLE FOR ANY DIRECT, INDIRECT, CONSEQUENTIAL INCIDENTAL, SPECIAL, OR PUNITIVE

DAMAGES, INCLUDING BUT NOT LIMITED TO, LOSS OF USE OR PRODUCTION, LOSS OF REVENUE OR PROFIT, LOSS OF DATA, OR CLAIMS OF THIRD PARTIES, EVEN IF HEXAGON HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

UNDER NO CIRCUMSTANCES SHALL HEXAGON’S LIABILITY EXCEED THE AMOUNT THAT HEXAGON HAS BEEN PAID BY

LICENSEE UNDER THIS AGREEMENT AT THE TIME THE CLAIM IS MADE. EXCEPT WHERE PROHIBITED BY APPLICABLE LAW, NO

CLAIM, REGARDLESS OF FORM, ARISING OUT OF OR IN CONNECTION WITH THE SUBJECT MATTER OF THIS DOCUMENT MAY

BE BROUGHT BY LICENSEE MORE THAN TWO (2) YEARS AFTER THE EVENT GIVING RISE TO THE CAUSE OF ACTION HAS

OCCURRED.

IF UNDER THE LAW RULED APPLICABLE ANY PART OF THIS SECTION IS INVALID, THEN HEXAGON LIMITS ITS LIABILITY TO THE

MAXIMUM EXTENT ALLOWED BY SAID LAW.

## **Export Controls**

To the extent prohibited by United States or other applicable laws, Intergraph Corporation, Hexagon’s Asset Lifecycle Intelligence division (“Hexagon”), and a Hexagon Group Company’s commercial-off-the-shelf software products, customized software, Technical Data, and/or https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

58/59

3/19/25, 10:35 AM

Hexagon Documentation Site Export

third-party software, or any derivatives thereof, obtained from Hexagon, its subsidiaries, or distributors must not be exported or re-exported, directly or indirectly (including via remote access) under the following circumstances: a. To Cuba, Iran, North Korea, Syria, or the Crimean, “Donetsk People’s Republic”, “Luhansk People’s Republic,” or Sevastopol regions of Ukraine, or any national of these countries or territories.

1. To any person or entity listed on any United States government denial list, including, but not limited to, the United States Department of Commerce Denied Persons, Entities, and Unverified Lists, the United States Department of Treasury Specially Designated Nationals List, and the United States Department of State Debarred List. Visit www.export.gov for more information or follow this link for the screening tool: https://legacy.export.gov/csl-search [https://legacy.export.gov/csl-search](https://legacy.export.gov/csl-search) .
2. To any entity when Customer knows, or has reason to know, the end use of the software product, customized software, Technical Data and/or third-party software obtained from Hexagon, its subsidiaries, or distributors is related to the design, development, production, or use of missiles, chemical, biological, or nuclear weapons, or other un-safeguarded or sensitive nuclear uses.
3. To any entity when Customer knows, or has reason to know, that an illegal reshipment will take place.

Any questions regarding export/re-export of relevant Hexagon software product, customized software, Technical Data, and/or third-party software obtained from Hexagon, its subsidiaries, or distributors, should be addressed to Hexagon’s Export Compliance Department, 305

Intergraph Way, Madison, Alabama 35758 USA or at exportcompliance@hexagon.com. Customer shall hold harmless and indemnify Hexagon and a Hexagon Group Company for any causes of action, claims, costs, expenses and/or damages resulting to Hexagon or a Hexagon Group Company from a breach by Customer.

## **Trademarks**

Intergraph®, the Intergraph logo®, Intergraph Smart®, SmartPlant®, SmartMarine, SmartSketch®, Intergraph Smart® Cloud, PDS®, FrameWorks®Plus, I-Route, I-Export, Isogen®, Intergraph Spoolgen®, SupportManager®, SupportModeler®, SAPPHIRE®, TANK®, PV

Elite®, CADWorx®, CADWorx DraftPro®, GT STRUDL®, CAESAR II® , and HxGN SDx® are trademarks or registered trademarks of Intergraph Corporation or its affiliates, parents, subsidiaries. Hexagon and the Hexagon logo are registered trademarks of Hexagon AB or its subsidiaries. Other brands and product names are trademarks of their respective owners. Microsoft and Windows are registered trademarks of Microsoft Corporation. Other brands and product names are trademarks of their respective owners.

## **Copyright**

Copyright© Hexagon AB and/or its subsidiaries and affiliates. All rights reserved.

https://docs.hexagonppm.com/internal/api/webapp/print/04470623-c9df-4626-b4bd-c33d3a86d009

59/59