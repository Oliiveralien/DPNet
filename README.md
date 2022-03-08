# DPNet
This repo contains the code, results and evaluations of the paper ''Dual-Pyramidal Image Inpainting with Dynamic Normalization'' submitted in TCSVT.

## Introductoin
Deep autoencoder-based approaches have achieved significant improvements on restoring damaged images, yet they still suffer from artifacts due to the inadequate representation and inaccurate regularization of existing features.
In this paper, we propose a dual-pyramidal inpainting framework called DPNet to address these two limitations, which seamlessly integrates sufficient feature learning and dynamic regularization within an autoencoder network.
Specifically, to exhaustively extract multi-scale features, we adopt layer-wise pyramidal convolution in encoder, which provides an arbitrary combination pool of various receptive fields.
Subsequently, to tackle the patch deterioration problem in previous cross-scale non-local schemes, we further propose a Pyramidal Attention Mechanism (PAM) in decoder to acquire finer patches directly from learned layers.
Mutually benefited with pyramidal features extraction in encoder, the dissemination space for non-local pixels in our PAM is notably enlarged to pyramidal level, thus significantly benefiting the feature representation.
Moreover, to avoid the mask error accumulation in existing works, a dynamic normalization mechanism utilizing the spatial mask information updated in encoder is introduced, which further ensures the feature integrity and consistency.
Such a dual-pyramidal structure along with dynamic normalization significantly improve the inpainting quality, outperforming existing competitors.
Comprehensive experiments conducted on three benchmark datasets demonstrate that our DPNet performs favorably against the state-of-the-arts.
