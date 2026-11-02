<h1 align="center">Asynchronous Flow Map Language Models</h1>

<div align="center">

**[Chanhyuk Lee](https://david3684.github.io)**<sup>1</sup>, **[Wonjung Kim](https://wjhjkim.github.io/)**<sup>1</sup>, **[Patrick Pynadath](https://patrickpynadath1.github.io/)**<sup>2</sup>, **[Jaehoon Yoo](https://sites.google.com/view/jaehoon-yoo/홈)**<sup>1</sup>, \
**[Satoshi Hayakawa](https://satoshi-hayakawa.github.io/)**<sup>3</sup>, **[Ruqi Zhang](https://ruqizhang.github.io/)**<sup>2</sup>, **[Jinwoo Kim](https://jw9730.github.io/)**<sup>†1</sup>, **[Seunghoon Hong](https://maga33.github.io/)**<sup>†1</sup>

<sup>1</sup>KAIST &nbsp; <sup>2</sup>Purdue University &nbsp; <sup>3</sup>The University of Tokyo &nbsp; <sup>†</sup>Equal advising

</div>

<div align="center">

[![arXiv](https://img.shields.io/badge/arXiv-2610.42018-b31b1b?style=flat&logo=arxiv)](https://arxiv.org/abs/2610.42018)

</div>

> [!NOTE]
> 🚧 **Code and checkpoints are coming soon.**

## TL;DR

<!-- TODO: figures/overview.png -->

The order in which tokens are predicted in language modeling has a profound impact on the quality of generated sequences.
Autoregressive and masked diffusion models iteratively fill in tokens and can exploit such orderings across generation steps, but how to leverage an ordering for one-step parallel language modeling is unclear.
We introduce asynchronous flow map language models (aFMLMs), which incorporate prediction order into one-step modeling by learning the flow maps of asynchronous flows.
These flows specify an ordering through a tokenwise time schedule that controls the relative denoising progress of tokens.
We formulate a general class of asynchronous flows that admit both prescribed and learned, state-adaptive schedules, show that they define valid flow maps, and develop new methods for their flow map distillation.
The resulting models can generate all tokens in a single forward pass by internalizing the ordering encoded in the flow into their hidden computations.
On Sudoku solving and code generation for GSM8K math word problems, aFMLM establishes new state-of-the-art one-step performance.

## Release Plan

- [ ] Training code: diffusion-forcing teacher and aFMLM distillation (TinyGSM, Sudoku)
- [ ] Evaluation code: GSM8K and Sudoku
- [ ] Pretrained checkpoints: teachers and aFMLM students

## BibTeX

```bibtex
@article{lee2026asynchronous,
    title={Asynchronous Flow Map Language Models},
    author={Chanhyuk Lee and Wonjung Kim and Patrick Pynadath
            and Jaehoon Yoo and Satoshi Hayakawa and Ruqi Zhang
            and Jinwoo Kim and Seunghoon Hong},
    journal={arXiv preprint arXiv:2610.42018},
    year={2026},
}
```
