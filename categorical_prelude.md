This prelude is derived from [a categorical view of typed lambda calculus](https://ncatlab.org/nlab/show/lambda-calculus).

# Categorical Prelude

| name       | descriptive name                   |	denotation    | definition
|------------|------------------------------------|---------------|--------------------------
| black      | term                               | <img src="/img/black_circle.png" title="black circle" style="height:1em;"/>   | a
| black	     | term                               | <img src="/img/black_line.png" title="black line" style="height:1em;"/>   | a(b)
| white      | type                               | <img src="/img/white_circle.png" title="white circle" style="height:1em;"/>   | B
| white	     | type                               | <img src="/img/white_line.png" title="white line" style="height:1em;"/>   | A->B
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

# Terms
| rank | kind | type | value | notes
|------|------|------|-------|-------
| <img src="/img/black_line.png" style="height:1em;"/> | Term | term | myFancyDomainModel | Terms are the natural units of Algebraic Categories.
| <img src="/img/white_line.png" style="height:1em;"/> | Metric | perplexity | (1,2,(3,4),5) | Metrics are the natural units of Type Categories. (1,(2,3)) > (1,∞,4) > (1,∞).
| <img src="/img/yellow_line.png" style="height:1em;"/> | (Term,Metric) -> Term | minimize | minimize(term,perplexity) | Objective Functions are the natural units of Join Categories.
| <img src="/img/orange_line.png" style="height:1em;"/> | ∀ A,B. A->B = B->A | ∀ a,b. a(b) = b(a) | = | Equations are the natural units of Split Categories.
| <img src="/img/blue_line.png" style="height:1em;"/> | SoundnessHole | divergent | λa. a a | Soundness Holes are units of More Categories.
| <img src="/img/red_line.png" style="height:1em;"/> | SoundnessExceptionHandler | not divergent | ... | Subsets of divergent languages that do not diverge can be sound. Soundness "exception handlers" are units of Less Categories.
| <img src="/img/green_line.png" style="height:1em;"/> | TermTransformation | α-conversion,η-reduction,... | (λx.M[x]) → (λy.M[y]) | Any reduction/normalization of equivalent terms that does not effect a change in the type signature.
| <img src="/img/purple_line.png" style="height:1em;"/> | TermTransformation | β-reduction | (λx.t)(u) → βt[u/x]	 | Replace bound variables with the argument expression in the body of the abstraction.
| <img src="/img/pink_line.png" style="height:1em;"/> | TypeReduction | T | <img src="/img/simply_typed1.svg" style="height:1em;"/>	<br/> <img src="/img/simply_typed2.svg" style="height:1em;"/> <br/> <img src="/img/simply_typed3.svg" style="height:1em;"/> <br/> <img src="/img/simply_typed4.svg" style="height:1em;"/> | The Type system is strongly normalizing.
| <img src="/img/grey_line.png" style="height:1em;"/> | MetaUnsound | panic | 0xDEADBEEF | False has been proven.


# Notes
- ≤ ≥ + - || ⊥: These categories exist to describe soundness holes. A soundness hole occurs when you can prove both True and False or when the type system refuses to normalize. Minimally, to eliminate a soundness hole, a prelude must somehow prune either all True or all False constructions from each Judgement.

# References
- [Categorial Foundations of Mathematics](https://ncatlab.org/nlab/show/foundation%20of%20mathematics)
