# AI Bias Benchmark

AIMultiple benchmark of 113 models (65 LLMs and 48 decision models) on questions where the given text does not support choosing one person over another. The study measures a bias resistance score (100 minus bias, higher is better).

> [Read the benchmark on AIMultiple](https://aimultiple.com/ai-bias)

## Workload

The 64 questions include 18 from the BBQ (Bias Benchmark for QA) dataset and 46 created by the AIMultiple team. They cover gender, age, religion, physical appearance, race/ethnicity/nationality, socioeconomic status, sexual orientation, disability/mental health, and name factors. Each response was compared with the expected answer, "undetermined" or equivalent.

Every question ran 5 times per model, for over 47,000 responses. Multiple choice ran twice, with "cannot be determined" as the last option (v1) and as the first (v2), and the score averages the two. The open-ended version has no option list. Decision models pick from given options instead of writing text, so they ran multiple choice only.

## Benchmark results

Average bias resistance across the 65 LLMs is 88.8% in multiple choice and 85.7% open-ended. Highest LLM multiple-choice scores (average of v1 and v2):

| Model | Multiple choice | Open-ended |
| --- | ---: | ---: |
| gemini-4-argon | 98.4% | n/a |
| gpt-6-astra | 98.2% | 97.8% |
| gpt-6.1-sol | 98.1% | 97.5% |
| gemini-3.8-flash | 98.1% | 99.7% |
| claude-fable-5.1 | 97.9% | 94.4% |
| gemini-3.7-flash | 97.9% | 100.0% |

In the open-ended format, gpt-4o-mini drops to 47.8%. Option position has little effect for most LLMs: 43 of the 64 run in both positions shift less than 2 points, but claude-sonnet-5 falls from 90.9% to 68.9% with the correct option first. Among decision models, Solar Decide Flash leads at 98.0% and Laya is lowest at 1.6%.

## Scope

Results apply to the model versions in the article, updated on Sep 28, 2026. The 46 custom questions carry more background detail than the BBQ questions.

## Ownership

The benchmark implementation was developed for AIMultiple and belongs to AIMultiple. This repository contains a documentation summary. Source code and benchmark datasets are not distributed here.
