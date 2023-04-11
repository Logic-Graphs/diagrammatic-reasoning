# Diagrammatic reasoning for Logic Graphs

Algorithms:
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

Examples:
- inconsistent: [Person ⊓ ∀eats.Plant ⊓ ¬(Person ⊓ ∀eats.(Plant ⊔ Dairy))](inconsistent/inconsistent1.html) (A person who is vegan, but not a vegetarian, i.e. a person who eats only plants, but eats not only plants or dairy)
- consistent: [Person ⊓ ∀eats.Plant ⊓ ∀eats.(Plant ⊔ Dairy)](consistent/consistent1.html) (A person who is vegan and vegeratian, i.e. a person who eats only plants and only plants or dairy)
