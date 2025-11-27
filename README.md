# Odoo Property Addon

A custom Odoo 18 module that extends the product template with real estate-specific fields and information management.

## Overview

This module adds comprehensive real estate property information to Odoo's product template, enabling users to manage property listings with details such as location, pricing, amenities, and unit specifications.

## Features

- **Project & Location Information**: Track project location and property type
- **Building Details**: Record building and unit numbers
- **Area Measurements**: Store unit area and total building area
- **Dual Pricing System**: 
  - Cash pricing (meter price and total)
  - Installment pricing (meter price and total)
- **Amenities Management**: Track facilities including:
  - Garage availability
  - Club house access
  - Garden features
  - Garden area
  - Roof area
- **Unit Description**: Text field for detailed property descriptions
- **Location Details**: Specific unit location information

## Requirements

- Odoo 18.0
- Dependencies:
  - `product` module
  - `stock` module

## Installation

1. Clone or copy the module to your Odoo custom addons directory:
   ```bash
   /path/to/odoo/custom_addons/app_one/
   ```

2. Update your `odoo.conf` file to include the custom addons path:
   ```ini
   [options]
   addons_path = /path/to/odoo/addons,
                 /path/to/odoo/odoo/addons,
                 /path/to/odoo/custom_addons
   ```

3. Restart the Odoo server

4. Update the apps list:
   - Go to Apps menu
   - Click "Update Apps List"

5. Search for "App one" and click Install

## Module Structure

```
app_one/
├── __init__.py
├── __manifest__.py
├── models/
│   ├── __init__.py
│   └── product_template.py
└── views/
    └── product_template_views.xml
```

## Configuration

### Database Setup

The module expects the following PostgreSQL configuration:

- **Host**: localhost
- **Port**: 5432
- **Database User**: odoo18
- **Database Password**: odoo18

Update your `odoo.conf` file with appropriate credentials for your environment.

## Usage

1. Navigate to **Inventory > Products > Products**
2. Open any product or create a new one
3. Scroll to the "General Information" tab
4. Find the new "Real Estate Information" section with the following groups:
   - Project / Location
   - Building Information
   - Area Information
   - Location Details
   - Cash Pricing
   - Installment Pricing
   - Amenities
   - Unit Description

## Field Descriptions

| Field Name | Type | Description |
|------------|------|-------------|
| Project / Location | Char | Name or location of the real estate project |
| Type | Char | Property type (e.g., apartment, villa, commercial) |
| Building No. | Char | Building identifier |
| Unit No. | Char | Unit identifier within the building |
| Unit Area | Char | Area of the unit |
| Total Building Area | Float | Total area of the building |
| Meter Price (Cash) | Monetary | Price per square meter for cash payment |
| Total Cash Price | Monetary | Total price for cash payment |
| Meter Price (Installment) | Float | Price per square meter for installment |
| Total Installment Price | Float | Total price for installment payment |
| Unit Location | Char | Specific location details of the unit |
| Garage | Boolean | Garage availability |
| Club House | Boolean | Club house access |
| Garden | Boolean | Garden availability |
| Garden Area | Boolean | Separate garden area |
| Roof Area | Boolean | Roof area access |
| Unit Description | Text | Detailed description of the property |

## Author

**Ahmed Abdulghany**

## License

LGPL-3

## Version

18.0.1.0.0

## Support

For issues, questions, or contributions, please contact the module author.

---

**Note**: This module is designed specifically for Odoo 18.0 and may require modifications for compatibility with other versions.
