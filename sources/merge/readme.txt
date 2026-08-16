======================================================================
     Obsidian Didone - Font Build Kit (Based on Warcraft-Font-Merger)
======================================================================

[Description]
This directory contains the font merging and patching toolchain, fully 
powered by Warcraft-Font-Merger (WFM) and otfcc. It is designed to link 
the AI-generated Latin base with high-quality CJK glyphs seamlessly.

[Directory Layout]
- SC.TTF          : Raw base Chinese font source (Noto Serif CJK / Source Han Serif)
- cjk.ttf         : A copy of the raw base Chinese font source (Noto Serif CJK / Source Han Serif)
- latin.ttf       : Raw Latin base font generated from Mixfont AI
- otfccdump.exe   : Decodes TTF/OTF into human-readable JSON/OTD data
- otfccbuild.exe  : Compiles JSON/OTD data back into optimized TTF/OTF
- merge-otd.exe   : Core engine of WFM to combine and sort font layers
- merge_auto.bat  : One-click automated merging pipeline
- merge.bat       : Semi-automated/Manual step-by-step font merger
- auto.bat        : Post-processing and packaging script
- pack.bat        : Generates font package structure

----------------------------------------------------------------------
HOW TO RUN THE FONT COMPILER
----------------------------------------------------------------------

Method 1: One-Click Fully Automated Merge (Recommended)
1. Select your generated OBSIDIAN font file and your targeted CJK font file.
2. Drag and drop BOTH font files together directly onto:
   "merge_auto.bat"
3. Wait for the terminal to finish processing. The merged font will be generated.

Method 2: Manual Step-by-Step Merge (Fallback)
If the automated script fails to properly overwrite the English alphabet 
part with the bold/obsidian styled glyphs, use the manual workflow:
1. Double-click to execute "merge.bat".
2. Follow the on-screen prompts to select your CJK font (e.g., "SC.TTF") 
   and the layout configuration (e.g., "out.ttf").
3. Once exported, take the resulting intermediate font file and drag 
   it directly into "auto.bat" to finalize the font container compilation.

----------------------------------------------------------------------
Credits: Special thanks to nowar-fonts/Warcraft-Font-Merger project!
======================================================================
