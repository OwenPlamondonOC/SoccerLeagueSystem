# Feature: Update Results
**Feature ID:** UR
**Branch pattern:** `feature/UR-update-results`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Update Results for a Game
**As a** Team Manager
**I want to** Input the results and stats of a game that has been played
**So that** the system is updated with the information and displays that information for the game
**Priority:** P1
**Independent test:** input results and stats of a game and see that information appear on the games list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST accept input from Team Managers for game data
- **FR-002**: System MUST store information of games in a season

---
## Key Entities
- **User**: Team Manager; inputs data involving game results and stats
- **Database**: information storage; tracks information including games and their results

---
## Acceptance Criteria
### US-N.1 - Update Results for a Game
#### Scenario: Manager adds results for a game that has happened
* **Given** The date and time for a game is in the past
* **When** I enter information for that game's results and stats
* **Then** The game's information in the database is updated to match the inputted data
#### Scenario: Manager adds results for a game that has yet to happen
* **Given** The date and time for a game is in the future
* **When** I enter information for that game's results and stats
* **Then** The game's information in the database is not updated to match the inputted data
* **And** the team manager is informed that the game has not happened yet

---

## Screen Requirements

### [View: Update Results] — route name `results`
*   Uses a `MenuBar` to quickly leave page.
*   Text fields for the results and statistics of the game
