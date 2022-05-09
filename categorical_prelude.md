# Categorical Prelude

| name       | descriptive name                   |	denotation    | definition
|------------|------------------------------------|---------------|--------------------------
| black      | self                               | <img src="/img/black_circle.png" title="black circle" style="height:1em;"/>   | a
| black	     | self                               | <img src="/img/black_line.png" title="black line" style="height:1em;"/>   | a(b)
| white      | meta                               | <img src="/img/white_circle.png" title="white circle" style="height:1em;"/>   | B
| white	     | meta                               | <img src="/img/white_line.png" title="white line" style="height:1em;"/>   | A->B
| yellow     | join                               | <img src="/img/yellow_circle.png" title="yellow circle" style="height:1em;"/> |	let a: A; let b: A
| yellow     | join                               | <img src="/img/yellow_line.png" title="yellow line" style="height:1em;"/> |	let f: A->C; let f: B->C
| orange     | split                              | <img src="/img/orange_circle.png" title="orange circle" style="height:1em;"/> |	let a: A; let a: B
| orange     | split                              | <img src="/img/orange_line.png" title="orange line" style="height:1em;"/> |	let f: A->B; let f: A->C
| red        | less                               | <img src="/img/red_circle.png" title="red circle" style="height:1em;"/>       |	≤
| red        | less                               | <img src="/img/red_line.png" title="red line" style="height:1em;"/>       |	≤
| blue       | more                               | <img src="/img/blue_circle.png" title="blue circle" style="height:1em;"/>     |	≥
| blue	     | more                               | <img src="/img/blue_line.png" title="blue line" style="height:1em;"/>     | ≥
| purple     | up                                 | <img src="/img/purple_circle.png" title="purple circle" style="height:1em;"/> |	+
| purple     | up                                 | <img src="/img/purple_line.png" title="purple line" style="height:1em;"/> |	+
| green	     | down                               | <img src="/img/green_circle.png" title="green circle" style="height:1em;"/>   |	-
| green	     | down                               | <img src="/img/green_line.png" title="green line" style="height:1em;"/>   |	-
| pink	     | parallel                           | <img src="/img/pink_circle.png" title="pink circle" style="height:1em;"/>     |	\|\|
| pink	     | parallel                           | <img src="/img/pink_line.png" title="pink line" style="height:1em;"/>     |	\|\|
| grey	     | perpendicular                      | <img src="/img/grey_circle.png" title="grey circle" style="height:1em;"/>     |	⊥
| grey	     | perpendicular                      | <img src="/img/grey_line.png" title="grey line" style="height:1em;"/>     |	⊥
| monad	     | monad                              | <span title="diagram looks like a Hydrogen Atom">H</span>                   | <img src="/img/monad.png" alt="monad" style="height:1em;"/>
| inequality | triangle inequality                | <span title="diagram expresses {forall a,b,c. a + b ≥ c} irrespective of dimensionality">≠</span>                          | <img src="/img/triangle_inequality.png" alt="inequality" style="height:1em;"/>

# Terms
| rank | kind | type | value | notes
|------|------|------|-------|-------
| <img src="/img/monad.png" style="height:1em;"/> | 1 | model | myFancyDomainModel | This is the rank 1 unit diagram. Models are the natural units of Algebraic Categories.
| <img src="/img/observe.png" style="height:1em;"/> | 2 | observe | : | This is a rank 2 diagram describing the relations and affinities of the rank 1 unit diagram.
| <img src="/img/white_circle.png" style="height:1em;"/> | Metric | perplexity | (1,2,(3,4),5) | Metrics are the natural units of Meta Categories. (1,(2,3)) > (1,∞,4) > (1,∞).
| <img src="/img/yellow_line.png" style="height:1em;"/> | (Term,Metric) -> Term | minimize | minimize(term,perplexity) | Objective Functions are the natural units of Join Categories.
| <img src="/img/yellow_line.png" style="height:1em;"/> | (Term,Metric) -> Term | maximize | maximize(term,perplexity) |
| <img src="/img/orange_line.png" style="height:1em;"/> | ∀ A,B. A->B = B->A | ∀ a,b. a(b) = b(a) | = | Equations are the natural units of Split Categories.

# Notes
- ≤ ≥ + - || ⊥: These categories exist to describe soundness holes. A soundness hole occurs when you can prove both True and False. Minimally, to eliminate a soundness hole, a prelude must somehow prune either all True or all False constructions from each Judgement.
- triangle_inequality.png: note the usage of black in both the object and functor position.

# References
- [Categorial Foundations of Mathematics](https://ncatlab.org/nlab/show/foundation%20of%20mathematics)
