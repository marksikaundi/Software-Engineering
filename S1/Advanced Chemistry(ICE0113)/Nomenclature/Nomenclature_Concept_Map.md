# Chemical Nomenclature Concept Map

## Chemical Nomenclature
```mermaid
graph TD
    A[Chemical Nomenclature] --> B[Inorganic Compounds]
    A --> C[Organic Compounds]

    %% Inorganic Branch
    B --> D[Ionic Compounds]
    B --> E[Molecular Compounds]
    B --> F[Acids]
    B --> G[Hydrates]
    B --> H[Coordination Compounds]

    D --> D1[Metal + Nonmetal]
    D --> D2[Metal + Polyatomic Ion]
    D1 --> D1a[Fixed Charge Metals: Na+, K+, Ca2+]
    D1 --> D1b[Variable Charge Metals: Fe2+/Fe3+, Cu+/Cu2+]

    E --> E1[Binary Molecular]
    E --> E2[With Polyatomic Groups]

    F --> F1[Binary Acids]
    F --> F2[Oxoacids]
    F1 --> F1a[Hydro-X-ic acid]
    F2 --> F2a[-ate → -ic acid]
    F2 --> F2b[-ite → -ous acid]

    %% Organic Branch
    C --> I[Hydrocarbons]
    C --> J[Functional Groups]

    I --> I1[Alkanes: -ane]
    I --> I2[Alkenes: -ene]
    I --> I3[Alkynes: -yne]
    I --> I4[Aromatics]

    J --> J1[Alcohols: -ol]
    J --> J2[Aldehydes: -al]
    J --> J3[Ketones: -one]
    J --> J4[Carboxylic Acids: -oic acid]
    J --> J5[Esters: -oate]
    J --> J6[Amines: -amine]
    J --> J7[Ethers]
    J --> J8[Amides: -amide]
```

## Rules for Naming Inorganic Compounds
```mermaid
flowchart TD
    A[Inorganic Compound] --> B{Contains Metal?}
    B -->|Yes| C[Ionic Compound]
    B -->|No| D[Molecular Compound]

    C --> E{Fixed or Variable Charge?}
    E -->|Fixed| F[Name metal + Name nonmetal with -ide]
    E -->|Variable| G[Name metal + Roman numeral + Name nonmetal with -ide]

    D --> H[Use prefixes to indicate number of atoms]

    A --> I{Contains Hydrogen?}
    I -->|Yes| J{In aqueous solution?}
    J -->|Yes| K[Acid]
    K --> L{Contains oxygen?}
    L -->|No| M[Binary Acid: Hydro-X-ic acid]
    L -->|Yes| N[Oxoacid: Based on anion name]
```

## Rules for Naming Organic Compounds
```mermaid
flowchart TD
    A[Organic Compound] --> B[Identify Parent Chain]
    B --> C[Identify Functional Groups]
    C --> D{Multiple Functional Groups?}

    D -->|No| E[Name based on functional group suffix]
    D -->|Yes| F[Determine highest priority group for suffix]

    F --> G[Other groups become prefixes]

    B --> H[Number carbons to give functional groups lowest numbers]
    H --> I[List substituents alphabetically with position numbers]
```

## Functional Group Priority Hierarchy
```mermaid
graph TD
    A[Functional Group Priority] --> B[1. Carboxylic Acids: -COOH]
    A --> C[2. Esters: -COOR]
    A --> D[3. Amides: -CONH₂]
    A --> E[4. Nitriles: -C≡N]
    A --> F[5. Aldehydes: -CHO]
    A --> G[6. Ketones: C=O]
    A --> H[7. Alcohols: -OH]
    A --> I[8. Amines: -NH₂]
    A --> J[9. Ethers: -O-]
    A --> K[10. Alkenes: C=C]
    A --> L[11. Alkynes: C≡C]
    A --> M[12. Alkanes: C-C]
```

## Common Polyatomic Ions
```mermaid
graph TD
    A[Common Polyatomic Ions] --> B[Positive Ions]
    A --> C[Negative Ions]

    B --> B1[NH₄⁺: Ammonium]
    B --> B2[H₃O⁺: Hydronium]

    C --> C1[OH⁻: Hydroxide]
    C --> C2[CN⁻: Cyanide]
    C --> C3[NO₃⁻: Nitrate]
    C --> C4[NO₂⁻: Nitrite]
    C --> C5[SO₄²⁻: Sulfate]
    C --> C6[SO₃²⁻: Sulfite]
    C --> C7[PO₄³⁻: Phosphate]
    C --> C8[CO₃²⁻: Carbonate]
    C --> C9[HCO₃⁻: Hydrogen carbonate]
    C --> C10[ClO₃⁻: Chlorate]
    C --> C11[ClO₂⁻: Chlorite]
    C --> C12[ClO⁻: Hypochlorite]
    C --> C13[ClO₄⁻: Perchlorate]
    C --> C14[CH₃COO⁻: Acetate]
```

## Key Relationships Between Naming Systems
```mermaid
graph TD
    A[Chemical Nomenclature Systems] --> B[IUPAC System]
    A --> C[Common Names]

    B --> D[Systematic Rules]
    D --> E[Structure-Based Naming]
    D --> F[Composition-Based Naming]

    C --> G[Historical Names]
    C --> H[Trivial Names]

    I[Acid-Base Relationships] --> J[Acid → Anion]
    J --> J1[Remove H+]
    J --> J2[-ic acid → -ate]
    J --> J3[-ous acid → -ite]
```

## Progression of Oxidation States in Nomenclature
```mermaid
graph LR
    A[Oxidation States] --> B[Per-X-ate: Highest]
    B --> C[X-ate]
    C --> D[X-ite]
    D --> E[Hypo-X-ite: Lowest]

    F[Example: Chlorine] --> G[ClO₄⁻: Perchlorate]
    G --> H[ClO₃⁻: Chlorate]
    H --> I[ClO₂⁻: Chlorite]
    I --> J[ClO⁻: Hypochlorite]
```

## Note
For the concept maps to render properly, you'll need a Markdown viewer that supports Mermaid diagrams. Many modern Markdown editors and viewers support this syntax, including GitHub, GitLab, and VSCode with the appropriate extensions.
