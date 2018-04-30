# Output Data
1. ADISS Load #
    - The [Trip Number](/ExtractDataFromFile/AdissCsvFile.md).
2. Dredge Load Number
    - A user input.
3. [Dredge](Dredge.md) Name
    - A user input.
4. Scow Vessel Name
    - The [Scow Vessel Name](/ExtractDataFromFile/AdissCsvFile.md).
5. Tug Vessel Name
    - A user input.
6. Disposal Area
    - A user input.
7. Average Draft Loss During Transit To Disposal Area
    - A nullable double value that represents the difference of the average of `Aft` and `Fore` `Draft` when the scow starts transiting to the disposal area and when it enters the disposal area.  
    - The first `Placement Phase = TRANSIT` record is when the scow starts transiting to the disposal area.
    - The first `Placement Phase = TRANSIT` record where the scow is inside the disposal area is when it enters the disposal area.
    - `null` if no record was found where the scow is inside the disposal area.
8. Maximum Speed during [`TRANSIT`](PlacementPhase.md)
    - The maximum speed from all the [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
9. Is Dump Outside Berm
    - A nullable boolean value that represents whether the scow dumped outside the berm.
    - `true` if the scow dumped outside the berm. `null` if no berm is designated based on the selected dredge (i.e. Dredge New York). otherwise `false`.
    - Is dump outside berm is `true` if any of the x/y [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL` or `Hull Status = OPEN` is outside the Berm boundary.
10. Is Mis-Dump
    - Is mis-dump is `true` if any of the x/y [records](/ExtractDataFromFile/AdissCsvFile.md#records) where Placement Phase = DISPOSAL or Hull Status = OPEN is outside the ODMDS boundary.
11. Is Emergency Dump
    - A user input boolean value indicating whether an emergency dump was carried out. `true` if emergency dump was carried out; otherwise `false`.
12. Start loading Date/Time
    - The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = LOADING`.
13. End loading Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = LOADING`.
14. Start Transit To Disposal Area Date/Time
    - The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
15. Average Draft Start Transit To Disposal Area
    - The average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
16. Average Draft Entering Disposal Area
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) when the scow is within the disposal area.
    - `null` if no records were found where the scow is inside the disposal area.
17. Start Dump X
    - The x coordinate of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
18. Start Dump Y
    - The y coordinate of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
19. Start Dump Date/Time
    -  The date/time of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
20. End Dump X
    - The x coordinate of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
21. End Dump Y
    - The y coordinate of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
22. End Dump Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
23. Average Draft Leaving The Channel
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` when the scow leaves the channel. The scow is considered to have left the channel at the instant it went outside the channel and never comes back in again while in `TRANSIT`.
    - `null` if all the x/y records `Placement Phase = TRANSIT` is outside the channel.
24. End Return From Disposal Area Date/Time
    - The date/time of the last [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = RETURN`.
25. Total Transit Duration
    - The difference of the date/time between the first and last [records](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`. 
26. Estimated Load
    - The volume when the scow starts transiting to the disposal area.
    - Looks up the volume using the average of `Aft` and `Fore` `Draft` of the first [record](/ExtractDataFromFile/AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
27. Start Transit To Disposal Area Dredge X
    - The x-coordinate of the dredged location when the scow starts transiting to the disposal area.
    - Dredge record is parsed from [CSD MDB](ExtractDataFromFile/CsdMdbQuerying.md) or [Dredge New York DRG](ExtractDataFromFile/DrgParsing.md) file/s.
        - Dredge Record DateTime should be greater than or equal the looked up DateTime and not later than 10 seconds.
28. Start Transit To Disposal Area Dredge Y
29. Start Transit To Disposal Area Dredge Depth
30. Start Transit To Disposal Area Dredge Station