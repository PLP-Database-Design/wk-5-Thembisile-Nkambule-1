# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager |Prisca Wamboka | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | | Risk identification, prioritization, test design linkage |
| Test Executor | | Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly |High - can lead to data loss |
| Leaderboard | Stores top 3 scores in localStorage |Medium-incorrect ranking affects user trust but doesn’t break gameplay|
| Bonus Round | Every 3 puzzles → doubles score | Medum - logic error|

## Test Plan

### Objectives
- Functional Testing - Verify that the word scrambling mechanism functions correctly, the scoring system follows defined rules and the hint, reset button and leaderboard update as expected.
- User Interface Testing - Verify that all UI elements (buttons, input fields, score display etc.) are visible, aligned and responsive across different screen sizes.
- Game Principle Testing - Ensure random word selection is functioning correctly, scrambled words differ from original words and scoring (including bonus points) is applied accurately.
- User Experience Testing - Validate that the hint system is helpful and concise, the leaderboard is clearly displayed and the game provides immediate, understandable feedback for user actions.


### Scope

**In Scope:**
- Functional, UI and risk-based testing of new features.

**Out of Scope:**
- Performance and load testing.
- Cross-browser compatibility beyond Chrome
- Mobile responsiveness

### Tools & Resources

- Github projects and issues, Google chrome, Snipping tool (for screenshots), Vs code

### Schedule

| Phase      |  Planned Duration| Actual Duration | Status |  
|----|---------|-----------|----------------|
|Requirement analysis |1 day      |1 day        | completed|
|Test planning    |    1 day |    1 day   |   completed |
|Test design & development | 2 days|  2 days| completed|
|Test execution | 1 day| 1 day | completed|
|Test closure (reporting) | 1 day | 1 day |completed|




## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
|✅ TC-01 |Reset Game Functionality | | | | | |


### Risk Coverage

- Tested Risks Percent: 
- Untested Risks Percent: 

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
|TC-01 |Word Scrambling | Verify word scrambling functionality|Scrambled word ≠ original word; all letters present; length unchanged |Scrambled word differs from original; all letters present; length unchanged |Pass | |
|TC-02 | Scoring system|Validate score updates correctly for correct guesses|+10 points (no hint), +5 points (with hint)|scores increases by 10 point for  correct guess without hnt, and 5 points wth hint|Pass||
|TC-03 |Bonus Round|Confirm bonus activates after every 3 puzzles|Score doubles after every 3 correct guessess|Score is multiplied by 2 after every 3 correctly solved puzzles|Pass|
|TC-04 |Leaderboard |Verify top 3 scores persist |Top 3 scores remain visible after refresh|Top 3 scores persists after refresh|Pass||
|TC-05 |Reset Game |Ensure reset clears progress and score |Score resets to zero; first puzzle is displayed; progress is cleared|Reset clears score & progress|Pass||
|TC-06|Input Validation-Empty Input Submission|Prevent submission of empty input|“Please enter a guess”; no score change|The phrase "please enter a guess" is displayed|pass||
|TC-07|Input Validation-Non-Alphabetic Input|Prevent submission of invalid characters|Input should be rejected with a specific error message like “Only alphabet characters allowed”; score should not change|Message displayed: “Incorrect, try again!”|Pass||
|TC-08|UI Layout-Mobile Responsiveness|Verify layout adapts to mobile view|All elements visible, aligned, and functional on mobile|Layout adjusts|Pass||



## Metrics

- Test Case Pass Percent: 
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 

### Defect Summary

- Total Defects Logged: 
- Critical High: 
- Fix Rate: 

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| | | | | |

**Progress Tracking Method:**  
**Change Control Notes:**

## Lessons Learned

- Most Defect Prone Feature: 
- Risk Analysis Impact: 
- Team Communication Effectiveness: 
- Improvements for Next Cycle: 

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| | Test Manager | | |
| | Risk Analyst | | |
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
