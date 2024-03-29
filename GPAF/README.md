# Grey Proprietary Audio Format

## Introduction

The Grey Proprietary Audio Format (GPAF) is a distribution audio format aimed to transmit proprietary audio media in the most secure and efficient way, 
to help curb copyright infringement and illegal distribution issues within the Greysoft Ecosystem.

## How it works

Audio is usually converted from it's original format into high quality Waveform Audio File Format and encrypted with keys only known within the ecosystem 
and rotated in short frequencies making it difficult to decrypt out of malicious intent.

During playback audio is decrypted using these known keys and converted to it's original Waveform Audio File Format and cached for the current session, 
after the session the original Waveform Audio File is deleted from cache, no user interation is required.

## Mitigating Latency

While retrieving and decrypting large files for playback might be expensive and possibly affect user experience, this is mitigated with the use of 
playlists where the first file in the list is retrieved and decrypted and during playback the next file is also retrived and decryted while the previous file is removed from memory.

## Tech Spec

**Filename extension:** .gpaf

**Format:** 11,025 Hz 4 bit ADPCM (44100 Hz, 16-bit stereo)

**Bitrate:** 44.1 kbit's

**Decodes To:** WAVE (audio/vnd.wave, audio/wav, audio/wave, audio/x-wav)
