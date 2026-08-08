# Graph Report - .  (2026-08-08)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 22 nodes · 38 edges · 4 communities (3 shown, 1 thin omitted)
- Extraction: 50% EXTRACTED · 50% INFERRED · 0% AMBIGUOUS · INFERRED: 19 edges (avg confidence: 0.5)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- cluster.py
- _surprise_score
- analyze.py
- build.py

## God Nodes (most connected - your core abstractions)
1. `_cross_file_surprises()` - 7 edges
2. `_is_file_node()` - 5 edges
3. `_cross_community_surprises()` - 5 edges
4. `_node_community_map()` - 4 edges
5. `_is_concept_node()` - 4 edges
6. `_surprise_score()` - 4 edges
7. `suggest_questions()` - 4 edges
8. `god_nodes()` - 3 edges
9. `surprising_connections()` - 3 edges
10. `_file_category()` - 2 edges

## Surprising Connections (you probably didn't know these)
- `_surprise_score()` --calls--> `_cross_file_surprises()`  [INFERRED]
  worked/mixed-corpus/raw/analyze.py → worked/mixed-corpus/raw/analyze.py  _Bridges community 1 → community 2_

## Import Cycles
- None detected.

## Communities (4 total, 1 thin omitted)

### Community 0 - "cluster.py"
Cohesion: 0.47
Nodes (4): cluster(), cohesion_score(), score_all(), _split_community()

### Community 1 - "_surprise_score"
Cohesion: 0.67
Nodes (3): _file_category(), _surprise_score(), _top_level_dir()

### Community 2 - "analyze.py"
Cohesion: 0.49
Nodes (8): _cross_community_surprises(), _cross_file_surprises(), god_nodes(), _is_concept_node(), _is_file_node(), _node_community_map(), suggest_questions(), surprising_connections()

## Knowledge Gaps
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `_cross_file_surprises()` connect `analyze.py` to `_surprise_score`?**
  _High betweenness centrality (0.024) - this node is a cross-community bridge._
- **Why does `_surprise_score()` connect `_surprise_score` to `analyze.py`?**
  _High betweenness centrality (0.007) - this node is a cross-community bridge._
- **Are the 6 inferred relationships involving `_cross_file_surprises()` (e.g. with `_cross_community_surprises()` and `_is_concept_node()`) actually correct?**
  _`_cross_file_surprises()` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 4 inferred relationships involving `_is_file_node()` (e.g. with `_cross_community_surprises()` and `_cross_file_surprises()`) actually correct?**
  _`_is_file_node()` has 4 INFERRED edges - model-reasoned connections that need verification._
- **Are the 4 inferred relationships involving `_cross_community_surprises()` (e.g. with `_cross_file_surprises()` and `_is_file_node()`) actually correct?**
  _`_cross_community_surprises()` has 4 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `_node_community_map()` (e.g. with `_cross_community_surprises()` and `_cross_file_surprises()`) actually correct?**
  _`_node_community_map()` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `_is_concept_node()` (e.g. with `god_nodes()` and `_cross_file_surprises()`) actually correct?**
  _`_is_concept_node()` has 3 INFERRED edges - model-reasoned connections that need verification._