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

2. Review the changes and focus on identifying critical issues related to:
   - **Correctness**: Does the code do what it's supposed to do?
   - **Design**: Is the code well-structured and following project conventions?
   - **Performance**: Are there any obvious performance issues?
   - **Security**: Are there any security concerns?
   - **Tests**: Are there appropriate tests for the changes?

3. If major issues are found, summarise them by file, with specific line references where applicable. If no major issues are found, provide a simple approval without listing each file.

# Tips
Keep your response concise. Only highlight critical issues that must be addressed before merging. Skip detailed style or minor suggestions unless they impact performance, security, or correctness.
