# DRAW: A Recurrent Neural Network For Image Generation

Karol Gregor, Ivo Danihelka, Alex Graves, Danilo Jimenez Rezende, Daan Wierstra, ICML, 2015

## Summary

This paper introduces a neural network architecture
that generates realistic images sequentially. They
also introduce a differentiable attention mechanism
that allows the network to focus on local regions of the image
during reconstruction. Main contributions:

- The network architecture is similar to other variational
auto-encoders, except that
    - The encoder and decoder are recurrent networks (LSTMs).
    The encoder's output is conditioned on the decoder's
    previous outputs, and the decoder's outputs are iteratively
    added to the resulting distribution from which images are
    generated.
    - The spatial attention mechanism restricts the input region
    observed by the encoder and available to write for the decoder.

## Strengths

- The spatial soft attention mechanism is effective and fully differentiable,
and can be used for other tasks.

- Images generated by DRAW look very realistic.

## Weaknesses / Notes