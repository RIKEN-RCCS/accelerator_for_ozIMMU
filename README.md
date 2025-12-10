# Accelerator for ozIMMU

This repository provides patch files that enhance the performance of the Ozaki scheme implementation in the original [ozIMMU](https://github.com/enp1s0/ozIMMU).
By replacing the files in the `src` directory of ozIMMU with the corresponding files from this repository, the enhanced functionality becomes available.

## Important Notice

Using the codes in this repository requires the original ozIMMU.
Users must accept the license terms of ozIMMU in addition to the license of this repository.

When citing this repository, please also cite ozIMMU.

## Usage

Replace the original source files in `src` of ozIMMU with the files provided in this repository, then compile ozIMMU as usual.

- Files in `src_errfree_sum` (ozIMMU_EF) reduce FP64 accumulation overhead in ozIMMU.
- Files in `src_nearest_split` (ozIMMU_RN) introduce an alternative splitting method that yields higher accuracy under the same number of slices.
- Files in `src_nearest_split+errfree_sum` (ozIMMU_H) combine both techniques to deliver higher accuracy and improved performance compared with the original ozIMMU.
- File in `acc` apply n-blocking to the INT8 GEMM calls in the original ozIMMU. This optimization prevents the performance degradation observed in INT8 GEMM for large matrices, improving scalability without altering ozIMMU's algorithmic structure.

Complex matrix multiplication is not provided.

## Citation

```
@article{doi:10.1177/10943420241313064,
      author = {Yuki Uchino and Katsuhisa Ozaki and Toshiyuki Imamura},
      title ={Performance enhancement of the Ozaki Scheme on integer matrix multiplication unit},
      journal = {The International Journal of High Performance Computing Applications},
      volume = {39},
      number = {3},
      pages = {462--476},
      year = {2025},
      doi = {10.1177/10943420241313064},
      URL = {https://doi.org/10.1177/10943420241313064},
}
```
