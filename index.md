---
title: "The Distillation 'Heist' Is Quietly Powering American AI"
date: 2026-05-29
---

<style>
.cite {
  position: relative;
  border-bottom: 1px dotted #4a7ec4;
  cursor: help;
  display: inline;
}
.cite > .src {
  visibility: hidden;
  opacity: 0;
  position: absolute;
  bottom: calc(100% + 10px);
  left: 50%;
  transform: translateX(-50%);
  background: #1a1a1a;
  color: #f0f0f0;
  padding: 10px 14px;
  border-radius: 8px;
  font-size: 0.78em;
  font-weight: 400;
  line-height: 1.5;
  white-space: normal;
  width: max-content;
  max-width: 320px;
  z-index: 100;
  box-shadow: 0 6px 20px rgba(0,0,0,0.25);
  transition: opacity 0.15s ease, visibility 0.15s ease;
  pointer-events: none;
  text-align: left;
  border-bottom: none;
  cursor: default;
}
.cite > .src::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 6px solid transparent;
  border-top-color: #1a1a1a;
}
.cite > .src a {
  color: #7eb6ff;
  text-decoration: none;
}
.cite > .src a:hover {
  text-decoration: underline;
}
.cite:hover > .src,
.cite:focus-within > .src,
.cite > .src:hover {
  visibility: visible;
  opacity: 1;
  pointer-events: auto;
}
@media (max-width: 640px) {
  .cite > .src {
    max-width: 260px;
    left: 0;
    transform: none;
  }
  .cite > .src::after { left: 20px; transform: none; }
}
</style>

# The Distillation "Heist" Is Quietly Powering American AI

A recent Foreign Affairs piece, [*China's AI Heist*](https://www.foreignaffairs.com/china/chinas-ai-heist), argues that Chinese labs distilling US frontier models constitutes "industrial-scale extraction" that threatens to lose the United States the AI "distribution war." It calls for extending the Foreign Direct Product Rule to cover Chinese open-weight models, formal entity designations, and IEEPA-backed asset freezes — and frames all of this in the cadence of a national emergency.

**The framing is incautious and reads more talking-head than policy analysis.** The proposed remedies misdiagnose the phenomenon, would hurt the firms they claim to protect, and rest on a slippery slope from "weights" to "geopolitical dependence" that does not survive contact with the actual deployment topology of these models. The piece is right that distribution matters as much as training. It is wrong about who is winning it, and it is wrong about what to do.

Three points.

## 1. Distillation has *expanded*, not undermined, American AI competition

The American AI economy is in the middle of a Cambrian explosion that is, in significant part, powered by Chinese open-weight releases. The clearest case is Cursor — the fastest-scaling SaaS company on record, <span class="cite">growing from $500M to $2B in annualized revenue between June 2025 and February 2026<span class="src"><strong>Cursor ARR trajectory</strong><br>Reached $500M ARR June 2025, $1B by Nov 2025, $2B by Feb 2026 — fastest SaaS scaling on record.<br><a href="https://sacra.com/c/cursor/" target="_blank" rel="noopener">Sacra: Cursor revenue & funding</a></span></span> at a $29.3B valuation. The flagship model powering that growth, <span class="cite">Composer 2, was reportedly post-trained on Kimi K2.5 — a Chinese open-weight model<span class="src"><strong>Composer 2 base model</strong><br>Cursor's Composer 2 was reportedly built on Kimi K2.5's open weights with a "4x scale-up" in training compute to bake in proprietary self-summarization logic. Developers identified shared tokenizers and other artifacts; Composer-1 was also suspected to be a fine-tune of an open-source Chinese base.<br><a href="https://venturebeat.com/technology/cursors-composer-2-was-secretly-built-on-a-chinese-ai-model-and-it-exposes-a" target="_blank" rel="noopener">VentureBeat report</a></span></span> — with Cursor's proprietary data and post-training baked on top. The headline-grabbing American AI productivity tool of 2026 is, mechanically, a post-trained Chinese open-weight model. This is exactly the pattern the Foreign Affairs piece treats as a problem, and it is exactly the pattern producing a multibillion-dollar American business.

The neo-cloud layer that hosts these models is even more clearly American-coded: <span class="cite">Fireworks AI hit $315M in annualized revenue by February 2026, up 416% year-over-year<span class="src"><strong>Fireworks AI ARR</strong><br>$315M ARR Feb 2026, +416% YoY; customer base grew from ~1,000 to 10,000+ companies in 2025.<br><a href="https://sacra.com/c/fireworks-ai/" target="_blank" rel="noopener">Sacra: Fireworks AI</a></span></span>, and <span class="cite">Together AI runs at roughly $150M ARR<span class="src"><strong>Together AI revenue</strong><br>Raised $305M Series B Feb 2025; generates ~$150M+ annualized revenue from open-model inference hosting.<br><a href="https://sacra.com/c/together-ai/" target="_blank" rel="noopener">Sacra: Together AI</a></span></span>, with both businesses built largely on serving the open-weight models the piece wants to restrict. Groq, Cerebras, and SambaNova compete in the same market on American custom silicon. None of this revenue exists without the open-weight releases.

And the underlying economics are what make this revenue possible: <span class="cite">DeepSeek-V3's final training run reportedly cost $5.576M in H800 hours<span class="src"><strong>DeepSeek-V3 training cost</strong><br>2.788M H800 GPU-hours total (pre-training + context extension + post-training) at $2/hr = $5.576M. Excludes prior research and ablations. From the DeepSeek-V3 technical report.<br><a href="https://arxiv.org/abs/2412.19437" target="_blank" rel="noopener">arXiv:2412.19437</a></span></span> — orders of magnitude less than what frontier US labs spend — which is *why* American startups can afford to build on these weights without raising frontier-scale capital. Removing that input does not strengthen US competition. It restricts it to whoever can afford a multi-hundred-million-dollar training run, which is a much smaller set of firms.

## 2. "Open weights" and "geopolitical dependence" are not the same thing

The piece's central causal claim is a slippery slope: a developer picks DeepSeek for cost, then Alibaba Cloud for hosting, then Huawei chips for compute, and "what starts as a cost-driven choice becomes a full-stack, enduring dependence." This is asserted, not argued.

Open weights are decoupled from where they originated. <span class="cite">Chinese open-weight models accounted for 17.1% of global AI model downloads in the year through August 2025<span class="src"><strong>Open-weight download share</strong><br>Chinese models reached 17.1% of global AI model downloads in the year through August 2025, overtaking US download share in some measurements after R1's January 2025 release.<br><a href="https://www.digitaltoday.co.kr/en/view/49856/" target="_blank" rel="noopener">DigitalToday coverage</a></span></span>, and the overwhelming majority of those downloads ran on American-built infrastructure: Hugging Face (US), vLLM and SGLang (US universities), llama.cpp (a primarily Western community project), and Apple Silicon and Nvidia hardware on the device side. <span class="cite">Hugging Face data showed user-generated derivatives of Qwen-family models exceeded the combined total of Google and Meta models<span class="src"><strong>HF derivative model counts</strong><br>Per Hugging Face activity data (late 2025), derivative/fine-tuned versions of Alibaba's Qwen family on the platform exceeded the combined total of Google and Meta open-weight derivatives.<br><a href="https://www.digitaltoday.co.kr/en/view/49856/" target="_blank" rel="noopener">DigitalToday coverage</a></span></span> — that is a flood of American and global developers fine-tuning Chinese weights toward their own ends, which is approximately the opposite of "enduring dependence on Beijing."

A US enterprise running Qwen on AWS is not dependent on Alibaba in any sense that resembles a Huawei 5G customer being dependent on Huawei. The telecom analogy the piece reaches for requires infrastructure the user cannot replicate. Weights are exactly the opposite — they are the thing the user owns once downloaded.

The piece's most empirically-grounded concern is embedded political behavior — the CrowdStrike finding that DeepSeek-R1 produced ~50% more vulnerable code when prompts mentioned politically sensitive terms like "Tibet" or "Uyghurs," and the broader observation that <span class="cite">safety training does not transfer through distillation<span class="src"><strong>Anthropic distillation claims</strong><br>Feb 2026: Anthropic alleged DeepSeek, Moonshot, and MiniMax used ~24,000 fake accounts and 16M+ exchanges to extract Claude's capabilities. Safety filtering and alignment tuning are applied post-training and do not transfer to distilled models.<br><a href="https://techcrunch.com/2026/02/23/anthropic-accuses-chinese-ai-labs-of-mining-claude-as-us-debates-ai-chip-exports/" target="_blank" rel="noopener">TechCrunch coverage</a></span></span>. This is real and worth investigating. But it does not justify the remedy. Trained-in bias and missing safety scaffolding are exactly what the American post-training ecosystem already specializes in: fine-tuning, abliteration, RL-from-human-feedback, and safety filtering are commercial products sold by US firms — the same firms whose revenue depends on having capable open weights to fine-tune in the first place. Unless the claim is that Chinese labs are smuggling spying code into the weights themselves — and the piece notably stops short of that claim — these behavioral artifacts are downstream-addressable by precisely the American companies the policy would harm.

## 3. The proposed remedies have a track record, and it doesn't favor them

The piece asks Washington to extend FDPR to AI models, citing its success against networking equipment and semiconductor tools. The more recent and more relevant precedent — the H100, H800, and B200 chip controls — is one the piece does not engage with, and it should.

The chip controls did not stop Chinese model progress. They forced it into a more compute-efficient regime — precisely the regime in which DeepSeek-V3 and R1 emerged, trained on the very H800s that the export controls produced as a workaround. They accelerated Huawei Ascend and SMIC roadmaps that were, beforehand, second-tier commercial projects. And <span class="cite">they cost Nvidia an estimated $5.5B in immediate charges plus a projected $15B in lost China revenue as of April 2025<span class="src"><strong>Nvidia China revenue impact</strong><br>April 2025: Nvidia disclosed a $5.5B charge from the inability to ship H20 processors to China, plus a projected additional $15B in lost revenue from the Chinese market due to extended export restrictions.<br><a href="https://www.csis.org/analysis/understanding-biden-administrations-updated-export-controls" target="_blank" rel="noopener">CSIS analysis</a></span></span> — revenue that funds the next generation of American AI training. The net effect on US AI leadership is, charitably, ambiguous.

Extending an FDPR-style regime to *models* would compound this. American frontier labs would lose a downstream commercial market. American neo-clouds — the Fireworks and Together AIs of the world that built nine-figure businesses serving these weights — would lose a substantial share of revenue. American startups would lose the cheap, capable open-weight backbone they currently build on. And Chinese labs, having already absorbed the lessons of the chip controls, would respond by training more from scratch — a path they are well-resourced to take, and one that, by the piece's own logic, would produce models with *more* distinctive behavioral artifacts, not fewer. Restriction makes the problem the piece identifies worse.

If the concern is American AI leadership, the lever is not restricting how Americans can use foreign open-weight models. It is what the piece correctly identifies as a secondary recommendation and should have made primary: funding and incentivizing American firms to release competitive open-weight models. Gemma 4 is a step. Llama has lost ground that needs to be recovered. The actual policy is *more American open weights, not fewer Chinese ones*.

## A closing note

"The distribution layer matters" and "the United States is losing a heist" are different claims, and the piece slides between them. The first is correct and important. The second is a narrative dressed in policy clothing. The American AI ecosystem is, on the actual numbers, winning the distribution game — on the strength of American chips, American clouds, American agentic tooling, and American post-training services, all of it amplified, not threatened, by the open-weight Chinese models the piece wants to restrict.

Policy should match the deployment topology, not the talking points.

---

<small><em>This piece was ghost-written by Claude (Anthropic) from a back-and-forth conversation with the author. The arguments — the read of the original piece as hawkish-by-default, the observation that open weights are decoupled from infrastructure dependence, and the skepticism that an FDPR-style escalation would survive its own track record — are the author's: liberal-arts-trained skepticism applied to a technical policy question. The prose is Claude's. Any errors of fact or judgment are jointly owned.</em></small>
