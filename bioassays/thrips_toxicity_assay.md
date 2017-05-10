# Thrips toxicity assay
__Goal:__ assess the survival of western flower thrips on leaf discs treated with increasing doses of compound(s) to test. 
Purified SPE fractions can also be tested. 

# Prepare an egg wave:
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
  a.  Untreated: 20µl of water  
  b.  Mock: 5µl of ethanol 100% mixed with 15µl of water
  c.  1µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of ethanol 100%. Once solubilized, it is mixed with 15µl of water.
  d.  10µg: a volume necessary for 1µg of 2-tridecanone is dried under liquid nitrogen in ice. This dry extract is then resuspended in 5µl of ethanol 100%. Once solubilized, it is mixed with 15µl of water.
  e.  etc.
5.  Seal with an adhesive transparent lid (adhesive seal for 96-well plate). You can also keep the transparent plastic lid and seal with regular tape.

# recordings are then done every day.
The analysis is a survival analysis also called "time to death". Thus, we only record:
*  __dead:__ dead thrips on day x: mark "1" in the corresponding the well coordinate and plate number
*  __alive:__ live thrips on day x: mark "0" in the well coordinate and plate number
*  __missing:__ if for some reasons you cannot find the thrips, mark "0" in the well coordinate and plate number


# Statistical analysis
A cox-proportional hazards model is then fit on the survival data. 
