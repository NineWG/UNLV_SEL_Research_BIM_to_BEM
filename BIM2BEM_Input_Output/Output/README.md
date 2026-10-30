# Workflow Outputs

These files are the intermediate and final artifacts from the case-study
agentic AI-assisted BIM-to-BEM workflow.

| Agent task | File |
| --- | --- |
| Agent 1: IFC entity extraction and units | seeds.json, ifc_units.json |
| Agent 2: IFC entity tracing | step2_traced.json |
| Agent 3: Geometry filtering and attributes | step3_geometry.json |
| Agent 4: IDF-ready geometry | step4_idf_geometry.json |
| Agent 5: Boundary-condition assignment | step5_obc.json |
| Agent 6: EnergyPlus-ready geometry | step6_ep_ready.json |
| Agent 7: Initial IDF generation | step7_output.idf |
| Agent 8: Energy-parameter enrichment | enriched_output.idf |

The JSON files are intermediate evidence files rather than standalone
EnergyPlus input models. The final workflow IDF is enriched_output.idf.

Filenames retain their original Step labels for compatibility with the
processing scripts and recorded case-study outputs.
