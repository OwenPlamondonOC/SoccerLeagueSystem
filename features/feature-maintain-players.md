# Feature: Maintain Player
**Feature ID:** MP
**Branch pattern:** `feature/MP-maintain-player`
**Status:** Draft
**Created:** 2026-11-07

---
## User Stories
### US-N.1: Create Player
**As a** System Admin
**I want to** input the information of a new player
**So that** the player is created in a team
**Priority:** P1
**Independent test:** add a new player and display it on a list
**Acceptance scenarios:** see ### US-N.1 under Acceptance Criteria

### US-N.2: Remove Player
**As a** System Admin
**I want to** select an existing player for removal
**So that** the team removes this player's information
**Priority:** P1
**Independent test:** remove a player and see that it no longer exists on the list
**Acceptance scenarios:** see ### US-N.2 under Acceptance Criteria

### US-N.3: Edit Player
**As a** System Admin
**I want to** input new information for an existing player
**So that** the information for that player is updated in the team
**Priority:** P1
**Independent test:** edit an existing player in the team and have the new information updated on the list
**Acceptance scenarios:** see ### US-N.3 under Acceptance Criteria

---
## Requirements
### Functional Requirements
- **FR-001**: System MUST allow users to add, remove, and edit players
- **FR-002**: System MUST store information of players in a team

---
## Key Entities
- **User**: System Admin; maintains most data for the players
- **Database**: information storage; tracks information including players and their information

---
## Acceptance Criteria
### US-N.1 - Add Player
#### Scenario: Admin adds a new player to the team
* **Given** I am prompted to enter information for the new player
* **When** I enter the player's information
* **And** The player does not already exist in the team
* **Then** The player's information is added to the team
#### Scenario: Manager attempts to add an existing player to the team
* **Given** I am prompted to enter information for the new player
* **When** I enter the player's information
* **And** The player already exists in the team
* **Then** I am informed that the player already exists and am prompted to either edit the player's information or cancel the operation

### US-N.2 - Remove Player
#### Scenario: Manager removes an existing player from the team
* **Given** There is an existing player in the team
* **When** I select the player I wish to delete
* **Then** The player's information is removed from the team

### US-N.3 - Edit Player
#### Scenario: Manager changes an existing player's information
* **Given** There is an existing player in the team
* **When** I select the player I wish to edit
* **And** I enter new information for the player 
* **Then** The player's information is changed the team

---

## Screen Requirements

### [View: Read Page] — route name `read`
*   Uses a `MenuBar` to quickly leave page.
*   No text fields
*   Displays player information

### [View: Edit Page] — route name `edit`
*   Fields: fields for all data of the player.
*   Primary action: **Edit Player**.
*   Buttons to save or cancel editing of player
*   Verify pressing of save or cancel button

### [View: Add Page] — route name `add`
*   Fields: fields for all data of the player.
*   Primary action: **Add Player**.
*   Buttons to save or cancel addition of player
*   Verify pressing of save or cancel button