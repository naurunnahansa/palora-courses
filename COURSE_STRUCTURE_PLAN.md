# Palora Course Structure Plan

## Overview

Restructure courses by **exam board** → **subject** with qualification level in the course slug.

---

## Folder Structure

```
palora-courses/
├── aqa/
│   ├── gcse-physics/
│   ├── gcse-chemistry/
│   ├── gcse-biology/
│   └── gcse-maths/
│
├── edexcel/
│   ├── gcse-physics/
│   ├── gcse-chemistry/
│   ├── gcse-biology/
│   ├── gcse-maths/
│   ├── igcse-physics/
│   ├── igcse-chemistry/
│   ├── igcse-biology/
│   └── igcse-maths/
│
└── cambridge/
    ├── igcse-physics/
    ├── igcse-chemistry/
    ├── igcse-biology/
    └── igcse-maths/
```

**Total: 16 courses** (4 AQA + 8 Edexcel + 4 Cambridge)

---

## Course Internal Structure

Each course follows this pattern:

```
{exam-board}/{qualification}-{subject}/
├── _course.json              # Course metadata
└── content/
    └── {NN}-{unit-slug}/
        ├── _unit.json        # Unit metadata
        └── {NN}-{topic}.json # Topic content pages
```

---

## Detailed Syllabus Breakdown by Exam Board

---

# AQA GCSE Courses

## AQA GCSE Physics (8463)

```
aqa/gcse-physics/content/
├── 01-energy/
│   ├── 01-energy-stores-and-systems.json
│   ├── 02-kinetic-energy.json
│   ├── 03-gravitational-potential-energy.json
│   ├── 04-elastic-potential-energy.json
│   ├── 05-specific-heat-capacity.json
│   ├── 06-power.json
│   ├── 07-energy-transfers-in-systems.json
│   ├── 08-efficiency.json
│   └── 09-national-and-global-energy-resources.json
│
├── 02-electricity/
│   ├── 01-circuit-symbols-and-diagrams.json
│   ├── 02-current-and-charge.json
│   ├── 03-potential-difference-and-resistance.json
│   ├── 04-component-characteristics.json
│   ├── 05-series-and-parallel-circuits.json
│   ├── 06-domestic-uses-of-electricity.json
│   ├── 07-electrical-power.json
│   ├── 08-energy-transfers-in-circuits.json
│   └── 09-static-electricity.json
│
├── 03-particle-model/
│   ├── 01-density.json
│   ├── 02-states-of-matter.json
│   ├── 03-changes-of-state.json
│   ├── 04-internal-energy.json
│   ├── 05-specific-latent-heat.json
│   └── 06-gas-pressure-and-temperature.json
│
├── 04-atomic-structure/
│   ├── 01-atoms-and-isotopes.json
│   ├── 02-atoms-and-nuclear-radiation.json
│   ├── 03-activity-and-half-life.json
│   ├── 04-nuclear-fission-and-fusion.json
│   └── 05-hazards-of-radioactivity.json
│
├── 05-forces/
│   ├── 01-scalar-and-vector-quantities.json
│   ├── 02-contact-and-non-contact-forces.json
│   ├── 03-gravity-and-weight.json
│   ├── 04-resultant-forces.json
│   ├── 05-work-done.json
│   ├── 06-forces-and-elasticity.json
│   ├── 07-distance-displacement-speed-velocity.json
│   ├── 08-acceleration.json
│   ├── 09-distance-time-graphs.json
│   ├── 10-velocity-time-graphs.json
│   ├── 11-newtons-laws.json
│   ├── 12-stopping-distances.json
│   ├── 13-momentum.json
│   └── 14-moments-levers-gears.json
│
├── 06-waves/
│   ├── 01-wave-properties.json
│   ├── 02-transverse-and-longitudinal-waves.json
│   ├── 03-reflection-and-refraction.json
│   ├── 04-sound-waves.json
│   ├── 05-ultrasound-and-seismic-waves.json
│   ├── 06-electromagnetic-spectrum.json
│   ├── 07-uses-of-em-waves.json
│   ├── 08-lenses.json
│   ├── 09-visible-light.json
│   └── 10-black-body-radiation.json
│
├── 07-magnetism/
│   ├── 01-permanent-and-induced-magnets.json
│   ├── 02-magnetic-fields.json
│   ├── 03-electromagnets.json
│   ├── 04-motor-effect.json
│   ├── 05-electric-motors.json
│   ├── 06-generator-effect.json
│   └── 07-transformers.json
│
└── 08-space-physics/          # Triple Science Only
    ├── 01-solar-system.json
    ├── 02-life-cycle-of-stars.json
    ├── 03-orbits.json
    └── 04-red-shift-and-big-bang.json
```

---

## AQA GCSE Chemistry (8462)

```
aqa/gcse-chemistry/content/
├── 01-atomic-structure/
│   ├── 01-atoms-elements-compounds.json
│   ├── 02-mixtures.json
│   ├── 03-atomic-structure.json
│   ├── 04-electronic-structure.json
│   └── 05-periodic-table-development.json
│
├── 02-bonding-and-structure/
│   ├── 01-chemical-bonds.json
│   ├── 02-ionic-bonding.json
│   ├── 03-ionic-compounds.json
│   ├── 04-covalent-bonding.json
│   ├── 05-metallic-bonding.json
│   ├── 06-states-of-matter.json
│   ├── 07-giant-structures.json
│   ├── 08-polymers.json
│   ├── 09-fullerenes-and-graphene.json
│   └── 10-nanoparticles.json
│
├── 03-quantitative-chemistry/
│   ├── 01-conservation-of-mass.json
│   ├── 02-relative-formula-mass.json
│   ├── 03-moles.json
│   ├── 04-limiting-reactants.json
│   ├── 05-concentration-of-solutions.json
│   └── 06-percentage-yield-and-atom-economy.json
│
├── 04-chemical-changes/
│   ├── 01-reactivity-of-metals.json
│   ├── 02-extraction-of-metals.json
│   ├── 03-oxidation-and-reduction.json
│   ├── 04-acids-and-bases.json
│   ├── 05-neutralisation.json
│   ├── 06-making-salts.json
│   └── 07-electrolysis.json
│
├── 05-energy-changes/
│   ├── 01-exothermic-and-endothermic.json
│   ├── 02-reaction-profiles.json
│   ├── 03-bond-energies.json
│   └── 04-chemical-cells-and-fuel-cells.json
│
├── 06-rate-and-equilibrium/
│   ├── 01-calculating-rates.json
│   ├── 02-factors-affecting-rate.json
│   ├── 03-collision-theory.json
│   ├── 04-catalysts.json
│   └── 05-reversible-reactions-and-equilibrium.json
│
├── 07-organic-chemistry/
│   ├── 01-crude-oil-and-hydrocarbons.json
│   ├── 02-fractional-distillation.json
│   ├── 03-alkanes.json
│   ├── 04-combustion.json
│   ├── 05-cracking.json
│   ├── 06-alkenes.json
│   ├── 07-alcohols.json
│   ├── 08-carboxylic-acids.json
│   ├── 09-addition-polymerisation.json
│   └── 10-condensation-polymerisation.json
│
├── 08-chemical-analysis/
│   ├── 01-purity-and-formulations.json
│   ├── 02-chromatography.json
│   ├── 03-test-for-gases.json
│   ├── 04-flame-tests.json
│   └── 05-tests-for-ions.json
│
├── 09-atmosphere/
│   ├── 01-earths-early-atmosphere.json
│   ├── 02-evolution-of-atmosphere.json
│   ├── 03-greenhouse-gases.json
│   ├── 04-carbon-footprint.json
│   └── 05-atmospheric-pollutants.json
│
└── 10-using-resources/
    ├── 01-finite-and-renewable-resources.json
    ├── 02-water-treatment.json
    ├── 03-waste-water-treatment.json
    ├── 04-life-cycle-assessment.json
    ├── 05-reduce-reuse-recycle.json
    ├── 06-corrosion.json
    ├── 07-alloys.json
    ├── 08-ceramics-polymers-composites.json
    └── 09-haber-process.json
```

---

## AQA GCSE Biology (8461)

```
aqa/gcse-biology/content/
├── 01-cell-biology/
│   ├── 01-cell-structure.json
│   ├── 02-cell-division.json
│   ├── 03-transport-in-cells.json
│   ├── 04-microscopy.json
│   ├── 05-cell-differentiation.json
│   ├── 06-stem-cells.json
│   └── 07-prokaryotes-and-eukaryotes.json
│
├── 02-organisation/
│   ├── 01-principles-of-organisation.json
│   ├── 02-digestive-system.json
│   ├── 03-enzymes.json
│   ├── 04-heart-and-blood-vessels.json
│   ├── 05-blood.json
│   ├── 06-cardiovascular-disease.json
│   ├── 07-plant-tissues.json
│   └── 08-transpiration.json
│
├── 03-infection-and-response/
│   ├── 01-communicable-diseases.json
│   ├── 02-viral-diseases.json
│   ├── 03-bacterial-diseases.json
│   ├── 04-fungal-and-protist-diseases.json
│   ├── 05-human-defence-systems.json
│   ├── 06-vaccination.json
│   ├── 07-antibiotics-and-painkillers.json
│   ├── 08-drug-development.json
│   └── 09-monoclonal-antibodies.json
│
├── 04-bioenergetics/
│   ├── 01-photosynthesis.json
│   ├── 02-rate-of-photosynthesis.json
│   ├── 03-uses-of-glucose.json
│   ├── 04-aerobic-respiration.json
│   ├── 05-anaerobic-respiration.json
│   ├── 06-response-to-exercise.json
│   └── 07-metabolism.json
│
├── 05-homeostasis/
│   ├── 01-homeostasis.json
│   ├── 02-nervous-system.json
│   ├── 03-reflexes.json
│   ├── 04-brain.json
│   ├── 05-eye.json
│   ├── 06-control-of-body-temperature.json
│   ├── 07-hormones.json
│   ├── 08-blood-glucose-control.json
│   ├── 09-diabetes.json
│   ├── 10-hormones-in-reproduction.json
│   ├── 11-contraception.json
│   ├── 12-fertility-treatments.json
│   ├── 13-adrenaline-and-thyroxine.json
│   └── 14-plant-hormones.json
│
├── 06-inheritance/
│   ├── 01-sexual-and-asexual-reproduction.json
│   ├── 02-meiosis.json
│   ├── 03-dna-and-genome.json
│   ├── 04-genetic-inheritance.json
│   ├── 05-inherited-disorders.json
│   ├── 06-sex-determination.json
│   ├── 07-variation.json
│   ├── 08-evolution.json
│   ├── 09-selective-breeding.json
│   ├── 10-genetic-engineering.json
│   ├── 11-cloning.json
│   ├── 12-fossils.json
│   ├── 13-extinction.json
│   ├── 14-antibiotic-resistance.json
│   └── 15-classification.json
│
└── 07-ecology/
    ├── 01-communities.json
    ├── 02-abiotic-and-biotic-factors.json
    ├── 03-adaptations.json
    ├── 04-food-chains.json
    ├── 05-sampling-techniques.json
    ├── 06-carbon-cycle.json
    ├── 07-water-cycle.json
    ├── 08-biodiversity.json
    ├── 09-land-use.json
    ├── 10-global-warming.json
    ├── 11-deforestation.json
    ├── 12-maintaining-biodiversity.json
    ├── 13-trophic-levels.json
    ├── 14-food-production.json
    └── 15-sustainable-fisheries.json
```

---

## AQA GCSE Mathematics (8300)

```
aqa/gcse-maths/content/
├── 01-number/
│   ├── 01-integers-and-place-value.json
│   ├── 02-decimals.json
│   ├── 03-indices-powers-roots.json
│   ├── 04-factors-multiples-primes.json
│   ├── 05-standard-form.json
│   ├── 06-fractions.json
│   ├── 07-percentages.json
│   ├── 08-ratio-and-proportion.json
│   ├── 09-approximation-and-estimation.json
│   ├── 10-surds.json
│   └── 11-bounds.json
│
├── 02-algebra/
│   ├── 01-algebraic-notation.json
│   ├── 02-simplifying-expressions.json
│   ├── 03-expanding-brackets.json
│   ├── 04-factorising.json
│   ├── 05-solving-linear-equations.json
│   ├── 06-solving-quadratic-equations.json
│   ├── 07-simultaneous-equations.json
│   ├── 08-inequalities.json
│   ├── 09-sequences.json
│   ├── 10-straight-line-graphs.json
│   ├── 11-quadratic-graphs.json
│   ├── 12-other-graphs.json
│   ├── 13-transformations-of-graphs.json
│   ├── 14-algebraic-fractions.json
│   ├── 15-functions.json
│   └── 16-proof.json
│
├── 03-ratio-and-proportion/
│   ├── 01-ratio.json
│   ├── 02-direct-proportion.json
│   ├── 03-inverse-proportion.json
│   ├── 04-compound-measures.json
│   ├── 05-speed-distance-time.json
│   ├── 06-density.json
│   ├── 07-pressure.json
│   └── 08-growth-and-decay.json
│
├── 04-geometry/
│   ├── 01-properties-of-shapes.json
│   ├── 02-angles.json
│   ├── 03-parallel-lines.json
│   ├── 04-polygons.json
│   ├── 05-circles.json
│   ├── 06-circle-theorems.json
│   ├── 07-perimeter-and-area.json
│   ├── 08-surface-area-and-volume.json
│   ├── 09-transformations.json
│   ├── 10-congruence.json
│   ├── 11-similarity.json
│   ├── 12-pythagoras-theorem.json
│   ├── 13-trigonometry.json
│   ├── 14-trigonometry-non-right-triangles.json
│   ├── 15-vectors.json
│   └── 16-constructions-and-loci.json
│
├── 05-probability/
│   ├── 01-probability-basics.json
│   ├── 02-probability-experiments.json
│   ├── 03-sample-spaces.json
│   ├── 04-tree-diagrams.json
│   ├── 05-venn-diagrams.json
│   ├── 06-conditional-probability.json
│   └── 07-independent-events.json
│
└── 06-statistics/
    ├── 01-collecting-data.json
    ├── 02-representing-data.json
    ├── 03-averages-and-spread.json
    ├── 04-scatter-graphs.json
    ├── 05-time-series.json
    ├── 06-cumulative-frequency.json
    ├── 07-box-plots.json
    └── 08-histograms.json
```

---

# Cambridge IGCSE Courses

## Cambridge IGCSE Physics (0625)

```
cambridge/igcse-physics/content/
├── 01-motion-forces-energy/
│   ├── 01-physical-quantities-and-units.json
│   ├── 02-measuring-length-and-time.json
│   ├── 03-speed-velocity-acceleration.json
│   ├── 04-distance-time-graphs.json
│   ├── 05-velocity-time-graphs.json
│   ├── 06-free-fall.json
│   ├── 07-mass-and-weight.json
│   ├── 08-density.json
│   ├── 09-forces.json
│   ├── 10-turning-effect-of-forces.json
│   ├── 11-centre-of-gravity.json
│   ├── 12-scalars-and-vectors.json
│   ├── 13-momentum.json
│   ├── 14-energy-stores.json
│   ├── 15-energy-transfers.json
│   ├── 16-work-done.json
│   ├── 17-power.json
│   ├── 18-efficiency.json
│   ├── 19-pressure.json
│   └── 20-pressure-in-fluids.json
│
├── 02-thermal-physics/
│   ├── 01-kinetic-particle-model.json
│   ├── 02-states-of-matter.json
│   ├── 03-evaporation.json
│   ├── 04-thermal-expansion.json
│   ├── 05-temperature.json
│   ├── 06-thermal-capacity.json
│   ├── 07-latent-heat.json
│   ├── 08-conduction.json
│   ├── 09-convection.json
│   └── 10-radiation.json
│
├── 03-waves/
│   ├── 01-wave-properties.json
│   ├── 02-transverse-and-longitudinal.json
│   ├── 03-wave-equation.json
│   ├── 04-reflection-of-waves.json
│   ├── 05-refraction-of-waves.json
│   ├── 06-diffraction.json
│   ├── 07-light.json
│   ├── 08-reflection-of-light.json
│   ├── 09-refraction-of-light.json
│   ├── 10-thin-lenses.json
│   ├── 11-dispersion.json
│   ├── 12-em-spectrum.json
│   ├── 13-sound.json
│   ├── 14-ultrasound.json
│   └── 15-pitch-and-loudness.json
│
├── 04-electricity-and-magnetism/
│   ├── 01-simple-magnetism.json
│   ├── 02-magnetic-fields.json
│   ├── 03-electrostatics.json
│   ├── 04-electric-fields.json
│   ├── 05-electric-current.json
│   ├── 06-emf-and-potential-difference.json
│   ├── 07-resistance.json
│   ├── 08-electrical-circuits.json
│   ├── 09-series-circuits.json
│   ├── 10-parallel-circuits.json
│   ├── 11-electrical-safety.json
│   ├── 12-electrical-energy-and-power.json
│   ├── 13-electromagnetic-effect.json
│   ├── 14-dc-motor.json
│   ├── 15-electromagnetic-induction.json
│   ├── 16-ac-generator.json
│   └── 17-transformers.json
│
├── 05-nuclear-physics/
│   ├── 01-atomic-model.json
│   ├── 02-nuclear-structure.json
│   ├── 03-isotopes.json
│   ├── 04-radioactivity.json
│   ├── 05-alpha-beta-gamma.json
│   ├── 06-half-life.json
│   ├── 07-safety-precautions.json
│   └── 08-uses-of-radioactivity.json
│
└── 06-space-physics/
    ├── 01-earth-and-solar-system.json
    ├── 02-the-sun.json
    ├── 03-stars-and-galaxies.json
    └── 04-the-universe.json
```

---

## Cambridge IGCSE Chemistry (0620)

```
cambridge/igcse-chemistry/content/
├── 01-states-of-matter/
│   ├── 01-solids-liquids-gases.json
│   ├── 02-particle-theory.json
│   ├── 03-changes-of-state.json
│   ├── 04-diffusion.json
│   └── 05-brownian-motion.json
│
├── 02-atoms-elements-compounds/
│   ├── 01-atomic-structure.json
│   ├── 02-electron-arrangement.json
│   ├── 03-elements-and-symbols.json
│   ├── 04-compounds.json
│   ├── 05-ions.json
│   ├── 06-ionic-bonding.json
│   ├── 07-covalent-bonding.json
│   ├── 08-metallic-bonding.json
│   └── 09-giant-structures.json
│
├── 03-stoichiometry/
│   ├── 01-relative-masses.json
│   ├── 02-mole-concept.json
│   ├── 03-chemical-formulae.json
│   ├── 04-chemical-equations.json
│   ├── 05-reacting-masses.json
│   ├── 06-molar-gas-volume.json
│   ├── 07-concentration.json
│   └── 08-percentage-composition.json
│
├── 04-electrochemistry/
│   ├── 01-electrolysis.json
│   ├── 02-electrolysis-of-molten-compounds.json
│   ├── 03-electrolysis-of-aqueous-solutions.json
│   ├── 04-electroplating.json
│   ├── 05-simple-cells.json
│   └── 06-fuel-cells.json
│
├── 05-chemical-energetics/
│   ├── 01-exothermic-and-endothermic.json
│   ├── 02-energy-diagrams.json
│   ├── 03-bond-energies.json
│   └── 04-activation-energy.json
│
├── 06-chemical-reactions/
│   ├── 01-measuring-rate-of-reaction.json
│   ├── 02-factors-affecting-rate.json
│   ├── 03-catalysts.json
│   ├── 04-enzymes.json
│   ├── 05-reversible-reactions.json
│   ├── 06-equilibrium.json
│   └── 07-redox.json
│
├── 07-acids-bases-salts/
│   ├── 01-acids-and-bases.json
│   ├── 02-ph-scale.json
│   ├── 03-indicators.json
│   ├── 04-neutralisation.json
│   ├── 05-oxides.json
│   ├── 06-preparing-salts.json
│   └── 07-identification-of-ions.json
│
├── 08-periodic-table/
│   ├── 01-periodic-table-arrangement.json
│   ├── 02-groups-and-periods.json
│   ├── 03-group-1-alkali-metals.json
│   ├── 04-group-17-halogens.json
│   ├── 05-group-18-noble-gases.json
│   ├── 06-transition-elements.json
│   └── 07-trends-in-periodic-table.json
│
├── 09-metals/
│   ├── 01-properties-of-metals.json
│   ├── 02-reactivity-series.json
│   ├── 03-extraction-of-metals.json
│   ├── 04-iron-extraction.json
│   ├── 05-aluminium-extraction.json
│   ├── 06-alloys.json
│   └── 07-corrosion.json
│
├── 10-environment/
│   ├── 01-water.json
│   ├── 02-air-composition.json
│   ├── 03-carbon-dioxide-and-carbon-cycle.json
│   ├── 04-nitrogen-cycle.json
│   ├── 05-pollution.json
│   └── 06-greenhouse-effect.json
│
└── 11-organic-chemistry/
    ├── 01-fuels-and-crude-oil.json
    ├── 02-alkanes.json
    ├── 03-alkenes.json
    ├── 04-alcohols.json
    ├── 05-carboxylic-acids.json
    ├── 06-esters.json
    ├── 07-polymers.json
    ├── 08-isomerism.json
    └── 09-cracking.json
```

---

## Cambridge IGCSE Biology (0610)

```
cambridge/igcse-biology/content/
├── 01-characteristics-of-living-organisms/
│   ├── 01-characteristics-of-life.json
│   └── 02-classification.json
│
├── 02-cells/
│   ├── 01-cell-structure.json
│   ├── 02-animal-vs-plant-cells.json
│   ├── 03-specialised-cells.json
│   ├── 04-cell-organisation.json
│   └── 05-cell-size-and-microscopy.json
│
├── 03-movement-into-and-out-of-cells/
│   ├── 01-diffusion.json
│   ├── 02-osmosis.json
│   └── 03-active-transport.json
│
├── 04-biological-molecules/
│   ├── 01-carbohydrates.json
│   ├── 02-lipids.json
│   ├── 03-proteins.json
│   ├── 04-enzymes.json
│   └── 05-testing-for-nutrients.json
│
├── 05-enzymes/
│   ├── 01-enzyme-structure.json
│   ├── 02-enzyme-action.json
│   ├── 03-factors-affecting-enzymes.json
│   └── 04-enzymes-in-industry.json
│
├── 06-plant-nutrition/
│   ├── 01-photosynthesis.json
│   ├── 02-leaf-structure.json
│   ├── 03-factors-affecting-photosynthesis.json
│   └── 04-mineral-requirements.json
│
├── 07-human-nutrition/
│   ├── 01-balanced-diet.json
│   ├── 02-digestive-system.json
│   ├── 03-mechanical-digestion.json
│   ├── 04-chemical-digestion.json
│   └── 05-absorption.json
│
├── 08-transport-in-plants/
│   ├── 01-xylem-and-phloem.json
│   ├── 02-water-uptake.json
│   ├── 03-transpiration.json
│   └── 04-translocation.json
│
├── 09-transport-in-animals/
│   ├── 01-circulatory-system.json
│   ├── 02-heart-structure.json
│   ├── 03-blood-vessels.json
│   ├── 04-blood.json
│   └── 05-lymphatic-system.json
│
├── 10-diseases-and-immunity/
│   ├── 01-pathogens.json
│   ├── 02-transmission-of-disease.json
│   ├── 03-body-defences.json
│   ├── 04-immune-response.json
│   └── 05-vaccination.json
│
├── 11-respiration/
│   ├── 01-aerobic-respiration.json
│   ├── 02-anaerobic-respiration.json
│   └── 03-gas-exchange.json
│
├── 12-excretion/
│   ├── 01-excretion-in-humans.json
│   ├── 02-kidney-structure.json
│   ├── 03-kidney-function.json
│   └── 04-dialysis-and-transplants.json
│
├── 13-coordination-and-response/
│   ├── 01-nervous-system.json
│   ├── 02-sense-organs.json
│   ├── 03-reflexes.json
│   ├── 04-hormones.json
│   ├── 05-homeostasis.json
│   ├── 06-plant-responses.json
│   └── 07-drugs.json
│
├── 14-reproduction/
│   ├── 01-asexual-reproduction.json
│   ├── 02-sexual-reproduction-in-plants.json
│   ├── 03-sexual-reproduction-in-humans.json
│   ├── 04-menstrual-cycle.json
│   ├── 05-fertilisation-and-pregnancy.json
│   └── 06-birth-control.json
│
├── 15-inheritance/
│   ├── 01-chromosomes-and-genes.json
│   ├── 02-dna-structure.json
│   ├── 03-cell-division.json
│   ├── 04-monohybrid-inheritance.json
│   ├── 05-genetic-diagrams.json
│   ├── 06-sex-determination.json
│   ├── 07-variation.json
│   ├── 08-mutation.json
│   ├── 09-natural-selection.json
│   └── 10-genetic-engineering.json
│
└── 16-ecology/
    ├── 01-organisms-and-environment.json
    ├── 02-food-chains-and-webs.json
    ├── 03-energy-flow.json
    ├── 04-nutrient-cycles.json
    ├── 05-population-size.json
    └── 06-human-impact-on-environment.json
```

---

## Cambridge IGCSE Mathematics (0580)

```
cambridge/igcse-maths/content/
├── 01-number/
│   ├── 01-integers.json
│   ├── 02-place-value.json
│   ├── 03-directed-numbers.json
│   ├── 04-squares-cubes-roots.json
│   ├── 05-order-of-operations.json
│   ├── 06-factors-and-multiples.json
│   ├── 07-prime-numbers.json
│   ├── 08-fractions.json
│   ├── 09-decimals.json
│   ├── 10-percentages.json
│   ├── 11-ratio-and-proportion.json
│   ├── 12-standard-form.json
│   ├── 13-bounds-and-accuracy.json
│   ├── 14-estimation.json
│   └── 15-surds.json
│
├── 02-algebra/
│   ├── 01-algebraic-notation.json
│   ├── 02-substitution.json
│   ├── 03-simplifying-expressions.json
│   ├── 04-expanding-brackets.json
│   ├── 05-factorising.json
│   ├── 06-linear-equations.json
│   ├── 07-changing-the-subject.json
│   ├── 08-quadratic-equations.json
│   ├── 09-completing-the-square.json
│   ├── 10-simultaneous-equations.json
│   ├── 11-inequalities.json
│   ├── 12-indices.json
│   ├── 13-sequences.json
│   ├── 14-direct-variation.json
│   ├── 15-inverse-variation.json
│   ├── 16-algebraic-fractions.json
│   └── 17-functions.json
│
├── 03-graphs/
│   ├── 01-cartesian-coordinates.json
│   ├── 02-plotting-graphs.json
│   ├── 03-gradient.json
│   ├── 04-straight-line-graphs.json
│   ├── 05-equation-of-a-line.json
│   ├── 06-parallel-and-perpendicular-lines.json
│   ├── 07-quadratic-graphs.json
│   ├── 08-cubic-graphs.json
│   ├── 09-reciprocal-graphs.json
│   ├── 10-exponential-graphs.json
│   ├── 11-graphical-solution-of-equations.json
│   ├── 12-gradient-of-curves.json
│   ├── 13-travel-graphs.json
│   └── 14-graph-transformations.json
│
├── 04-geometry/
│   ├── 01-angles.json
│   ├── 02-parallel-lines.json
│   ├── 03-triangles.json
│   ├── 04-quadrilaterals.json
│   ├── 05-polygons.json
│   ├── 06-circles.json
│   ├── 07-symmetry.json
│   ├── 08-similarity.json
│   ├── 09-congruence.json
│   ├── 10-constructions.json
│   ├── 11-loci.json
│   └── 12-nets-and-3d-shapes.json
│
├── 05-mensuration/
│   ├── 01-perimeter.json
│   ├── 02-area-of-triangles.json
│   ├── 03-area-of-quadrilaterals.json
│   ├── 04-area-of-circles.json
│   ├── 05-arc-length-and-sector-area.json
│   ├── 06-surface-area.json
│   ├── 07-volume-of-prisms.json
│   ├── 08-volume-of-pyramids-cones.json
│   ├── 09-volume-of-spheres.json
│   └── 10-compound-shapes.json
│
├── 06-trigonometry/
│   ├── 01-pythagoras-theorem.json
│   ├── 02-trigonometric-ratios.json
│   ├── 03-finding-angles.json
│   ├── 04-finding-sides.json
│   ├── 05-angles-of-elevation-and-depression.json
│   ├── 06-bearings.json
│   ├── 07-sine-rule.json
│   ├── 08-cosine-rule.json
│   ├── 09-area-of-triangle.json
│   ├── 10-trigonometry-in-3d.json
│   └── 11-trig-graphs.json
│
├── 07-vectors-and-transformations/
│   ├── 01-vectors.json
│   ├── 02-vector-addition.json
│   ├── 03-scalar-multiplication.json
│   ├── 04-position-vectors.json
│   ├── 05-translations.json
│   ├── 06-reflections.json
│   ├── 07-rotations.json
│   ├── 08-enlargements.json
│   └── 09-combined-transformations.json
│
├── 08-probability/
│   ├── 01-probability-scale.json
│   ├── 02-theoretical-probability.json
│   ├── 03-experimental-probability.json
│   ├── 04-combined-events.json
│   ├── 05-tree-diagrams.json
│   ├── 06-venn-diagrams.json
│   └── 07-conditional-probability.json
│
└── 09-statistics/
    ├── 01-data-collection.json
    ├── 02-frequency-tables.json
    ├── 03-pictograms-and-bar-charts.json
    ├── 04-pie-charts.json
    ├── 05-mean-median-mode.json
    ├── 06-range.json
    ├── 07-grouped-data.json
    ├── 08-scatter-graphs.json
    ├── 09-correlation.json
    ├── 10-cumulative-frequency.json
    └── 11-histograms.json
```

---

# Edexcel Courses

## Edexcel GCSE Physics (1PH0)

```
edexcel/gcse-physics/content/
├── 01-key-concepts/
│   ├── 01-units-and-prefixes.json
│   ├── 02-equations.json
│   ├── 03-scalar-and-vector.json
│   └── 04-practical-skills.json
│
├── 02-motion-and-forces/
│   ├── 01-distance-and-displacement.json
│   ├── 02-speed-and-velocity.json
│   ├── 03-acceleration.json
│   ├── 04-distance-time-graphs.json
│   ├── 05-velocity-time-graphs.json
│   ├── 06-equations-of-motion.json
│   ├── 07-newtons-first-law.json
│   ├── 08-newtons-second-law.json
│   ├── 09-newtons-third-law.json
│   ├── 10-stopping-distances.json
│   ├── 11-momentum.json
│   └── 12-conservation-of-momentum.json
│
├── 03-conservation-of-energy/
│   ├── 01-energy-stores-and-transfers.json
│   ├── 02-kinetic-energy.json
│   ├── 03-gravitational-potential-energy.json
│   ├── 04-work-done.json
│   ├── 05-power.json
│   ├── 06-efficiency.json
│   ├── 07-elastic-potential-energy.json
│   └── 08-specific-heat-capacity.json
│
├── 04-waves/
│   ├── 01-wave-properties.json
│   ├── 02-wave-types.json
│   ├── 03-measuring-waves.json
│   ├── 04-reflection.json
│   ├── 05-refraction.json
│   ├── 06-sound-waves.json
│   ├── 07-seismic-waves.json
│   └── 08-echo-and-ultrasound.json
│
├── 05-light-and-em-spectrum/
│   ├── 01-reflection-of-light.json
│   ├── 02-refraction-of-light.json
│   ├── 03-lenses.json
│   ├── 04-visible-light.json
│   ├── 05-em-spectrum.json
│   ├── 06-properties-of-em-waves.json
│   ├── 07-uses-of-em-waves.json
│   └── 08-dangers-of-em-waves.json
│
├── 06-radioactivity/
│   ├── 01-atomic-structure.json
│   ├── 02-isotopes.json
│   ├── 03-radioactive-decay.json
│   ├── 04-alpha-particles.json
│   ├── 05-beta-particles.json
│   ├── 06-gamma-rays.json
│   ├── 07-half-life.json
│   ├── 08-uses-of-radiation.json
│   ├── 09-hazards-of-radiation.json
│   ├── 10-nuclear-fission.json
│   └── 11-nuclear-fusion.json
│
├── 07-astronomy/
│   ├── 01-solar-system.json
│   ├── 02-earth-and-moon.json
│   ├── 03-satellites.json
│   ├── 04-life-cycle-of-stars.json
│   ├── 05-origin-of-elements.json
│   └── 06-expanding-universe.json
│
├── 08-energy-sources/
│   ├── 01-energy-resources.json
│   ├── 02-fossil-fuels.json
│   ├── 03-nuclear-power.json
│   ├── 04-renewable-energy.json
│   └── 05-generating-electricity.json
│
├── 09-electricity/
│   ├── 01-electric-circuits.json
│   ├── 02-current.json
│   ├── 03-potential-difference.json
│   ├── 04-resistance.json
│   ├── 05-resistors.json
│   ├── 06-series-circuits.json
│   ├── 07-parallel-circuits.json
│   ├── 08-power.json
│   ├── 09-energy-transfer.json
│   ├── 10-domestic-electricity.json
│   └── 11-electrical-safety.json
│
├── 10-static-electricity/
│   ├── 01-static-charge.json
│   ├── 02-electric-fields.json
│   └── 03-uses-and-dangers.json
│
├── 11-magnetism/
│   ├── 01-magnets.json
│   ├── 02-magnetic-fields.json
│   ├── 03-electromagnets.json
│   ├── 04-motor-effect.json
│   ├── 05-dc-motors.json
│   ├── 06-electromagnetic-induction.json
│   ├── 07-generators.json
│   ├── 08-transformers.json
│   └── 09-national-grid.json
│
├── 12-particle-model/
│   ├── 01-states-of-matter.json
│   ├── 02-particle-model.json
│   ├── 03-density.json
│   ├── 04-changes-of-state.json
│   ├── 05-internal-energy.json
│   ├── 06-specific-heat-capacity.json
│   ├── 07-specific-latent-heat.json
│   └── 08-gas-pressure.json
│
└── 13-forces-and-matter/
    ├── 01-pressure.json
    ├── 02-pressure-in-fluids.json
    ├── 03-atmospheric-pressure.json
    ├── 04-springs.json
    ├── 05-hookes-law.json
    └── 06-moments.json
```

---

## Edexcel GCSE Chemistry (1CH0)

```
edexcel/gcse-chemistry/content/
├── 01-key-concepts/
│   ├── 01-states-of-matter.json
│   ├── 02-elements-compounds-mixtures.json
│   ├── 03-atomic-structure.json
│   ├── 04-periodic-table.json
│   ├── 05-ionic-bonding.json
│   ├── 06-covalent-bonding.json
│   ├── 07-metallic-bonding.json
│   ├── 08-conservation-of-mass.json
│   ├── 09-relative-formula-mass.json
│   └── 10-moles.json
│
├── 02-states-of-matter/
│   ├── 01-particle-model.json
│   ├── 02-changes-of-state.json
│   ├── 03-limitations-of-model.json
│   ├── 04-pure-substances.json
│   ├── 05-mixtures.json
│   └── 06-separation-techniques.json
│
├── 03-chemical-changes/
│   ├── 01-acids-and-alkalis.json
│   ├── 02-neutralisation.json
│   ├── 03-making-salts.json
│   ├── 04-electrolysis.json
│   ├── 05-electrolysis-of-molten-compounds.json
│   ├── 06-electrolysis-of-solutions.json
│   ├── 07-oxidation-and-reduction.json
│   └── 08-extraction-of-metals.json
│
├── 04-extracting-metals/
│   ├── 01-reactivity-series.json
│   ├── 02-extraction-methods.json
│   ├── 03-iron-extraction.json
│   ├── 04-aluminium-extraction.json
│   ├── 05-copper-purification.json
│   ├── 06-recycling.json
│   └── 07-life-cycle-assessment.json
│
├── 05-groups-in-periodic-table/
│   ├── 01-group-1.json
│   ├── 02-group-7.json
│   ├── 03-group-0.json
│   └── 04-transition-metals.json
│
├── 06-rates-of-reaction/
│   ├── 01-measuring-rate.json
│   ├── 02-factors-affecting-rate.json
│   ├── 03-collision-theory.json
│   ├── 04-surface-area.json
│   ├── 05-temperature.json
│   ├── 06-concentration.json
│   ├── 07-catalysts.json
│   └── 08-enzymes.json
│
├── 07-heat-energy-changes/
│   ├── 01-exothermic-reactions.json
│   ├── 02-endothermic-reactions.json
│   ├── 03-energy-level-diagrams.json
│   ├── 04-activation-energy.json
│   └── 05-bond-energies.json
│
├── 08-fuels-and-earth-science/
│   ├── 01-hydrocarbons.json
│   ├── 02-crude-oil.json
│   ├── 03-fractional-distillation.json
│   ├── 04-combustion.json
│   ├── 05-cracking.json
│   ├── 06-early-atmosphere.json
│   ├── 07-evolution-of-atmosphere.json
│   ├── 08-greenhouse-gases.json
│   └── 09-climate-change.json
│
├── 09-earth-and-atmospheric-science/
│   ├── 01-composition-of-atmosphere.json
│   ├── 02-pollutants.json
│   ├── 03-carbon-footprint.json
│   ├── 04-water-treatment.json
│   ├── 05-potable-water.json
│   └── 06-waste-water.json
│
└── 10-organic-chemistry/
    ├── 01-alkanes.json
    ├── 02-alkenes.json
    ├── 03-alcohols.json
    ├── 04-carboxylic-acids.json
    ├── 05-esters.json
    ├── 06-addition-polymers.json
    ├── 07-condensation-polymers.json
    └── 08-dna.json
```

---

## Edexcel GCSE Biology (1BI0)

```
edexcel/gcse-biology/content/
├── 01-key-concepts/
│   ├── 01-microscopy.json
│   ├── 02-animal-cells.json
│   ├── 03-plant-cells.json
│   ├── 04-specialised-cells.json
│   ├── 05-enzymes.json
│   ├── 06-factors-affecting-enzymes.json
│   └── 07-enzyme-controlled-reactions.json
│
├── 02-cells-and-control/
│   ├── 01-mitosis.json
│   ├── 02-cell-growth-and-differentiation.json
│   ├── 03-stem-cells.json
│   ├── 04-nervous-system.json
│   ├── 05-neurones.json
│   ├── 06-synapses.json
│   └── 07-reflexes.json
│
├── 03-genetics/
│   ├── 01-meiosis.json
│   ├── 02-dna.json
│   ├── 03-protein-synthesis.json
│   ├── 04-genetic-inheritance.json
│   ├── 05-genetic-diagrams.json
│   ├── 06-sex-determination.json
│   ├── 07-genetic-variation.json
│   └── 08-mutations.json
│
├── 04-natural-selection/
│   ├── 01-evidence-for-evolution.json
│   ├── 02-darwin.json
│   ├── 03-natural-selection.json
│   ├── 04-selective-breeding.json
│   ├── 05-genetic-engineering.json
│   └── 06-ethics-of-genetic-technology.json
│
├── 05-health-disease-medicine/
│   ├── 01-health-and-disease.json
│   ├── 02-pathogens.json
│   ├── 03-viral-diseases.json
│   ├── 04-bacterial-diseases.json
│   ├── 05-spread-of-pathogens.json
│   ├── 06-body-defences.json
│   ├── 07-immune-system.json
│   ├── 08-vaccination.json
│   ├── 09-antibiotics.json
│   └── 10-drug-development.json
│
├── 06-plant-structures/
│   ├── 01-photosynthesis.json
│   ├── 02-factors-affecting-photosynthesis.json
│   ├── 03-uses-of-glucose.json
│   ├── 04-leaf-structure.json
│   ├── 05-roots.json
│   ├── 06-transpiration.json
│   └── 07-translocation.json
│
├── 07-animal-coordination/
│   ├── 01-hormonal-coordination.json
│   ├── 02-hormones-in-reproduction.json
│   ├── 03-contraception.json
│   ├── 04-control-of-blood-glucose.json
│   ├── 05-diabetes.json
│   ├── 06-negative-feedback.json
│   └── 07-hormone-interaction.json
│
├── 08-exchange-and-transport/
│   ├── 01-diffusion.json
│   ├── 02-osmosis.json
│   ├── 03-active-transport.json
│   ├── 04-surface-area-to-volume.json
│   ├── 05-gas-exchange-in-lungs.json
│   ├── 06-circulatory-system.json
│   ├── 07-blood-vessels.json
│   └── 08-blood.json
│
└── 09-ecosystems/
    ├── 01-communities.json
    ├── 02-abiotic-biotic-factors.json
    ├── 03-food-chains-and-webs.json
    ├── 04-energy-transfer.json
    ├── 05-carbon-cycle.json
    ├── 06-nitrogen-cycle.json
    ├── 07-decay.json
    ├── 08-sampling.json
    ├── 09-biodiversity.json
    └── 10-human-impact.json
```

---

## Edexcel GCSE Mathematics (1MA1)

```
edexcel/gcse-maths/content/
├── 01-number/
│   ├── 01-integers-and-place-value.json
│   ├── 02-decimals.json
│   ├── 03-indices.json
│   ├── 04-roots.json
│   ├── 05-factors-multiples-primes.json
│   ├── 06-fractions.json
│   ├── 07-operations-with-fractions.json
│   ├── 08-percentages.json
│   ├── 09-percentage-change.json
│   ├── 10-standard-form.json
│   ├── 11-surds.json
│   └── 12-bounds.json
│
├── 02-algebra/
│   ├── 01-expressions.json
│   ├── 02-simplifying.json
│   ├── 03-expanding-brackets.json
│   ├── 04-factorising.json
│   ├── 05-solving-equations.json
│   ├── 06-rearranging-formulae.json
│   ├── 07-quadratics.json
│   ├── 08-completing-the-square.json
│   ├── 09-quadratic-formula.json
│   ├── 10-simultaneous-equations.json
│   ├── 11-inequalities.json
│   ├── 12-sequences.json
│   ├── 13-nth-term.json
│   ├── 14-iteration.json
│   ├── 15-functions.json
│   └── 16-algebraic-proof.json
│
├── 03-ratio-proportion/
│   ├── 01-ratio.json
│   ├── 02-proportion.json
│   ├── 03-direct-proportion.json
│   ├── 04-inverse-proportion.json
│   ├── 05-scale.json
│   ├── 06-compound-measures.json
│   └── 07-growth-and-decay.json
│
├── 04-geometry/
│   ├── 01-angles.json
│   ├── 02-properties-of-shapes.json
│   ├── 03-triangles.json
│   ├── 04-quadrilaterals.json
│   ├── 05-polygons.json
│   ├── 06-circles.json
│   ├── 07-constructions.json
│   ├── 08-loci.json
│   ├── 09-3d-shapes.json
│   ├── 10-perimeter-and-area.json
│   ├── 11-circles-area.json
│   ├── 12-surface-area.json
│   ├── 13-volume.json
│   ├── 14-transformations.json
│   ├── 15-similarity.json
│   ├── 16-congruence.json
│   ├── 17-pythagoras.json
│   ├── 18-trigonometry.json
│   ├── 19-exact-values.json
│   ├── 20-sine-cosine-rules.json
│   ├── 21-circle-theorems.json
│   └── 22-vectors.json
│
├── 05-probability/
│   ├── 01-probability-basics.json
│   ├── 02-calculating-probability.json
│   ├── 03-experimental-probability.json
│   ├── 04-combined-events.json
│   ├── 05-tree-diagrams.json
│   ├── 06-venn-diagrams.json
│   └── 07-conditional-probability.json
│
├── 06-statistics/
│   ├── 01-collecting-data.json
│   ├── 02-sampling.json
│   ├── 03-tables-and-charts.json
│   ├── 04-averages.json
│   ├── 05-range.json
│   ├── 06-grouped-data.json
│   ├── 07-scatter-graphs.json
│   ├── 08-time-series.json
│   ├── 09-cumulative-frequency.json
│   ├── 10-box-plots.json
│   └── 11-histograms.json
│
└── 07-graphs/
    ├── 01-coordinates.json
    ├── 02-linear-graphs.json
    ├── 03-gradient.json
    ├── 04-y-intercept.json
    ├── 05-parallel-perpendicular.json
    ├── 06-quadratic-graphs.json
    ├── 07-cubic-graphs.json
    ├── 08-reciprocal-graphs.json
    ├── 09-real-life-graphs.json
    ├── 10-distance-time.json
    ├── 11-velocity-time.json
    ├── 12-gradient-of-curve.json
    ├── 13-area-under-curve.json
    └── 14-transformations-of-graphs.json
```

---

## Edexcel IGCSE Courses

Edexcel IGCSEs follow similar structures to Cambridge IGCSEs but with Edexcel-specific content. Use the Cambridge structure as a template with adjustments for Edexcel specifications.

```
edexcel/igcse-physics/     # Similar to Cambridge, aligned to Edexcel 4PH1
edexcel/igcse-chemistry/   # Similar to Cambridge, aligned to Edexcel 4CH1
edexcel/igcse-biology/     # Similar to Cambridge, aligned to Edexcel 4BI1
edexcel/igcse-maths/       # Similar to Cambridge, aligned to Edexcel 4MA1
```

---

# Summary Table

| Exam Board | Qualification | Subject   | Est. Topics | Est. Pages |
|------------|--------------|-----------|-------------|------------|
| AQA        | GCSE         | Physics   | 8 units     | ~55 pages  |
| AQA        | GCSE         | Chemistry | 10 units    | ~60 pages  |
| AQA        | GCSE         | Biology   | 7 units     | ~65 pages  |
| AQA        | GCSE         | Maths     | 6 units     | ~60 pages  |
| Cambridge  | IGCSE        | Physics   | 6 units     | ~50 pages  |
| Cambridge  | IGCSE        | Chemistry | 11 units    | ~55 pages  |
| Cambridge  | IGCSE        | Biology   | 16 units    | ~60 pages  |
| Cambridge  | IGCSE        | Maths     | 9 units     | ~55 pages  |
| Edexcel    | GCSE         | Physics   | 13 units    | ~70 pages  |
| Edexcel    | GCSE         | Chemistry | 10 units    | ~55 pages  |
| Edexcel    | GCSE         | Biology   | 9 units     | ~55 pages  |
| Edexcel    | GCSE         | Maths     | 7 units     | ~70 pages  |
| Edexcel    | IGCSE        | Physics   | ~6 units    | ~50 pages  |
| Edexcel    | IGCSE        | Chemistry | ~11 units   | ~55 pages  |
| Edexcel    | IGCSE        | Biology   | ~16 units   | ~60 pages  |
| Edexcel    | IGCSE        | Maths     | ~9 units    | ~55 pages  |

**Total: ~16 courses, ~140 units, ~900+ content pages**

---

# Next Steps

1. Migrate existing Cambridge IGCSE content to new structure
2. Create `_course.json` metadata files for all courses
3. Create `_unit.json` metadata files for all units
4. Generate placeholder content files
5. Prioritize content creation based on student demand
