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

As of 2025/11/6, the dataset is currently incomplete, and is only a beta release, but is completely labeled, and fully capable of being used with no issues at all. This beta version contains 21 songs. Measuring roughly 56 minutes and 50 seconds, including silence. (56 min 19 sec excluding the samples including English)

The dataset is recorded at 16 bit 44.1k Hz wav format and labeled in HTK label format (.lab).

The dataset is released with two versions, full length and segmented. The full length dataset only includes wav and lab files, whereas the segmented dataset includes ds files and a transcription.csv for diffsinger usage. The ds contains f0 and slur data.

## Additional Info:
In the full length version of the dataset, humming is labeled `M` instead of `m` to prevent the converter from merging it with `SP` and `AP` phonemes. It is converted back into `m` in the segmented dataset.

The dataset includes the joke phoneme `mlem` for mouth clicks at the start of breaths.

## Song List (Beta version)
```
001	11 GEM ver.
002	再見
003	多遠都要在一起
004	透明
005	你是我的歌
006	光（星塵版）
007	光（永夜版）
008	星願
009	反正(short ver.)
010	給某某
011	大雨
012	又將盛夏
013	失陷(short ver.)
014	鼎沸
015	眼瞳之火(short ver.)
016	Solar Storm
017	明日
018	失戀無罪(short ver.)
019	希望懸空
020	零和
021	現在我很幸福
```

# License:
    ACV-001  © 2025 by YiChen Huang is licensed under CC BY-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
