[README.md](https://github.com/user-attachments/files/34562072/README.md)
# BBC-pesantren: coded corpus and analysis script

Supplementary materials for the manuscript on YouTube comments under the BBC News Indonesia documentary *Aib Sang Guru: Di Balik Dinding Pesantren* (N = 1,595 comments; export of 2 October 2026, 09:54).

## Files
- `coded_corpus_public.csv`: one row per comment, **without comment text** and with pseudonymised account codes.
- `analysis_full_corpus.py`: reproduces every statistic in the manuscript from the CSV (`python analysis_full_corpus.py coded_corpus_public.csv`; requires pandas, numpy, scipy, statsmodels).

## Columns
| Column | Meaning |
|---|---|
| `comment_no` | Order in the export; the `#` numbers in the manuscript refer to it. Replies follow their parent. |
| `type`, `date`, `likes` | Top-level comment or reply; posting day; like count at export |
| `account_pseud` | Salted-hash pseudonym of the account |
| `emo_manual`, `emo_final` | Emotion codes by reading, and after adding explicit-cue lexicons. A anger, D disgust, S sadness, F fear, E empathy or solidarity, `-` none |
| `topic` | P punishment and legal justice, I institutional responsibility, V survivor support, R religious authority and doctrine, C child protection and choice of pesantren, D denial and counter-narratives, L evaluation of the documentary, O other |
| `practice` | Highest tier met: `x` expressive condemnation, `m` mobilisation and avoidance, `1` endorsing private or mob punishment, `2` calling out or boycotting a target, `3` urging pursuit, `4` disclosing personal details, `-` none |
| `flags` | J institutional demands, T distrust of institutions, G divine retribution, W explicit amplification |
| `case_lexical` | Case assigned by keyword rules (jombang, lombok, both, none); not verified comment by comment |
| `validation_sample` | 1 if drawn for human double coding (34 core comments plus 166 random, seed 42) |
| `n_words`, `kw_*` | Word count and keyword indicators derived from the text (aib, kebatilan, oknum, fitnah, institutions, violence screen, etc.) |

## Comment text
Comment text is not distributed, because it may breach the platform's terms and allows commenters to be re-identified by search. It is available to reviewers and researchers on request. The script also runs on a version of the CSV that includes a `text` column.

## Coding
Codes were assigned by a large language model (Claude Sonnet 5.5) applying the codebook in the manuscript, followed by a second reading of truncated comments. Human validation of the 200-comment sample is pending; see the manuscript.

## Licence
To be added by the authors.
