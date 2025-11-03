# Repository Rulesets Test

This repository demonstrates GitHub repository rulesets.

## Configured Rulesets

This repository has the following rulesets configured:

### 1. Main Branch Protection Ruleset
- **Target**: main branch
- **Rules**:
  - Require pull request before merging
  - Require status checks to pass
  - Require branches to be up to date
  - Block force pushes
  - Restrict deletions

### 2. Production Branch Ruleset
- **Target**: production branch
- **Rules**:
  - Require pull request with 2 approvals
  - Require code owner review
  - Block force pushes
  - Restrict deletions

### 3. Tag Protection Ruleset
- **Target**: Tags matching v*
- **Rules**:
  - Restrict tag creation
  - Restrict tag updates
  - Restrict tag deletions

### 4. Development Branch Ruleset
- **Target**: develop and staging branches
- **Rules**:
  - Require status checks
  - Allow force pushes (for development)

## Benefits of Rulesets

- Centralized rule management
- Apply rules to multiple branches/tags with patterns
- More flexible than traditional branch protection
- Can bypass rules for specific actors or teams
- Audit log for rule enforcement

## Testing Rulesets

Try the following to test rulesets:
1. Attempt to push directly to main (should be blocked)
2. Create a PR to main (should require approval)
3. Try to delete a protected branch
4. Try to create/delete a tag matching v*

For more information, see [GitHub Rulesets Documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets).
