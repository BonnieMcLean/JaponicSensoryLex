# Japonic

## About this data
The file **dat.csv** is a cognate coded dataset of sensory language for Japonic. It contains words for 110 sensory concepts in 49 Japonic varieties (48 Japanese varieties and 1 Ryukyuan variety). Information about the linguistic varieties can be found in the file **varieties.tsv**. Information about the concepts can be found in the file **concepts.tsv**. A bibliography of the data sources used is available in **sources.bib**. 

## Cognate coding

### Coding decisions
Cognate coding was carried out using the following principles:

* Words sharing the same root, e.g. *kuro* 'black' and *kura* 'dark', are coded the same.
* For ideophones, reduplicated, non-reduplicated, and suffixed forms are considered to share the same root and are coded the same, as well as forms derived through regular vowel and consonant alternations. For example, *pokipoki* 'snapping repeatedly', *pokiQ* 'snapping once', *pokiN* 'a prolonged, single snap', *pokkiri* 'a light, single snap', *bokiboki* 'louder snapping', *pokopoko* 'lower frequency snapping', etc. would all be coded the same.
* Compounds sharing at least one root between them are also coded the same, e.g. *siokarai* 'salty' (=*sio* 'salt' + *karai* 'spicy/salty') and *karai* 'salty' are coded the same. However, if part of the compound does not add any core semantic value it is ignored for the coding, e.g. the *bukai* in *syuuneNbukai* 'obstinate' (=*syuuneN* 'obstinate' + *bukai* 'deep') and *neQtyobukai* (=*neQtyo* 'obstinate' + *bukai* 'deep') is ignored, and these are coded differently.
* When there is no corresponding single word expression, or only an evaluative expression is used (e.g. *yoi* 'good' or *warui* 'bad'), this is coded NA.
* NAs are excluded from the analysis.
* Negations of nouns and adjectives (e.g. *oisikunai* 'not tasty' and *azinai* 'no flavour' for *mazui* 'disgusting') that are conventionalised, very common and seem to unite a set of locations are considered single word expressions, and coded. However, negations that are not conventionalised and used sporadically across disparate locations (e.g. *hazyisyirazu*, or *pazyinee* for RUDE, both of which mean 'no shame' but one was elicited in Tokyo and the other in Okinawa) are considered as expressions (even if they are an inflection of a single word).
* When there is no corresponding word for the specific meaning, but a hypernym is used in the same context (e.g. *itai* 'painful' for *zukizuki* 'throbbing pain'), this is also coded.
* Where multiple expressions are given, all are coded. If they belong to the same cognate set, they are coded on the same line separated by /. If they belong to different cognate sets, they are coded on separate lines.

For difficult cases, I consulted Tokugawa (2002) to ascertain the cognate status of a word. This is noted in the 'CognateDetectionMethod' column (where tokugawa_2002 appears). Otherwise, cognate coding was based on my own knowledge of the Japonic languages. 

### Coding system
Cognate classes are labelled a, b, c, d etc. for items in the same class. If a form contains multiple roots from different cognate classes, the different cognate classes are separated by a '; ', eg. 'a; b'.

'?' is used when the cognate status is ambiguous/uncertain. 

'NA' is used when there is no corresponding expression in that variety for that concept (when both the CognateCode column and the Form column have 'NA'), or when the only way to express the concept is through a sentence or multiword expression (in which case the expression is given in the Form column, but the CognateCode column has 'NA'). 

'MISSING' is used when the source was missing data for that variety (so we don't know whether they have an expression for that concept or not).

## Transcription system

Two of the sources, Sanada & Tomosada (2015; 2018), are only transcribed using Japanese kana. The third source, Hirayama (1992), contains IPA as well. Hirayama (1992) provides a lot more phonetic detail than Sanada & Tomosada (2015; 2018). The transcriptions in this data should be regarded as phonemic rather than phonetic. Features like devoicing, aspiration, nasalisation etc. are not transcribed. 

The table below explains the transcription symbols used in dat.csv (where they differ from standard IPA characters); their correspondence with IPA symbols; and with the Japanese kana used in the original sources. 

|dat.csv|IPA        |kana |notes                                                                                                                                          |
|-------|-----------|-----|-----------------------------------------------------------------------------------------------------------------------------------------------|
|u      |ɯ          |う   |                                                                                                                                               |
|U      |ɯ̈          |-    |                                                                                                                                               |
|I      |ï          |-    |                                                                                                                                               |
|A      |æ          |あぇ |                                                                                                                                               |
|E      |ɛ          |えぁ |                                                                                                                                               |
|O      |ø          |おぇ |                                                                                                                                               |
|we     |we         |うぇ |                                                                                                                                               |
|G      |ŋ          |-    |                                                                                                                                               |
|Q      |ʔ/ː        |っ   |ʔ if word final, otherwise the following consonant is lengthened (geminate)                                                                    |
|N      |ɴ:/m:/n:/ŋ:|ん   |ɴ if word final, otherwise assimilates to following consonant, and these are all moraic.                                                       |
|n      |n/ⁿ/ᵐ/ᵑ    |-    |n if an onset, as a coda it is used to indicate that the following consonant is prenasalised (with assimilation to the place of that consonant)|
|sy     |ʃ          |し   |                                                                                                                                               |
|zy     |ʒ          |じ   |                                                                                                                                               |
|ty     |t͡ʃ         |ち   |                                                                                                                                               |
|dy     |d͡ʒ         |ぢ   |                                                                                                                                               |
|ts     |t͡s         |つ   |                                                                                                                                               |
|dz     |d͡z         |づ   |                                                                                                                                               |
|h      |h/ç        |     |ç if before /i/, otherwise h (this difference is not phonemic in any variety)                                                                  |
|f      |ɸ          |     |                                                                                                                                               |
|y      |j          |     |                                                                                                                                               |

Double letters (e.g. aa, ii, uu etc.) are used to indicate long vowels, whereas geminate consonants are indicated using Q (see table above).

## Sources

Hirayama, Teruo. 1992. Gendai Nihongo Hōgen Daijiten [Dictionary of Contemporary Japanese Dialects]. Tokyo, Japan: Meiji-shoin.

Sanada, Shinji, and Kenji Tomosada, eds. 2015. Kenbetsu Hoogen Kanzyoo Hyoogen Jiten [Dialect Dictionary of Emotion Expressions by Prefecture]. Tokyo: Tokyodo.

Sanada, Shinji, and Kenji Tomosada, eds. 2018. Kenbetsu Hoogen Kankaku Hyoogen Jiten [Dialect Dictionary of Sensory Expressions by Prefecture]. Tokyo: Tokyodo.

Tokugawa, Munemasa. 2002. Nihon Hogen Daijiten: The Comprehensive Dictionary of Dialects in Japan. Tokyo: Shogakukan.
