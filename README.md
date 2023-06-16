# Diagrammatic reasoning for Logic Graphs

## Algorithm

- build a logic graph for the initial concept
- build a tree applying the rules until it is possible:
  - ⊓<sup>+</sup>-rule:

    <img src="rules/rule1.png"  width="50%" height="50%">
  - ⊓<sup>-</sup>-rule:

    <img src="rules/rule2.png"  width="50%" height="50%">
  - ∃<sup>+</sup>-rule:

    <img src="rules/rule3.png"  width="50%" height="50%">
  - ∃<sup>-</sup>-rule:

    <img src="rules/rule4.png"  width="50%" height="50%">
- if each branch of the tree contains a clash, the initial concept is inconsistent. Clash:

  <img src="rules/clash.png"  width="50%" height="50%">
- otherwise, it is consistent

## Examples

- inconsistent: a person who is vegan, but not a vegetarian, i.e. a person who eats only plants, but eats not only plants or dairy
<p align="center"><a href="inconsistent/inconsistent1.html">Person ⊓ ∀eats.Plant ⊓ ¬(Person ⊓ ∀eats.(Plant ⊔ Dairy))</a></p>

- consistent: a person who is vegan and vegeratian, i.e. a person who eats only plants and only plants or dairy
<p align="center"><a href="consistent/consistent1.html">Person ⊓ ∀eats.Plant ⊓ ∀eats.(Plant ⊔ Dairy)</a></p>

## Comparison
- Logic Graphs

<img src="comparison/LG.png"  width="50%" height="50%">
- Conceptual Diagrams

<img src="comparison/CD.png"  width="50%" height="50%">
- Relation Graphs

<img src="comparison/RG.png"  width="25%" height="25%">

We compare the complexity of visual syntaxes regarding their graph-theoretic terms.

|    | N of nodes | N of edges | Depth |
| -- | ---------- | ---------- | ----- |
| LG | **_10_** | **_2_** | **_2_** |
| CD | 11 | **_2_** | 3 |
| RG | 13 | 5 | 3 |
