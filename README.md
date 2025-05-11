# Tilling Presentation


## Description
This repository contains a presentation on tilling, specifically focusing on periodic to aperiodic tilling.

## Content
- `presentation.pdf`: The main presentation file.
- `presentation.tex`: The LaTeX source code for the presentation.
- `presentation.bib`: The bibliography file for the presentation.
- `diagrams/`: A directory containing all the tikz diagrams.



## Resources
https://www.aperiodictiling.org/wpaperiodictiling/index.php/2x2-supertiles/large-supertiles/

### Mermaid diagram of wallpaper groups classification
```mermaid
flowchart TD
    A[Largest rotational order] -->|none| B0(Is there a reflection?)
    A -->|2| B2(Is there a reflection?)
    A -->|3| B3(Is there a reflection?)
    A -->|4| B4(Is there a reflection?)
    A -->|6| B6(Is there a reflection?)


    B0-->|yes| C01(Is there a glide reflection?)
    B0-->|no| C02(Is there a glide reflection?)

    B2-->|yes| C21(Are there reflections in two directions?)
    B2-->|no| C22(Is there a glide reflection?)

    B3-->|yes| C31(Are all rotation centres on mirror lines?)
    B3-->|no| C32((p3))

    B4-->|yes| C41(Are there mirror lines intesecting 45 degrees?)
    B4-->|yes| C42((p4))

    B6-->|yes| C61((p6m))
    B6-->|no| C62((p6))


    C01-->|yes| D01((cm))
    C01-->|no| D02((cm))

    C02-->|yes| D03((pg))
    C02-->|no| D04((p1))

    C21-->|yes| D21(Are all roation centers on mirror lines?)
    C21-->|no| D22((pmg))
    C22-->|yes| D23((pgg))
    C22-->|no| D24((p2))

    C31-->|yes| D31((p3m1))
    C31-->|no| D32((p31m))

    C41-->|yes| D41((p4m))
    C41-->|no| D42((p4g))

    D21-->|yes| E21((pmm))
    D21-->|no| E22((cmm))
```

### TeX Overflow
- https://tex.stackexchange.com/questions/61437/penrose-tiling-in-tikz

### Code
- https://github.com/loopspace/tilings
