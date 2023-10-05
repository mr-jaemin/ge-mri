## GE B0 fieldmap

The document [GE_B0Mapping_Info.pdf](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GE_B0Mapping_Info.pdf) is intended to provide information about B0 field mapping on scanners by GE HealthCare. All these information is expected to help research users to acquire B0 maps and to facilitate users who wish to apply distortion corrections to EPI data (fMRI and DTI) with B0 fieldmap using popular research tools like FSL/AFNI/SPM.

### Acquisition
The document [GE_B0Mapping_Info.pdf](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GE_B0Mapping_Info.pdf) provides a detailed instruction how to acquire B0 map using product PSDs.
- Type-in PSD: `B0rf` (2D) or `3db0mamp` (3D)
- The default protocol described in the above document is avaialble to download:
  - [B0 Mapping Protocol (MR29.1)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/B0_Mapping_PSDs_MR29.1_Protocols_v1.2.tar.gz)

### DICOM To NIfTI Converter
We recommend to use [`dcm2niix`](https://github.com/rordenlab/dcm2niix) from Chris Rorden.
- `dcm2niix` converts B0 map into a fieldmap in Hertz and the corresponding magnitude:
  - B0Map_fieldmaphz.nii
  - B0Map_fieldmaphz.json, which includes `EchoTime1` and `EchoTime2`
  - B0Map.nii
  - B0Map.json
- We recommend to use the [latest stable release of dcm2niix](https://github.com/rordenlab/dcm2niix/releases)
  - Refer to the [change list in dcm2niix](https://github.com/mr-jaemin/ge-mri/tree/main/dcm2niix) for more details


### Processing Tools
- FSL
  - Preprocessing: [Making Fieldmap Images for FEAT](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FUGUE/Guide#SIEMENS_and_GEHC_data)
    - including the usage of the `fsl_prepare_fieldmap` command-line tool
  - [B0 unwarping in FEAT Pre-Stats](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FEAT/UserGuide#Pre-Stats)
