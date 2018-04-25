# ADISS CSV File

## File Header
The following items represent each line at the start of the ADISS CSV file.

1. Project Name
2. Contract Number
3. Client Name
4. Trip Number
5. Vessel Name
    - The scow vessel name.
6. Material Source
7. Transit Start
8. Disposal Start
9. Note
10. Line Separation
    - A single empty line to separate the [file header](#file-header) and [records](#records).
11. Record Header part 1
    - The first line populated by the header of the [records](#records):
    `Local Date/Time,Easting,Northing,Heading,Speed (knots),Aft Draft (ft),Fore Draft (ft),`
12. Record Header part 2
    - The second line populate by the header of the [records](#records):
    `Water Depth (ft),Placement Phase,Hull Status`

## Records
The following items represent each field/column of the data starting from line 13 of the ADISS CSV file.

1. Local Date Time
    - A date/time value.
2. Easting
    - A double value of easting in international feet.
3. Northing
    - A double value of northing in international feet.
4. Heading
    - A double value of heading in decimal degrees.
5. Speed
    - A double value of speed in knots.
6. Aft Draft
    - A double value of aft draft in international feet.
7. Fore Draft
    - A double avlue of fore draft in international feet.
8. Water Depth
    - A nullable double value of water depth in international feet.
    - If `null`, printed as "N/A" without the quotes.
9. [Placement Phase](PlacementPhase.md)
    - Upper case
10. [Hull Status](HullStatus.md)
    - Upper case