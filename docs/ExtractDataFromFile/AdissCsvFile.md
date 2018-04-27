# ADISS CSV File

## File Header
The following items represent each line at the start of the ADISS CSV file.

1. Project Name
    - raw example (without quotes): "Project: 2018 Freeport LNG Maintenance Dredging Project"
2. Permit Code
    - raw example (without quotes): "Permit: SWG-2013-00147"
3. Client Name
    - raw example (without quotes): "Client: Great Lakes Dredge & Dock Co."
4. Trip Number
    - raw example (without quotes): "Trip: 51"
5. Scow Vessel Name
    - The scow vessel name.
    - raw example (without quotes): "Vessel Name: GL61"
6. Material Source
    - raw example (without quotes): "Material Source: UNKNOWN"
7. Transit Start
    - raw example (without quotes): "Transit Start: 4/25/2018 7:01:55 PM"
8. Disposal Start
    - raw example (without quotes): "Disposal Start: 4/25/2018 8:00:55 PM"
9. Note
    - raw example (without quotes): "Note: Coordinates are in NAD 1983 StatePlane Texas South Central FIPS 4204 Feet"
10. Line Separation
    - A single empty line to separate the [file header](#file-header) and [records](#records).
11. Record Header
    - The line populated by the header of the [records](#records):
    `Local Date/Time,Easting,Northing,Heading,Speed (knots),Aft Draft (ft),Fore Draft (ft),Water Depth (ft),Placement Phase,Hull Status`

## Records
The following items represent each field/column of the data starting from line 12 of the ADISS CSV file.

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