# HDS Product Management Implementation: Run Book Plan

**Offering:** Product Management (SCM) | **Release:** 26D | **Tasks:** 266 | **Functional areas:** 29

## How to use this document
1. Work top to bottom. Step numbers are the order FSCR will run the tasks.
2. The Run Book is only a plan. It has not been created in Oracle and no Fusion changes were made.
3. Before any step runs, a Fusion connection and your explicit approval are needed.
4. Mode: **assisted** = Claude helps, you confirm. **manual** = you do it in Fusion.

## Your requirements and where they land

| Requirement | Functional area(s) below |
|---|---|
| Items | Items; Item Organizations; Inventory Organizations; New Item Requests; Mass Update |
| Item Classification | Catalogs; Advanced Catalogs |
| Custom Attributes | Product Rules; Application Extensions; Data Quality Rules; Audit Trail |
| BOM | Advanced Product Structure |
| Change Orders | Change Orders |
| Documents | Product Development; Concept Design; Requirements and Ideas; Product Portfolio (to be confirmed) |
| Deviations | Quality Issue and Action (to be confirmed, may need a custom solution) |

## Summary by functional area

| # | Functional area | Tasks | Steps |
|---|---|---|---|
| 1 | Initial Users | 6 | 1-6 |
| 2 | Enterprise Profile | 9 | 7-15 |
| 3 | Users and Security | 24 | 16-39 |
| 4 | Application Extensions | 31 | 40-70 |
| 5 | Inventory Organizations | 24 | 71-94 |
| 6 | Item Organizations | 26 | 95-120 |
| 7 | Items | 35 | 121-155 |
| 8 | Catalogs | 3 | 156-158 |
| 9 | Structures | 7 | 159-165 |
| 10 | Suppliers for Product Management | 14 | 166-179 |
| 11 | Item Mass Update | 1 | 180-180 |
| 12 | Advanced Catalogs | 1 | 181-181 |
| 13 | New Item Requests | 5 | 182-186 |
| 14 | Change Orders | 13 | 187-199 |
| 15 | Product Rules | 2 | 200-201 |
| 16 | Data Quality Rules for Products | 1 | 202-202 |
| 17 | Audit Trail | 1 | 203-203 |
| 18 | Product Spoke Systems | 5 | 204-208 |
| 19 | Item Batches | 6 | 209-214 |
| 20 | Data Pool Integration | 3 | 215-217 |
| 21 | Data Quality for Products | 1 | 218-218 |
| 22 | Supplier Portal | 6 | 219-224 |
| 23 | Product Development | 2 | 225-226 |
| 24 | Product Requirements and Ideation Management | 9 | 227-235 |
| 25 | Concept Design Management | 9 | 236-244 |
| 26 | Product Lifecycle Portfolio Management | 9 | 245-253 |
| 27 | Quality Issue and Action Management | 5 | 254-258 |
| 28 | Sustainability | 7 | 259-265 |
| 29 | Index Management | 1 | 266-266 |

## Step-by-step plan

### 1. Initial Users (6 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 1 | Manage Applications Security Preferences | Manage applications security preferences including user name generation rules, password policy and user notification templates. | assisted |
| 2 | Import Users and Roles into Application Security | Schedule import of users and roles into Application Security tables. | assisted |
| 3 | Import User Login History | Schedule import of users and roles into Application Security tables. | assisted |
| 4 | Run User and Roles Synchronization Process | Batch process to Synchronize User and Roles. | assisted |
| 5 | Create Implementation Users | Create user accounts for implementation users. | manual |
| 6 | Create Data Role for Implementation Users | Create a data role based on the Human Capital Management Application Administrator job role to view all security profiles so a single user will be able to perform all required Human Capital Management setup steps. This role combines granted entitlements with unrestricted access to the setup data relevant to the tasks performed by this role. | manual |

### 2. Enterprise Profile (9 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 7 | Manage Geographies | Manage geographic entities such as country, state, province, and city. Manage geography hierarchy structure and validations. | assisted |
| 8 | Load Geography Interface Data | Manually load geography interface data before running the geography loader. | manual |
| 9 | Run Geography Loader | Schedule and monitor the process to load geography data from external data providers. | manual |
| 10 | Run Maintain Geography Name Referencing | Schedule and monitor the process to verify addresses against reference geography data. | assisted |
| 11 | Run Geocode Generation | Schedule and monitor the process to load geocode data for addresses. | assisted |
| 12 | Manage Geography Lookups | Review and define lookup values that provide choices related to geographies, such as address validation methods. | manual |
| 13 | Establish Enterprise Structures | Determine the high-level structures of the enterprise using an interview style process. | manual |
| 14 | Manage Enterprise HCM Information | Review and update information associated to the enterprise, such as default workday information. | assisted |
| 15 | Manage Locations | Create and manage the locations relevant to your enterprise. For example, create the locations where people work as well as the locations of your external organizations. | assisted |

### 3. Users and Security (24 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 16 | Manage Legal Entity | Create and maintain information for legal entities and legal reporting units to achieve legal compliance for business activities handled by the Oracle Fusion applications. | assisted |
| 17 | Manage Chart of Accounts Value Sets | Create new or review existing value sets for association with a key flexfield segment. | assisted |
| 18 | Manage Chart of Accounts Structures | Review and update existing account structures that support chart of accounts structure instances, which are used to record transactions and maintain account balances, or create new account structures. | assisted |
| 19 | Manage Chart of Accounts Structure Instances | Review and update existing account structure instances used to record transactions and maintain account balances, or create new account structure sets. | assisted |
| 20 | Manage Chart of Accounts Value Set Values | Review and update existing groups of values assigned to a key flexfield segment, or create new groups of values. | assisted |
| 21 | Manage Accounting Calendars | Review and update existing groupings of accounting periods, and create new groupings. | assisted |
| 22 | Manage Primary Ledgers | Review and update a self-contained accounting information set, and define new information sets. | assisted |
| 23 | Assign Legal Entities | Associate a recognized party with given rights and responsibilities by legislation with an accounting configuration. | assisted |
| 24 | Specify Ledger Options | Define the various additional attributes for the ledger. | assisted |
| 25 | Assign Balancing Segment Values to Legal Entities | Associate chart of account segment values to a legal entity where transactions will be balanced for each of the values in the segment. | assisted |
| 26 | Manage Reporting Currencies | Review and update a self-contained accounting information set that differs in currency from the primary ledger, and define new information sets. | assisted |
| 27 | Assign Balancing Segment Values to Ledger | Associate chart of account segment values to a ledger where transactions will be balanced for each of the values in the segment. | assisted |
| 28 | View Accounting Configuration Summary | Verify the current status and details of the accounting configuration. | manual |
| 29 | Review and Submit Accounting Configuration | Verify and submit the accounting configuration for completion. | assisted |
| 30 | Manage Business Unit | Create and maintain information on units of an enterprise to allow for flexible implementation, to provide a consistent entity for controlling and reporting on transactions, and to be an anchor for the sharing of reference data sets across applications. | assisted |
| 31 | Assign Business Unit Business Function | Assign business functions to be performed by a business unit, such as customer invoicing and order capture. | assisted |
| 32 | Manage Business Unit Set Assignment | Assign reference data, which represents business rules and policies, to business units. | assisted |
| 33 | Manage HCM Role Provisioning Rules | Create and manage rules for provisioning roles to people based on assignment information, such as job, position, and person type. | assisted |
| 34 | Import Worker Users | Import Worker users as HCM Workers from legacy applications. The import process will automatically create user accounts and assign roles to workers using HCM role provisioning rules. | manual |
| 35 | Manage Users | Manage application user definitions. | assisted |
| 36 | Manage Data Access for Users | Manage data access for user provisioned roles. | manual |
| 37 | Manage Job Roles | Review, create, or update enterprise-wide abstract and job roles. Create role hierarchies. | assisted |
| 38 | Manage Duties | Review the logical groupings of tasks that define duty roles. Provision duty roles to abstract, job, or other duty roles. | assisted |
| 39 | Manage Data Security Policies | Review, create, or update grants of entitlement to a user or role on an object or attribute group for a given condition. | assisted |

### 4. Application Extensions (31 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 40 | Manage Enterprise Scheduler Job Definitions and Job Sets for Financial, Supply Chain Management, and Related Applications | Manage the Enterprise Scheduler job definitions and job sets used for running scheduled processes, as well as the lists of values used for job definitions. | manual |
| 41 | Set Help Options | Set options for help windows, including whether help icons used to open the windows are shown or hidden by default. | manual |
| 42 | Assign Help Text Administration Duty | Make sure that users who need to add and edit help have roles with the privilege that gives them access to do so. | manual |
| 43 | Manage Help Security Groups | Create or update security groups that you can use to control access to specific help content. | assisted |
| 44 | Manage Taxonomy Hierarchy | Review and edit the hierarchy of functional units that make up Oracle Fusion Applications, from product families and applications to functional components. | manual |
| 45 | Manage Reference Data Sets | Review and manage sets for partitioning and sharing reference data across organizations. | assisted |
| 46 | Manage Currencies | Review and edit ISO standard currencies. | assisted |
| 47 | Manage ISO Languages | Review and edit ISO standard languages. | manual |
| 48 | Manage Territories | Review and edit ISO standard territories. | manual |
| 49 | Manage Languages | Review and edit the installed languages. | manual |
| 50 | Manage Industries | Review and edit ISO standard industries. | manual |
| 51 | Manage Natural Languages | Review and edit natural, spoken languages. | manual |
| 52 | Manage Time Zones | Review and edit time zones. | manual |
| 53 | Manage Data Security Policies | Review, create, or update grants of entitlement to a user or role on an object or attribute group for a given condition. | assisted |
| 54 | Set User General Preferences | Specify the general preferences settings for all users, for example language and date format. | manual |
| 55 | Manage Audit Policies | Select the business object attributes to audit for Oracle Fusion Applications, and set audit levels for other Oracle products. | assisted |
| 56 | Manage Applications Core Messages | Review and edit messages that are used for Oracle Middleware Extensions for Applications. | manual |
| 57 | Manage Applications Core Standard Lookups | Review and manage lookup values for Oracle Middleware Extensions for Applications. | manual |
| 58 | Manage Applications Core Profile Options | Review and manage profile options that affect Oracle Middleware Extensions for Applications behavior, and specify the levels at which they can be set. | manual |
| 59 | Manage Applications Core Administrator Profile Values | Specify profile option settings and values to control Oracle Middleware Extensions for Applications behavior. | manual |
| 60 | Manage Applications Core Profile Categories | Review and manage categories to group profile options that are used in Oracle Middleware Extensions for Applications, based on their functional area. Categories can be used to search for related profiles and to define data security rules. | manual |
| 61 | Manage Applications Core Value Sets | Review and manage value sets for Oracle Middleware Extensions for Applications. | manual |
| 62 | Manage Applications Core Descriptive Flexfields | Review and edit descriptive flexfields that are used for Oracle Middleware Extensions for Applications. | manual |
| 63 | Manage Applications Core Attachment Entities | Review and manage attachment entities for Oracle Middleware Extensions for Applications. | manual |
| 64 | Manage Applications Core Attachment Categories | Review and manage attachment categories for Oracle Middleware Extensions for Applications. | manual |
| 65 | Manage Applications Core Global Search Configurations | Manage global search configurations that determine how Global Search looks on specific pages and which groups appear by default in the search box auto-suggest | assisted |
| 66 | Manage Applications Core Global Search Suggestion Groups | Register and edit suggestion groups to appear in the search box auto-suggest | assisted |
| 67 | Enable Click to Dial | Enable automated dialing by clicking a phone number. | manual |
| 68 | Guided Journeys | Manage guided journeys for use on selected application pages. Administrators can create and edit guided journeys to embed tutorials, company policies, or best practices at the page or section level of application pages. | manual |
| 69 | Manage Task Configurations for Supply Chain Management | Review and edit approval flow rules for workflow tasks. | manual |
| 70 | Manage Approval Groups | Manage Approval Groups | manual |

### 5. Inventory Organizations (24 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 71 | Manage Facility Shifts | Configure facility shifts to represent a time period that affects a resource's availability. A shift can be defined by start time and end time, start time and duration, or only duration. | assisted |
| 72 | Manage Facility Workday Patterns | Configure facility workday patterns to represent a collection of one or more shifts over a number of days. A pattern will repeat itself for a specific date range to define the complete schedule of a resource. | assisted |
| 73 | Manage Facility Schedule Exceptions | Configure facility schedule exceptions to define deviations in availability from a schedule. Exceptions can be added to one or more schedules. | assisted |
| 74 | Manage Facility Schedules | Configure facility schedules to define the actual calendar dates worked, and the pattern shifts to apply to those dates worked. The date range in a schedule is defined by a schedule start date and a schedule end date. | assisted |
| 75 | Manage Legal Entity | Create and maintain information for legal entities and legal reporting units to achieve legal compliance for business activities handled by the Oracle Fusion applications. | assisted |
| 76 | Manage Chart of Accounts Value Sets | Create new or review existing value sets for association with a key flexfield segment. | assisted |
| 77 | Manage Chart of Accounts Structures | Review and update existing account structures that support chart of accounts structure instances, which are used to record transactions and maintain account balances, or create new account structures. | assisted |
| 78 | Manage Chart of Accounts Structure Instances | Review and update existing account structure instances used to record transactions and maintain account balances, or create new account structure sets. | assisted |
| 79 | Manage Chart of Accounts Value Set Values | Review and update existing groups of values assigned to a key flexfield segment, or create new groups of values. | assisted |
| 80 | Manage Accounting Calendars | Review and update existing groupings of accounting periods, and create new groupings. | assisted |
| 81 | Manage Primary Ledgers | Review and update a self-contained accounting information set, and define new information sets. | assisted |
| 82 | Assign Legal Entities | Associate a recognized party with given rights and responsibilities by legislation with an accounting configuration. | assisted |
| 83 | Specify Ledger Options | Define the various additional attributes for the ledger. | assisted |
| 84 | Assign Balancing Segment Values to Legal Entities | Associate chart of account segment values to a legal entity where transactions will be balanced for each of the values in the segment. | assisted |
| 85 | Manage Reporting Currencies | Review and update a self-contained accounting information set that differs in currency from the primary ledger, and define new information sets. | assisted |
| 86 | Assign Balancing Segment Values to Ledger | Associate chart of account segment values to a ledger where transactions will be balanced for each of the values in the segment. | assisted |
| 87 | View Accounting Configuration Summary | Verify the current status and details of the accounting configuration. | manual |
| 88 | Review and Submit Accounting Configuration | Verify and submit the accounting configuration for completion. | assisted |
| 89 | Manage Business Unit | Create and maintain information on units of an enterprise to allow for flexible implementation, to provide a consistent entity for controlling and reporting on transactions, and to be an anchor for the sharing of reference data sets across applications. | assisted |
| 90 | Assign Business Unit Business Function | Assign business functions to be performed by a business unit, such as customer invoicing and order capture. | assisted |
| 91 | Manage Business Unit Set Assignment | Assign reference data, which represents business rules and policies, to business units. | assisted |
| 92 | Manage Inventory Organizations | Configure inventory organizations to describe distinct entities within the company such as manufacturing facilities, warehouses, or distribution centers. | assisted |
| 93 | Manage Organization Trees | Create and manage hierarchies of organizations to view the structures of the enterprise. | assisted |
| 94 | Associate Fixed Asset Books with Inventory Organizations | Define and maintain the fixed asset books that are associated with inventory organizations. | manual |

### 6. Item Organizations (26 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 95 | Manage Facility Shifts | Configure facility shifts to represent a time period that affects a resource's availability. A shift can be defined by start time and end time, start time and duration, or only duration. | assisted |
| 96 | Manage Facility Workday Patterns | Configure facility workday patterns to represent a collection of one or more shifts over a number of days. A pattern will repeat itself for a specific date range to define the complete schedule of a resource. | assisted |
| 97 | Manage Facility Schedule Exceptions | Configure facility schedule exceptions to define deviations in availability from a schedule. Exceptions can be added to one or more schedules. | assisted |
| 98 | Manage Facility Schedules | Configure facility schedules to define the actual calendar dates worked, and the pattern shifts to apply to those dates worked. The date range in a schedule is defined by a schedule start date and a schedule end date. | assisted |
| 99 | Manage Legal Entity | Create and maintain information for legal entities and legal reporting units to achieve legal compliance for business activities handled by the Oracle Fusion applications. | assisted |
| 100 | Manage Chart of Accounts Value Sets | Create new or review existing value sets for association with a key flexfield segment. | assisted |
| 101 | Manage Chart of Accounts Structures | Review and update existing account structures that support chart of accounts structure instances, which are used to record transactions and maintain account balances, or create new account structures. | assisted |
| 102 | Manage Chart of Accounts Structure Instances | Review and update existing account structure instances used to record transactions and maintain account balances, or create new account structure sets. | assisted |
| 103 | Manage Chart of Accounts Value Set Values | Review and update existing groups of values assigned to a key flexfield segment, or create new groups of values. | assisted |
| 104 | Manage Accounting Calendars | Review and update existing groupings of accounting periods, and create new groupings. | assisted |
| 105 | Manage Primary Ledgers | Review and update a self-contained accounting information set, and define new information sets. | assisted |
| 106 | Assign Legal Entities | Associate a recognized party with given rights and responsibilities by legislation with an accounting configuration. | assisted |
| 107 | Specify Ledger Options | Define the various additional attributes for the ledger. | assisted |
| 108 | Assign Balancing Segment Values to Legal Entities | Associate chart of account segment values to a legal entity where transactions will be balanced for each of the values in the segment. | assisted |
| 109 | Manage Reporting Currencies | Review and update a self-contained accounting information set that differs in currency from the primary ledger, and define new information sets. | assisted |
| 110 | Assign Balancing Segment Values to Ledger | Associate chart of account segment values to a ledger where transactions will be balanced for each of the values in the segment. | assisted |
| 111 | View Accounting Configuration Summary | Verify the current status and details of the accounting configuration. | manual |
| 112 | Review and Submit Accounting Configuration | Verify and submit the accounting configuration for completion. | assisted |
| 113 | Manage Business Unit | Create and maintain information on units of an enterprise to allow for flexible implementation, to provide a consistent entity for controlling and reporting on transactions, and to be an anchor for the sharing of reference data sets across applications. | assisted |
| 114 | Assign Business Unit Business Function | Assign business functions to be performed by a business unit, such as customer invoicing and order capture. | assisted |
| 115 | Manage Business Unit Set Assignment | Assign reference data, which represents business rules and policies, to business units. | assisted |
| 116 | Manage Item Organizations | Configure item organization structures to use in standalone application deployments with Oracle Fusion Product Model. Structures contain information on the parent item, components, attachments, and descriptive elements. | assisted |
| 117 | Manage Organization Trees | Create and manage hierarchies of organizations to view the structures of the enterprise. | assisted |
| 118 | Configure Electronic Signature Preferences | Configure when e-records and e-signatures are required for a transaction. | manual |
| 119 | Manage Task Configurations for Supply Chain Management | Review and edit approval flow rules for workflow tasks. | manual |
| 120 | Manage Approval Groups | Manage Approval Groups | manual |

### 7. Items (35 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 121 | Manage Item Profile Options | Define profile option settings and values to control item behavior such as updating items and controlling the number of threads used in item imports. | assisted |
| 122 | Manage Advanced Item Profile Options | Define profile option settings and values to control item behavior such as controlling the update of items. | assisted |
| 123 | Manage Units of Measure Profiles | Review and maintain profile values for units of measure. | assisted |
| 124 | Manage SCM Common Value Sets | Create and edit SCM Common value sets. | assisted |
| 125 | Manage Units of Measure Descriptive Flexfields | Define validation and display properties of descriptive flexfields for UOM. Descriptive flexfields are used to add attributes to entities. | assisted |
| 126 | Manage Units of Measure | Create and maintain units of measure used within your organization to clearly identify the quantity of an item. | assisted |
| 127 | Manage Unit of Measure Classes | Manage Unit of Measure Classes. | assisted |
| 128 | Manage Lifecycle Phases | Create and edit item life cycle phases. | assisted |
| 129 | Manage Product and Child Value Sets | Create and edit value sets. | assisted |
| 130 | Manage Attachment Categories for Product Management | Create and edit the attachment categories that are used to group messages. | assisted |
| 131 | Manage Operational Attributes Groups | Edit operation attribute group parameters. | assisted |
| 132 | Manage Item Attribute Groups and Attributes | Create and edit item attribute groups and attributes. | assisted |
| 133 | Manage Item Classes | Create and edit item classes. | assisted |
| 134 | Manage Item Class Descriptive Flexfields | Create and Edit Item Class descriptive flexfield attributes. | assisted |
| 135 | Deploy Item Extensible Flexfields | Deploy extensible flexfields for the Product Information Management. | assisted |
| 136 | Manage Item Statuses | Create and edit item statuses. | assisted |
| 137 | Manage Item Types | Create and edit item types. | assisted |
| 138 | Manage Cross Reference Types | Create and edit item cross references types. | assisted |
| 139 | Manage Item Descriptive Flexfields | Define validation and display properties of descriptive flexfields for items. Descriptive flexfields are used to add attributes to entities. | assisted |
| 140 | Manage Import Maps | Create and edit import maps that map a source data set to a destination data set. | assisted |
| 141 | Download Import Template from Oracle Help Center | Download the import template spreadsheet from the Oracle Help Center. | manual |
| 142 | Upload Item Data | Upload the data file to the import processing area. | manual |
| 143 | Load Interface File through Scheduled Process | Run the scheduled process job that loads the interface file. | manual |
| 144 | Import Items | Import items using interface tables. | assisted |
| 145 | Manage Related Item Subtypes | Create and edit subtype values for related items. | assisted |
| 146 | Manage Item Revision Descriptive Flexfields | Define validation and display properties of descriptive flexfields for item revisions. Descriptive flexfields are used to add attributes to entities. | manual |
| 147 | Manage Item Relationship Descriptive Flexfields | Create and Edit item relationship descriptive flexfield attributes. | assisted |
| 148 | Manage Trading Partner Item Descriptive Flexfields | Create and Edit Trading Partner Item descriptive flexfield attributes. | assisted |
| 149 | Manage Units of Measure for Interclass Conversion | Create and maintain units of measure used in interclass conversions to clearly identify the quantity of an item. | assisted |
| 150 | Manage Units of Measure for Intraclass Conversion | Create and maintain units of measure used in intraclass conversions to clearly identify the quantity of an item. | assisted |
| 151 | Manage Item-Specific UOM Conversions | Manage Item-Specific UOM Conversions. | manual |
| 152 | Manage Item Keyword Search Attributes | Add and edit item keyword search attributes. | manual |
| 153 | Manage Related Item Types | Govern cyclic relationship setup for related item relationship types. | assisted |
| 154 | Manage Manufacturer Attribute Groups and Attributes | Create and edit manufacturer attribute groups and attributes. | manual |
| 155 | Reference Organization Items Import |  | manual |

### 8. Catalogs (3 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 156 | Manage Functional Area Catalogs | Create and edit functional area catalogs. | assisted |
| 157 | Manage Catalog Descriptive Flexfields | Create and edit catalog descriptive flexfield attributes. | assisted |
| 158 | Manage Category Descriptive Flexfields | Create and edit category descriptive flexfield attributes. | assisted |

### 9. Structures (7 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 159 | Manage Structure Header Descriptive Flexfields | Create and edit item structure type descriptive flexfield attributes. | assisted |
| 160 | Manage Item Structure Type Details | Create and edit structure type details. | assisted |
| 161 | Manage Valid Component Type Rules | Create and edit valid component type rules. | manual |
| 162 | Manage Structure Component Descriptive Flexfields | Create and edit item structure component descriptive flexfield attributes. | assisted |
| 163 | Manage Structure Substitute Component Descriptive Flexfields | Create and edit item structure substitute component descriptive flexfield attributes. | assisted |
| 164 | Manage Structure Reference Designator Descriptive Flexfields | Create and edit item structure reference designator descriptive flexfield attributes. | assisted |
| 165 | Item Structure Import |  | assisted |

### 10. Suppliers for Product Management (14 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 166 | Specify Supplier Numbering | Specify the supplier number to be used when the next supplier record is created. | assisted |
| 167 | Manage Supplier Type Lookup | Define and maintain the set of values that categorize suppliers for reporting purposes. | assisted |
| 168 | Manage Tax Organization Type Lookup | Define and maintain the set of values that categorize suppliers for tax reporting purposes. | assisted |
| 169 | Manage Supplier Value Sets | Define and maintain supplier value sets. | assisted |
| 170 | Manage Supplier Descriptive Flexfields | Define and maintain the descriptive flexfields value for the supplier. | assisted |
| 171 | Manage Supplier Messages | Review and edit Supplier messages. | assisted |
| 172 | Configure Party Relationships for Supplier Match | Configure party relationships for matching suppliers during deduplication process. | manual |
| 173 | Manage Server Configurations | Review and define the data quality server configuration to integrate with Informatica Data Quality. The server name is then associated with the matching and cleansing configuration to provide duplicate prevention, batch duplicate identification, and real-time and batch data cleansing. | assisted |
| 174 | Manage Enterprise Data Quality Matching Configurations | Allows management of matching configurations associated with enterprise data quality integration. | manual |
| 175 | Create Supplier in Procurement | Create supplier and supplier addresses in Procurement. | manual |
| 176 | Manage Business Classification Lookup | Define and maintain the set of values describing the classifications used for tracking supplier diversity. | assisted |
| 177 | Manage Minority Group Lookup | Define and maintain the set of minority groups that are used to subclassify minority owned suppliers. | assisted |
| 178 | Manage Geographies | Manage geographic entities such as country, state, province, and city. Manage geography hierarchy structure and validations. | assisted |
| 179 | Manage Address Formats | Review and configure how addresses appear in the application, such as the sequence of address elements in a postal address. | assisted |

### 11. Item Mass Update (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 180 | Manage Item Import Formats Configuration | Create and edit item import formats for item batch and item mass update. | manual |

### 12. Advanced Catalogs (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 181 | Manage Catalog Mappings | Create and edit catalog mappings. | assisted |

### 13. New Item Requests (5 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 182 | Manage Change Order and New Item Request Header Descriptive Flexfields | Define validation and display properties of descriptive flexfields for change orders. Descriptive flexfields are used to add attributes to entities. | assisted |
| 183 | Manage New Item Request Type Details | Create and edit new item request type details. | manual |
| 184 | Manage Change Order and New Item Request Line Descriptive Flexfields | Define validation and display properties of descriptive flexfields for change orders and new item requests lines. Descriptive flexfields are used to add attributes to entities. | assisted |
| 185 | Manage Task Configurations for Supply Chain Management | Review and edit approval flow rules for workflow tasks. | manual |
| 186 | Manage Approval Groups | Manage Approval Groups | manual |

### 14. Change Orders (13 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 187 | Manage Change Reasons | Create and edit change reasons. | assisted |
| 188 | Manage Change Priorities | Create and edit change priorities. | assisted |
| 189 | Manage Change Statuses | Create and edit change statuses. | assisted |
| 190 | Manage Change Order Types | Create and edit change order types. | assisted |
| 191 | Manage Change Order and New Item Request Header Descriptive Flexfields | Define validation and display properties of descriptive flexfields for change orders. Descriptive flexfields are used to add attributes to entities. | assisted |
| 192 | Manage Change Order and New Item Request Line Descriptive Flexfields | Define validation and display properties of descriptive flexfields for change orders and new item requests lines. Descriptive flexfields are used to add attributes to entities. | assisted |
| 193 | Manage Organization Trees | Create and manage hierarchies of organizations to view the structures of the enterprise. | assisted |
| 194 | Manage Task Configurations for Supply Chain Management | Review and edit approval flow rules for workflow tasks. | manual |
| 195 | Manage Approval Groups | Manage Approval Groups | manual |
| 196 | Manage Change Order Entry and Exit Rule Sets | Configure required fields for a change order when the change moves from one state to another. | manual |
| 197 | Manage Change Attribute Groups and Attributes | Create and edit change order header attribute groups and attributes. | assisted |
| 198 | Manage Workflow Rejection Reasons | Configure the reasons that can be selected by approvers while rejecting a workflow approval request. | assisted |
| 199 | Change Orders Import |  | assisted |

### 15. Product Rules (2 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 200 | Manage Item Rule Sets | Create and edit item rule sets. | assisted |
| 201 | Register Web Services through Oracle CRM Application Composer | Web services used with rules are registered with Oracle CRM Application Composer. | manual |

### 16. Data Quality Rules for Products (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 202 | Manage Data Quality for Products Profile Options | Define profile option settings and values for data quality for products. | manual |

### 17. Audit Trail (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 203 | Manage Audit Policies | Select the business object attributes to audit for Oracle Fusion Applications, and set audit levels for other Oracle products. | assisted |

### 18. Product Spoke Systems (5 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 204 | Manage Trading Community Source Systems | Review and define the types of information imported for each source system. | assisted |
| 205 | Manage Source System Entities | Review and define entity associations for various source systems. For example, some source systems are configured to import customer data, whereas others are configured to import customers and contacts. | assisted |
| 206 | Manage Source System Lookups | Review and define lookup values that provide choices related to the source system model, such as original system types. | assisted |
| 207 | Manage Source System Descriptive Flexfields | Define additional fields to enter and track information that is not otherwise captured. Descriptive flexfields can be validated and dependent on other values entered in other areas of the page. | assisted |
| 208 | Manage Spoke Systems | Edit source system parameters for import. | assisted |

### 19. Item Batches (6 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 209 | Manage Trading Community Source Systems | Review and define the types of information imported for each source system. | assisted |
| 210 | Manage Source System Entities | Review and define entity associations for various source systems. For example, some source systems are configured to import customer data, whereas others are configured to import customers and contacts. | assisted |
| 211 | Manage Source System Lookups | Review and define lookup values that provide choices related to the source system model, such as original system types. | assisted |
| 212 | Manage Source System Descriptive Flexfields | Define additional fields to enter and track information that is not otherwise captured. Descriptive flexfields can be validated and dependent on other values entered in other areas of the page. | assisted |
| 213 | Manage Spoke Systems | Edit source system parameters for import. | assisted |
| 214 | Manage Item Import Formats Configuration | Create and edit item import formats for item batch and item mass update. | manual |

### 20. Data Pool Integration (3 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 215 | Manage Review Codes | Create and edit review codes for data pool synchronization processes. | manual |
| 216 | Manage Correction Codes | Create and edit Correction codes for data pool synchronization processes. | manual |
| 217 | Manage Rejection Codes | Create and edit Rejection codes for data pool synchronization processes. | manual |

### 21. Data Quality for Products (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 218 | Manage Data Quality for Products Profile Options | Define profile option settings and values for data quality for products. | manual |

### 22. Supplier Portal (6 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 219 | Manage Supplier User Roles | Define the roles that can be provisioned to supplier users. | assisted |
| 220 | Manage Supplier User Role Usages | Define the roles a supplier administrator can provision and set default roles for Oracle Fusion Supplier Portal and Oracle Fusion Sourcing. | assisted |
| 221 | Specify User Category for New Supplier Users | Specify user category with the name SUPPLIER_USER in the Security Console. This user category will be assigned to new supplier user account. | manual |
| 222 | Specify Supplier News Content | Define and maintain supplier news and information content for suppliers to view on the supplier portal overview page. | assisted |
| 223 | Manage Supplier Portal Messages | Review and edit Supplier Portal messages. | assisted |
| 224 | Configure Supplier Notifications | Configure notification generation and delivery interval for supplier user notifications, such as expiring business classification. | assisted |

### 23. Product Development (2 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 225 | Manage Product Development Lookups | Review and manage lookups for product development. | manual |
| 226 | Manage Structure Component Descriptive Flexfields | Create and edit item structure component descriptive flexfield attributes. | assisted |

### 24. Product Requirements and Ideation Management (9 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 227 | Manage Product Idea Classes | Configure the category of objects for ideas. | manual |
| 228 | Manage Product Idea Statuses | Configure statuses available for ideas that indicate the various stages or conditions. | manual |
| 229 | Manage Product Requirement Classes | Configure the category of objects for requirements. | manual |
| 230 | Manage Product Requirement Statuses | Configure statuses available for requirements that indicate the various stages or conditions. | manual |
| 231 | Manage Product Requirements and Ideation Lookups | Review and maintain lookup values for ideas and requirements. | manual |
| 232 | Register Agile PLM | Register Agile PLM for connection to Oracle Fusion Innovation Management. | manual |
| 233 | Manage Target System | Configure connections and mappings between the Applications Unlimited Framework and Oracle Fusion Innovation Management. | manual |
| 234 | Register Agile EDM System | Register the Agile EDM system for connection to Oracle Fusion Innovation Management. | manual |
| 235 | Register Agile EDM File Server | Register the Agile EDM file server for connection to Oracle Fusion Innovation Management. | manual |

### 25. Concept Design Management (9 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 236 | Manage Product Concept Classes | Configure the category of objects for concepts that are possible solutions. | manual |
| 237 | Manage Product Concept Component Classes | Configure the category of objects for concept components that are modifiable elements or parts of a possible solution. | manual |
| 238 | Manage Product Concept Statuses | Configure statuses available for concepts that indicate the various stages or conditions. | manual |
| 239 | Manage Proposal Statuses | Configure statuses available for proposals that indicate the various stages or conditions. | manual |
| 240 | Manage Product Concept Lookups | Review and maintain lookup values for concepts and proposals. | manual |
| 241 | Register Agile PLM | Register Agile PLM for connection to Oracle Fusion Innovation Management. | manual |
| 242 | Manage Target System | Configure connections and mappings between the Applications Unlimited Framework and Oracle Fusion Innovation Management. | manual |
| 243 | Register Agile EDM System | Register the Agile EDM system for connection to Oracle Fusion Innovation Management. | manual |
| 244 | Register Agile EDM File Server | Register the Agile EDM file server for connection to Oracle Fusion Innovation Management. | manual |

### 26. Product Lifecycle Portfolio Management (9 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 245 | Manage Product Portfolio Classes | Configure the category of objects for portfolios. | manual |
| 246 | Manage Portfolio Statuses | Configure statuses available for portfolios that indicate the various stages or conditions. | manual |
| 247 | Manage Product Portfolio Planning Periods | Configure the time period range when data is collected for analysis by the portfolio. | manual |
| 248 | Manage Product Portfolio Metrics | Configure specific attributes of metrics that affect portfolios and products within a portfolio. | manual |
| 249 | Manage Product Portfolio Lookups | Review and maintain lookup values for portfolios. | manual |
| 250 | Register Agile PLM | Register Agile PLM for connection to Oracle Fusion Innovation Management. | manual |
| 251 | Manage Target System | Configure connections and mappings between the Applications Unlimited Framework and Oracle Fusion Innovation Management. | manual |
| 252 | Register Agile EDM System | Register the Agile EDM system for connection to Oracle Fusion Innovation Management. | manual |
| 253 | Register Agile EDM File Server | Register the Agile EDM file server for connection to Oracle Fusion Innovation Management. | manual |

### 27. Quality Issue and Action Management (5 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 254 | Manage Workflow Templates for Product Lifecycle Management | Define the sequence of statuses and approvals for each workflow template. | manual |
| 255 | Manage Workflow Statuses for Product Lifecycle Management | Set up the list of workflow statuses that can be used to define workflow templates. | manual |
| 256 | Manage Quality Issue and Action Lookups | Review and manage lookups for quality issues and quality actions. | manual |
| 257 | Manage Quality Issue Types | Configure the category of objects for quality issues. | manual |
| 258 | Manage Quality Action Types | Configure the category of objects for quality actions. | manual |

### 28. Sustainability (7 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 259 | Manage Sustainability Ledgers | Manage Sustainability Ledgers | manual |
| 260 | Manage Sustainability Lookups | Manage lookup values for Cloud Sustainability, such as activity status, source, entry type. | manual |
| 261 | Manage Sustainability Value Sets | Manage value sets for Cloud Sustainability. | manual |
| 262 | Manage Sustainability Descriptive Flexfields | Manage descriptive flexfields for Cloud Sustainability Activity and Emission Factor Map. | manual |
| 263 | Manage Activity Types | Manage Activity Types | manual |
| 264 | Manage Sustainability Profile Options | Manage Sustainability Profile Options | manual |
| 265 | Manage Global Warming Potentials | Manage Global Warming Potentials | manual |

### 29. Index Management (1 tasks)

| Step | Task | What it does | Mode |
|---|---|---|---|
| 266 | Manage Product Management Indexes |  | assisted |

## Notes

- 4 tasks are not in the standard 26D list (Items, Advanced Product Structure, Change Orders, Index Management). They are placed last in their area.
- Task phases are not set yet. Assign them before scheduling.
- Files: `project/product-management-implementation/artifacts/shared/runbook/current/`.
