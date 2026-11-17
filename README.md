# chronos2-go-base-part2

Shards 4 through 6 of the 12 that make up Amazon's [Chronos-2](https://huggingface.co/amazon/chronos-2) checkpoint, for [`chronos2-go-base`](https://github.com/pinkhop/chronos2-go-base).

Do not import this module. Import `github.com/pinkhop/chronos2-go-base`, which requires all four parts and assembles them into a ready-to-use model; `go get` fetches the parts automatically. The checkpoint is split across four modules so that each stays small enough for the Go module proxy to serve.


## Contents

| File | Bytes | SHA-256 |
|---|---|---|
| `model-00004-of-00012.safetensors` | 37,759,488 | `3d0bcee7d99f08103f7b6f5f84d7323b8d2b9ed71a71af0f9a0596dec6cef2bd` |
| `model-00005-of-00012.safetensors` | 37,759,488 | `6326829b36022b402947e10fd34a5eecf336c86c41bdb3c8c16a066fdbb42637` |
| `model-00006-of-00012.safetensors` | 37,759,488 | `178b8ae1100f217942347bead90cab1594c1868be454da01a59c003722afcb38` |

The shards are fp32 safetensors files cut from the upstream `model.safetensors` at revision [`29ec3766d36d6f73f0696f85560a422f50e8498c`](https://huggingface.co/amazon/chronos-2/tree/29ec3766d36d6f73f0696f85560a422f50e8498c), with every tensor bit-identical to upstream. [`weights/manifest.json`](weights/manifest.json) records the upstream source and each shard's size and SHA-256, and `make verify-weights` checks the files against it.


## Contributing

[`AGENTS.md`](AGENTS.md) describes the repository, the `make` targets, and the rules every change follows, for human and AI contributors alike.


## License

Licensed under the Apache License, Version 2.0; see [`LICENSE`](LICENSE).

Chronos-2 was created by Amazon, and its weights are distributed under Apache-2.0; see [`NOTICE`](NOTICE).
