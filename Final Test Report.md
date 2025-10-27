# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Prisca Wamboka | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Ivy Nagide| Risk identification, prioritization, test design linkage |
| Test Executor | Thembisile Nkambule | Execution, evidence capture, defect logging |

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
- Reset game logic and score clearing.
- Leaderboard storage, sorting, and persistence.
- Bonus round score-doubling mechanism.
- Word scrambling, guessing, and hint system.
- Score calculation and progression tracking.

**Out of Scope:**
- Performance and load testing.
- Cross-browser compatibility beyond Chrome
- Mobile responsiveness

### Tools & Resources
- Roles- Test Manager,  Risk Analyst, Test Executor.
- Tools- Github projects and issues, Google chrome, Snipping tool (for screenshots), Vs code

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
|001|Word Scrambling Algorithm|Failure to work properly | Medium|High | High| additional validation to ensure scrambled word is different from original |
|002|Reset function|Failure to clear score|High |High |High |Validate that clicking rest button clears the score but not the leaderboard|
|003|Score calculation| Score calculation errors|Medium |High |High | Add score validation checks|
|004|Browser compatibility| Unable to launch on other browsers|Low|Medium |Medium | Cross-browser testing, use widely supported features|
|005|Bowser refresh| Game state loss during browser refresh| Medium|High |Medium| Implement session storage backup, auto-save feature


### Risk Coverage

- Tested Risks Percent: 100%
- Untested Risks Percent: 0%

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
|TC-01 |Word Scrambling | Verify word scrambling functionality|Scrambled word ≠ original word; all letters present; length unchanged |Not all words are scrambled |Failed | |
|TC-02 |Scoring system|Validate score updates correctly for correct guesses|+10 points (no hint), +5 points (with hint)|scores increases by 10 point for  correct guess without hnt, and 5 points wth hint|Pass||
|TC-03 |Bonus Round|Confirm bonus activates after every 3 puzzles|Score doubles after every 3 correct guessess|Score is multiplied by 2 after every 3 correctly solved puzzles|Pass|
|TC-04 |Leaderboard |Verify top 3 scores persist |Top 3 scores remain visible after refresh|Top 3 scores persists after refresh|Pass||
|TC-05 |Reset Game |Ensure reset clears progress and score |Score resets to zero; first puzzle is displayed; progress is cleared|Reset clears score & progress|Pass||
|TC-06|Input Validation-Empty Input Submission|Prevent submission of empty input|“Please enter a guess”; no score change|The phrase "please enter a guess" is displayed|pass||
|TC-07|Input Validation-Non-Alphabetic Input|Prevent submission of invalid characters|Input should be rejected with a specific error message like “Only alphabet characters allowed”; score should not change|Message displayed: “Incorrect, try again!”|Failed||
|TC-08|UI Layout-Mobile Responsiveness|Verify layout adapts to mobile view|All elements visible, aligned, and functional on mobile|Layout accomodate the adjusted size|Pass||
|TC-O9|input validation|Test handling the number of characters added is the same as the characters in the word to be guessed |error message "word incomplete"|Error message "incorect, try again"|Failed||
|TC-10 | Hint Button| Ensure score decreases by 2 on hint usage| Score decreases and hint displayed|The score decrease by 2 and the hint is displayed | Pass | |

ID: TC-01
Feature: Word Scrambling
Objective: Verify word scrambling functionality
Steps:
1. Launch index.html
2. Check scrambled word displayed
3. Compare with original word

Achieve: Scrambled word differs from original; all letters present; length unchanged |
Expected: Scrambled word ≠ original word; all letters present; length unchanged 
Risk Priority: High

ID: TC-02
Feature: Scoring System
Objective: Validate score updates correctly for correct guesses
Steps:
1. Launch index.html
2. Check scrambled word displayed
3. Input your correct guess in the input text without using a hint/ using a hint
4. Click the submit button

Achieve score: Not all words are scrambled 
Expected: +10 points (without hint) +5 point(with hint)
Risk Priority: High

ID: TC-03
Feature: Bonus round
Objective: Confirm bonus activates after every 3 puzzles
Steps:
1. Launch index.html
2. Check scrambled word displayed
3. Input your correct guess in the input text without using a hint/ using a hint
4. Click the submit button
5. Input your correct guess in the input text without using a hint/ using a hint
6. Click the submit button
5. Input your correct guess in the input text without using a hint/ using a hint
6. Click the submit button

Achieve score: sum of the 3 correct guess multiply by 2, e.g if you solve the puzzles correctly without using a hint ((10 + 10 + 10) * 2)
Expected: After third puzzle solved correctly score must be doubled.
Risk Priority: High

ID: TC-04
Feature: Leaderboard 
Objective: Verify top 3 scores persist
Steps:
1. Launch index.html
2. Input the correct answer
3. Current high score added on Leaderboard
4. Input the correct answer
5. Current high score added on Leaderboard
6. Input the correct answer
7. Current high score added on Leaderboard

Achieve result: Top 3 scores persists after refresh
Expected: Top 3 scores remain visible after refresh
Risk Priority: Medium

D: TC-05
Feature: Reset Game 
Objective: Ensure reset clears progress and score
Steps:
1. Launch index.html
2. Input the correct answer (update the score, number of solved and left to solve before getting bonus)
4. Click Reset button

Achieve result: Reset clears score & progress
Expected: Score resets to zero; first puzzle is displayed; progress is cleared
Risk Priority: Medium

D: TC-06
Feature: Input Validation-Empty Input Submission
Objective: Prevent submission of empty input|“Please enter a guess”; no score change
Steps:
1. Launch index.html
2. leave input text empty
3. Click the submit button

Achieve result: The phrase "please enter a guess" is displayed
Expected: Prevent submission of empty input|“Please enter a guess”; no score change
Risk Priority: Medium

ID: TC-07
Feature: Input Validation-Non-Alphabetic Input
Objective: Prevent submission of invalid characters
Steps:
1. Launch index.html
2. Input numbers or special symbols on the input text
3. Click the submit button

Achieve result: Error message "incorect, try again"
Expected: Input should be rejected with a specific error message like “Only alphabet characters allowed”; score should not change
Risk Priority: Medium

ID: TC-08
Feature:UI Layout-Mobile Responsiveness
Objective: Verify layout adapts to mobile view
Steps:
1. Launch index.html
2. Adjust the layout to phone and tablet sizes

Achieve result: Layout accomodate the adjusted size
Expected: Verify layout adapts to mobile view|All elements visible, aligned, and functional on mobile
Risk Priority: Medium

ID: TC-09
Feature: input validation
Objective: Test handling the number of characters added is the same as the characters in the word to be guessed 
Steps:
1. Launch index.html
2. Input wrong number of characters
3. Click the submit button

Achieve result: Error message "incorect, try again"
Expected: Should disable the submit button and write an error message underneath the input text "word incomplete" until the correct number of characters is inputed.
Risk Priority: Medium

ID: TC-10
Feature: Hint Button
Objective: Ensure score decreases by 2 on hint usage
Steps:
1. Launch index.html
2. Click on the hint button

Achieve result: The score decrease by 2 and the hint is displayed
Expected: Score decreases and hint displayed.
Risk Priority: Medium



## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
|001| All score disappears after refresh|Medium |001 | Open|https://github.com/PLP-Database-Design/wk-5-Thembisile-Nkambule-1/issues/2 |
|002| Repeating the same puzzle/ word many times|Medium|001|Open|https://github.com/PLP-Database-Design/wk-5-Thembisile-Nkambule-1/issues/3
|003| Resetting  doesn't display a new word scramble|Low|003|Open|https://github.com/PLP-Database-Design/wk-5-Thembisile-Nkambule-1/issues/4

## Metrics |  Test Control & Project Management

- Test Case Pass Percent: 66.67%
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 100%

### Defect Summary

- Total Defects Logged: 
- Critical High: 
- Fix Rate: 


## Lessons Learned

- Most Defect Prone Feature: Scrambled word to guess- keeps on repeating the same word
- Risk Analysis Impact: High
- Team Communication Effectiveness: 100%
- Improvements for Next Cycle: Group task allocation

## Attachments

- Test case 1: (images/TC01.png)
- Test case 3: (images/TC03.png)
- Test case 4: (images/TC04.png)
- Test case 5: (images/TC05.png)
- Test case 6: (images/TC06.png)
- Test case 7: (images/TC07.png)
- Test case 8: (images/TC08.png)
- Test case 9: (images/TC09.png)
- Test case 10: (images/TC10.png)

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
|Prisca Wamboka | Test Manager |P | 28/11/2025 |
|Ivy Nagide | Risk Analyst |I |28/11/2025 |
|Thembisile Nkambule | Test Executor | T|28/11/2025 |

## Overall Summary

**Statement:** 

**Test Status:** Completed 
