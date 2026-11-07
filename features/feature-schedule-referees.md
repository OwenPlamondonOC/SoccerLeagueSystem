# Feature: Schedule Referees
**Feature ID:** SR
**Branch pattern:** `feature/SR-schedule-referees`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Contact Referees
**As a** System Admin
**I want to** notify referees that a game is happening
**So that** the system schedules available referees for that game
**Priority:** P1
**Independent test:** contact a test referee and simulate a response
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Accept or Deny Assignment
**As a** Referee
**I want to** respond whether I can referee for a game or not
**So that** the system either schedules me or moves on to find another referee
**Priority:** P1
**Independent test:** contact a test referee and simulate a response
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST accept input from System Admins and Referees
- **FR-002**: System MUST store information of referees and games, as well as which referees are scheduled for which games

---
## Key Entities
- **User**: System Admin; manages most league data
- **User**: Referee; accepts or denies assignments to games
- **System**: Automatically contacts referees and processes their responses
- **Database**: information storage; tracks information including games and their referees

---
## Acceptance Criteria
### US-N.1 - Contact Referees
#### Scenario: Admin notifies referees that there is a game
* **Given** The game does not already have referees assigned to it
* **When** I tell the system to search for referees
* **Then** The system contacts referees in the system

### US-N.2 - Accept or Deny Assignment
#### Scenario: Referee accepts game assignment
* **Given** The system admin searches for referees
* **And** I recieve an assignment
* **When** I respond to accept the assignment
* **Then** The system updates the game's information to include me as a referee
#### Scenario: Referee rejects game assignment
* **Given** The system admin searches for referees
* **And** I recieve an assignment
* **When** I respond to reject the assignment
* **Then** The system does not update the game's information to include me as a referee
* **And** The system goes on to contact another referee

---

## Screen Requirements

### [View: Scheduled Game Info] — route name `game`
*   Uses a `MenuBar` to quickly leave page.
*   Has a button to search for referees
*   Displays location, time, date, teams, and referees for the scheduled game

### [View: Assignment Screen] — route name `assignment`
*   Displays location, time, date, and teams for a scheduled game
*   Options to either accept or reject the referee assignment
*   Accessible through a link sent to referee's email / phone
