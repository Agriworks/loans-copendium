# Loans Compendium

A comprehensive repository of government loan schemes from both Central and State governments in India. This compendium provides structured information about various loan programs, their eligibility criteria, application processes, and contact details.

## Repository Structure

```
loans-copendium/
├── AP-Governement/          # Andhra Pradesh State Government Schemes
│   ├── Scheme-1.md         # Agricultural Loan Scheme
│   └── Scheme-2.md         # Micro-enterprise Development Scheme
├── Central-Government/      # Central Government Schemes
│   ├── Scheme-1.md         # Pradhan Mantri Mudra Yojana
│   └── Scheme-2.md         # Pradhan Mantri Kisan Sampada Yojana
└── README.md               # This documentation file
```

## Data Structure

Each scheme document follows a standardized format with:

### 1. YAML Front Matter (Metadata Block)
All documents contain structured metadata in YAML format at the beginning, enclosed between `---` markers:

```yaml
---
title: "Scheme Name"
description: "Brief description of the scheme"
category: "government-level"
government_level: "state|central"
state: "State Name or all-states"
scheme_type: "loan"
target_audience: "target-group"
loan_amount_min: 50000
loan_amount_max: 500000
interest_rate: 4.5
tenure_years: 5
eligibility_criteria:
  - "Criteria 1"
  - "Criteria 2"
required_documents:
  - "Document 1"
  - "Document 2"
application_process:
  - "Step 1"
  - "Step 2"
contact_info:
  office: "Office Name"
  phone: "Phone Number"
  email: "Email Address"
  website: "Website URL"
last_updated: "2024-01-15"
status: "active"
---
```

### 2. Markdown Content
After the metadata block, each document contains detailed information in Markdown format including:
- Overview
- Key Features
- Loan Details
- Eligibility Requirements
- Required Documents
- Application Process
- Benefits
- Contact Information
- Important Notes

## Parsing the Data

To parse the scheme documents, you need to:

1. **Extract YAML Front Matter**: Parse the metadata block between the `---` markers at the beginning of each document
2. **Parse Markdown Content**: Extract the markdown content after the metadata block
3. **Convert to Desired Format**: Transform the data into your application's required format (JSON, HTML, etc.)

### General Approach

1. **Split the document** at the `---` markers to separate metadata from content
2. **Parse YAML metadata** using a YAML parser for your programming language
3. **Process markdown content** using a markdown parser if HTML output is needed
4. **Query and filter** based on metadata fields as needed

### Common Use Cases

- **Filter by government level**: Find all central or state government schemes
- **Search by loan amount**: Find schemes within specific loan amount ranges
- **Filter by target audience**: Find schemes for specific groups (farmers, entrepreneurs, etc.)
- **Search by interest rate**: Find schemes with competitive interest rates
- **Filter by state**: Find schemes applicable to specific states

## Metadata Fields Reference

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `title` | String | Name of the scheme | "AP Government Scheme 1" |
| `description` | String | Brief description | "Comprehensive loan scheme..." |
| `category` | String | Category classification | "state-government" |
| `government_level` | String | Level of government | "state" or "central" |
| `state` | String | Applicable state | "Andhra Pradesh" or "all-states" |
| `scheme_type` | String | Type of scheme | "loan" |
| `target_audience` | String | Target group | "farmers", "entrepreneurs" |
| `loan_amount_min` | Integer | Minimum loan amount | 50000 |
| `loan_amount_max` | Integer | Maximum loan amount | 500000 |
| `interest_rate` | Float | Interest rate percentage | 4.5 |
| `tenure_years` | Integer | Maximum tenure in years | 5 |
| `eligibility_criteria` | Array | List of eligibility requirements | ["Must be resident", "Age 18-65"] |
| `required_documents` | Array | List of required documents | ["Aadhaar Card", "PAN Card"] |
| `application_process` | Array | Steps in application process | ["Visit office", "Fill form"] |
| `contact_info` | Object | Contact details | `{office: "Name", phone: "123"}` |
| `last_updated` | String | Last update date | "2024-01-15" |
| `status` | String | Scheme status | "active" |

## Contributing

When adding new schemes to this repository:

1. Follow the established metadata structure
2. Use consistent field names and data types
3. Include all required metadata fields
4. Provide comprehensive markdown content
5. Update this README if adding new metadata fields


## License

This project is licensed under the MIT License - see the LICENSE file for details.