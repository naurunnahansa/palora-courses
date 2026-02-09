# Palora Course Development Plan

## Executive Summary

This document provides a comprehensive plan for developing educational course content for the Palora platform. The plan follows a **"Generic First" strategy** where we build the Generic Physics course as the reference implementation, then use it as a template for all other courses.

**Total Scope:**
- 20 courses (4 exam boards x 4 subjects + 4 generic courses)
- ~900+ individual lesson pages
- 4 subjects: Physics, Chemistry, Biology, Mathematics

---

# Part 1: Generic Physics Course Development

## 1.1 Overview

The Generic Physics course serves as the **foundational content** that maps to all exam board specifications. It contains 8 units covering all GCSE/IGCSE physics topics.

### Current State
- **Completed:** 0 lessons (only unit metadata exists)
- **Target:** 65-75 lessons across 8 units
- **Reference Content:** 2 completed lessons exist in Cambridge IGCSE Physics (Newton's Laws, Friction)

### Unit Structure

| Unit | Title | Estimated Lessons |
|------|-------|-------------------|
| 01 | Forces and Motion | 12-15 |
| 02 | Energy | 8-10 |
| 03 | Thermal Physics | 8-10 |
| 04 | Waves | 10-12 |
| 05 | Electricity | 10-12 |
| 06 | Magnetism and Electromagnetism | 8-10 |
| 07 | Atomic and Nuclear Physics | 6-8 |
| 08 | Space Physics | 4-6 |

---

## 1.2 Content Standards

### File Format
All content files use JSON with the following schema:

```json
{
  "title": "Lesson Title",
  "content": "# Markdown content with LaTeX equations",
  "order": 1
}
```

### Naming Convention
```
{NN}-{slug}.json
```
- `NN` = Two-digit order number (01, 02, 03...)
- `slug` = Kebab-case topic name
- Example: `01-newtons-laws.json`, `02-friction.json`

### Content Structure Template
Every lesson should follow this structure:

```markdown
# [Topic Title]

## Introduction
[1-2 paragraphs explaining what this topic is and why it matters]

## Key Concepts

### [Concept 1]
[Explanation with examples]

### [Concept 2]
[Explanation with examples]

## Mathematical Relationships

[Key equations using LaTeX]

$$F = ma$$

Where:
- $F$ = Force (N)
- $m$ = Mass (kg)
- $a$ = Acceleration (m/s²)

## Worked Examples

**Example 1:** [Problem statement]

**Solution:**
[Step-by-step solution with equations]

## Real-World Applications
[2-3 practical examples of where this concept applies]

## Common Misconceptions
[List common student errors and correct understanding]

## Practice Problems

1. [Problem 1]
2. [Problem 2]
3. [Problem 3]

## Summary
[Bullet-point summary of key takeaways]
```

### LaTeX Standards
- Inline equations: `$E = mc^2$`
- Block equations: `$$E = mc^2$$`
- Units: Always include units in explanations
- Variables: Define all variables after equations
- Fractions: Use `\frac{a}{b}` format

### Quality Standards
- **Reading Level:** Appropriate for 14-16 year olds
- **Length:** 500-1500 words per lesson
- **Equations:** Include all syllabus-required equations
- **Diagrams:** Note where diagrams would be helpful (use placeholder text `[DIAGRAM: description]`)
- **Accuracy:** All scientific content must be factually correct
- **Exam Focus:** Include exam-style questions and command words

---

## 1.3 Detailed Topic Breakdown by Unit

### Unit 01: Forces and Motion
**Location:** `generic/physics/content/01-forces-and-motion/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-physical-quantities.json` | Physical Quantities and Units | SI units, prefixes, significant figures |
| 02 | `02-scalars-and-vectors.json` | Scalars and Vectors | Definitions, examples, vector addition |
| 03 | `03-distance-displacement.json` | Distance and Displacement | Definitions, differences, examples |
| 04 | `04-speed-velocity.json` | Speed and Velocity | Average/instantaneous, calculations |
| 05 | `05-acceleration.json` | Acceleration | Definition, calculations, deceleration |
| 06 | `06-distance-time-graphs.json` | Distance-Time Graphs | Interpreting, gradient = speed |
| 07 | `07-velocity-time-graphs.json` | Velocity-Time Graphs | Interpreting, gradient = acceleration, area = displacement |
| 08 | `08-equations-of-motion.json` | Equations of Motion (SUVAT) | v = u + at, s = ut + ½at², v² = u² + 2as |
| 09 | `09-mass-and-weight.json` | Mass and Weight | Differences, W = mg, g values |
| 10 | `10-newtons-first-law.json` | Newton's First Law | Inertia, balanced forces |
| 11 | `11-newtons-second-law.json` | Newton's Second Law | F = ma, resultant force |
| 12 | `12-newtons-third-law.json` | Newton's Third Law | Action-reaction pairs, examples |
| 13 | `13-friction-and-drag.json` | Friction and Drag | Types, factors, terminal velocity |
| 14 | `14-momentum.json` | Momentum | p = mv, conservation, collisions |
| 15 | `15-moments-and-equilibrium.json` | Moments and Equilibrium | Moment = F × d, principle of moments |

### Unit 02: Energy
**Location:** `generic/physics/content/02-energy/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-energy-stores.json` | Energy Stores | Types: kinetic, potential, thermal, chemical, nuclear |
| 02 | `02-energy-transfers.json` | Energy Transfers | Pathways: mechanical, electrical, heating, radiation |
| 03 | `03-kinetic-energy.json` | Kinetic Energy | KE = ½mv², calculations |
| 04 | `04-gravitational-pe.json` | Gravitational Potential Energy | GPE = mgh, calculations |
| 05 | `05-elastic-pe.json` | Elastic Potential Energy | EPE = ½ke², Hooke's Law |
| 06 | `06-work-done.json` | Work Done | W = Fd, energy transfer |
| 07 | `07-power.json` | Power | P = E/t, P = Fv, watts |
| 08 | `08-efficiency.json` | Efficiency | η = useful output / total input, Sankey diagrams |
| 09 | `09-conservation-of-energy.json` | Conservation of Energy | First law of thermodynamics, dissipation |
| 10 | `10-energy-resources.json` | Energy Resources | Renewable vs non-renewable, environmental impact |

### Unit 03: Thermal Physics
**Location:** `generic/physics/content/03-thermal-physics/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-kinetic-particle-model.json` | Kinetic Particle Model | Particles in solids, liquids, gases |
| 02 | `02-states-of-matter.json` | States of Matter | Properties, arrangement, movement |
| 03 | `03-density.json` | Density | ρ = m/V, calculations, floating/sinking |
| 04 | `04-changes-of-state.json` | Changes of State | Melting, boiling, sublimation, condensation |
| 05 | `05-internal-energy.json` | Internal Energy | Kinetic + potential energy of particles |
| 06 | `06-specific-heat-capacity.json` | Specific Heat Capacity | E = mcΔθ, practical applications |
| 07 | `07-specific-latent-heat.json` | Specific Latent Heat | E = mL, fusion vs vaporisation |
| 08 | `08-thermal-conduction.json` | Thermal Conduction | Mechanism, conductors vs insulators |
| 09 | `09-convection.json` | Convection | Mechanism, convection currents |
| 10 | `10-thermal-radiation.json` | Thermal Radiation | Emission, absorption, factors affecting |
| 11 | `11-gas-pressure.json` | Gas Pressure and Temperature | pV = nRT basics, pressure-temperature relationship |

### Unit 04: Waves
**Location:** `generic/physics/content/04-waves/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-wave-properties.json` | Wave Properties | Amplitude, wavelength, frequency, period |
| 02 | `02-wave-equation.json` | Wave Equation | v = fλ, calculations |
| 03 | `03-transverse-longitudinal.json` | Transverse and Longitudinal Waves | Differences, examples |
| 04 | `04-reflection.json` | Reflection of Waves | Law of reflection, applications |
| 05 | `05-refraction.json` | Refraction of Waves | Snell's law, refractive index |
| 06 | `06-diffraction.json` | Diffraction | Through gaps and around obstacles |
| 07 | `07-sound-waves.json` | Sound Waves | Production, properties, speed in different media |
| 08 | `08-ultrasound.json` | Ultrasound | Applications: medical imaging, sonar |
| 09 | `09-electromagnetic-spectrum.json` | Electromagnetic Spectrum | All EM waves, properties, dangers |
| 10 | `10-uses-of-em-waves.json` | Uses of EM Waves | Applications by type |
| 11 | `11-lenses.json` | Lenses | Converging, diverging, ray diagrams |
| 12 | `12-colour-and-filters.json` | Colour and Filters | White light, primary colours, absorption |

### Unit 05: Electricity
**Location:** `generic/physics/content/05-electricity/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-static-electricity.json` | Static Electricity | Charging by friction, uses and dangers |
| 02 | `02-electric-fields.json` | Electric Fields | Field lines, strength |
| 03 | `03-current.json` | Electric Current | I = Q/t, conventional vs electron flow |
| 04 | `04-potential-difference.json` | Potential Difference | V = E/Q, voltage in circuits |
| 05 | `05-resistance.json` | Resistance | R = V/I, factors affecting |
| 06 | `06-ohms-law.json` | Ohm's Law | V = IR, I-V characteristics |
| 07 | `07-circuit-components.json` | Circuit Components | Resistors, LDR, thermistor, diode, LED |
| 08 | `08-series-circuits.json` | Series Circuits | Current, voltage, resistance rules |
| 09 | `09-parallel-circuits.json` | Parallel Circuits | Current, voltage, resistance rules |
| 10 | `10-electrical-power.json` | Electrical Power | P = IV, P = I²R, P = V²/R |
| 11 | `11-electrical-energy.json` | Electrical Energy | E = Pt, E = IVt, kilowatt-hours |
| 12 | `12-domestic-electricity.json` | Domestic Electricity | Mains supply, fuses, earth wire, safety |

### Unit 06: Magnetism and Electromagnetism
**Location:** `generic/physics/content/06-magnetism/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-magnets-and-fields.json` | Magnets and Magnetic Fields | Poles, field lines, Earth's field |
| 02 | `02-permanent-induced-magnets.json` | Permanent and Induced Magnets | Hard/soft magnetic materials |
| 03 | `03-electromagnetism.json` | Electromagnetism | Current-carrying wires, solenoids |
| 04 | `04-electromagnets.json` | Electromagnets | Construction, uses, factors affecting strength |
| 05 | `05-motor-effect.json` | Motor Effect | F = BIL, left-hand rule |
| 06 | `06-dc-motors.json` | DC Motors | Construction, operation, split-ring commutator |
| 07 | `07-electromagnetic-induction.json` | Electromagnetic Induction | Faraday's law, Lenz's law |
| 08 | `08-generators.json` | Generators | AC and DC generators, differences |
| 09 | `09-transformers.json` | Transformers | Construction, step-up/down, Vp/Vs = Np/Ns |
| 10 | `10-national-grid.json` | National Grid | High voltage transmission, efficiency |

### Unit 07: Atomic and Nuclear Physics
**Location:** `generic/physics/content/07-atomic-physics/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-atomic-structure.json` | Atomic Structure | Protons, neutrons, electrons, atomic/mass number |
| 02 | `02-isotopes.json` | Isotopes | Definition, examples, notation |
| 03 | `03-radioactive-decay.json` | Radioactive Decay | Random nature, decay equations |
| 04 | `04-alpha-beta-gamma.json` | Alpha, Beta, and Gamma Radiation | Properties, penetration, ionisation |
| 05 | `05-half-life.json` | Half-Life | Definition, calculations, graphs |
| 06 | `06-uses-of-radiation.json` | Uses of Radioactivity | Medical, industrial, dating |
| 07 | `07-hazards-of-radiation.json` | Hazards and Safety | Effects on living tissue, protection |
| 08 | `08-nuclear-fission.json` | Nuclear Fission | Chain reactions, nuclear power |
| 09 | `09-nuclear-fusion.json` | Nuclear Fusion | Stars, energy release, challenges |

### Unit 08: Space Physics
**Location:** `generic/physics/content/08-space/`

| Order | File Name | Title | Key Content |
|-------|-----------|-------|-------------|
| 01 | `01-solar-system.json` | The Solar System | Planets, moons, asteroids, comets |
| 02 | `02-orbits.json` | Orbits | Circular motion, satellites, orbital period |
| 03 | `03-lifecycle-of-stars.json` | Life Cycle of Stars | Nebula to black hole/neutron star |
| 04 | `04-origin-of-elements.json` | Origin of Elements | Nuclear fusion in stars, supernovae |
| 05 | `05-red-shift.json` | Red Shift | Doppler effect, evidence for expansion |
| 06 | `06-big-bang.json` | Big Bang Theory | Evidence: CMBR, expansion |

---

## 1.4 Development Workflow

### Step 1: Create Unit Directory (if not exists)
```bash
mkdir -p generic/physics/content/01-forces-and-motion
```

### Step 2: Create Unit Metadata (if not exists)
Create `_unit.json`:
```json
{
  "title": "Forces and Motion",
  "description": "Explore forces, motion, and Newton's laws",
  "order": 1
}
```

### Step 3: Create Lesson Content
Create individual lesson files following the content template:
```json
{
  "title": "Newton's First Law",
  "content": "# Newton's First Law\n\n## Introduction\n...",
  "order": 10
}
```

### Step 4: Quality Review
- [ ] All equations use correct LaTeX syntax
- [ ] All variables are defined
- [ ] Practice problems have appropriate difficulty
- [ ] Content matches syllabus requirements
- [ ] No scientific inaccuracies

### Step 5: Cross-Reference Syllabus Mapping
Verify content covers all subsections listed in `_syllabus_map.json`:
- AQA GCSE 8463
- Cambridge IGCSE 0625
- Edexcel GCSE 1PH0
- Edexcel IGCSE 4PH1

---

## 1.5 Prioritized Development Order

### Phase 1: Core Mechanics (High Priority)
1. Unit 01: Forces and Motion (most commonly tested)
2. Unit 05: Electricity (large syllabus weight)
3. Unit 02: Energy (fundamental concepts)

### Phase 2: Waves and Thermal (Medium Priority)
4. Unit 04: Waves
5. Unit 03: Thermal Physics

### Phase 3: Electromagnetism and Nuclear (Medium Priority)
6. Unit 06: Magnetism and Electromagnetism
7. Unit 07: Atomic and Nuclear Physics

### Phase 4: Space (Lower Priority - often optional)
8. Unit 08: Space Physics

---

## 1.6 Estimated Effort

| Phase | Units | Est. Lessons | Est. Hours* |
|-------|-------|--------------|-------------|
| Phase 1 | 3 | 37 | 55-75 |
| Phase 2 | 2 | 23 | 35-45 |
| Phase 3 | 2 | 19 | 30-40 |
| Phase 4 | 1 | 6 | 10-15 |
| **Total** | **8** | **85** | **130-175** |

*Estimated 1.5-2 hours per lesson for research, writing, and review

---

# Part 2: Scaling to Other Courses

## 2.1 Strategy: "Generic First, Then Map"

The Generic courses serve as the **master content**. Exam-board-specific courses should:

1. **Reference generic content** where topics overlap (90%+ of content)
2. **Add board-specific content** for unique requirements
3. **Adjust terminology** to match specification language
4. **Include board-specific exam tips** and command words

### Course Relationship Diagram

```
                    ┌─────────────────────┐
                    │   GENERIC PHYSICS   │
                    │   (Master Content)  │
                    └──────────┬──────────┘
                               │
       ┌───────────────────────┼───────────────────────┐
       │                       │                       │
       ▼                       ▼                       ▼
┌──────────────┐     ┌──────────────────┐     ┌────────────────┐
│  AQA GCSE    │     │ Cambridge IGCSE  │     │ Edexcel GCSE   │
│  (8463)      │     │ (0625)           │     │ (1PH0)         │
└──────────────┘     └──────────────────┘     └────────────────┘
                                                      │
                                              ┌───────┴───────┐
                                              ▼               ▼
                                       ┌──────────┐   ┌──────────┐
                                       │ Edexcel  │   │ Edexcel  │
                                       │ IGCSE    │   │ Other    │
                                       │ (4PH1)   │   │ Quals    │
                                       └──────────┘   └──────────┘
```

---

## 2.2 Creating Board-Specific Physics Courses

### Option A: Direct Copy with Modifications (Recommended for MVP)

1. **Copy generic content** to board-specific folder
2. **Modify as needed:**
   - Update terminology to match specification
   - Add/remove topics as required
   - Include board-specific exam tips
   - Add "Required Practical" sections for relevant boards

### Option B: Reference-Based System (Future Enhancement)

Create a system where board-specific courses reference generic content:
```json
{
  "title": "Newton's Laws",
  "baseContent": "generic/physics/content/01-forces-and-motion/10-newtons-first-law.json",
  "additions": {
    "exam_tip": "AQA often asks you to identify action-reaction pairs...",
    "required_practical": "Investigate the effect of force on acceleration..."
  },
  "order": 11
}
```

### Board-Specific Requirements

#### AQA GCSE Physics (8463)
- **Unique Topics:** Triple Science content marked clearly
- **Required Practicals:** 10 specific investigations
- **Exam Style:** 6-mark extended response questions
- **Maths Skills:** Explicit maths requirements (30%)

#### Cambridge IGCSE Physics (0625)
- **Unique Topics:** Moments, pressure in more depth
- **Practical Component:** Alternative to Practical paper
- **Exam Style:** Structured questions, graph interpretation
- **Core/Extended:** Clearly differentiate difficulty levels

#### Edexcel GCSE Physics (1PH0)
- **Unique Topics:** Key Concepts paper
- **Required Practicals:** 16 core practicals
- **Exam Style:** Multiple choice in Paper 1
- **Higher/Foundation:** Content differentiation

#### Edexcel IGCSE Physics (4PH1)
- **Unique Topics:** Astrophysics depth
- **Exam Style:** 2 papers, no coursework
- **International Focus:** Context examples

---

## 2.3 Adapting for Chemistry, Biology, and Maths

### Template Application Process

1. **Review Generic Physics structure** as a template
2. **Create subject-specific unit breakdown** (see existing `COURSE_STRUCTURE_PLAN.md`)
3. **Apply same content standards:**
   - JSON file format
   - Markdown with LaTeX
   - Consistent section structure
   - Practice problems

### Subject-Specific Considerations

#### Chemistry
- **Equations:** Chemical equations using `$\ce{...}$` mhchem syntax
- **Diagrams:** Heavy reliance on molecular structures, apparatus
- **Practicals:** Strong practical component
- **Example Format:**
```markdown
$$\ce{2H2 + O2 -> 2H2O}$$
```

#### Biology
- **Terminology:** Heavy vocabulary load
- **Diagrams:** Essential for anatomy, processes
- **Data Analysis:** Interpreting graphs, statistics
- **Practicals:** Microscopy, dissection descriptions

#### Mathematics
- **Worked Examples:** Step-by-step solutions critical
- **Difficulty Progression:** Foundation → Higher tier
- **Equations:** Pure LaTeX mathematics
- **Example Format:**
```markdown
**Solve:** $x^2 + 5x + 6 = 0$

**Solution:**
$(x + 2)(x + 3) = 0$
$x = -2$ or $x = -3$
```

---

## 2.4 Content Creation Pipeline

### For Each New Course:

```
1. SETUP
   └── Create directory structure
   └── Copy _course.json template
   └── Create _unit.json files

2. CONTENT PLANNING
   └── Map syllabus to topics
   └── Create topic file list
   └── Identify priority order

3. CONTENT CREATION
   └── Research topic thoroughly
   └── Write using content template
   └── Include all required equations
   └── Add practice problems

4. QUALITY ASSURANCE
   └── Technical accuracy review
   └── Syllabus coverage check
   └── LaTeX rendering test
   └── Readability assessment

5. INTEGRATION
   └── Update syllabus mapping
   └── Cross-reference related topics
   └── Add to course navigation
```

---

## 2.5 Resource Requirements by Subject

### Physics (Reference Implementation)
| Task | Est. Lessons | Est. Hours |
|------|--------------|------------|
| Generic Physics | 85 | 130-175 |
| AQA Adaptations | 55 | 30-40 |
| Cambridge Adaptations | 50 | 25-35 |
| Edexcel GCSE Adaptations | 70 | 35-45 |
| Edexcel IGCSE Adaptations | 50 | 25-35 |
| **Physics Total** | **~310** | **245-330** |

### Chemistry
| Task | Est. Lessons | Est. Hours |
|------|--------------|------------|
| Generic Chemistry | 75 | 115-150 |
| Board Adaptations (x4) | 200 | 100-130 |
| **Chemistry Total** | **~275** | **215-280** |

### Biology
| Task | Est. Lessons | Est. Hours |
|------|--------------|------------|
| Generic Biology | 85 | 130-170 |
| Board Adaptations (x4) | 230 | 115-150 |
| **Biology Total** | **~315** | **245-320** |

### Mathematics
| Task | Est. Lessons | Est. Hours |
|------|--------------|------------|
| Generic Maths | 80 | 120-160 |
| Board Adaptations (x4) | 220 | 110-145 |
| **Maths Total** | **~300** | **230-305** |

### Grand Total
| Subject | Total Lessons | Total Hours |
|---------|---------------|-------------|
| Physics | ~310 | 245-330 |
| Chemistry | ~275 | 215-280 |
| Biology | ~315 | 245-320 |
| Mathematics | ~300 | 230-305 |
| **ALL SUBJECTS** | **~1200** | **935-1235** |

---

# Part 3: Development Standards and Guidelines

## 3.1 Git Workflow

### Branch Naming
```
feature/physics-unit01-forces
feature/chemistry-generic-unit03
fix/physics-equation-typo
```

### Commit Messages
```
feat(physics): Add Newton's Laws lessons (01-forces-and-motion)
fix(chemistry): Correct equation in ionic bonding
docs(biology): Update unit description for cells
```

### Pull Request Template
```markdown
## Summary
- Added X lessons to Unit Y
- Topics covered: [list]

## Checklist
- [ ] All equations render correctly
- [ ] Practice problems included
- [ ] Syllabus coverage verified
- [ ] No scientific inaccuracies
- [ ] JSON validates

## Syllabus References
- AQA: Section X.Y
- Cambridge: Topic X
- Edexcel: Topic X
```

---

## 3.2 Quality Checklist

### Per Lesson
- [ ] Title is descriptive and matches syllabus terminology
- [ ] Introduction explains relevance
- [ ] All key concepts from syllabus are covered
- [ ] Equations use correct LaTeX syntax
- [ ] All variables are defined with units
- [ ] At least one worked example included
- [ ] At least 3 practice problems
- [ ] Content is factually accurate
- [ ] Appropriate for target age (14-16)
- [ ] Diagrams noted where helpful
- [ ] Order number is correct
- [ ] JSON is valid

### Per Unit
- [ ] All required syllabus topics covered
- [ ] Logical progression of concepts
- [ ] Unit metadata (_unit.json) complete
- [ ] No duplicate content
- [ ] Cross-references to related units noted

### Per Course
- [ ] Course metadata (_course.json) complete
- [ ] All units present
- [ ] Syllabus mapping updated
- [ ] No broken references
- [ ] Consistent formatting throughout

---

## 3.3 Common Pitfalls to Avoid

### Content Issues
- **DON'T:** Copy directly from textbooks (copyright)
- **DON'T:** Use ambiguous terminology
- **DON'T:** Skip equation derivations students need
- **DON'T:** Assume prior knowledge without stating it
- **DON'T:** Use non-SI units without conversion

### Technical Issues
- **DON'T:** Use unsupported LaTeX commands
- **DON'T:** Create invalid JSON
- **DON'T:** Use relative file paths
- **DON'T:** Skip order numbers
- **DON'T:** Use inconsistent naming conventions

### Structure Issues
- **DON'T:** Create lessons that are too long (>2000 words)
- **DON'T:** Create lessons that are too short (<300 words)
- **DON'T:** Combine unrelated topics
- **DON'T:** Split topics that belong together
- **DON'T:** Forget practical applications

---

## 3.4 Tools and Resources

### Recommended Tools
- **JSON Validator:** https://jsonlint.com/
- **LaTeX Editor:** https://www.overleaf.com/ (for testing equations)
- **Markdown Preview:** VS Code with Markdown preview
- **Syllabus PDFs:** Official exam board specifications

### Reference Materials
- AQA Physics Specification: https://www.aqa.org.uk/subjects/science/gcse/physics-8463
- Cambridge IGCSE Physics: https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-physics-0625/
- Edexcel GCSE Physics: https://qualifications.pearson.com/en/qualifications/edexcel-gcses/physics-2016.html
- Edexcel IGCSE Physics: https://qualifications.pearson.com/en/qualifications/edexcel-international-gcses/physics-2017.html

---

# Part 4: Implementation Roadmap

## 4.1 Milestone 1: Generic Physics MVP
**Goal:** Complete Generic Physics course with all 8 units

### Tasks
1. Create all 85 lesson files
2. Complete quality review
3. Test syllabus coverage
4. Validate all JSON and LaTeX

### Deliverables
- 85 lesson JSON files
- 8 unit metadata files
- Updated syllabus mapping
- Quality assurance report

---

## 4.2 Milestone 2: AQA Physics Adaptation
**Goal:** Adapt Generic Physics for AQA GCSE

### Tasks
1. Copy and modify generic content
2. Add AQA-specific content:
   - Required practicals
   - Triple Science topics
   - Command word guidance
3. Map to AQA specification sections
4. Quality review

### Deliverables
- Complete AQA GCSE Physics course
- AQA-specific exam tips
- Required practical guides

---

## 4.3 Milestone 3: Cambridge and Edexcel Physics
**Goal:** Adapt Generic Physics for remaining boards

### Tasks
1. Cambridge IGCSE adaptation
2. Edexcel GCSE adaptation
3. Edexcel IGCSE adaptation
4. Cross-board quality review

### Deliverables
- Complete physics courses for all boards
- Board comparison documentation

---

## 4.4 Milestone 4: Generic Chemistry
**Goal:** Create Generic Chemistry using Physics as template

### Tasks
1. Apply Physics structure to Chemistry
2. Create 75 Chemistry lessons
3. Add chemistry-specific elements (equations, structures)
4. Quality review

### Deliverables
- Complete Generic Chemistry course
- Chemistry content standards

---

## 4.5 Milestone 5: Generic Biology

### Tasks
1. Apply template to Biology
2. Create 85 Biology lessons
3. Add biology-specific elements (diagrams, terminology)
4. Quality review

### Deliverables
- Complete Generic Biology course

---

## 4.6 Milestone 6: Generic Mathematics

### Tasks
1. Apply template to Maths
2. Create 80 Maths lessons
3. Heavy focus on worked examples
4. Foundation/Higher differentiation
5. Quality review

### Deliverables
- Complete Generic Maths course

---

## 4.7 Milestone 7: All Board Adaptations

### Tasks
1. Adapt all generic courses to all boards
2. Final quality assurance
3. Complete syllabus mapping verification
4. Documentation

### Deliverables
- All 20 courses complete
- Full platform content ready

---

# Appendices

## Appendix A: Sample Lesson File (Complete Example)

**File:** `generic/physics/content/01-forces-and-motion/11-newtons-second-law.json`

```json
{
  "title": "Newton's Second Law",
  "content": "# Newton's Second Law of Motion\n\n## Introduction\n\nNewton's Second Law explains the relationship between force, mass, and acceleration. It tells us that the acceleration of an object depends on the net force acting on it and its mass. This is one of the most important equations in physics.\n\n## The Law\n\nNewton's Second Law states:\n\n> The acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass.\n\nMathematically, this is expressed as:\n\n$$F = ma$$\n\nWhere:\n- $F$ = Net force (Newtons, N)\n- $m$ = Mass (kilograms, kg)\n- $a$ = Acceleration (metres per second squared, m/s²)\n\n## Understanding the Equation\n\n### Direct Proportionality to Force\n\nIf you double the force acting on an object (keeping mass constant), the acceleration doubles.\n\n- Force of 10 N on 2 kg → acceleration = 5 m/s²\n- Force of 20 N on 2 kg → acceleration = 10 m/s²\n\n### Inverse Proportionality to Mass\n\nIf you double the mass (keeping force constant), the acceleration halves.\n\n- Force of 10 N on 2 kg → acceleration = 5 m/s²\n- Force of 10 N on 4 kg → acceleration = 2.5 m/s²\n\n## Rearranging the Equation\n\nThe equation $F = ma$ can be rearranged to find any of the three quantities:\n\n**To find acceleration:**\n$$a = \\frac{F}{m}$$\n\n**To find mass:**\n$$m = \\frac{F}{a}$$\n\n## Worked Examples\n\n**Example 1:** A 1500 kg car accelerates at 2 m/s². Calculate the driving force.\n\n**Solution:**\n$$F = ma$$\n$$F = 1500 \\times 2$$\n$$F = 3000 \\text{ N}$$\n\n**Example 2:** A force of 600 N acts on an object, causing it to accelerate at 4 m/s². Find the mass.\n\n**Solution:**\n$$m = \\frac{F}{a}$$\n$$m = \\frac{600}{4}$$\n$$m = 150 \\text{ kg}$$\n\n**Example 3:** A resultant force of 20 N acts on a 5 kg mass. What is the acceleration?\n\n**Solution:**\n$$a = \\frac{F}{m}$$\n$$a = \\frac{20}{5}$$\n$$a = 4 \\text{ m/s}^2$$\n\n## Resultant Force\n\nImportant: In Newton's Second Law, $F$ refers to the **resultant (net) force**, not individual forces.\n\nIf multiple forces act on an object:\n1. Find the resultant force first\n2. Then use $F = ma$\n\n**Example:** A 50 kg sled has a driving force of 200 N and friction of 50 N. Find the acceleration.\n\n**Solution:**\n1. Resultant force: $200 - 50 = 150$ N\n2. $a = \\frac{150}{50} = 3$ m/s²\n\n## Common Misconceptions\n\n1. **\"More mass means more force\"** - No, more mass means more force is *needed* for the same acceleration\n2. **\"Objects need force to keep moving\"** - No, force causes *acceleration*, not constant velocity\n3. **\"The formula works with weight\"** - Weight (in N) is not mass (in kg) - don't confuse them\n\n## Real-World Applications\n\n- **Car safety:** Heavier cars need larger braking forces to stop\n- **Space rockets:** Must produce enormous force to accelerate large masses\n- **Sports:** Athletes use force to accelerate their body or equipment\n\n## Practice Problems\n\n1. Calculate the force needed to accelerate a 800 kg car at 1.5 m/s².\n\n2. A 0.5 kg ball is kicked with a force of 250 N. What is its acceleration?\n\n3. An object accelerates at 6 m/s² when a 120 N force is applied. Find its mass.\n\n4. A 60 kg skateboarder pushes off with a force of 180 N. If friction provides 30 N of resistance, what is their acceleration?\n\n## Summary\n\n- Newton's Second Law: $F = ma$\n- Acceleration is proportional to force\n- Acceleration is inversely proportional to mass\n- Always use the resultant force\n- Units: Force (N), Mass (kg), Acceleration (m/s²)",
  "order": 11
}
```

---

## Appendix B: Syllabus Mapping Reference

The `_syllabus_map.json` file in each generic course folder maps content to exam board specifications. See `/generic/physics/_syllabus_map.json` for the complete physics mapping.

Key fields:
- `spec`: Specification code (e.g., "8463" for AQA Physics)
- `sections`: Major syllabus sections covered
- `subsections`: Specific syllabus points covered
- `paper`: Which exam paper tests this content
- `notes`: Special notes (e.g., "Triple Science only")

---

## Appendix C: Directory Structure Reference

```
palora-courses/
├── README.md
├── COURSE_STRUCTURE_PLAN.md
├── DEVELOPMENT_PLAN.md                 ← This document
│
├── generic/
│   ├── physics/
│   │   ├── _course.json
│   │   ├── _syllabus_map.json
│   │   └── content/
│   │       ├── 01-forces-and-motion/
│   │       │   ├── _unit.json
│   │       │   ├── 01-physical-quantities.json
│   │       │   ├── 02-scalars-and-vectors.json
│   │       │   └── ...
│   │       ├── 02-energy/
│   │       └── ...
│   ├── chemistry/
│   ├── biology/
│   └── maths/
│
├── aqa/
│   ├── gcse-physics/
│   ├── gcse-chemistry/
│   ├── gcse-biology/
│   └── gcse-maths/
│
├── cambridge/
│   ├── igcse-physics/
│   ├── igcse-chemistry/
│   ├── igcse-biology/
│   └── igcse-maths/
│
└── edexcel/
    ├── gcse-physics/
    ├── gcse-chemistry/
    ├── gcse-biology/
    ├── gcse-maths/
    ├── igcse-physics/
    ├── igcse-chemistry/
    ├── igcse-biology/
    └── igcse-maths/
```

---

## Appendix D: Recommended Development Order Summary

### Phase 1: Foundation (Physics)
1. Generic Physics (all 8 units)
2. AQA GCSE Physics adaptation
3. Cambridge IGCSE Physics adaptation
4. Edexcel GCSE Physics adaptation
5. Edexcel IGCSE Physics adaptation

### Phase 2: Expand Sciences
6. Generic Chemistry
7. All Chemistry board adaptations
8. Generic Biology
9. All Biology board adaptations

### Phase 3: Mathematics
10. Generic Maths
11. All Maths board adaptations

---

*Document Version: 1.0*
*Created: February 2025*
*Last Updated: February 2025*
