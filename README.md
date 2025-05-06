# Accelerator for ozIMMU

Acceleration codes for the Ozaki-scheme on integer matrix multiplication units.

## Important Notice

To use these codes, [ozIMMU](https://github.com/enp1s0/ozIMMU) is required.

Therefore, users must agree to the license terms of ozIMMU in addition to the license for these codes.

**When citing these codes, please also include a citation for ozIMMU.**

## Usage

Compile [ozIMMU](https://github.com/enp1s0/ozIMMU) with our files instead of the same name files in `src` of the original ozIMMU.

- Codes in `src_errfree_sum` (ozIMMU_EF) reduce the accumuration in FP64 in ozIMMU.
- Codes in `src_nearest_split` (ozIMMU_RN) offer an alternative splitting method and produce more accurate results than ozIMMU when the numbers of slices are the same.
- Codes in `src_nearest_split+errfree_sum` (ozIMMU_H) provides the hyblid method of the above and produce more accurate results faster than ozIMMU.

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
