Chemistry Adapters
==================

![Python](https://img.shields.io/badge/python-3.6-blue.svg)
[![PEP8](https://img.shields.io/badge/code%20style-pep8-orange.svg)](https://www.python.org/dev/peps/pep-0008/)


A place for quick conversions between languages using SMILES as the base key. A Quick Converter From Amino Acid Sequences to Smiles and Back again. 


Installation 
============

ChemistryAdapters is going to be distribute via PyPi and as the content store grows we can expand it to other pieces of software
making it accessible to all regardless of what you use. Alternatively, you could have a glance at the source code and copy/paste
it yourself.

```

pip install 

```
Using Adapters
=====================

Currently only one adapter is implemented which is the Amino Acids to SMILES and back again.

```python

test = 'RSTEFGHIKLADPQ'


adapter = AminoAcidAdapter()
smiles = adapter.convert_amino_acid_sequence_to_smiles(test)

>>> NC(CCCCNC(N)=N)C(NC(CO)C(NC(C(C)([H])O)C(NC(CCC(O)=O)C(NC(CC1=CC=CC=C1)C(NC([H])C(NC(CC1=CNC=N1)C(NC(C(CC)([H])C)C(NC(CCCCN)C(NC(CC(C)C)C(NC(C)C(NC(CC(O)=O)C(NC(C2CCCN2)C(NC(CCC(N)=O)C(NCC(O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O)=O

sequence = adapter.convert_smiles_to_amino_acid_sequence(smiles)

>>> RSTEFGHIKLADPQ

```

Quick Start
===========

Just with no dependencies, intialize the class and there you go! All the common and rare groups of the world
at your disposal 

```

from global_chem import GlobalChem

global_chem = GlobalChem()

compounds = global_chem.rings_in_drugs_smiles
```

Variables List
==============

| Chemical List                       | Languages                    | Variables                                                                                                                  | References                                                                                                                                                                                                                                     |
|-------------------------------------|------------------------------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amino Acids                         | IUPAC/SMILES/SMARTS          | amino_acid_side_smiles, amino_acid_side_smarts                                                                             | Common Knowledge                                                                                                                                                                                                                               |
| Essential Vitamins                  | Preferred Name/SMILES/SMARTS | vitamins_smiles, vitamins_smarts                                                                                           | Common Knowledge                                                                                                                                                                                                                               |
| Common R Group Replacement          | Preferred Name/SMILES/SMARTS | r_groups_replacements_smiles, r_groups_replacements_smarts                                                                 | Takeuchi, Kosuke, et al. “R-Group Replacement Database for Medicinal Chemistry.” Future Science OA, vol. 7, no. 8, Sept. 2021, p. FSO742. future-science.com (Atypon), https://doi.org/10.2144/fsoa-2021-0062.                                 |
| Common Organic Solvents             | IUPAC/SMILES/SMARTS          | common_organic_solvents_smiles, common_organic_solvents_smarts                                                             | Fulmer, Gregory R., et al. “NMR Chemical Shifts of Trace Impurities: Common Laboratory Solvents, Organics, and Gases in Deuterated Solvents Relevant to the Organometallic Chemist.”Organometallics , vol. 29, no. 9, May 2010, pp. 2176–79.   |
| Open Smiles                         | IUPAC/SMILES/SMARTS          | open_smiles_functional_groups_smiles, open_smiles_functional_groups_smarts                                                 | OpenSMILES Home Page. http://opensmiles.org/.                                                                                                                                                                                                  |
| IUPAC Blue Book (CRC Handbook) 2003 | Preferred Name/SMILES/SMARTS | iupac_blue_book_radical_smiles, iupac_blue_book_radical_smarts, iupac_blue_book_rings_smiles, iupac_blue_book_rings_smarts | Chemical Rubber Company. CRC Handbook of Chemistry and Physics: A Ready-Reference Book of Chemical and Physical Data . Edited by David R. Lide, 85. ed, CRC Press, 2004.                                                                       |
| Rings in Drugs                      | IUPAC/SMILES/SMARTS          | rings_in_drugs_smiles, rings_in_drugs_smarts                                                                               | Taylor, Richard D., et al. “Rings in Drugs.” Journal of Medicinal Chemistry, vol. 57, no. 14, July 2014, pp. 5845–59.  ACS Publications, https://doi.org/10.1021/jm4017625.                                                                    |
| Common Regex Patterns               | Mol2                         | common_regex_patterns                                                                                                      |                                                                                                                                                                                                                                                |

Genesis
=======

GlobalChem was created because I noticed I was using the same variable across multiple scripts and figure it would be useful
for folk to have.

- Lead Developer [Suliman sharif](http://sulstice.github.io/)
- Artwork [Elena Chow](http://www.chowelena.com/)

* * * * *

Citation
========

If you find my personal dictionary is useful please feel free to cite me under:

```

Sul, Elena Y. Chow: "Sul's Dictionary" 

```
External links
==============


