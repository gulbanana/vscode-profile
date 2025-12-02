---
description: 'Code Review'
agent: agent
model: Claude Opus 4.5 (Preview)
tools: ['edit', 'search', 'runCommands', 'usages', 'problems', 'changes', 'testFailure', 'fetch', 'todos', 'runTests']
---

# Instructions

1. Get the diff for ${input:revset} using jujutsu:
   ```powershell
   jj diff --no-pager --git -r "${input:revset}"
   ```

2. Review the changes for:
   - **Correctness**: Does the code do what it's supposed to do?
   - **Design**: Is the code well-structured and following project conventions?
   - **Naming**: Are variables, methods, and classes named clearly?
   - **Error handling**: Are errors handled appropriately?
   - **Performance**: Are there any obvious performance issues?
   - **Security**: Are there any security concerns?
   - **Tests**: Are there appropriate tests for the changes?

3. Provide feedback organized by file, with specific line references where applicable.

4. Summarize the overall assessment and any blocking issues.
