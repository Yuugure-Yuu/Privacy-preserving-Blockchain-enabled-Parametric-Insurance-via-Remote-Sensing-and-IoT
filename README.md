Full codes and the dataset will be published as long as the paper *Privacy-preserving Blockchain-enabled Parametric Insurance via Remote Sensing and IoT* is published.



## Running tips



Prover (main part is set up by Haskell and followed by Python, Elliptic Curve Digital Signature (ECDSA) is generated by Go) generated data has to be copied from output file to verifier code.

For verifier, please notice that current code may be temporary code for cost estimation, and right version is annotated.

Feasibility-check code is in ./src/RSP, and the dataset used is the ./data folder.



## Data source



Digital Earth Australia is a project powered by Geoscience Australia. It is a digital platform based on open-sourced geospatial-data management platform Open Data Cube (ODC). The platform features a large collection of Earth observation data from Australia and a Python API for data access. Particularly, the platform provides surface reflectance imagery retrieved from Sentinel-2 ground observation satellites. The satellites provide high spatial resolution (up to 10 m) with 13 spectral bands, including NIR and SWIR. More specifically, we use the Sentinel-2B MSI Definitive ARD product, which contains high-quality surface reflectance data retrieved from Sentinel-2B satellite since 2017, with near-weekly sample frequency.



## Cost estimation



Deployment for sonic verifier:

![2](graphs//2.png)



Deployment for Enhanced verifier:

![2](graphs//4.png)



Enhanced verification:

![3](graphs//3.png)



Unbatched verification:

![1](graphs//1.png)



If we assume that Necessary SRS elements are not stored on chain during deployment, but obtained from trusted third-party during verification, then:



Deployment for Enhanced verifier:

![1](graphs//5.png)



Enhanced verification:

![1](graphs//6.png)





We can estimate the transaction fee regarding [ETH price by the end of 2022 (ETH/USD = 1199.11)](https://ycharts.com/indicators/ethereum_price) and average gas price = 20 gwei.



| Transaction                              | Gas Cost | Estimated USD  |
| ---------------------------------------- | -------- | -------------- |
| Contract Deployment                      | 3194644  | 76.6145913368  |
| Contract Deployment (Enhanced Verifier)  | 2884986  | 69.1883112492  |
| Enhanced Verification                    | 437370   | 10.489094814   |
| Sonic Verification                       | 1740170  | 41.733104974   |
| Enhanced Contract & Verification         | 3322356  | 79.6774060632  |
| Sonic Contract & Verification            | 4934814  | 118.3476963108 |
| Contract Deployment (Enhanced+ Verifier) | 2566978  | 61.5617797916  |
| Enhanced+ Verification                   | 426877   | 10.2374495894  |
| Enhanced+ Contract & Verification        | 2993855  | 71.799229381   |




