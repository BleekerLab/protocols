# Toxicity cup bioassay for whiteflies

## Description
This controlled bioassay is meant to assess the toxicity of a compound on adult whiteflies during 24h or 48h. 
A purified SPE fraction can also be tested (e.g. hexane leaf wash fractions from Solid Phased Extraction). 

## Assay Setup (example of 7-epizingiberene)

*  Around 15 adult whiteflies per cup
*  5 biological replicates per condition.
*  5 conditions (mock, dose1, dose2, dose3, dose4)

Conditions :
*  Mock (TX-100 0,1%)
*  7-epizingiberene_1,8ug
*  7-epizingiberene_18ug
*  7-epizingiberene_35ug
*  7-epizingiberene_88ug

5 biological replicates (5 cups) x 5 conditions = 25 cups
15 whiteflies x 25 cups = 375 whiteflies


## Material needed
* Analyser cups (reference Greiner-bio one 668102); lid punched to make a hole of ~1cm diameter.
* Parafilm
* 15 whiteflies (biotype Q) per cup (keep them in ice for 1h to get them sleepy)
* 1 leaf punch of 1.5cm diameter per cup from the Moneymaker tomato cultivar.
* 30mm Whatman filter paper disc
* 2ml safe-lock eppendorf tube
* Stock solutions of the compound/fraction to be tested. 

## Protocol (per leaf disc):
1) Add a volume neccessary for given amount of the compound (hexane solution) in a 1,5ml safe-lock Eppendorf tube.
2) Dry under nitrogen and in ice.
3) Resuspend extract in 20ul of TX-100 0,1%.
4) Apply 20ul onto abaxial (bottom) side of a 1,5cm leaf disc. 
5) Let dry for ~2h at room temperature on a lab bench.
6) Place 15 “sleepy” whiteflies in a cup. Place the leaf disc abaxial (treated) side down onto punched lid, so that the hole is covered. Place wet 30mm Whatman filter paper disc on top of the leaf disc. Seal the lid on top of the cup with parafilm.
7) Measure survival after 48h incubation in the whitefly growth cabinet.

## Measurement of whitefly mortality
1) Count the number of dead and alive flies per condition and biological replicates. 

The final table should follow this format for further analysis with R. 

cup | dose | alive | dead
-------|------|-------|-----
mock-1 | mock | 10 | 3
mock-2 | mock | 11 | 3
mock-3 | mock | 9 | 4
mock-4 | mock | 10 | 3
mock-5 | mock | 10 | 5
1,8µg-1 | 1,8µg | 8 | 6
1,8µg-2 | 1,8µg | 6 | 9
1,8µg-3 | 1,8µg | 7 | 9
1,8µg-4 | 1,8µg | 4 | 11
1,8µg-5 | 1,8µg | 10 | 4
18µg-1 | 18µg | 9 | 6
18µg-1 | 18ug |	7	| 3
18µg-2 | 18ug | 14 | 10
18µg-3 | 18ug |	11 | 3
18µg-4 | 18ug |	3 | 10
18µg-5 | 18ug |	4 | 10
35µg-1 | 35ug |	8 |	4
35µg-2 | 35ug |	7 | 9
35µg-3 | 35ug | 6 | 7
35µg-4 | 35ug | 12 | 7
35µg-5 | 35ug | 12 | 6
88ug-1 | 100ug |	8 |	4
88ug-2 | 10ug | 14 | 10
88ug-3 | 10ug |	11 | 3
88ug-4 | 10ug |	3 | 10
88ug-5 | 100ug |	7 | 9







