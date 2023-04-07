# Diagrammatic reasoning for Logic Graphs

Algorithms:
- build a logic graph for the initial concept
- build a tree applying the rules until it is possible:
  - ⊓<sup>+</sup>-rule:

    [](rules/rule1.png)
  - ⊓<sup>-</sup>-rule:

    [](rules/rule2.png)
  - ∃<sup>+</sup>-rule:

    [](rules/rule3.png)
  - ∃<sup>-</sup>-rule:

    [](rules/rule4.png)
- if each branch of the tree contains a clash, the initial concept is inconsistent. Clash:

  [](rules/clash.png)
- otherwise, it is consistent

Examples:
- inconsistent: [Person ⊓ ∀eats.Plant ⊓ ¬(Person ⊓ ∀eats.(Plant ⊔ Dairy))](inconsistent/inconsistent1.html) (A person who is vegan, but not a vegetarian, i.e. a person who eats only plants, but eats not only plants or dairy)
- consistent: [Person ⊓ ∀eats.Plant ⊓ ∀eats.(Plant ⊔ Dairy)](consistent/consistent1.html) (A person who is vegan and vegeratian, i.e. a person who eats only plants and only plants or dairy)
