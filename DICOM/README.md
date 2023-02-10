# GE MR DICOM tags

## AIR Recon DL
PSD AIR Recon DL GUI

![Screen Shot 2023-02-10 at 3 28 41 PM](https://user-images.githubusercontent.com/72111485/218191319-2959b15a-1be9-4487-a358-89af53e63fc7.png)

| Attribute Name    | Tag         | VR | Example        | Explanation                | BIDS |
| ----------------- | ----------- | -- | -------------- | -------------------------- | ---- |
| Recon DL Strength | (0043,10CA) | LO | [0.75\\High] | Off: The tag doesn't exist |      |
|                   |             |    |                | High: [0.75\\High]       |      |
|                   |             |    |                | Medium: [0.5\\Medium]    |      |
|                   |             |    |                | Low: [0.3\\Low]          |      |

## Acceleration
PSD Acceleration GUI

![Screen Shot 2023-02-01 at 9 20 03 AM](https://user-images.githubusercontent.com/72111485/216160380-45be0aeb-bb6f-40a6-9337-1a21aa934f3f.png)

With HyperSense Option:

![Screen Shot 2023-02-01 at 9 27 05 AM](https://user-images.githubusercontent.com/72111485/216160251-5cac21e1-deab-4cc1-9976-5c2018654b8f.png)

With HyperBand Optoin: 

![Screen Shot 2023-02-01 at 3 47 18 PM](https://user-images.githubusercontent.com/72111485/216160162-33b9ed66-d5ad-4181-8945-d5d9d4012f18.png)


| Attribute Name                | Tag         | VR | Example            | Explanation                        | BIDS                              |
| ----------------------------- | ----------- | -- | ------------------ | ---------------------------------- | --------------------------------- |
| Asset R Factors               | (0043,1083) | DS | [0.5\\0.5]         | The reciprocal of 1st: Phase  Acceleration     | [ParallelReductionFactorInPlane](https://bids-specification.readthedocs.io/en/latest/glossary.html#objects.metadata.ParallelReductionFactorInPlane)    |
|                               |             |    |                    | The reciprocal of 2nd: Slice Acceleration      | [ParallelReductionFactorOutOfPlane](https://bids-specification.readthedocs.io/en/latest/glossary.html#objects.metadata.ParallelReductionFactorOutOfPlane) |
| Multiband Parameters          | (0043,10B6) | LO | [2\\4\\19\\\\\\\\] | 1st: Multiband factor              | [MultibandAccelerationFactor](https://bids-specification.readthedocs.io/en/latest/glossary.html#objects.metadata.MultibandAccelerationFactor)       |
|                               |             |    |                    | 2nd: Slice FOV shift factor        |                                   |
|                               |             |    |                    | 3rd: Calbiration method            |                                   |
| Compressed Sensing Parameters | (0043,10B7) | LO | [1.24\\1\\10\\0]   | 1st: Compressed Sensing(CS) factor |
|                               |             |    |                    | 2nd: CS Flag                       |
|                               |             |    |                    | 3rd: CS data consistency paramter  |
