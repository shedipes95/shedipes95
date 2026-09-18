# Sepideh Saadaei Jahromi

I build and evaluate machine-learning systems, with most of my attention on the
part people skip: proving the model does what it claims to do.

Finishing an MSc in Human-Centred AI at TU Dublin, on top of an earlier MSc in
Financial and Risk Management Engineering. The finance background is why I work
this way. In risk, a model that is confidently wrong is worse than no model, and
you are expected to show your working — where the number came from, what it
assumes, and where it breaks. I have never seen a reason to hold ML to a lower
standard.

## What I work on

- **LLM evaluation** — measuring whether generated text is actually grounded in
  its source, at the level of individual claims, and validating the detector
  against human labels instead of trusting its own score.
- **Model explainability** — SHAP at both the global and the single-decision
  level, including what the explanations reveal that you would rather they did not.
- **Evaluation under class imbalance** — the 8%-positive problems where accuracy
  is a distraction and the interesting question is what a threshold costs.
- **AI governance** — my dissertation turns EU AI Act requirements into
  measurements you can actually run, for SMEs using LLMs in recruitment.

## Two projects worth your time

**[groundcheck](https://github.com/shedipes95/groundcheck)** — an installable
tool that audits whether an LLM's output is grounded in the document it was
given. It breaks the output into atomic claims, checks each against the source,
and reports a three-way verdict: supported, contradicted, or never mentioned.

What makes it different is the part most tools leave out — it measures its own
agreement with a human annotator using Cohen's κ. The worked example in the
README shows a detector at 78.9% raw agreement and κ = 0.483, with a confusion
matrix that reveals it never produced a single "contradicted" label. It could not
detect the failure mode that matters most, and its score looked fine anyway.
Also ships cost estimation before any paid run, resumable output, deterministic
sampling, tests with the API mocked, and CI.

**[credit-default-nn-shap](https://github.com/shedipes95/credit-default-nn-shap)**
— a Keras network predicting loan default on 307,511 Home Credit applications,
8.07% of them positive. Nine-run hyperparameter sweep, evaluation built around
recall and average precision rather than accuracy, and SHAP explanations for the
most confident correct and incorrect predictions.

The honest findings are in the README: the whole sweep spans 0.0035 ROC-AUC, so
the architecture barely mattered; the model catches 73% of real defaults by
wrongly flagging 5,431 people who would have repaid; and a gender variable came
out as the second most important feature in the model, which is written up as
the fairness problem it is rather than left out.

## Tools

Python and SQL. TensorFlow/Keras and scikit-learn for modelling, SHAP for
explainability, the OpenAI API and Hugging Face transformers for the LLM and NLI
work. pytest and GitHub Actions, because an evaluation tool nobody else can
re-run is an anecdote. pandas, NumPy and matplotlib for everything in between.

## Also here

[credit-scoring-fairness](https://github.com/shedipes95/credit-scoring-fairness) —
credit-risk model on German Credit with SHAP and a fairness audit across sex and age.
[sql-finance-analytics](https://github.com/shedipes95/sql-finance-analytics) —
analytical SQL on a retail-bank schema: CTEs, window functions, business questions.
[market-risk-returns](https://github.com/shedipes95/market-risk-returns) —
Sharpe, volatility, correlation and drawdown across a multi-asset basket.

Based in Dublin. Open to AI/ML engineering and LLM evaluation roles, in Ireland
or remote.

[LinkedIn](https://linkedin.com/in/sepidehsj) · [shedipes95@gmail.com](mailto:shedipes95@gmail.com)
