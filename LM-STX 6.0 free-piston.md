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
A conventional electric car stores energy as chemical potential in a battery. A conventional solar car adds photovoltaic panels and hopes a few square meters of roof can feed that battery. Physics is unkind to that hope. Midday sun is about 1,000 W/m21{,}000\,\mathrm{W/m^2}1{,}000\,\mathrm{W/m^2}
. A car roof is small. Highway drag is not. You cannot collect highway power from a sedan lid.Lumens starts one step earlier in the energy chain. Photons are concentrated onto a high-temperature receiver. Heat is stored in a dense thermal reservoir. A Stirling engine — an external-heat machine with no combustion inside it — spends the highest-value heat on motion or electricity. A smaller battery remains, but it is a shock absorber: acceleration, hills, clouds, regen. The “fuel tank” is supposed to be heat.The sentence the project has been rewriting since Version 1 is:Sun → heat + a little electricity → storage → propulsion → recovery → (in 6.0) cold → propulsion again.Heat does continuous work. Electricity handles transients. Cold, after 6.0, is supposed to be made from heat that already failed to make more work. Only then may leftover heat reach a radiator.That is the whole thesis. Every version is an argument about where to put the next conversion.How the idea grew: Version 1 to 6.0Version 1 — photon to piston to wheelThe first files define a photonic thermal-mechanical automobile, not a battery car with panels. Path: sunlight → optics → thermal receiver → Stirling-type engine → crank and magnetic torque → wheels. Integrated optical skin of a few square meters on the body; a large deployable canopy (about (100)–150 m2150\,\mathrm{m^2}150\,\mathrm{m^2}
) for parked charging; silicon-carbide-class receiver; high-temperature storage on the order of 100 kWh100\,\mathrm{kWh}100\,\mathrm{kWh}
; helium Stirling; regenerator; a small electronics battery. Range sketches were modest: roughly (180)–(210) miles at 30 mph30\,\mathrm{mph}30\,\mathrm{mph}
 from a 100 kWh100\,\mathrm{kWh}100\,\mathrm{kWh}
 thermal store at a raw 30%30\%30\%
 conversion assumption. The point was not the number. The point was that thermal storage plus concentration might beat a roof of PV. 

raw.githubusercontent.com

Kept into 6.0: sunlight as primary source, concentrating optics, SiC-class receiver, helium Stirling, regenerator, canopy, thermal “tank,” energy-management computer.Version 1.5 — rejected heat is a resourceHeat-waste-cooling-Recycle-V1.5.md adds the second principle. Useful leftover heat should be recovered, stored again at lower temperature, used, and only then dumped. This is the ancestor of every later cascade. 6.0 still lives inside that sentence. The missing hardware was how leftover heat becomes cold without a compressor.Version 2.0 — a parallel electric pathThe 2.0 hybrid files admit what Version 1 could not politely say: a heat engine is slow to change its mind. Instant torque, regenerative braking, and electronics want electricity. 2.0 keeps the thermal trunk and adds motors, a modest battery, and regen. From here on Lumens is dual-path: heat for endurance, electricity for edges.Kept into 6.0: battery buffer, motors that also generate, shared electrical highway.Version 3.0 / 3.1 — expedition packaging and a blender3.0 sizes the car so the optics and the store can exist: about 8.2 m8.2\,\mathrm{m}8.2\,\mathrm{m}
 long by 2.6 m2.6\,\mathrm{m}2.6\,\mathrm{m}
 wide. Canopy becomes a variable-geometry collector (full spread, cruise wing, stowed teardrop). PCM store is treated as structure, not a brick in the trunk. A magnetic torque coupler blends Stirling shaft torque with electric motor torque on one mechanical line. Battery is still small ((28)–35 kWh35\,\mathrm{kWh}35\,\mathrm{kWh}
). Full-system range sketches rise into the hundreds of miles if sun, store, and cascade all cooperate. EL-40 appears as the hybrid energy manager: Divergence, Resonance, Phase-Lock, Convergence. 

raw.githubusercontent.com

Kept into 6.0: expedition envelope as a packaging seed, large canopy, multi-zone thermal thinking, EL four-movement logic.
Softened later: magnetic shaft blending is optional. 5.1 and 6.0 prefer Stirling → electricity → motors so every converter shares one bus.Version 4.0 — the engine gets a nameLM-STX 4.0 is the custom sealed-helium free-piston Stirling rebuilt for this vehicle: SiC/Inconel heater head, expansion and compression spaces, multi-zone regenerator, cold-side exchanger, linear alternator. “Free-piston” means no combustion crank train, not “no piston.” LM-TCC is added as a heat-recovery and cooling cascade after the engine — still a block that might be absorption or thermoelectric, not yet a named solid-state machine. Photonic skin, canopy, receiver, exchanger all harden into named parts.Kept into 6.0: almost the entire 4.0 machine list. LM-STX is still the defining engine.Version 5.0 — bottoming recovery and “zero-radiator” as a mode5.0 keeps 4.0 and adds a more serious bottoming stage: thermoelectric generators on residual heat, multi-stage cascade, predictive routing that tries to use cabin, pack, and PCM as sinks so the radiator can sleep. The claim is architectural: under cruise, Lumens should reject less heat than a typical EV’s electronics-and-pack loop. The stronger “cabin AC from waste heat” language lives here. Physics later forces 6.0 to walk that language back to an assist.Version 5.1 — long-range thermal-electric5.1 is the last complete vehicle file in the repo before 6.0. Battery grows to ∼90 kWh\sim 90\,\mathrm{kWh}\sim 90\,\mathrm{kWh}
 usable. Thermal store grows to ∼300 kWh\sim 300\,\mathrm{kWh}\sim 300\,\mathrm{kWh}
 thermal, three zones, SiC + graphite + PCM + multilayer insulation. LM-STX target ∼35\sim 35\sim 35
–45 kWe45\,\mathrm{kW_e}45\,\mathrm{kW_e}
. ATEG targets (5)–8%8\%8\%
 of an appropriate residual stream. Skin becomes adaptive solar-thermal (PV + thermal + guides). EL-50+ inherits EL-40’s four movements. Propulsion default becomes electric wheels. Central range targets, still conceptual: ∼900\sim 900\sim 900
 mi at 30 mph30\,\mathrm{mph}30\,\mathrm{mph}
, ∼625\sim 625\sim 625
 at (45), ∼350\sim 350\sim 350
 at (65). Zero-radiator remains a mode, not a law of nature. 

raw.githubusercontent.com

The hole: 5.1 can turn leftover heat into watts (ATEG) or warmth (cabin/pack). It cannot turn leftover heat into cold without spending battery current on a compressor. That is the sentence 6.0 exists to finish.Version 6.0 — heat becomes strain, strain becomes cold6.0 does not enlarge the store, the pack, the canopy, or the paper range. It rebuilds every inherited block so mid-grade heat can actuate a real cooler: the KIT / University of Tsukuba heat-driven elastocaloric device. Two ultrathin nickel-titanium films. One turns ∼86\sim 86\sim 86
–130∘C130^\circ\mathrm{C}130^\circ\mathrm{C}
 heat into pull. The other uses that pull to drop temperature. No electric compressor in the actuation path. Lab proof is small: 2.79 mW2.79\,\mathrm{mW}2.79\,\mathrm{mW}
 and 2.2 K2.2\,\mathrm{K}2.2\,\mathrm{K}
 lift on waste heat. 6.0 treats that as existence of a mechanism, not as cabin air-conditioning. 

kit.edu

One-line verdict from the 6.0 write-up: it is an upgrade if “upgrade” means the car finally uses heat for cooling. It is not an upgrade if “upgrade” means the 900/625/350900/625/350900/625/350
 mile targets get larger on paper.How 6.0 is supposed to runPrimary loop
Sun → adaptive optics → SiC receiver → 300 kWh300\,\mathrm{kWh}300\,\mathrm{kWh}
 multi-zone store → LM-STX 6.0 → linear alternator → HV DC bus → inverters → motors → wheels.Parallel loops  Sun → PV fraction of the skin → DC bus / 90 kWh90\,\mathrm{kWh}90\,\mathrm{kWh}
 battery  
Wheels → motors as generators → battery  
Residual heat → ATEG → extra watts  
Residual (90)–130∘C130^\circ\mathrm{C}130^\circ\mathrm{C}
 heat → LM-H2C → cold to electronics, pack edges, later cabin assist  
Last heat → radiator

Philosophy
Heat works first. Electricity covers spikes. Cold is manufactured from heat that already lost the chance to make more work. EL-60 decides the mix, including a new question: is one watt of cold worth more than one watt from ATEG on this stream?Default propulsion is electrical. The floor drive shaft you asked to see is the older 3.0 magnetic/mechanical option, retained only if someone insists on a shaft. 6.0’s own text prefers one bus so Stirling, PV, ATEG, regen, and H2C valves all meet in the same electrical highway.Every 6.0 part, and why the vehicle needs itThese are the catalog objects. Each is either inherited and re-plumbed for H2C, or new.P01 — Adaptive photonic / solar-thermal skin
From 4.0 / 5.1. The body is structure, aero surface, and collector at once: PV cells, thermal patches, light guides, protected concentrators. On the move it is a range extender, not the highway engine. 6.0 adds a second job: when cabin and pack are already satisfied, the skin can dump low-grade heat into the H2C reject path. The shell is no longer only an input.P02 — Deployable canopy ∼130 m2\sim 130\,\mathrm{m^2}\sim 130\,\mathrm{m^2}

From 3.0–5.1. Parked or slow, this is the real charger. At 800 W/m2800\,\mathrm{W/m^2}800\,\mathrm{W/m^2}
 it sees about 104 kW104\,\mathrm{kW}104\,\mathrm{kW}
 incident before losses. 6.0 can reserve a mid-temperature slice of that charge to pre-cool electronics and the pack through H2C instead of draining the battery to pre-cool.P03 — Adaptive concentrator
From 5.1. EL-60 opens concentration when the high-T store is hungry and defocuses at the receiver limit. New 6.0 rule: do not overfill the mid-T zone just to run the cooler if the high-T zone needs heat. Propulsion heat outranks cooling heat.P04 — SiC photonic receiver
From 4.0 / 5.1. Concentrated light hits silicon carbide. No flame, no exhaust gas. This is the furnace. Without it there is no high-grade heat and therefore no Stirling.P05 — SiC / Inconel high-temperature exchanger
From 4.0 / 5.1. Moves heat from receiver into store and Stirling heater head. 6.0 needs it more, because three customers now wait: Stirling, ATEG, H2C. Transfer rate is as important as stored kilowatt-hours.P06 — Multi-zone thermal reservoir ∼300 kWh\sim 300\,\mathrm{kWh}\sim 300\,\mathrm{kWh}
 usable
From 5.1, made explicit as a three-customer store.  High-T → LM-STX hot side  
Mid-T ∼90\sim 90\sim 90
–130∘C130^\circ\mathrm{C}130^\circ\mathrm{C}
 → ATEG and the H2C actuator  
Low-T → cabin heat, pack warmup, H2C dump

Architecture: SiC matrix + graphite spreader + encapsulated high-T PCM + multilayer insulation. PCM chemistry waits for a real Stirling hot-side temperature. This is the main tank. The 90 kWh90\,\mathrm{kWh}90\,\mathrm{kWh}
 battery is not.P07 — Multilayer high-T insulation
Keeps a several-hundred-degree store from becoming the cabin.P08 — LM-STX 6.0 helium free-piston Stirling
Defining engine since 4.0. Sealed helium, SiC/Inconel heater head, expansion and compression spaces, multi-zone regenerator, cold-side exchanger, linear alternator, electromagnetic control. Sun heats the hot side; helium expands; the power piston oscillates; the alternator writes DC onto the bus. Target: (35)–45 kW45\,\mathrm{kW}45\,\mathrm{kW}
 electrical under favorable conditions. Mid-to-high-40%40\%40\%
 thermal-to-electric is a research target, not a measurement. 6.0 change: the cold-side exchanger can send a slice of leftover heat to the H2C actuator. The Stirling is never starved to make cabin air.P09 — Multi-zone regenerator
Internal recycle inside the Stirling cycle. Heat is reused before anything is offered to ATEG or H2C. That order is load-bearing. H2C must not rob the regenerator.P10 — Cold-side exchanger
Helium stays sealed. Liquid jackets pull heat off the cold end. That stream splits to ATEG, H2C, cabin, or radiator.P11 — Linear alternator
Heat → piston motion → electricity. This is why thermal energy can push the wheels without first becoming battery charge.P12 — ATEG
From 5.0 / 5.1. Seebeck modules on residual gradient. Target (5)–8%8\%8\%
 of an appropriate leftover stream. EL-60 bypasses it when losses beat the watts. 6.0 rule: heat on one stream cannot do ATEG and H2C at full strength. Cold can win the argument.P13 / P14 — LM-H2C and its cold plates
The only truly new core stage. Rebuilt LM-TCC, no longer “absorption or TE cooler.” Mid-T heat strokes ∼22 μm\sim 22\,\mu\mathrm{m}\sim 22\,\mu\mathrm{m}
 one-way shape-memory TiNi. That pull loads ∼26.5 μm\sim 26.5\,\mu\mathrm{m}\sim 26.5\,\mu\mathrm{m}
 superelastic TiNiFe. Unloading drops temperature. Coupling transfers force, not heat. Cycle about 0.83 Hz0.83\,\mathrm{Hz}0.83\,\mathrm{Hz}
.Sized honestly:  Electronics / EL-60 / inverters: (50)–200 W200\,\mathrm{W}200\,\mathrm{W}
 cold — the KIT automotive-electronics use case  
Pack edges: (200)–500 W500\,\mathrm{W}500\,\mathrm{W}
 assist if span improves  
Cabin: assist, not plant. Cabin still wants (3)–9 kW9\,\mathrm{kW}9\,\mathrm{kW}
 and (15)–25 K25\,\mathrm{K}25\,\mathrm{K}
 lift  
Lab device: 2.79 mW2.79\,\mathrm{mW}2.79\,\mathrm{mW}
, 2.2 K2.2\,\mathrm{K}2.2\,\mathrm{K}
 on waste heat — proof of mechanism only

It is still a heat pump. Actuator waste plus lifted heat must be rejected. 6.0 does not repeal the second law. It relocates cold production onto a stream 5.1 was already carrying.P15 — 90 kWh90\,\mathrm{kWh}90\,\mathrm{kWh}
 battery
From 5.1. Peaks, hills, Stirling lulls, regen, HVAC backup. The only honest range mechanism H2C has is using this pack less for compressor cooling on a hot day. That is a real but small effect, not a new hundred-mile band.P16 / P17 — HV DC bus, inverters, four motors
Common electrical highway. Four motors for torque vectoring and regen; two-motor fallback if mass wins. Motors become generators when the car slows. H2C sits on this bus only as valve and fan load.P18 — Magnetic torque / floor shaft
From 3.0. Optional. 6.0 default is electric-only wheels.P19 / P20 — Cabin and pack loops
Bidirectional. Winter: mid-T and low-T heat to cabin and battery; H2C off. Summer: mid-T to H2C; cold to electronics first, pack second, cabin third. Saturated: radiator. This is 5.1’s zero-radiator idea with a real cold sink added. Zero radiator still cannot last forever.P21 — Final radiator
Last sink. Inherited reject targets stay the baseline: about (1)–3 kW3\,\mathrm{kW}3\,\mathrm{kW}
 at 30 mph30\,\mathrm{mph}30\,\mathrm{mph}
, (2)–(5) at (45), (4)–(9) at (65), depending how much heat cabin, pack, ATEG, PCM, and now H2C absorb. H2C can cut electrical HVAC draw and can also increase dump heat, because it moves cabin/pack heat onto the reject stream.P22 — EL-60
EL-40 / EL-50+ plus one state variable: cold demand.  Divergence: list sun, store, Stirling, battery, regen, ATEG, H2C, route, weather  
Resonance: cheapest legal mix  
Phase-lock: sync Stirling, inverters, H2C cycle rate, SOC  
Convergence: sit in the lowest-loss legal state

Hard locks: never cool the high-T store to feed H2C; never block regen room for comfort; if the cabin needs heat, H2C is off. Implementation can be ordinary automotive compute. Older “memory phase crystal” language is flavor, not required silicon.P23 — Platform seed
From 3.0: ∼8.2×2.6 m\sim 8.2 \times 2.6\,\mathrm{m}\sim 8.2 \times 2.6\,\mathrm{m}
 so canopy, store, and cascade fit. The sports-GT images used for visualization are a tighter body. The catalog packaging is still the expedition envelope.Cooling, said cleanlyOlder cars spend electricity to pump heat out of cabin and pack. Lumens already spends heat to make electricity. 6.0 inserts a third conversion between those facts.Concentrated sun charges the high-T store.  
LM-STX spends the best heat on watts.  
ATEG skims a little more from the leftover gradient.  
LM-H2C uses the (90)–130∘C130^\circ\mathrm{C}130^\circ\mathrm{C}
 band as an actuator for solid-state cold.  
Only heat with no remaining job hits the radiator.

That is why every inherited part was rebuilt: skin, canopy, receiver, reservoir, Stirling cold side, ATEG priority, battery duty, motors, and the computer all have to accept a cold-demand term. Without that plumbing, the KIT film pair is a lab curiosity on the bench, not a vehicle stage.Anticipated performance — and what it is notAll figures are 5.1 targets unless marked as an H2C effect.Store
Role
6.0
Battery
buffer, peaks, regen
∼90 kWh\sim 90\,\mathrm{kWh}\sim 90\,\mathrm{kWh}
 usable
Thermal
main tank; mid-T slice is now also cooling fuel
∼300 kWhth\sim 300\,\mathrm{kWh_{th}}\sim 300\,\mathrm{kWh_{th}}

Electrical-equivalent of 300 kWhth300\,\mathrm{kWh_{th}}300\,\mathrm{kWh_{th}}
 at 45%45\%45\%

if that efficiency is ever shown
∼135 kWh\sim 135\,\mathrm{kWh}\sim 135\,\mathrm{kWh}
 before downstream loss
Parked canopy
incident at 800 W/m2800\,\mathrm{W/m^2}800\,\mathrm{W/m^2}
 on 130 m2130\,\mathrm{m^2}130\,\mathrm{m^2}

∼104 kW\sim 104\,\mathrm{kW}\sim 104\,\mathrm{kW}
 before losses

Central range targets, unchanged by H2C:Speed
Central concept target
30 mph30\,\mathrm{mph}30\,\mathrm{mph}

∼900\sim 900\sim 900
 mi
45 mph45\,\mathrm{mph}45\,\mathrm{mph}

∼625\sim 625\sim 625
 mi
65 mph65\,\mathrm{mph}65\,\mathrm{mph}

∼350\sim 350\sim 350
 mi

H2C does not raise those bands. It can protect them on a hot day by cutting compressor watts. A few hundred watts of HVAC saving at 30 mph30\,\mathrm{mph}30\,\mathrm{mph}
 is small and real. It is not a new range class.What got better versus 5.1: a named cold machine; a summer job for mid-T heat besides ATEG or the radiator; electronics cooled without a compressor loop; EL-60 can trade ATEG watts against avoided HVAC watts; parked canopy energy can pre-cool thermally.What did not get better: Stirling watts, store size, battery size, canopy area, paper range. The radiator can still run indefinitely in hot, saturated weather. H2C adds mass, valves, film fatigue, and another exchanger. 5.0’s stronger cabin-AC-from-waste-heat claim is reduced to an assist, which is the physically honest direction.What would have to be true nextThe repository’s own next page is not more architecture. It is an energy-balance sheet:mid-T heat available after Stirling + ATEG at 30/45/65 mph30/45/65\,\mathrm{mph}30/45/65\,\mathrm{mph}
  
cold demand of inverters, pack, and cabin  
H2C heat-in per watt-cold using the 2.2 K2.2\,\mathrm{K}2.2\,\mathrm{K}
 waste-heat case  
extra reject heat  
film or tube mass and cycle life

Until those are measured, 6.0 is a complete argument about how to finish the cascade that Version 1.5 opened: keep every conversion that already earned its place, and finally spend leftover heat on cold before you spend battery current to fight your own waste heat. 


That is the vehicle, part by part, from the first photonic-mechanical sketch to the heat-driven elastocaloric close.
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

===============================================================

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

