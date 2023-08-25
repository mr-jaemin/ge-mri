## `dcm2niix` change list related to GE MR
This page is intended for providing consolidated change list in [dcm2niix](https://github.com/rordenlab/dcm2niix) for GE MR users from newest to oldest, relative to stable releases.
### [The latest stable release version (download)](https://github.com/rordenlab/dcm2niix/releases): 11-April-2023
The above link provides pre-compiled stable release version of dcm2niix on Winodows, MacOS, Linux
### Build the development branch
This is the simplest way to compile dcm2niix on a Linux or MacOS.
```
git clone --branch development https://github.com/rordenlab/dcm2niix.git dcm2niix_dev
cd dcm2niix_dev/console
make
./dcm2niix
```
### Change list for GE MR users from newest to oldest, relative to stable releases.
- [Support GE feet first DTI bvec](https://github.com/rordenlab/dcm2niix/issues/737)
  - v1.0.20230807+
  - [Code changes](https://github.com/rordenlab/dcm2niix/pull/736)
- [Improve GE fieldmap (3db0map and B0map)](https://github.com/rordenlab/dcm2niix/pull/741)
  - v1.0.20230807+
- [Improve GE BIDS autodetection](https://github.com/rordenlab/dcm2niix/commit/459fed06a2fedea9bcace006b93594f8c1cc00dd)
  - v1.0.20230731+
- [Improve BidsGuess for GE](https://github.com/rordenlab/dcm2niix/commit/6c96364f45504fc46c3e42b7eec6b8783c5486fb)
  - v1.0.20230731+
- [BidsGuess](https://github.com/rordenlab/dcm2niix/tree/development/BidsGuess)
  - v1.0.20230731+ 
  - This experimental feature is designed to aid wrappers that use dcm2niix to create BIDS compatible datasets
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/0d48e95839ba767dcda4bf0bdccff23810a0c642)
- [Improve GE TotalReadoutTime with interpolation](https://github.com/rordenlab/dcm2niix/pull/725) 
  - v1.0.20230706+
- [GE epiRT slicetiming (REVSLICEORDER vs SLICEORDER)](https://github.com/rordenlab/dcm2niix/issues/723)
  - v1.0.20230623+
  - dissociate REVSLICEORDER from SLICEORDER (#723)
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/14c66a1fd2a80c1346d0fccb08db14ecc263db66)
### [Stable releases: version 11-April-2023](https://github.com/rordenlab/dcm2niix/releases/tag/v1.0.20230411)
- [Improve detection of GE isotropic diffusion](https://github.com/rordenlab/dcm2niix/issues/690)
  - v1.0.20230315+   
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/c2a4b28e7ae7d4761a959b44dda5c6c34986b300)
- New BIDS for AIR Recon DL: DeepLearning, DeepLearningDetail
  - v1.0.20230210+  
  - [GE MR DICOM tags: AIR Recon DL](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM)
  - [GE MR DICOM tags: Acceleration](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM)
  - [Sample DICOM](https://github.com/mr-jaemin/ge-mri/tree/main/data)
  - [BIDS discussion for Deep Learning and Compressed Sensing](https://github.com/bids-standard/bids-specification/issues/1407)
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/19738600abc66f2107a57161527fa7ecc5347072)
- [New BIDS for HyperSense: CompressedSensingFactor](https://github.com/rordenlab/dcm2niix/commit/19738600abc66f2107a57161527fa7ecc5347072)
  - v1.0.20230210+
- [Improve GE PROGRES' REV_POL](https://github.com/rordenlab/dcm2niix/issues/674)
  - v1.0.20230201+
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/865dab86761bbc73f89ea4df6a5655679af28a75)
- [BIDS sidecar field ParallelReductionFactorInPlane](https://github.com/rordenlab/dcm2niix/issues/672)
  - v1.0.20230127+
  - [Code changes](https://github.com/rordenlab/dcm2niix/commit/e53c23038a1d137712c9ed3d8809c5be6baffb0a)
- [GE Diffusion SliceTiming](https://github.com/rordenlab/dcm2niix/issues/635)
  - v1.0.20220915+
  - Added SliceTiming for GE Diffusion
  - New keys added in JSON for GE diffusion:
    - `NumberOfDiffusionDirectionGE`
    - `NumberOfDiffusionT2GE`
    - `TensorFileNumberGE`
    - `DiffGradientCyclingGE`
  - [Code changes](https://github.com/rordenlab/dcm2niix/pull/636/)
- [Improved GE software version reading (version 30)](https://github.com/rordenlab/dcm2niix/issues/634)
  - v1.0.20220915+ 
### [Stable releases: version 20-July-2022](https://github.com/rordenlab/dcm2niix/releases/tag/v1.0.20220720)
- [GE Direct field mapping deltaTE (or TE1/TE2)](https://github.com/rordenlab/dcm2niix/issues/617)
  - Adding `EchoTime1` and `EchoTime2` to BIDS JSON
- [GE ShimSetting in BIDS JSON](https://github.com/rordenlab/dcm2niix/issues/608)
  - Adding `ShimSetting` to BIDS JSON from `ShimGradientX`, `ShimGradientY`, `ShimGradientZ`
- [Improve b-value detection](https://github.com/rordenlab/dcm2niix/issues/602)
  - Subtracting `BIAS_FOR_BVALUE` from private tag b-value if needed 
