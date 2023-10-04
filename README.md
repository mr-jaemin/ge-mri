## GE MRI research
- Documentations (How-to)
  - [GE Diffusion tensor (gradient directions)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GE_tensor.pdf)
    - Consolidated information for users who want to generate a custom tensor or convert existing table/file to a GE format.
    - Multi-shell DTI on GE scanners
    - [Pre-loaded multi-shell diffusion tensor files](https://github.com/mr-jaemin/ge-mri/tree/main/tensor)
      - [ABCD (tensor4321.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor4321.dat)
      - [UK Biobank (tensor521.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor521.dat)
      - [ADNI3 Advanced (tensor1127.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1127.dat)
      - [HCP Lifespan (tensor1225.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1225.dat)
  - [GE fMRI Slice Timing information](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GE_fMRI_Slice_Timing_Info_Rev5.pdf)
    - [GE Diffusion slice timing](https://github.com/rordenlab/dcm2niix/issues/635) 
  - Distortion Correction for EPI (fMRI/DTI)
    - [B0 fieldmap acuisition/processing](https://github.com/mr-jaemin/ge-mri/tree/main/B0fieldmap)
    - EPI with phase-encoding polarity (AP/PA)
      - [How to get two sets of spin-echo EPI for fMRI a.k.a “SpinEchoFieldMap”](https://github.com/mr-jaemin/ge-mri/blob/main/doc/SE_EPI_fMRI_Fieldmap.pdf)
      - [Type-in PSDs for EPI (fMRI/Diffusion) with phase-encoding polarity](https://github.com/mr-jaemin/ge-mri/blob/main/doc/GE_EPI_PhaseEncoding.pdf)
    - [ABCD epi_pepolar prototype's flipped issue with solution](https://github.com/mr-jaemin/ge-mri/blob/main/doc/ABCD_epi_pepolar.pdf) 
- [GE MR DICOM tags & BIDS](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM)
  - [AIR Recon DL](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#air-recon-dl)   
  - [Acceleration](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#acceleration)
- [GE MR DICOM examplers](https://github.com/mr-jaemin/ge-mri/tree/main/data)
  - [AIR Recon DL](https://github.com/mr-jaemin/ge-mri/tree/main/data#ge-air-recon-dl)
  - [Acceleration BIDS validation dataset](https://github.com/mr-jaemin/ge-mri/tree/main/data#ge-acceleration-bids-validation-dataset)

## Change List related to GE MR
- [dcm2niix](https://github.com/mr-jaemin/ge-mri/tree/main/dcm2niix)

