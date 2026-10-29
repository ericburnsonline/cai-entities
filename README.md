# Conversational AI Entities

A growing collection of reusable entity sets for building Conversational AI virtual assistants, demos, prototypes, and MVPs.

The goal is to maintain practical entity data that can be reused across platforms rather than rebuilding common lists for every project.

## Project Status

**Active**

New entity sets will be added over time, and existing sets may be expanded, cleaned up, or normalized as they are reused in projects.

## Data Format

Entity sets are currently stored as CSV files so they remain simple to inspect, edit, and convert.

The intended columns are:

1. **Keyphrase / Entity**
2. **Slot / Tags**
3. **Synonyms**
4. **Notes**

Example:

```csv
Homeowners insurance,insurance_type,Homeowners,
```

Some entries may contain multiple tags or multiple synonyms.

Platform-specific conversion tools may be added later for systems that use different entity, lexicon, or slot formats.

## Current Entity Sets

### Aviation

**`Aviation/AirportCodes.csv`**

Contains more than 3,500 airport codes with associated city/location information.

Current follow-up work:

- Check for duplicate entries
- Review and normalize data where useful
- Potentially expand beyond the current dataset

Source and dataset notes are documented in:

`Aviation/AirportCodes.md`

### Insurance

**`Insurance/InsuranceTypes.csv`**

Contains common insurance product types and synonyms, including:

- Homeowners insurance
- Renters insurance
- Auto insurance
- Motorcycle insurance
- Life insurance
- Health insurance
- Pet insurance
- Businessowners insurance

The current dataset contains 18 entity entries.

Additional synonym expansion would make this set more useful for natural-language matching.

Source and dataset notes are documented in:

`Insurance/InsuranceTypes.md`

### eCommerce

**`eCommerce/PaymentMethods.csv`**

Contains 14 payment-method entities and associated synonyms.

The dataset distinguishes between:

- `payment_method`
- `accepted_payment_method`

This allows a conversational application to identify a requested payment method independently from whether that method is accepted by a particular site or service.

Examples include:

- PayPal
- Credit Card
- Gift Card
- Electronic Funds Transfer
- Buy Now Pay Later
- Cryptocurrency
- Cash on Delivery

Dataset notes are documented in:

`eCommerce/PaymentMethods.md`

## Planned and Candidate Entity Sets

Some likely additions include:

- Automotive makes
- Automotive models
- Vehicle service types
- Food items
- Restaurant cuisines
- Shipping carriers
- Shipping service levels
- Retail product categories
- Banking transaction types
- Account types
- Hotel amenities
- Travel classes
- Appointment types
- IT support issue categories
- Device types
- Operating systems
- Cloud platforms
- Programming languages

The exact list will evolve as useful conversational use cases come up.

## Design Goals

Entity sets in this repository should generally be:

- Reusable across multiple conversational applications
- Easy to read and edit manually
- Useful for demos as well as prototypes
- Broad enough to recognize common user phrasing
- Explicit about synonyms and alternate terminology
- Documented when data comes from an external source

## Future Work

Potential future improvements include:

- CSV validation and consistency checking
- Duplicate detection
- Automated normalization
- Conversion into platform-specific formats
- Import/export scripts for common Conversational AI platforms
- Expanded synonym coverage
- Dataset-specific tests
- Schema validation

## Data Quality Checklist

Before adding or updating an entity dataset:

- Check for duplicate keyphrases and conflicting synonyms.
- Use consistent capitalization, spacing, and naming conventions.
- Verify that CSV rows follow the documented column structure.
- Include common spoken variations, abbreviations, and alternate terminology where useful.
- Document original data sources and any transformations or assumptions in the accompanying Markdown file.
- Avoid including personal, confidential, or proprietary information.

These checks are currently manual. Automated validation and duplicate detection are planned improvements.

## Contributing

Suggestions, corrections, additional synonyms, and new entity sets are welcome.

When adding a new dataset, include a short Markdown file alongside the CSV when source attribution, assumptions, or usage notes would be helpful.

## License

See `LICENSE` for licensing information.
