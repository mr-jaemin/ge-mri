## Welcom to GE HealthCare MRI research documention!
This page will hopefully provide information for GE HeahthCare MRI research users, with a focus of neuroscience users. 

### Change List related to GEHC MR
- [dcm2niix](https://github.com/mr-jaemin/ge-mri/tree/main/dcm2niix)


### How-to Documentation
  - [GEHC Diffusion Phase-Encoding Polarity & No Interpolation](https://github.com/mr-jaemin/ge-mri/tree/main/How-to/Diffusion_PSD)
    - This guide explains how to manage phase-encoding polarity and native resolution in reconstruction in GE HealthCare diffusion EPI using type-in PSDs such as epi2alt, epi2as, epi2asalt. 
  - [GEHC Diffusion tensor (gradient directions)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_tensor.pdf)
    - Consolidated information for users who want to generate a custom tensor or convert existing table/file to a GEHC format.
    - [GEtensor-app](https://getensor.streamlit.app/) is a web-based tool created with Python and Streamlit to facilitate the viewing and conversion of GE diffusion tensor files in a user-friendly format. 
    - [New locations of diffusion tensor files from MR30.0](https://github.com/mr-jaemin/ge-mri/blob/main/tensor/README.md#locations-of-diffusion-tensor-files)
    - [Pre-loaded multi-shell diffusion tensor files on GEHC scanners](https://github.com/mr-jaemin/ge-mri/tree/main/tensor)
      - [ABCD (tensor4321.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor4321.dat)
      - [UK Biobank (tensor521.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor521.dat)
      - [ADNI3 Advanced (tensor1127.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1127.dat)
      - [HCP Lifespan (tensor1225.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1225.dat)
    - [Emmanuel Caruyer's web appliation](http://www.emmanuelcaruyer.com/q-space-sampling.php) to design multi-shell sampling schemes
      - [python script to conver to GE tensor format](https://github.com/naveau/qspacesampling2GE) by Mikael Naveau
  - [GEHC fMRI Slice Timing information](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_fMRI_Slice_Timing_Info.pdf)
  - [GEHC Diffusion slice timing](https://github.com/rordenlab/dcm2niix/issues/635) 
  - Distortion Correction for EPI (fMRI/DTI)
    - [B0 fieldmap acquisition/processing](https://github.com/mr-jaemin/ge-mri/tree/main/B0fieldmap)
    - EPI with phase-encoding polarity (AP/PA)
      - [How to get two sets of spin-echo EPI for fMRI a.k.a “SpinEchoFieldMap”](https://github.com/mr-jaemin/ge-mri/blob/main/doc/SE_EPI_fMRI_Fieldmap.pdf)
      - [Type-in PSDs for EPI (fMRI/Diffusion) with phase-encoding polarity](https://github.com/mr-jaemin/ge-mri/blob/main/doc/GEHC_EPI_PhaseEncoding.pdf)
    - [ABCD epi_pepolar prototype's flipped issue with solution](https://github.com/mr-jaemin/ge-mri/blob/main/doc/ABCD_epi_pepolar.pdf) 
- [GEHC MR DICOM tags & BIDS](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM)
  - [AIR Recon DL](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#air-recon-dl)   
  - [Acceleration](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#acceleration)
### Sample Datasets
- [GEHC MR DICOM examplers](https://github.com/mr-jaemin/ge-mri/tree/main/data)
  - [AIR Recon DL](https://github.com/mr-jaemin/ge-mri/tree/main/data#ge-air-recon-dl)
  - [Acceleration BIDS validation dataset](https://github.com/mr-jaemin/ge-mri/tree/main/data#ge-acceleration-bids-validation-dataset)


