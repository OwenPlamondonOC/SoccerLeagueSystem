# Feature: Maintain Game
**Feature ID:** MG
**Branch pattern:** `feature/MG-maintain-game`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Game
**As a** System Admin
**I want to** input the information of a new game
**So that** the game is created in a season
**Priority:** P1
**Independent test:** add a new game and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Game
**As a** System Admin
**I want to** select an existing game for removal
**So that** the season removes this game's information
**Priority:** P1
**Independent test:** remove a game and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Game
**As a** System Admin
**I want to** input new information for an existing game
**So that** the information for that game is updated in the season
**Priority:** P1
**Independent test:** edit an existing game in the season and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit games
- **FR-002**: System MUST store information of games in a season

---
## Key Entities
- **User**: System Admin; maintains most data for the games
- **Database**: information storage; tracks information including games and their information

---
## Acceptance Criteria
### US-N.1 - Add Game
#### Scenario: Admin adds a new game to the season
* **Given** I am prompted to enter information for the new game
* **When** I enter the game's information
* **And** The game does not already exist in the season
* **Then** The game's information is added to the season
#### Scenario: Manager attempts to add an existing game to the season
* **Given** I am prompted to enter information for the new game
* **When** I enter the game's information
* **And** The game already exists in the season
* **Then** I am informed that the game already exists and am prompted to either edit the game's information or cancel the operation

### US-N.2 - Remove Game
#### Scenario: Manager removes an existing game from the season
* **Given** There is an existing game in the season
* **When** I select the game I wish to delete
* **Then** The game's information is removed from the season

### US-N.3 - Edit Game
#### Scenario: Manager changes an existing game's information
* **Given** There is an existing game in the season
* **When** I select the game I wish to edit
* **And** I enter new information for the game 
* **Then** The game's information is changed the season

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays game information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the game.
*   Primary action: **Edit Game**.
*   Buttons to save or cancel editing of game
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the game.
*   Primary action: **Add Game**.
*   Buttons to save or cancel addition of game
*   Verify pressing of save or cancel button