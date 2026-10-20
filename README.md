# DINOv2 for Abstract Art Retrieval
Evaluating DINOv2 for content-based image retrieval (CBIR) on abstract art, focusing on instance retrieval. Tested on Schüttbilder (action paintings) by Hermann Nitsch.

## Context
Capstone project for the course *GenAI for Humanists*, Instructor: Renato Rocha Souza, MA Digital Humanities, University of Vienna, WS 2026. Instructor: Renato Rocha Souza

## Motivation
Image retrieval models are largely trained to recognise objects, and cataloguing relies on describable content. Non-figurative painting offers neither, which leaves abstract art largely unexplored in image retrieval. DINOv2 learns texture, structure and composition directly from pixels, without labels or text, which makes it a promising candidate for this domain.

## Research Questions
**Main:** To what extent are DINOv2 embeddings suitable for instance retrieval of abstract paintings in a closed corpus?

**Sub:** How robust are these embeddings when the query image is degraded (cropping, oblique angles, smartphone photos)?

## Data
A closed, single-artist corpus of digitised Schüttbilder (action paintings) by Hermann Nitsch, provided by the Nitsch Foundation and the Atelier Hermann Nitsch. The images are protected by copyright and are used for research purposes only. They are not distributed in this repository.

## Approach
Frozen DINOv2 features, indexed with FAISS. Details will follow.

## Evaluation
| Run | Query | Purpose |
|---|---|---|
| Sanity check | identical image | verifies the pipeline |
| Baseline | synthetic transformations (crop, rotation, brightness) | basic re-identification |
| Robustness | real-world smartphone photos | performance under real distortion |

## Status
Work in progress.

## License
Code: MIT License

## References
Oquab, M. et al. (2024). DINOv2: Learning Robust Visual Features without Supervision. *Transactions on Machine Learning Research*. Model by Meta AI, released under the Apache 2.0 License.
