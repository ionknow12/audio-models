# kookie-models

Model files that [Kookie](https://github.com/ionknow12) downloads on first use. Nothing else lives here.

## htdemucs-v1.onnx (release `htdemucs-v1`)

Meta's **Hybrid Transformer Demucs** (`htdemucs`, 4 sources: drums, bass, other, vocals),
converted to ONNX for Kookie's built-in stem separation. Only the network is in the file;
the STFT/iSTFT and segment cross-fades run in Kookie. Weights are stored as float16 and
cast to float32 when loaded (the maths is float32).

- Source: https://github.com/facebookresearch/demucs — MIT License, Copyright (c) Meta Platforms, Inc. and affiliates.
- SHA-256: `f3ad66657fa57e1fa2622aa70475e011361afbe324bd16f4754c75be5f3b7d4b` (90,561,457 bytes)
- Inputs: `mix` [1,2,343980], `spec` [1,4,2048,336]. Outputs: `spec_out` [1,4,4,2048,336], `wave_out` [1,4,2,343980].
