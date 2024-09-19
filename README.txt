# Define potential
pair_style flare
pair_coeff    * * lmp.flare

#Computational uncertainty, which can significantly reduce the speed of computation
#compute unc all flare/std/atom L_inv_lmp.flare sparse_desc_lmp.flare
#compute MaxUnc all reduce max c_unc
#dump a all custom 10 maxunc.atom id type x y z c_unc