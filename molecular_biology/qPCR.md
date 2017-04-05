# From RNA isolation to Q-PCR

## RNA isolation
•	make sure to have at least 3 biological replicates
•	isolate clean total RNA (kit or phenol), there should be no degradation

## DNase treatment of isolated RNA (TURBO DNase kit Ambion)
•	RNA in 45 µl H2O dd 
•	add 5 µl 10x buffer and 0,5 µl DNase
•	20’ 37°C
•	add 5 µl DNase inactivation reagent
•	3’ RT with occasional mixing
•	1,5 ‘ max speed spin
•	pipette off RNA into clean tube without disturbing the pellet
•	nanodrop and/or put on gel to check integrity and quantify carefully

## cDNA synthesis (Revert Aid kit Fermentas)
•	include NAC and NTC (see below)
•	0,5-2 µg total RNA
•	add 1 µl oligo(dT)18
•	up to 12 µl with H2O dd
•	5’ 70°C, chill on melting ice
•	add 4 µl 5x buffer
•	add 2 µl 10 mM dNTPs
•	add 0,25-1 µl RT transcriptase (amount depending on total RNA input)
•	add 0,75-0 µl H2O dd (adds up to 1 µl with RT transcriptase)
•	60’ 42°C
•	10’ 70°C, chill on melting ice
•	when used 1 µg you count with RNA equivalent concentration of 50 ng µl-1 

## Preparation Q-PCR
•	check all cDNA samples with normal PCR (check: primer dimers, gDNA, cDNA integrity)
•	dilute to equivalent of 10 ng RNA for all samples
•	to calculate primer efficiencies take cDNA sample expected to have the highest expression and make dilution range: 1x-4x-16x-64x-256x (1x = 10 ng)
•	make non amplification control (NAC): RT reaction without RT enzyme; test cDNA for gDNA contamination
•	make no target control (NTC): do RT reaction with a water sample; test for contamination and primer dimers
•	make H2O control: water sample for each primer pair on each plate; test primer dimers 
•	dilute primers from stock (filter-tips!) to 10 µM working stocks

## Q-PCR
•	work on ice, not in strong daylight, work fast
•	see excel sheet for pipetting scheme
•	make MasterMix: 	5x EvaGreen Mix / ROX / water
•	make PrimerMix: 	dilute primers to 300 nM and add pairs together
•	mix cDNA with MM: mix 1 - mix n
•	aliquot mix 1-n over each PM
•	disperse into 2 or 3 wells (=technical replicates)
•	add NAC and NTC controls on the plate
•	add dilution range for each primer pair on the plate

## Machine
•	switch on and check the if the holder is right for strip or plate
•	start computer,  open 7500 system software
•	file / new / absolute quantification / next
•	select detector (make sure it is one with SYBR reporter)
•	next / 96-well scheme is shown; possible to fill in sample names
•	close / go to instrument tab
•	deselect 9600 emulation
•	volume 10 µl
•	stage 1: 2’ 50°C
•	stage 2: 15’ 95°C
•	stage 3: 15’’ 95°C, 1’ 60°C, 45 cycles
•	add dissociation stage
•	save as, save in your folder as sds
•	put samples in machine, close, press start and wait until run starts

•	result / amplification / 
•	select Rn vs cycle and set baseline (where all curves are flat)
•	deltaRn vs cycle and set manual Ct to point where a) all curves still linear b) nicely parallel to each other c) having largest distance from each other
•	press analyse
•	export your data to file and also to memory-stick: file / export / results / cvs

## Quality Checks
•	check raw data for strange amplification curves: both in Rn vs cycle and deltaRn vs cycle. 
•	curves should be parallel in log-linear phase, certain samples might have abnormal amplification efficiency.
•	check dissociation curves (Tdissociation should be equal in all reactions)
•	check NTC or water control for primer dimers and contaminations
•	if product in NTC, check if its Tm is different from target reaction Tm. If Tm is not very different: its Ct should be at least 5 higher than of the target reaction.
•	check NAC control for amplification of gDNA. If Tm of NAC fragment is different, check that NAC fragment is not present in target reactions. If Tm is not very different, Ct value should be at least 5 higher than of the target reaction.
•	primer specificity: only one clear curve should be present in the dissociation analysis
•	check primer efficiencies in dilution series; should be around 2 (double each cycle). Plot the log of cDNA concentration against the Ct value. (see excel calculation sheet).
