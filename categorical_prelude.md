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
| <img src="/andrew-johnson-4/perplexity/raw/main/img/black_line.png" style="height:1em;"/> | Term | term | myFancyDomainModel | Terms are the natural units of Category Algebras.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/white_line.png" style="height:1em;"/> | Metric | perplexity | (1,2,(3,4),5) | Metrics are the natural units of Type Categories. (1,(2,3)) > (1,∞,4) > (1,∞).
| <img src="/andrew-johnson-4/perplexity/raw/main/img/yellow_line.png" style="height:1em;"/> | (Term,Metric) -> Term | minimize | minimize(term,perplexity) | Objective Functions are the natural units of Join Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/orange_line.png" style="height:1em;"/> | ∀ A,B. A->B = B->A | ∀ a,b. a(b) = b(a) | = | Equations are the natural units of Split Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/blue_line.png" style="height:1em;"/> | SoundnessHole | divergent | λa. a a | Soundness Holes are units of More Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/red_line.png" style="height:1em;"/> | SoundnessExceptionHandler | not divergent | ... | Subsets of divergent languages that do not diverge can be sound. Soundness "exception handlers" are units of Less Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/green_line.png" style="height:1em;"/> | TermTransformation | α-conversion,η-reduction,... | (λx.M[x]) → (λy.M[y]) | Any reductions/normalizations of equivalent terms that do not effect a change in the type signature are grouped into Down Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/purple_line.png" style="height:1em;"/> | TermTransformation | β-reduction | (λx.t)(u) → βt[u/x]	 | Replacing bound variables with the argument expression in the body of an abstraction is the basis of Up Categories. β-reduction is exclusively allowed to introduce changes to the type signatures of terms to account for things like polymorphism.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/pink_line.png" style="height:1em;"/> | TypeReduction | \|\| | $\pi_1(s:\sigma,t:\tau) = s:\sigma$ <br/> $\pi_2(s:\sigma,t:\tau) = t:\tau$ <br/> $(\pi_1(u:\sigma \times \tau),\pi_2(u:\sigma \times \tau)) = u:\sigma \times \tau$ <br/> $t:1 = ()$ | The Type system should be strongly normalizing. Type unification and reduction is the basis of Parallel Categories.
| <img src="/andrew-johnson-4/perplexity/raw/main/img/grey_line.png" style="height:1em;"/> | MetaUnsound | ⊥ | absurd | False has been proven. Unsound type systems are considered "perpendicular" to good language structure.


# Notes
- ≤ ≥ + - || ⊥: These categories exist to describe soundness holes. A soundness hole occurs when you can prove both True and False or when the type system refuses to normalize. Minimally, to eliminate a soundness hole, a prelude must somehow prune either all True or all False constructions from each Judgement.

# References
- [Categorical Foundations of Mathematics](https://ncatlab.org/nlab/show/foundation%20of%20mathematics)
- [A Two-Category perspective of Arbitrary Typed Lambda Calculus](https://www.kurims.kyoto-u.ac.jp/~hassei/papers/ctcs95.pdf)
