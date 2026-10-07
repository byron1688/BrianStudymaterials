# Brian Study Materials

Reviewed study materials with Chinese and English reading options.

## Read online

**[Open the Transformer Study Guide](https://byron1688.github.io/BrianStudymaterials/)**

Open this link on any computer, tablet, or phone. No download or GitHub login is required. Use the language buttons at the top of the guide to switch languages. Each language contains all 13 topics, formulas, diagrams, and references.

## Transformer Study Guide

The guide is based on Alan Ritter's CS4641 Neural Networks for Text lectures, with explanations checked against the original lecture and research papers.

Topics include:

- RNN limitations and encoder–decoder attention
- Self-Attention, Query/Key/Value, scaling, and multiple heads
- Positional encoding and its limitations
- Transformer Encoder and Decoder blocks
- Causal masking, Cross-Attention, and Teacher Forcing
- BPE and WordPiece tokenization
- BERT, GPT, T5, and interview self-checks

The review corrects notation, BERT's masking scheme, positional-encoding claims, lecture attribution, and diagram omissions. Attention weights in the diagrams are illustrative, not measured model outputs.

## Read offline

Download [the HTML guide](transformer/transformer-study-guide-bilingual.html) and open it in a browser. Its text, diagrams, and language switch work offline. External research-paper links require internet access.

GitHub's repository file view displays HTML source. Use the online guide above for the rendered reading experience.

## Repository files

- [Bilingual Transformer guide](transformer/transformer-study-guide-bilingual.html)
- [Review notes in Chinese](transformer/REVIEW.zh-CN.md)
- `index.html`: entry page for the hosted guide
- `.nojekyll`: serves the static files directly through GitHub Pages

## References

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- [BERT](https://aclanthology.org/N19-1423/)
- [ELMo](https://aclanthology.org/N18-1202/)
- [WordPiece tokenization](https://huggingface.co/learn/llm-course/en/chapter6/6)
- [T5](https://arxiv.org/abs/1910.10683)

This is an independent study aid, not an official course publication. Original lecture PDFs are not included.
