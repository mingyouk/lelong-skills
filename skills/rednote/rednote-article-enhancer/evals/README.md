# Evals for rednote-article-enhancer

Manual test suite for the skill. Since skills run inside Claude Code conversation,
evals are run by pasting test prompts and checking results by observation.

## How to run

**Trigger evals:** In a fresh Claude Code session, paste each test prompt.
Check whether the skill loads (you should see "Loading rednote-article-enhancer…").

**Quality evals:** Invoke the skill with the given input. Check the output against
each expected behavior in the checklist.

## Pre-commit checklist

Before committing changes to SKILL.md:

- [ ] Ran trigger evals — all positive cases trigger, all negative cases don't
- [ ] Ran quality evals — output matches formatting rules
- [ ] Updated CHANGELOG.md with the change summary
- [ ] Reviewed the diff as you would code — does each change have clear intent?

## When to run

- Before committing changes to SKILL.md
- After rewriting the description
- After changing workflow, rules, or checklist
- After tightening/relaxing trigger boundaries
