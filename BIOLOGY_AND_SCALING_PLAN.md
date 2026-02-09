# Generic Biology Development Plan & Cross-Subject Scaling Strategy

## Document Overview

This document contains two major sections:
1. **Part 1:** Comprehensive development plan for Generic Biology
2. **Part 2:** Strategy for creating other courses (Chemistry, Maths, Board-Specific) based on the Generic Physics template

---

# Part 1: Generic Biology Course Development

## 1.1 Course Overview

Generic Biology is a comprehensive course covering all fundamental biology concepts for GCSE/IGCSE level. It maps to AQA (8461), Cambridge (0610), Edexcel GCSE (1BI0), and Edexcel IGCSE (4BI1) specifications.

### Current State
- **Completed:** 0 lessons
- **Existing Structure:** 10 unit directories with `_unit.json` metadata
- **Target:** 95-110 lessons across 10 units

### Unit Structure Overview

| Unit | Title | Syllabus Coverage | Est. Lessons |
|------|-------|-------------------|--------------|
| 01 | Cells | Cell structure, division, transport | 10-12 |
| 02 | Biological Molecules | Carbohydrates, proteins, lipids, enzymes | 8-10 |
| 03 | Nutrition | Photosynthesis, digestion, balanced diet | 10-12 |
| 04 | Transport | Circulatory system, blood, plant transport | 12-14 |
| 05 | Respiration and Gas Exchange | Aerobic/anaerobic, lungs | 6-8 |
| 06 | Excretion | Kidneys, waste removal | 4-6 |
| 07 | Coordination and Homeostasis | Nervous system, hormones, control | 14-16 |
| 08 | Reproduction | Sexual/asexual, plant and human | 10-12 |
| 09 | Inheritance and Evolution | DNA, genetics, natural selection | 14-16 |
| 10 | Ecology | Ecosystems, food chains, human impact | 10-12 |

**Total Estimated Lessons: 98-118**

---

## 1.2 Biology-Specific Content Standards

### File Format
Same as Physics - JSON with Markdown content:

```json
{
  "title": "Lesson Title",
  "content": "# Markdown content with scientific notation",
  "order": 1
}
```

### Biology-Specific Markdown Conventions

#### Scientific Terminology
Use **bold** for key terms on first occurrence with definitions:

```markdown
**Mitosis** is the type of cell division that produces two genetically identical daughter cells.
```

#### Chemical/Biochemical Equations
Use LaTeX for equations:

```markdown
**Photosynthesis equation:**
$$\text{6CO}_2 + \text{6H}_2\text{O} \xrightarrow{\text{light}} \text{C}_6\text{H}_{12}\text{O}_6 + \text{6O}_2$$

Or simplified:
$$\text{carbon dioxide} + \text{water} \xrightarrow{\text{light energy}} \text{glucose} + \text{oxygen}$$
```

#### Diagram Placeholders
Biology is heavily diagram-dependent. Mark where diagrams are needed:

```markdown
[DIAGRAM: Structure of an animal cell showing nucleus, cytoplasm, cell membrane, mitochondria, ribosomes]

[DIAGRAM: Cross-section of a leaf showing palisade mesophyll, spongy mesophyll, stomata, guard cells]

[DIAGRAM: The human heart showing four chambers, valves, and blood flow direction]
```

#### Tables for Comparisons
Biology often requires comparison tables:

```markdown
| Feature | Plant Cell | Animal Cell |
|---------|-----------|-------------|
| Cell wall | Present (cellulose) | Absent |
| Chloroplasts | Present | Absent |
| Vacuole | Large, permanent | Small or absent |
| Shape | Fixed, rectangular | Variable |
```

### Content Structure Template for Biology

```markdown
# [Topic Title]

## Learning Objectives
By the end of this lesson, you should be able to:
- [Objective 1]
- [Objective 2]
- [Objective 3]

## Introduction
[1-2 paragraphs introducing the topic and its importance]

## Key Concepts

### [Concept 1]
[Detailed explanation]

[DIAGRAM: Description of required diagram]

### [Concept 2]
[Detailed explanation with examples]

## Processes and Mechanisms
[Step-by-step descriptions of biological processes]

## Practical Applications
[Real-world examples and applications]

## Common Exam Questions
[Types of questions commonly asked on this topic]

## Common Misconceptions
- **Misconception:** [What students often get wrong]
- **Reality:** [The correct understanding]

## Practice Questions

1. [Knowledge recall question]
2. [Application question]
3. [Analysis/explain question]
4. [Extended response/6-mark style question]

## Key Terms Glossary
| Term | Definition |
|------|------------|
| [Term 1] | [Definition] |
| [Term 2] | [Definition] |

## Summary
- [Key point 1]
- [Key point 2]
- [Key point 3]
```

---

## 1.3 Detailed Topic Breakdown by Unit

### Unit 01: Cells
**Location:** `generic/biology/content/01-cells/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-cell-structure.json` | Cell Structure | Nucleus, cytoplasm, cell membrane, organelles |
| 02 | `02-animal-vs-plant-cells.json` | Animal and Plant Cells | Differences: cell wall, chloroplasts, vacuole |
| 03 | `03-bacterial-cells.json` | Bacterial Cells | Prokaryotic structure, comparison with eukaryotes |
| 04 | `04-specialised-cells.json` | Specialised Cells | Nerve, muscle, red blood, root hair, xylem, phloem |
| 05 | `05-levels-of-organisation.json` | Levels of Organisation | Cell → tissue → organ → organ system → organism |
| 06 | `06-microscopy.json` | Microscopy | Light vs electron microscopes, magnification, resolution |
| 07 | `07-cell-size-calculations.json` | Cell Size Calculations | Magnification formula, scale bars, unit conversions |
| 08 | `08-mitosis.json` | Mitosis | Stages, purpose (growth, repair, asexual reproduction) |
| 09 | `09-cell-cycle.json` | The Cell Cycle | Interphase, mitosis, cell division |
| 10 | `10-stem-cells.json` | Stem Cells | Types, uses, ethical considerations |
| 11 | `11-diffusion.json` | Diffusion | Definition, factors affecting rate, examples |
| 12 | `12-osmosis.json` | Osmosis | Water movement, concentration gradients, plant cells |
| 13 | `13-active-transport.json` | Active Transport | Energy requirement, examples (root hairs, gut) |

### Unit 02: Biological Molecules
**Location:** `generic/biology/content/02-biological-molecules/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-carbohydrates.json` | Carbohydrates | Glucose, starch, glycogen, cellulose |
| 02 | `02-lipids.json` | Lipids (Fats and Oils) | Structure, function, saturated vs unsaturated |
| 03 | `03-proteins.json` | Proteins | Amino acids, peptide bonds, protein structure |
| 04 | `04-enzymes-introduction.json` | Introduction to Enzymes | Biological catalysts, lock and key model |
| 05 | `05-enzyme-action.json` | Enzyme Action | Active site, substrate, products, specificity |
| 06 | `06-factors-affecting-enzymes.json` | Factors Affecting Enzymes | Temperature, pH, substrate concentration |
| 07 | `07-enzyme-experiments.json` | Enzyme Experiments | Amylase, catalase, pepsin investigations |
| 08 | `08-food-tests.json` | Food Tests | Benedict's, iodine, biuret, emulsion tests |

### Unit 03: Nutrition
**Location:** `generic/biology/content/03-nutrition/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-photosynthesis-overview.json` | Photosynthesis Overview | Word equation, importance, where it occurs |
| 02 | `02-photosynthesis-equation.json` | Photosynthesis Equation | Balanced chemical equation, reactants, products |
| 03 | `03-leaf-structure.json` | Leaf Structure | Adaptations for photosynthesis, cross-section |
| 04 | `04-factors-affecting-photosynthesis.json` | Factors Affecting Photosynthesis | Light, CO2, temperature, limiting factors |
| 05 | `05-uses-of-glucose.json` | Uses of Glucose | Respiration, starch, cellulose, proteins, lipids |
| 06 | `06-balanced-diet.json` | Balanced Diet | Nutrients, food groups, deficiency diseases |
| 07 | `07-digestive-system.json` | The Digestive System | Organs and their functions |
| 08 | `08-mechanical-digestion.json` | Mechanical Digestion | Teeth, chewing, churning, peristalsis |
| 09 | `09-chemical-digestion.json` | Chemical Digestion | Enzymes: amylase, protease, lipase |
| 10 | `10-absorption.json` | Absorption | Villi structure, adaptations, surface area |
| 11 | `11-egestion.json` | Egestion | Large intestine, water absorption, faeces |

### Unit 04: Transport
**Location:** `generic/biology/content/04-transport/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-need-for-transport.json` | The Need for Transport Systems | Surface area to volume ratio, multicellular organisms |
| 02 | `02-circulatory-system.json` | The Circulatory System | Double circulation, systemic and pulmonary |
| 03 | `03-heart-structure.json` | Heart Structure | Chambers, valves, blood vessels |
| 04 | `04-heart-function.json` | Heart Function | Cardiac cycle, heartbeat, pacemaker |
| 05 | `05-blood-vessels.json` | Blood Vessels | Arteries, veins, capillaries - structure and function |
| 06 | `06-blood-composition.json` | Blood Composition | Plasma, red cells, white cells, platelets |
| 07 | `07-red-blood-cells.json` | Red Blood Cells | Adaptations, haemoglobin, oxygen transport |
| 08 | `08-white-blood-cells.json` | White Blood Cells | Phagocytes, lymphocytes, immune response |
| 09 | `09-cardiovascular-disease.json` | Cardiovascular Disease | Coronary heart disease, risk factors, treatments |
| 10 | `10-plant-transport-overview.json` | Plant Transport Overview | Need for transport, xylem and phloem |
| 11 | `11-xylem-and-transpiration.json` | Xylem and Transpiration | Structure, function, transpiration stream |
| 12 | `12-factors-affecting-transpiration.json` | Factors Affecting Transpiration | Light, temperature, humidity, wind |
| 13 | `13-phloem-and-translocation.json` | Phloem and Translocation | Structure, function, source to sink |

### Unit 05: Respiration and Gas Exchange
**Location:** `generic/biology/content/05-respiration/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-respiration-overview.json` | Respiration Overview | Definition, purpose, comparison with breathing |
| 02 | `02-aerobic-respiration.json` | Aerobic Respiration | Equation, location in cell, ATP production |
| 03 | `03-anaerobic-respiration.json` | Anaerobic Respiration | In humans (lactic acid), in yeast (fermentation) |
| 04 | `04-comparing-respiration-types.json` | Comparing Aerobic and Anaerobic | Energy yield, oxygen requirement, products |
| 05 | `05-exercise-and-respiration.json` | Exercise and Respiration | Oxygen debt, breathing rate, heart rate changes |
| 06 | `06-gas-exchange-overview.json` | Gas Exchange Overview | Purpose, requirements for efficient exchange |
| 07 | `07-lungs-structure.json` | Structure of the Lungs | Trachea, bronchi, bronchioles, alveoli |
| 08 | `08-alveoli-adaptations.json` | Alveoli Adaptations | Surface area, thin walls, blood supply, ventilation |
| 09 | `09-breathing-mechanism.json` | Breathing Mechanism | Inhalation, exhalation, diaphragm, intercostal muscles |

### Unit 06: Excretion
**Location:** `generic/biology/content/06-excretion/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-excretion-overview.json` | Excretion Overview | Definition, waste products, excretory organs |
| 02 | `02-kidney-structure.json` | Kidney Structure | Cortex, medulla, pelvis, ureter |
| 03 | `03-nephron-structure.json` | Nephron Structure | Bowman's capsule, tubules, loop of Henle |
| 04 | `04-kidney-function.json` | Kidney Function | Filtration, reabsorption, secretion |
| 05 | `05-urine-formation.json` | Urine Formation | What is filtered, reabsorbed, excreted |
| 06 | `06-kidney-failure.json` | Kidney Failure | Dialysis, transplants, treatment options |

### Unit 07: Coordination and Homeostasis
**Location:** `generic/biology/content/07-coordination/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-homeostasis-introduction.json` | Introduction to Homeostasis | Definition, importance, negative feedback |
| 02 | `02-nervous-system-overview.json` | Nervous System Overview | CNS, PNS, neurons |
| 03 | `03-neurone-structure.json` | Neurone Structure | Sensory, relay, motor neurons |
| 04 | `04-nerve-impulses.json` | Nerve Impulses | Electrical signals, synapses, neurotransmitters |
| 05 | `05-reflex-arcs.json` | Reflex Arcs | Components, pathway, importance |
| 06 | `06-the-eye.json` | The Eye | Structure, function, focusing |
| 07 | `07-eye-defects.json` | Eye Defects | Long/short sight, colour blindness, corrections |
| 08 | `08-endocrine-system.json` | The Endocrine System | Glands, hormones, comparison with nervous system |
| 09 | `09-hormones-overview.json` | Key Hormones | Insulin, glucagon, adrenaline, thyroxine |
| 10 | `10-blood-glucose-control.json` | Blood Glucose Control | Insulin, glucagon, negative feedback |
| 11 | `11-diabetes.json` | Diabetes | Type 1 vs Type 2, symptoms, treatments |
| 12 | `12-body-temperature.json` | Body Temperature Regulation | Thermoregulation, sweating, shivering, vasodilation |
| 13 | `13-menstrual-cycle.json` | The Menstrual Cycle | FSH, LH, oestrogen, progesterone |
| 14 | `14-contraception.json` | Contraception | Hormonal, barrier, surgical methods |
| 15 | `15-plant-hormones.json` | Plant Hormones | Auxins, phototropism, gravitropism |
| 16 | `16-uses-of-plant-hormones.json` | Uses of Plant Hormones | Rooting powder, weedkillers, fruit ripening |

### Unit 08: Reproduction
**Location:** `generic/biology/content/08-reproduction/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-types-of-reproduction.json` | Types of Reproduction | Sexual vs asexual, advantages/disadvantages |
| 02 | `02-asexual-reproduction.json` | Asexual Reproduction | Binary fission, budding, runners, bulbs |
| 03 | `03-meiosis.json` | Meiosis | Stages, halving chromosome number, genetic variation |
| 04 | `04-comparing-mitosis-meiosis.json` | Comparing Mitosis and Meiosis | Purpose, number of divisions, offspring |
| 05 | `05-plant-reproduction.json` | Plant Reproduction | Flower structure, pollination, fertilisation |
| 06 | `06-seed-dispersal.json` | Seed Dispersal | Methods: wind, animal, water, explosion |
| 07 | `07-male-reproductive-system.json` | Male Reproductive System | Structure and function |
| 08 | `08-female-reproductive-system.json` | Female Reproductive System | Structure and function |
| 09 | `09-fertilisation.json` | Fertilisation | Sperm meets egg, zygote formation |
| 10 | `10-pregnancy.json` | Pregnancy | Implantation, placenta, development |
| 11 | `11-birth.json` | Birth | Labour, delivery, hormonal control |

### Unit 09: Inheritance and Evolution
**Location:** `generic/biology/content/09-inheritance/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-dna-structure.json` | DNA Structure | Double helix, nucleotides, base pairing |
| 02 | `02-genes-and-chromosomes.json` | Genes and Chromosomes | Definitions, human chromosome number |
| 03 | `03-protein-synthesis.json` | Protein Synthesis | Transcription, translation (overview) |
| 04 | `04-genetic-terminology.json` | Genetic Terminology | Allele, genotype, phenotype, dominant, recessive |
| 05 | `05-monohybrid-inheritance.json` | Monohybrid Inheritance | Single gene crosses, Punnett squares |
| 06 | `06-genetic-diagrams.json` | Genetic Diagrams | Drawing and interpreting crosses |
| 07 | `07-sex-determination.json` | Sex Determination | XX and XY chromosomes, inheritance of sex |
| 08 | `08-inherited-disorders.json` | Inherited Disorders | Cystic fibrosis, polydactyly, sickle cell |
| 09 | `09-variation.json` | Variation | Genetic vs environmental, continuous vs discontinuous |
| 10 | `10-mutations.json` | Mutations | Types, causes, effects |
| 11 | `11-evolution-theory.json` | Theory of Evolution | Darwin, natural selection, evidence |
| 12 | `12-natural-selection.json` | Natural Selection | Mechanism, examples (antibiotic resistance) |
| 13 | `13-selective-breeding.json` | Selective Breeding | Process, examples, advantages/disadvantages |
| 14 | `14-genetic-engineering.json` | Genetic Engineering | Process, examples, applications |
| 15 | `15-cloning.json` | Cloning | Natural, artificial, Dolly the sheep |
| 16 | `16-classification.json` | Classification | Kingdoms, domains, binomial nomenclature |

### Unit 10: Ecology
**Location:** `generic/biology/content/10-ecology/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-ecosystems.json` | Ecosystems | Definitions: population, community, habitat, ecosystem |
| 02 | `02-abiotic-factors.json` | Abiotic Factors | Light, temperature, water, pH, CO2 |
| 03 | `03-biotic-factors.json` | Biotic Factors | Competition, predation, disease |
| 04 | `04-adaptations.json` | Adaptations | Structural, behavioural, physiological |
| 05 | `05-food-chains.json` | Food Chains | Producers, consumers, trophic levels |
| 06 | `06-food-webs.json` | Food Webs | Interconnected food chains, ecosystem stability |
| 07 | `07-energy-transfer.json` | Energy Transfer | Pyramids of number, biomass, energy |
| 08 | `08-carbon-cycle.json` | The Carbon Cycle | Photosynthesis, respiration, decomposition, combustion |
| 09 | `09-nitrogen-cycle.json` | The Nitrogen Cycle | Nitrogen fixation, nitrification, denitrification |
| 10 | `10-water-cycle.json` | The Water Cycle | Evaporation, condensation, precipitation |
| 11 | `11-sampling-techniques.json` | Sampling Techniques | Quadrats, transects, random sampling |
| 12 | `12-biodiversity.json` | Biodiversity | Definition, importance, measurement |
| 13 | `13-human-impact.json` | Human Impact on Environment | Pollution, deforestation, global warming |
| 14 | `14-conservation.json` | Conservation | Methods, sustainability, protecting biodiversity |

---

## 1.4 Biology Content Quality Standards

### Scientific Accuracy Requirements
- All equations must balance chemically
- Use correct biological terminology consistently
- Cite syllabus-specific command words
- Include current scientific understanding (e.g., updated ATP yield values)

### Diagram Requirements (For Future Integration)
Every lesson should note required diagrams. Priority diagrams include:

**Cells Unit:**
- Animal cell structure (labelled)
- Plant cell structure (labelled)
- Comparison table
- Microscopy images
- Stages of mitosis

**Transport Unit:**
- Heart cross-section
- Circulatory system overview
- Blood vessel cross-sections
- Xylem and phloem structure

**Inheritance Unit:**
- DNA double helix
- Chromosome structure
- Punnett square examples
- Genetic diagram format

### Required Practical Content
Include guidance for required practicals:

| Practical | Unit | Key Points |
|-----------|------|------------|
| Microscopy | 01 | Using microscopes, calculating magnification |
| Osmosis investigation | 01 | Potato cylinders, mass change |
| Enzyme rate | 02 | Effect of temperature/pH on enzyme activity |
| Photosynthesis rate | 03 | Light intensity, CO2, pondweed |
| Food tests | 02 | Benedict's, iodine, biuret, emulsion |
| Heart dissection | 04 | Identifying structures |
| Sampling | 10 | Quadrats, random sampling, population estimates |

---

## 1.5 Biology Development Prioritization

### Phase 1: Foundation Topics (High Exam Weight)
1. **Unit 01: Cells** - Fundamental to all biology
2. **Unit 09: Inheritance and Evolution** - Heavy exam weighting
3. **Unit 07: Coordination and Homeostasis** - Complex, needs thorough coverage

### Phase 2: Life Processes
4. **Unit 03: Nutrition** - Photosynthesis and digestion
5. **Unit 04: Transport** - Heart, blood, plant transport
6. **Unit 05: Respiration** - Core metabolic process

### Phase 3: Advanced Topics
7. **Unit 02: Biological Molecules** - Enzymes focus
8. **Unit 08: Reproduction** - Human and plant
9. **Unit 06: Excretion** - Often assessed with homeostasis

### Phase 4: Ecology
10. **Unit 10: Ecology** - Often Paper 2 focus

---

## 1.6 Estimated Effort for Generic Biology

| Phase | Units | Est. Lessons | Est. Hours* |
|-------|-------|--------------|-------------|
| Phase 1 | 3 | 45 | 70-90 |
| Phase 2 | 3 | 33 | 50-65 |
| Phase 3 | 3 | 25 | 40-50 |
| Phase 4 | 1 | 14 | 20-28 |
| **Total** | **10** | **117** | **180-233** |

*Estimated 1.5-2 hours per lesson including research, writing, and review

---

# Part 2: Cross-Subject Scaling Strategy

## 2.1 Overview: Physics as the Template

Generic Physics serves as the **reference implementation** for all course development. The structure, standards, and workflows established for Physics should be applied consistently across all subjects.

### Core Principles
1. **Consistency:** All courses follow identical JSON structure and content patterns
2. **Quality:** Same quality standards apply across all subjects
3. **Mapping:** All generic courses map to the same 4 exam boards
4. **Scalability:** Board-specific courses derive from generic content

---

## 2.2 Creating Generic Chemistry

### Apply Physics Template

| Physics Element | Chemistry Equivalent |
|-----------------|---------------------|
| Equations (F=ma) | Chemical equations, moles calculations |
| Units (N, m/s²) | Units (mol, g/dm³, mol/dm³) |
| Diagrams (circuits) | Diagrams (apparatus, structures) |
| Practical focus | Strong practical focus |

### Chemistry-Specific Standards

#### Chemical Equations
Use mhchem-style LaTeX where supported, or plain text with subscripts:

```markdown
**Balanced equation:**
$$\text{2Mg} + \text{O}_2 \rightarrow \text{2MgO}$$

**Ionic equation:**
$$\text{Mg}^{2+}(aq) + \text{2OH}^-(aq) \rightarrow \text{Mg(OH)}_2(s)$$
```

#### Structure Diagrams
Note required structure diagrams:
```markdown
[STRUCTURE: Dot-and-cross diagram for sodium chloride]
[STRUCTURE: Displayed formula for ethanol C₂H₅OH]
[APPARATUS: Setup for fractional distillation]
```

#### Moles Calculations
Include clear step-by-step calculation methods:

```markdown
**Worked Example: Calculate moles**

Given: Mass = 24g, Mr of Mg = 24

$$\text{moles} = \frac{\text{mass}}{\text{Mr}} = \frac{24}{24} = 1 \text{ mol}$$
```

### Chemistry Unit Mapping (from syllabus map)

| Unit | Title | Est. Lessons |
|------|-------|--------------|
| 01 | Atomic Structure | 8-10 |
| 02 | Bonding and Structure | 10-12 |
| 03 | Quantitative Chemistry | 8-10 |
| 04 | Chemical Changes | 8-10 |
| 05 | Chemical Energetics | 6-8 |
| 06 | Rates and Equilibrium | 6-8 |
| 07 | Acids, Bases and Salts | 8-10 |
| 08 | The Periodic Table | 8-10 |
| 09 | Organic Chemistry | 10-12 |
| 10 | Environmental Chemistry | 6-8 |
| **Total** | | **78-98** |

### Chemistry Content Template

```markdown
# [Topic Title]

## Learning Objectives
- [Objective 1]
- [Objective 2]

## Key Concepts

### [Concept]
[Explanation]

## Chemical Equations
[Relevant equations with explanations]

## Calculations
[Worked examples with clear steps]

## Practical Application
[Laboratory context and safety considerations]

## Exam Tips
[Command words, common question types]

## Practice Questions
1. [Recall question]
2. [Calculation question]
3. [Extended response question]

## Key Terms
| Term | Definition |
|------|------------|
```

---

## 2.3 Creating Generic Mathematics

### Apply Physics Template with Adaptations

Mathematics requires the most significant adaptation from the Physics template due to its problem-solving nature.

### Maths-Specific Standards

#### Worked Examples (Critical)
Maths lessons require extensive worked examples:

```markdown
## Worked Example 1

**Solve:** $2x + 5 = 13$

**Solution:**
$$2x + 5 = 13$$
$$2x = 13 - 5$$
$$2x = 8$$
$$x = 4$$

**Check:** $2(4) + 5 = 8 + 5 = 13$ ✓
```

#### Tier Differentiation
Mark content as Foundation/Higher where applicable:

```markdown
## Quadratic Formula (Higher Tier)

For $ax^2 + bx + c = 0$:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
```

#### Graph Descriptions
Mark required graphs:

```markdown
[GRAPH: y = x² showing parabola with vertex at origin]
[GRAPH: Linear graph showing y = 2x + 1 with gradient and intercept marked]
```

### Maths Unit Mapping (from syllabus map)

| Unit | Title | Est. Lessons |
|------|-------|--------------|
| 01 | Number | 12-14 |
| 02 | Algebra | 14-16 |
| 03 | Graphs | 10-12 |
| 04 | Geometry | 12-14 |
| 05 | Mensuration | 8-10 |
| 06 | Trigonometry | 10-12 |
| 07 | Vectors and Transformations | 8-10 |
| 08 | Probability | 8-10 |
| 09 | Statistics | 10-12 |
| **Total** | | **92-110** |

### Maths Content Template

```markdown
# [Topic Title]

## Learning Objectives
- [Objective 1]
- [Objective 2]

## Introduction
[Brief context and real-world relevance]

## Key Concepts

### Method/Formula
[Clear statement of method or formula]

## Worked Examples

### Example 1 (Foundation)
**Question:** [Problem]

**Solution:**
[Step-by-step working]

### Example 2 (Higher)
**Question:** [More challenging problem]

**Solution:**
[Step-by-step working]

## Common Mistakes to Avoid
- [Mistake 1 and how to avoid it]
- [Mistake 2 and how to avoid it]

## Practice Questions

### Foundation Level
1. [Question]
2. [Question]

### Higher Level
3. [Question]
4. [Question]

## Summary
- [Key formula/method]
- [When to use it]
```

---

## 2.4 Creating Board-Specific Courses

### Strategy: Adapt, Don't Rebuild

Board-specific courses should **reference and adapt** generic content, not duplicate it entirely.

### Adaptation Process

#### Step 1: Content Mapping
For each generic unit, identify:
- Which board sections it covers
- Any board-specific content needed
- Any content to exclude for that board

#### Step 2: Terminology Alignment
Adjust terminology to match specification language:

| Generic Term | AQA | Cambridge | Edexcel |
|--------------|-----|-----------|---------|
| "Equation of motion" | "SUVAT equations" | "Kinematic equations" | "Equations of motion" |
| "Active transport" | Same | Same | Same |
| "Fractional distillation" | Same | "Separating crude oil" | Same |

#### Step 3: Add Board-Specific Content

**AQA GCSE:**
- Required Practical guidance
- Triple Science only content marked
- 6-mark question practice

**Cambridge IGCSE:**
- Core/Extended differentiation
- Alternative to Practical guidance
- Paper 1/2 focus areas

**Edexcel GCSE:**
- Core Practical guidance
- Higher Tier content marked
- Multiple choice practice

**Edexcel IGCSE:**
- Specific practical content
- International context examples

### Board Adaptation Template

```json
{
  "title": "Newton's Laws of Motion",
  "baseContent": "generic/physics/content/01-forces-and-motion/10-newtons-first-law.json",
  "boardAdditions": {
    "requiredPractical": "Investigate the effect of varying force on the acceleration of an object of constant mass",
    "examTips": [
      "AQA often asks you to describe an experiment to investigate F=ma",
      "Common 6-mark question: Explain how a car's braking distance depends on speed"
    ],
    "commonQuestions": [
      "Calculate the force needed to...",
      "Explain why an object accelerates when..."
    ]
  },
  "contentModifications": {
    "removeSection": null,
    "addSection": "### Required Practical\n[Content]"
  },
  "order": 10
}
```

---

## 2.5 Unified Development Workflow

### For Any New Course

```
┌──────────────────────────────────────────────────────────────┐
│                    COURSE DEVELOPMENT WORKFLOW                │
└──────────────────────────────────────────────────────────────┘

1. SETUP PHASE
   ├── Create course directory structure
   ├── Copy _course.json template
   ├── Create _unit.json files for all units
   └── Verify syllabus mapping exists

2. PLANNING PHASE
   ├── Map syllabus to topics (use _syllabus_map.json)
   ├── Create ordered list of lessons per unit
   ├── Identify priority order based on exam weighting
   └── Note required diagrams/practicals

3. CONTENT CREATION PHASE (Per Lesson)
   ├── Research topic thoroughly
   │   ├── Consult specification documents
   │   ├── Review examiner reports
   │   └── Check textbook treatments
   ├── Write content using subject template
   │   ├── Apply markdown/LaTeX standards
   │   ├── Include worked examples
   │   └── Add practice questions
   └── Mark diagram placeholders

4. QUALITY ASSURANCE PHASE (Per Lesson)
   ├── Technical accuracy review
   │   ├── Equations correct
   │   ├── Terminology accurate
   │   └── Content factually correct
   ├── Syllabus coverage check
   │   ├── All spec points addressed
   │   └── Command words used appropriately
   ├── Format validation
   │   ├── JSON valid
   │   ├── LaTeX renders correctly
   │   └── Markdown formatted properly
   └── Readability assessment
       ├── Appropriate for age 14-16
       ├── Clear explanations
       └── Logical progression

5. INTEGRATION PHASE
   ├── Verify order numbers correct
   ├── Cross-reference related topics
   ├── Update syllabus mapping if needed
   └── Final course-level review

6. BOARD ADAPTATION PHASE (If applicable)
   ├── Copy generic content
   ├── Apply terminology adjustments
   ├── Add board-specific content
   ├── Remove non-applicable content
   └── Quality review adapted content
```

---

## 2.6 Resource Estimates Summary

### All Subjects Overview

| Subject | Generic Lessons | Board Adaptations | Total Lessons | Est. Hours |
|---------|-----------------|-------------------|---------------|------------|
| Physics | 85 | 225 | 310 | 245-330 |
| Biology | 117 | 300 | 417 | 330-440 |
| Chemistry | 88 | 230 | 318 | 250-340 |
| Mathematics | 101 | 260 | 361 | 285-380 |
| **TOTAL** | **391** | **1,015** | **1,406** | **1,110-1,490** |

### Development Order Recommendation

```
RECOMMENDED SEQUENCE
────────────────────
Phase 1: Generic Physics (Reference Implementation)
    └── Establishes patterns, standards, templates

Phase 2: Physics Board Adaptations
    └── Validates adaptation process

Phase 3: Generic Biology
    └── Applies Physics template to second science

Phase 4: Generic Chemistry
    └── Completes science subjects

Phase 5: Biology + Chemistry Adaptations
    └── All sciences complete

Phase 6: Generic Mathematics
    └── Applies template to non-science subject

Phase 7: Mathematics Adaptations
    └── All 20 courses complete
```

---

## 2.7 Quality Checklist (All Subjects)

### Per Lesson Checklist

```markdown
## Content Quality
- [ ] Title matches syllabus terminology
- [ ] Learning objectives clearly stated
- [ ] All key concepts from spec covered
- [ ] Explanations are clear and age-appropriate
- [ ] Real-world applications included

## Technical Quality
- [ ] JSON is valid
- [ ] LaTeX equations render correctly
- [ ] All variables defined with units
- [ ] Markdown formatting correct
- [ ] Order number is correct

## Subject-Specific
### Science (Physics/Chemistry/Biology)
- [ ] Equations are balanced/correct
- [ ] Safety considerations mentioned where relevant
- [ ] Practical applications noted
- [ ] Diagrams marked where needed

### Mathematics
- [ ] Multiple worked examples included
- [ ] Foundation/Higher clearly marked
- [ ] Common mistakes addressed
- [ ] Method clearly explained
- [ ] Check/verify steps shown

## Assessment
- [ ] At least 3 practice questions
- [ ] Questions range from recall to application
- [ ] Extended response question included
- [ ] Mark scheme guidance (if applicable)
```

---

## 2.8 Tools and Resources by Subject

### All Subjects
- **JSON Validator:** https://jsonlint.com/
- **LaTeX Tester:** https://www.overleaf.com/
- **Markdown Preview:** VS Code

### Physics
- AQA 8463 Spec: https://www.aqa.org.uk/subjects/science/gcse/physics-8463
- Practical handbook guidance

### Biology
- AQA 8461 Spec: https://www.aqa.org.uk/subjects/science/gcse/biology-8461
- Required practical guides
- Biological terminology glossaries

### Chemistry
- AQA 8462 Spec: https://www.aqa.org.uk/subjects/science/gcse/chemistry-8462
- Periodic table reference
- Equation balancing tools

### Mathematics
- AQA 8300 Spec: https://www.aqa.org.uk/subjects/mathematics/gcse/mathematics-8300
- Graph plotting tools
- Mathematical notation guides

---

# Appendices

## Appendix A: Sample Biology Lesson (Complete)

**File:** `generic/biology/content/01-cells/08-mitosis.json`

```json
{
  "title": "Mitosis",
  "content": "# Mitosis\n\n## Learning Objectives\nBy the end of this lesson, you should be able to:\n- Define mitosis and explain its purpose\n- Describe the stages of mitosis\n- Explain the importance of mitosis for growth and repair\n\n## Introduction\n\n**Mitosis** is a type of cell division that produces two genetically identical daughter cells from one parent cell. It is essential for growth, repair, and asexual reproduction in organisms.\n\n## Why Do Cells Divide?\n\nCells divide for three main reasons:\n\n1. **Growth** - Organisms grow by producing more cells\n2. **Repair** - Damaged tissues are replaced by new cells\n3. **Asexual reproduction** - Some organisms reproduce by mitosis alone\n\n## The Cell Cycle\n\nBefore mitosis occurs, the cell goes through a preparation phase called **interphase**:\n\n1. **G1 phase** - Cell grows and carries out normal functions\n2. **S phase** - DNA replicates (copies itself)\n3. **G2 phase** - Cell checks DNA and prepares for division\n\n[DIAGRAM: The cell cycle showing interphase and mitosis]\n\n## Stages of Mitosis\n\nMitosis has four main stages:\n\n### 1. Prophase\n- Chromosomes condense and become visible\n- Nuclear membrane breaks down\n- Spindle fibres form\n\n### 2. Metaphase\n- Chromosomes line up along the middle (equator) of the cell\n- Spindle fibres attach to chromosomes at the centromere\n\n### 3. Anaphase\n- Sister chromatids separate\n- Spindle fibres pull chromatids to opposite poles\n- Cell begins to elongate\n\n### 4. Telophase\n- Chromatids reach opposite poles\n- Nuclear membranes reform around each set\n- Chromosomes decondense\n\n[DIAGRAM: Four stages of mitosis in an animal cell]\n\n## Cytokinesis\n\nAfter mitosis, the cytoplasm divides in a process called **cytokinesis**:\n\n- In **animal cells**: The cell membrane pinches inward\n- In **plant cells**: A new cell wall forms down the middle\n\n## Key Points About Mitosis\n\n| Feature | Detail |\n|---------|--------|\n| Number of divisions | 1 |\n| Daughter cells produced | 2 |\n| Chromosome number | Same as parent (diploid) |\n| Genetic variation | None - identical copies |\n| Purpose | Growth, repair, asexual reproduction |\n\n## Importance of Mitosis\n\n### For Growth\nWhen you grow from a baby to an adult, your body produces trillions of new cells through mitosis. Each new cell is genetically identical, ensuring your body develops correctly.\n\n### For Repair\nWhen you cut your skin, cells around the wound divide by mitosis to produce new cells that heal the wound. The new cells are identical to the original skin cells.\n\n### For Asexual Reproduction\nOrganisms like bacteria, yeast, and strawberry plants can reproduce using mitosis. The offspring are genetically identical clones of the parent.\n\n## Common Misconceptions\n\n- **Misconception:** Mitosis and cell division are the same thing\n- **Reality:** Mitosis is the division of the nucleus; cytokinesis is the division of the whole cell\n\n- **Misconception:** Mitosis produces variation\n- **Reality:** Mitosis produces genetically identical cells; only meiosis produces genetic variation\n\n## Practice Questions\n\n1. State the number of daughter cells produced by mitosis. (1 mark)\n\n2. Name the stage of mitosis where chromosomes line up in the middle of the cell. (1 mark)\n\n3. Explain why mitosis is important for wound healing. (2 marks)\n\n4. A human body cell has 46 chromosomes. How many chromosomes will be in each daughter cell after mitosis? Explain your answer. (3 marks)\n\n5. Describe the stages of mitosis. (6 marks)\n\n## Key Terms Glossary\n\n| Term | Definition |\n|------|------------|\n| Mitosis | Cell division producing two genetically identical daughter cells |\n| Interphase | Stage before mitosis where DNA replicates |\n| Chromosome | Structure made of DNA carrying genetic information |\n| Sister chromatids | Two identical copies of a chromosome joined at the centromere |\n| Cytokinesis | Division of the cytoplasm after mitosis |\n\n## Summary\n\n- Mitosis produces two genetically identical daughter cells\n- It occurs in four stages: prophase, metaphase, anaphase, telophase\n- DNA replicates during interphase before mitosis begins\n- Mitosis is essential for growth, repair, and asexual reproduction\n- The chromosome number stays the same after mitosis",
  "order": 8
}
```

---

## Appendix B: Sample Chemistry Lesson (Complete)

**File:** `generic/chemistry/content/03-quantitative-chemistry/02-moles.json`

```json
{
  "title": "The Mole Concept",
  "content": "# The Mole Concept\n\n## Learning Objectives\nBy the end of this lesson, you should be able to:\n- Define the mole and Avogadro's constant\n- Calculate the number of moles from mass and molar mass\n- Convert between moles, mass, and number of particles\n\n## Introduction\n\nChemists need a way to count atoms and molecules, which are far too small to count individually. The **mole** is the unit chemists use to measure amounts of substances.\n\n## What is a Mole?\n\nA **mole** (mol) is the amount of substance that contains exactly $6.02 \\times 10^{23}$ particles.\n\nThis number is called **Avogadro's constant** ($N_A$).\n\n$$N_A = 6.02 \\times 10^{23} \\text{ mol}^{-1}$$\n\n### Why This Number?\n\nOne mole of any substance contains the same number of particles as there are atoms in exactly 12 g of carbon-12.\n\n## Molar Mass\n\nThe **molar mass** ($M$) is the mass of one mole of a substance, measured in g/mol.\n\nFor elements: Molar mass = Relative atomic mass (in g/mol)\nFor compounds: Molar mass = Relative formula mass (in g/mol)\n\n**Examples:**\n- Carbon: $M = 12$ g/mol\n- Oxygen gas ($\\text{O}_2$): $M = 32$ g/mol\n- Water ($\\text{H}_2\\text{O}$): $M = 18$ g/mol\n- Sodium chloride ($\\text{NaCl}$): $M = 58.5$ g/mol\n\n## The Mole Equation\n\nThe key equation relating moles, mass, and molar mass is:\n\n$$n = \\frac{m}{M}$$\n\nWhere:\n- $n$ = number of moles (mol)\n- $m$ = mass (g)\n- $M$ = molar mass (g/mol)\n\n### Rearranging the Equation\n\n**To find mass:**\n$$m = n \\times M$$\n\n**To find molar mass:**\n$$M = \\frac{m}{n}$$\n\n## Worked Examples\n\n### Example 1: Calculate moles from mass\n**Question:** Calculate the number of moles in 48 g of magnesium. ($A_r$ of Mg = 24)\n\n**Solution:**\n$$n = \\frac{m}{M} = \\frac{48}{24} = 2 \\text{ mol}$$\n\n### Example 2: Calculate mass from moles\n**Question:** Calculate the mass of 0.5 mol of sodium chloride. ($M_r$ of NaCl = 58.5)\n\n**Solution:**\n$$m = n \\times M = 0.5 \\times 58.5 = 29.25 \\text{ g}$$\n\n### Example 3: Calculate moles of a compound\n**Question:** Calculate the number of moles in 9 g of water. ($M_r$ of $\\text{H}_2\\text{O}$ = 18)\n\n**Solution:**\n$$n = \\frac{m}{M} = \\frac{9}{18} = 0.5 \\text{ mol}$$\n\n## Number of Particles\n\nTo find the number of particles:\n\n$$\\text{Number of particles} = n \\times N_A$$\n\n### Example 4: Calculate number of molecules\n**Question:** How many molecules are in 2 mol of water?\n\n**Solution:**\n$$\\text{Number of molecules} = 2 \\times 6.02 \\times 10^{23}$$\n$$= 1.204 \\times 10^{24} \\text{ molecules}$$\n\n## Triangle Method\n\nUse this triangle to remember the relationships:\n\n```\n      m\n    ─────\n    n × M\n```\n\nCover what you want to find:\n- Cover $n$: $n = m ÷ M$\n- Cover $m$: $m = n × M$\n- Cover $M$: $M = m ÷ n$\n\n## Common Mistakes to Avoid\n\n1. **Forgetting units:** Always include units in your answer\n2. **Using atomic mass for compounds:** Remember to calculate $M_r$ first\n3. **Incorrect formula for $M_r$:** Don't forget subscripts (e.g., $\\text{H}_2\\text{O}$ has 2 H atoms)\n\n## Practice Questions\n\n1. Calculate the number of moles in 56 g of iron. ($A_r$ of Fe = 56) (2 marks)\n\n2. Calculate the mass of 3 mol of carbon dioxide. ($M_r$ of $\\text{CO}_2$ = 44) (2 marks)\n\n3. Calculate the number of moles in 4.9 g of sulfuric acid, $\\text{H}_2\\text{SO}_4$. ($M_r$ = 98) (2 marks)\n\n4. How many molecules are present in 0.25 mol of oxygen gas? (2 marks)\n\n5. Calculate the mass of sodium hydroxide (NaOH) that contains $3.01 \\times 10^{23}$ formula units. ($M_r$ of NaOH = 40) (3 marks)\n\n## Key Terms\n\n| Term | Definition |\n|------|------------|\n| Mole | Amount of substance containing $6.02 \\times 10^{23}$ particles |\n| Avogadro's constant | $6.02 \\times 10^{23}$ mol$^{-1}$ |\n| Molar mass | Mass of one mole of a substance (g/mol) |\n\n## Summary\n\n- One mole contains $6.02 \\times 10^{23}$ particles (Avogadro's constant)\n- Molar mass (g/mol) = relative atomic/formula mass\n- Key equation: $n = \\frac{m}{M}$\n- Number of particles = $n \\times N_A$",
  "order": 2
}
```

---

## Appendix C: Sample Maths Lesson (Complete)

**File:** `generic/maths/content/02-algebra/05-solving-linear-equations.json`

```json
{
  "title": "Solving Linear Equations",
  "content": "# Solving Linear Equations\n\n## Learning Objectives\nBy the end of this lesson, you should be able to:\n- Solve one-step and two-step linear equations\n- Solve equations with the unknown on both sides\n- Solve equations involving brackets\n\n## Introduction\n\nA **linear equation** contains a variable (usually $x$) raised to the power of 1. Solving an equation means finding the value of $x$ that makes the equation true.\n\n## Key Principle: Balance\n\nWhatever you do to one side of an equation, you must do to the other side to keep it balanced.\n\n## One-Step Equations\n\n### Addition/Subtraction\n\n**Example 1:** Solve $x + 5 = 12$\n\n**Solution:**\n$$x + 5 = 12$$\n$$x + 5 - 5 = 12 - 5$$\n$$x = 7$$\n\n**Check:** $7 + 5 = 12$ ✓\n\n**Example 2:** Solve $x - 3 = 8$\n\n**Solution:**\n$$x - 3 = 8$$\n$$x - 3 + 3 = 8 + 3$$\n$$x = 11$$\n\n### Multiplication/Division\n\n**Example 3:** Solve $4x = 20$\n\n**Solution:**\n$$4x = 20$$\n$$\\frac{4x}{4} = \\frac{20}{4}$$\n$$x = 5$$\n\n**Example 4:** Solve $\\frac{x}{3} = 7$\n\n**Solution:**\n$$\\frac{x}{3} = 7$$\n$$\\frac{x}{3} \\times 3 = 7 \\times 3$$\n$$x = 21$$\n\n## Two-Step Equations\n\nFor two-step equations, use inverse operations in reverse order (BODMAS backwards).\n\n**Example 5:** Solve $2x + 3 = 11$\n\n**Solution:**\nStep 1: Subtract 3 from both sides\n$$2x + 3 - 3 = 11 - 3$$\n$$2x = 8$$\n\nStep 2: Divide both sides by 2\n$$\\frac{2x}{2} = \\frac{8}{2}$$\n$$x = 4$$\n\n**Check:** $2(4) + 3 = 8 + 3 = 11$ ✓\n\n**Example 6:** Solve $\\frac{x - 4}{2} = 5$\n\n**Solution:**\nStep 1: Multiply both sides by 2\n$$x - 4 = 10$$\n\nStep 2: Add 4 to both sides\n$$x = 14$$\n\n## Equations with Unknown on Both Sides\n\nCollect the $x$ terms on one side and numbers on the other.\n\n**Example 7:** Solve $5x + 2 = 3x + 10$\n\n**Solution:**\nStep 1: Subtract $3x$ from both sides\n$$5x - 3x + 2 = 10$$\n$$2x + 2 = 10$$\n\nStep 2: Subtract 2 from both sides\n$$2x = 8$$\n\nStep 3: Divide by 2\n$$x = 4$$\n\n**Check:** LHS = $5(4) + 2 = 22$, RHS = $3(4) + 10 = 22$ ✓\n\n## Equations with Brackets\n\nExpand brackets first, then solve.\n\n**Example 8:** Solve $3(x + 2) = 15$\n\n**Solution:**\nStep 1: Expand brackets\n$$3x + 6 = 15$$\n\nStep 2: Subtract 6\n$$3x = 9$$\n\nStep 3: Divide by 3\n$$x = 3$$\n\n**Example 9 (Higher):** Solve $2(3x - 1) = 4(x + 3)$\n\n**Solution:**\nStep 1: Expand brackets on both sides\n$$6x - 2 = 4x + 12$$\n\nStep 2: Subtract $4x$\n$$2x - 2 = 12$$\n\nStep 3: Add 2\n$$2x = 14$$\n\nStep 4: Divide by 2\n$$x = 7$$\n\n## Equations with Negative Solutions\n\n**Example 10:** Solve $2x + 7 = 3$\n\n**Solution:**\n$$2x + 7 = 3$$\n$$2x = 3 - 7$$\n$$2x = -4$$\n$$x = -2$$\n\n## Common Mistakes to Avoid\n\n1. **Sign errors:** Be careful with negative numbers\n2. **Forgetting to apply to both sides:** Whatever you do to one side, do to the other\n3. **Wrong order of operations:** Undo addition/subtraction before multiplication/division\n4. **Not checking:** Always substitute your answer back in to verify\n\n## Practice Questions\n\n### Foundation Level\n\n1. Solve $x + 7 = 15$\n\n2. Solve $3x = 21$\n\n3. Solve $2x - 5 = 9$\n\n4. Solve $\\frac{x}{4} + 2 = 6$\n\n5. Solve $5x - 3 = 2x + 9$\n\n### Higher Level\n\n6. Solve $4(x - 2) = 20$\n\n7. Solve $3(2x + 1) = 2(x - 5) + 19$\n\n8. Solve $\\frac{2x + 3}{5} = 3$\n\n9. Solve $\\frac{x + 1}{2} = \\frac{x - 3}{4}$\n\n10. Solve $5(x - 1) - 2(x + 3) = 4$\n\n## Method Summary\n\n| Equation Type | Method |\n|---------------|--------|\n| $x + a = b$ | Subtract $a$ |\n| $x - a = b$ | Add $a$ |\n| $ax = b$ | Divide by $a$ |\n| $\\frac{x}{a} = b$ | Multiply by $a$ |\n| $ax + b = c$ | Subtract $b$, then divide by $a$ |\n| Unknown both sides | Collect $x$ terms on one side |\n| Brackets | Expand first |\n\n## Summary\n\n- Use inverse operations to isolate $x$\n- Whatever you do to one side, do to the other\n- For two-step equations, undo addition/subtraction first\n- For equations with $x$ on both sides, collect like terms\n- Always expand brackets before solving\n- Always check your answer by substituting back",
  "order": 5
}
```

---

## Appendix D: Complete Unit Structure Reference

### Biology Units (Generic)
```
generic/biology/content/
├── 01-cells/               (13 lessons)
├── 02-biological-molecules/ (8 lessons)
├── 03-nutrition/           (11 lessons)
├── 04-transport/           (13 lessons)
├── 05-respiration/         (9 lessons)
├── 06-excretion/           (6 lessons)
├── 07-coordination/        (16 lessons)
├── 08-reproduction/        (11 lessons)
├── 09-inheritance/         (16 lessons)
└── 10-ecology/             (14 lessons)
```

### Chemistry Units (Generic)
```
generic/chemistry/content/
├── 01-atomic-structure/        (10 lessons)
├── 02-bonding/                 (12 lessons)
├── 03-quantitative-chemistry/  (10 lessons)
├── 04-chemical-changes/        (10 lessons)
├── 05-energetics/              (8 lessons)
├── 06-rates-and-equilibrium/   (8 lessons)
├── 07-acids-and-bases/         (10 lessons)
├── 08-periodic-table/          (10 lessons)
├── 09-organic-chemistry/       (12 lessons)
└── 10-environment/             (8 lessons)
```

### Mathematics Units (Generic)
```
generic/maths/content/
├── 01-number/                      (14 lessons)
├── 02-algebra/                     (16 lessons)
├── 03-graphs/                      (12 lessons)
├── 04-geometry/                    (14 lessons)
├── 05-mensuration/                 (10 lessons)
├── 06-trigonometry/                (12 lessons)
├── 07-vectors-and-transformations/ (10 lessons)
├── 08-probability/                 (10 lessons)
└── 09-statistics/                  (12 lessons)
```

---

*Document Version: 1.0*
*Created: February 2025*
*Companion to: DEVELOPMENT_PLAN.md*
