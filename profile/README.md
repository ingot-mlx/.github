# ingot

An LLM inference engine for Apple silicon, written in Swift with hand-written Metal kernels.

- **MLX-format weights**, no Python at runtime, served through an OpenAI-compatible API.
- **Mixture-of-experts first**: experts can be streamed from the SSD, so a 35B MoE runs on a 16 GB Mac, and the engine tells you what fits on yours before you download anything.
- **Speculative decoding** with DFlash drafters, on by default where it pays off, and exact: the same tokens as without it.
- Needs an **M5 or later** and **macOS 27**.

**Repository:** [ingot-mlx/ingot](https://github.com/ingot-mlx/ingot) · **Models:** [huggingface.co/ingot-mlx](https://huggingface.co/ingot-mlx), calibrated 4-bit MLX conversions that also load in mlx-lm.
