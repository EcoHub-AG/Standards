# Standards
This project contains the schemas for the standards used in the data exchange via DXP or SAF

# Usage
There are multiple ways to download the schemas for further use, for example for code generation.

## 1. Git
Directly use git to clone the repository. However, be aware that this will include all available standards and version. 

## 2. Sparse Checkout
Use the sparse-checkout mechanismn to directly check out the files you need via git:

1. Clone the repository:
   ```
   git clone --no-checkout https://github.com/EcoHub-AG/Standards.git
   cd Standards
   ```

2. Set up sparse-checkout:
   ```
   git config core.sparseCheckout true
   git checkout main -- sparse-checkout-configs/
   
   # chose the correct config file for the desired standard and version from ./sparse-checkout-configs
   cp sparse-checkout-configs/offer_nlpi_v0.3.0.txt .git/info/sparse-checkout
   ```

3. Checkout the files:
   ```
   git read-tree -mu HEAD
   ```


## 3. Download consolidated zip
Alternatively, you can download a zip file containing only the files for a specific version from the available 
releases.