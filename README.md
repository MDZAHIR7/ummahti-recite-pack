# ummahti-recite-pack

Download-only files for the Ummahti Quran app's **Recite to add** feature:
the on-device speech recognition pack, published as versioned release
attachments.

- Each release is tagged with the pack identity the app pins, for example
  `fastconformer-quran-ctc-int8-1`. There is no "latest" pointer, and a
  published release is never replaced with different bytes; a new model is a
  new identity and a new release.
- The app checks every file against sizes and SHA-256 digests compiled into
  it before installing anything.
- This repository contains no Ummahti application source code, no user data
  and no credentials.

See `NOTICE.md` in each release for the files, digests, licence (Quran-Lab
No-Profit License 1.1) and the CC BY 4.0 attribution for NVIDIA's upstream
model.
