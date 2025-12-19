# IWSLT26 metrics shared task

This repository contains data and all the wrangling, baseline and evaluation scripts for [IWSLT26 Metrics Shared Task](https://iwslt.org/2026/metrics).

```bash
pip3 install -r requirements
```

## Baselines

We include several baselines. The format for a submission is a list of numbers with the same length as the input JSONL file.
```bash
mkdir data/output/
python3 baselines -i data/wmt25.jsonl -m asr_comet -o data/output/wmt25_comet.jsonl
python3 baselines -i data/wmt25.jsonl -m asr_comet_partial -o data/output/wmt25_comet_partial.jsonl
```

## Meta-evaluation

To evaluate the output of automated metrics, pass it in `-m` to the following script.

```bash
python3 evaluation -i data/wmt25.jsonl -m data/output/*.jsonl
```

The results for baselines (WMT25) are:
```
WIP
```