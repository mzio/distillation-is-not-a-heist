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

## 1. Chinese open weights *create* American competition that wouldn't otherwise exist

Without Chinese open-weight releases, the American frontier-AI market would consist of OpenAI, Anthropic, and Google DeepMind — plus a long tail of wrapper products that depend on their APIs. *With* Chinese open-weight releases, there is a robust American middle layer building competitive products on top: post-training labs, neo-clouds, RL-as-a-service companies, and at least one multibillion-dollar end-user product. That middle layer is what keeps the three frontier labs from segmenting the market by vertical and pricing as comfortable incumbents.

Cursor is the clearest concrete case. Most of its <span class="cite">growth from $500M to $2B in annualized revenue between June 2025 and February 2026<span class="src"><strong>Cursor ARR trajectory</strong><br>$100M ARR Jan 2025, $500M June 2025, $1B Nov 2025, $2B Feb 2026 — fastest SaaS scaling on record. Now in talks at a ~$50B valuation.<br><a href="https://sacra.com/c/cursor/" target="_blank" rel="noopener">Sacra: Cursor revenue & funding</a></span></span> ran on routing to Anthropic and OpenAI APIs — the American frontier labs were the direct beneficiaries of Cursor's success, not the victims of it, and the open-weight story is not what built the first $2B. What the open-weight story *did* do shows up in what Cursor built next. When Cursor went to ship its own in-house model to control margins and pricing leverage at scale, <span class="cite">it built Composer 2 on top of Kimi K2.5 — an open-weight Chinese base model from Moonshot AI<span class="src"><strong>Composer 2 base model (officially confirmed)</strong><br>Cursor co-founder Aman Sanger and VP DevEd Lee Robinson confirmed in March 2026 that Composer 2 was built on Kimi K2.5 after the base model was identified in API headers. Cursor reports ~3/4 of total training compute came from its own continued pretraining + RL on top of Kimi. Moonshot's official account confirmed the partnership runs through Fireworks AI under a commercial license.<br><a href="https://cursor.com/blog/composer-2-technical-report" target="_blank" rel="noopener">Cursor: Composer 2 technical report</a><br><a href="https://techcrunch.com/2026/03/22/cursor-admits-its-new-coding-model-was-built-on-top-of-moonshot-ais-kimi/" target="_blank" rel="noopener">TechCrunch coverage</a></span></span> — with roughly three-quarters of Composer 2's total training compute coming from Cursor's own continued pretraining and RL on top of the Kimi base. This is not "Cursor shipping a Chinese model"; it is Cursor shipping a Cursor model that would not exist without a high-quality open-weight base to start from. The point generalizes: every American AI product company that wants to control its own model economics — rather than live on API margin from the Big 3 forever — currently has two choices, raise $100M+ to train from scratch, or build on top of an open-weight base. Almost all are choosing the latter, and the highest-quality open-weight bases available right now happen to be Chinese.

The same dynamic is happening one layer down. The American neo-cloud and inference layer — <span class="cite">Fireworks AI at $315M ARR, up 416% YoY<span class="src"><strong>Fireworks AI ARR</strong><br>$315M ARR Feb 2026, +416% YoY; customer base grew from ~1,000 to 10,000+ companies in 2025.<br><a href="https://sacra.com/c/fireworks-ai/" target="_blank" rel="noopener">Sacra: Fireworks AI</a></span></span>, <span class="cite">Together AI at roughly $150M ARR<span class="src"><strong>Together AI revenue</strong><br>Raised $305M Series B Feb 2025; generates ~$150M+ annualized revenue from open-model inference hosting.<br><a href="https://sacra.com/c/together-ai/" target="_blank" rel="noopener">Sacra: Together AI</a></span></span>, plus Groq, Cerebras, and SambaNova on custom American silicon — built nine-figure businesses on top of serving and post-training the open-weight models the Foreign Affairs piece wants to restrict. The RL-as-a-service layer (continued pretraining, fine-tuning, eval, agent post-training) is similarly American-owned and similarly dependent on having a capable open-weight starting point. None of this revenue, and none of this competitive pressure on the Big 3, exists without the open-weight releases.

The underlying economics explain why: <span class="cite">DeepSeek-V3's final training run reportedly cost $5.576M in H800 hours<span class="src"><strong>DeepSeek-V3 training cost</strong><br>2.788M H800 GPU-hours total (pre-training + context extension + post-training) at $2/hr = $5.576M. Excludes prior research and ablations. From the DeepSeek-V3 technical report.<br><a href="https://arxiv.org/abs/2412.19437" target="_blank" rel="noopener">arXiv:2412.19437</a></span></span> — orders of magnitude less than what frontier US labs spend. Restricting access to these bases would not strengthen American competition. It would restrict it to whoever can afford a multi-hundred-million-dollar training run, which is exactly the three incumbents the middle layer is currently keeping honest. The likely result is not "American AI leadership" in any distributed sense; it is a narrower, more concentrated American AI industry in which OpenAI, Anthropic, and Google DeepMind face less domestic competition than they do today.

## 2. "Open weights" and "geopolitical dependence" are not the same thing

The piece's central causal claim is a slippery slope: a developer picks DeepSeek for cost, then Alibaba Cloud for hosting, then Huawei chips for compute, and "what starts as a cost-driven choice becomes a full-stack, enduring dependence." This is asserted, not argued.

Open weights are decoupled from where they originated. <span class="cite">Chinese open-weight models accounted for 17.1% of global AI model downloads in the year through August 2025<span class="src"><strong>Open-weight download share</strong><br>Chinese models reached 17.1% of global AI model downloads in the year through August 2025, overtaking US download share in some measurements after R1's January 2025 release.<br><a href="https://www.digitaltoday.co.kr/en/view/49856/" target="_blank" rel="noopener">DigitalToday coverage</a></span></span>, and the overwhelming majority of those downloads ran on American-built infrastructure: Hugging Face (US), vLLM and SGLang (US universities), llama.cpp (a primarily Western community project), and Apple Silicon and Nvidia hardware on the device side. <span class="cite">Hugging Face data showed user-generated derivatives of Qwen-family models exceeded the combined total of Google and Meta models<span class="src"><strong>HF derivative model counts</strong><br>Per Hugging Face activity data (late 2025), derivative/fine-tuned versions of Alibaba's Qwen family on the platform exceeded the combined total of Google and Meta open-weight derivatives.<br><a href="https://www.digitaltoday.co.kr/en/view/49856/" target="_blank" rel="noopener">DigitalToday coverage</a></span></span> — that is a flood of American and global developers fine-tuning Chinese weights toward their own ends, which is approximately the opposite of "enduring dependence on Beijing."

A US enterprise running Qwen on AWS is not dependent on Alibaba in any sense that resembles a Huawei 5G customer being dependent on Huawei. The telecom analogy the piece reaches for requires infrastructure the user cannot replicate. Weights are exactly the opposite — they are the thing the user owns once downloaded.

The right precedent is not Huawei or Belt and Road. It is PyTorch and Linux. PyTorch was developed at Meta and became the world's de facto deep-learning framework — used by every American lab, every Chinese lab, every research group on earth — and no one seriously argues that Meta "controls" global AI research as a result, because PyTorch is genuinely open: anyone can read it, fork it, and modify it. <span class="cite">PyTorch is now governed by the PyTorch Foundation under the Linux Foundation<span class="src"><strong>PyTorch governance</strong><br>In September 2022, Meta transferred PyTorch governance to the PyTorch Foundation under the Linux Foundation. The project is now multi-stakeholder, with member contributions from AMD, AWS, Google, Meta, Microsoft, and Nvidia.<br><a href="https://pytorch.org/foundation" target="_blank" rel="noopener">PyTorch Foundation</a></span></span>, and "American origin" has become a historical fact about the project rather than an ongoing source of geopolitical leverage. Linux was written by a Finnish student and now runs <span class="cite">over 96% of the world's top one million web servers and the entire Android ecosystem<span class="src"><strong>Linux deployment scale</strong><br>Linux runs ~96% of the top 1M web servers and is the kernel underlying Android (~70% of global mobile market share), ChromeOS, embedded systems, and most cloud infrastructure. "Finnish geopolitical influence over computing" is not a meaningful category despite this scale.<br><a href="https://w3techs.com/technologies/details/os-linux" target="_blank" rel="noopener">W3Techs server share</a></span></span> — and "Finnish geopolitical influence over computing" is not a meaningful category, because the kernel is forked and rebuilt by every vendor that ships it. The piece's framing requires Chinese-origin open weights to be categorically different from these precedents. It does not explain why.

Vendor lock-in is a real phenomenon and worth taking seriously. It happens when migrating away from a vendor is costly because of proprietary formats, data egress fees, integrated services, hardware tying, or licensing tail. None of these apply to open weights. Downloading Qwen does not bind a developer to Alibaba's cloud. Running DeepSeek on AWS does not generate a contractual or technical relationship with DeepSeek. There is no proprietary inference engine, no licensing renewal, no upgrade path that compels continued use of any Chinese product. If a better US-developed equivalent appears tomorrow, switching cost is: download the new weights. The "creep" the piece describes — model adoption leading inexorably to cloud adoption leading inexorably to chip adoption — requires a causal mechanism that the piece never specifies, because there isn't one. The mechanism it gestures at (network effects, ecosystem gravity) actually runs the other direction: developers already on AWS, Apple Silicon, and Hugging Face have every reason to *stay* on American infrastructure even as they swap which weights they fine-tune.

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

<small><em>This piece was ghost-written by Claude (Opus 4.7 (1M context)) via prompt-to-prose instructions by the author. The arguments are the author's own, applying that good old liberal-arts education of actually thinking about an article's points, and engaging both as an example of discourse to his lab and out of disagreement with the incautious framing of the original piece. The author would encourage others to do the same. Any errors of fact or judgment are jointly owned.</em></small>

<small><strong>Disclosure.</strong> <em>The author has previously consulted at Together AI, one of the neo-clouds mentioned by name in this piece, and has helped start an American neo-lab.</em></small>
