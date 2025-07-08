---
name: '[LEARNING] Researching Robot Code'
about: A templated task covering what to look for when researching another team's robot code. Assign yourself to the task and complete it as instructed below.
title: '[LEARNING] Researching Robot Code'
labels: ''
assignees: ''
---

## 🎯 Description

There are a lot of FRC teams out there who do code really well. We should learn from them! Many codebases are open source so we can read through how other teams code their robots, watch for patterns and standard conventions, and use what we find to write our code even better!

When reading through a teams's codebase, look for answers to the following quesitons:
 - Does this code use a state machine or follow the standard FRC command based flow?
 - Are they using a swerve starter codebase? YAGSL? CTRE? Something else?
 - What naming conventions does the team use? Are the variables in a constants file?
 - How does the team break up their subsystems?
 - Where does the team write most of their commands? In the commands folder? In RobotContainer? In a subsystem?
 - How do teams write commands that require more than one subsystem?
 - How big is the RobotContainer.java file? What goes in there?
 - What are they using for Autonomous? PathPlanner? Choreo? Both?
 - What naming convention do they use for autonomous paths?
 - Do they break their paths down into multiple connected paths or do they have one big path per path?

## 📂 Acceptance Criteria
- [ ] Choose a team that you were impressed by and search for their code on github
- [ ] Create an issue called "[LEARNING] {yourFullNameInCamelCase} - Researching FIRST Team {teamNumber}, {Team Name's} Code" in the [TaskTracking repo](https://github.com/5804/TaskTracking/tree/main). For example: "[LEARNING] gavinAlberghini - Researching FIRST Team 2890, The Hawk Collective's Code".
  - [ ] Assign the created ticket to @5804/mentors
  - [ ] In the body of the issue, answer the questions above. Include links to files to show answers to each of the questions where possible
  - [ ] Create the issue and move it to the "In Review" column of the [TaskTracking repo's project board](https://github.com/orgs/5804/projects/1). 

## 🔗 Additional References
Here are some teams that stood out with and links to their codebases!
 - [3005](https://github.com/frc3005) RoboChargers
 - [340](https://github.com/greater-rochester-robotics) G.R.R.
 - [1706](https://github.com/rr1706) Ratchet Rockers Robotics
 - [7457](https://github.com/suPURDUEper) suPERDUper
 - [1731](https://github.com/team1731/FRC2025) Fresta Valley
 - [4118](https://github.com/FRC-Riptide-4118) Riptide
 - [180](https://github.com/frc180) S.P.A.M.
 - [3015](https://github.com/3015rangerrobotics) Ranger Robotics
 - [2767](https://github.com/strykeforce) Stryke Force
 - [1690](https://github.com/team1690) Orbit
 - [604](https://github.com/frc604) Quixilver
 - [1629](https://github.com/gaco1629) GaCo
 - [442](https://github.com/team422) Mech Tech Dragons
 - [449](https://github.com/blair-robot-project) Blair Robot Project
 - [8592](https://github.com/frc8592) Newton Squared
 - [836](https://gitlab.com/growingstems/frc-836-the-robobees) The RoboBees
 - [1727](https://github.com/frc-team-1727) REX
 - [9072](https://github.com/team9072) TigerBots
 - [2106](https://github.com/WindingMotor/SwerveDrive2025) Junkyard Dogs

## 📓 Notes
- The goal of this work is to inform our codebase for next year so the more research you do the better shape our code will be in for next year! Good luck!

## 🎈 Size
2
