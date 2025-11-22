
# AGENT BASED GENETIC ALGORITHM FOR CRYPTO TRADING STRATEGY OPTIMIZATION

This project implements an intelligent, agent driven genetic algorithm model designed to optimize crypto trading strategies. It combines market analysis, technical indicators, evolutionary optimization, and backtesting in a single automated workflow.

The system evolves trading parameters through genetic operations, evaluates their performance, and continuously refines them until the best strategy emerges.

# Overview

This script provides:

Multi agent decision making

Dynamic parameter generation

Fitness evaluation for trading strategies

Selection, crossover, and mutation

Automated backtesting

Real time optimization insights

It is built for traders, researchers, and developers experimenting with algorithmic trading and evolutionary algorithms.

# Features

# Core Components

Agent based architecture

Genetic algorithm operations:

Initial population generation

Fitness scoring

Elite selection

Crossover

Mutations

Configurable optimization parameters

Price data handling with indicators

Progress logging and parameter tracking

# Backtesting Engine

Buy or sell signal generation

Detailed trade log

Portfolio simulation

Performance summary

Strategy comparison

# File Structure

agent_based_genetic_algorithm.py


This file contains the complete implementation:

Agents

Utility functions

Strategy rules

Genetic algorithm cycles

Backtester

Main execution logic

# How It Works

The system initializes a population of strategy parameters

Each strategy is tested on market data

Fitness scores determine which ones survive

Top performers breed through crossover

Mutations maintain diversity

The process repeats for multiple generations

Best strategy is backtested and analyzed

# Requirements

Install the required Python libraries:

pip install numpy pandas yfinance matplotlib ta-lib


If TA-Lib fails to install, install the wheel manually.

# Running the Script

Run it directly in your terminal:

python agent_based_genetic_algorithm.py


The script will:

Download or load price data

Perform optimization

Backtest best strategy

Show charts and results

# Output Includes

RSI length optimization

Filter activation

Fitness performance

Trade count and profit stats

Equity curve plot

Optimization history

# Best Use Cases

This project is ideal for:

Crypto strategy research

Academic AI modeling

Automated trading development

Optimization experiments

GA based learning projects

