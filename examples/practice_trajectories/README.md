# Practice PDB Trajectory Files (multi-model, for animation)

Each file is a multi-model PDB (`MODEL`/`ENDMDL` blocks) that can be played
frame-by-frame in PyMOL (`mclear; load file.pdb; mplay`), VMD, ChimeraX,
3Dmol.js, NGL, etc.

| File | Frames | Atoms | System | Force field | Source |
|------|--------|-------|--------|-------------|--------|
| `adk_adenylate_kinase_charmm27_98frames.pdb` | 98 | 3341 | Adenylate kinase (AdK), open→closed transition | CHARMM27 (NAMD/CHARMM DCD) | MDAnalysis test suite (Temple Univ. / ASU) |
| `trpzip2_amber_101frames.pdb` | 101 | 223 | Trpzip2 β-hairpin peptide (ACE/NME-capped) | AMBER (parm7) | Amber-MD/pytraj test suite (Amber consortium: Rutgers, UCSF, Stony Brook, ...) |
| `peptide_14mer_amber_100frames.pdb` | 100 | 332 | 14-residue capped peptide in water | AMBER (parm7) | Amber-MD/pytraj test suite |
| `ala2_dipeptide_amber_501frames.pdb` | 501 | 22 | Alanine dipeptide (ACE–Ala–NME), classic conformational-sampling system | AMBER | mdtraj example data (Pande lab, Stanford) |
| `trpcage_1L2Y_nmr_38models.pdb` | 38 | ~304/model | Trp-cage miniprotein (TC5B), NMR ensemble — direct download, already multi-model PDB | experimental (NMR) | RCSB entry 1L2Y, mirrored by Amber-MD/pytraj |

Notes:
- Files 1–4 were converted to multi-model PDB from the original AMBER/CHARMM
  trajectory formats (DCD / AMBER NetCDF / HDF5) with mdtraj 1.11.2. The raw
  source files are kept in `originals/`.
- File 5 is the NMR model ensemble as deposited; useful for practicing
  animation with the exact file you'd download from the PDB.
- MODEL numbering in the AdK file starts at 0 (mdtraj convention); most
  viewers handle this fine.
