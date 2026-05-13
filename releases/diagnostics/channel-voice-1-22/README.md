# Channel Voice Diagnostics (1-22)

This folder contains generated spoken-number WAV files for channel routing tests:

- `channel-01.wav` through `channel-22.wav`

Generation profile:

- voice engine: `flite` (`voice=kal`)
- sample rate: `48000`
- channels: mono (`1`)
- duration cap: `1.2s`

Intended use:

- route one file at a time to one hardware output channel
- stand at a known speaker and confirm the heard channel number
- build a verified physical speaker-to-hardware-channel map
