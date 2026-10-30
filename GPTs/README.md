# Agentic AI-Assisted Workflow Configurations

This directory contains the configuration materials for the eight agents used
in the case study, implemented through two customized GPT configurations.

| Directory | Agents | Responsibility |
| --- | --- | --- |
| BIM2BEM_Geometry | Agents 1–7 | IFC extraction and tracing, geometry processing, boundary assignment, and initial IDF generation. |
| BIM2BEM_Enrichment | Agent 8 | Traceable energy-input enrichment and model-readiness checks. |

## Configuration Design

Each agent follows instructions specifying its inputs, processing tools,
expected outputs, verification requirements, and permitted corrective actions.
The user initiates tasks, reviews intermediate outputs, and guides corrections.
The Geometry configuration executes reusable processing scripts, with code
adaptation or repair when necessary. The Enrichment configuration interprets
available information and selects applicable inputs through the prescribed
source hierarchy. Information passes between configurations through explicit
intermediate files.

The two configurations were used because the combined geometry-processing and
enrichment rules exceeded the instruction-field capacity of a single
configuration in the case study.

## Reconstructing the Configurations

For each configuration, use the applicable instruction file and companion
knowledge files from its directory. Enable Code Interpreter and Data Analysis.
Enable Web Search for enrichment when official prototype, code, or reference
sources must be consulted.

The included files document the case-study configuration and its agent labels.
A custom GPT deployment can change as the underlying ChatGPT product evolves;
the instruction files, scripts, and stored artifacts support reconstruction
and inspection of the workflow.

## Agent Numbering and Compatibility

Geometry instructions accept `Run Agent 1` through `Run Agent 7` and retain
the corresponding `Run Step N` prompts as aliases. Agent 8 uses the initial
IDF, original IFC, processed geometry evidence, building type, and location.
The enrichment files named `BIM2BEM_Step_00_...` through
`BIM2BEM_Step_08_...` define internal procedures within Agent 8. They are not
the workflow's Agents 1–8.

## Example Prompts and Outputs

`BIM2BEM_Geometry/Result_with_Input_and_Prompt/` contains the recorded
interactions for Agents 1–7, and
`BIM2BEM_Enrichment/Result_with_Input_and_Prompt/` contains the interaction
for Agent 8. The screenshots retain the original Step labels. Use the
accompanying machine-readable scripts and workflow artifacts for reproduction.
