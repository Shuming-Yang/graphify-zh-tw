# Graph Report - graphify-out/graph.json  (2026-08-08)

## Corpus Check
- 0 files · ~0 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 177 nodes · 246 edges · 16 communities (14 shown, 2 thin omitted)
- Extraction: 83% EXTRACTED · 17% INFERRED · 0% AMBIGUOUS · INFERRED: 43 edges (avg confidence: 0.5)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- adder.py
- model.py
- train.py
- Layer
- bpe.py
- Value
- utils.py
- AdditionDataset
- setup.py

## God Nodes (most connected - your core abstractions)
1. `Value` - 15 edges
2. `GPT` - 9 edges
3. `Layer` - 8 edges
4. `Neuron` - 7 edges
5. `Encoder` - 7 edges
6. `CfgNode` - 7 edges
7. `AdditionDataset` - 7 edges
8. `CharDataset` - 7 edges
9. `Module` - 6 edges
10. `MLP` - 6 edges
11. `Trainer` - 6 edges
12. `Block` - 5 edges

## Surprising Connections (you probably didn't know these)
- `from_pretrained()` --calls--> `get_default_config()`  [INFERRED]
  /home/safi/graphify-benchmark/repos/nanoGPT/model.py → /home/safi/graphify-benchmark/repos/minGPT/mingpt/model.py

## Import Cycles
- None detected.

## Communities (16 total, 2 thin omitted)

### Community 0 - "adder.py"
Cohesion: 0.08
Nodes (18): batch_end_callback(), eval_split(), get_config(), get_default_config(), get_config(), get_default_config(), collections, mingpt_bpe (+10 more)

### Community 1 - "model.py"
Cohesion: 0.11
Nodes (12): dataclasses, inspect, Block, CausalSelfAttention, from_pretrained(), get_default_config(), GPT, GPTConfig (+4 more)

### Community 2 - "train.py"
Cohesion: 0.11
Nodes (14): contextlib, datasets, math, os, pickle, requests, tiktoken, time (+6 more)

### Community 3 - "Layer"
Cohesion: 0.13
Nodes (6): micrograd_engine, Layer, MLP, Module, Neuron, random

### Community 4 - "bpe.py"
Cohesion: 0.21
Nodes (7): BPETokenizer, bytes_to_unicode(), Encoder, get_encoder(), get_file(), get_pairs(), regex

### Community 6 - "utils.py"
Cohesion: 0.16
Nodes (6): ast, json, numpy, sys, CfgNode, setup_logging()

### Community 7 - "AdditionDataset"
Cohesion: 0.15
Nodes (3): AdditionDataset, CharDataset, Dataset

## Knowledge Gaps
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `AdditionDataset` connect `AdditionDataset` to `adder.py`?**
  _High betweenness centrality (0.053) - this node is a cross-community bridge._
- **Are the 4 inferred relationships involving `Value` (e.g. with `.__add__()` and `.__mul__()`) actually correct?**
  _`Value` has 4 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `Layer` (e.g. with `.__init__()` and `.__call__()`) actually correct?**
  _`Layer` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Should `adder.py` be split into smaller, more focused modules?**
  _Cohesion score 0.08333333333333333 - nodes in this community are weakly interconnected._
- **Should `model.py` be split into smaller, more focused modules?**
  _Cohesion score 0.10574712643678161 - nodes in this community are weakly interconnected._
- **Should `train.py` be split into smaller, more focused modules?**
  _Cohesion score 0.10869565217391304 - nodes in this community are weakly interconnected._
- **Should `Layer` be split into smaller, more focused modules?**
  _Cohesion score 0.13333333333333333 - nodes in this community are weakly interconnected._