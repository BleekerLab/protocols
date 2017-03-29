# Toxicity cup bioassay for whiteflies

## Description
This controlled bioassay is meant to assess the toxicity of a compound on adult whiteflies during 24h or 48h. 
A purified SPE fraction can also be tested (e.g. hexane leaf wash fractions from Solid Phased Extraction). 

## Setup for one cup

*  Around 15 adult whiteflies per cup
*  5 biological replicates per condition.
*  5 conditions (untreated, mock, dose1, dose2, dose3)

Conditions (for one cup):
*  Untreated (water)
*  Mock (water)
*  Compound1ug 2-tridecanone / cup
*  10ug 2-tridecanone / cup
*  100ug 2-tridecanone / cup
5 biological replicates (15 whiteflies each) x 5 conditions = 25 cups

Per sample
Untreated = 20ul water
Mock = 15ul water + 5ul 100% ethanol
1ug = 15ul water + 5ul 100% ethanol + 1ug dry extract
10ug = 15ul water + 5ul 100% ethanol + 10ug dry extract
100ug = 15ul water + 5ul 100% ethanol + 100ug dry extract


## Material needed
* Analyser cups (reference Greiner-bio one 668102) pierced within the lid
* Parafilm
* 15 whiteflies (biotype Q) per cup (keep them in ice for 1h to get them sleepy)
* 1 leaf punch of 1.5cm diameter per cup from the Moneymaker tomato cultivar.
* 30mm whatman filter paper 
* 2ml safe-lock eppendorf tube
* Stock solutions of the compound/fraction to be tested. 

## Protocol:
1) Add the necessary volume for each quantity of compound/fraction in a 2ml safe-lock Eppendorf tube.
2) Dry under nitrogen and in ice. You get a dry extract of the compound/fraction
3) Resuspend the 2-tridecanone dry extract in 5ul of 100% ethanol 
4) Add 15ul of MilliQ water. Mix well. 
5) Apply 20ul per leaf punch 
6) Place 15 “sleepy” whiteflies in each cup. Place the pierced lid, the leaf coated with the product and a piece of parafilm to hold it in place. 
7) Measure after 24h or 48h in the whitefly growth cabinet

## Measurement of whitefly mortality
1) Place the cup with the whiteflies in ice for ~1h. 
2) Count the number of dead and alive flies per condition and biological replicates. 

The final table should follow this format for further analysis with R. 

cup | dose | alive | dead
-------|------|-------|-----
untreated-1 | untreated | 10 | 3
untreated-2 | untreated | 10 | 3
untreated-3 | untreated | 10 | 3
untreated-4 | untreated | 10 | 3
untreated-5 | untreated | 10 | 3
mock-1 | mock | 10 | 3
mock-2 | mock | 10 | 3
mock-3 | mock | 10 | 3
mock-4 | mock | 10 | 3
mock-5 | mock | 10 | 3
1µg-1 | 1µg | 10 | 3
1µg-2 | 1µg | 10 | 3
1µg-3 | 1µg | 10 | 3
1µg-4 | 1µg | 10 | 3
1µg-5 | 1µg | 10 | 3
10µg-1 | 10µg | 9 | 6
10ug-1 | 10ug |	7	| 3
10ug-2 | 10ug | 14 | 10
10ug-3 | 10ug |	11 | 3
10ug-4 | 10ug |	3 | 10
100ug-1 | 100ug |	8 |	4
100ug-2 | 100ug |	7 | 9
100ug-3 | 100ug | 6 | 7
100ug-4 | 100ug | 12 | 7






