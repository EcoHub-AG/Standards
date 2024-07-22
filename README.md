# Standards
Schemas for all the standards used in the data exchange via DXP or SAF

## Sparse Checkout
To checkout only the files you need:

1. Clone the repository:
   ```
   git clone --no-checkout https://github.com/EcoHub-AG/Standards.git
   cd Standards
   ```

2. Set up sparse-checkout:
   ```
   git config core.sparseCheckout true
   git checkout main -- sparse-checkout-configs/
   cp sparse-checkout-configs/offer_nlpi_v0.3.0.txt .git/info/sparse-checkout
   ```

3. Checkout the files:
   ```
   git read-tree -mu HEAD
   ```


## Download consolidated zip
Alternatively, you can download a zip file that contains only the files you need from the latest release.