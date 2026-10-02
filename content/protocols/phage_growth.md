---
title: Phage growth (for beginners)
---

This protocol is written for folks who are starting out phage work and don't super care about getting the maximum yield (highest titer or concentration of phages). Once you carry out literature review, you might find facts about the phage of your interest. You may also do some preliminary experiments to determine what works best for your phage.

There are many ways to ~~skin the cat~~ grow your phages; the important thing is that you report the protocol that you ended up using for your published data.

Online protocols and YouTube videos are super helpful. This practical protocol can supplement them, with the hope that each step's reasoning is explained.

# Growth conditions
## Growth media & temperature
- The rule of thumb is to use the growth media & temperature that you use for growing bacteria. Some phages grow better at certain temperatures, but the physiologically optimum temperature (e.g., 37°C for *E. coli*) generally works fine for rapid growth.
- Ca<sup>2+</sup> and Mg<sup>2+</sup> are shown to enhance binding of some phages to hosts. It may increase the phage yield if you add 10 mM MgSO<sub>4</sub> and 5 mM CaCl<sub>2</sub>. 

## Phage stock to propagate
You can...
- either start from a previous stock of the phage
- or, if you care about picking a single phage genotype for your experiment: make plaques, pick a single plaque, dissolve it in buffer/growth media, and use that solution as the growth source.

## Propagation media
- There are two main ways to propagate phages: in double-layer agar or in liquid cultures. Both generally work well for lab-adapted phages. 

# The actual protocol(s)

## Propagation in liquid cultures - easier, requires less media prep
- Grow bacterial cells to exponential phase in shaking culture flasks.
	- Some phages care about the host's growth phase (e.g., exponential phase may be when maximum number of receptors are expressed), some don't.
- Add 10-100 μL of phages (see "Phage stock to propagate" above).
- Grow for 4 h – overnight. Then move on to the isolation step.

## Propagation on solid media (Double Layer Agar method)
- Bottom agar: 1.5% agar in growth media (similar to agar plates that we pour for growing bacterial colonies)
- Top agar: 0.3-0.75% agar in growth media. Keep this molten.
	- Autoclaved agar can be stored on the shelf (solidified) and microwaved *gradually* when used. *Gradually* means that if you blast the microwave for a few minutes at full power, the bottle will spill which will change effective agar concentration and make a mess in the microwave.
	- Exact agar concentration varies from phage to phage. Traditionally common λ or T-phages infecting *E. coli* grow fine within 0.75% (or lower) top agar. Jumbo phages of *Pseudomonas* or *Enterobacter* are temperamental and need low agar concentration (0.3-0.35%) for top agar.
	- If you are working with a phage that has published concentration of top agar, just go with what is in the publication. If you got your phage from a collaborator, just ask them what top agar concentration to use.
	- When in doubt about not getting phage growth, lower the top agar concentration- this is to account for potential water loss (and hence effective raise in agar concentration) during storage or treatment of the top agar.
- Make ~4 mL aliquots of the molten agar and keep them on a heating block around 50°C. Most phages are not degraded at this temperature. If you think that might be happening for you, lower this temperature to ~40-45°C. I would use low-melting agarose instead of agar if lowering this temperature further (to avoid solidification on the heat block which results in chunky top agar on the plate).
- Dilute your source phage stock 1:100 (10<sup>-2</sup> dilution) and prepare a 10-fold dilution series (10<sup>-3</sup> – 10<sup>-7</sup>).
	- Dilution medium can be growth medium (liquid) or salty buffer. I would refrain from using water to avoid osmotic shock for the phages, but have heard of folks using water for robust phages like T4. PBS works great if you are frugal (like me) about restricting access (source of potential contamination) to the growth medium. 
	- You can dilute 10 μL of original stock in 990 μL for the 10<sup>-2</sup> dilution and 20 μL of previous solution into 180 μL of the dilution medium.
	- U-bottom well plates paired with multichannel pipettes are a lifesaver for dilutions, especially if working with multiple phages. If working with just one, microcentrifuge tubes are slightly better (because you can vortex them to mix thoroughly).
- Add 100 μL of overnight bacterial culture and 100 μL of a dilution-solution to 4 mL molten agar, vortex the tube to mix the contents, and pour them on pre-warmed bottom agar plates.
	- Pre-warming is to avoid immediate and uneven solidification of top agar. Room temperature plates are generally fine, but make sure to pre-warm plates if pulling them out of the fridge.
	- Bottom agar is often optional, but helps support robust growth.
- Incubate at the desired temperature overnight/longer.
- The plates will have varying number of plaques (clearings made by the phage on the bacterial lawn), generally depending on the dilution-solution used. Pick a plate with lacey or webby pattern (plaques overlapping with one another) for phage isolation.
	- If plaques are too far apart (in a plate made from a higher dilution of phages), the number of phages isolated will be small. If phage concentration is too high, they will kill all the bacteria and will run out of food source to replicate. So we pick an intermediate dilution to optimize the phage concentration that we get at the end of incubation.
- Scoop up the top agar using a spatula, dissolve it in equal amount of liquid (4 mL media or salty buffer), and vortex thoroughly to dislodge phage particles from the agar.
	
## Phage isolation
- [Optional] Add a few drops of chloroform to lyse cells and extract any assembled phage particles from within the cells.
	- Chloroform will inactivate enveloped/lipid-containing phages (e.g., phage phi6 infecting *Pseudomonas syringae*), so it should be skipped for those systems.
- Centrifuge for 10-15 minutes (anything between 1500×g and 5000×g generally works great) to pellet down cells and/or agar debris.
- Pass the supernatant through 0.22 μm filter (PVDF filter works great). 
	- You might have to use multiple filters, generally when the phage concentration is too high. This is a first-world problem, enjoy your high phage concentration!
	- If working with unusually large phages, consider 0.45 μm filters.
- The filtrate is your phage solution (also called a "lysate" or "phage stock"). 

## Storage 
- __Short/medium-term (4°C) __: Most lab-adapted phages are perfectly happy sitting in the fridge at 4°C, often for months to years. This is the easiest and most common storage method, and is fine for day-to-day lab use.
	- Phage titer (concentration) can slowly decay over time at 4°C. The rate of decay depends heavily on the phage. If you're relying on an old stock for an important experiment, it's good practice to re-titer it (count plaques again) rather than assume the original titer still holds.
	- Store stocks in a buffer or media you trust won't support bacterial growth if contaminated (e.g., SM buffer or PBS), and keep lysates in tightly capped tubes to avoid evaporation (which concentrates salts/agar and can stress phages).



- __Long-term (-80°C) __: For archival stocks (e.g., a reference stock of an important phage you don't want to lose), freezing at -80°C is common.
	- Glycerol (typically 15-25% final concentration) is often added as a cryoprotectant, similar to how you'd freeze a bacterial stock; though many robust phages survive freezing without it. If you're unsure, check what others have published for your phage of interest.
	- Avoid repeated freeze-thaw cycles, which can reduce titer over time. If you expect to use a frozen stock often, consider making several single-use aliquots up front rather than freeze-thawing one tube repeatedly.
	- Note that -80°C storage isn't strictly necessary for most lab-adapted phages. 4°C stocks will likely outlive your PhD. Freezing is more about long-term insurance (e.g., protecting against fridge failure, contamination, or just wanting a "clean" backup you don't touch).
	
# Bonus: phage enumeration
- Follow the dilution series approach mentioned under Propagation on solid media (Double Layer Agar method) above, for 10<sup>-4</sup>–10<sup>-9</sup> dilution.
- Identify a plate with countable (30–300) plaques.
- Count the number of plaques and back-calculate the dilution, like the example below:
	- Assume you found 63 plaques at 10<sup>-7</sup> dilution.
	- This means 63 PFU (Plaque-Forming Units) were there in 100 uL of this dilution.
	- Which implies that there must be 630 PFU in 1 mL of this dilution. 
	- Hence, there must be 630×10<sup>7</sup> PFU/mL = 6.3×10<sup>9</sup> PFU/mL in the original stock.