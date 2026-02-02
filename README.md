# Verification of the F-PKI Client
This project aims to verify the policy mode of the FP-PKI Browser Extension (forked from their [GitHub repository](https://github.com/cyrill-k/fpki-firefox-extension)). 

## Verifying the project
After setting up [Gobra](https://github.com/viperproject/gobra), run Gobra with the following command:
`run -p verify-fpki-firefox-extension/app/go_wasm/cache_v2 -I verify-fpki-firefox-extension/stubs -I verify-fpki-firefox-extension/app -I verify-fpki-firefox-extension/stubs/gostd`

The flag `--parallelizeBranches` can be added to improve verification runtime, although the prover might crash occasionally. 

Note, because of a recent syntax change in Gobra, this project currently only verifies with a Gobra version of up to (including) commit e48c03a.
