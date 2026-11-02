# HDS Product Management: Data Loader Mapping

This maps each sample file in `docs/samples/` to the FSCR task that loads it and the way it loads.

## Important limits
- FSCR does **not** ship fixed Oracle templates. For FBDI loads, `Import Items` fetches the current public Oracle template on every run. Exact Oracle column names and order are therefore **not listed here**. They are confirmed at run time.
- Sample-to-Oracle field links below are by meaning ("maps to item number"), not by Oracle column name.
- Actual loading needs a Fusion connection and your approval. Neither exists yet.
- All loads go through `core/data-loader`.

## Load modes
| Mode | Meaning | Source file you give |
|---|---|---|
| FBDI | Oracle's File-Based Data Import. Template downloaded at run time, output is a ZIP of headerless CSV files | Your CSV |
| FSM CSV | Functional Setup Manager setup export/import | Your Excel or CSV, converted by FSCR |
| REST | Setup records created through Fusion REST services | Your Excel or CSV |
| Manual | Configured in Fusion screens; no file loaded | Your Excel as a reference |

## Mapping: each sample file to an FSCR task

| # | Sample file | FSCR task (functional area) | Mode | Meaning of each sample column |
|---|---|---|---|---|
| 1 | `01_users_roles.csv` | Users and Security tasks | Manual | user_name = login; job_role = role to assign; access_area = which areas the role covers |
| 2 | `02_organizations.csv` | Inventory Organizations and Item Organizations tasks | Manual | org_code = organization code; org_type Master/Child = item master or child organization |
| 3 | `03_item_classes.csv` | Manage Item Classes (Items) | FSM CSV | item_class = class name; parent_class = parent in hierarchy; item_type = item type; numbering_rule = how numbers are generated |
| 4 | `04_items.csv` | Import Items (Items) | FBDI, business object `item` | item_number = item number; description = item description; item_class = item class; uom = primary UOM; status = item status; lifecycle_phase = lifecycle phase; revision = initial revision; org_code = organization; template = item template |
| 5 | `05_suppliers.csv` | Suppliers for Product Management tasks | Manual or REST (to be confirmed) | supplier_name, supplier_site = supplier and site; manufacturer_part_number = manufacturer part; item_number = linked item |
| 6 | `06_catalog_categories.csv` | Catalogs and Advanced Catalogs tasks | Manual (to be confirmed) | catalog_name = catalog; level = hierarchy level; category_code/name = category; parent_category_code = parent |
| 7 | `07_item_category_assignment.csv` | Item category assignment | To be confirmed. Likely part of `Import Items` | item_number, catalog_name, category_code = item-to-category link |
| 8 | `08_custom_attributes.csv` | Manage Item Attribute Groups and Attributes (Items) | FSM CSV | attribute_name = attribute; applies_to = item class; data_type; required = Y/N; allowed_values = value set; validation = rule |
| 9 | `09_item_attribute_values.csv` | Import Items | FBDI | item_number = item; attribute_name = attribute; attribute_value = value |
| 10 | `10_bom.csv` | Item Structure Import (Structures) | FBDI, business object `item` | parent_item = structure header item; component_item = component; quantity, uom = component quantity and UOM; find_number = item sequence; effective_from = start date; substitute_item = substitute; structure_type = structure name |
| 11 | `11_change_order_types.csv` | Manage Change Order Types, Change Reasons, Change Priorities, Change Statuses (Change Orders) | FSM CSV | change_type = type name; applies_to = what it changes; approver_role and approval_order = workflow approval; reason_codes = change reasons |
| 12 | `12_documents.csv` | Product Development tasks | Manual (to be confirmed) | document_type, attached_to, owner_role, approval_needed, file_name = attachment definitions |
| 13 | `13_deviations.csv` | Quality Issue and Action tasks | Manual (to be confirmed) | deviation_type = issue type; scope; approver_role; linked_to; duration_days |
| 14 | `14_phases.csv` | None | Not loaded | Used only to plan |

Also in the Change Orders area: `Change Orders Import` (FBDI, business object `Change Order`) loads change order transactions. Your sample does not include them, since they are not setup data.

## Load order
1. Manual setup: files 1, 2.
2. Setup records: files 3, 8, 11, then 6 (and 5 if loaded).
3. Data: files 4, 9, 7, then 10.
4. Change orders last.

## How exact templates will be produced
1. A Fusion connection is configured (`core/auth/fusionEnv.properties`).
2. The Data Loader generates a sample workbook from the live business object, or `Import Items` downloads the current Oracle template.
3. Your files are mapped to those columns. You review the mapping preview.
4. After your approval, the file is validated, uploaded and loaded.

## Questions that decide the "to be confirmed" rows
- Files 5, 6, 7: do you load these, or set them up in Fusion screens?
- Files 12, 13: which Fusion area do you use for documents and deviations?
