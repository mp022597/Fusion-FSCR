# HDS Product Management: Input Template

Fill in every table. Write `N/A` if not needed and `TBD` if unknown. Do not enter passwords, tokens or keys.

## 0. Project
| Field | Value |
|---|---|
| Customer | HDS |
| Fusion release | 26D |
| Pod/environment name (no credentials) | |
| Primary contact | |
| Target go-live date | |

## 1. Foundation (Initial Users, Enterprise Profile, Users and Security)
| Field | Value |
|---|---|
| Enterprise name | |
| Industry | |
| Country / currency / time zone | |
| Initial admin user (name only) | |

### Users and roles
| User name | Job role | Needs access to |
|---|---|---|
| | | |

## 2. Organizations (Inventory Organizations, Item Organizations)
| Org code | Org name | Type (Master / Child) | Location | Business unit | Legal entity |
|---|---|---|---|---|---|
| | | | | | |

Item master organization code:

## 3. Items
### Item classes
| Item class | Parent class | Item type | Numbering rule |
|---|---|---|---|
| | | | |

### Item settings
| Setting | Value |
|---|---|
| Item statuses (e.g. Active, Inactive) | |
| Lifecycle phases (e.g. Design, Production, Obsolete) | |
| Unit of measure list | |
| Revision scheme | |
| Item templates needed | |

### New item requests
| Requester role | Approver role | Approval needed (Y/N) |
|---|---|---|
| | | |

### Suppliers
| Supplier | Manufacturer part no. needed (Y/N) |
|---|---|
| | |

## 4. Item Classification (Catalogs, Advanced Catalogs)
| Catalog name | Purpose | Level 1 category | Level 2 category | Level 3 category |
|---|---|---|---|---|
| | | | | |

Is a standard such as UNSPSC used? (Y/N, name):

## 5. Custom Attributes (Product Rules, Application Extensions, Data Quality)
| Attribute name | Applies to (Item / Revision / Class) | Data type | Required (Y/N) | Allowed values | Used for validation (Y/N) |
|---|---|---|---|---|---|
| | | | | | |

Attributes tracked in audit trail:

## 6. Bill of Materials (Structures)
| Structure type | Components per BOM (approx.) | Levels | Substitutes (Y/N) | Effectivity (Date / Revision) |
|---|---|---|---|---|
| | | | | |

## 7. Change Orders
| Change type | Applies to (Items / BOM / Both) | Approver role(s) | Approval order | Reason codes |
|---|---|---|---|---|
| | | | | |

## 8. Documents (Product Development, Concept Design, Requirements, Portfolio)
| Document type | Attached to (Item / BOM / Change) | Owner role | Approval needed (Y/N) |
|---|---|---|---|
| | | | |

Which of these will you use? Tick: Product Development ☐  Concept Design ☐  Requirements and Ideas ☐  Product Portfolio ☐

## 9. Deviations (Quality Issue and Action)
| Deviation type | Scope (qty / lot / date) | Approver role(s) | Linked to (Item / BOM / Change) |
|---|---|---|---|
| | | | |

Is quality issue tracking acceptable for deviations? (Y/N):

## 10. Data in and out
| Topic | Answer |
|---|---|
| Data to load first (items, BOMs, catalogs) | |
| Source file format (Excel / CSV) | |
| Approx. record counts | |
| Source systems to connect | |
| Supplier portal needed (Y/N) | |
| Sustainability needed (Y/N) | |

## 11. Phases
Assign each functional area to a phase in the plan.
| Functional area | Phase (Design / Build / Test / Deploy) | Target date |
|---|---|---|
| | | |
