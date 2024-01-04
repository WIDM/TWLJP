# Legal Knowledge Management for Prosecutors based on Judgement Prediction and Error Analysis from Indictments: Dataset

## Overview
Legal AI aims to provide improved knowledge management services based on legal documents. Existing legal judgement prediction datasets mainly use court verdicts. However, for prosecutors, the use of indictments for judgment predictions can help detecting inconsistencies between predictions and prosecution, providing prosecutors with more accurate references to laws and charges through error analysis.

In this study, we collect a dataset called TWLJP, which contains 342,754 indictments. We compared three possible messaging passing architectures among the law, regulation, and accusation cause prediction tasks, i.e. independent, topological, and interactive. The result shows that interactive message passing among the three tasks achieved the best Macro-F1 performance of 95.2\%, 79.62\%, and 65.84\% for laws, regulations, and accusation cause prediction, respectively.

## Dataset

### Annotation Example

### Data Format

``` json
{
  "fact": "一、緣坐落新北市...",
  "file": "臺灣新北地方檢察署 108 年度 偵 字第 8909 號刑事起訴書.txt",
  "meta":
    {
      "relevant_articles": [["水土保持法", "第32條"]],
      "#_relevant_articles": 1,
      "relevant_articles_org": ["水土保持法第32條"],
      "accusation": "水土保持法",
      "criminals": ["王世昌"],
      "#_criminals": 1,
      "term_of_imprisonment":
      {
        "death_penalty": null,
        "imprisonment": null,
        "life_imprisonment": null
      }
    }
}
```
## Experiments

### Baselines
We implement three competitive Baselines: Multi-task BERT/[Lawformer](https://aclanthology.org/2020.coling-main.88/) and [Topjudge](https://aclanthology.org/D18-1390/)

### Prefomance
The performance of baselines and our model Message-passing are as follows.


