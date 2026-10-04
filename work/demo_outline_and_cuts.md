# ML-12 — Demo outline + shareable cuts

## 5-minute demo outline
- **Question (30s):** Which pages should we refresh first? A content team can only refresh so many
  pages per cycle — the order of the queue decides how much declining search visibility gets recovered.
- **Method (1 min):** 30,000 anonymized pages. First a transparent rule baseline (no ML, fully explainable),
  then three classifiers — logistic regression, decision tree, random forest — compared against that
  baseline on the SAME client-holdout split, scored at precision@K.
- **One chart (1 min):** model comparison — random forest precision@20 0.85 vs baseline rule 0.10,
  base rate 0.39. The forest wins everywhere that matters for a queue.
- **One honest result (1 min):** the naive random split flattered the model (p@100 0.91); the honest
  client-holdout split says 0.73. And the label is a declining *proxy* — nothing here proves refreshing
  *causes* recovery. Decision-support, not proof.
- **One recommendation (1.5 min):** work the queue top-down; rewrite snippets first for page 2–5 movers;
  expand thin pages before refreshing; a human reviews every page before refresh effort is spent.

## Shareable cut 1 — social post (methodology)
Built a content refresh queue two ways: first a transparent rule (no ML at all), then three classifiers
on the same client-holdout split. Random forest hit precision@20 0.85 vs the rule's 0.10 — but here's
the honest part: a naive split inflated p@100 to 0.91, the honest split says 0.73. Baselines keep you honest.

## Shareable cut 2 — employer-facing summary (3 sentences)
I built a refresh-opportunity scoring system over 30,000 anonymized content pages for the FlyRank ML
internship. I compared a transparent rule baseline against three classifiers on a client-holdout split —
a random forest reached precision@20 of 0.85, with a full leakage audit and error analysis. The work
shipped as a deployed research paper with a ranked action playbook a content team can work top-down.
