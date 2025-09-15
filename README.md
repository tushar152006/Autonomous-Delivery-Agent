# Autonomous-Delivery-Agent
Implementation of autonomous delivery agent using BFS/UCS, A*, and simulated annealing for dynamic grid navigation
# CSA2001: Autonomous Delivery Agent

## Overview
This project implements a rational autonomous delivery agent navigating a 2D grid with static/dynamic obstacles and varying terrain costs. Uses UCS, A*, and simulated annealing for pathfinding.

## Environment Model
- 2D grid with costs ≥1 (0=obstacle).
- 4-connected movement (up/down/left/right).
- Dynamic obstacles simulated via replanning (unpredictable appearance).

## Installation & Dependencies
- Python 3.8+ (tested on 3.12).
- No external deps: `pip install -r requirements.txt` (empty file).
- Reproducibility: `random.seed(42)` in code.

## Running the Planners
1. Clone repo: `git clone https://github.com/yourusername/CSA2001-Autonomous-Delivery-Agent.git`
2. Run CLI: `python agent.py`
- Outputs: Path cost, length, nodes expanded, time for each map/planner.
- Maps: small_map.txt, medium_map.txt, large_map.txt, dynamic_map.txt.

## Tests & Reproducibility
- Built-in: Code validates paths (adjacency, no obstacles).
- Dynamic POC: Run shows initial A* path, obstacle block at step 3, SA replan log.
- Seed: 42 ensures same random obstacles/paths.

## Report & Demo
- See `report.pdf` for model, design, heuristics, results (tables/plots), analysis.
- Demo: `demo_screenshots/` folder with sequence (initial plan → block → replan).

## Grid File Format
First line: `rows cols start_r start_c goal_r goal_c`
Subsequent lines: Space-separated costs per row.

