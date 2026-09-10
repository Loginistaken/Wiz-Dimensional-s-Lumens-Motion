LM-STX 6.0 free-piston Stirling + 300 kWh multi-zone thermal reserve + 90 kWh battery + ATEG + LM-H2C heat-to-cold 
stage + adaptive solar-thermal skin + EL-60 predictive energy computerRebuilt from every architectural idea in Wiz-Dimensional-s-Lumens-Motion,
then closed with the KIT / University of Tsukuba heat-driven elastocaloric cooler.scitechdaily.comEngineering status. Lumens Motion 6.0 is a
conceptual reconstruction. No mileage, power, thermal-efficiency, cooling-capacity, heat-exhaust, charging, or material figure below has been 
demonstrated on a working vehicle. The numbers are engineering targets used to decide whether the rebuilt architecture is worth pursuing. 
Prototype, thermal, optical, Stirling, elastocaloric, battery, aerodynamic, and full energy-balance tests would be required before any 
performance number could be claimed.
Not yet as proven range.6.0 is an upgrade because 
it rebuilds the whole Lumens stack around one missing conversion that 1.5 through 5.1 kept asking for and never named as hardware:waste 
heat → mechanical strain → cold.From Heat-waste-cooling-Recycle-V1.5.md onward, the repo treated rejected Stirling heat as a resource. 
LM-TCC put a heat-driven refrigeration block after the engine. 5.0.md said that block could be an absorption or thermoelectric cabin cooler. 
5.1.md kept the cascade, added ATEG, and then described cabin heating and battery conditioning — but dropped the explicit heat-to-cold machine. 
That left a hole: 5.1 can turn leftover heat into a few more watts, or into warmth. It cannot turn leftover heat into cold without spending 
battery current on a compressor.github.comThe SciTechDaily / Nature Energy device fills that hole with a real mechanism. 
Two ultrathin nickel-titanium films do the two jobs that used to require an electric actuator: one film turns ~86–130 °C heat into pull; 
the second film uses that pull to drop temperature through the elastocaloric effect. KIT already lists automotive electronics cooled by
drivetrain heat as a target.kit.eduThat is the upgrade.It is not an upgrade of the 5.1 range envelope by itself. 
The published cooler produced 2.79 mW and a device lift of 2.2 K on real external heat. Cabin air-conditioning is
still a 3–9 kW problem. 6.0 therefore upgrades the thermal logic of every inherited part — skin, canopy, receiver, 
reservoir, Stirling, ATEG, battery, motors, EL computer — so mid-grade heat can become cold for electronics,
pack hot spots, and later a cabin assist. It does not claim 1,200-mile summers or a deleted radiator.One-line 
verdict: 6.0 is an upgrade if “upgrade” means the vehicle finally uses heat for cooling instead of burning
electricity to fight its own waste heat. It is not an upgrade if “upgrade” means the 900 / 625 / 350 mile 
targets get larger on paper.The heat-to-cold conceptConventional cars spend electricity to pump heat out of 
the cabin and pack. Lumens already spends heat to make electricity. 6.0 inserts a third conversion between 
those two facts.Concentrated sunlight charges a high-temperature store.
The LM-STX Stirling turns the highest-value heat into electricity for the wheels.
ATEG skims a little more electricity from the leftover gradient.
LM-H2C takes what is left in the 90–130 °C band and uses it as the actuator for solid-state cooling.
Only heat with no remaining job hits the radiator.The published machine works like this:electronicsforu.comActuator
film: 22 µm one-way shape-memory TiNi. Heat shrinks it. That is the motor.
Refrigerant film: 26.5 µm superelastic TiNiFe. Stretch and release change its crystal structure and its temperature. That is the refrigerator.
Coupling transfers force, not heat.
Cycle ~0.83 Hz.Published anchors used as 6.0 design limits, not marketing numbers:nature.comQuantity
Lab result
6.0 use
Actuator heat
86 °C / 130 °C external
LM-TCC mid-T zone
Film ΔT
12.9 K
material limit
Device ΔT
4.0 K electric / 2.2 K waste-heat
conservative design case
Specific cooling power
4.43 / 3.32 W g⁻¹
scale-up estimate
Device cooling power
2.79 mW
proof only
First vehicle job
—
electronics + pack edges
Cabin job
—
assist after multi-stage span existsHeat-driven cooling is still a heat pump. Driving heat plus lifted cabin/pack heat 
must be rejected. 6.0 does not repeal the second law. It relocates cold production onto a heat stream that 5.1 was already carrying.
Design canvastextLUMENS MOTION 6.0 CANVAS
================================================================
PURPOSE
  Long-range solar-thermal-electric vehicle that stores heat and
  electricity, then spends leftover heat on cold before the radiator.IS THIS AN UPGRADE?
  Architecture: YES.  Range claim: NOT YET.
  New conversion: heat → strain → cold (LM-H2C).PRIMARY LOOP
  Sun → optics → SiC receiver → 300 kWh multi-zone store
    → LM-STX → linear alternator → DC bus → motors → wheelsPARALLEL LOOPS
  Sun → PV skin → DC bus / battery
  Wheels → regen → battery
  Residual heat → ATEG → electricity
  Residual 90–130 °C heat → LM-H2C → cold
  Cold → electronics / pack / cabin assist
  Last heat → radiatorSTORES
  Thermal  ~300 kWh usable   (SiC + graphite + PCM + insulation)
  Electric ~90 kWh usable    (buffer, peaks, regen)CONVERTERS
  LM-STX 6.0     35–45 kW electric target from heat
  ATEG           5–8% of appropriate residual stream (target)
  LM-H2C         heat-actuated elastocaloric cold
  4 motors       propel + regenerateBRAIN
  EL-60          Divergence → Resonance → Phase-Lock → Convergence
                 now includes a cold-demand termPLATFORM SEED (from 3.0)
  Expedition envelope ~8.2 m × 2.6 m so canopy, store, and cascade fit
================================================================

Energy philosophySUN → HEAT + ELECTRICITY → STORAGE → PROPULSION → RECOVERY → COLD → PROPULSION AGAINHeat does work first. 
Electricity handles transients. Cold is made from heat that already failed to make more work.Rebuilt energy pathEvery
earlier path is kept. One stage is added.textSUNLIGHT
   ├─ photonic / concentrating skin ──────────────► thermal receiver
   ├─ PV fraction of skin ────────────────────────► DC bus / 90 kWh battery
   └─ 130 m² deployable canopy (parked / slow) ───► receiver / storeSiC RECEIVER  →  SiC/Inconel exchanger  →  HIGH-T ZONE (~Stirling hot side)
                                         →  MID-T ZONE (~90–200 °C)
                                         →  LOW-T ZONE (cabin / pack / H2C reject)HIGH-T ZONE → LM-STX 6.0 (He free-piston) → linear alternator → HV DC BUS
                                         → cold-side residual heatRESIDUAL HEAT
   → ATEG  → extra watts to DC bus
   → preheat / intermediate PCM
   → LM-H2C actuator (90–130 °C) → cold to electronics / pack / cabin assist
   → cabin heat or battery warmup
   → radiator (last)HV DC BUS → inverters → 4 motors → wheels
Wheels → motors as generators → inverter → battery
EL-60 coordinates every arrow.Rebuilt componentsEach block below is an inherited repo idea, reconstructed so it can feed or accept
LM-H2C.1. Photonic energy skinKept from 4.0 / 5.1. The body is still structure, aero surface, and collector at once: PV cells,
thermal collection patches, light guides, and protected concentrators. On-the-move collection is a range extender, 
not the highway engine. In 6.0 the skin also dumps a little low-grade heat into the H2C reject path when the cabin 
is already cold and the pack is already warm, so the skin is no longer only an input.2. Deployable solar canopyKept 
at ~130 m² as the design point. At 800 W/m² that is ~104 kW incident before losses. The old 23% “electrical-equivalent”
figure (~24 kW) stays a target, not a measured efficiency. Parked charging of the thermal store is still the canopy’s main
job. 6.0 can also hold a mid-T slice of that charge specifically for H2C so the vehicle can pre-cool electronics and the
pack before a hot drive, instead of pre-cooling with the battery.3. Adaptive optical concentratorKept. EL-60 opens
concentration when the high-T store is low, and defocuses at the receiver limit. New rule: do not over-fill the mid-T 
zone just to run H2C if the high-T zone is hungry. Propulsion heat outranks cooling heat.4. SiC photonic receiverKept 
as the combustion-free furnace. Concentrated light hits silicon carbide; heat crosses into the store or the Stirling heater head. 
No gasoline flame, no exhaust gas.5. SiC / Inconel high-temperature exchangerKept. 6.0 needs it even more because three customers 
now wait downstream: Stirling, ATEG, and H2C. Transfer rate is still as important as stored kilowatt-hours.6. High-density multi-zone 
thermal reservoirKept from 5.1 and made explicit as a three-customer store.Zone
Job
6.0 customer
High-T
Stirling hot side
LM-STX
Mid-T ~90–130 °C
leftover work + actuation
ATEG and LM-H2C actuator
Low-T
comfort and reject
cabin heat, pack warmup, H2C heat dumpArchitecture remains SiC structural/porous matrix + graphite spreader + encapsulated high-T
PCM + multilayer insulation. Target usable store: ~300 kWh thermal. PCM chemistry stays unfixed until the real Stirling hot-side
temperature is chosen.7. LM-STX 6.0 custom StirlingKept as the defining engine. Sealed helium, free-piston, SiC/Inconel 
heater head, expansion and compression spaces, multi-zone regenerator, cold-side exchanger, linear alternator, 
electromagnetic control, cascade outlet.“Free-piston” still means no combustion crank train, not “no piston.” 
Sun heats the hot side; helium expands; the piston moves the alternator; electricity hits the DC bus.Continuous
electrical target remains 35–45 kW under favorable conditions. Mid-to-high-40% thermal-to-electric stays a 
research target, not a measured value.6.0 change: the cold-side exchanger is plumbed so EL-60 can send a
slice of cold-side heat to the H2C actuator instead of only to ATEG or the radiator. The Stirling is 
never starved to make cabin air.8. Multi-zone regeneratorKept and still temperature-staged. Internal
heat is recycled inside the cycle before anything is offered to ATEG or H2C. That order matters. 
H2C must not rob the regenerator.9. ATEG cascadeKept from 5.0 / 5.1. Seebeck modules take residual 
gradient after the Stirling and make extra DC. System-level target remains 5–8% of an appropriate 
residual stream, ambitious, not guaranteed. EL-60 bypasses ATEG when pumping and thermal-resistance 
losses beat the watts.6.0 rule: if the vehicle needs cold more than it needs those extra watts, 
mid-T heat is handed to H2C. Heat cannot do both jobs at full strength on the same stream.10. 
LM-H2C — the new core stageThis is the rebuilt LM-TCC refrigeration block, no longer a blank 
labeled “absorption or TE cooler.”What it is. A heat-actuated elastocaloric stack. Mid-T heat 
strokes TiNi actuator films. Those films load TiNiFe refrigerant films. Unloading produces cold 
at the electronics plate, pack edge loop, or a later cabin heat exchanger.What it is sized for in 6.0.Duty
Target class
Why
Inverters, EL-60, cabin electronics
50–200 W cold
matches KIT’s stated auto use; 2–4 K lift can help a hot-spot
Pack edge / tab cooling
200–500 W assist
only if a regenerative stack raises span
Cabin air
assist, not plant
cabin still needs 3–9 kW and ~15–25 K lift
Stirling cold-side assist
research option
only if extra Stirling watts beat the extra reject loadMass sketch if published specific power survived scaling: ~3.3 W/g on 
external heat implies on the order of 30–60 g of refrigerant film for 100–200 W. The hard problems are temperature span, heat 
exchangers, and tensile-film fatigue at vehicle hours, not the grams.What it rejects. Actuator waste heat plus lifted heat. 
That reject stream is a new low-T customer for cabin heat, pack warmup, or the radiator.11. 90 kWh batteryKept from 5.1 as 
the electrical shock absorber. It is not the only fuel tank. It covers acceleration, hills, Stirling lulls, and regen. 6.0 
also uses it less for compressor cooling when H2C is running, which is the only honest range mechanism H2C has.12. HV DC
bus and four motorsKept. Four motors for torque vectoring and regen; two-motor fallback if mass or cost wins. Motors 
still become generators when the vehicle slows. Thermal energy does not have to pass through the battery before it
can push the wheels. H2C never sits on this bus except as a tiny valve/fan load.13. Regenerative brakingKept.
EL-60 still lowers SOC before predicted descents. Hot-weather H2C load is treated as a planned electrical saving, 
not as an excuse to carry a smaller pack.14. Cabin and pack loopsRebuilt as bidirectional.Winter / cold pack: 
mid-T and low-T heat go to cabin and battery. H2C is off.
Summer / hot pack: mid-T heat goes to H2C. Cold goes to electronics first, pack second, cabin third.
Saturated everything: radiator.This is the 5.1 Zero-Radiator idea with a real cold sink added. Zero radiator still cannot last forever.15.
Final radiatorKept as last sink. 5.1 targets for active powertrain/radiator rejection stay the baseline: about 1–3 kW at 30 mph, 2–5 kW 
at 45, 4–9 kW at 65, depending on how much heat cabin, pack, ATEG, PCM, and now H2C can absorb. H2C can lower electrical HVAC draw and
can also increase heat that must be dumped, because it moves heat from the cabin/pack onto the reject stream. EL-60 only runs it
when the electrical saving is worth that extra dump.16. EL-60 energy computerEL-40 / EL-50+ rebuilt with one new state variable: 
cold demand.Still four movements:Divergence — list solar, store, Stirling, battery, regen, ATEG, H2C, route, weather.
Resonance — pick the cheapest legal mix. New question: is 1 W of cold worth more than 1 W from ATEG on this stream?
Phase-locking — sync Stirling output, inverter demand, H2C cycle rate, and battery SOC.
Convergence — sit in the lowest-loss legal configuration.Hard locks:Never cool the high-T store to feed H2C.
Never block regen room in the battery to chase a comfort nicety.
If the cabin needs heat, H2C is off.The older “Memory Phase Crystals / photonic-excitonic core” language from the EL-40 memo is
treated as research flavor, not as required silicon. EL-60 is specified here as a predictive multi-domain controller. 
Implementation can be ordinary automotive compute until a custom stack exists.Parts catalogID
Part
Inherited from
6.0 reconstruction
P01
Adaptive photonic skin
4.0 / 5.1
PV + thermal + guides; also a low-T reject surface
P02
Deployable canopy ~130 m²
3.0–5.1
parked thermal recharge; optional mid-T pre-cool charge
P03
Adaptive concentrator
5.1
defocus on overheat; propulsion heat prioritized
P04
SiC receiver
4.0 / 5.1
combustion-free furnace
P05
SiC/Inconel HT exchanger
4.0 / 5.1
feeds store and Stirling
P06
SiC + graphite + PCM store ~300 kWh-th
5.1
three zones; mid-T reserved for ATEG/H2C
P07
Multilayer HT insulation
5.1
keeps store out of the cabin
P08
LM-STX 6.0 He free-piston
4.0 / 5.1
35–45 kW_e target; cascade tap on cold side
P09
Multi-zone regenerator
4.0 / 5.1
internal recycle before bottoming stages
P10
Cold-side exchanger
4.0 / 5.0
split to ATEG, H2C, cabin, radiator
P11
Linear alternator
4.0 / 5.1
heat → motion → DC bus
P12
ATEG / high-ZT TEG
5.0 / 5.1
5–8% residual-stream target
P13
LM-H2C TiNi / TiNiFe stack
new / KIT 2026
heat-actuated cold; electronics first
P14
H2C cold plates / loops
new
inverters, EL-60, pack edges, later cabin coil
P15
90 kWh usable battery
5.1
peaks, regen, HVAC backup
P16
HV DC bus + inverters
4.0 / 5.1
common electrical highway
P17
Four traction motors
4.0 / 5.1
drive + regen; 2-motor option
P18
Magnetic torque option
3.0
retained only if a mechanical Stirling shaft is used; 6.0 default is electric-only wheels
P19
Cabin HX
4.0 TCC / 5.1
heat or H2C-assisted cool
P20
Pack conditioning loop
5.1
warmup from cascade or cool from H2C
P21
Final radiator
all versions
last sink
P22
EL-60 computer
EL-40 / EL-50+
adds cold-demand and H2C valves
P23
Platform envelope
3.0
~8.2 × 2.6 m expedition packaging seed3.0’s magnetic coupler stays optional. 5.1 already moved propulsion to “Stirling makes electricity, 
motors turn wheels.” 6.0 keeps that as default so H2C, ATEG, PV, and regen all share one bus.Performance canvasAll figures are conceptual 
targets inherited from 5.1 unless marked as an H2C effect.Stored energyStore
5.1
6.0
Battery usable
~90 kWh
same
Thermal usable
~300 kWh-th
same, but mid-T slice is now a cooling fuel
Electrical-equivalent from 300 kWh-th at 45%
~135 kWh before downstream loss
same, if that efficiency is ever shown
ATEG
5–8% of residual stream
same, or less when H2C takes the stream
On-move solar
skin limited by area
same
Parked solar
~104 kW incident on 130 m² at 800 W/m²
sameRange envelope (unchanged central targets)These are still 5.1 upper-end concept numbers, not EPA figures.Speed
Concept range
Central target
30 mph
800–1,000 mi
~900
45 mph
550–700 mi
~625
65 mph
300–400 mi
~350H2C does not raise those numbers. It can protect them on a hot day by cutting compressor watts. A 300–500 W electrical HVAC
saving at 30 mph is a real but small range effect. It is not a new hundred-mile band.Heat exhaust (still not “zero”)Speed
5.1 active radiator target
6.0 comment
30 mph
~1–3 kW
H2C may use some of this as actuator heat, then dump actuator+lifted heat later
45 mph
~2–5 kW
same
65 mph
~4–9 kW
aero still dominates; H2C is comfort/electronicsCooling performance — honest splitLoad
Typical need
6.0 H2C stance
Electronics
tens–hundreds of W
primary design case
Pack
~0.5–5 kW depending on weather and load
assist after span is improved
Cabin
~3–9 kW, large temperature lift
not replaced by the published 2.2 K device
Lab H2C
2.79 mW, 2.2 K on waste heat
existence proof onlyWhat got better vs 5.1The cascade now has a named cold machine instead of a missing sentence.
Mid-T heat has a summer job other than ATEG or the radiator.
Electronics can be cooled without a compressor loop.
EL-60 can trade ATEG watts against avoided HVAC watts on purpose.
Parked canopy energy can pre-cool the vehicle thermally.What did not get betterStirling watts, store size, battery size, canopy area, 
and range targets are not increased.
Radiator can still be required indefinitely in hot, saturated conditions.
H2C adds mass, valves, cycling fatigue, and another heat exchanger.
5.0’s stronger “cabin AC from waste heat” claim is reduced to an assist, which is the physically honest direction.Is 6.0 worth writing
into the repo?Yes — as a new file, not as a silent edit of 5.1.md.Suggested drop-in name:6.0.md
plus
LM-H2C 6.0 — Heat-Driven Elastocaloric Cascade.mdLeave Heat-waste-cooling-Recycle-V1.5.md, the LM-TCC files, 5.0.md, 
and 5.1.md as history. 6.0 is the reconstruction that finally gives LM-TCC a mechanism.The next real page is not more architecture. 
It is an energy-balance sheet:mid-T heat available after Stirling + ATEG at 30 / 45 / 65 mph  
cold demand of inverters / pack / cabin  
H2C heat-in per watt-cold using the 2.2 K waste-heat case  
extra reject heat  
film or tube mass and cycle life

