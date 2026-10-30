# BIM2BEM Geometry GPT

This package contains the configuration materials for the custom GPT that
implements Agents 1–7 for IFC geometry processing and initial EnergyPlus
IDF generation.

## Included Materials

- BIM2BEM_Geo_Instructions.txt: primary workflow instructions.
- basic_setup.txt: initial IDF template and setup content.
- IFCextraction.py: Agent 1 IFC entity extraction.
- IFCtracing.py: Agent 2 IFC relationship tracing.
- IFCgeometry_filter.py: Agent 3 geometry filtering and attributes.
- IFCtoIDFGeometry.py: Agent 4 IDF-ready surface generation.
- IFC_obc.py: Agent 5 boundary-condition assignment and surface matching.
- convert_to_ep_ready.py: Agent 6 EnergyPlus vertex-order conversion.
- bim_geo_to_idf.py: Agent 7 initial IDF generation.
- Result_with_Input_and_Prompt/: case-study screenshots for the prompts and
  outputs of Agents 1–7.

## Custom GPT Setup

Upload this directory's instruction and helper files as knowledge files for the
Geometry GPT. Enable Code Interpreter and Data Analysis so the workflow can
run the supplied Python scripts and create the JSON and IDF artifacts described
in ../../BIM2BEM_Input_Output/Output/.

The helper scripts use Python standard-library modules. The workflow expects an
IFC input file such as
../../BIM2BEM_Input_Output/Input/4StoryFactoryBuilding.ifc.

## Example Prompts and Outputs

The screenshots in `Result_with_Input_and_Prompt/` visually document the
case-study interactions and outputs for Agents 1–7. They supplement, rather
than replace, the machine-readable artifacts in
`../../BIM2BEM_Input_Output/Output/`.

## Invocation and Recorded Labels

Use `Run Agent N` to initiate a geometry task. The original `Run Step N`
prompts remain accepted aliases. Recorded screenshots and output filenames
retain their original Step labels, corresponding to Agents 1–7.
