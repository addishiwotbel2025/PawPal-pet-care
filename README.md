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

## My Contributions

I designed and implemented the scheduling system behind PawPal+, including priority-based planning, time-budget management, conflict detection, recurring tasks, and explainable scheduling decisions.

I also built the Streamlit interface and wrote automated tests covering core scheduling behavior and edge cases.
