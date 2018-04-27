# Output Data
1. ADISS Load #
    - The [Trip Number](/ExtractDataFromFile/AdissCsvFile.md).
2. Dredge Load Number
    - A user input.
3. [Dredge](Dredge.md) Name
    - A user input.
4. Scow Vessel Name: From File
    - The [Scow Vessel Name](/ExtractDataFromFile/AdissCsvFile.md).
5. Tug Vessel Name
    - A user input.
6. Disposal Area
    - A user input.
7. Estimated Load
    - The volume when the scow departs the spider barge.
    - Looks up the volume using the average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
8. Average Draft Departing Spider Barge
    - The average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
9. Average Draft Leaving The Channel
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` when the scow leaves the channel. The scow is considered to have left the channel at the instant it went outside the channel and never comes back in again while in `TRANSIT`.
    - `null` if all the x/y records `Placement Phase = TRANSIT` is outside the channel.
10. Average Draft Entering ODMDS
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) when the scow is within the ODMDS Boundary.
    - `null` if no records were found where the scow is inside the ODMDS.
11. Average Draft Loss during Transit to ODMDS
    - A nullable double value that represents the difference of the average of `Aft` and `Fore` `Draft` when it departs the spider barge and when it enters the ODMDS.
    - The difference of the average of `Aft` and `Fore` `Draft` between the last [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT` and the first record where the scow is inside the ODMDS. 
    - `null` if no records were found where the scow is inside the ODMDS.
12. Start loading Date/Time
    - The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = LOADING`.
13. End loading Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = LOADING`.
14. Total Transit Time
    - The difference of the date/time between the first and last [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`. 
15. Maximum Speed during [`TRANSIT`](PlacementPhase.md)
    - The maximum speed from all the [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
16. Scow Open Date/Time
    - The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Hull Status = CLOSED`.
17. Start Dump Date/Time
    -  The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
18. Start Dump X
    - The x coordinate of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
19. Start Dump Y
    - The y coordinate of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
20. End Dump Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
21. End Dump X
    - The x coordinate of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
22. End Dump Y
    - The y coordinate of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
23. Is Emergency Dump
    - A user input indicating whether an emergency dump was carried out. `true` if emergency dump was carried out; otherwise `false`.
24. Is Mis-Dump
    - Is mis-dump is `true` if any of the x/y [records](/ExtractDataFromFile/AdissCsvFile.md#records) where Placement Phase = DISPOSAL or Hull Status = OPEN is outside the ODMDS boundary.
25. Is Dump Outside Berm
    - Is dump outside berm is `true` if any of the x/y [records](/ExtractDataFromFile/AdissCsvFile.md#records) where Placement Phase = DISPOSAL or Hull Status = OPEN is outside the Berm boundary.
26. Depart Spider Barge Date/Time
    - The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
27. Return Spider Barge Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = RETURN`.
28. StartDepartSpiderBargeDredgeCutterX
    - Dredge record is parsed from CSD MDB File.
    - StartDepart DateTime parsed from AdissCsvFile is looked up in the CSD MDB File.
        - Hydro Record DateTime should be greater than or equal the StartDepart DateTime and not later than 10 seconds.
29. StartDepartSpiderBargeDredgeCutterY
30. StartDepartSpiderBargeDredgeLadderDepth
31. StartDepartSpiderBargeDredgeCutterStation