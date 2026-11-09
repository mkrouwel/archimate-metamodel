# Metamodel diagrams for the ArchiMate® specifications

Complete specialization hierarchies for ArchiMate® 3.2 and ArchiMate 4, each in a single diagram. Every specialization is traced to the figure or section of the specification that supports it. Links that the text implies but no figure draws are marked separately.

> **Disclaimer:** These diagrams are an independent interpretation of the ArchiMate specifications. They are not an official publication of The Open Group, and The Open Group does not endorse them. They may contain errors; please report any you find.

## Contents

| File | Description |
| --- | --- |
| `archimate-3.2/archimate-3.2-metamodel.svg` | ArchiMate 3.2 hierarchy, scalable vector image |
| `archimate-3.2/archimate-3.2-metamodel.png` | ArchiMate 3.2 hierarchy, bitmap image |
| `archimate-4/archimate-4-metamodel.svg` | ArchiMate 4 hierarchy, scalable vector image |
| `archimate-4/archimate-4-metamodel.png` | ArchiMate 4 hierarchy, bitmap image |

## Reading the diagrams

Each diagram is one specialization tree, running from Model and Concept down to every concrete element, relationship and junction.

| Notation | Meaning |
| --- | --- |
| Dark gray fill (`#ABABAB`) | Active structure element |
| Mid gray fill (`#DDDDDD`) | Behavior element |
| Light gray fill (`#F3F3F3`) | Passive structure element |
| White fill (`#FFFFFF`) | Abstract element, not used directly in models |
| Solid arrow, hollow head | Specialization drawn in a figure of the specification |
| Dashed arrow, hollow head | Implied specialization: stated or required by the text, not drawn in any figure |
| Filled diamond | Composition (Model is composed of Concepts) |

The fill colors follow the convention the specifications use in their own metamodel figures (ArchiMate 3.2, Section 3.9; ArchiMate 4, Section 3.8). ArchiMate 4 only distinguishes white for abstract and gray for concrete concepts, but its figures still use the same shades per aspect, so both diagrams use the 3.2 scheme.

Only specialization is shown. The other metamodel relationships, such as assignment, serving and realization, are left out to keep the hierarchy readable.

## Element counts

| | ArchiMate 3.2 | ArchiMate 4 |
| --- | --- | --- |
| Concrete elements | 60 | 42 |
| Specialization arrows | 119 | 77 |
| Of which implied | 31 | 1 |

Concrete elements exclude relationships and junctions.

## Implied specializations

### ArchiMate 4

| Specialization | Support |
| --- | --- |
| Technology Internal Active Structure Element → Internal Active Structure Element | Figure 10-1 draws it only under Technology Active Structure Element. Section 3.4.1 counts nodes among the internal active structure elements, and Role and Collaboration (Section 4.1) require it. |

### ArchiMate 3.2

The layer figures (Figures 52, 53, 58, 64, 70, 71, 75, 82, 83 and 91) stop at layer-level abstract elements. They connect to the generic elements only through the note at Figure 5, which presents the generic metamodel as a template that each layer specializes.

| # | Specialization | Support |
| --- | --- | --- |
| 1–3 | Business, Application and Technology Internal Active Structure Element → Internal Active Structure Element | Note at Figure 5 |
| 4–6 | Business, Application and Technology Internal Behavior Element → Internal Behavior Element | Note at Figure 5 |
| 7 | Business Passive Structure Element → Passive Structure Element | Note at Figure 5 |
| 8 | Technology Passive Structure Element → Passive Structure Element | Note at Figure 5; Section 10.4 |
| 9 | Data Object → Passive Structure Element | Section 9.4 |
| 10 | Technology Active Structure Element → Active Structure Element | Note at Figure 5 |
| 11–19 | Business, Application and Technology Process, Function and Interaction → Process, Function and Interaction | Figure 12 draws only the generic types |
| 20–22 | Business, Application and Technology Collaboration → Collaboration | Figure 12; Sections 8.2.3, 9.2.2 and 10.2.4 |
| 23–25 | Business, Application and Technology Service → External Behavior Element (Service) | Figures 4 and 5 |
| 26–28 | Business, Application and Technology Interface → External Active Structure Element (Interface) | Figures 4 and 5 |
| 29–31 | Business, Application and Technology Event → Event | Figure 4; Implementation Event → Event is drawn in Figure 106 |

## Sources for the explicit specializations

### ArchiMate 4

- Top level: Figures 3-3 and 5-1
- Structure and behavior: Figures 3-4 and 4-1
- Composite elements: Figures 4-9, 8-5 and 12-1
- Motivation: Figure 6-1
- Strategy: Figure 7-1
- Business, application and technology: Figures 8-1, 9-1, 10-1 and 10-11
- Implementation and migration: Figure 12-1
- Removed and merged elements: Appendix E.4

### ArchiMate 3.2

- Top level and relationships: Figures 1 and 21
- Structure and behavior: Figures 4 and 12
- Composite elements: Figures 18 and 68
- Motivation: Figure 34
- Strategy: Figure 46
- Business: Figures 53, 58 and 64
- Application: Figures 71 and 75
- Technology and physical: Figures 83, 91, 97 and 99
- Implementation and migration: Figure 106

## How the diagrams were checked

1. The source files of both diagrams were parsed and every specialization arrow was listed.
2. Each arrow was matched to a figure that draws it or a section that states it.
3. Arrows with only textual support were marked as implied and dashed.
4. Each element was checked to appear exactly once and to have a parent.
5. For ArchiMate 4, every element listed as removed or merged in Appendix E.4 was confirmed absent.

## The specifications

The specifications are not included in this repository. Get them from [The Open Group](https://www.opengroup.org).

## Contributing

Open an issue if you find an error, read a passage differently, or know of a figure that settles an implied link. Please cite the section or figure number, not quoted text.

## License

The diagrams and this README are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The license covers only the diagrams and documentation in this repository, not the ArchiMate specifications.

ArchiMate is a registered trademark of The Open Group.
