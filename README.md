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

Genesis
=======

I demonstrated I have a need for this so I built a quick one. 

- Lead Developer [Suliman sharif](http://sulstice.github.io/)

* * * * *

Citation
========


```

Sul: "ChemistryAdapters" 

```
External links
==============


