---
name: '[LEARNING] Code A Robot'
about: A templated learning task to cover Robot programming skills. Simply assign yourself to the task and complete it by following the instructions.
title: '[LEARNING] Code A Robot'
labels: ''
assignees: ''
---

## 🎯 Description

This issue serves as a technical challenge and qualification assessment for students pursuing leadership roles in FRC 5804. It ensures you have the foundational skills to work independently with the robot codebase and support others during the build season.

You will go through a complete robot code deployment cycle, test and tune control loops, and demonstrate your ability to plan and execute autonomous paths using PathPlanner. This is not a guided tutorial — use existing team code and documentation to figure things out. Leadership candidates are expected to be resourceful and self-directed.

## 📂 Acceptance Criteria
- [ ] Complete a "zero-to-robot" exercise:
  - [ ] Set up a 5804-style robot project in WipiLib. Be sure to reference [Gary-ctre](https://github.com/5804/Gary-ctre), [Crescendo2025](https://github.com/5804/Crescendo2025), and [Reefscape](https://github.com/5804/Reefscape) as needed. The Wipilib docs are your friend, they are available [here](https://docs.wpilib.org/en/2021/docs/software/vscode-overview/creating-robot-program.html#creating-a-robot-program).
  - [ ] Generate a swerve configuration using [CTRE Swerve Generator](https://v6.docs.ctr-electronics.com/en/latest/docs/tuner/tuner-swerve/index.html).
- [ ] Tune a PID loop (drive or turning PID) and document your process (include before/after values and graphs if possible).
- [ ] Create a PathPlanner path and integrate it into your robot code.
  - [ ] Run a 1-meter forward test using PathPlanner.
  - [ ] Tune the odometry-related PIDs until the robot follows the path with moderate precision.
- [ ] Record and upload a 1-2 minute demo video OR provide screenshots + detailed documentation showing each step was completed successfully.
- [ ] Submit your final code in a GitHub repository within the [5804 GitHub org](https://github.com/5804), and link it in this issue.
  - [ ] Include a short README explaining what you did, what you struggled with, and what you'd do differently next time.

## 🔗 Additional References
- [Gary-ctre](https://github.com/5804/Gary-ctre) — Basic robot framework
- [Crescendo2025](https://github.com/5804/Crescendo2025) — competition robot using swerve + PathPlanner
- [Reefscape](https://github.com/5804/Reefscape) — Full-featured competition codebase
- [PathPlanner docs](https://github.com/mjansen4857/pathplanner/wiki)
- [Swerve Drive Specialties Setup](https://github.com/Swerve-Drive-Specialties/swerve-lib)

## 📓 Notes
- This is a **required task** for students seeking leadership positions in controls, software, or strategy.
- Don’t wait for help to begin — show your ability to independently reference codebases, docs, and other resources.
- Ask specific questions if stuck, but **document what you've tried first.**

## 🎈 Size
3
