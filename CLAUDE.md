# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A standalone Monte Carlo simulation visualization for sizing "niches" (storage compartments) in a Put Wall Sorter system ("Sistema Sure Sort X", 128 ports). The entire application is a single self-contained HTML file.

## Running the App

Open `graficas_montecarlo_con_video (2).html` directly in a browser — no build step, server, or dependencies to install. Chart.js is loaded from CDN.

## Architecture

- **Single file**: all logic, styles, and markup live in one HTML file
- **Simulation**: 5000 Monte Carlo iterations using a seeded PRNG with Box-Muller transform for normal-distributed random variables
- **Visualizations** (Chart.js v4.4.1):
  - Histogram of required niches per iteration
  - Convergence graph (running mean over iterations)
  - Bar chart of niches needed at each service level (80%–99%)
- **No backend, no framework, no build tooling**
