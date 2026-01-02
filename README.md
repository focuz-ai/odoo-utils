# Odoo UX Improvements

[![Odoo Version](https://img.shields.io/badge/Odoo-18.0-blue.svg)](https://www.odoo.com)
[![License](https://img.shields.io/badge/License-AGPL--3-green.svg)](https://www.gnu.org/licenses/agpl-3.0.html)

User experience improvement modules for Odoo 18.0. Includes mass editing, search widgets, and developer utilities from OCA and community sources.

**Table of contents**

- [Overview](#overview)
- [Modules](#modules)
- [Installation](#installation)
- [Usage](#usage)
- [Bug Tracker](#bug-tracker)
- [Credits](#credits)

## Overview

This repository provides UX enhancement modules for Odoo:

- **Mass Editing**: Edit multiple records at once with server actions
- **Search Widgets**: Quick search in One2many fields
- **Developer Tools**: Onchange helper for Python code

## Modules

| Module | Version | License | Description |
|--------|---------|---------|-------------|
| `server_action_mass_edit` | 18.0.1.1.1 | AGPL-3 | Mass editing of records via server actions |
| `server_action_mass_edit_onchange` | 18.0.1.1.1 | AGPL-3 | Onchange support for mass editing |
| `one2many_search_widget` | 18.0.1.0.0 | AGPL-3 | Quick search in One2many fields |
| `onchange_helper` | 18.0.1.0.1 | LGPL-3 | Execute onchange methods in Python code |

### server_action_mass_edit

Mass editing functionality for any Odoo model via server actions.

**Features:**
- Create mass edit actions for any model
- Select multiple records and edit fields at once
- Support for all field types
- Configure which fields are editable
- Add to action menu automatically

**Usage:**
1. Go to **Settings > Technical > Server Actions**
2. Create a new action with type "Mass Edit"
3. Select the model and fields to edit
4. Action appears in the record's action menu

### server_action_mass_edit_onchange

Extension that triggers onchange methods during mass editing.

**Features:**
- Automatically execute onchange methods when mass editing
- Maintain data consistency across related fields
- Works with computed fields that depend on edited values

### one2many_search_widget

Adds a search box to One2many fields for quick filtering.

**Features:**
- Search within One2many field lines
- Filter rows based on search text
- Non-matching rows are hidden
- Works with any One2many field

**Usage:**
The search widget is automatically available on One2many fields. Type in the search box to filter visible rows.

### onchange_helper

Technical module for developers to execute onchange methods programmatically.

**Features:**
- Execute onchange in Python code
- Useful for data imports and migrations
- Maintains field dependencies

**Example:**
```python
record.play_onchanges(values, ['field_name'])
```

## Installation

```bash
# Clone the repository
git clone https://github.com/focuz-ai/odoo-ux.git

# Add to addons path in odoo.conf
addons_path = /path/to/odoo-ux,...
```

### Dependencies

| Module | Depends On |
|--------|------------|
| `server_action_mass_edit` | `base` |
| `server_action_mass_edit_onchange` | `server_action_mass_edit`, `onchange_helper` |
| `one2many_search_widget` | `web` |
| `onchange_helper` | `web` |

## Usage

### Mass Edit Records

1. Go to any list view (e.g., Contacts, Products)
2. Select multiple records using checkboxes
3. Click **Action > Mass Edit**
4. Modify desired fields
5. Click **Apply** to update all selected records

### Search in One2many

1. Open any form with One2many fields
2. Use the search box above the One2many list
3. Type to filter visible rows
4. Clear search to show all rows

## Bug Tracker

Bugs are tracked on [GitHub Issues](https://github.com/focuz-ai/odoo-ux/issues).

For OCA modules, report issues on the original repositories:
- [OCA/server-tools](https://github.com/OCA/server-tools) (onchange_helper)
- [OCA/server-ux](https://github.com/OCA/server-ux) (mass_edit modules)

## Credits

### Authors

* Odoo Community Association (OCA)
* Serpent Consulting Services Pvt. Ltd.
* Tecnativa
* Camptocamp
* Akretion
* Cybrosys Technologies Pvt. Ltd.

### Maintainers

This repository is maintained by [Focuz AI S.A.C.](https://www.focuz.io)

Modules are sourced from OCA and community repositories, adapted for Odoo 18.0.
