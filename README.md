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

## References

```bib
@InProceedings{ide_nlp2023_dialogue,
    author =    "井手竜也 and 榮田亮真 and 河原大輔 and 山崎天 and 李聖哲 and 新里顕大 and 佐藤敏紀",
    title =     "対話に基づく常識知識グラフの構築と対話応答生成に対する適用",
    booktitle = "言語処理学会第29回年次大会",
    year =      "2023",
}
```
