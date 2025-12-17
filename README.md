# 25-Day AI Agents Course by Google

A hands-on learning journey through Google's AI Agents capabilities.

> **Official Course**: [Advent of Agents 2025](https://adventofagents.com/) - 25 days of Zero to Production-Ready AI Agents on Google Cloud

## About This Course

This is Google Cloud's **Advent of Agents 2025** program - a 25-day journey to master AI Agents using:
- **Gemini 3** - Google's latest AI models
- **Agent Development Kit (ADK)** - Comprehensive agent development platform
- **Agent Engine** - Production deployment infrastructure

### Course Highlights
- 🎯 One feature per day, each taking less than 5 minutes to try
- 📋 Copy-paste commands that work out of the box
- 📚 Links to official documentation
- 🆓 100% free

### Difficulty Curve

<p align="center">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 320" width="600">
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
      <polygon points="0 0, 10 3.5, 0 7" fill="#333"/>
    </marker>
  </defs>
  <rect width="600" height="320" fill="none"/>
  <text x="300" y="30" text-anchor="middle" font-family="system-ui, sans-serif" font-size="18" font-weight="bold" fill="#333">25天课程难度曲线</text>
  <line x1="60" y1="280" x2="60" y2="50" stroke="#333" stroke-width="2" marker-end="url(#arrowhead)"/>
  <text x="45" y="55" text-anchor="middle" font-family="system-ui, sans-serif" font-size="12" fill="#333">难度</text>
  <line x1="60" y1="280" x2="570" y2="280" stroke="#333" stroke-width="2" marker-end="url(#arrowhead)"/>
  <text x="560" y="300" text-anchor="end" font-family="system-ui, sans-serif" font-size="12" fill="#333">天数</text>
  <rect x="80" y="220" width="100" height="50" rx="6" fill="#2d5a3d"/>
  <text x="130" y="240" text-anchor="middle" font-family="system-ui, sans-serif" font-size="11" font-weight="bold" fill="white">Day 1-5</text>
  <text x="130" y="256" text-anchor="middle" font-family="system-ui, sans-serif" font-size="10" fill="white">基础 + 部署</text>
  <rect x="200" y="165" width="100" height="50" rx="6" fill="#3d6a4d"/>
  <text x="250" y="185" text-anchor="middle" font-family="system-ui, sans-serif" font-size="11" font-weight="bold" fill="white">Day 8-13</text>
  <text x="250" y="201" text-anchor="middle" font-family="system-ui, sans-serif" font-size="10" fill="white">高级特性</text>
  <rect x="320" y="110" width="100" height="50" rx="6" fill="#4d7a5d"/>
  <text x="370" y="130" text-anchor="middle" font-family="system-ui, sans-serif" font-size="11" font-weight="bold" fill="white">Day 14-15</text>
  <text x="370" y="146" text-anchor="middle" font-family="system-ui, sans-serif" font-size="10" fill="white">多Agent协作</text>
  <rect x="440" y="60" width="110" height="50" rx="6" fill="#5d8a6d"/>
  <text x="495" y="80" text-anchor="middle" font-family="system-ui, sans-serif" font-size="11" font-weight="bold" fill="white">Day 16+</text>
  <text x="495" y="96" text-anchor="middle" font-family="system-ui, sans-serif" font-size="10" fill="white">LangGraph + A2A</text>
  <path d="M180 245 Q190 220 200 190" stroke="#666" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  <path d="M300 190 Q310 165 320 135" stroke="#666" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  <path d="M420 135 Q430 110 440 85" stroke="#666" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
</svg>
</p>

## Setup

### Prerequisites

- Python 3.11+
- [uv](https://github.com/astral-sh/uv) package manager

### Installation

```bash
# Install dependencies
uv sync

# Create .env file and add your API key
cp .env.example .env
# Edit .env and add your GOOGLE_API_KEY
```

## Project Structure

```
.
├── day-01/                 # Day 1: Introduction
├── day-02/                 # Day 2: ...
├── ...
├── shared/                 # Shared utilities
│   ├── __init__.py
│   └── config.py          # Configuration helpers
├── pyproject.toml         # Project dependencies
└── README.md
```

## Daily Progress

| Day | Topic | Status |
|-----|-------|--------|
| 01 | Introduction to AI Agents | 🚧 In Progress |
| 02 | TBD | ⏳ Pending |
| ... | ... | ... |

## Running Daily Exercises

```bash
# Run day 1 exercises
uv run python day-01/main.py

# Run with dev dependencies (for testing)
uv sync --dev
uv run pytest
```

## Resources

- [Advent of Agents 2025](https://adventofagents.com/) - Official course website
- [Google AI Studio](https://aistudio.google.com/)
- [Gemini API Documentation](https://ai.google.dev/docs)
- [Agent Development Kit (ADK)](https://google.github.io/adk-docs/)
