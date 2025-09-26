# Chemical Equilibrium Study Notes

Based on "Fundamentals of Chemistry" by David Goldberg (pp. 477-493)

## 1. Introduction to Chemical Equilibrium

### Definition

- Chemical equilibrium is a dynamic state where the rates of forward and reverse reactions are equal
- The concentrations of reactants and products remain constant over time
- The system appears to stop changing macroscopically while continuing to react microscopically

### Visual Representation

```
       Forward reaction
A + B ----------------------→ C + D
      ←----------------------
        Reverse reaction
```

## 2. Equilibrium Constant (K)

### General Form

For a reaction: aA + bB ⇌ cC + dD

- K = [C]ᶜ[D]ᵈ / [A]ᵃ[B]ᵇ
- Square brackets [ ] represent molar concentrations
- Exponents are coefficients from balanced equation

### Detailed Examples

1. N₂ + 3H₂ ⇌ 2NH₃
   K = [NH₃]² / ([N₂][H₂]³)

2. 2SO₂ + O₂ ⇌ 2SO₃
   K = [SO₃]² / ([SO₂]²[O₂])

3. H₂ + I₂ ⇌ 2HI
   K = [HI]² / ([H₂][I₂])

### Types of Equilibrium Constants

1. Kc - concentration-based equilibrium constant
   - Used for solutions
   - Units depend on stoichiometry

2. Kp - pressure-based equilibrium constant (for gases)
   - Kp = Kc(RT)ᵈⁿ
   - Δn = moles of gaseous products - moles of gaseous reactants

3. Ka - acid dissociation constant
   Example: CH₃COOH ⇌ H⁺ + CH₃COO⁻
   Ka = [H⁺][CH₃COO⁻] / [CH₃COOH]

4. Kb - base dissociation constant
   Example: NH₃ + H₂O ⇌ NH₄⁺ + OH⁻
   Kb = [NH₄⁺][OH⁻] / [NH₃]

## 3. Le Chatelier's Principle (Extended)

### Detailed Examples

1. Temperature Effect
   N₂ + 3H₂ ⇌ 2NH₃ (ΔH = -92.4 kJ/mol)
   - Temperature ↑: Shifts left (endothermic direction)
   - Temperature ↓: Shifts right (exothermic direction)

2. Pressure Effect
   2SO₂ + O₂ ⇌ 2SO₃
   - Pressure ↑: Shifts right (fewer moles of gas)
   - Pressure ↓: Shifts left (more moles of gas)

3. Concentration Effect
   PCl₅ ⇌ PCl₃ + Cl₂
   - Adding Cl₂: Shifts left
   - Removing PCl₃: Shifts right

## 4. ICE Tables - Detailed Example

Problem: For the reaction N₂O₄ ⇌ 2NO₂, initial [N₂O₄] = 0.400 M. At equilibrium, [NO₂] = 0.200 M. Calculate Kc.

ICE Table:

```
             N₂O₄   ⇌    2NO₂
I:          0.400          0
C:           -x           +2x
E:         0.400-x        0.200
```

Solution:

1. [NO₂] = 0.200 M = 2x
   Therefore, x = 0.100 M
2. [N₂O₄]ₑq = 0.400 - 0.100 = 0.300 M
3. Kc = [NO₂]² / [N₂O₄] = (0.200)² / 0.300 = 0.133

## 5. Advanced Practice Problems

### Problem Set 1: Equilibrium Calculations

1. For the reaction 2NOBr ⇌ 2NO + Br₂
   Initial [NOBr] = 0.300 M
   At equilibrium, [NO] = 0.080 M
   Calculate:
   a) Equilibrium concentrations of all species
   b) Kc

2. The equilibrium constant Kc for N₂ + 3H₂ ⇌ 2NH₃ is 0.50 at 400°C
   If initial concentrations are:
   [N₂] = 0.80 M
   [H₂] = 0.60 M
   [NH₃] = 0 M
   Calculate equilibrium concentrations.

### Problem Set 2: Le Chatelier's Principle

3. For the equilibrium: CO(g) + H₂O(g) ⇌ CO₂(g) + H₂(g), ΔH = -41.2 kJ/mol
   Predict the direction of shift for:
   a) Addition of CO₂
   b) Decrease in pressure
   c) Increase in temperature
   d) Removal of H₂O

4. CaCO₃(s) ⇌ CaO(s) + CO₂(g), ΔH = +178 kJ/mol
   How would the following affect the equilibrium:
   a) Adding more CaCO₃
   b) Removing CO₂
   c) Decreasing temperature
   d) Increasing pressure

## 6. Real-World Applications

### Industrial Processes

1. Haber Process (NH₃ production)
   - Conditions: 450°C, 200 atm, iron catalyst
   - Why these conditions?
     - High pressure favors products (fewer moles of gas)
     - Moderate temperature (compromise between rate and yield)
     - Catalyst increases rate without affecting equilibrium

2. Contact Process (H₂SO₄ production)
   2SO₂ + O₂ ⇌ 2SO₃
   - Conditions: V₂O₅ catalyst, 400-450°C
   - Removal of SO₃ drives reaction forward

### Biological Systems

1. Oxygen Transport in Blood
   Hb + O₂ ⇌ HbO₂
   - Affected by:
     - pH (Bohr effect)
     - CO₂ concentration
     - Temperature
     - Altitude

2. Buffer Systems
   H₂CO₃ ⇌ H⁺ + HCO₃⁻
   - Maintains blood pH
   - Common ion effect demonstration

## 7. Advanced Concepts

### Relationship Between ΔG° and K

- ΔG° = -RT ln K
- When K > 1, ΔG° < 0 (spontaneous)
- When K < 1, ΔG° > 0 (non-spontaneous)

### Temperature Dependence of K

- Van 't Hoff equation:
  ln(K₂/K₁) = -(ΔH°/R)(1/T₂ - 1/T₁)

### Heterogeneous Equilibria

- Pure solids and liquids omitted from K expression
- Example: CaCO₃(s) ⇌ CaO(s) + CO₂(g)
  K = [CO₂]

## Study Tips and Additional Resources

1. Visualization Techniques
   - Draw concentration vs. time graphs
   - Use arrow diagrams for shifts
   - Create your own ICE tables

2. Problem-Solving Strategy
   a) Write balanced equation
   b) Write K expression
   c) Create ICE table
   d) Solve for unknown
   e) Check assumptions

3. Online Resources
   - PhET Interactive Simulations
   - Khan Academy videos
   - Chemistry software for equilibrium calculations

4. Common Mistakes to Avoid
   - Forgetting to square/cube concentrations in K
   - Including solids/liquids in K
   - Incorrect stoichiometric relationships
   - Wrong direction in Le Chatelier predictions

---

Note: These enhanced notes include advanced concepts and practical applications. Work through all practice problems for better understanding. For complete mastery, combine these notes with textbook study and laboratory experience.
