The results of U2UT Model with GRU based phoneme (target) decoder, Conformer Encoder block set to 4 and Phoneme decoder block set to 1, MHSA set to 4 and MSCA set to 4,
sequence length set to 600, d_model set to 512, and dropout set to 0.4 on 1980/420 parallel audio data split of English and Yoruba.
The training was carried out with Adam optimiser (lr = 0.0001) without a scheduler. Label smoothing was used for the cross-entropy loss function during computation.
