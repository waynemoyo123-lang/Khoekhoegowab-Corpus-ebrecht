# KhoeKhoegowab Computational Corpus Project

## Overview
This project addresses the critical need for computational tools in the processing of **KhoeKhoegowab (Khoekhoegowab)**, a Khoe-Kwadi language. As an agglutinative language with complex PGN (Person-Gender-Number) marking, KhoeKhoegowab presents significant challenges for standard NLP parsers. This project develops an automated pipeline to synthesize, annotate, and analyze the language to bridge the gap between linguistic theory and digital accessibility.

## Methodology
The project leverages standardized linguistic frameworks to ensure scalability and model compatibility:
- **Annotation Standards:** Shifted from traditional Leipzig Glossing to **Universal Dependencies (UD)** and **CoNLL-U** formats.
- **Data Lifecycle:** The pipeline utilizes a semi-automated iterative process to filter and pre-annotate raw text, specifically focusing on the KhoeKhoegowab Bible corpus.
- **Active Learning:** A "Human-in-the-loop" (HITL) strategy is implemented where human verification is triggered only when model confidence scores fall below a defined threshold (80%).

## Research Roadmap
1.  **Iterative Filtering:** Automated identification of recurrent sentences and lexical units to create a robust seed corpus.
2.  **Model Training:** Training custom dependency parsers on a hybrid dataset of Bible corpora and UD treebanks.
3.  **Constrained LLM Synthesis:** Utilizing the trained parser as a structural constraint to guide Large Language Model (LLM) synthesis, ensuring the generated text adheres to strict grammatical and morphological rules.

## Future Research & Expansion
To move beyond formal text, the project is expanding into **Morphophonological Normalization** to handle the "noisy" reality of conversational speech:
- **Normalization:** Implementing sub-word processing to map colloquial contractions to their lemma forms (e.g., mapping *huit’ma* to *hui tama* or *|har’tab* to *|haratab*).
- **Ellipsis and Syncope:** Creating specialized CoNLL-U layers for elliptical constructions (e.g., resolving *mâitsa mî* to *mâti tsî ta mî*), allowing the model to interpret conversational speech.
- **Synthetic Augmentation:** Developing constraint-based synthesis to simulate rare linguistic structures, mitigating the impact of current data scarcity.

## Status
- **Current Pipeline:** Active.
- **Parsing Accuracy:** ~30% for raw text; currently undergoing iterative improvement via HITL correction.
- **Objective:** To build a fully automated, scalable annotation and synthesis tool for low-resource linguistic environments.
