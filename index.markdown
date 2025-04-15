---
layout: default
---
<div align="center">

<h1>AgentRewardBench</h1>

<table>
  <tr>
    <td><a href="https://github.com/McGill-NLP/agent-reward-bench"><strong>💾Code</strong></a></td>
    <td><a href="https://arxiv.org/abs/2504.08942"><strong>📄Paper</strong></a></td>
    <td><a href="https://agent-reward-bench.github.io"><strong>🌐Website</strong></a></td>
  </tr>
  <tr>
    <td><a href="https://huggingface.co/datasets/McGill-NLP/agent-reward-bench"><strong>🤗Dataset</strong></a></td>
    <td><a href="https://huggingface.co/spaces/McGill-NLP/agent-reward-bench-demo"><strong>💻Demo</strong></a></td>
    <td><a href="https://huggingface.co/spaces/McGill-NLP/agent-reward-bench-leaderboard"><strong>🏆Leaderboard</strong></a></td>
  </tr>
</table>

<br>

<p><strong><a href="#">AgentRewardBench: Evaluating Automatic Evaluations of Web Agent Trajectories</a></strong><br>
<em>
<a href="https://xinghanlu.com/">Xing Han Lù</a>, 
<a href="https://kazemnejad.com/">Amirhossein Kazemnejad*</a>, <br>
<a href="https://ncmeade.github.io/">Nicholas Meade</a>, 
<a href="https://arkilpatel.github.io/">Arkil Patel</a>, 
<a href="https://scholar.google.com/citations?user=QzZOkfIAAAAJ&amp;hl=en">Dongchan Shin</a>, 
<a href="https://www.linkedin.com/in/alejandra-zambrano-a71092196/">Alejandra Zambrano</a>, <br>
<a href="https://kstanczak.github.io/">Karolina Stańczak</a>, 
<a href="https://www.ptshaw.com/">Peter Shaw</a>, 
<a href="https://sites.google.com/view/christopher-pal">Christopher J. Pal</a>, 
<a href="https://sivareddy.in/">Siva Reddy</a>
</em><br>
<em>*Core Contributor</em>
</p>

</div>


<img src="/assets/primary.png" alt="AgentRewardBench" width="100%"/>

## Using the `agent-reward-bench` library

This library provides tools for evaluating the performance of agents in various environments. It includes a set of environments, a set of agents, and a set of evaluation metrics.

To install the library:
```bash
pip install agent-reward-bench
```

You can now import the library in your Python code:
```python
# Using agents and environments:
import agent_reward_bench.modeling as arbm
import agent_reward_bench.benchmarks as arbb

# Using the judge for evaluating agents:
import agent_reward_bench.judge as arbj
from agent_reward_bench.judge.existing import aer, nnetnav
from agent_reward_bench.judge.args import default_judge_args, judge_args
```

See [`run_judge.py`](https://github.com/McGill-NLP/agent-reward-bench/blob/main/scripts/run_judge.py) for an example of how to use the library.



## Dataset

You can use the `huggingface_hub` library to load the dataset. The dataset is available on Huggingface Hub at [`McGill-NLP/agent-reward-bench`](https://huggingface.co/datasets/McGill-NLP/agent-reward-bench).

Install the hugginface-hub with:
```python
pip install huggingface_hub
```

```python
from huggingface_hub import snapshot_download

# Download the dataset to ./trajectories/
snapshot_download(
    repo_id="McGill-NLP/agent-reward-bench",
    repo_type="dataset",
    local_dir="./trajectories/"
)
```

## Leaderboard

You can find the ranking of automatic evaluators, including LLM judges, on [the Huggingface leaderboard](https://huggingface.co/spaces/McGill-NLP/agent-reward-bench-leaderboard). You can also see the breakdown by benchmark, allowing 

### Submission

To submit your results, please [open an issue on the GitHub repository](https://github.com/McGill-NLP/agent-reward-bench/issues) with your results and a link to your paper/artifacts.

## Citation

If you use AgentRewardBench in your research, please cite the following paper:

```bibtex
@misc{lù2025agentrewardbenchevaluatingautomaticevaluations,
      title={AgentRewardBench: Evaluating Automatic Evaluations of Web Agent Trajectories}, 
      author={Xing Han Lù and Amirhossein Kazemnejad and Nicholas Meade and Arkil Patel and Dongchan Shin and Alejandra Zambrano and Karolina Stańczak and Peter Shaw and Christopher J. Pal and Siva Reddy},
      year={2025},
      eprint={2504.08942},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2504.08942}, 
}
```
