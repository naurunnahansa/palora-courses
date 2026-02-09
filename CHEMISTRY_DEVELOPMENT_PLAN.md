# Generic Chemistry Development Plan

## Document Overview

This document provides a comprehensive plan for developing the Generic Chemistry course, including:
1. **Part 1:** Complete Generic Chemistry course specification
2. **Part 2:** Chemistry-specific content standards and conventions
3. **Part 3:** Detailed topic breakdowns for all 10 units
4. **Part 4:** Board adaptation strategy
5. **Part 5:** Cross-subject insights from Chemistry development

---

# Part 1: Generic Chemistry Course Specification

## 1.1 Course Overview

Generic Chemistry is a comprehensive course covering all fundamental chemistry concepts for GCSE/IGCSE level. It maps to AQA (8462), Cambridge (0620), Edexcel GCSE (1CH0), and Edexcel IGCSE (4CH1) specifications.

### Current State
- **Completed:** 0 lessons
- **Existing Structure:** 10 unit directories with `_unit.json` metadata
- **Target:** 95-105 lessons across 10 units

### Unit Structure Overview

| Unit | Title | Syllabus Focus | Est. Lessons |
|------|-------|----------------|--------------|
| 01 | Atomic Structure | Atoms, elements, periodic table | 10-12 |
| 02 | Bonding and Structure | Ionic, covalent, metallic bonding | 12-14 |
| 03 | Quantitative Chemistry | Moles, equations, calculations | 10-12 |
| 04 | Chemical Changes | Reactivity, extraction, electrolysis | 10-12 |
| 05 | Chemical Energetics | Exo/endothermic, bond energies | 6-8 |
| 06 | Rates and Equilibrium | Reaction rates, catalysts, equilibrium | 8-10 |
| 07 | Acids, Bases and Salts | pH, neutralisation, salt preparation | 10-12 |
| 08 | The Periodic Table | Groups 1, 7, 0, transition metals | 10-12 |
| 09 | Organic Chemistry | Hydrocarbons, functional groups, polymers | 12-14 |
| 10 | Environmental Chemistry | Atmosphere, water, pollution | 6-8 |

**Total Estimated Lessons: 94-114**

---

## 1.2 Chemistry Exam Board Mapping

### AQA GCSE Chemistry (8462)
- **Papers:** 2 papers (1h 45m each)
- **Focus Areas:** Quantitative chemistry, organic chemistry
- **Special Content:** Chemistry-only topics clearly marked
- **Required Practicals:** 8 practicals

### Cambridge IGCSE Chemistry (0620)
- **Papers:** Paper 1 (MCQ), Paper 2 (Theory), Paper 3/4 (Practical)
- **Focus Areas:** Stoichiometry, organic chemistry depth
- **Core/Extended:** Clear differentiation required

### Edexcel GCSE Chemistry (1CH0)
- **Papers:** 2 papers (1h 45m each)
- **Focus Areas:** Earth science integration
- **Core Practicals:** 16 practicals
- **Higher/Foundation:** Tier differentiation

### Edexcel IGCSE Chemistry (4CH1)
- **Papers:** Paper 1 (2h), Paper 2 (1h 15m)
- **Focus Areas:** International context
- **Practical Skills:** Paper 2 focus

---

# Part 2: Chemistry-Specific Content Standards

## 2.1 File Format

Standard JSON format:
```json
{
  "title": "Lesson Title",
  "content": "# Markdown content with chemical notation",
  "order": 1
}
```

## 2.2 Chemical Equation Standards

### Word Equations
Always provide word equations before symbol equations:
```markdown
**Word equation:**
magnesium + oxygen → magnesium oxide

**Symbol equation:**
$$\text{2Mg} + \text{O}_2 \rightarrow \text{2MgO}$$
```

### Balanced Symbol Equations
Use LaTeX with text mode for chemical formulae:
```markdown
$$\text{2Na} + \text{2H}_2\text{O} \rightarrow \text{2NaOH} + \text{H}_2$$
```

### State Symbols
Include state symbols where appropriate:
```markdown
$$\text{HCl}(aq) + \text{NaOH}(aq) \rightarrow \text{NaCl}(aq) + \text{H}_2\text{O}(l)$$
```

State symbol key:
- $(s)$ = solid
- $(l)$ = liquid
- $(g)$ = gas
- $(aq)$ = aqueous (dissolved in water)

### Ionic Equations
Show ionic equations with charges:
```markdown
**Full ionic equation:**
$$\text{Na}^+(aq) + \text{Cl}^-(aq) + \text{H}^+(aq) + \text{OH}^-(aq) \rightarrow \text{Na}^+(aq) + \text{Cl}^-(aq) + \text{H}_2\text{O}(l)$$

**Net ionic equation:**
$$\text{H}^+(aq) + \text{OH}^-(aq) \rightarrow \text{H}_2\text{O}(l)$$
```

### Half Equations (Electrolysis)
```markdown
**At the cathode (reduction):**
$$\text{Cu}^{2+} + 2e^- \rightarrow \text{Cu}$$

**At the anode (oxidation):**
$$2\text{Cl}^- \rightarrow \text{Cl}_2 + 2e^-$$
```

## 2.3 Calculation Standards

### Moles Calculations
Present calculations with clear structure:
```markdown
## Worked Example

**Question:** Calculate the number of moles in 12 g of magnesium. ($A_r$ of Mg = 24)

**Given:**
- Mass ($m$) = 12 g
- Molar mass ($M$) = 24 g/mol

**Formula:**
$$n = \frac{m}{M}$$

**Solution:**
$$n = \frac{12}{24} = 0.5 \text{ mol}$$

**Answer:** 0.5 mol
```

### Key Equations Reference
Always include the formula being used:

| Calculation | Formula | Units |
|-------------|---------|-------|
| Moles from mass | $n = \frac{m}{M}$ | mol |
| Mass from moles | $m = n \times M$ | g |
| Concentration | $c = \frac{n}{V}$ | mol/dm³ |
| Moles from conc. | $n = c \times V$ | mol |
| Atom economy | $\frac{\text{Mr of desired product}}{\text{Mr of all products}} \times 100$ | % |
| Percentage yield | $\frac{\text{actual yield}}{\text{theoretical yield}} \times 100$ | % |

## 2.4 Structure Diagram Conventions

### Dot-and-Cross Diagrams
Mark where diagrams are needed:
```markdown
[DOT-CROSS: Sodium chloride NaCl showing electron transfer]
[DOT-CROSS: Water H₂O showing shared pairs]
[DOT-CROSS: Methane CH₄ showing covalent bonds]
```

### Displayed Formulae (Organic)
```markdown
[DISPLAYED FORMULA: Ethanol CH₃CH₂OH showing all bonds]
[DISPLAYED FORMULA: Ethanoic acid CH₃COOH]
```

### Apparatus Diagrams
```markdown
[APPARATUS: Setup for electrolysis of copper sulfate solution]
[APPARATUS: Fractional distillation column]
[APPARATUS: Titration equipment with burette and conical flask]
```

### Structural Representations
For organic molecules, use text-based structures when simple:
```markdown
**Structural formula of ethanol:**
CH₃-CH₂-OH

**Structural formula of propan-1-ol:**
CH₃-CH₂-CH₂-OH
```

## 2.5 Chemistry Content Template

```markdown
# [Topic Title]

## Learning Objectives
By the end of this lesson, you should be able to:
- [Objective 1 - using syllabus command words]
- [Objective 2]
- [Objective 3]

## Introduction
[1-2 paragraphs explaining the topic and its importance in chemistry]

## Key Concepts

### [Concept 1]
[Detailed explanation]

[DIAGRAM/STRUCTURE: Description]

### [Concept 2]
[Detailed explanation with examples]

## Chemical Equations
[Relevant equations with word equations first, then symbol equations]

## Calculations (if applicable)

### Method
[Step-by-step calculation method]

### Worked Examples
[At least 2 worked examples with different difficulty levels]

## Practical Applications
[Real-world uses and industrial applications]

## Required Practical (if applicable)
**Aim:** [What the practical investigates]
**Method:** [Brief overview]
**Key Results:** [What to expect]
**Safety:** [Key safety points]

## Exam Tips
- [Command word guidance]
- [Common question types]
- [Mark scheme hints]

## Common Mistakes
- **Mistake:** [What students get wrong]
- **Correct:** [The right approach]

## Practice Questions

1. [1-2 mark recall question]
2. [2-3 mark application question]
3. [Calculation question]
4. [4-6 mark extended response]

## Key Terms Glossary

| Term | Definition |
|------|------------|
| [Term 1] | [Definition] |
| [Term 2] | [Definition] |

## Summary
- [Key point 1]
- [Key point 2]
- [Key equation to remember]
```

---

# Part 3: Detailed Topic Breakdown by Unit

## Unit 01: Atomic Structure
**Location:** `generic/chemistry/content/01-atomic-structure/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-elements-compounds-mixtures.json` | Elements, Compounds and Mixtures | Definitions, differences, examples |
| 02 | `02-atoms-and-elements.json` | Atoms and Elements | Atomic structure basics, element definition |
| 03 | `03-subatomic-particles.json` | Subatomic Particles | Protons, neutrons, electrons; mass and charge |
| 04 | `04-atomic-number-mass-number.json` | Atomic Number and Mass Number | Definitions, notation, calculations |
| 05 | `05-isotopes.json` | Isotopes | Definition, examples, relative atomic mass |
| 06 | `06-electronic-structure.json` | Electronic Structure | Electron shells, 2,8,8 rule, electron configuration |
| 07 | `07-development-of-atomic-model.json` | Development of the Atomic Model | Dalton → Thomson → Rutherford → Bohr |
| 08 | `08-periodic-table-arrangement.json` | Periodic Table Arrangement | Periods, groups, relationship to electron structure |
| 09 | `09-metals-and-non-metals.json` | Metals and Non-Metals | Properties, position in periodic table |
| 10 | `10-separating-mixtures.json` | Separating Mixtures | Filtration, evaporation, distillation, chromatography |
| 11 | `11-pure-substances.json` | Pure Substances and Formulations | Melting point test, formulations |

## Unit 02: Bonding and Structure
**Location:** `generic/chemistry/content/02-bonding/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-chemical-bonds-overview.json` | Chemical Bonds Overview | Why atoms bond, types of bonding |
| 02 | `02-ionic-bonding.json` | Ionic Bonding | Electron transfer, formation of ions |
| 03 | `03-ionic-compounds.json` | Ionic Compounds | Giant ionic lattices, properties |
| 04 | `04-covalent-bonding.json` | Covalent Bonding | Electron sharing, single/double/triple bonds |
| 05 | `05-simple-covalent-molecules.json` | Simple Covalent Molecules | Properties, intermolecular forces |
| 06 | `06-giant-covalent-structures.json` | Giant Covalent Structures | Diamond, graphite, silicon dioxide |
| 07 | `07-graphene-and-fullerenes.json` | Graphene and Fullerenes | Structure, properties, uses |
| 08 | `08-metallic-bonding.json` | Metallic Bonding | Sea of electrons, metal properties |
| 09 | `09-bonding-and-properties.json` | Bonding and Properties | Linking structure to properties |
| 10 | `10-nanoparticles.json` | Nanoparticles | Size, properties, applications |
| 11 | `11-states-of-matter.json` | States of Matter | Particle model, state changes |
| 12 | `12-changes-of-state.json` | Changes of State | Melting, boiling, energy changes |

## Unit 03: Quantitative Chemistry
**Location:** `generic/chemistry/content/03-quantitative-chemistry/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-conservation-of-mass.json` | Conservation of Mass | Law, balancing equations |
| 02 | `02-relative-formula-mass.json` | Relative Formula Mass | Calculating Mr from Ar |
| 03 | `03-the-mole.json` | The Mole | Avogadro's constant, mole calculations |
| 04 | `04-moles-and-mass.json` | Moles and Mass Calculations | n = m/M, worked examples |
| 05 | `05-balancing-equations.json` | Balancing Chemical Equations | Method, practice |
| 06 | `06-reacting-masses.json` | Reacting Masses | Using moles to calculate masses |
| 07 | `07-limiting-reactants.json` | Limiting Reactants | Identifying limiting reactant, excess |
| 08 | `08-concentration-of-solutions.json` | Concentration of Solutions | mol/dm³, g/dm³, conversions |
| 09 | `09-moles-in-solutions.json` | Moles in Solutions | n = c × V calculations |
| 10 | `10-percentage-yield.json` | Percentage Yield | Calculating, reasons for <100% |
| 11 | `11-atom-economy.json` | Atom Economy | Calculating, green chemistry |
| 12 | `12-molar-gas-volume.json` | Molar Gas Volume | 24 dm³ at RTP, calculations |

## Unit 04: Chemical Changes
**Location:** `generic/chemistry/content/04-chemical-changes/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-oxidation-and-reduction.json` | Oxidation and Reduction | Definitions (oxygen, electrons), OILRIG |
| 02 | `02-reactivity-series.json` | Reactivity Series | Order, determining reactivity |
| 03 | `03-metal-reactions-water-acids.json` | Reactions of Metals | With water, with acids, observations |
| 04 | `04-displacement-reactions.json` | Displacement Reactions | Predicting reactions, ionic equations |
| 05 | `05-extraction-of-metals.json` | Extraction of Metals | Relationship to reactivity |
| 06 | `06-reduction-with-carbon.json` | Reduction with Carbon | Iron extraction, blast furnace |
| 07 | `07-electrolysis-introduction.json` | Introduction to Electrolysis | Terminology, setup, requirements |
| 08 | `08-electrolysis-molten-compounds.json` | Electrolysis of Molten Compounds | Lead bromide, aluminium oxide |
| 09 | `09-electrolysis-aqueous-solutions.json` | Electrolysis of Aqueous Solutions | Competing reactions, rules |
| 10 | `10-electroplating.json` | Electroplating | Process, applications |
| 11 | `11-rusting-and-corrosion.json` | Rusting and Corrosion | Conditions, prevention methods |

## Unit 05: Chemical Energetics
**Location:** `generic/chemistry/content/05-energetics/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-energy-changes-introduction.json` | Energy Changes in Reactions | Energy in/out, energy profiles |
| 02 | `02-exothermic-reactions.json` | Exothermic Reactions | Definition, examples, temperature rise |
| 03 | `03-endothermic-reactions.json` | Endothermic Reactions | Definition, examples, temperature drop |
| 04 | `04-reaction-profiles.json` | Reaction Profiles | Drawing and interpreting energy diagrams |
| 05 | `05-activation-energy.json` | Activation Energy | Definition, catalysts effect |
| 06 | `06-bond-energies.json` | Bond Energies | Calculating energy changes from bond energies |
| 07 | `07-bond-energy-calculations.json` | Bond Energy Calculations | Worked examples, ΔH calculations |
| 08 | `08-cells-and-batteries.json` | Cells and Batteries | Chemical cells, rechargeable batteries |
| 09 | `09-fuel-cells.json` | Fuel Cells | Hydrogen fuel cells, advantages |

## Unit 06: Rates and Equilibrium
**Location:** `generic/chemistry/content/06-rates-and-equilibrium/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-rate-of-reaction.json` | Rate of Reaction | Definition, measuring rates |
| 02 | `02-collision-theory.json` | Collision Theory | Successful collisions, activation energy |
| 03 | `03-effect-of-concentration.json` | Effect of Concentration | On rate, explanation using collision theory |
| 04 | `04-effect-of-temperature.json` | Effect of Temperature | On rate, explanation using collision theory |
| 05 | `05-effect-of-surface-area.json` | Effect of Surface Area | On rate, particle size |
| 06 | `06-effect-of-pressure.json` | Effect of Pressure (Gases) | On rate for gaseous reactions |
| 07 | `07-catalysts.json` | Catalysts | Definition, how they work, examples |
| 08 | `08-rate-graphs.json` | Rate Graphs | Interpreting, calculating rate from graphs |
| 09 | `09-reversible-reactions.json` | Reversible Reactions | Definition, examples, ⇌ symbol |
| 10 | `10-dynamic-equilibrium.json` | Dynamic Equilibrium | Definition, conditions |
| 11 | `11-le-chateliers-principle.json` | Le Chatelier's Principle | Predicting equilibrium shifts |

## Unit 07: Acids, Bases and Salts
**Location:** `generic/chemistry/content/07-acids-and-bases/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-acids-introduction.json` | Introduction to Acids | Common acids, properties, H⁺ ions |
| 02 | `02-bases-and-alkalis.json` | Bases and Alkalis | Definitions, OH⁻ ions, examples |
| 03 | `03-ph-scale.json` | The pH Scale | 0-14, indicators, measuring pH |
| 04 | `04-strong-and-weak-acids.json` | Strong and Weak Acids | Ionisation, concentration vs strength |
| 05 | `05-neutralisation.json` | Neutralisation Reactions | Acid + alkali, acid + base |
| 06 | `06-reactions-of-acids.json` | Reactions of Acids | With metals, carbonates, metal oxides |
| 07 | `07-making-soluble-salts.json` | Making Soluble Salts | Methods: neutralisation, using excess |
| 08 | `08-making-insoluble-salts.json` | Making Insoluble Salts | Precipitation, solubility rules |
| 09 | `09-titrations.json` | Titrations | Method, calculations, indicators |
| 10 | `10-titration-calculations.json` | Titration Calculations | Finding unknown concentrations |
| 11 | `11-tests-for-ions.json` | Tests for Ions | Flame tests, precipitate tests, gas tests |
| 12 | `12-tests-for-gases.json` | Tests for Gases | H₂, O₂, CO₂, Cl₂, NH₃ |

## Unit 08: The Periodic Table
**Location:** `generic/chemistry/content/08-periodic-table/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-history-of-periodic-table.json` | History of the Periodic Table | Döbereiner → Newlands → Mendeleev |
| 02 | `02-periodic-table-structure.json` | Structure of the Periodic Table | Periods, groups, blocks |
| 03 | `03-group-1-alkali-metals.json` | Group 1: Alkali Metals | Properties, reactions, trends |
| 04 | `04-group-1-reactions.json` | Group 1 Reactions | With water, with oxygen, with chlorine |
| 05 | `05-group-7-halogens.json` | Group 7: Halogens | Properties, appearance, uses |
| 06 | `06-group-7-reactions.json` | Group 7 Reactions | Displacement, reactions with metals |
| 07 | `07-group-7-trends.json` | Group 7 Trends | Reactivity, melting/boiling points |
| 08 | `08-group-0-noble-gases.json` | Group 0: Noble Gases | Properties, uses, why unreactive |
| 09 | `09-transition-metals.json` | Transition Metals | Properties, comparison with Group 1 |
| 10 | `10-transition-metal-compounds.json` | Transition Metal Compounds | Coloured compounds, catalysts |

## Unit 09: Organic Chemistry
**Location:** `generic/chemistry/content/09-organic-chemistry/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-introduction-to-organic.json` | Introduction to Organic Chemistry | Carbon compounds, homologous series |
| 02 | `02-crude-oil.json` | Crude Oil | Formation, composition, importance |
| 03 | `03-fractional-distillation.json` | Fractional Distillation | Process, fractions, uses |
| 04 | `04-alkanes.json` | Alkanes | General formula, naming, properties |
| 05 | `05-combustion.json` | Combustion | Complete vs incomplete, products |
| 06 | `06-cracking.json` | Cracking | Thermal and catalytic, products |
| 07 | `07-alkenes.json` | Alkenes | General formula, double bond, test |
| 08 | `08-reactions-of-alkenes.json` | Reactions of Alkenes | Addition reactions, polymerisation |
| 09 | `09-alcohols.json` | Alcohols | General formula, properties, uses |
| 10 | `10-reactions-of-alcohols.json` | Reactions of Alcohols | Combustion, oxidation, fermentation |
| 11 | `11-carboxylic-acids.json` | Carboxylic Acids | General formula, properties, reactions |
| 12 | `12-esters.json` | Esters | Formation, properties, uses |
| 13 | `13-addition-polymers.json` | Addition Polymers | Formation, examples (polyethene, PVC) |
| 14 | `14-condensation-polymers.json` | Condensation Polymers | Polyesters, polyamides, proteins, DNA |

## Unit 10: Environmental Chemistry
**Location:** `generic/chemistry/content/10-environment/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-earths-atmosphere.json` | Earth's Atmosphere | Current composition, percentages |
| 02 | `02-evolution-of-atmosphere.json` | Evolution of the Atmosphere | Early atmosphere, how it changed |
| 03 | `03-greenhouse-gases.json` | Greenhouse Gases | CO₂, CH₄, water vapour, greenhouse effect |
| 04 | `04-climate-change.json` | Climate Change | Evidence, consequences, mitigation |
| 05 | `05-carbon-footprint.json` | Carbon Footprint | Definition, reduction methods |
| 06 | `06-atmospheric-pollutants.json` | Atmospheric Pollutants | CO, NOx, SO₂, particulates |
| 07 | `07-water-treatment.json` | Water Treatment | Potable water, purification steps |
| 08 | `08-waste-water-treatment.json` | Waste Water Treatment | Sewage treatment, stages |
| 09 | `09-life-cycle-assessment.json` | Life Cycle Assessment | Cradle to grave analysis |
| 10 | `10-recycling.json` | Recycling | Benefits, limitations, materials |

---

# Part 4: Board Adaptation Strategy

## 4.1 AQA GCSE Chemistry (8462) Adaptation

### Content Modifications
| Generic Unit | AQA Mapping | Notes |
|--------------|-------------|-------|
| 01 Atomic Structure | 4.1 | Include development of atomic model in depth |
| 02 Bonding | 4.2 | Emphasise graphene and fullerenes |
| 03 Quantitative | 4.3 | Strong calculation focus, molar gas volume |
| 04 Chemical Changes | 4.4 | Include electrolysis of aluminium |
| 05 Energetics | 4.5 | Fuel cells for Chemistry only |
| 06 Rates | 4.6 | Include equilibrium shifts |
| 07 Acids | 4.4.2 | Titration calculations essential |
| 08 Periodic Table | 4.1.3 | Transition metals for Chemistry only |
| 09 Organic | 4.7 | Full organic content for Chemistry only |
| 10 Environment | 4.9, 4.10 | Potable water, LCA |

### Required Practicals to Add
1. Making salts from insoluble bases
2. Temperature changes in reactions
3. Rates of reaction (marble chips)
4. Chromatography
5. Electrolysis
6. Titration
7. Identifying ions
8. Water purification

### AQA-Specific Exam Tips
- 6-mark questions require QWC (Quality of Written Communication)
- "Describe" vs "Explain" distinction important
- Calculations: show working, correct units
- Graph skills: drawing lines of best fit, calculating gradients

## 4.2 Cambridge IGCSE Chemistry (0620) Adaptation

### Core/Extended Differentiation

| Topic | Core | Extended |
|-------|------|----------|
| Atomic structure | Basic model | Electron arrangement detail |
| Moles | Simple calculations | Limiting reactants, concentration |
| Energetics | Exo/endo | Bond energy calculations |
| Rates | Factors | Collision theory detail |
| Equilibrium | Basic concept | Le Chatelier's principle |
| Organic | Alkanes, alkenes | All functional groups |

### Cambridge-Specific Content
- Detailed stoichiometry calculations
- Molar gas volume (24 dm³)
- Stronger emphasis on industrial processes
- Extended organic chemistry (isomerism)

### Alternative to Practical
- Include practical-based questions
- Method descriptions
- Data analysis skills

## 4.3 Edexcel GCSE Chemistry (1CH0) Adaptation

### Paper Distribution
| Paper 1 | Paper 2 |
|---------|---------|
| Topics 1-5 | Topics 6-9 |
| Atomic structure | Rates |
| Bonding | Energetics |
| Chemical changes | Fuels |
| Acids | Organic |
| Electrolysis | Atmosphere |

### Core Practicals to Include
1. Investigate changes in pH
2. Investigate temperature changes
3. Investigate rates of reaction
4. Investigate electrolysis
5. Prepare a sample of pure, dry salt
6. Investigate gas production

### Higher Tier Only Content
- Atom economy
- Concentration calculations
- Equilibrium position changes
- Full organic nomenclature

## 4.4 Edexcel IGCSE Chemistry (4CH1) Adaptation

### International Context
- Global industrial processes
- Environmental issues worldwide
- Metric units throughout

### Practical Skills Paper
- Ensure experimental descriptions included
- Data analysis and graph interpretation
- Evaluation skills

---

# Part 5: Chemistry Development Workflow

## 5.1 Prioritized Development Order

### Phase 1: Foundation (High Exam Weight)
1. **Unit 01: Atomic Structure** - Basis for all chemistry
2. **Unit 02: Bonding** - Essential for understanding properties
3. **Unit 03: Quantitative Chemistry** - Calculation-heavy, high marks

### Phase 2: Core Reactions
4. **Unit 07: Acids and Bases** - Common exam topic
5. **Unit 04: Chemical Changes** - Reactivity and electrolysis
6. **Unit 08: Periodic Table** - Group properties

### Phase 3: Advanced Topics
7. **Unit 05: Energetics** - Energy calculations
8. **Unit 06: Rates and Equilibrium** - Challenging concepts
9. **Unit 09: Organic Chemistry** - Large topic area

### Phase 4: Applications
10. **Unit 10: Environmental Chemistry** - Contemporary relevance

## 5.2 Estimated Development Effort

| Phase | Units | Est. Lessons | Est. Hours* |
|-------|-------|--------------|-------------|
| Phase 1 | 3 | 35 | 55-70 |
| Phase 2 | 3 | 33 | 50-65 |
| Phase 3 | 3 | 34 | 50-70 |
| Phase 4 | 1 | 10 | 15-20 |
| **Total** | **10** | **112** | **170-225** |

*Estimated 1.5-2 hours per lesson

## 5.3 Quality Assurance Checklist

### Chemical Accuracy
- [ ] All equations balanced
- [ ] Correct state symbols
- [ ] Accurate relative atomic masses used
- [ ] Correct formula for compounds
- [ ] Reaction conditions stated where needed

### Calculation Quality
- [ ] Clear step-by-step method
- [ ] Formula stated before substitution
- [ ] Correct units throughout
- [ ] Answer with appropriate significant figures
- [ ] "Check" step where appropriate

### Diagram Requirements
- [ ] Dot-and-cross diagrams marked
- [ ] Apparatus diagrams noted
- [ ] Structural formulae included
- [ ] Energy profile diagrams specified

### Practical Content
- [ ] Safety considerations mentioned
- [ ] Method clearly described
- [ ] Expected observations stated
- [ ] Sources of error discussed

---

# Part 6: Cross-Subject Insights from Chemistry

## 6.1 Lessons for Other Subject Development

### Calculation-Heavy Content (Applies to Physics, Maths)
Chemistry's moles calculations provide a template for:
- Step-by-step worked examples
- Formula → Substitution → Solution format
- Unit tracking throughout
- Multiple practice questions at varying difficulty

### Practical-Based Content (Applies to Physics, Biology)
Chemistry's required practicals template:
```markdown
## Required Practical: [Title]

**Aim:** [What is being investigated]

**Equipment:**
- [List of apparatus]

**Method:**
1. [Step 1]
2. [Step 2]
3. [Step 3]

**Safety:**
- [Safety consideration 1]
- [Safety consideration 2]

**Expected Results:**
[What should be observed]

**Analysis:**
[How to interpret results]
```

### Notation Standards (Applies to All Sciences)
Chemistry establishes clear standards for:
- LaTeX equation formatting
- Subscript/superscript usage
- State symbol conventions
- Unit formatting

## 6.2 Subject-Specific Adaptations

### For Physics
- Use Chemistry's calculation format
- Similar practical write-up structure
- Equation notation consistency

### For Biology
- Adapt equation format for biochemical equations
- Use similar key terms glossary format
- Practical methods template

### For Mathematics
- Chemistry's step-by-step calculation approach
- Clear formula statement before use
- Checking/verification emphasis

---

# Appendices

## Appendix A: Sample Chemistry Lesson (Complete)

**File:** `generic/chemistry/content/02-bonding/02-ionic-bonding.json`

```json
{
  "title": "Ionic Bonding",
  "content": "# Ionic Bonding\n\n## Learning Objectives\nBy the end of this lesson, you should be able to:\n- Describe how ionic bonds form\n- Explain why metals and non-metals form ionic compounds\n- Draw dot-and-cross diagrams for ionic compounds\n- Describe the structure of ionic compounds\n\n## Introduction\n\n**Ionic bonding** occurs between metals and non-metals. It involves the transfer of electrons from metal atoms to non-metal atoms, forming charged particles called **ions**.\n\n## Why Do Atoms Form Ions?\n\nAtoms are most stable when they have a full outer shell of electrons (like noble gases). To achieve this:\n\n- **Metal atoms** lose electrons → form **positive ions** (cations)\n- **Non-metal atoms** gain electrons → form **negative ions** (anions)\n\n## Formation of Sodium Chloride\n\n### Step 1: Electron Configuration\n- Sodium (Na): 2,8,1 → has 1 electron in outer shell\n- Chlorine (Cl): 2,8,7 → needs 1 electron for full shell\n\n### Step 2: Electron Transfer\n- Sodium loses 1 electron → Na⁺ (2,8)\n- Chlorine gains 1 electron → Cl⁻ (2,8,8)\n\n[DOT-CROSS: Sodium chloride formation showing electron transfer]\n\n### Step 3: Ionic Bond Forms\nThe oppositely charged ions attract each other with strong **electrostatic forces** - this is the ionic bond.\n\n## Writing Ion Formulae\n\n| Element | Electrons Lost/Gained | Ion Formula | Electron Configuration |\n|---------|----------------------|-------------|------------------------|\n| Sodium | Loses 1 | Na⁺ | 2,8 |\n| Magnesium | Loses 2 | Mg²⁺ | 2,8 |\n| Aluminium | Loses 3 | Al³⁺ | 2,8 |\n| Chlorine | Gains 1 | Cl⁻ | 2,8,8 |\n| Oxygen | Gains 2 | O²⁻ | 2,8 |\n| Nitrogen | Gains 3 | N³⁻ | 2,8 |\n\n## Dot-and-Cross Diagrams\n\nDot-and-cross diagrams show:\n- The outer shell electrons of each atom\n- How electrons transfer\n- The charge on each ion\n- Square brackets around ions with charge outside\n\n### Example: Magnesium Oxide\n\n- Magnesium: 2,8,2 → loses 2 electrons → Mg²⁺\n- Oxygen: 2,6 → gains 2 electrons → O²⁻\n\n[DOT-CROSS: Magnesium oxide MgO formation]\n\n### Example: Calcium Chloride\n\n- Calcium: 2,8,8,2 → loses 2 electrons → Ca²⁺\n- Each chlorine: gains 1 electron → Cl⁻\n- Need 2 chlorine atoms to balance calcium's 2+ charge\n- Formula: CaCl₂\n\n[DOT-CROSS: Calcium chloride CaCl₂ formation]\n\n## Structure of Ionic Compounds\n\nIonic compounds form **giant ionic lattices**:\n\n- Regular arrangement of ions\n- Each positive ion surrounded by negative ions\n- Each negative ion surrounded by positive ions\n- Strong electrostatic forces in all directions\n\n[DIAGRAM: Sodium chloride lattice structure showing arrangement of Na⁺ and Cl⁻ ions]\n\n## Properties of Ionic Compounds\n\n| Property | Explanation |\n|----------|-------------|\n| High melting/boiling points | Strong electrostatic forces between ions require lots of energy to break |\n| Solid at room temperature | Strong forces hold ions in fixed positions |\n| Conduct electricity when molten or dissolved | Ions free to move and carry charge |\n| Do not conduct when solid | Ions fixed in position, cannot move |\n| Often soluble in water | Water molecules can separate the ions |\n| Brittle | Layers can slip, like charges repel |\n\n## Worked Examples\n\n**Example 1:** Predict the formula of aluminium oxide.\n\n**Solution:**\n- Aluminium forms Al³⁺ (loses 3 electrons)\n- Oxygen forms O²⁻ (gains 2 electrons)\n- Need charges to balance: 2 × Al³⁺ = 6+ and 3 × O²⁻ = 6−\n- Formula: Al₂O₃\n\n**Example 2:** Explain why sodium chloride has a high melting point.\n\n**Solution:**\nSodium chloride is an ionic compound with a giant ionic lattice structure. There are strong electrostatic forces of attraction between the oppositely charged Na⁺ and Cl⁻ ions. A lot of energy is required to overcome these strong forces, so the melting point is high.\n\n## Common Mistakes\n\n- **Mistake:** Drawing dots and crosses mixed in the same ion\n- **Correct:** Use dots for one atom's electrons, crosses for the other\n\n- **Mistake:** Forgetting charges on dot-and-cross diagrams\n- **Correct:** Always include the charge outside the square bracket\n\n- **Mistake:** Saying ionic compounds conduct electricity in solid state\n- **Correct:** Only conduct when molten or dissolved (ions must be free to move)\n\n## Practice Questions\n\n1. State what type of particles are found in sodium chloride. (1 mark)\n\n2. Draw a dot-and-cross diagram to show the bonding in potassium chloride, KCl. (3 marks)\n\n3. Explain why magnesium oxide has a higher melting point than sodium chloride. (3 marks)\n\n4. Explain, in terms of particles, why sodium chloride conducts electricity when molten but not when solid. (4 marks)\n\n5. Predict the formula of the ionic compound formed between calcium and nitrogen. Show your working. (3 marks)\n\n## Key Terms Glossary\n\n| Term | Definition |\n|------|------------|\n| Ionic bonding | The electrostatic attraction between oppositely charged ions |\n| Ion | An atom that has gained or lost electrons |\n| Cation | A positive ion formed when an atom loses electrons |\n| Anion | A negative ion formed when an atom gains electrons |\n| Giant ionic lattice | A regular 3D arrangement of ions held by strong electrostatic forces |\n| Electrostatic force | The force of attraction between opposite charges |\n\n## Summary\n\n- Ionic bonds form between metals and non-metals\n- Metals lose electrons to form positive ions (cations)\n- Non-metals gain electrons to form negative ions (anions)\n- Ionic compounds have giant ionic lattice structures\n- Properties include: high melting points, conduct when molten/dissolved, brittle\n- The strong electrostatic forces explain the high melting points",
  "order": 2
}
```

---

## Appendix B: Organic Chemistry Naming Reference

### Alkanes (CₙH₂ₙ₊₂)
| Name | Formula | Structure |
|------|---------|-----------|
| Methane | CH₄ | CH₄ |
| Ethane | C₂H₆ | CH₃-CH₃ |
| Propane | C₃H₈ | CH₃-CH₂-CH₃ |
| Butane | C₄H₁₀ | CH₃-CH₂-CH₂-CH₃ |

### Alkenes (CₙH₂ₙ)
| Name | Formula | Structure |
|------|---------|-----------|
| Ethene | C₂H₄ | CH₂=CH₂ |
| Propene | C₃H₆ | CH₃-CH=CH₂ |
| Butene | C₄H₈ | CH₃-CH₂-CH=CH₂ |

### Alcohols (CₙH₂ₙ₊₁OH)
| Name | Formula | Structure |
|------|---------|-----------|
| Methanol | CH₃OH | CH₃-OH |
| Ethanol | C₂H₅OH | CH₃-CH₂-OH |
| Propan-1-ol | C₃H₇OH | CH₃-CH₂-CH₂-OH |

### Carboxylic Acids (CₙH₂ₙ₊₁COOH)
| Name | Formula | Structure |
|------|---------|-----------|
| Methanoic acid | HCOOH | H-COOH |
| Ethanoic acid | CH₃COOH | CH₃-COOH |
| Propanoic acid | C₂H₅COOH | CH₃-CH₂-COOH |

---

## Appendix C: Common Ion Tests Reference

### Flame Tests (Cations)
| Ion | Flame Colour |
|-----|--------------|
| Lithium Li⁺ | Crimson red |
| Sodium Na⁺ | Yellow |
| Potassium K⁺ | Lilac |
| Calcium Ca²⁺ | Orange-red |
| Copper Cu²⁺ | Blue-green |

### Hydroxide Precipitation Tests
| Ion | Colour of Precipitate |
|-----|----------------------|
| Copper(II) Cu²⁺ | Blue |
| Iron(II) Fe²⁺ | Green |
| Iron(III) Fe³⁺ | Brown |
| Aluminium Al³⁺ | White (dissolves in excess NaOH) |
| Calcium Ca²⁺ | White |

### Anion Tests
| Ion | Test | Positive Result |
|-----|------|-----------------|
| Carbonate CO₃²⁻ | Add dilute acid | Bubbles, gas turns limewater milky |
| Sulfate SO₄²⁻ | Add BaCl₂ + HCl | White precipitate |
| Halides | Add AgNO₃ + HNO₃ | Cl⁻: white, Br⁻: cream, I⁻: yellow |

### Gas Tests
| Gas | Test | Positive Result |
|-----|------|-----------------|
| Hydrogen H₂ | Burning splint | Squeaky pop |
| Oxygen O₂ | Glowing splint | Relights |
| Carbon dioxide CO₂ | Limewater | Turns milky |
| Chlorine Cl₂ | Damp litmus | Bleaches white |
| Ammonia NH₃ | Damp red litmus | Turns blue |

---

## Appendix D: Key Equations Reference

### Moles and Mass
$$n = \frac{m}{M}$$

### Concentration
$$c = \frac{n}{V}$$ (mol/dm³)

$$c = \frac{m}{V}$$ (g/dm³)

### Molar Gas Volume (at RTP)
$$n = \frac{V}{24}$$ where V is in dm³

### Percentage Yield
$$\text{Percentage yield} = \frac{\text{actual yield}}{\text{theoretical yield}} \times 100$$

### Atom Economy
$$\text{Atom economy} = \frac{M_r \text{ of desired product}}{\text{sum of } M_r \text{ of all reactants}} \times 100$$

### Energy Change from Bond Energies
$$\Delta H = \text{Energy to break bonds} - \text{Energy released making bonds}$$

$$\Delta H = \sum(\text{bonds broken}) - \sum(\text{bonds formed})$$

---

## Appendix E: Reactivity Series Reference

**Most reactive ↓**
| Metal | Reaction with Water | Reaction with Dilute Acid | Extraction Method |
|-------|---------------------|---------------------------|-------------------|
| Potassium | Violent | Too dangerous | Electrolysis |
| Sodium | Vigorous | Too dangerous | Electrolysis |
| Lithium | Vigorous | Very reactive | Electrolysis |
| Calcium | Fairly vigorous | Vigorous | Electrolysis |
| Magnesium | Very slow (steam) | Vigorous | Electrolysis |
| Aluminium | No reaction (oxide layer) | Slow | Electrolysis |
| **Carbon** | - | - | - |
| Zinc | No reaction | Moderate | Reduction with carbon |
| Iron | No reaction | Slow | Reduction with carbon |
| **Hydrogen** | - | - | - |
| Copper | No reaction | No reaction | Heating in air |
| Silver | No reaction | No reaction | Found native |
| Gold | No reaction | No reaction | Found native |

**Least reactive ↑**

---

*Document Version: 1.0*
*Created: February 2025*
*Companion to: DEVELOPMENT_PLAN.md, BIOLOGY_AND_SCALING_PLAN.md*
