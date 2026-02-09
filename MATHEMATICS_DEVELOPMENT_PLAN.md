# Generic Mathematics Development Plan

## Document Overview

This document provides a comprehensive plan for developing the Generic Mathematics course, including:
1. **Part 1:** Complete Generic Mathematics course specification
2. **Part 2:** Mathematics-specific content standards and conventions
3. **Part 3:** Detailed topic breakdowns for all 9 units
4. **Part 4:** Foundation/Higher tier strategy
5. **Part 5:** Board adaptation strategy
6. **Part 6:** Cross-subject insights and workflow

---

# Part 1: Generic Mathematics Course Specification

## 1.1 Course Overview

Generic Mathematics is a comprehensive course covering all fundamental mathematical concepts for GCSE/IGCSE level. It maps to AQA (8300), Cambridge (0580), Edexcel GCSE (1MA1), and Edexcel IGCSE (4MA1) specifications.

### Current State
- **Completed:** 0 lessons
- **Existing Structure:** 9 unit directories with `_unit.json` metadata
- **Target:** 115-130 lessons across 9 units

### Unit Structure Overview

| Unit | Title | Exam Weighting* | Est. Lessons |
|------|-------|-----------------|--------------|
| 01 | Number | F: 25%, H: 15% | 14-16 |
| 02 | Algebra | F: 20%, H: 30% | 18-20 |
| 03 | Graphs | (included in Algebra) | 12-14 |
| 04 | Geometry | F: 15%, H: 20% | 14-16 |
| 05 | Mensuration | (included in Geometry) | 10-12 |
| 06 | Trigonometry | (included in Geometry) | 12-14 |
| 07 | Vectors and Transformations | F: 5%, H: 10% | 10-12 |
| 08 | Probability | F: 15%, H: 15% | 10-12 |
| 09 | Statistics | F: 15%, H: 15% | 12-14 |

*Approximate AQA weightings; F = Foundation, H = Higher

**Total Estimated Lessons: 112-130**

---

## 1.2 Mathematics Exam Board Mapping

### AQA GCSE Mathematics (8300)
- **Papers:** 3 papers (Paper 1 non-calculator, Papers 2-3 calculator)
- **Duration:** 1h 30m each
- **Tiers:** Foundation (grades 1-5), Higher (grades 4-9)
- **Assessment Objectives:**
  - AO1: Use and apply standard techniques (50%)
  - AO2: Reason, interpret and communicate (25%)
  - AO3: Solve problems (25%)

### Cambridge IGCSE Mathematics (0580)
- **Papers:** Core (Papers 1, 3) or Extended (Papers 2, 4)
- **Core:** Grades C-G, Extended: Grades A*-E
- **Calculator:** Paper 1/2 non-calculator, Paper 3/4 calculator
- **Duration:** 1h (Paper 1/2), 2h (Paper 3/4)

### Edexcel GCSE Mathematics (1MA1)
- **Papers:** 3 papers (Paper 1 non-calculator, Papers 2-3 calculator)
- **Duration:** 1h 30m each
- **Tiers:** Foundation (grades 1-5), Higher (grades 4-9)
- **Structure:** Similar to AQA

### Edexcel IGCSE Mathematics (4MA1)
- **Papers:** 2 papers (Paper 1F/1H, Paper 2F/2H)
- **Duration:** 2h each
- **Tiers:** Foundation (grades 1-5), Higher (grades 4-9)
- **Calculator:** Both papers allow calculators

---

## 1.3 Key Differences: Maths vs Science Courses

| Aspect | Science Courses | Mathematics |
|--------|-----------------|-------------|
| Content focus | Concepts + applications | Methods + practice |
| Worked examples | Some | Essential (multiple per topic) |
| Practice questions | 3-5 per lesson | 8-15 per lesson |
| Diagrams | Subject-specific | Graphs, geometric constructions |
| Tier differentiation | Less prominent | Critical (F/H content differs significantly) |
| Calculator skills | Usually allowed | Non-calc skills essential |
| Proofs | Not typically | Required at Higher level |

---

# Part 2: Mathematics-Specific Content Standards

## 2.1 File Format

Standard JSON format:
```json
{
  "title": "Lesson Title",
  "content": "# Markdown content with LaTeX mathematics",
  "order": 1
}
```

## 2.2 Mathematical Notation Standards

### Inline Mathematics
Use single dollar signs for inline maths:
```markdown
The equation $y = mx + c$ represents a straight line.
```

### Display Mathematics
Use double dollar signs for displayed equations:
```markdown
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
```

### Common LaTeX Commands

| Symbol/Expression | LaTeX | Rendered |
|-------------------|-------|----------|
| Fraction | `\frac{a}{b}` | $\frac{a}{b}$ |
| Square root | `\sqrt{x}` | $\sqrt{x}$ |
| nth root | `\sqrt[n]{x}` | $\sqrt[n]{x}$ |
| Power | `x^2` | $x^2$ |
| Subscript | `x_1` | $x_1$ |
| Plus/minus | `\pm` | $\pm$ |
| Multiplication | `\times` | $\times$ |
| Division | `\div` | $\div$ |
| Not equal | `\neq` | $\neq$ |
| Less than or equal | `\leq` | $\leq$ |
| Greater than or equal | `\geq` | $\geq$ |
| Approximately | `\approx` | $\approx$ |
| Therefore | `\therefore` | $\therefore$ |
| Angle | `\angle` | $\angle$ |
| Degree | `^\circ` | $^\circ$ |
| Pi | `\pi` | $\pi$ |
| Infinity | `\infty` | $\infty$ |
| Parallel | `\parallel` | $\parallel$ |
| Perpendicular | `\perp` | $\perp$ |
| Triangle | `\triangle` | $\triangle$ |
| Sum | `\sum` | $\sum$ |

### Aligned Equations
For multi-step solutions:
```markdown
$$\begin{aligned}
2x + 3 &= 11 \\
2x &= 11 - 3 \\
2x &= 8 \\
x &= 4
\end{aligned}$$
```

### Cases/Piecewise Functions
```markdown
$$f(x) = \begin{cases}
x^2 & \text{if } x \geq 0 \\
-x^2 & \text{if } x < 0
\end{cases}$$
```

## 2.3 Worked Example Format

**Critical:** Mathematics lessons MUST include multiple worked examples. Use this format:

```markdown
## Worked Example 1

**Question:** Solve $3x + 7 = 22$

**Solution:**

$$\begin{aligned}
3x + 7 &= 22 \\
3x &= 22 - 7 \\
3x &= 15 \\
x &= 5
\end{aligned}$$

**Check:** $3(5) + 7 = 15 + 7 = 22$ ✓

---

## Worked Example 2 (Higher)

**Question:** Solve $x^2 - 5x + 6 = 0$

**Solution:**

**Method 1: Factorisation**
$$\begin{aligned}
x^2 - 5x + 6 &= 0 \\
(x - 2)(x - 3) &= 0 \\
x - 2 = 0 \quad &\text{or} \quad x - 3 = 0 \\
x = 2 \quad &\text{or} \quad x = 3
\end{aligned}$$

**Check:**
- When $x = 2$: $4 - 10 + 6 = 0$ ✓
- When $x = 3$: $9 - 15 + 6 = 0$ ✓
```

## 2.4 Tier Differentiation Marking

### Foundation Content
Mark Foundation-only approaches:
```markdown
## Method (Foundation)

For simple cases, use trial and improvement...
```

### Higher Content
Clearly mark Higher-only content:
```markdown
## Completing the Square (Higher Only)

To write $x^2 + bx + c$ in the form $(x + p)^2 + q$...
```

### Both Tiers
Mark content required for both:
```markdown
## Expanding Single Brackets (Foundation & Higher)

To expand $3(x + 4)$, multiply each term inside by 3...
```

## 2.5 Graph and Diagram Conventions

### Graph Placeholders
```markdown
[GRAPH: y = x² parabola with vertex at origin, passing through (1,1) and (-1,1)]

[GRAPH: Linear graph y = 2x - 3 showing gradient = 2 and y-intercept = -3]

[GRAPH: Scatter diagram showing positive correlation between height and weight]
```

### Geometric Diagrams
```markdown
[DIAGRAM: Triangle ABC with angle A = 40°, angle B = 75°, side AB = 8cm]

[DIAGRAM: Circle with centre O, radius 5cm, chord AB, tangent at point P]

[CONSTRUCTION: Perpendicular bisector of line segment AB using compass and straightedge]
```

### Table of Values
For graph plotting:
```markdown
| $x$ | -2 | -1 | 0 | 1 | 2 | 3 |
|-----|----|----|---|---|---|---|
| $y = x^2 - 2$ | 2 | -1 | -2 | -1 | 2 | 7 |
```

## 2.6 Mathematics Content Template

```markdown
# [Topic Title]

## Learning Objectives
By the end of this lesson, you should be able to:
- [Objective 1]
- [Objective 2]
- [Objective 3]

## Introduction
[Brief context explaining when this skill is used]

## Key Concepts

### [Concept/Method Name]
[Clear explanation of the method]

### Formula/Rule
$$[Key formula]$$

Where:
- [Variable 1] = [meaning]
- [Variable 2] = [meaning]

## Worked Examples

### Example 1 (Foundation)
**Question:** [Problem]

**Solution:**
[Step-by-step working with aligned equations]

**Answer:** [Final answer with units if applicable]

### Example 2 (Foundation)
[Another example, slightly harder]

### Example 3 (Higher)
[More challenging example]

### Example 4 (Higher)
[Complex/multi-step example]

## Method Summary
1. [Step 1]
2. [Step 2]
3. [Step 3]

## Common Mistakes
| Mistake | Why It's Wrong | Correct Approach |
|---------|----------------|------------------|
| [Error 1] | [Explanation] | [How to do it right] |
| [Error 2] | [Explanation] | [How to do it right] |

## Practice Questions

### Foundation Level
1. [Basic question]
2. [Basic question]
3. [Standard question]
4. [Standard question]

### Crossover (Foundation & Higher)
5. [Moderate question]
6. [Moderate question]

### Higher Level
7. [Challenging question]
8. [Challenging question]
9. [Problem-solving question]
10. [Multi-step question]

## Exam Tips
- [Calculator/non-calculator advice]
- [Common exam question types]
- [Mark scheme hints]

## Summary
- [Key point 1]
- [Key formula to remember]
- [When to use this method]
```

---

# Part 3: Detailed Topic Breakdown by Unit

## Unit 01: Number
**Location:** `generic/maths/content/01-number/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-types-of-numbers.json` | Types of Numbers | F+H | Integers, natural, rational, irrational |
| 02 | `02-place-value.json` | Place Value | F+H | Reading, writing, ordering numbers |
| 03 | `03-negative-numbers.json` | Negative Numbers | F+H | Operations with negatives |
| 04 | `04-factors-multiples-primes.json` | Factors, Multiples, Primes | F+H | Definitions, finding, factor trees |
| 05 | `05-hcf-and-lcm.json` | HCF and LCM | F+H | Methods: listing, prime factors, Venn |
| 06 | `06-powers-and-roots.json` | Powers and Roots | F+H | Squares, cubes, square/cube roots |
| 07 | `07-laws-of-indices.json` | Laws of Indices | F+H | Multiplication, division, power of power |
| 08 | `08-negative-and-fractional-indices.json` | Negative and Fractional Indices | H | $a^{-n}$, $a^{\frac{1}{n}}$, $a^{\frac{m}{n}}$ |
| 09 | `09-standard-form.json` | Standard Form | F+H | Writing, calculating, converting |
| 10 | `10-fractions-basics.json` | Fractions Basics | F+H | Equivalent, simplifying, mixed/improper |
| 11 | `11-fractions-operations.json` | Fractions Operations | F+H | Add, subtract, multiply, divide |
| 12 | `12-decimals.json` | Decimals | F+H | Operations, recurring decimals |
| 13 | `13-percentages.json` | Percentages | F+H | Of amount, increase/decrease, reverse |
| 14 | `14-ratio.json` | Ratio | F+H | Simplifying, sharing, scaling |
| 15 | `15-proportion.json` | Proportion | F+H | Direct, inverse proportion |
| 16 | `16-approximation-estimation.json` | Approximation and Estimation | F+H | Rounding, significant figures, estimation |
| 17 | `17-bounds.json` | Bounds and Error Intervals | H | Upper/lower bounds, calculations |
| 18 | `18-surds.json` | Surds | H | Simplifying, rationalising denominators |

## Unit 02: Algebra
**Location:** `generic/maths/content/02-algebra/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-algebraic-notation.json` | Algebraic Notation | F+H | Terms, expressions, conventions |
| 02 | `02-substitution.json` | Substitution | F+H | Into expressions and formulae |
| 03 | `03-collecting-like-terms.json` | Collecting Like Terms | F+H | Simplifying expressions |
| 04 | `04-expanding-single-brackets.json` | Expanding Single Brackets | F+H | $a(b + c) = ab + ac$ |
| 05 | `05-expanding-double-brackets.json` | Expanding Double Brackets | F+H | $(x + a)(x + b)$, FOIL method |
| 06 | `06-expanding-triple-brackets.json` | Expanding Triple Brackets | H | $(x + a)(x + b)(x + c)$ |
| 07 | `07-factorising-single-brackets.json` | Factorising into Single Brackets | F+H | Taking out common factors |
| 08 | `08-factorising-quadratics.json` | Factorising Quadratics | F+H | $x^2 + bx + c$, difference of squares |
| 09 | `09-factorising-harder-quadratics.json` | Factorising Harder Quadratics | H | $ax^2 + bx + c$ where $a \neq 1$ |
| 10 | `10-solving-linear-equations.json` | Solving Linear Equations | F+H | One-step, two-step, unknowns both sides |
| 11 | `11-solving-linear-equations-brackets.json` | Linear Equations with Brackets | F+H | Expanding then solving |
| 12 | `12-rearranging-formulae.json` | Rearranging Formulae | F+H | Changing the subject |
| 13 | `13-rearranging-harder-formulae.json` | Rearranging Harder Formulae | H | Subject appears twice |
| 14 | `14-solving-quadratics-factorising.json` | Solving Quadratics by Factorising | F+H | Setting equal to zero |
| 15 | `15-quadratic-formula.json` | The Quadratic Formula | H | $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$ |
| 16 | `16-completing-the-square.json` | Completing the Square | H | $(x + p)^2 + q$ form |
| 17 | `17-simultaneous-equations-elimination.json` | Simultaneous Equations: Elimination | F+H | Adding/subtracting to eliminate |
| 18 | `18-simultaneous-equations-substitution.json` | Simultaneous Equations: Substitution | F+H | Substituting one into other |
| 19 | `19-simultaneous-one-linear-one-quadratic.json` | Simultaneous: Linear and Quadratic | H | Solving graphically and algebraically |
| 20 | `20-inequalities-linear.json` | Linear Inequalities | F+H | Solving, representing on number line |
| 21 | `21-inequalities-quadratic.json` | Quadratic Inequalities | H | Solving using graphs |
| 22 | `22-sequences-term-to-term.json` | Sequences: Term-to-Term | F+H | Finding next terms, describing rules |
| 23 | `23-sequences-nth-term-linear.json` | nth Term of Linear Sequences | F+H | Finding and using $an + b$ |
| 24 | `24-sequences-nth-term-quadratic.json` | nth Term of Quadratic Sequences | H | Finding $an^2 + bn + c$ |
| 25 | `25-algebraic-fractions.json` | Algebraic Fractions | H | Simplifying, operations |
| 26 | `26-functions-notation.json` | Functions and Notation | H | $f(x)$, composite, inverse functions |
| 27 | `27-iteration.json` | Iteration | H | Using iterative formulae |
| 28 | `28-algebraic-proof.json` | Algebraic Proof | H | Proving statements algebraically |

## Unit 03: Graphs
**Location:** `generic/maths/content/03-graphs/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-coordinates.json` | Coordinates | F+H | Plotting, reading, midpoints |
| 02 | `02-plotting-linear-graphs.json` | Plotting Linear Graphs | F+H | Table of values, plotting |
| 03 | `03-gradient.json` | Gradient | F+H | Finding, interpreting, positive/negative |
| 04 | `04-y-intercept.json` | y-Intercept | F+H | Finding, meaning |
| 05 | `05-equation-of-straight-line.json` | Equation of a Straight Line | F+H | $y = mx + c$ form |
| 06 | `06-finding-equation-from-graph.json` | Finding Equation from Graph | F+H | Reading gradient and intercept |
| 07 | `07-parallel-perpendicular-lines.json` | Parallel and Perpendicular Lines | H | Gradient relationships |
| 08 | `08-plotting-quadratic-graphs.json` | Plotting Quadratic Graphs | F+H | Table of values, parabolas |
| 09 | `09-features-of-quadratics.json` | Features of Quadratic Graphs | F+H | Vertex, roots, line of symmetry |
| 10 | `10-cubic-graphs.json` | Cubic Graphs | H | $y = x^3$ and variations |
| 11 | `11-reciprocal-graphs.json` | Reciprocal Graphs | H | $y = \frac{1}{x}$ and $y = \frac{a}{x}$ |
| 12 | `12-exponential-graphs.json` | Exponential Graphs | H | $y = a^x$ growth and decay |
| 13 | `13-trigonometric-graphs.json` | Trigonometric Graphs | H | sin, cos, tan graphs |
| 14 | `14-real-life-graphs.json` | Real-Life Graphs | F+H | Distance-time, conversion graphs |
| 15 | `15-gradient-of-curve.json` | Gradient of a Curve | H | Tangent method, rate of change |
| 16 | `16-area-under-curve.json` | Area Under a Curve | H | Trapezium rule, estimation |
| 17 | `17-graph-transformations.json` | Graph Transformations | H | $f(x) + a$, $f(x + a)$, $af(x)$, $f(ax)$ |
| 18 | `18-graphical-solutions.json` | Solving Equations Graphically | F+H | Intersection of graphs |

## Unit 04: Geometry
**Location:** `generic/maths/content/04-geometry/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-angle-facts.json` | Angle Facts | F+H | Angles on line, at point, vertically opposite |
| 02 | `02-angles-in-triangles.json` | Angles in Triangles | F+H | Sum = 180°, types of triangles |
| 03 | `03-angles-in-quadrilaterals.json` | Angles in Quadrilaterals | F+H | Sum = 360°, properties |
| 04 | `04-angles-in-parallel-lines.json` | Angles in Parallel Lines | F+H | Corresponding, alternate, co-interior |
| 05 | `05-angles-in-polygons.json` | Angles in Polygons | F+H | Interior and exterior angles |
| 06 | `06-properties-of-triangles.json` | Properties of Triangles | F+H | Types, properties, angle rules |
| 07 | `07-properties-of-quadrilaterals.json` | Properties of Quadrilaterals | F+H | Square, rectangle, parallelogram, etc. |
| 08 | `08-congruent-triangles.json` | Congruent Triangles | F+H | SSS, SAS, ASA, RHS |
| 09 | `09-similar-shapes.json` | Similar Shapes | F+H | Identifying, finding missing sides |
| 10 | `10-similar-shapes-area-volume.json` | Similar Shapes: Area and Volume | H | Scale factor relationships |
| 11 | `11-circle-parts.json` | Parts of a Circle | F+H | Radius, diameter, chord, arc, sector, tangent |
| 12 | `12-circle-theorems.json` | Circle Theorems | H | Angle at centre, angles in semicircle |
| 13 | `13-circle-theorems-advanced.json` | Circle Theorems (Advanced) | H | Cyclic quadrilaterals, tangent properties |
| 14 | `14-constructions.json` | Constructions | F+H | Perpendicular bisector, angle bisector |
| 15 | `15-loci.json` | Loci | F+H | Equidistant from point/line, intersection |
| 16 | `16-bearings.json` | Bearings | F+H | Three-figure bearings, problems |

## Unit 05: Mensuration
**Location:** `generic/maths/content/05-mensuration/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-perimeter.json` | Perimeter | F+H | Rectangles, triangles, compound shapes |
| 02 | `02-area-rectangles-triangles.json` | Area: Rectangles and Triangles | F+H | Formulae, applications |
| 03 | `03-area-parallelograms-trapeziums.json` | Area: Parallelograms and Trapeziums | F+H | Formulae, derivations |
| 04 | `04-area-compound-shapes.json` | Area of Compound Shapes | F+H | Breaking into parts |
| 05 | `05-circumference-of-circle.json` | Circumference of a Circle | F+H | $C = \pi d$ or $C = 2\pi r$ |
| 06 | `06-area-of-circle.json` | Area of a Circle | F+H | $A = \pi r^2$ |
| 07 | `07-arc-length-sector-area.json` | Arc Length and Sector Area | F+H | Fractions of circles |
| 08 | `08-surface-area-prisms.json` | Surface Area of Prisms | F+H | Cuboids, triangular prisms |
| 09 | `09-surface-area-cylinders.json` | Surface Area of Cylinders | F+H | Curved + circular ends |
| 10 | `10-surface-area-cones-spheres.json` | Surface Area: Cones and Spheres | H | Formulae given |
| 11 | `11-volume-prisms.json` | Volume of Prisms | F+H | Cross-section × length |
| 12 | `12-volume-cylinders.json` | Volume of Cylinders | F+H | $V = \pi r^2 h$ |
| 13 | `13-volume-pyramids-cones.json` | Volume: Pyramids and Cones | H | $\frac{1}{3}$ × base area × height |
| 14 | `14-volume-spheres.json` | Volume of Spheres | H | $V = \frac{4}{3}\pi r^3$ |
| 15 | `15-units-conversions.json` | Units and Conversions | F+H | Length, area, volume conversions |

## Unit 06: Trigonometry
**Location:** `generic/maths/content/06-trigonometry/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-pythagoras-theorem.json` | Pythagoras' Theorem | F+H | $a^2 + b^2 = c^2$, finding sides |
| 02 | `02-pythagoras-applications.json` | Pythagoras Applications | F+H | Distance, diagonals, 3D |
| 03 | `03-trigonometric-ratios.json` | Trigonometric Ratios | F+H | sin, cos, tan definitions |
| 04 | `04-finding-sides-trig.json` | Finding Sides using Trigonometry | F+H | SOHCAHTOA applications |
| 05 | `05-finding-angles-trig.json` | Finding Angles using Trigonometry | F+H | Using inverse functions |
| 06 | `06-exact-trig-values.json` | Exact Trigonometric Values | H | 0°, 30°, 45°, 60°, 90° |
| 07 | `07-angles-elevation-depression.json` | Angles of Elevation and Depression | F+H | Real-world applications |
| 08 | `08-sine-rule.json` | The Sine Rule | H | $\frac{a}{\sin A} = \frac{b}{\sin B}$ |
| 09 | `09-cosine-rule.json` | The Cosine Rule | H | $a^2 = b^2 + c^2 - 2bc\cos A$ |
| 10 | `10-area-triangle-sine.json` | Area of Triangle using Sine | H | $\text{Area} = \frac{1}{2}ab\sin C$ |
| 11 | `11-3d-trigonometry.json` | 3D Trigonometry | H | Pythagoras and trig in 3D |
| 12 | `12-trig-problem-solving.json` | Trigonometry Problem Solving | H | Multi-step problems |

## Unit 07: Vectors and Transformations
**Location:** `generic/maths/content/07-vectors-and-transformations/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-translations.json` | Translations | F+H | Column vectors, describing |
| 02 | `02-reflections.json` | Reflections | F+H | Mirror lines, describing |
| 03 | `03-rotations.json` | Rotations | F+H | Centre, angle, direction |
| 04 | `04-enlargements.json` | Enlargements | F+H | Scale factor, centre |
| 05 | `05-negative-fractional-enlargements.json` | Negative and Fractional Enlargements | H | Effects on shape |
| 06 | `06-describing-transformations.json` | Describing Transformations | F+H | Full descriptions |
| 07 | `07-combined-transformations.json` | Combined Transformations | H | Sequence of transformations |
| 08 | `08-vectors-introduction.json` | Introduction to Vectors | H | Notation, representation |
| 09 | `09-vector-addition-subtraction.json` | Vector Addition and Subtraction | H | Resultant vectors |
| 10 | `10-scalar-multiplication.json` | Scalar Multiplication of Vectors | H | Multiplying by scalar |
| 11 | `11-position-vectors.json` | Position Vectors | H | Relative to origin |
| 12 | `12-vector-geometry.json` | Vector Geometry | H | Proofs using vectors |

## Unit 08: Probability
**Location:** `generic/maths/content/08-probability/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-probability-scale.json` | The Probability Scale | F+H | 0 to 1, impossible to certain |
| 02 | `02-calculating-probability.json` | Calculating Probability | F+H | Theoretical probability |
| 03 | `03-experimental-probability.json` | Experimental Probability | F+H | Relative frequency |
| 04 | `04-expected-outcomes.json` | Expected Outcomes | F+H | Probability × number of trials |
| 05 | `05-mutually-exclusive-events.json` | Mutually Exclusive Events | F+H | P(A or B) = P(A) + P(B) |
| 06 | `06-sample-spaces.json` | Sample Spaces | F+H | Listing outcomes systematically |
| 07 | `07-two-way-tables.json` | Two-Way Tables | F+H | Reading and constructing |
| 08 | `08-tree-diagrams.json` | Tree Diagrams | F+H | Independent events |
| 09 | `09-tree-diagrams-dependent.json` | Tree Diagrams: Dependent Events | H | Without replacement |
| 10 | `10-venn-diagrams.json` | Venn Diagrams | F+H | Two and three sets |
| 11 | `11-set-notation.json` | Set Notation | H | $\cup$, $\cap$, $\xi$, $A'$ |
| 12 | `12-conditional-probability.json` | Conditional Probability | H | P(A|B), from Venn diagrams |

## Unit 09: Statistics
**Location:** `generic/maths/content/09-statistics/`

| Order | File Name | Title | Tier | Key Content |
|-------|-----------|-------|------|-------------|
| 01 | `01-data-types.json` | Types of Data | F+H | Qualitative, quantitative, discrete, continuous |
| 02 | `02-collecting-data.json` | Collecting Data | F+H | Primary, secondary, sampling methods |
| 03 | `03-frequency-tables.json` | Frequency Tables | F+H | Constructing and reading |
| 04 | `04-grouped-frequency-tables.json` | Grouped Frequency Tables | F+H | Class intervals, modal class |
| 05 | `05-pictograms-bar-charts.json` | Pictograms and Bar Charts | F+H | Drawing and interpreting |
| 06 | `06-pie-charts.json` | Pie Charts | F+H | Drawing and interpreting |
| 07 | `07-mean.json` | The Mean | F+H | Calculating, from frequency tables |
| 08 | `08-median-mode.json` | Median and Mode | F+H | Finding, from tables |
| 09 | `09-range.json` | Range | F+H | Calculating, interpreting |
| 10 | `10-mean-from-grouped-data.json` | Mean from Grouped Data | F+H | Using midpoints, estimated mean |
| 11 | `11-comparing-distributions.json` | Comparing Distributions | F+H | Using averages and range |
| 12 | `12-scatter-graphs.json` | Scatter Graphs | F+H | Plotting, correlation types |
| 13 | `13-lines-of-best-fit.json` | Lines of Best Fit | F+H | Drawing, using for estimation |
| 14 | `14-cumulative-frequency.json` | Cumulative Frequency | H | Tables, graphs, median, quartiles |
| 15 | `15-box-plots.json` | Box Plots | H | Drawing, interpreting, comparing |
| 16 | `16-histograms.json` | Histograms | H | Frequency density, unequal class widths |

---

# Part 4: Foundation/Higher Tier Strategy

## 4.1 Content Distribution

### Foundation Only Topics
- Basic number work
- Simple percentages
- Basic ratio
- Simple linear equations
- Plotting straight line graphs
- Basic angle facts
- Simple probability

### Higher Only Topics
- Surds
- Negative and fractional indices
- Bounds
- Quadratic formula and completing the square
- Algebraic fractions
- Functions
- Iteration
- Algebraic proof
- Circle theorems
- Sine/cosine rules
- Vectors
- Histograms
- Conditional probability

### Crossover Topics (Both Tiers)
- Most topics appear in both tiers but at different depths
- Foundation: procedural methods, standard questions
- Higher: reasoning, proof, complex applications

## 4.2 Marking Tier Content

Use these markers consistently:

```markdown
## Foundation Approach

[Simpler method suitable for Foundation tier]

---

## Higher Extension

[Additional content, methods, or depth for Higher tier]
```

## 4.3 Exam Paper Strategy

### AQA/Edexcel Structure
| Paper | Calculator | Topics |
|-------|------------|--------|
| Paper 1 | No | All topics (non-calc skills) |
| Paper 2 | Yes | All topics |
| Paper 3 | Yes | All topics |

### Non-Calculator Skills to Emphasise
- Mental arithmetic
- Fraction operations without calculator
- Standard form by hand
- Solving equations without decimals
- Exact values in trigonometry

---

# Part 5: Board Adaptation Strategy

## 5.1 AQA GCSE Mathematics (8300) Adaptation

### Assessment Objectives
| AO | Description | Weighting |
|----|-------------|-----------|
| AO1 | Use and apply standard techniques | 50% |
| AO2 | Reason, interpret and communicate | 25% |
| AO3 | Solve problems in context | 25% |

### AQA-Specific Content
- Strong emphasis on problem-solving
- Multi-step questions common
- "Show that" questions
- Quality of written communication in extended answers

### Required Adaptations
- Add more AO2/AO3 style questions
- Include "explain" and "show that" questions
- Problem-solving contexts

## 5.2 Cambridge IGCSE Mathematics (0580) Adaptation

### Core vs Extended

| Topic | Core (Grades C-G) | Extended (Grades A*-E) |
|-------|-------------------|------------------------|
| Number | Basic operations | Surds, bounds |
| Algebra | Linear equations | Quadratics, functions |
| Geometry | Basic properties | Circle theorems |
| Trigonometry | Basic ratios | Sine/cosine rules |
| Statistics | Averages, charts | Histograms, cumulative freq |

### Cambridge-Specific Content
- More emphasis on calculations
- Functions covered in more depth
- Set notation and Venn diagrams essential
- 3D trigonometry and vectors

### Required Adaptations
- Clear Core/Extended split
- More calculation practice
- Cambridge-style structured questions

## 5.3 Edexcel GCSE Mathematics (1MA1) Adaptation

### Paper Structure
Same as AQA: 3 papers, Paper 1 non-calculator

### Edexcel-Specific Features
- Functional skills integration
- "Explain your answer" questions
- Grid-based questions for graphs

### Required Adaptations
- Include functional context questions
- Graph grid practice
- Explanation-style questions

## 5.4 Edexcel IGCSE Mathematics (4MA1) Adaptation

### Structure
- 2 papers (both calculator)
- Foundation and Higher tiers

### Edexcel IGCSE-Specific Content
- Calculus introduction (differentiation basics)
- More rigorous algebra
- International contexts

### Required Adaptations
- Add basic differentiation (Higher)
- More algebraic manipulation
- International contexts

---

# Part 6: Development Workflow

## 6.1 Prioritized Development Order

### Phase 1: Core Skills (Highest Exam Weight)
1. **Unit 01: Number** - Foundation for everything
2. **Unit 02: Algebra** - Highest weighting at Higher
3. **Unit 03: Graphs** - Closely linked to algebra

### Phase 2: Shape and Space
4. **Unit 04: Geometry** - Visual, accessible
5. **Unit 05: Mensuration** - Calculation-heavy
6. **Unit 06: Trigonometry** - Essential Higher content

### Phase 3: Data and Vectors
7. **Unit 08: Probability** - Often well-liked by students
8. **Unit 09: Statistics** - Real-world applications
9. **Unit 07: Vectors and Transformations** - Higher-focused

## 6.2 Estimated Development Effort

| Phase | Units | Est. Lessons | Est. Hours* |
|-------|-------|--------------|-------------|
| Phase 1 | 3 | 54 | 80-110 |
| Phase 2 | 3 | 43 | 65-85 |
| Phase 3 | 3 | 28 | 40-55 |
| **Total** | **9** | **125** | **185-250** |

*Estimated 1.5-2 hours per lesson including worked examples

## 6.3 Quality Assurance Checklist

### Mathematical Accuracy
- [ ] All calculations are correct
- [ ] LaTeX renders properly
- [ ] Equations are properly aligned
- [ ] Exact values used where appropriate

### Pedagogical Quality
- [ ] Multiple worked examples (minimum 3-4)
- [ ] Examples progress in difficulty
- [ ] Both Foundation and Higher content included
- [ ] Common mistakes addressed
- [ ] Method summary provided

### Practice Questions
- [ ] Minimum 10 questions per lesson
- [ ] Clear Foundation/Higher split
- [ ] Variety of question types
- [ ] Includes "show that" and "explain" questions

### Exam Readiness
- [ ] Calculator/non-calculator skills noted
- [ ] Command words used correctly
- [ ] Mark-scheme style answers modelled

---

# Part 7: Mathematics-Specific Appendices

## Appendix A: Sample Mathematics Lesson (Complete)

**File:** `generic/maths/content/02-algebra/15-quadratic-formula.json`

```json
{
  "title": "The Quadratic Formula",
  "content": "# The Quadratic Formula\n\n## Learning Objectives\nBy the end of this lesson, you should be able to:\n- State the quadratic formula\n- Use the quadratic formula to solve quadratic equations\n- Determine when to use the formula vs factorising\n- Give answers to an appropriate degree of accuracy\n\n> **Note:** This is Higher tier content.\n\n## Introduction\n\nThe **quadratic formula** is a method that can solve ANY quadratic equation, even when factorising doesn't work. It's especially useful when the solutions are not whole numbers or simple fractions.\n\n## The Formula\n\nFor any quadratic equation in the form $ax^2 + bx + c = 0$:\n\n$$x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}$$\n\nWhere:\n- $a$ = coefficient of $x^2$\n- $b$ = coefficient of $x$\n- $c$ = constant term\n- $\\pm$ means you calculate twice: once with + and once with −\n\n## When to Use the Quadratic Formula\n\n| Situation | Best Method |\n|-----------|-------------|\n| Equation factorises easily | Factorising |\n| Coefficients are awkward | Quadratic formula |\n| Question asks for exact answer with surds | Formula or completing square |\n| Question says \"give answers to 2 d.p.\" | Quadratic formula |\n\n## Method\n\n1. Rearrange to $ax^2 + bx + c = 0$\n2. Identify values of $a$, $b$, and $c$\n3. Substitute into the formula\n4. Calculate the discriminant $b^2 - 4ac$\n5. Find both solutions using + and −\n6. Round if required\n\n## Worked Examples\n\n### Example 1\n**Question:** Solve $x^2 + 5x + 3 = 0$, giving answers to 2 decimal places.\n\n**Solution:**\n\n**Step 1:** Identify $a$, $b$, $c$\n- $a = 1$, $b = 5$, $c = 3$\n\n**Step 2:** Calculate the discriminant\n$$b^2 - 4ac = 5^2 - 4(1)(3) = 25 - 12 = 13$$\n\n**Step 3:** Substitute into formula\n$$x = \\frac{-5 \\pm \\sqrt{13}}{2(1)} = \\frac{-5 \\pm \\sqrt{13}}{2}$$\n\n**Step 4:** Find both solutions\n$$x = \\frac{-5 + \\sqrt{13}}{2} = \\frac{-5 + 3.606...}{2} = \\frac{-1.394...}{2} = -0.70$$\n\n$$x = \\frac{-5 - \\sqrt{13}}{2} = \\frac{-5 - 3.606...}{2} = \\frac{-8.606...}{2} = -4.30$$\n\n**Answer:** $x = -0.70$ or $x = -4.30$ (2 d.p.)\n\n---\n\n### Example 2\n**Question:** Solve $2x^2 - 7x + 4 = 0$, giving exact answers in surd form.\n\n**Solution:**\n\n- $a = 2$, $b = -7$, $c = 4$\n\n$$b^2 - 4ac = (-7)^2 - 4(2)(4) = 49 - 32 = 17$$\n\n$$x = \\frac{-(-7) \\pm \\sqrt{17}}{2(2)} = \\frac{7 \\pm \\sqrt{17}}{4}$$\n\n**Answer:** $x = \\frac{7 + \\sqrt{17}}{4}$ or $x = \\frac{7 - \\sqrt{17}}{4}$\n\n---\n\n### Example 3\n**Question:** Solve $3x^2 + 2x - 7 = 0$, giving answers to 3 significant figures.\n\n**Solution:**\n\n- $a = 3$, $b = 2$, $c = -7$\n\n$$b^2 - 4ac = 2^2 - 4(3)(-7) = 4 + 84 = 88$$\n\n$$x = \\frac{-2 \\pm \\sqrt{88}}{2(3)} = \\frac{-2 \\pm \\sqrt{88}}{6}$$\n\n$$x = \\frac{-2 + 9.38...}{6} = 1.23 \\quad \\text{(3 s.f.)}$$\n\n$$x = \\frac{-2 - 9.38...}{6} = -1.90 \\quad \\text{(3 s.f.)}$$\n\n**Answer:** $x = 1.23$ or $x = -1.90$\n\n---\n\n### Example 4\n**Question:** The equation $x^2 + kx + 9 = 0$ has exactly one solution. Find the value of $k$.\n\n**Solution:**\n\nFor exactly one solution, the discriminant equals zero:\n$$b^2 - 4ac = 0$$\n$$k^2 - 4(1)(9) = 0$$\n$$k^2 - 36 = 0$$\n$$k^2 = 36$$\n$$k = \\pm 6$$\n\n**Answer:** $k = 6$ or $k = -6$\n\n## The Discriminant\n\nThe expression $b^2 - 4ac$ is called the **discriminant**. It tells us about the solutions:\n\n| Discriminant | Number of Solutions | Graph |\n|--------------|--------------------|---------|\n| $b^2 - 4ac > 0$ | Two distinct solutions | Crosses x-axis twice |\n| $b^2 - 4ac = 0$ | One repeated solution | Touches x-axis |\n| $b^2 - 4ac < 0$ | No real solutions | Doesn't cross x-axis |\n\n[GRAPH: Three parabolas showing the three discriminant cases]\n\n## Common Mistakes\n\n| Mistake | Why It's Wrong | Correct Approach |\n|---------|----------------|------------------|\n| Forgetting the $\\pm$ | Gives only one solution | Always calculate both + and − |\n| Writing $-b$ as positive when $b$ is negative | Sign error | $-(-7) = +7$ |\n| Dividing only the $-b$ by $2a$ | Must divide entire numerator | Use brackets: $\\frac{-b \\pm \\sqrt{...}}{2a}$ |\n| Using $2a = by$ when $a = 1$ | $2a = 2 \\times 1 = 2$ | Still need to divide by 2 |\n\n## Practice Questions\n\n### Standard Questions\n1. Solve $x^2 + 4x + 1 = 0$, giving answers to 2 d.p.\n\n2. Solve $x^2 - 6x + 2 = 0$, giving exact answers in surd form.\n\n3. Solve $2x^2 + 5x - 1 = 0$, giving answers to 2 d.p.\n\n4. Solve $3x^2 - x - 5 = 0$, giving answers to 3 s.f.\n\n### Rearranging First\n5. Solve $x^2 + 3x = 7$, giving answers to 2 d.p.\n\n6. Solve $2x^2 = 4x + 3$, giving answers to 2 d.p.\n\n### Discriminant Questions\n7. Show that $x^2 + 3x + 5 = 0$ has no real solutions.\n\n8. The equation $x^2 + px + 16 = 0$ has exactly one solution. Find the possible values of $p$.\n\n9. Find the range of values of $k$ for which $x^2 + 4x + k = 0$ has two distinct solutions.\n\n### Problem Solving\n10. The length of a rectangle is 3 cm more than its width. The area is 15 cm². Find the dimensions, giving answers to 2 d.p.\n\n## Exam Tips\n\n- **Always check:** if the question says \"to 2 d.p.\" use the formula (don't try to factorise)\n- **Show your working:** write out $a = $, $b = $, $c = $ clearly\n- **Don't round too early:** keep full calculator values until the final answer\n- **State both solutions:** even if one seems unreasonable, give both and discuss if needed\n\n## Summary\n\n- The quadratic formula is $x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}$\n- Works for ANY quadratic equation $ax^2 + bx + c = 0$\n- The discriminant $b^2 - 4ac$ tells you how many solutions exist\n- Remember to give both solutions (use $\\pm$)\n- Round only at the final step",
  "order": 15
}
```

---

## Appendix B: Key Formulae Reference

### Number
| Topic | Formula |
|-------|---------|
| Percentage change | $\\frac{\\text{change}}{\\text{original}} \\times 100$ |
| Compound interest | $A = P(1 + \\frac{r}{100})^n$ |
| Reverse percentage | $\\text{Original} = \\frac{\\text{New}}{1 \\pm \\frac{\\%}{100}}$ |

### Algebra
| Topic | Formula |
|-------|---------|
| Quadratic formula | $x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}$ |
| Difference of squares | $a^2 - b^2 = (a+b)(a-b)$ |
| nth term (linear) | $a_n = dn + (a - d)$ where $d$ = common difference |
| nth term (quadratic) | $a_n = an^2 + bn + c$ |

### Geometry
| Topic | Formula |
|-------|---------|
| Angles in polygon | Interior = $\\frac{(n-2) \\times 180}{n}$ |
| Arc length | $\\frac{\\theta}{360} \\times 2\\pi r$ |
| Sector area | $\\frac{\\theta}{360} \\times \\pi r^2$ |

### Mensuration
| Shape | Perimeter/Circumference | Area | Volume |
|-------|------------------------|------|--------|
| Rectangle | $2(l + w)$ | $l \\times w$ | - |
| Triangle | $a + b + c$ | $\\frac{1}{2} \\times b \\times h$ | - |
| Circle | $2\\pi r$ or $\\pi d$ | $\\pi r^2$ | - |
| Trapezium | Sum of sides | $\\frac{1}{2}(a + b)h$ | - |
| Prism | - | - | Area × length |
| Cylinder | - | - | $\\pi r^2 h$ |
| Cone | - | $\\pi r^2 + \\pi rl$ | $\\frac{1}{3}\\pi r^2 h$ |
| Sphere | - | $4\\pi r^2$ | $\\frac{4}{3}\\pi r^3$ |
| Pyramid | - | - | $\\frac{1}{3} \\times \\text{base} \\times h$ |

### Trigonometry
| Topic | Formula |
|-------|---------|
| Pythagoras | $a^2 + b^2 = c^2$ |
| SOHCAHTOA | $\\sin\\theta = \\frac{O}{H}$, $\\cos\\theta = \\frac{A}{H}$, $\\tan\\theta = \\frac{O}{A}$ |
| Sine rule | $\\frac{a}{\\sin A} = \\frac{b}{\\sin B} = \\frac{c}{\\sin C}$ |
| Cosine rule | $a^2 = b^2 + c^2 - 2bc\\cos A$ |
| Area (sine) | $\\frac{1}{2}ab\\sin C$ |

### Probability
| Topic | Formula |
|-------|---------|
| Probability | $P(A) = \\frac{\\text{favourable outcomes}}{\\text{total outcomes}}$ |
| P(not A) | $P(A') = 1 - P(A)$ |
| P(A or B) mutually exclusive | $P(A \\cup B) = P(A) + P(B)$ |
| P(A and B) independent | $P(A \\cap B) = P(A) \\times P(B)$ |

### Statistics
| Topic | Formula |
|-------|---------|
| Mean | $\\bar{x} = \\frac{\\sum x}{n}$ or $\\frac{\\sum fx}{\\sum f}$ |
| Range | Highest − Lowest |
| Frequency density | $\\frac{\\text{Frequency}}{\\text{Class width}}$ |

---

## Appendix C: Exact Trigonometric Values

| Angle | $\sin\theta$ | $\cos\theta$ | $\tan\theta$ |
|-------|--------------|--------------|--------------|
| $0°$ | $0$ | $1$ | $0$ |
| $30°$ | $\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{\sqrt{3}}$ or $\frac{\sqrt{3}}{3}$ |
| $45°$ | $\frac{\sqrt{2}}{2}$ or $\frac{1}{\sqrt{2}}$ | $\frac{\sqrt{2}}{2}$ or $\frac{1}{\sqrt{2}}$ | $1$ |
| $60°$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $\sqrt{3}$ |
| $90°$ | $1$ | $0$ | undefined |

---

## Appendix D: Circle Theorems Reference

1. **Angle at centre** = 2 × angle at circumference (same arc)

2. **Angle in semicircle** = 90°

3. **Angles in same segment** are equal

4. **Opposite angles in cyclic quadrilateral** sum to 180°

5. **Tangent perpendicular to radius** at point of contact

6. **Tangents from external point** are equal length

7. **Alternate segment theorem**: Angle between tangent and chord = angle in alternate segment

[DIAGRAMS: All seven circle theorems illustrated]

---

## Appendix E: Graph Shapes Reference

### Linear: $y = mx + c$
- Straight line
- Gradient $m$, y-intercept $c$

### Quadratic: $y = ax^2 + bx + c$
- Parabola (U-shape if $a > 0$, ∩-shape if $a < 0$)
- Vertex at $x = -\frac{b}{2a}$

### Cubic: $y = ax^3$
- S-shape through origin
- Positive $a$: bottom-left to top-right

### Reciprocal: $y = \frac{a}{x}$
- Two curves in opposite quadrants
- Asymptotes at $x = 0$ and $y = 0$

### Exponential: $y = a^x$
- Growth curve (if $a > 1$)
- Passes through $(0, 1)$
- Asymptote at $y = 0$

### Trigonometric
- $y = \sin x$: Wave, period 360°, range [-1, 1]
- $y = \cos x$: Same as sin shifted 90°
- $y = \tan x$: Period 180°, asymptotes at 90°, 270°, etc.

[GRAPHS: All graph types illustrated]

---

## Appendix F: Indices Laws Reference

| Law | Rule | Example |
|-----|------|---------|
| Multiplication | $a^m \times a^n = a^{m+n}$ | $2^3 \times 2^4 = 2^7$ |
| Division | $a^m \div a^n = a^{m-n}$ | $5^6 \div 5^2 = 5^4$ |
| Power of power | $(a^m)^n = a^{mn}$ | $(3^2)^4 = 3^8$ |
| Power of product | $(ab)^n = a^n b^n$ | $(2x)^3 = 8x^3$ |
| Zero power | $a^0 = 1$ | $7^0 = 1$ |
| Negative power | $a^{-n} = \frac{1}{a^n}$ | $2^{-3} = \frac{1}{8}$ |
| Fractional power | $a^{\frac{1}{n}} = \sqrt[n]{a}$ | $8^{\frac{1}{3}} = 2$ |
| Combined | $a^{\frac{m}{n}} = \sqrt[n]{a^m}$ | $8^{\frac{2}{3}} = 4$ |

---

## Appendix G: Command Words Reference

| Command Word | Meaning | Example Response |
|--------------|---------|------------------|
| Calculate | Work out numerically | Show working, give answer |
| Solve | Find the value(s) that satisfy | $x = 3$ or $x = -2$ |
| Simplify | Reduce to simplest form | $\frac{6x}{3} = 2x$ |
| Expand | Multiply out brackets | $3(x + 2) = 3x + 6$ |
| Factorise | Write as product of factors | $x^2 + 5x = x(x + 5)$ |
| Write/State | Give answer (minimal working) | The gradient is 3 |
| Explain | Give reasons using maths | "Because angles on a straight line sum to 180°..." |
| Show that | Prove a given result | Work towards the given answer |
| Prove | Logical argument from start | Full algebraic proof |
| Sketch | Show key features (not accurate) | Shape, intercepts, asymptotes |
| Draw | Accurate diagram | Use ruler, protractor |
| Estimate | Approximate calculation | Round then calculate |

---

*Document Version: 1.0*
*Created: February 2025*
*Companion to: DEVELOPMENT_PLAN.md, BIOLOGY_AND_SCALING_PLAN.md, CHEMISTRY_DEVELOPMENT_PLAN.md*
