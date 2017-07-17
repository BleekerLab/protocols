# Thrips toxicity assay
__Goal:__ assess the survival of western flower thrips on leaf discs treated with increasing doses of compound(s) to test. 
Purified SPE fractions can also be tested. 

# Prepare an egg wave:
Pod preparation:
*  Get fresh non-organic green bean pods ("snijbonen") from your local shop. 
*  Rinse with a lot of water and some bleach. Rinse thoroughly until bleach is gone (no more smell).
*  Dry them with paper towel.
*  Store at 4°C in between paper towels

Buy new pods every 1 or 2 weeks.

In a plastic box with a mesh filter (for aeration), place adult female thrips on green bean pods dusted with pollen.
The rule of thumb is to count 5 eggs/day/female thrips.
*  Day 1: place adult female thrips to lay eggs (1 female lays around 5 eggs per day)
*  Day 3 to day 5: adult thrips can left on the green bean pods for 2 to 5 full days. For instance, 10 female thrips will lay around 60 eggs.
*  Day 5 to day 7: the first nymphs should be ready for experiments. Egg hatching depends on the environment conditions. Take a look frequently.


# Assay Setup (example of 2-tridecanone)
1.  Fill each well of a Greiner Bio-one 12-well plate (no 665180) with a 20mm Whatman filter paper with 150µl of tap water.
2.  Take a 1.5cm diameter leaf disc from the accession of interest (leaf disk area = 1.77cm2)
3.  Place the leaf disc in the well with the abaxial side ("down side of the leaf") upwards. 
4.  Each leaf disk receives 20µl of liquid. Depending on the condition:
  *  Untreated: 20µl of water  
  *  Mock: ACETONE
  *  1µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of ethanol 100%. Once solubilized, it is mixed with 15µl of water.
  *  10µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of ethanol 100%. Once solubilized, it is mixed with 15µl of water.
  *   10µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of ethanol 100%. Once solubilized, it is mixed with 15µl of water.
5.  Seal with the sides of the 12-well plate with normal adhesive tape. That way, you can keep the transparent plastic lid and seal with regular tape.
6. Place in controlled environmental conditions (temperature, light, humidity)

# Measurements
Recordings are then done every day __until all larvae die__

The analysis is a survival analysis also called "time to death". Thus, we only record:
*  __dead:__ dead thrips on day x: mark "1" in the corresponding the well coordinate and plate number
*  __alive:__ live thrips on day x: mark "0" in the well coordinate and plate number
*  __missing:__ if for some reasons you cannot find the thrips, mark "0" in the well coordinate and plate number


# Statistical analysis
A cox-proportional hazards model is then fit on the survival data. 
