# AlphaCrop
split AlphaFold 2.x and 3.x models by confidence. Works on both pdb and cif files. Needs biopython bio.pdb module.

Run with

    python alphacrop.py --filename mystructure.pdb

or mystructure.cif. If needed, explicitly specify file format with the --file_format flag

Confidence defined by Deepmind, each input into multiple files made up of:
- only very high confidence regions (plDDT > 90)
- only confident regions and above (plDDT > 70)
- only low concfidence regions and above, discarding very low confidence (plDDT > 50)

Essentially splits the file by b-factor column, generating 3 files.

Also available as colab here  https://colab.research.google.com/drive/1kfF_Kkozi5ox8mVebqKgvc7UEWdXWpnf?usp=sharing
