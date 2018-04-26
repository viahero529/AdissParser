# Output Data
1. ADISS Load #
    - The [Trip Number](AdissCsvFile.md).
2. Dredge Load Number
    - A user input.
3. [Dredge](Dredge.md) Name
    - A user input.
4. Scow GL#: From File
    - The [Scow Vessel Name](AdissCsvFile.md).
5. Tug Vessel Name
    - A user input.
6. Disposal Area
    - A user input.
7. Average Draft Departing Spider Barge
    - The average of `Aft` and `Fore` `Draft` of the first [record](AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
8. Average Draft Leaving The Channel
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` when the scow leaves the channel. The scow is considered to have left the channel at the instant it went outside the channel and never comes back in again while in `TRANSIT`.
    - `null` if all the x/y records `Placement Phase = TRANSIT` is outside the channel.
9. Average Draft Entering ODMDS
    - A nullable double value that represents the average of `Aft` and `Fore` `Draft` of the first [record](AdissCsvFile.md#records) when the scow is within the ODMDS Boundary.
    - `null` if no records were found where the scow is inside the ODMDS.
10. Average Draft Loss during Transit to ODMDS
    - A nullable double value that represents the difference of the average of `Aft` and `Fore` `Draft` when it departs the spider barge and when it enters the ODMDS.
    - The difference of the average of `Aft` and `Fore` `Draft` between the last [records](AdissCsvFile.md#records) where `Placement Phase = TRANSIT` and the first record where the scow is inside the ODMDS. 
    - `null` if no records were found where the scow is inside the ODMDS.
11. Maximum Speed during [`TRANSIT`](PlacementPhase.md)
    - The maximum speed from all the [records](AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
12. Is Emergency Dump
    - A user input indicating whether an emergency dump was carried out. `true` if emergency dump was carried out; otherwise `false`.
13. Is Mis-Dump
    - Is mis-dump is `true` if any of the x/y [records](AdissCsvFile.md#records) where Placement Phase = DISPOSAL or Hull Status = OPEN is outside the ODMDS boundary.
14. Is Dump Outside Berm
    - Is dump outside berm is `true` if any of the x/y [records](AdissCsvFile.md#records) where Placement Phase = DISPOSAL or Hull Status = OPEN is outside the Berm boundary.
15. Start loading Date/Time
    - The date/time of the first [record](AdissCsvFile.md#records) where `Placement Phase = LOADING`.
16. End loading Date/Time
    - The date/time of the last [record](AdissCsvFile.md#records) where `Placement Phase = LOADING`.
17. Depart Spider Barge Date/Time
    - The date/time of the first [record](AdissCsvFile.md#records) where `Placement Phase = TRANSIT`.
18. Return Spider Barge Date/Time
    - The date/time of the last [record](AdissCsvFile.md#records) where `Placement Phase = RETURN`.
19. Total Transit Time
    - The difference of the date/time between the first and last [records](AdissCsvFile.md#records) where `Placement Phase = TRANSIT`. 
20. Start Dump X
    - The x coordinate of the first [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
21. Start Dump Y
    - The y coordinate of the first [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
22. Start Dump Date/Time
    -  The date/time of the first [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
23. End Dump X
    - The x coordinate of the last [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
24. End Dump Y
    - The y coordinate of the last [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
25. End Dump Date/Time
    - The date/time of the last [record](AdissCsvFile.md#records) where `Placement Phase = DISPOSAL`.
26. Scow Open Date/Time
    - The date/time of the first [record](AdissCsvFile.md#records) where `Hull Status = CLOSED`.
27. Estimated Load
    - A user input.
    - TODO: [Lookup from a ullage table](https://github.com/gojanpaolo/AdissParser/issues/2)
28. Start `LOADING` Dredge Station X
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
29. Start `LOADING` Dredge Station Y
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
30. Start `LOADING` Dredge Range X
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
31. Start `LOADING` Dredge Range Y
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)
32. Start `LOADING` Dredge Cutter Depth
    - A user input.
    - TODO: [Query .mdb file](https://github.com/gojanpaolo/AdissParser/issues/1)