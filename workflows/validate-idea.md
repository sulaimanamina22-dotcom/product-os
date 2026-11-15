# Workflow: Validate an Idea

**Trigger:** the user submits a raw idea, "I have an idea…", "should we build…", "is X worth doing", "run this through Agent 1."

---

## Steps

1. **Read memory.** Load `memory/principles.md`, the retained-project index and applicable project records. Continue existing work. Rejected histories are intentionally unavailable; do not infer a past verdict from the aggregate count. Use relevant conversation context when supplied.
2. **Run Agent 1** (`agents/idea-originator-validator.md`) through its four passes: Generate → Research → Attack → Judge. Research must compare relevant market/population size, existing solution count, actual adoption and awareness with sources and uncertainty. Compare compatible populations and metrics only. Examine first adoption, adding a solution and incumbent switching according to the customer's actual behavior. Apply `memory/principles.md` section 2a; competitor existence alone cannot establish saturation or failure.
   Record the entry approach, market trajectory, customer-language evidence and first acquisition hypothesis. Where a material uncertainty needs a live demand test, use `workflows/test-demand.md`; designing a test does not mean it ran or passed.
3. **Return one of two exits:**
   - **KILL**: which criterion failed, the strongest adverse fact or explicitly missing critical evidence, the relevant market/adoption findings and limits, and what would flip it to a yes. Distinguish withholding validation from demonstrated nonviability. No brief.
   - **PASS**: the full A-to-Z brief in the fixed schema, wrapped in the `=== HANDOFF → AGENT 2 ===` block.
4. **Save output (PASS only):** write the brief to `outputs/[YYYY-MM-DD]-[idea-slug]/brief.md`.
5. **Write back (always):**
   - On a fresh KILL: increment the aggregate decision count in `memory/projects.md` once; keep the explanation in the conversation without saving an idea dossier. Do not count a repeated explanation as a fresh verdict. Apply any explicit user-retained experiment exception.
   - On PASS: add a Passed ideas row and update the retained PASS total in `memory/projects.md`, create `memory/projects/[slug]/` from `_TEMPLATE`, seed decisions/state/questions, and save the brief to `outputs/[YYYY-MM-DD]-[slug]/brief.md`.
6. **Respect the requested scope.** An assessment-only request ends at its verdict/brief. A PASS does not itself authorize a product build, but an existing explicit build authorization carries forward without another intake pause. A demand-test follow-up uses the shared workflow: Agent 1 owns evidence/verdicts, Agent 2 owns design/build/protection, and Agent 3 owns positioning/acquisition/measurement. Do not repeat completed research or change the verdict merely because specialist test assets were created.
