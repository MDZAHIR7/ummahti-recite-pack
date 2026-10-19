# Recite to add recognition pack: fastconformer-quran-ctc-int8-1

These files are the on-device speech recognition pack that the Ummahti Quran
app downloads, after the reader taps Set up in My Hifz > Recite to add. The
app runs the model on the phone. It does not send recitation anywhere.

This repository holds downloadable files only. It contains no Ummahti
application source code.

## Files

| File | Bytes | SHA-256 |
|---|---|---|
| `fastconformer_quran_ctc_int8.tflite` | 112,082,640 | `6d8428c7f4830b36046664299b6789d6b42412a49369c34e8eb0a3f6ba07ba8f` |
| `vocab.txt` | 8,837 | `3997e4ecab2c5f6c215a9bd71ec6ea88727b90ece701ae613c809a45404e9f31` |
| `LICENSE` | 5,852 | `8ee6366f4b3ccb70dd2e9265d8a02505b402c088065a72b2251e1b89e8476b34` |

The app has these sizes and digests compiled in and installs nothing that
differs. `SHA256SUMS` lists the same values for convenience; it is not what
the app trusts.

## Licence

The model is a derivative of Quran-Lab's `fastconformer-quran`
(https://huggingface.co/Muno459/fastconformer-quran, revision
`77dbe5d809628ea89422243695de4c0d69770775`) and is distributed under the
Quran-Lab No-Profit License 1.1 (NPL-1.1). The licence text is the `LICENSE`
file in this release, byte for byte as Quran-Lab published it.

## Upstream attribution (CC BY 4.0)

Quran-Lab's model is NVIDIA's `stt_ar_fastconformer_hybrid_large_pcd_v1.0`
(https://huggingface.co/nvidia/stt_ar_fastconformer_hybrid_large_pcd_v1.0),
by NVIDIA, licensed under the Creative Commons Attribution 4.0 International
licence (https://creativecommons.org/licenses/by/4.0/), trained further by
Quran-Lab on Quran recitation.

## Changes made for this pack

- Only the CTC decoder of the hybrid model is kept; its other decoder is
  discarded.
- The network was re-expressed in TensorFlow operations and converted with
  TensorFlow 2.19 to LiteRT, with dynamic-range 8-bit weight quantization.
  The weights are otherwise Quran-Lab's.
- `vocab.txt` is the model's own SentencePiece vocabulary, one piece per line,
  in id order.

No warranty is given, as stated in the licence.
