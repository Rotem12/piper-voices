# Russian Piper voice mirror

Versioned Russian voice artifacts for the [Piper](https://github.com/rhasspy/piper)
text-to-speech runtime. Each voice is a separate [GitHub Release asset](https://github.com/Rotem12/piper-russian-voices/releases/tag/russian-voices-2026-09-15),
so clients download only the voice they need.

## Download

Choose a voice from the release and download its ZIP. Each archive contains the
Piper ONNX model, JSON sidecar, and the available upstream model and license
notices. Verify the SHA-256 value in [`MODEL_MANIFEST.json`](MODEL_MANIFEST.json)
before extracting it into the Piper model directory.

The TTS client checks Steam Workshop, this GitHub mirror, Hugging Face, and its
configured Hugging Face mirror in that order.

## Provenance

Source revisions and licensing information are recorded in [`NOTICE.md`](NOTICE.md).
The repository does not include the Piper runtime.
