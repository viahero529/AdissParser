# Output Data
1. ADISS Load #
    - The Trip Number parsed from an [ADISS CSV file](AdissCsvFile.md).
2. Dredge Load Number
    - A user input.
3. [Dredge](Dredge.md) Name
    - A user input.
4. Scow GL#: From File
    - The Vessel Name parsed from an [ADISS CSV file](AdissCsvFile.md).
5. Vessel Name
    - A user input.
6. Disposal Area
    - A user input.
7. Average Draft Departing Spider Barge
    - The average of `Aft` and `Fore` `Draft` of the first record where `Placement Phase = TRANSIT` parsed from an [ADISS CSV file](AdissCsvFile.md).
8. Average Draft Entering ODMDS
    - TODO: How to determine if entering ODMDS?
9. Average Draft Loss during Transit
    - The difference of the average of `Aft` and `Fore` `Draft` between the first and last records where `Placement Phase = TRANSIT` parsed from an [ADISS CSV file](AdissCsvFile.md). 
10. Maximum Speed during [`TRANSIT`](PlacementPhase.md)
    - The maximum speed from all the records where `Placement Phase = TRANSIT` parsed from an [ADISS CSV file](AdissCsvFile.md).
11. MisDump
    - TODO: How to determine if mis-dump?
12. E-Dump
    - A user input indicating whether an emergency dump was carried out.
13. Start `LOADING` Date/Time
    - The date/time of the first record where `Placement Phase = LOADING` parsed from an [ADISS CSV file](AdissCsvFile.md).
14. End `LOADING` Date/Time
    - The date/time of the last record where `Placement Phase = LOADING` parsed from an [ADISS CSV file](AdissCsvFile.md).
15. Depart Spider Barge Date/Time
    - The date/time of the first record where `Placement Phase = TRANSIT` parsed from an [ADISS CSV file](AdissCsvFile.md).
16. Return Spider Barge Date/Time
    - The date/time of the last record where `Placement Phase = RETURN` parsed from an [ADISS CSV file](AdissCsvFile.md).
17. Total Transit Time
    - The difference of the date/time between the first and last records where `Placement Phase = TRANSIT` parsed from an [ADISS CSV file](AdissCsvFile.md). 
18. Start Dump X/Y
    - The x/y coordinate of the first record where `Placement Phase = DISPOSAL` parsed from an [ADISS CSV file](AdissCsvFile.md).
    - TODO: [Implement other NAD83](https://github.com/gojanpaolo/AdissParser/issues/3)
19. Start Dump Date/Time
    -  The date/time of the first record where `Placement Phase = DISPOSAL` parsed from an [ADISS CSV file](AdissCsvFile.md).
20. End Dump X/Y
    - The x/y coordinate of the last record where `Placement Phase = DISPOSAL` parsed from an [ADISS CSV file](AdissCsvFile.md).
    - TODO: [Implement other NAD83](https://github.com/gojanpaolo/AdissParser/issues/3)
21. End Dump Date/Time
    - The date/time of the last record where `Placement Phase = DISPOSAL` parsed from an [ADISS CSV file](AdissCsvFile.md).
22. Scow Open Date/Time
    - The date/time of the first record where `Hull Status = CLOSED` parsed from an [ADISS CSV file](AdissCsvFile.md).
23. Estimated Load
    - A user input.
    - TODO: [Lookup from a ullage table](https://github.com/gojanpaolo/AdissParser/issues/2)
24. Start `LOADING` Dredge Station X/Y
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
25. Start `LOADING` Dredge Range X/Y
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
26. Start `LOADING` Dredge Cutter Depth
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)