# Thrips toxicity assay
__Goal:__ assess the survival of western flower thrips on leaf discs treated with increasing doses of compound(s) to test. 
Purified SPE fractions can also be tested. 

# Prepare an egg wave:
Pod preparation:
*  Get fresh non-organic green bean pods ("snijbonen") from your local shop. 
*  Add 5ml of thick bleach and 10 drops of dishwashing liquid to 5L of tap water. Rinse 5x with tap water thoroughly until bleach is gone (no more smell).
*  Dry them with paper towel.
*  Store at 4°C in between paper towels

Buy new pods every 1 or 2 weeks.

In a plastic box with a mesh filter (for aeration), place adult female thrips on green bean pods dusted with [Typha latifolia](https://en.wikipedia.org/wiki/Typha_latifolia) (broadleaf cattail) pollen.
The rule of thumb is to count 5 eggs/day/female thrips.
*  Day 1: place adult female thrips to lay eggs (1 female lays around 5 eggs per day)
*  Day 3 to day 5: adult thrips can left on the green bean pods for 2 to 5 full days. For instance, 10 female thrips will lay around 60 eggs.
*  Day 5 to day 7: the first nymphs should be ready for experiments. Egg hatching depends on the environment conditions. Take a look frequently.


# Assay Setup (example of 2-tridecanone)
1.  Fill each well of a Greiner Bio-one 12-well plate (no 665180) with a 20mm Whatman filter paper (ref. WHA1001020) with 120µl of tap water.
2.  Take a 1.5cm diameter leaf disc from the accession of interest (leaf disk area = 1.77cm2)
3.  Place the leaf disc in the well with the adaxial side ("upper side of the leaf") upwards. 
4. Place one larvae per well onto each leaf disc.
5.  Place a 10mm Whatman filter paper (ref. WHA10016508) onto a glass dish on ice and add 20µl of liquid to the filter paper. Depending on the condition:
  *  Untreated: 20µl of water  
  *  Mock: 5µl of 100% acetone mixed with 15µl of water
  *  1µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of acetone 100%. Once solubilized, it is mixed with 15µl of water.
  *  10µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of acetone 100%. Once solubilized, it is mixed with 15µl of water.
  *   100µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of acetone 100%. Once solubilized, it is mixed with 15µl of water.
Dry for 5s with nitrogen gas. Place one treated filter paper per well.          
6.  Seal with the sides of the 12-well plate with normal adhesive tape. That way, you can keep the transparent plastic lid and seal with regular tape.
7. Place in controlled environmental conditions (21°C,16/8 day night, 60%RH).

# Measurements
Recordings are then done every day __until all larvae die__ or until a specified number of days (e.g. 7 days).

## Data recoding
The data will be analysed follwing a survival analysis also called "time to death". Thus, we only record:
*  __death:__ dead thrips on day x: mark "1" in the corresponding the well coordinate and plate number
*  __alive:__ live thrips on day x: mark "0" in the well coordinate and plate number
*  __missing:__ if for some reasons you cannot find the thrips, mark "0" in the well coordinate and plate number

To record the data, use a form where:
  - __A__ stands for "Alive"
  - __M__ stands for "Missing"
  - __D__ stands for "Dead"

For a 12-well plate for one treatment condition (e.g. untreated)

| Well | Day 1 | Day 2 | Day 3 | Day 4 | Day 5 | Day 6 | Day 7 |
| -----|-------|-------|-------|------ |-------|-------|-------|
| A1   | A | A | A | A | A | A | A |
| A2   | A | A | A | A | A | M | M |
| A3   | A | A | M | M | A | A | A |
| A4   | A | A | D | D | A | A | A | 
| B1   | A | A | A | D | D | D | D |
| B2   | A | A | A | A | A | A | D | D |

These 6 measurements should be saved as a tab-separated text file "results.txt" such as :


| Dose | Status | Day |
|------|-------|-----|
| Untreated | 0 | 7 | 
| Untreated | 0 | 6 | 
| Untreated | 0 | 7 | 
| Untreated | 0 | 7 | 
| Untreated | 1 | 3 | 
| Untreated | 1 | 7 | 

You can see that:
  - __A__ that stands for "Alive" has been translated to "0" (death event occured)
  - __M__ that stands for "Missing" has been translated to "0" (no death event occured)
  - __D__ that stands for "Dead" has been translated to "1" (death event occured) 
  
_Remark_: in some cases, thrips end up in the same well. You can then record "2xA" if the two thrips are alive and 

| Well | Day 1 | Day 2 | Day 3 | Day 4 | Day 5 | Day 6 | Day 7 |
| -----|-------|-------|-------|------ |-------|-------|-------|
| A1  | A | A | 2xA | 2xA | 2xA | 2xA | 2xA |
| A1  | A | A | 2xA | 3xA | 4xA | 2xA | 2xA |

For the first row, both individuals survived until the end. So record "0 7" twice.
For the second row, you can only be sure for two thrips so only record the measurements for these. Record "0 7" twice. 

Split the observations like:

| Dose | Status | Day |
| ------------- | ------------- | ------ |
| Untreated  | 0  | 7 |
| Untreated  | 0  | 7 |
| Untreated  | 0  | 7 |
| Untreated  | 0  | 7 |

Do this for all doses and compile all data in a "results.txt" file. An example can be seen in the Shiny app [online](http://genseq-h0.science.uva.nl/shiny/MarcGalland/thrips_survival/).

# Data analysis
## Shiny app
To analyse the data, a dedicated Shiny app is available [here](http://genseq-h0.science.uva.nl/shiny/MarcGalland/thrips_survival/) and the underlying code can be found on [Github](https://github.com/BleekerLab/project20accessions/tree/7744041b68d24ae0892e46c089058fef328b9c44/scripts/shinyApps/thrips_survival)

## Statistical analysis
A cox-proportional hazards model is then fit on the survival data. 
