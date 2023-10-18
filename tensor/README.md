## GEHC diffusion gradient directions (tensorXX.dat)

I have consolidated [information regarding GE diffusion gradient directions (tensorXX.dat)](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/doc/GEHC_tensor.pdf)) for those who want to generate a custom tensor or convert existing table/file to a GEHC format.

## Locations of diffusion tensor files
### Prior to MR30.0
All tensor file are saved in `/usr/g/bin`

### MR30.0 or later
- GE-preloaded tensor files are located in `/srv/nfs/psd/etc`
- User-provided tensor files should be placed in `/srv/nfs/psd/usr/etc`
- Precedence is given to the GE directory (`/srv/nfs/psd/etc`) when files with the same name exist in both locations


## Pre-loaded multi-shell tensor files
- [tensor4321](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor4321.dat): ABCD (Adolescent Brain Cognitive Development)
- [tensor521](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor521.dat): UK Biobank
- [tensor1127](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1127.dat): ADNI-3 Advanced
- [tensor1225](https://raw.githubusercontent.com/mr-jaemin/ge-mri/main/tensor/tensor1225.dat): HCP Lifespan
