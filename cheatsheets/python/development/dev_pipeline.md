# Development Pipeline
- git
  - make sure the previous version was tagged in git
  - PowerShell: gitnewb <featurename>
      - `git checkout -b featurename`
      - (optional) `git push --set-upstream origin featurename`
- code
  - write tests, commit
  - write code, commit
  - tox - ensure all PASSes and 100% coverage
  - commit

## Commit
- pipecommit

## Afterwards
  - `git push --delete origin featurename` (only if I had pushed it to remote)
- Afterwards
  - check readthedocs
  - Document fixes to this pipeline.
  - push changes to this pipeline doc