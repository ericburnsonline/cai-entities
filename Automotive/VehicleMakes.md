# Vehicle Makes

## Source

The initial vehicle-make data was derived from the U.S. National Highway Traffic Safety Administration (NHTSA) Vehicle Product Information Catalog and Vehicle Listing API (vPIC).

Source:

https://vpic.nhtsa.dot.gov/api/

The source data includes NHTSA `Make_ID` values and vehicle manufacturer names.

## Dataset Notes

This dataset is not intended to reproduce the complete NHTSA manufacturer list.

NHTSA's source data includes thousands of manufacturers covering passenger vehicles, trailers, specialty equipment, custom manufacturers, and other vehicle-related companies.

For Conversational AI use, this dataset contains a curated subset of commonly encountered consumer vehicle makes.

The source names have been normalized for readability where appropriate, while the corresponding NHTSA `Make_ID` is retained in the Notes field for traceability.

Conversational aliases have also been added where they are likely to occur in normal user language.

Examples include:

- Chevrolet → `Chevy`
- Volkswagen → `VW`
- Mercedes-Benz → `Mercedes`, `Mercedes Benz`
- Lamborghini → `Lambo`

Aliases are intended to improve entity recognition and are not part of the original NHTSA dataset.

## Entity Type

`vehicle_make`

## Format

See the repository README for the current CSV column format and conventions.

## Future Work

Potential future improvements include:

- Adding additional current vehicle makes
- Adding historically significant or discontinued makes
- Reviewing and expanding conversational aliases
- Adding vehicle models as a separate entity set
- Creating scripts to regenerate or validate the dataset against current NHTSA vPIC data
