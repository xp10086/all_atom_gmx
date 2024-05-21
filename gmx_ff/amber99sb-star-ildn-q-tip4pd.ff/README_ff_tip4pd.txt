Amber99sb*-ildn-q force field with tip4pd water:

Amber99sb*-ildn-q FF from Robert Best repository 
- Best, De Sancho, Mittal, Biophys. J. 2012
- https://github.com/bestlab/force_fields

TIP4P-D water model from Kara Grotz
- She adapted the TIP4P/2005 parameters manually to make tip4pd topology
- Discarded the positions in topology files (simply use the tip4p2005.gro in the best force field), but saved the new parameters to tip4pd.itp

Adapted the following files in the force field:
- Added tip4pd.itp
- Added entry "tip4p-D" in aminoacids.rtp
- Added lines for "HW_tip4p-D" and "OW_tip4p-D" in atomtypes.atp
- Added entry for tip4p-d in ffnonbonded.itp (here, the rescaled LJ-interactions can be seen in the scaled epsilon value)
- Copied tip4p2005.gro from FF amber99sb*-ildn (amber99sb*-ildn-q did not have that water model by default); this needs to be called by gmx solvate -cs
- Added line for tip4pd in watermodels.dat
- modified ion parameters

pSer has been added
