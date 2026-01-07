# ACV-001
public male singing voice dataset

# Dataset Info:
## Format and Specs:
The dataset is manually labeled with the following systems (the native/non native refers to level of fluency):\
>[Cantonese](https://github.com/Archivoice/diffsinger-Cantonese-phonetic-system) (language tag: `ca/`, non native)\
[Mandarin Chinese](https://github.com/Archivoice/AV-diffsinger-Chinese-support) (language tag: `cn/`, native)\
arpabet for English (language tag: `en/`, native)\
Japanese via romaji (language tag: `ja/`, non native)\
Korean via Team Coda's [system](https://github.com/Coda-SVS/diffsinger-korean-support/tree/main) (language tag: `ko/`, non native)\
[Taiwanese](https://github.com/Archivoice/diffsinger-Taiwanese-phonetic-system) (language tag: `tw/`, native)

The dataset is around 3/5 fully manually labeled, around 2/5 is generated via [WFL](https://github.com/MLo7Ghinsan/WFL-ASR) and manually corrected.\
Overall, all labels have been manually checked and should be correct, save for a few incorrectly labeled phonemes.

To train exclusively in specific language, you can use tools such as [notepad++](https://notepad-plus-plus.org/downloads/) to search for `/` in the files via the "Find in Files" function.
Which will make a list showing every sample that has a language tag.\
It's recommended to use `/` instead of the full language tab, since in the case of Chinese and English, there can be more than one additional language.\
Cantonese and Taiwanese do not have extra language tags.

The dataset is recorded at 16 bit 44.1k Hz in wav format and labeled in HTK label format (.lab).\
Audio has been dereverbed, denoised, and partially normalized for more even consistency.

The dataset is released with two versions, full length and segmented.\
The full length dataset only includes wav and lab files, whereas the segmented dataset includes ds files and a transcription.csv for diffsinger usage.\
The ds contains f0 and note slur data. (Aside from English, all other data has been manually slur cut, English samples were processed via [SOME](https://github.com/openvpi/SOME))

## Additional Info:
In the full length version of the dataset, humming is labeled `MM` instead of `m` to prevent the converter from merging it with `SP` and `AP` phonemes.\
For English, since consonant clusters can have varying placement in a note. For example, in "drought", the `r` is treated as a vowel, but when it comes to "had read", the `r` is a consonant.\
To prevent placement issues, consonant clusters where the semivowel (r, w, y, l) become vowels, the consonant before it is labeled in all caps (ie. "straight": `s T r ey t`).
> The above only applies to full length samples, the segmented samples have already been converted back.

The dataset includes the joke phoneme `mlem` for mouth clicks at the start of breaths.

## Song List:
Moved to [song list](/song_list)

# Credits:
Voice provided by Jonathan Huang 黃奕晨, owner of ArchiVoice, [X/Twitter](https://x.com/NekroTheCorpse)

# License:
<a href="https://github.com/Archivoice/ACV-001">ACV-001</a> © 2025 by <a href="https://github.com/Archivoice">YiChen Huang</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;">

The license only applies to direct use of the dataset, and does not apply to models trained.\
Any model trained using ACV-001 can follow its own license.
