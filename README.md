The results of U2UT Model with GRU based phoneme (target) decoder, Conformer Encoder block set to 4 and Phoneme decoder block set to 1, MHSA set to 4 and MSCA set to 4,
sequence length set to 600, d_model set to 512, and dropout set to 0.4 on 1980/420 parallel audio data split of English and Yoruba.
The training was carried out with Adam optimiser (lr = 0.0001) without a scheduler. Label smoothing (0.1) was used for the cross-entropy loss function during computation.

It also contains the performance metrics of U2UT Model with same set up above except the used of 6 and 2 encoder and decoder layers respectively for each of: 
(i) U2UT Model with CosineAnnealingWarmRestartLR with Adam optimser with lr = 1e-4.
(ii) U2UT Model with ReducedOnPlateauLR with Adam optimser with lr = 1e-4.
(iii) U2UT Model without a scheduler, with Adam optimser with lr = 1e-4.

The arguments set for the schedulers are highlighted below:
CosineAnnealingWarmRestartLR: It was set to reduce from maximum learning rate of 1e-4 to 1e-6 over the first 10 epochs, and same reduction for subsequent multiples of 10 epochs for other cycles.
ReducedOnPlateauLR: It was set to optimise the average validation loss and reduce the current learning rate by a factor of 0.5 if consecutive 3 epochs run (patience window) does not improve average validation loss. 
Without a scheduler, just Adam optimiser alone with same lr as above
