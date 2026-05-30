---
title: "The Distillation 'Heist' Is Quietly Powering American AI"
date: 2026-05-29
---

# The Distillation "Heist" Is Quietly Powering American AI

A recent Foreign Affairs piece by Jared Dunnmon, Avanika Narayan, and Jon Saad-Falcon ([*China's AI Heist*](https://www.foreignaffairs.com/china/chinas-ai-heist)) argues that Chinese labs distilling US frontier models constitutes "industrial-scale extraction" that threatens to lose the United States the AI "distribution war." It calls for extending the Foreign Direct Product Rule to cover Chinese open-weight models, formal entity designations, and IEEPA-backed asset freezes — and frames all of this in the cadence of a national emergency.

**The framing is incautious and reads more talking-head than policy analysis.** The proposed remedies misdiagnose the phenomenon, would hurt the firms they claim to protect, and rest on a slippery slope from "weights" to "geopolitical dependence" that does not survive contact with the actual deployment topology of these models. The authors are right that distribution matters as much as training. They are wrong about who is winning it, and they are wrong about what to do.

Three points.

## 1. Distillation has *expanded*, not undermined, American AI competition

The American AI economy is in the middle of a Cambrian explosion that is directly powered by Chinese open-weight releases. Cursor ships completions backed by fine-tuned DeepSeek variants. Perplexity serves R1. A long tail of American "neo-clouds" — Together, Fireworks, Groq, Cerebras, OpenRouter — generates real revenue serving Qwen and DeepSeek on American hardware, in American data centers, billed in dollars. The RL-as-a-service shops have built profitable businesses post-training these models for enterprise customers who would otherwise have nothing to fine-tune at all.

If the goal of policy is "American firms making money on AI," the status quo is working. The article's proposed FDPR-on-models would criminalize commercial deployment of distilled Chinese models, cutting off this revenue stream entirely and disadvantaging US startups against international competitors who would face no such constraint. The cure attacks the patient.

## 2. "Open weights" and "geopolitical dependence" are not the same thing

The article's central causal claim is a slippery slope: a developer picks DeepSeek for cost, then Alibaba Cloud for hosting, then Huawei chips for compute, and "what starts as a cost-driven choice becomes a full-stack, enduring dependence." This is asserted, not argued.

Open weights are decoupled from where they originated. Qwen runs beautifully on Apple Silicon. DeepSeek is served via AWS Bedrock. The agentic and inference tooling that actually moves these models — vLLM, SGLang, llama.cpp — is built and maintained in the United States and Europe and runs on whatever hardware you point it at. A US enterprise using Qwen on AWS is not in any meaningful sense dependent on Alibaba, in the way a Huawei 5G customer is dependent on Huawei. The telecom analogy requires infrastructure the user cannot replicate. Weights are exactly the opposite — they are the thing the user owns once downloaded.

The article's strongest residual concern is embedded political behavior: the CrowdStrike finding that DeepSeek-R1 produced ~50% more vulnerable code when prompts mentioned "Tibet" or "Uyghurs" is genuinely odd and worth investigating. But it does not justify the remedy. Trained-in bias is exactly what the American post-training ecosystem already specializes in scrubbing: fine-tuning, abliteration, RL-from-human-feedback, and safety filtering are commercial products sold by American firms. Unless the claim is that Chinese labs are smuggling spying code into the weights themselves — and the article notably stops short of that claim — these behavioral artifacts are downstream-addressable by precisely the American companies the policy would harm. The economically rational response to a slightly-biased capable open-weight model is to fine-tune it. The economically rational response to a restriction is to leave the market.

## 3. The proposed remedies have a track record, and it doesn't favor them

The article asks Washington to extend FDPR to AI models, citing its success against networking equipment and semiconductor tools. The more recent and more relevant precedent — the H100 and B200 chip controls — is one the article does not engage with, and it should.

The chip controls did not stop Chinese model progress. They forced it into a more compute-efficient regime, which is precisely the regime in which DeepSeek-V3 and R1 emerged. They accelerated Huawei Ascend and SMIC roadmaps that were, beforehand, second-tier commercial projects. They cost Nvidia tens of billions in revenue that ultimately funds the next generation of American training. The net effect on US AI leadership is, charitably, ambiguous.

Extending an FDPR-style regime to models would compound this. American frontier labs would lose a downstream commercial market. American neo-clouds would lose hosting revenue. American startups would lose the cheap, capable open-weight backbone they currently build on. And Chinese labs, having already absorbed the lessons of the chip controls, would respond by training more from scratch — a path they are well-resourced to take, and one that, by the article's own logic, would produce models with *more* distinctive behavioral artifacts, not fewer. Restriction makes the problem the article identifies worse.

If the concern is American AI leadership, the lever is not restricting how Americans can use foreign open-weight models. It is what the article correctly identifies as a secondary recommendation and should have made primary: funding and incentivizing American firms to release competitive open-weight models. Gemma 4 is a step. Llama has lost ground that needs to be recovered. The actual policy is *more American open weights, not fewer Chinese ones*.

## A closing note

"The distribution layer matters" and "the United States is losing a heist" are different claims, and the article slides between them. The first is correct and important. The second is a narrative dressed in policy clothing. The American AI ecosystem is, on the actual numbers, winning the distribution game — on the strength of American chips, American clouds, American agentic tooling, and American post-training services, all of it amplified, not threatened, by the open-weight Chinese models the article wants to restrict.

Policy should match the deployment topology, not the talking points.
