### R1 (2.5)

> The motivation feels underwhelming. The paper does not convincingly show that real lobbyists would use such methods, nor that policy experts would be fooled.

> Provide stronger evidence that this scenario parallels real lobbying or that legislative drafters/analysts might genuinely be misled.

We would like to clarify that we acknowledge that legal matters and lobbying are very comprehensive processes and include several other complicated elements which cannot be imitated for this study. Our proposed framework focuses on some objective elements which are relevant to produce a measurable form of this subtle deception, in an algorithmic way.

We build a robust algorithm to identify the benefactors which shows strong performance for initial generations. We do not claim for it to be at par with policy experts at the current stage, and it holds the sole purpose of identifying a benefactor company.

Along with this, the human evaluations of amendments show strong support for the generations being sensible and also showing certain patterns of strategies used.

**Reviewer 875j** has referred an important and relevant previous work [1] which builds a classifier for lobbied bills. In our case, we required a classifier for benefactors of amendment suggestions. Due to immense situational understanding and reasoning capabilities of LLMs, we were able to build a zero-shot strong classifier using the proposed algorithm. 

> The novelty is limited, as iterative feedback loops for LLMs are already a well-studied approach. The authors merely apply it to a legislative “deception” case without deeply expanding the technique itself

We’d like to reiterate that this work does not propose the iterative feedback loop as its novelty and we’ve mentioned that we use this simple and well known method as a tool to uncover the capabilities of LLMs for such subtle deception which has not been explored before. Beyond that, our analysis is focussed only on what supports and hinders these intelligent capabilities in LLMs.

> Consider comparing human detection results to the LLM-based critic, to reinforce practical relevance.

The detection mechanism requires processing a large bill text and business information of several companies (>= 4) from the SEC10K filings, and hiring external human evaluators for this brings in a financial constraint for our group.
Therefore, we currently rely on the robust algorithmic detection which shows strong performance, upto 83% with 72B model and 94% with GPT4 (Appendix A.2). This strong benefactor identification performance supported our decision to continue this study with it.

While our aim of detecting and analysing subtle deception behaviour was verified by 10 in-house AI expert evaluators and authors themselves.

Citations:

[1] [Slobozhan et al. 2020. Which bills are lobbied? Predicting and interpreting lobbying activity in the US](https://arxiv.org/abs/2005.06386)


### R2 (3.5)

> This study focus on using LLM to deceive LLM-based detectors, which may not be the most practical scenario.

> First, the study focuses on using LLM to deceive LLM-based detectors, which may not be the most practical scenario. I'm curious about how the results would change if the critics are acted by humans.

The aim is to evaluate the subtle deception capabilities. The robust detection algorithm shows strong identification capabilities and hence was used consistently. We have also referred to several works [citations] supporting the robustness of this method for identifying latent intents in legal and political contexts.
Our human evaluations from in-house AI experts verify the sensibility of generated amendments and evaluation by authors identifies certain patterns of subtle deception, which follows the aim of the work.
This identification of benefactors requires comprehensive processing of large bill texts and (>= 4) company business details from SEC10K filings, and hiring external human experts brings in a financial constraint for the group, at this stage. We do not have enough in-house power to perform this evaluation even on a small set.

**Reviewer 875j** has referred to an important and relevant previous work [6] which builds a classifier for lobbied bills. In our case, we required a classifier for benefactors of amendment suggestions. Due to immense situational understanding and reasoning capabilities of LLMs, we were able to build a zero-shot strong classifier using the proposed algorithm. 

> Lack evalution using latest production models like GPT-4.

> Second, the study lacks evaluation using the latest production models like GPT-4. I understand this may cost a lot of resources, but it would be interesting to see how the results would be. Probably just a few experiments would be enough to show the difference.

We highly appreciate the reviewer’s understanding of our financial constraints. This became the major reason for limiting to open-source models. We provide results in Appendix A.2 for using GPT-4-Turbo as only the critic for identification. We see stronger identification of the initial generations by Qwen 72B, going up to 94%. 
We provide identification rates only for generations of two trials to keep costs down. This evaluation alone cost over a thousand USD and was supported by credits granted by OpenAI for this project.
As we couldn’t dive deeper into the GPT-4 evaluation, we decided to keep it in the appendix. We welcome the reviewer’s input on if this should be brought to the main body. 

We hope these results provide some clarity.


Citations: 

[1] [Wu et al. 2023. LLMs Can Be Used to Estimate the Latent Positions of Politicians](https://arxiv.org/abs/2303.12057)\
[2] [Lowen et al. 2012. Testing the power of arguments in referendums: A Bradley–Terry approach](https://www.sciencedirect.com/science/article/abs/pii/S0261379411000953?via%3Dihub)\
[3] [Carlson and Montgomery, 2017. A Pairwise Comparison Framework for Fast, Flexible, and Reliable Human Coding of Political Texts](https://www.cambridge.org/core/journals/american-political-science-review/article/abs/pairwise-comparison-framework-for-fast-flexible-and-reliable-human-coding-of-political-texts/017BF6B024228962FDF90B47FD90EF5F)\
[4] [Hopkins and Noel, 2022. Trump and the Shifting Meaning of “Conservative”: Using Activists’ Pairwise Comparisons to Measure Politicians’ Perceived Ideologies](https://www.cambridge.org/core/journals/american-political-science-review/article/abs/trump-and-the-shifting-meaning-of-conservative-using-activists-pairwise-comparisons-to-measure-politicians-perceived-ideologies/EC8511D8EB16CD947D9B5DC8201F0515)\
[5] [Maystre and Grossglauser, 2015. Fast and Accurate Inference of Plackett–Luce Models](https://proceedings.neurips.cc/paper_files/paper/2015/file/2a38a4a9316c49e5a833517c45d31070-Paper.pdf)\
[6] [Slobozhan et al. 2020. Which bills are lobbied? Predicting and interpreting lobbying activity in the US](https://arxiv.org/abs/2005.06386)
