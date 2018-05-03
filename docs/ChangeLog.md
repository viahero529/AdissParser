# Change Log

# 0.1.7
- Added [Offsite to Placement Phase](PlacementPhase.md)
- Output Data
    - Changed Is Dump Outside Berm to [Is Start Dump Inside Of Berm](OutputData.md)
    - Corrected [Is Mis-Dump](OutputData.md) to only check the start dump record.
        - Was checking all the `Placement Phase = DISPOSAL or Hull Status = OPEN` records
    - Added [Is Scow Open Violation](OutputData.md)

# 0.1.6
- Corrected AverageDraftLossDuringTransitToDisposalArea calculation
- Added Aft and Fore Ullage in ADISS CSV Records.

# 0.1.5
- Corrected IsMisDump and IsDumpOutsideBerm calculation

# 0.1.4
- Added Dredge New York. See [#17](https://github.com/gojanpaolo/AdissParser/issues/17)
    - Parse DRG file. [doc](https://gojanpaolo.github.io/AdissParser/ExtractDataFromFile/DrgParsing.html)
    - Added Reef U and Reef S disposal areas. [doc](https://gojanpaolo.github.io/AdissParser/Boundaries.html)
- Updated Output Data. See [#21](https://github.com/gojanpaolo/AdissParser/issues/21) 

# 0.1.3
- Added Query CSD MDB File feature. See [#1](https://github.com/gojanpaolo/AdissParser/issues/1)
- Updated Output Data CSV column order
- Removed User Input related to Start Loading

# 0.1.2
- Updated accepted ADISS CSV file format. See [#14](https://github.com/gojanpaolo/AdissParser/issues/14)

# 0.1.1
### [Output Data](OutputData.md)
- Implemented Average Draft Entering ODMDS
- Added Is Dump Outside Berm. See [#8](https://github.com/gojanpaolo/AdissParser/issues/8)
- Added Is Mis-Dump. See [#7](https://github.com/gojanpaolo/AdissParser/issues/7)
- Added Average Draft Leaving The Channel
- Corrected Average Draft Loss during Transit to ODMDS.
- Implemented Lookup Estimated Load Size From Ullage Table. See [#2](https://github.com/gojanpaolo/AdissParser/issues/2)

### [ADISS CSV File](AddisCsvFile.md)
- Changed accepted format when parsing. See [#6](https://github.com/gojanpaolo/AdissParser/issues/6)

# 0.1.0
Initial release.