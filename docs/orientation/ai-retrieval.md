# Designing for AI Retrieval

Well-structured content is not just readable — it is retrievable. This is the discipline of
writing so an AI agent surfaces the right answer without hallucinating.

## Principles

1. **Single source of truth.** Every fact lives in exactly one canonical place, so retrieval
   never returns conflicting answers.
2. **Atomic, reusable blocks.** Long articles are broken into short, self-contained units
   (a definition, a step, a policy clause) that can be recombined per query.
3. **Metadata and retrieval tags.** Each block is tagged by intent, product, and scope so the
   model pulls the correct block for the correct context.
4. **Consistent terminology.** One term per concept, everywhere. Synonyms fragment retrieval.
5. **Complete context per entry point.** A retrieved block must stand on its own, because the
   user may never see the page around it.

## Applied result

I built an intent-based content architecture with metadata, retrieval tags, and eight canonical
content warehouses that an AI support agent could retrieve without hallucination. It independently
resolved **more than 177,000 customer interactions at a 26% self-serve rate** and cut contact
rate from **18% to 11%**.
