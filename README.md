# NeedleInAHaystack-PLUS
To assess the longtext capabilities more comprehensively, we propose Needle-in-a-Haystack PLUS, which shifts the focus from simple fact retrieval to more challenging single-document/multi-document question answering tasks.

## How to evaluate on NeedleInAHaystack-PLUS
### Load Data
Our test data can be download in [NeedleInAHaystack-PLUS](https://drive.google.com/file/d/1aov5kwy4DRYWgxu4Ulaf3omx3uNd3M2r/view?usp=sharing).

### Data Format
All datas in NeedleInAHaystack-PLUS are standardized to the following format:

```python
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
![picture alt](https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/singleQA.jpg)
###  Multi-document QA
![picture alt](https://github.com/zuucan/NeedleInAHaystack-PLUS/blob/main/multiQA.jpg)

## Acknowledgement
NeedleInAHaystack-PLUS is based on the datasets proposed by previous researchers, including [NeedleInAHaystack](https://github.com/gkamradt/LLMTest_NeedleInAHaystack?tab=readme-ov-file), [Squad](https://rajpurkar.github.io/SQuAD-explorer/), [HotpotQA](https://hotpotqa.github.io).

## Citation
```javascript
@misc{zhao2024longagent,
      title={LongAgent: Scaling Language Models to 128k Context through Multi-Agent Collaboration}, 
      author={Jun Zhao and Can Zu and Hao Xu and Yi Lu and Wei He and Yiwen Ding and Tao Gui and Qi Zhang and Xuanjing Huang},
      year={2024},
      eprint={2402.11550},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
