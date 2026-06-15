# Foundation Model Talent Map

> Working notes on foundation model roles, candidate pools, sourcing directions, and recruiting questions.

## 1. Why This Note

When people talk about large models, the discussion is often about model releases, benchmarks, product demos, or pricing.

From a recruiting perspective, I care more about a different question:

**What kinds of people are actually needed to build and improve these models?**

A foundation model team is not simply a group of “LLM algorithm engineers”. The work is usually split across several different areas:

* Pre-training
* Post-training
* Alignment
* Data
* Evaluation
* Model research
* Training infra / ML systems

Each area has a different talent pool, search strategy, and evaluation standard.

This note is my attempt to break down foundation model recruiting in a more practical way.

## 2. Scope

In this note, “foundation model” refers to the core model layer behind large language models and multimodal models.

It includes work related to:

* Building base model capabilities;
* Training models at scale;
* Improving model behavior after pre-training;
* Building high-quality training and preference data;
* Evaluating model capability, safety, and reliability;
* Supporting large-scale training and inference systems.

I separate foundation model roles from application-layer LLM roles.

For example, Agent product engineers, AI application engineers, and LLM application developers may work closely with large models, but they are not always part of the core model team.

This distinction matters because the sourcing logic is different.

## 3. Role Map

| Area                        | Main Focus                                                    | Typical Roles                                                                       |
| --------------------------- | ------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Pre-training                | Base model capability and large-scale training                | Pre-training Researcher, Foundation Model Researcher, Large-scale Training Engineer |
| Post-training               | Model behavior, usefulness, reasoning, instruction following  | Post-training Researcher, RLHF Researcher, SFT Engineer, Reasoning Researcher       |
| Alignment                   | Safety, preference learning, reward modeling, controllability | Alignment Researcher, Reward Modeling Researcher, Safety Researcher                 |
| Data                        | Data quality, data mixture, synthetic data, preference data   | Data Researcher, LLM Data Engineer, Synthetic Data Researcher                       |
| Evaluation                  | Benchmarking, model quality, safety, failure analysis         | Evaluation Engineer, Benchmark Researcher, Applied Evals Engineer                   |
| Model Research              | New model capabilities and frontier research topics           | Research Scientist, Research Engineer, Multimodal Researcher                        |
| Training Infra / ML Systems | Distributed training, GPU efficiency, inference and serving   | ML Systems Engineer, Distributed Training Engineer, GPU Performance Engineer        |

## 4. Candidate Source Map

For foundation model roles, I would not only search for people who already have “LLM” in their title.

Some relevant candidates may come from adjacent teams, especially if they have experience in large-scale training, data systems, model evaluation, distributed systems, or strong ML research.

| Source Type                               | Why It Matters                                           | Possible Fit                                              |
| ----------------------------------------- | -------------------------------------------------------- | --------------------------------------------------------- |
| Leading LLM companies                     | Closest match to foundation model work                   | Pre-training, post-training, evals, infra                 |
| Big tech AI labs                          | Strong research and engineering resources                | Model research, data, infra, applied model work           |
| Search / recommendation / ads teams       | Strong large-scale training and data experience          | Training infra, data, large-scale modeling                |
| Cloud / AI infrastructure teams           | Strong GPU, distributed systems, and platform experience | Training infra, inference, serving                        |
| University labs / research institutes     | Strong research depth                                    | Model research, reasoning, alignment, multimodal          |
| Open-source model communities             | Hands-on model training and release experience           | Pre-training, post-training, data, evaluation             |
| NLP / CV / RL teams                       | Transferable model and research skills                   | Reasoning, multimodal, alignment, robotics-related models |
| Data platform / annotation platform teams | Data pipeline and quality control experience             | LLM data, preference data, data quality                   |
| AI safety / model quality teams           | Evaluation and risk awareness                            | Evals, safety, red teaming, reliability                   |

## 5. Pre-training

Pre-training is about building the base capability of a model.

This area is closely related to model architecture, training data, compute, training stability, and scaling behavior.

### Typical Roles

* Pre-training Researcher
* Pre-training Engineer
* Foundation Model Researcher
* Large-scale Training Engineer
* Scaling Law Researcher

### What to Look For

* Experience with large-scale model training;
* Understanding of Transformer, MoE, dense models, or related architectures;
* Experience with training stability, loss curves, and experiment analysis;
* Understanding of data mixture and scaling behavior;
* Ability to work across model, data, and compute constraints.

### Candidate Sources

* Foundation model teams at leading LLM companies;
* AI labs inside big tech companies;
* Open-source LLM training projects;
* NLP / ML research teams;
* Search, recommendation, or ads teams with large-scale training experience;
* Deep learning framework or training platform teams.

### Search Keywords

```text
pre-training, pretraining, foundation model, large-scale training, scaling law, MoE, Transformer, training stability, loss curve, data mixture
```

Chinese keywords:

```text
预训练、基座模型、大规模训练、Scaling Law、MoE、模型训练、训练稳定性、数据配比
```

### Recruiting Notes

For pre-training candidates, keywords are often not enough.

A resume may mention “large model training”, but the key question is whether the candidate was close to the core process: data, architecture, training stability, experiment design, or scaling.

## 6. Post-training

Post-training is about making a pre-trained model more useful, reliable, and aligned with real user needs.

It often includes SFT, RLHF, preference optimization, reasoning improvement, tool use, instruction following, and safety-related work.

### Typical Roles

* Post-training Researcher
* RLHF Researcher
* SFT Engineer
* Alignment Researcher
* Reward Modeling Researcher
* Reasoning / RL Researcher

### What to Look For

* Experience with SFT, RLHF, DPO, PPO, GRPO, or other preference optimization methods;
* Understanding of reward models and preference data;
* Experience improving reasoning, coding, math, instruction following, or tool use;
* Ability to connect model behavior with product scenarios;
* Awareness of safety, reliability, and user experience.

### Candidate Sources

* Post-training teams at LLM companies;
* RL / reinforcement learning teams;
* NLP researchers with alignment or instruction-tuning experience;
* Coding model, math reasoning, or Agent training teams;
* AI product teams working on model behavior optimization;
* Data teams that build SFT or preference datasets.

### Search Keywords

```text
post-training, RLHF, SFT, DPO, PPO, GRPO, reward model, preference optimization, alignment, reasoning, instruction tuning, tool use
```

Chinese keywords:

```text
后训练、SFT、RLHF、DPO、PPO、GRPO、奖励模型、偏好优化、对齐、推理能力、指令微调、工具调用
```

### Recruiting Notes

Post-training is closer to model behavior and product experience than pre-training.

A strong candidate should not only know the methods, but also understand how training choices change the way a model behaves.

## 7. Alignment

Alignment focuses on making models safer, more controllable, and more consistent with human preferences.

In practice, alignment may overlap with post-training, reward modeling, safety, evaluation, and red teaming.

### Typical Roles

* Alignment Researcher
* AI Safety Researcher
* Reward Modeling Researcher
* Preference Learning Researcher
* Red Teaming / Safety Evaluation Researcher

### What to Look For

* Understanding of preference learning and reward modeling;
* Experience with RLHF, DPO, safety tuning, or red teaming;
* Ability to analyze model failure cases;
* Awareness of misuse, hallucination, bias, jailbreaks, and reliability issues;
* Ability to work with both research and evaluation teams.

### Candidate Sources

* LLM alignment teams;
* AI safety labs;
* Model evaluation teams;
* RL researchers;
* NLP researchers working on controllability or robustness;
* Trust and safety teams with technical model evaluation experience.

### Search Keywords

```text
alignment, AI safety, reward modeling, preference learning, red teaming, robustness, jailbreak, controllability, harmlessness
```

Chinese keywords:

```text
模型对齐、AI安全、奖励模型、偏好学习、红队、鲁棒性、越狱、可控性、安全性
```

### Recruiting Notes

Alignment candidates can be hard to classify because some come from research, some from safety, and some from evaluation.

The key is to understand whether their work is close to model behavior, preference learning, or safety evaluation.

## 8. Data

Data is one of the most important parts of foundation model work, but it is often underestimated.

For foundation model teams, data is not just labeling. It may include data collection, cleaning, filtering, deduplication, quality scoring, data mixture, domain data, synthetic data, preference data, and data pipeline design.

### Typical Roles

* LLM Data Researcher
* LLM Data Engineer
* Data Quality Engineer
* Synthetic Data Researcher
* Corpus Engineer
* Dataset Engineer

### What to Look For

* Experience with large-scale data cleaning and filtering;
* Understanding of data quality, data mixture, and domain coverage;
* Experience building instruction data or preference data;
* Experience with synthetic data;
* Ability to turn model problems into data problems;
* Strong attention to detail and judgment on data quality.

### Candidate Sources

* LLM data teams;
* Search / recommendation / content understanding teams;
* NLP data construction teams;
* Data platform teams;
* Annotation platform teams;
* Trust and safety data teams;
* Product data teams with strong model evaluation or feedback-loop experience.

### Search Keywords

```text
data quality, data mixture, synthetic data, corpus, dataset, deduplication, filtering, data pipeline, preference data, instruction data
```

Chinese keywords:

```text
数据质量、数据配比、合成数据、语料、数据清洗、去重、过滤、数据管线、偏好数据、指令数据
```

### Recruiting Notes

Data candidates may come from more diverse backgrounds than model researchers.

The main question is whether they understand the relationship between data quality and model performance, rather than only having general data processing experience.

## 9. Evaluation

Evaluation is about understanding whether a model is actually improving.

It is not just about running public benchmarks. In real model development, evaluation may involve benchmark design, red teaming, safety evaluation, hallucination analysis, reasoning tests, coding tests, user-behavior evaluation, and product-specific evals.

### Typical Roles

* Model Evaluation Engineer
* Evaluation Researcher
* Benchmark Researcher
* Safety Evaluation Researcher
* Applied Evals Engineer
* Model Quality Engineer

### What to Look For

* Experience designing evaluation sets or benchmarks;
* Understanding of model capabilities such as reasoning, coding, math, long-context, tool use, and safety;
* Ability to turn product problems into evaluation cases;
* Ability to analyze model failure patterns;
* Ability to connect evaluation results back to training or product iteration.

### Candidate Sources

* Model evaluation teams;
* AI safety teams;
* NLP benchmark researchers;
* Coding model evaluation teams;
* AI product quality teams;
* QA teams with strong model or data understanding;
* Red teaming teams;
* Applied AI teams with strong user-feedback analysis experience.

### Search Keywords

```text
model evaluation, evals, benchmark, red teaming, safety evaluation, hallucination, reasoning evaluation, coding benchmark, applied evals
```

Chinese keywords:

```text
模型评测、模型评估、Benchmark、红队、安全评测、幻觉评估、推理评测、代码评测、应用评测
```

### Recruiting Notes

Evaluation talent is becoming more important because model teams need more than one benchmark score.

They need to know where the model improves, where it fails, and whether the improvement matters in real use cases.

## 10. Model Research

Model research focuses on improving model capability and exploring new directions.

This area may include reasoning, long context, multimodal learning, model architecture, tool use, interpretability, memory, planning, and other frontier topics.

### Typical Roles

* Research Scientist
* Research Engineer
* Foundation Model Researcher
* Reasoning Researcher
* Multimodal Researcher
* Long-context Researcher
* Interpretability Researcher

### What to Look For

* Strong research background in ML, NLP, CV, RL, or related areas;
* Publications, open-source work, or strong project evidence;
* Ability to design and run meaningful experiments;
* Ability to connect research ideas with model training or product needs;
* Ability to collaborate with engineering, infra, data, and product teams.

### Candidate Sources

* University labs;
* AI research labs;
* Foundation model companies;
* Top conference authors;
* Open-source model contributors;
* NLP / CV / RL research teams;
* Multimodal and reasoning research groups.

### Search Keywords

```text
research scientist, research engineer, reasoning, long context, multimodal, interpretability, model architecture, frontier model, tool use, planning
```

Chinese keywords:

```text
研究科学家、研究工程师、推理、多模态、长上下文、可解释性、模型结构、前沿模型、工具调用、规划
```

### Recruiting Notes

For research roles, it is important to distinguish between paper experience, open-source experience, and real large-scale model experience.

They may overlap, but they are not the same thing.

## 11. Training Infra / ML Systems

Training infra is not always listed under foundation model roles, but it is closely tied to foundation model work.

Without strong infra, large-scale training and efficient inference are not possible.

### Typical Roles

* ML Systems Engineer
* Distributed Training Engineer
* Training Platform Engineer
* GPU Performance Engineer
* Inference Engineer
* Model Serving Engineer

### What to Look For

* Experience with distributed training;
* Familiarity with GPU, CUDA, NCCL, or high-performance computing;
* Experience with training stability, cluster scheduling, and resource utilization;
* Experience with inference optimization, serving, quantization, KV cache, or deployment;
* Ability to work across model, system, and hardware constraints.

### Candidate Sources

* LLM infra teams;
* Cloud vendor AI infrastructure teams;
* GPU / HPC teams;
* Search, recommendation, and ads training platform teams;
* Deep learning framework teams;
* Distributed systems teams;
* Model serving or inference platform teams.

### Search Keywords

```text
ML systems, distributed training, GPU, CUDA, NCCL, inference, serving, quantization, KV cache, training platform, cluster, performance optimization
```

Chinese keywords:

```text
ML Systems、分布式训练、GPU、CUDA、NCCL、推理优化、模型部署、量化、KV Cache、训练平台、集群、性能优化
```

### Recruiting Notes

Infra candidates may not always describe themselves as LLM candidates.

Some of them come from search, recommendation, ads, cloud computing, high-performance computing, or distributed systems. For these roles, sourcing should not be limited to “large model” keywords.

## 12. Candidate Evaluation Questions

When evaluating foundation model candidates, I would avoid relying only on job titles.

The following questions can help clarify the candidate’s real experience.

### Depth of Involvement

* Which part of the model lifecycle did you work on?
* Were you involved in training, post-training, evaluation, data, infra, or deployment?
* What was your personal contribution?
* Were you close to the core model work, or mainly using models downstream?

### Scale of Experience

* What model scale or data scale did you work with?
* Did you work on experiments, production training, or both?
* What compute environment did you use?
* Was your work done at research scale or production scale?

### Research vs. Engineering

* Was your work more research-oriented or engineering-oriented?
* Did you design methods, implement systems, run experiments, or support deployment?
* How did your work affect model performance or product experience?

### Data and Evaluation Awareness

* How did you evaluate whether the model improved?
* What kind of data quality issues did you encounter?
* How did data or eval results influence the next round of training?

### Collaboration Context

* Which teams did you work with?
* Did you collaborate with infra, data, product, safety, or research teams?
* What trade-offs did you need to make?

## 13. Sourcing Strategy

For foundation model roles, I would not start with only one keyword such as “LLM”.

A better sourcing strategy is to combine several layers.

### Role Keywords

```text
foundation model, large language model, LLM, research scientist, research engineer, machine learning engineer
```

### Lifecycle Keywords

```text
pre-training, post-training, alignment, RLHF, SFT, evaluation, data quality, inference, distributed training
```

### Technical Keywords

```text
Transformer, MoE, scaling law, reward model, preference optimization, DPO, PPO, GRPO, synthetic data, benchmark, CUDA, NCCL
```

### Capability Keywords

```text
reasoning, coding, math, tool use, long context, multimodal, safety, hallucination
```

### Source Keywords

```text
open-source model, model release, technical report, benchmark, paper, GitHub, Hugging Face
```

The goal is to move from broad keyword search to a more structured sourcing map.

## 14. Candidate Motivation Hypotheses

Foundation model candidates may consider new opportunities for different reasons.

Possible motivation points:

* Access to better compute resources;
* Better data resources;
* More ownership over model direction;
* Stronger research team;
* Faster product feedback loop;
* Better compensation;
* Better location or work arrangement;
* More visible model impact;
* Less internal coordination cost;
* More freedom to publish or open source.

Possible concerns:

* Compute uncertainty;
* Unclear research direction;
* Weak data pipeline;
* Weak infra support;
* Unstable company funding;
* Limited product adoption;
* Poor collaboration between research and engineering;
* High work intensity without clear upside.

## 15. Outreach Angle

For foundation model candidates, a generic outreach message is usually not enough.

The message should depend on the candidate’s background.

### For pre-training candidates

Emphasize:

* Model scale;
* Compute resources;
* Research direction;
* Training ownership;
* Team quality.

### For post-training candidates

Emphasize:

* Model behavior problems;
* Reasoning, coding, tool use, or alignment challenges;
* Product feedback loop;
* Opportunity to influence real user experience.

### For data candidates

Emphasize:

* Data quality problems;
* Ownership of the data pipeline;
* Connection between data and model capability;
* Opportunity to build high-quality datasets.

### For evaluation candidates

Emphasize:

* The role of evaluation in model iteration;
* Real-world model failure cases;
* Safety, reliability, and product quality;
* Impact on training and product decisions.

### For infra candidates

Emphasize:

* System scale;
* GPU efficiency;
* Training and inference challenges;
* Engineering complexity;
* Cost and performance impact.

## 16. Example: Breaking Down a Foundation Model JD

If a JD says:

> We are hiring a foundation model researcher to improve model reasoning and alignment.

I would not only search for “foundation model researcher”.

I would break it down into several possible directions:

| Direction     | Search Focus                                                 |
| ------------- | ------------------------------------------------------------ |
| Reasoning     | math reasoning, code reasoning, verifier, RL, tool use       |
| Alignment     | RLHF, DPO, reward model, preference learning, safety         |
| Post-training | SFT, instruction tuning, model behavior, tool use            |
| Evaluation    | reasoning eval, coding benchmark, safety eval, applied evals |
| Data          | high-quality reasoning data, synthetic data, preference data |

Then I would ask:

* Is this role closer to post-training or pure research?
* Does the team need someone to design algorithms, run experiments, build data, or improve evaluation?
* Is large-scale training experience required, or is strong reasoning / alignment research enough?
* Which companies and teams are most likely to have this kind of person?
* What would make this opportunity attractive to candidates from those teams?

## 17. Questions to Keep Updating

This map is still incomplete. Questions I want to keep tracking:

1. How do different companies divide pre-training, post-training, data, evals, and infra teams?
2. Which foundation model roles are truly scarce in the market?
3. Which candidate backgrounds are easier to transfer into foundation model teams?
4. How important are top papers compared with large-scale training experience?
5. How do foundation model candidates evaluate compute, data, team quality, and product adoption?
6. Which roles are becoming more important as models move from benchmark competition to product competition?
7. How will open-source models affect the foundation model talent market?
8. What parts of foundation model recruiting can be supported by tools, and what parts still require human judgment?

## 18. Personal Note

For me, the biggest lesson is that “large model recruiting” should not be treated as one single category.

A foundation model team contains different types of work, and each type has its own talent pool.

To build a useful talent map, I need to understand not only company names and job titles, but also the model lifecycle behind them:

```text
Data → Pre-training → Post-training → Evaluation → Deployment → Product Feedback
```

Only after understanding this lifecycle can I map candidates more accurately and have more meaningful conversations with them.
