# Monte Carlo Forecasting

A single-page web app for probabilistic delivery forecasting using Monte Carlo simulation. Built for agile teams who want data-driven answers to "when will it ship?" and "how much can we deliver?"

**Live app:** [pathways-nb.github.io/mc-forecasting](https://pathways-nb.github.io/mc-forecasting/)

## Tools

### Backlog Forecast
Forecast a single backlog or epic. Given scope and throughput, when will it be done?

### Portfolio Forecast
Forecast multiple features with shared or per-feature throughput. Supports WIP limits, weighted allocation, and portfolio-level confidence reporting.

### Capacity Forecast
How much can your team deliver in a given time window? Given throughput history and a planning horizon, get probabilistic item and feature counts.

### Product Forecast
Forecast a product delivered by multiple teams with inter-team dependencies. Uses topological sorting to simulate dependency chains and compares with/without dependency scenarios.

## Methodology

Based on the work of:
- **Troy Magennis** ([Focused Objective](https://focusedobjective.com)) — Size-Growth-Pace scope model, linear interpolation percentiles, empirical throughput sampling
- **Nick Brown** ([Real World Agility](https://realworldagility.com)) — Practical Monte Carlo forecasting for agile teams

Key principles:
- Throughput sampled from empirical data, not fitted distributions
- Scope modeled with low/high range and split rate multiplier (SGP model)
- Data quality measured with `(n-1)/(n+1)` formula
- Zero-throughput periods included for realism

## Tech

Single HTML file, no dependencies, no build step. Pure HTML/CSS/JavaScript with Canvas for charts.
