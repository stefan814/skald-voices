# skald-voices

This repo holds the voice pack for the bard in **Skald**. The bard reads a session's chapter aloud, using four
voices fine-tuned with GPT-SoVITS v2 for the phone:

- a storyteller;
- a herald;
- a villain;
- a second voice for quotes.

Skald downloads the pack from this repo's
[Releases](https://github.com/stefan814/skald-voices/releases) and checks it against a pinned SHA-256. The voices
run entirely on the phone, through ONNX Runtime.

This repo holds only the voice pack and its credits. The app's code isn't here.

## What's in the pack

| File | What it is |
|---|---|
| `enc.onnx` | text encoder |
| `dec.onnx` | semantic-token decoder, int8 |
| `vits.onnx` | vocoder, 32 kHz |
| `voices/*.json` | each part's reference: phone ids, semantic tokens and speaker vector |
| `cmu.txt`, `names.txt`, `homographs.txt`, `symbols.json`, `g2p_gru.bin` | English pronunciation data |
| `CREDITS.md` | sources and licences |

## Credits

The voices are trained on LibriTTS-R readers 251, 2803, 6345 and 7850 (CC BY 4.0), using GPT-SoVITS (MIT).
[CREDITS.md](CREDITS.md) has the full attribution, including the pronunciation data (CMUdict, g2p_en).

The voice pack is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please don't use
it to impersonate a real person.
