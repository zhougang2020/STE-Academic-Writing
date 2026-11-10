# Test Samples

Test the skill on real AI/IR academic paper paragraphs. For each sample, the "Before" text contains common academic writing issues, and the "After" text shows the expected result after applying Draft/Rewrite/Polish modes.

---

## Test 1: Polish mode — remove hedge stacks and nominalization

**Before:**

It is important to note that our method demonstrates significant improvements over the baseline, which is facilitated by the utilization of a novel attention mechanism. Additionally, it should be noted that the performance of the model is substantially enhanced through the incorporation of multi-scale features.

**After:**

Our method improves over the baseline by using a new attention mechanism. The model also benefits from multi-scale features.

**Violations fixed:**

- Hedge stack "It is important to note that" → deleted
- "demonstrates" → "improves" (verb for action, short word)
- "facilitated by the utilization of" → "by using" (nominalization + leverage)
- "Additionally, it should be noted that" → deleted (hedge stack)
- "performance ... is substantially enhanced through the incorporation of" → "also benefits from" (nominalization)

---

## Test 2: Polish mode — synonym rotation

**Before:**

We validate our approach on three benchmarks. To verify the effectiveness, we compare with several baselines. We also confirm that the model generalizes well. Our results check out across all settings.

**After:**

We evaluate our approach on three benchmarks. To verify the effectiveness, we compare with several baselines. We also verify that the model generalizes well. Our results hold across all settings.

**Violations fixed:**

- Synonym rotation: validate / verify / confirm / check out → pick "verify" and reuse (Rule 1.11)
- "check out" is also a phrasal verb → "hold"

---

## Test 3: Rewrite mode — broken paragraph logic

**Before:**

Our method uses a transformer encoder. We also add a contrastive loss. Previous methods struggle with long documents. The transformer has 12 layers. Our contrastive loss brings 2.3% improvement. The attention mechanism captures long-range dependencies.

**After (rewritten with proper paragraph structure):**

Previous methods struggle with long documents because their encoders cannot capture long-range dependencies. To address this, we use a 12-layer transformer encoder, whose attention mechanism captures dependencies across the full input length. We also add a contrastive loss, which brings a 2.3% improvement by aligning representations of similar documents.

**Logic fixed:**

- Motivation now comes before design.
- Each sentence connects to the previous one.
- Technical advantage is tied to each design choice.

---

## Test 4: Review mode — claim-evidence gap

**Text:**

Our method achieves state-of-the-art performance on document retrieval. We propose a novel sparse attention mechanism that significantly reduces computational cost while maintaining retrieval accuracy. Experiments on MS MARCO show that our method outperforms BM25 by 15% on MRR@10.

**Findings:**

| Category | Location | Issue | Suggestion | Severity |
|---|---|---|---|---|
| Claim-evidence | Abstract | "state-of-the-art" claim not supported: only BM25 baseline compared | Compare with recent neural retrievers (ColBERT, ANCE, SPLADE) | high |
| Language | Abstract | "significantly reduces" — no quantity given | State the actual FLOPs or latency reduction | medium |
| Terminology | Abstract | "novel" is a marketing adjective — cannot be measured | Describe what makes it structurally different | low |

---

## Test 5: Polish mode — protected content must not change

**Before:**

It is worth noting that the loss function $mathcal{L} = mathcal{L}_{	ext{CE}} + lambda mathcal{L}_{	ext{reg}}$ demonstrates superior convergence properties. Additionally, as shown in cite{vaswani2017attention}, the attention mechanism leverages multi-head computation.

**After:**

The loss function $mathcal{L} = mathcal{L}_{	ext{CE}} + lambda mathcal{L}_{	ext{reg}}$ converges faster. As shown in cite{vaswani2017attention}, the attention mechanism uses multi-head computation.

**Violations fixed:**

- "It is worth noting that" → deleted (hedge)
- "demonstrates superior convergence properties" → "converges faster" (nominalization + marketing)
- "Additionally" → deleted (connector not needed with short sentences)
- "leverages" → "uses" (short word)

**Protected content preserved:**

- Math formula: $mathcal{L} = mathcal{L}_{	ext{CE}} + lambda mathcal{L}_{	ext{reg}}$
- Citation: cite{vaswani2017attention}
- Technical term: "attention mechanism"

---

## Test 6: Polish mode — passive voice in academic context

**Before:**

The model was trained on the WikiText-103 dataset. The results were evaluated using perplexity. It is crucial to understand that the proposed method was inspired by the work of cite{dai2019transformer}.

**After:**

The model was trained on the WikiText-103 dataset. We evaluated the results using perplexity. The proposed method builds on cite{dai2019transformer}.

**Violations fixed:**

- "was trained" → kept (academic convention for experimental setup)
- "were evaluated" → "We evaluated" (actor is known, prefer active)
- "It is crucial to understand that" → deleted (hedge stack)
- "was inspired by" → "builds on" (active, more precise)
