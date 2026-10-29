# Subexponential elliptic-curve discrete logarithms

The manuscript is available in [subexponential-ecdl.pdf](subexponential-ecdl.pdf).

The [ECC2K-130 experiments](experiments/ecc2k130/README.md) include an executable
scalar Boolean tensor-contraction implementation, a characteristic-two
coordinate encoder, tests, and reproducible result records.

```bash
cd experiments/ecc2k130
python -m pip install -r requirements.txt
python -m unittest -v test_ecc2k test_tensor_contraction test_tensor_encoding
python tensor_cli.py recursive-check
```

The implementation does not recover the ECC2K-130 challenge scalar or demonstrate
a practical subexponential attack. The manuscript's default parameters select
exact summation at the encoded challenge's size. See the experiment's
[results](experiments/ecc2k130/RESULTS.md) and
[implementation notes](experiments/ecc2k130/TENSOR_IMPLEMENTATION.md).
