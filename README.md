# PawPal+ 🐾

PawPal+ is a pet care planning assistant that turns everyday care tasks into personalized schedules based on priority, available time, conflicts, and recurring routines.

🚀 [Try PawPal+ Live](https://pawpal-pet-care-addishiwot-dagnew-2026.streamlit.app)

## Why I Built This

I wanted to explore how scheduling algorithms could solve a practical, everyday problem. PawPal+ started as a way to think about how software can balance competing priorities, limited time, and changing routines while still making its decisions understandable to the user.

## Key Features

- **Priority-based scheduling** that plans the most important care tasks first
- **Time-budget planning** that works within the owner's available time
- **Conflict detection** that identifies overlapping tasks and prioritizes accordingly
- **Recurring tasks** for daily and weekly care routines
- **Multi-pet support** for organizing tasks across pets
- **Explainable decisions** that tell the user why a task was scheduled or left out

## How It Works

PawPal+ takes the owner's available time and a list of care tasks, then builds a daily plan.

Tasks are evaluated based on priority, duration, timing, and recurrence. The scheduler checks for conflicts and available time before deciding what to include. When a task cannot be scheduled, PawPal+ explains the decision to the user.

This approach lets the application balance multiple constraints while keeping its scheduling decisions transparent.

## Tech Stack

**Language:** Python  
**Interface:** Streamlit  
**Testing:** Pytest

## 🧪 Testing PawPal+

Run the automated test suite from the project root:

```bash
python -m pytest
```
## Project Structure

```text
PawPal-pet-care/
├── app.py              # Streamlit interface
├── main.py             # Command-line demo
├── pawpal_system.py    # Core scheduling logic
├── tests/              # Automated tests
└── requirements.txt    # Project dependencies


# PawPal+ 🐾

**PawPal+** is a pet care planning assistant. It helps a busy pet owner stay consistent
with care by turning a list of tasks — walks, feeding, meds, grooming, enrichment — into
a clear daily plan that respects the time they actually have, and explains every choice.

It runs as an interactive **Streamlit app** and as a small **command-line demo**.

## ✨ Features

- **Priority sorting** — orders tasks HIGH → MEDIUM → LOW so the most important care is
  planned first (`Scheduler.sort_by_priority`).
- **Sorting by time** — orders tasks chronologically by start time, with flexible
  (no fixed time) tasks placed last (`Scheduler.sort_by_time`).
- **Time-budget planning** — fits tasks into the owner's available minutes, highest
  priority first, and drops what doesn't fit (`Scheduler.build_plan`).
- **Conflict warnings** — detects tasks whose fixed times overlap and warns the owner;
  the schedule keeps the higher-priority task and drops the clash
  (`Scheduler.conflicts`, `Scheduler.find_conflicts`).
- **Filtering by status** — completed tasks are skipped when building a new plan
  (`Scheduler.pending`).
- **Filtering by pet** — narrows tasks to a single pet for multi-pet households
  (`Scheduler.for_pet`).
- **Recurring tasks** — once / daily / weekly recurrence; completing a recurring task
  automatically queues its next occurrence (`Task.frequency`, `Task.next_occurrence`,
  `Pet.complete_task`, `Scheduler.tasks_for_day`).
- **Explainable plans** — every scheduled or dropped task comes with a plain-English
  reason (`Plan.explain`).

## Getting started

### Setup

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### Suggested workflow

1. Read the scenario carefully and identify requirements and edge cases.
2. Draft a UML diagram (classes, attributes, methods, relationships).
3. Convert UML into Python class stubs (no logic yet).
4. Implement scheduling logic in small increments.
5. Add tests to verify key behaviors.
6. Connect your logic to the Streamlit UI in `app.py`.
7. Refine UML so it matches what you actually built.

## 🧪 Testing PawPal+

Run the automated test suite from the project root:

```bash
python -m pytest
```
## Project Structure

```text
PawPal-pet-care/
├── app.py              # Streamlit interface
├── main.py             # Command-line demo
├── pawpal_system.py    # Core scheduling logic
├── tests/              # Automated tests
└── requirements.txt    # Project dependencies
