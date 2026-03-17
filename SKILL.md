# Smart To-Do Organizer Skill

This skill provides guidance and tooling for developing the **Smart To-Do Organizer** project, which automatically prioritizes tasks based on deadlines, user habits, and other context.

## Purpose

- Help developers and contributors understand the project goals and requirements.
- Provide a reference for task prioritization rules and data models.
- Serve as a quick-start guide for building the app and implementing core features (tasks, habits, scheduling, priorities, notifications).

## Usage

- Use this document when planning features, writing code, or adding tests.
- Refer to the requirements in `requirements.txt` for behavior expectations.
- Keep the priority scoring logic and data model in sync with this document.

## Key Concepts

### Task
- Title, description, due date/time, duration, tags/categories
- Status: pending, in_progress, completed, snoozed
- Priority score computed from deadline proximity, habit streaks, and user overrides

### Habit
- Recurring tasks (daily/weekly/custom) with streak tracking
- Used to influence priority when a streak is close to breaking

### Priority Engine
- Produces a daily focus list (top N tasks)
- Prioritizes:
  - Tasks due soon
  - Tasks needed to maintain habits/streaks
  - User-specified priority overrides
  - Estimated task duration (fill gaps)

## Recommended Next Steps

1. Implement core task CRUD and persistence.
2. Add habit tracking and streak calculation.
3. Build the priority engine (score & sort tasks).
4. Add UI for daily focus list + notifications.

---

> Note: This file is intended for contributors to quickly understand the project's intent and should be kept aligned with `requirements.txt`.
