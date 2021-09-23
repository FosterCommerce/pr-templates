*Note: Update the date in the PR title, then delete this line.*

## PRs contained in this merge

- #000: description

## Notes
- Are there changes needed to environment variables and/or content on production?

---
# Deployment Checklist

## Prepare for deploy
- [ ] The [staging site] () looks good.
- [ ] All tests are passing on staging.
    - Look in the logs in the [Actions tab] (). Did any tests fail? [Follow the flowchart](https://miro.com/app/board/o9J_lSEaAM0=/).
- [ ] It's an okay time to interrupt production (the client or PM said it's okay).
- [ ] The production DB is backed up and I know how to restore it.

## Merge the PR

- [ ] The PR has been merged. 
    - [GitHub Actions] () will deploy the `main` branch to the production site and run integration tests.
    - [Forge] () will deploy the `main` branch to the production site.

## Quality control & closing
- [ ] The deployment completed successfully.
- [ ] All tests are passing or manually confirmed **on production**.
    - Look in the logs in the [Actions tab] () and/or in the [Cypress Dashboard] (). Did any tests fail? [Follow the flowchart](https://miro.com/app/board/o9J_lSEaAM0=/).
- [ ] The new features are working [on production] ().
- [ ] I've added screenshots and/or links in comments for the deployed Basecamp tasks so PMs and clients can confirm the new features.
- [ ] Relevant tasks are in the `Review on production` group in Basecamp and assigned to the PM.

---

## Resources
- [Our approach to Cypress tests](https://www.notion.so/fostercommerce/Our-approach-to-Cypress-tests-d1361cf2bc5240fbb7bc35749f0f559b)
- [QA Workflow](https://www.notion.so/fostercommerce/QA-Workflow-c2a1b045233c4e49bc2031d2c8f4a8f6)
- [Dev & Deployment Workflow](https://www.notion.so/fostercommerce/Development-and-Deployment-Workflow-Foster-Commerce-301c48dc6e5b43ec9073b708846f7ae5)
