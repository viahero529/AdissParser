# ADISS CSV File

## File Header
The following items represent each line at the start of the ADISS CSV file.

1. Project Name
2. Contract Number
3. Client Name
4. Trip Number
5. Vessel Name
6. Material Source
7. Transit Start
8. Disposal Start
9. Note
10. Line Separation
    - A single line populated by `,,,,,,,,,` to separate the header and records.
11. Record Header
    - A single line populated by the header of the records:
    `Local Date/Time,Latitiude,Longitude,Heading,Speed (knots),Aft Draft (ft),Fore Draft (ft),Water Depth (ft),Placement Phase,Hull Status`

## Records
The following items represent each field/column of the data starting from line 12 of the ADISS CSV file.

1. Local Date Time
    - A date/time value in ""
2. Latitude
    - A double value of latitude in decimal degrees.
3. Longitude
    - A double value of longitude in decimal degrees.
4. Heading
    - A double value of heading in decimal degrees.
5. Speed
    - A double value of speed in knots.
6. Aft Draft
    - A double value of aft draft in feet.
7. Fore Draft
    - A double avlue of fore draft in feet.
8. Water Depth
    - A nullable double value of water depth in feet.
    - If `null`, printed as "N/A" without the quotes.
9. [Placement Phase](PlacementPhase.md)
    - Upper case
10. [Hull Status](HullStatus.md)
    - Upper case