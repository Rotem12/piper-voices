# Russian Piper voice mirror

This repository publishes a small, versioned mirror of selected Russian voice
artifacts for the Piper text-to-speech runtime. Each voice is delivered as a
separate GitHub Release asset so clients can download only the voice they need.
The repository does not contain the Piper runtime and does not grant a blanket
license over the model artifacts.

## Contents

The `russian-voices-2026-09-15` release contains the Russian voices listed in
`NOTICE.md`. Each ZIP contains the model ONNX file, its Piper JSON sidecar, the
upstream model card when one was published, and the applicable license text.
`MODEL_MANIFEST.json` records the pinned upstream revision, release asset, byte
counts, and SHA-256 values.

The mirror is intentionally per voice. A client should request one release
asset after the user selects a voice, verify the recorded SHA-256 value, then
extract the files into its normal Piper model directory.

The TTS client checks its Steam Workshop item first, then the matching asset in
this release, then the existing Hugging Face download path and configured
Hugging Face mirror. The release tag is part of the URL so an already shipped
client never follows a moving asset.

## Provenance and licensing

Every mirrored artifact retains its upstream source and license information in
`NOTICE.md` and in the downloaded ZIP. The license files in `LICENSES/` are
provided for reference and do not replace the upstream terms. Where the
upstream model card did not provide an explicit redistributable license, the
voice is omitted from this mirror.

This is a redistribution record for the stated upstream artifacts, not legal
advice or a new license grant. Before a commercial release, the publisher
should review the upstream model cards, training-data rights, and any
applicable platform rules.

## Excluded voices

`ru_RU-irina-medium` is omitted because its upstream model card says
`License: Unknown`. `ru_RU-ruslan-medium` is omitted because its upstream card
specifies CC BY-NC-SA 4.0, which is incompatible with an unrestricted
commercial mirror. They remain available only through their existing upstream
routes until their terms are cleared.
