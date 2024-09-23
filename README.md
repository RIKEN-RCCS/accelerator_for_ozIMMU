# Accelerator for ozIMMU

Acceleration codes for the Ozaki-scheme on integer matrix multiplication units.

## Important Notice

To use these codes, the [ozIMMU](https://github.com/enp1s0/ozIMMU) is required.
Therefore, users must agree to the license terms of the ozIMMU in addition to the license for these codes.
When citing these codes, please also include a citation for the ozIMMU.

## Usage

Compile the [ozIMMU](https://github.com/enp1s0/ozIMMU) with our files instead of the same name files in `src` of the original ozIMMU.

- Codes in `src_errfree_sum` reduce the accumuration in FP64 in the ozIMMU.
- Codes in `src_nearest_split` offer an alternative splitting method and produce more accurate result than the ozIMMU when the numbers of slices are the same.
- Codes in `src_nearest_split+errfree_sum` provides the hyblid method of the above and produce more accurate result faster than the ozIMMU.

Complex matrix multiplication is not provided.

## Citation

```
@misc{uchino2024performanceenhancementozakischeme,
      title={Performance Enhancement of the Ozaki Scheme on Integer Matrix Multiplication Unit},
      author={Yuki Uchino and Katsuhisa Ozaki and Toshiyuki Imamura},
      year={2024},
      eprint={2409.13313},
      archivePrefix={arXiv},
      primaryClass={cs.DC},
      url={https://arxiv.org/abs/2409.13313},
}
```
