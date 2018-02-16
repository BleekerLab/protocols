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
Recordings are then done every day __until all larvae die__

The analysis is a survival analysis also called "time to death". Thus, we only record:
*  __dead:__ dead thrips on day x: mark "1" in the corresponding the well coordinate and plate number
*  __alive:__ live thrips on day x: mark "0" in the well coordinate and plate number
*  __missing:__ if for some reasons you cannot find the thrips, mark "0" in the well coordinate and plate number


# Statistical analysis
A cox-proportional hazards model is then fit on the survival data. 
