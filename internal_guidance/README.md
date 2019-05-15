This directory contains data related to experiments with applying recurrent
neural networks for internal guidance for connection tableau proofs.

- a directory `leancop_mizar_proofs` contains 13818 connection tableau proofs of
Mizar theorems obtained with use of leanCoP
- a file `numbers_to_clauses_dictionary` contains enumeration of all clauses
  appearing in the proofs, simplified by putting a symbol `VAR` in place of all
  variables and `SKLM` in place of all Skolem symbols
- directories `cls_to_1_2_3_cls`, `cls_to_1_cls`, `cls_to_2_cls`,
  `cls_to_3_cls`, `lits_to_1_2_3_cls`, `lits_to_1_cls`, `lits_to_2_cls`
  and `lits_to_3_cls` contain training, validation and testing data for
  training NMT model for the task of predicting subsequent 1, 2 or 3 clauses in
  the proof from the sequence of preceding literals or clauses. Each of the
  folders contains files:
  - `train.in`, `train.out`
  - `dev.in`, `dev.out`
  - `test.in`, `test.out`
  These are input and output sequences for NMT, split into trainind, validation
  and testing. Additionally, files `vocab.in`, `vocab.out` contain vocabulary
  of the input and output sequences, which are required for NMT models.
  (Some large training files are compressed.)

