# Perplexity 😵
The Perplexity 😵 language is a notational semantic for documenting neural networks through diagrams.

![MNIST Keras Python Perplexity](/img/mnist_keras_python_perplexity.png)

# Scope
This visual language was created to help document neural networks.
The language may not be suitable to formally describe all characteristics of all possible neural network configurations.

# Format
The Perplexity 😵 language consists of two languages: one [textual](/syntax.md), the other [visual](/syntax.md).
The visual language consists of two-dimensional images that can be created in Paint or other visual editors.
The textual language consists of [Typed Lambda Calculus expressions](https://github.com/andrew-johnson-4/LSTS#readme).

Any file, textual or visual, defines a substitution rule according to its filename.
For example, a diagram "helpful.png" may be referred to as "helpful" in other textual language documentation.

# Why?
UML is not information dense enough and often leaves out important details. Mathematical Notation is too information dense and often repeats itself. Perplexity 😵 is created specifically to model Neural Networks and cuts a lot of corners by specializing itself for this use-case.

# Checklist for Documenting a Model

1. How many languages/algebras are you going to use in documentation?
> This determines the rank of your model. It is recommended to use different colored lines and circles
> when swapping between languages.
> For example, if you just want to document a TensorFlow model, then you only need Python and your model's rank will be 1.

2. What prelude do you want to use?
> A prelude will include some terms that you then don't need to define again yourself. Each prelude defines its own ranks, kinds, types, values etc. Please consider using a prelude.

# List of Preludes
Preludes are optional-ish.
- [Categorical Prelude](/categorical_prelude.md)
- [TensorFlow Prelude](/tensorflow_prelude.md)
