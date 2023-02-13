# Dialogue Commonsense Graph in Japanese

We propose a commonsense knowledge graph (CSKG) grounded on dialogues.
This repository contains the graph built in Japanese.

## Data Format

We define the eight relations based on categories, time series and target persons:

| Relation | Category | Time | Person |
|:-|:-|:-|:-|
| Cause | Event | Before | Speaker |
| Prerequisite | Event | Before | Listener |
| Subsequent event | Event | After | Speaker |
| Effect | Event | After | Listener |
| Motivation | Mental state | Before | Speaker |
| Guess | Mental state | Before | Listener |
| Reflection | Mental state | After | Speaker |
| Reaction | Mental state | After | Listener |

Each utterance is annotated with inferences of the eight relations.
An example of the utterances and inferences is shown below:

```json
{
    "status_id": 1557164592392183808,
    "cause": [
        "暑い暑い"
    ],
    "prerequisite": [
        "確かに全然外に出てない"
    ],
    "subsequent_event": [
        "宿題が終わらない"
    ],
    "effect": [
        "じゃあ家で宿題すればちょうどいいじゃん",
        "外に出ないでエアコンが効いた部屋で過ごす"
    ],
    "motivation": [
        "暑すぎてキツイ",
        "夏が終わらないと困る"
    ],
    "guess": [
        "暑くない",
        "夏がすぐ終わると宿題が終わらなくて困る"
    ],
    "reflection": [
        "暑さには何も勝てないよ"
    ],
    "reaction": [
        "そうかもね",
        "その通りだ"
    ]
}
```

Note that the utterance texts are replaced by their Twitter IDs.

## Reference

```bibtex
@InProceedings{ide_nlp2023_dcsg,
    author =    "井手竜也 and 榮田亮真 and 河原大輔 and 山崎天 and 李聖哲 and 新里顕大 and 佐藤敏紀",
    title =     "対話に基づく常識知識グラフの構築と対話応答生成に対する適用",
    booktitle = "言語処理学会第29回年次大会",
    year =      "2023",
    url =       "https://www.anlp.jp/proceedings/annual_meeting/2023/pdf_dir/H1-4.pdf"
    note=       "in Japanese"
}
```

## License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
