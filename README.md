# ACV-001
public male singing voice dataset

# Dataset Info:
## Format and Specs:
The dataset is labeled with the ACV format Chinese phonemes as mentioned [here](https://github.com/Archivoice/AV-diffsinger-Chinese-support) and arpabet for English, which are labeled with diffsinger's multi language dataset preparation in mind, so bear the language tag `en/`.

To train exclusively in Chinese with no English included, remove the following samples:
- 001_seg002 (.wav/.lab/.ds)
- 001_seg011 (.wav/.lab/.ds)
- 001_seg012 (.wav/.lab/.ds)
- 001_seg018 (.wav/.lab/.ds)
- 001_seg019 (.wav/.lab/.ds)
(or just the entirety of sample 001)

As of 2025/11/6, the dataset is currently incomplete, and is only a beta release, but is completely labeled, and fully capable of being used with no issues at all. This beta version (v0.1) contains 21 Chinese songs. Measuring roughly 56 minutes and 50 seconds, including silence. (56 min 19 sec excluding the samples including English)

As of night of 11/6 (beta v0.1 was uploaded at around 3 AM), the dataset includes an English section, of 9 songs, the first few of which contain Korean (namely samples en_001, en_002, and en_005). (26 min 42 secs including silence)

The dataset is recorded at 16 bit 44.1k Hz wav format and labeled in HTK label format (.lab).

The dataset is released with two versions, full length and segmented. The full length dataset only includes wav and lab files, whereas the segmented dataset includes ds files and a transcription.csv for diffsinger usage. The ds contains f0 and slur data.

## Additional Info:
In the full length version of the dataset, humming is labeled `M` instead of `m` to prevent the converter from merging it with `SP` and `AP` phonemes. It is converted back into `m` in the segmented dataset.

The dataset includes the joke phoneme `mlem` for mouth clicks at the start of breaths.

## Song List (Beta version)
Moved to [song list](https://github.com/Archivoice/ACV-001/tree/8800afb3fd3e6178a7e13773ecd8b13e17ebe758/song%20list)

# Credits:

Voice provided by Jonathan Huang 黃奕晨, owner of ArchiVoice, [X/Twitter](https://x.com/NekroTheCorpse)

# License:

<a href="https://github.com/Archivoice/ACV-001">ACV-001</a> © 2025 by <a href="https://github.com/Archivoice">YiChen Huang</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;">
