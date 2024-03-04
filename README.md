# NeedleInAHaystack-PLUS
To assess the longtext capabilities more comprehensively, we propose Needle-in-a-Haystack PLUS, which shifts the focus from simple fact retrieval to more challenging single-document/multi-document question answering tasks.

## How to evaluate on NeedleInAHaystack-PLUS
### Load Data
Our test data can be download in [NeedleInAHaystack-PLUS](https://drive.google.com/file/d/1aov5kwy4DRYWgxu4Ulaf3omx3uNd3M2r/view?usp=sharing).

### Data Format
All datas in NeedleInAHaystack-PLUS are standardized to the following format:

```javascript
{
    "id": "The unique identifier for each test data.",
    "context": "The long context of the comprehension task.",
    "context_length": "The length of haystack ranges from 1,000 to 128,000 tokens with equal intervals, totaling 15 different lengths.",
    "depth_percent": "The position of the needle in the haystack.",
    "input": "The questions of the comprehension task.",
    "dataset": "The name of the dataset, currently divided into needle_squad and needle_hotpotqa.",
    "answers": "A List of all true answers.",
}
```

## Results Visualization
The invocation time of the APIs:
* OpenAI's GPT-4-128K (Run 2024-01-31)
* Anthropic's Claude 2.1 (Run 2024-02-08)
### Single-document QA
Markup : ![picture alt]([http://via.placeholder.com/200x150](https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/multiQA.jpg)https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/singleQA.jpg)
###  Multi-document QA
Markup : ![picture alt]([http://via.placeholder.com/200x150](https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/multiQA.jpg)https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/multiQA.jpg)
