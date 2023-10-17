## GEHC B0 fieldmap

The document [GEHC_B0Mapping_Info.pdf](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_B0Mapping_Info.pdf) is intended to provide information about B0 field mapping on GE HealthCare scanners. All these information is expected to help research users to acquire B0 maps and to facilitate users who wish to apply distortion corrections to EPI data (fMRI and DTI) with B0 fieldmap using popular research tools like FSL/AFNI/SPM.

### Acquisition
The document [GEHC_B0Mapping_Info.pdf](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_B0Mapping_Info.pdf) provides a detailed instruction how to acquire B0 map using product PSDs.
- Type-in PSD: `B0rf` (2D) or `3db0mamp` (3D)
- The default protocol described in the above document is available to download:
  - [B0 Mapping Protocol (MR29.1)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/B0_Mapping_PSDs_MR29.1_Protocols_v1.2.tar.gz)
  - Instructions to install the protocol are given in [GEHC_B0Mapping_Info.pdf](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_B0Mapping_Info.pdf).

### DICOM To NIfTI Converter
We recommend to use [`dcm2niix`](https://github.com/rordenlab/dcm2niix) from Chris Rorden.
- `dcm2niix` converts/split a B0 map series into a fieldmap image in Hertz and the corresponding magnitude image.

  For example:
  
  ![Screenshot 2023-10-06 at 10 18 36 AM](https://github.com/mr-jaemin/ge-mri/assets/72111485/66e83248-b551-49a3-9f3d-0bd901262484)

  B0Map_fieldmaphz.json reports `Units`, `EchoTime1`, and `EchoTime2`: 
    ```json
    {
      "PulseSequenceName": "3db0map",
      "Units": "Hz",
      "EchoTime1": 0.004544,
      "EchoTime2": 0.006816,
    }
    ```
- We recommend to use the [latest stable release of dcm2niix](https://github.com/rordenlab/dcm2niix/releases)
  - dcm2niix version v1.0.20210410 or later required (see [here](https://github.com/rordenlab/dcm2niix/issues/501) for more details)
  - Refer to the [change list in dcm2niix](https://github.com/mr-jaemin/ge-mri/tree/main/dcm2niix)


### Processing Tools
- FSL
  - Preprocessing: [Making Fieldmap Images for FEAT](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FUGUE/Guide#SIEMENS_and_GEHC_data)
    - including the usage of the `fsl_prepare_fieldmap` command-line tool (see below)
    - FSL 6.0.7.1 or later
  - [B0 unwarping in FEAT Pre-Stats](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FEAT/UserGuide#Pre-Stats)
```
  Usage: fsl_prepare_fieldmap <scanner> <phase_image> <magnitude_image> <out_image> <deltaTE (in ms)> [--nocheck]

  Prepares a fieldmap suitable for FEAT from SIEMENS or GEHC data - saves output in rad/s format
  <scanner> must be SIEMENS or GEHC_FIELDMAPHZ
  <phase_image> should be the phase difference for SIEMENS and the fieldmap in HERTZ for GEHC_FIELDMAPHZ
  <magnitude image> should be Brain Extracted (with BET or otherwise)
  <deltaTE> is the echo time difference of the fieldmap sequence - find this out form the operator (defaults are *usually* 2.46ms on SIEMENS)
            (defaults are *usually* 2.304ms for GEHC 2D-B0MAP at 3.0T and 2.272 ms GEHC 3D B0MAP at 3.0T)
  --nocheck supresses automatic sanity checking of image size/range/dimensions

   e.g. fsl_prepare_fieldmap SIEMENS images_3_gre_field_mapping images_4_gre_field_mapping fmap_rads 2.65
   e.g. fsl_prepare_fieldmap GEHC_FIELDMAPHZ 3dB0map_fieldmaphz mag_3dB0map fmap_rads 2.272
```
   - `Fsl_prepare_fieldmap` (GUI)

     ![Screenshot 2023-10-17 at 3 20 59 PM](https://github.com/mr-jaemin/ge-mri/assets/72111485/63147caf-bb8c-41ab-98cc-2d428c3f9fda)
