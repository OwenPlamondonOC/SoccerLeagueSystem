# Feature: Create Games
**Feature ID:** CG
**Branch pattern:** `feature/CG-create-games`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Games for Season
**As a** System Admin
**I want to** tell the system to automatically create games for a season
**So that** the season is populated with games based on team and location information
**Priority:** P1
**Independent test:** press the create games button and populate the games list of a season
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST create games based on team and location information
- **FR-002**: System MUST store information of games in a season

---
## Key Entities
- **User**: System Admin; maintains most data for the games and seasons
- **Database**: information storage; tracks information including seasons and their information

---
## Acceptance Criteria
### US-N.1 - Create Games for Season
#### Scenario: Admin creates games for a season with information
* **Given** I have entered information for locations and teams
* **When** I press the "Create Games" button
* **Then** The season's game list is automatically populated with a set of games
#### Scenario: Admin creates games for a season with not enough information
* **Given** I have not entered enough information to make a working season
* **When** I press the "Create Games" button
* **Then** I am informed that there is not enough information to make a working season and games are not created

---

## Screen Requirements

### [View: List Page] — route name `list`
*   Uses a `MenuBar` to quickly leave page.
*   A "Create Games" button to populate the list automatically
*   Displays list of games for a season
