\## Week 7 — Issue selection



\*\*Issue link:\*\* https://github.com/ascherj/pathreview/issues/156



\*\*Issue title:\*\* README scorer test fixture is too short for its own word-count assertion



\*\*Tier:\*\* \[X] Tier 1  \[ ] Tier 2  \[ ] Tier 3



\*\*Selection reasoning:\*\*

Picked a Tier 1 problem since it is the skill level that seems adequate for me. It deals with seemingly one component, the readme\_scorer.py and the given logic. A higher tier would likely be more involvement of files that rely on one another, which appears far more difficult than I might be able to manage at the moment. This is also a very realistic example where one would have to search for the cause of a "perfect" test file failing and the cause not being the actual behavior but another asserted aspect.



\*\*Problem summary:\*\*

The test\_readme\_with\_all\_quality\_signals in the tests for the readme\_scorer.py has it set that the word count of the README would be over 100 words in length \[line: assert data\["word\_count"] > 100], but the current fixture README only has 52 and the test is failing even though its behavior being tested beside that works. Basically the README test is failing the README because it has smaller word count than assumed and not because the README is incorrect in any other fashion. A successful fix would allow for the README scorer to work properly as long as the README is not empty.



\*\*Branch name:\*\* fix/156-readme-scorer-fixture



\*\*Setup confirmation:\*\* \[X] App runs locally at localhost:5173



\*\*Cohort ledger:\*\* \[X] Issue added to cohort ledger







\## Week 8 — Reproduction \& solution planning



\*\*Reproduction commit link:\*\* https://github.com/Cristina-Adame/pathreview/commit/af2b33ae77174ed0458f0b4933df1de57c2088bd 



\*\*Reproduction summary:\*\*

Ran the command "pytest tests/unit/test\_readme\_scorer.py -q" on my branch and saw the failure:

```

FAILED tests/unit/test\_readme\_scorer.py::TestReadmeScorer::test\_readme\_with\_all\_quality\_signals - assert 51 > 100



```

Confirms that the README has 51 words but the assertion expects more than 100, causing it to fail. This is failing even though the other README requirements/assertions are met.



\*\*PLAN.md link:\*\* https://github.com/Cristina-Adame/pathreview/blob/fix/156-readme-scorer-fixture/PLAN.md



\*\*Walkthrough video (recommended):\*\* N/A



\*\*Blockers or open questions:\*\*


