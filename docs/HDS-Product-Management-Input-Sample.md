# HDS Product Management: Filled Sample and Data Formats

All values are **sample data**, not real HDS data. Replace them with yours. Sample files are in `docs/samples/`.

## 1. Which file format for each data point

Rule used: **CSV** for bulk data you load (many rows, loaded by tools). **Excel** for small lists that people review and approve.

| # | Data point | Format | Sample file | Columns (in order) |
|---|---|---|---|---|
| 1 | Users and roles | Excel | `01_users_roles.csv` | user_name, first_name, last_name, email, job_role, access_area |
| 2 | Organizations | Excel | `02_organizations.csv` | org_code, org_name, org_type, location, business_unit, legal_entity |
| 3 | Item classes | Excel | `03_item_classes.csv` | item_class, parent_class, item_type, numbering_rule |
| 4 | Items | CSV | `04_items.csv` | item_number, description, item_class, uom, status, lifecycle_phase, revision, org_code, template |
| 5 | Suppliers and manufacturer parts | CSV | `05_suppliers.csv` | supplier_name, supplier_site, manufacturer_part_number, item_number |
| 6 | Catalog and categories | Excel | `06_catalog_categories.csv` | catalog_name, level, category_code, category_name, parent_category_code |
| 7 | Item-to-category assignment | CSV | `07_item_category_assignment.csv` | item_number, catalog_name, category_code |
| 8 | Custom attribute definitions | Excel | `08_custom_attributes.csv` | attribute_name, applies_to, data_type, required, allowed_values, validation |
| 9 | Custom attribute values per item | CSV | `09_item_attribute_values.csv` | item_number, attribute_name, attribute_value |
| 10 | Bill of materials | CSV | `10_bom.csv` | parent_item, component_item, quantity, uom, find_number, effective_from, substitute_item, structure_type |
| 11 | Change order types and approvers | Excel | `11_change_order_types.csv` | change_type, applies_to, approver_role, approval_order, reason_codes |
| 12 | Documents list | Excel | `12_documents.csv` | document_type, attached_to, owner_role, approval_needed, file_name |
| 13 | Deviations setup | Excel | `13_deviations.csv` | deviation_type, scope, approver_role, linked_to, duration_days |
| 14 | Phase plan | Excel | `14_phases.csv` | functional_area, phase, target_date |

The document files themselves (PDF, drawings) are sent as separate files, not inside the CSV.

## 2. Format rules for each field

| Field type | Rule | Example |
|---|---|---|
| Text | No line breaks, no commas unless the value is in double quotes | Industrial Pump 5HP |
| Item number | Capital letters, digits and hyphen; follow the numbering rule | FG-000001 |
| Unit of measure | Short code from your UOM list | EA, KG |
| Yes/No | `Y` or `N` (attribute values use `Yes` or `No`) | Y |
| Date | `YYYY-MM-DD` | 2026-11-01 |
| Number | Digits and one decimal point, no thousands separator | 2.5 |
| Several values in one cell | Separate with `;` | Items;BOM |
| Empty value | Leave blank, do not write NULL | |
| File encoding | UTF-8, first row is the header, header names unchanged | |

## 3. Filled template (sample)

### 0. Project
| Field | Value |
|---|---|
| Customer | HDS |
| Fusion release | 26D |
| Pod/environment name | SAMPLE-DEV1 |
| Primary contact | Asha Rao |
| Target go-live date | 2027-04-01 |

### 1. Foundation
| Field | Value |
|---|---|
| Enterprise name | HDS Industries |
| Industry | Industrial machinery |
| Country / currency / time zone | India / INR / Asia/Kolkata |
| Initial admin user | SAMPLE_PLM_ADMIN |

Users and roles: see `01_users_roles.csv`.

### 2. Organizations
| Org code | Org name | Type | Location | Business unit | Legal entity |
|---|---|---|---|---|---|
| HDM | HDS Item Master | Master | Pune | HDS India BU | HDS India Ltd |
| HD1 | HDS Plant 1 | Child | Pune | HDS India BU | HDS India Ltd |
| HD2 | HDS Plant 2 | Child | Chennai | HDS India BU | HDS India Ltd |

Item master organization code: **HDM**

### 3. Items
| Item class | Parent class | Item type | Numbering rule |
|---|---|---|---|
| Finished Good | Root Item Class | Finished | FG-###### |
| Component | Root Item Class | Purchased | CP-###### |
| Raw Material | Root Item Class | Purchased | RM-###### |

| Setting | Value |
|---|---|
| Item statuses | Active, Inactive, Obsolete |
| Lifecycle phases | Design, Prototype, Production, Obsolete |
| Unit of measure list | EA, KG, M |
| Revision scheme | Letters: A, B, C |
| Item templates needed | FG_TEMPLATE, CP_TEMPLATE, RM_TEMPLATE |

| New item requests: requester role | Approver role | Approval needed |
|---|---|---|
| Product Engineer | Product Data Administrator | Y |

Suppliers: see `05_suppliers.csv`. Manufacturer part number needed: Y.

### 4. Item Classification
| Catalog | Purpose | Level 1 | Level 2 |
|---|---|---|---|
| HDS Product Catalog | Product reporting | Pumps | Industrial Pumps |
| HDS Product Catalog | Product reporting | Parts | Rotating Parts |

Standard such as UNSPSC used: N

### 5. Custom Attributes
| Attribute | Applies to | Type | Required | Allowed values | Validated |
|---|---|---|---|---|---|
| Motor Power (HP) | Finished Good class | Number | Y | 0.5 to 100 | Y |
| Material Grade | Component class | Text | N | SS304; SS316; MS | Y |
| Hazardous | Item | Yes/No | Y | Yes; No | N |

Attributes in audit trail: Motor Power (HP), Material Grade

### 6. Bill of Materials
| Structure type | Components per BOM | Levels | Substitutes | Effectivity |
|---|---|---|---|---|
| Primary | 25 | 3 | N | Date |

### 7. Change Orders
| Change type | Applies to | Approver roles | Approval order | Reason codes |
|---|---|---|---|---|
| ECO | Items; BOM | Product Engineer; Quality Engineer | 1; 2 | Cost Reduction; Design Fix |
| ECN | Items | Product Data Administrator | 1 | Information Update |

### 8. Documents
| Document type | Attached to | Owner role | Approval |
|---|---|---|---|
| Specification | Item | Product Engineer | Y |
| Drawing | BOM | Product Engineer | Y |
| Test Report | Change Order | Quality Engineer | N |

Used: Product Development ☒  Concept Design ☐  Requirements and Ideas ☐  Product Portfolio ☐

### 9. Deviations
| Type | Scope | Approver roles | Linked to |
|---|---|---|---|
| Production Deviation | Lot | Quality Engineer | Item |
| Supplier Deviation | Quantity | Quality Engineer; Product Engineer | BOM |

Quality issue tracking acceptable for deviations: Y

### 10. Data in and out
| Topic | Answer |
|---|---|
| Data to load first | Items, then categories, then BOMs |
| Source file format | CSV for items, suppliers, assignments, attribute values, BOMs; Excel for the rest |
| Approx. record counts | Items 5,000; BOM lines 20,000 |
| Source systems | Legacy ERP export |
| Supplier portal needed | N |
| Sustainability needed | N |

### 11. Phases
See `14_phases.csv`.

## 4. Load order
Load in this order, because later files refer to earlier ones: 2, 3, 6, 8, then 4, 5, 7, 9, then 10.
