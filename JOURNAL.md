\## Week 7 — Issue selection



\*\*Issue link:\*\* https://github.com/ascherj/pathreview/issues/156



\*\*Issue title:\*\* README scorer test fixture is too short for its own word-count assertion



\*\*Tier:\*\* \[X] Tier 1  \[ ] Tier 2  \[ ] Tier 3



\*\*Problem summary:\*\*

The test\_readme\_with\_all\_quality\_signals in the tests for the readme\_scorer.py has it set that the word count of the README would be over 100 words in length \[line: assert data\["word\_count"] > 100], but the current fixture README only has 52 and the test is failing even though its behavior being tested beside that works. Basically the README test is failing the README because it has smaller word count than assumed and not because the README is incorrect in any other fashion. A successful fix would allow for the README scorer to work properly as long as the README is not empty.



\*\*Branch name:\*\* \[paste branch name here]



\*\*Setup confirmation:\*\* \[X] App runs locally at localhost:5173



\*\*Cohort ledger:\*\* \[X] Issue added to cohort ledger

