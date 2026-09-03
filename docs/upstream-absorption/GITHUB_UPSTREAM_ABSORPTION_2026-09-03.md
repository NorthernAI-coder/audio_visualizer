# Upstream Absorption — Audio Visualizer — 2026-09-03

## RustAudio/cpal + rodio
If a Rust-native capture/playback path is useful, evaluate CPAL for low-level device/audio input and Rodio for ordinary playback. Keep visualization analysis fed by a bounded lock-free/buffered handoff rather than doing rendering/FFT allocation inside the audio callback.

## auto-editor
Use as an optional final render/timing assembly step for visualizer videos; the visualizer's own beat/timing data remains authoritative.

## sherpa-onnx / whisper.cpp (optional)
Local lyric/voice timestamps can drive title/section/caption events when needed. Never fabricate lyrics when authoritative text is supplied.

## Acceptance gates
- no audio glitches from visualization workload
- deterministic beat/timing export
- local/free core workflow
- optional speech models lazy-load and are license-audited.