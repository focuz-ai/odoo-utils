# Odoo Utils

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/focuz-ai/odoo-utils)
[![Coverage Status](https://img.shields.io/badge/coverage-95%25-yellowgreen)](https://github.com/focuz-ai/odoo-utils)
[![Odoo Version](https://img.shields.io/badge/odoo-17.0-blue)](https://www.odoo.com/)
[![License: AGPL-3](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This repository contains utility modules for Odoo 17.0 that extend and enhance the standard Odoo functionality.

## Available Modules

| Module | Version | Summary |
|--------|---------|---------|
| [partner_vat_unique](partner_vat_unique/) | 17.0.1.0.0 | Module to make the VAT number unique for customers and suppliers |
| [server_action_mass_edit](server_action_mass_edit/) | 17.0.1.0.2 | Mass Editing - Allows to edit multiple records at once |

## Installation

### Requirements

- Odoo 17.0
- Python 3.8+

### Installing Modules

1. Clone this repository into your Odoo addons directory:
```bash
git clone https://github.com/focuz-ai/odoo-utils.git
```

2. Update the addons list in Odoo:
   - Go to Apps menu
   - Click on "Update Apps List"
   - Search for the module you want to install

3. Install the desired modules from the Apps menu

## Modules Description

### Partner VAT Unique

This module ensures that VAT numbers are unique across all partners (customers and suppliers) in the system. It prevents duplicate VAT numbers from being created, helping maintain data integrity and compliance with tax regulations.

**Key Features:**
- Validates VAT uniqueness on partner creation and update
- Excludes child partners from validation
- Provides clear error messages when duplicates are detected
- Allows empty VAT numbers

### Server Action Mass Edit

This module provides powerful mass editing capabilities for Odoo records. It allows users to update multiple records at once through customizable server actions.

**Key Features:**
- Edit multiple records simultaneously
- Configure custom mass edit actions for any model
- Support for various field types
- Domain-based filtering for targeted edits
- User-friendly wizard interface
- Security group restrictions

## Configuration

Each module may have specific configuration requirements. Please refer to the individual module README files for detailed configuration instructions:

- [Partner VAT Unique Configuration](partner_vat_unique/README.rst)
- [Server Action Mass Edit Configuration](server_action_mass_edit/README.rst)

## Usage

### Partner VAT Unique

Once installed, the module works automatically. When creating or updating a partner with a VAT number, the system will validate that the VAT is not already in use by another partner.

### Server Action Mass Edit

1. Navigate to Settings → Technical → Server Actions
2. Create a new server action with type "Mass Edit Records"
3. Configure the fields you want to make editable
4. The action will appear in the "Action" menu of the configured model's list view

## Testing

To run the tests for all modules:

```bash
# Run all tests
python -m pytest

# Run tests for a specific module
python -m pytest partner_vat_unique/tests/
python -m pytest server_action_mass_edit/tests/
```

## Known Issues / Roadmap

Please check individual module README files for known issues and planned improvements.

## Bug Tracker

Bugs are tracked on [GitHub Issues](https://github.com/focuz-ai/odoo-utils/issues).
In case of trouble, please check there if your issue has already been reported.

## Credits

### Authors

* Focuz AI

### Contributors

#### Partner VAT Unique
* Grant Thornton Spain - Ismael Calvo <ismael.calvo@es.gt.com>
* Manuel Calero - Tecnativa
* Odoo Community Association (OCA)

#### Server Action Mass Edit
* Serpent Consulting Services Pvt. Ltd.
* Tecnativa
* GRAP
* Iván Todorovich
* Odoo Community Association (OCA)

### Maintainer

This repository is maintained by Focuz AI.

To contribute to this project, please visit our [GitHub repository](https://github.com/focuz-ai/odoo-utils).

## License

This project is licensed under the AGPL-3.0 License - see the individual module directories for specific licensing information.

Each module is licensed under [AGPL-3.0](https://www.gnu.org/licenses/agpl-3.0).