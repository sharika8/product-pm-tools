# 🛠️ Product & PM Tools

Small standalone tools for product management workflows — built as self-contained HTML apps, powered by Claude.

---

## Tools

### 📊 Story to Diagram (`story-to-diagram.html`)
Paste a user story or requirements text, get back a Mermaid sequence diagram or flowchart. Extracts the actual actor and system names from your text rather than using generic placeholders.

- Sequence diagram or flowchart toggle
- View rendered diagram or raw Mermaid code
- Copy Mermaid code to clipboard

### ⚗️ A/B Test Planner (`ab-test-planner.html`)
Describe a feature idea, get back a structured A/B test plan — hypothesis, control/variant description, success metrics (primary/secondary/guardrail), duration estimate, ship/no-ship criteria, and risks to watch.

- Structured hypothesis in "If we X, then Y, because Z" format
- Primary, secondary, and guardrail metrics
- Ship / no-ship / extend decision criteria
- Copy full plan to clipboard

---

## Usage

Both tools are self-contained single-file HTML apps that call Claude via the `claude.use('sample')` runtime capability. They're built to run inside a Claude Artifact environment (e.g. published via claude.ai) rather than as plain static pages — opening them directly in a browser outside that environment won't trigger the AI generation feature, since the `claude` object isn't available there.

To use them:
1. Publish via Claude's Artifact feature (paste the HTML content into a new artifact), or
2. Adapt the `generate()` function to call an LLM API directly if hosting elsewhere (e.g. swap `claude.use('sample')` for a `fetch` call to your own backend)

---

## 📜 Licence
MIT
