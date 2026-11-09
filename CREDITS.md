# Skald voices: credits and licences

The voices in this pack were made for Skald, an app that writes up tabletop role-playing sessions and reads
them back aloud. Everything here runs on the phone.

## Voices

The voices were fine-tuned from the speech of four LibriTTS-R readers. Each reader is identified only by their
corpus number:

| Part in Skald | LibriTTS-R reader |
|---|---|
| Storyteller (narrator) | 251 |
| Villain (boss) | 2803 |
| Herald | 6345 |
| Quotes | 7850 |

LibriTTS-R is by Y. Koizumi, H. Zen, S. Karita, Y. Ding, K. Yatabe, N. Morioka, M. Bacchiani, Y. Zhang, W. Han
and A. Bapna, 2023 (https://www.openslr.org/141/). It is licensed under CC BY 4.0
(https://creativecommons.org/licenses/by/4.0/). It is a restored version of LibriTTS, by Zen et al., 2019. The
recordings themselves are LibriVox public-domain audiobooks, read by volunteers.

The voices were changed from the source recordings: they were fine-tuned, as described below.

## Model

- GPT-SoVITS v2 by RVC-Boss and contributors (MIT licence), from https://github.com/RVC-Boss/GPT-SoVITS.
  - The pretrained v2 weights come from https://huggingface.co/lj1995/GPT-SoVITS.
  - They were fine-tuned on the readers above, then exported to ONNX.
  - The decoder was quantized to int8.
- The English pronunciation front end ports GPT-SoVITS's `english.py` to Kotlin. It uses:
  - the CMU Pronouncing Dictionary (Copyright (C) 1993-2008 Carnegie Mellon University, BSD-style licence);
  - the GPT-SoVITS names and homograph lists (MIT);
  - the neural speller weights of g2p_en by Kyubyong Park and Jongseok Kim (Apache-2.0).

## Licence of this pack

The trained voices are released under CC BY 4.0, the licence of the data they learnt from. The parts listed
above keep their own licences.

Please don't use these voices to impersonate a real person.
