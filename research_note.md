# Research Notes

## A Review of 3D Printing Batteries — Mottaghi & Pearce (2024)

### Summary

1. Motivation: Intermittent renewable energy (wind, solar) needs cost-effective storage; high capital costs of batteries are a key barrier, and 3D printing offers a manufacturing path to reduce them.

2. Diff of ideas: Unlike earlier reviews focusing on one technique, this paper covers four mainstream methods (DIW, FFF, IJP, SLA) and explicitly ties them to battery performance metrics — efficiency, mechanical stability, energy/power density, customizability, material conservation, and solid-state batteries.

3. Method: Literature review organized by printing method. Each section covers principles, advantages, limitations, and tabulated electrochemical performance from representative studies.

4. Results: DIW is most versatile and common (1–250 µm resolution, wide material compatibility); FFF enables solid-state all-in-one batteries but suffers from high processing temperatures; IJP gives high resolution but low ink viscosity constraint; SLA enables complex porous geometries but is limited to photocurable resins.

5. Significance: Establishes that 3D printing offers design freedom, reduces weight/waste, and enables solid-state battery integration — providing a roadmap for researchers choosing between methods based on their application.

---

## Electrode Fabrication Techniques for Li Ion Based Energy Storage System — Singh, Kuthe & Skorodumova (2023)

### Summary

1. Motivation: With renewable energy expanding, reliable Li-ion storage is critical; but fabrication technique choice profoundly affects electrode performance and scalability.

2. Diff of ideas: Broadest comparative scope of any paper here — covers both conventional (doctor blade, CVD, electrodeposition, roll-to-roll, pressing) and advanced printing (IJP, FDM, DIW) techniques in one framework, with publication statistics (2003–2022) to quantify research trends.

3. Method: Systematic review across 14 fabrication techniques applied to Li-ion battery electrodes, categorized by operating principle and performance outcomes.

4. Results: Roll-to-roll and doctor blade dominate industry; printing techniques (especially DIW) are growing rapidly in the literature but still lag in areal capacity and scalability. Publication volume on IJP and FDM increased >5× from 2015 to 2022.

5. Significance: Positions 3D printing as a rising complement — not replacement — to conventional methods, especially for complex geometries and prototyping. Identifies standardization of inks as the key remaining bottleneck.

---

## 3D Printing of Electrochemical Energy Storage Devices — Cheng, Deivanayagam & Shahbazian-Yassar (2019)

### Summary

1. Motivation: Conventional EES fabrication methods (sputtering, lithography) impose geometric and cost constraints; 3D printing's freeform capability could unlock higher energy and power densities through architecture control.

2. Diff of ideas: Rather than organizing by printing technique, this review organizes by electrode architecture — interdigitated structures, 3D scaffolds, and fibers — making it the first to frame the 3D printing advantage as fundamentally architectural, not just material.

3. Method: Review of 3D printed EES devices (batteries and supercapacitors) organized by architectural category. Compares electrochemical performance (energy density, power density) across architectures vs. conventional planar designs.

4. Results: Interdigitated and scaffold designs consistently outperform planar designs by increasing active material loading, footprint area, and shortening ion transport paths. Fiber architecture enables wearable/flexible integration. Quantitative improvements in energy density of 10–30× reported for interdigitated designs vs. planar.

5. Significance: The architecture-first framing is influential: it clarifies that printing method choice should be driven by desired architecture, not the other way around.

---

## Evolution of 3D Printing Methods and Materials for Electrochemical Energy Storage — Egorov et al. (2020)

### Summary

1. Motivation: Fixed form factors of commercial batteries/supercapacitors limit integration into IoT, wearables, and complex devices; 3D printing could decouple form factor from electrochemical design.

2. Diff of ideas: Tracks the temporal evolution of the field — starting from extrusion-based methods, moving to photopolymerization — and argues that materials and printing methods must be co-designed, not selected independently.

3. Method: Review of AM methods for Li-ion batteries and supercapacitors at UCC, with critical analysis of material-method compatibility. Covers extrusion, photopolymerization (SLA/DLP), and material jetting (inkjet) with attention to solvent sensitivity.

4. Results: Supercapacitors gravitate toward inkjet (solvent-tolerant); batteries favor extrusion and photopolymerization. Higher-resolution multimaterial printers are identified as the key unmet need. Performance limitations trace directly to printable material purity and fidelity.

5. Significance: The co-design principle — that printable material development cannot be decoupled from printer design — is a conceptual advance over "use existing inks in existing printers." Provides a guide for choosing printing method + material by application.

---

## Additive Manufacturing for Energy Storage: Methods, Designs and Material Selection — Gulzar, Glynn & O'Dwyer (2021)

### Summary

1. Motivation: 3D printed EESDs offer customization and form-factor freedom, but the field lacks a unified framework connecting AM method choice, device design, and material selection.

2. Diff of ideas: Concise opinion piece (7 pages) that synthesizes across ASTM's 7 AM categories, linking each to electrochemical requirements. Unique focus on printable composite materials and their electrochemical stability.

3. Method: Selective literature review and expert synthesis across AM methods as applied to batteries and supercapacitors. Discusses performance requirements driving material printability.

4. Results: Each AM category has distinct material compatibility constraints tied to the underlying physics (e.g., powder bed fusion requires dry powders, incompatible with liquid electrolytes; binder jetting adds dead mass). DIW and inkjet most electrochemically compatible.

5. Significance: Practical decision guide for researchers: given an application (wearable, IoT, EV), which AM method and material combination is feasible? Complements the Egorov2020 co-design principle with actionable guidance.

---

## 3D Printed Functional Nanomaterials for Electrochemical Energy Storage — Zhu et al. (2017)

### Summary

1. Motivation: Engineering nanostructured electrode materials into macroscopic devices with controlled porosity and architecture is the central fabrication challenge for next-generation EES; conventional methods cannot achieve this controllably.

2. Diff of ideas: First comprehensive review to cover all four major 3D printing families (laser-based, lithography-based, electrodeposition-based, extrusion-based) specifically for functional nanomaterial electrode fabrication — distinct from reviews focused on bulk printing.

3. Method: Review of 3D printing techniques applied to nanomaterial electrodes, focusing on how each method controls pore architecture and nanoscale structure in Li-ion batteries and supercapacitors. LLNL + UCSC expertise in graphene aerogel and DIW.

4. Results: Laser (SLM/DMLS) enables metallic current collectors; lithography (PμSL, holographic) enables sub-micron porous structures; electrodeposition builds conformal 3D thin films; extrusion (DIW, inkjet) prints composite active material inks. Each technique has a distinct resolution-throughput-material tradeoff.

5. Significance: Foundational 2017 reference that established the multi-technique landscape for 3D printed EES nanomaterials and defined the "nanoarchitecture" framing that later papers (Reale Batista 2023, Pinilla 2023) build on.

---

## 3D Printed Separator for Thermal Management of High-Performance Li Metal Anodes — Liu et al. (2018)

### Summary

1. Motivation: Li metal anodes suffer from dendrite growth and "hot spots" that cause safety failures; existing separator strategies don't address thermal heterogeneity at the electrode interface.

2. Diff of ideas: First paper to use 3D printing not to fabricate the electrode, but the separator — integrating boron nitride (BN) nanosheets into a PVDF-HFP matrix via extrusion 3D printing to create a thermally managing separator.

3. Method: BN nanosheets dispersed in PVDF-HFP, printed via extrusion into spiral separator patterns. Tested in Li/Cu and Li/Li symmetric cells. Compared against control (bare PVDF-HFP) separators at 1 mA cm⁻².

4. Results: BN-separator achieves 92% Coulombic efficiency after 90 cycles vs. 70% in control after only 30 cycles. Over 500 h stable cycling in symmetric cells with lower voltage polarization. Uniform thermal distribution suppresses dendrite nucleation at hot spots.

5. Significance: Expands the 3D printing application space for batteries from electrodes to separators; demonstrates that thermal management — often ignored in electrode-focused work — is a viable and important design target for printing.

---

## Comparative Study on LiFePO4 Cathodes Fabricated by Low Temperature 3D Printing, DIW and Roller Coating — Liu et al. (2019)

### Summary

1. Motivation: DIW-fabricated LFP electrodes require viscosifiers that dilute active material; a novel low temperature direct writing (LTDW) process may overcome this limitation by freeze-solidifying standard battery slurry inks.

2. Diff of ideas: First head-to-head quantitative comparison of three fabrication methods — LTDW, conventional DIW, and industrial roller coating — using the same LFP ink at varying solid content. No extra rheological additives needed in LTDW.

3. Method: LFP inks at four solid contents (0.244–0.576 g/mL) printed via all three methods. Characterized by mercury porosimetry, SEM, EIS, rate performance, and CV. Shenzhen University Additive Manufacturing Institute.

4. Results: LTDW electrodes outperform DIW and roller coating at high solid content (≥0.467 g/mL), achieving 82 mAh/g @ 10C. Roller coating is superior at low solid content. LTDW produces higher porosity through freeze-drying, benefiting ion transport.

5. Significance: Demonstrates that ink solid content is a critical, underappreciated variable that determines which fabrication method is optimal — challenging the assumption that 3D printing always outperforms conventional coating for battery electrodes.

---

## Novel Rechargeable 3D-Microbatteries on 3D-Printed-Polymer Substrates — Cohen et al. (2018)

### Summary

1. Motivation: IoT, implantable medical devices, and wireless sensor networks need mm-scale microbatteries with high areal energy density — impossible with planar thin-film designs constrained to 2D geometry.

2. Diff of ideas: Uses 3D printing not to print the battery itself, but to print the substrate (a perforated polymer with 3D-interconnected channels), then uses electrophoretic deposition (EPD) to conformally coat all channel surfaces with LFP, LTO, and polymer-in-ceramic electrolyte.

3. Method: FDM-printed perforated polymer substrate (3DPS) with through-channels in XYZ planes. EPD of nanosize LFP cathode, LTO anode, and polymer-in-ceramic electrolyte. Assembled as quasi-solid-state microbattery. Tel Aviv University.

4. Results: 3D microbattery delivers high reversible specific capacity and high pulse-power capability. The 3D substrate-EPD combination enables conformal thin-film coverage of complex geometries — something direct printing of battery materials cannot yet achieve at this scale.

5. Significance: Demonstrates a hybrid approach: use 3D printing for substrate geometry and a separate deposition technique for active material — a pragmatic strategy when printing resolution is insufficient for the active layer itself.

---

## Toward a Remarkable Li-S Battery via 3D Printing — Gao et al. (2019)

### Summary

1. Motivation: Li-S batteries have high theoretical energy density (~2600 Wh/kg) but practical performance is limited by low sulfur loading achievable with conventional blade-casting and poor cycle stability due to polysulfide shuttle.

2. Diff of ideas: Applies robocasting (extrusion-based DIW) to fabricate self-standing, binder-assisted S/carbon black (BP-2000) cathodes with controlled areal loading simply by stacking more layers — a capability impossible with 2D casting.

3. Method: Ink of sulfur/BP-2000, acetylene black, CNTs, and PVDF-HFP in NMP. Robocasting at room temperature. Tested at sulfur loadings of 3 mg/cm² and 5.5 mg/cm². Western Ontario (Sun group).

4. Results: At 5.5 mg/cm² loading: 1009 mAh/g initial, 87% retention after 200 cycles at 1C; 912 mAh/g at 2C. Stable capacity of 564 mAh/g at 3C for 3 mg/cm² samples. Performance attributed to hierarchical porosity from printed structure enabling Li+/e⁻ transport at macro/micro/nano scales.

5. Significance: Demonstrates that 3D printing's layer-controllable thickness is a direct solution to one of Li-S's fundamental problems (insufficient sulfur loading), a strategy applicable to other high-capacity chemistries limited by electrode thickness.

---

## Considering Li-Ion Battery 3D-Printing via Thermoplastic Material Extrusion and Polymer Powder Bed Fusion — Maurel et al. (2021)

### Summary

1. Motivation: Embedding batteries into complex smart structures (aerospace, implants, structural electronics) requires directly printing batteries within the object — not inserting pre-made cells — but thermal constraints of FFF and PBF conflict with battery material requirements.

2. Diff of ideas: First paper to seriously evaluate both ME (FFF) and PBF for LIBs and compare them, using polypropylene/LFP composite electrodes. Includes computational modeling of 3D electrode geometries at high current densities.

3. Method: PP/LFP composite filaments for ME; PP/LFP powders for PBF. Characterized electrochemically, electrically, morphologically, and mechanically. Modeling study compares 2D planar vs. complex 3D architectures. Université de Picardie Jules Verne.

4. Results: Both methods produce functional electrodes but with lower electrochemical performance than DIW-based approaches due to high polymer content reducing ion transport. Modeling confirms 3D architectures theoretically outperform 2D at high current densities. Liquid electrolyte must be infused post-printing.

5. Significance: Realistic assessment of thermoplastic AM methods for LIBs — acknowledging both promise (geometric freedom for structural integration) and limitations (lower conductivity, post-processing needed), which is more nuanced than most earlier optimistic reviews.

---

## 3D Printing for Rechargeable Lithium Metal Batteries — Zhou et al. (2021)

### Summary

1. Motivation: LMBs (Li-S, Li-O2, Li-CO2) offer 35–50% higher energy density than Li-ion batteries but are plagued by Li dendrite growth and infinite volume expansion of the metallic Li anode — problems that 3D printing's geometric precision may address.

2. Diff of ideas: Unlike reviews focused on Li-ion batteries, this paper centers on Li metal batteries (LMBs) specifically, reviewing how 3D printing controls geometry and structure at nano-to-macroscale for each LMB component (anode, cathode, separator, electrolyte).

3. Method: Review of 3D printing applications to LMB components. Organizes by component: cathodes (S, O2, CO2), Li anode structures, separators, solid electrolytes. Central South University.

4. Results: 3D printing of hosts for Li metal anodes (3D carbon frameworks) significantly suppresses dendrite growth by confining Li deposition. 3D printed cathodes for Li-S achieve high sulfur loading. 3D solid electrolytes improve interfacial contact and reduce local current density hotspots.

5. Significance: Establishes 3D printing as a systems-level tool for LMBs — not just for individual components — and identifies suppression of local current density concentration as the mechanistic reason for dendrite mitigation via 3D printed hosts.

---

## Coaxial 3D-Printing Constructing All-in-One Fibrous Li-, Na-, and Zn-Ion Batteries — Ji et al. (2022)

### Summary

1. Motivation: Wearable and flexible electronics need fiber-form batteries; current fiber battery fabrication requires multiple separate steps for anode, cathode, and separator, reducing scalability and increasing fabrication complexity.

2. Diff of ideas: Universal coaxial extrusion printing of all three components (anode ink, cathode ink, separator ink) simultaneously in a single pass — an "all-in-one" fiber architecture — demonstrated across three battery chemistries (LIB, SIB, AZIB).

3. Method: Coaxial nozzle DIW with kg-scale shear-thinning inks. Three battery chemistries tested. Characterized for capacity, rate capability, and cycle stability. Zhengzhou University of Light Industry.

4. Results: LIBs: 60 mAh/g, 33 mAh/g @ 510 mA/g, 1000 cycles. SIBs: 50 mAh/g, 31 mAh/g @ 500 mA/g, 2000 cycles. AZIBs: 121 mAh/g, 68 mAh/g @ 1600 mA/g, stable cycling. Inks scalable to kg quantities.

5. Significance: The coaxial single-pass approach is a manufacturing breakthrough for fiber batteries — comparable to how multi-nozzle printing advanced planar batteries — and demonstrates cross-chemistry universality that most 3D printing battery work lacks.

---

## Design and Additive Manufacturing of Optimized Electrodes for Energy Storage — Reale Batista et al. (2023)

### Summary

1. Motivation: Thick electrodes boost energy density but suffer from transport limitations; topology optimization can theoretically solve this by designing morphologies that maximize both active material volume and ion/electron transport paths.

2. Diff of ideas: First paper to combine formal topology optimization (computationally derived electrode morphologies) with high-resolution PμSL (0.6 µm) 3D printing to fabricate those optimized structures in a supercapacitor context. Earlier work used intuitive lattice/log-pile designs.

3. Method: Topology optimization to generate electrode geometry. PμSL printing of PR48 resin, then pyrolysis to create conductive carbon. Also tested GO/TMPTA resin composites. Compared to cubic lattice control electrodes. LLNL + UCSC + UCLA.

4. Results: Topology-optimized PR48-P electrodes show 99% improvement in capacitance vs. cubic lattice controls. 3 wt% GO/TMPTA electrodes retain more capacitance post-pyrolysis than pure PR48-P. Demonstrates that morphology alone (same material, different architecture) can double performance.

5. Significance: Closes the loop between computational design and AM fabrication for energy storage — a paradigm shift from empirical geometry selection to mathematically optimal electrode architecture.

---

## Additive Manufacturing of Li-Ion Batteries: A Comparative Study between Electrode Fabrication Processes — Pinilla et al. (2023)

### Summary

1. Motivation: 3D-printed Li-ion electrodes often underperform conventionally manufactured ones; the reason — which specific physical parameter is degraded by which printing process — has not been quantitatively identified.

2. Diff of ideas: Rather than reporting capacity numbers, introduces a semi-empirical model linking rate performance to physical electrode parameters (τ, n), enabling systematic identification of the rate-limiting mechanism for each technique. First to apply this diagnostic framework comparatively across 5 methods.

3. Method: Five techniques compared (slurry casting, vacuum filtration, extrusion/DIW, spray coating, aerosol jet printing) using identical LTO/CNT inks at three CNT mass fractions. FIB-SEM microstructure + galvanostatic cycling + chronoamperometry fitted to $Q_M = Q_{M0}(1 - e^{-(\tau R)^{-n}})(\tau R)^{-n}$. Trinity College Dublin.

4. Results: "Wet" techniques (slurry, filtration, extrusion) preserve CNT segregated networks → better conductivity → higher n (resistance-limited, improvable with more CNT). "Dry" techniques (spray, AJP) disrupt networks → n saturates at ~0.7 → improvement ceiling reached earlier. Primary limiting factor in dry-technique electrodes is electronic conductivity.

5. Significance: Provides both a diagnostic tool (fit τ and n to find bottleneck) and a design principle (printing processes must allow sufficient drying time for CNT network formation). Most quantitatively rigorous paper in the collection.

---
