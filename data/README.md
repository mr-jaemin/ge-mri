# GE MR DICOM examplers

## GE AIR Recon DL  

[3D Ax T1 MPRAGE with DL High sample (145 MB)](https://gehealthcare-amer.my.salesforce.com/sfc/p/30000001F94O/a/3a000000YKLC/hc86mVNJvwRToWDW.2iHxI8zxRLKLmxpuXIZumsUtM4)

![AIR_Recon_DL_T1_MPRAGE_exam7892](https://user-images.githubusercontent.com/72111485/218240653-0ba91254-a60b-416e-ad09-cdcbbb729fef.png)

The relavant [DICOM tag](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#air-recon-dl) is described in [this page](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#air-recon-dl)

![Screen Shot 2023-02-10 at 3 28 41 PM](https://user-images.githubusercontent.com/72111485/218191319-2959b15a-1be9-4487-a358-89af53e63fc7.png)

[AIR_Recon_DL_images_exam10_target.tar (362.4MB) (dummy dataset)](https://gehealthcare-amer.my.salesforce.com/sfc/p/30000001F94O/a/3a000000YKLM/z_IPNy.idRXUugGO1P4sPjMO5BEcWGOPaX_ntc7MgT4)

| Folder                      | Series No. | Recon DL Stregth | Type      |
| --------------------------- | ---------- | ---------------- | --------- |
| 02_3D_Ax_T1_MP_RAGE_DL_Off  | 2          | Off              | 3D        |
| 04_Ax_DWI_ALL_DL_High       | 4          | High             | 2D        |
| 05_Ax_DWI_ALL_DL_Medium     | 5          | Medium           | 2D        |
| 06_Ax_DWI_ALL_DL_Low        | 6          | Low              | 2D        |
| 07_Ax_DWI_ALL_DL_Off        | 7          | Off              | 2D        |
| 08_3D_Ax_T1_MP_RAGE_DL_High | 8          | High             | 3D        |
| 09_DTI_DL_High              | 9          | High             | 2D        |
| 10_DTI_DL_Off               | 10         | Off              | 2D        |
| 11_Ax_T2_PROPELLER_DL_Off   | 11         | Off              | 2D        |
| 12_Ax_T2_PROPELLER_DL_High  | 12         | High             | 2D        |
| 13_Ax_T2_FLAIR_FS_DL_High   | 13         | High             | 2D        |
| 14_Ax_T2_FLAIR_FS_DL_Off    | 14         | Off              | 2D        |
| 15_Sag_PD_frFSE_DL_High     | 15         | High             | 2D        |

## GE MR Acceleration BIDS validation dataset

[e10_exam12_T1_MPRAGE_Acceleration_t17.tar (371.4MB) (dummy dataset)](https://gehealthcare-amer.my.salesforce.com/sfc/p/30000001F94O/a/3a000000YKJV/4x7le_OZaIGqLKUzIh4JlTQuKZxI0eIv0relvnX9KVE)

The relavant [DICOM tags and BIDS metadata fields](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#acceleration) (stored in sidecar JSON files) are described in [this page](https://github.com/mr-jaemin/ge-mri/tree/main/DICOM#acceleration)

![Screen Shot 2023-02-01 at 9 27 05 AM](https://user-images.githubusercontent.com/72111485/216192223-479acb29-6f76-4027-b681-7b1d369f0e57.png)


| Folder                 | Series No. | Acceleration Phase | Acceleration Slice | Acceleration HyperSense |
| ---------------------- | ---------- | ------------------ | ------------------ | ----------------------- |
| 02_T1_MPRAGE           | 2          | 1                  | 1                  | 1                       |
| 03_T1_MPRAGE_P2S1      | 3          | 2                  | 1                  | 1                       |
| 04_T1_MPRAGE_P1S2      | 4          | 1                  | 2                  | 1                       |
| 05_T1_MPRAGE_P2S2      | 5          | 2                  | 2                  | 1                       |
| 06_T1_MPRAGE_P2_5S1    | 6          | 2.5                | 1                  | 1                       |
| 07_T1_MPRAGE_P1S2_5    | 7          | 1                  | 2.5                | 1                       |
| 08_T1_MPRAGE_P1_2S1    | 8          | 1.2                | 1                  | 1                       |
| 09_T1_MPRAGE_P1_2S1_44 | 9          | 1.2                | 1.44               | 1                       |
| 10_MPRAGE_P2S1H1_24    | 10         | 2                  | 1                  | 1.24                    |

