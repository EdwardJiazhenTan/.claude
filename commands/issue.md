Plan and analyze a GitHub issue: $ARGUMENTS

### Steps:

1. **Retrieve Issue Details**
   - Use `gh issue view $ARGUMENTS` to get the full issue details
   - Review issue title, description, labels, and comments

2. **Understand and Explain the Problem**
   - Clearly explain what the issue is asking for
   - Identify the core problem or feature request
   - Note any technical requirements or constraints mentioned

3. **Ask Clarifying Questions**
   - If anything is unclear or ambiguous, ask specific clarifying questions
   - Identify any missing information needed for implementation

4. **Research Prior Art**
   - Search scratchpads for previous thoughts related to this issue:
     `find . -name "*.md" -path "*/scratchpads/*" -exec grep -l "issue_keyword" {} \;`
   - Search PRs to find history on this issue:
     `gh pr list --search "issue_keyword" --state all`
   - Search codebase for relevant files and patterns:
     `git grep -n "relevant_keywords"`

5. **Break Down into Manageable Tasks**
   - Think systematically about how to decompose the issue
   - Create a series of small, independent tasks
   - Consider dependencies between tasks
   - Estimate complexity and effort for each task

6. **Document the Plan**
   - Create a new scratchpad file: `scratchpads/issue-$ARGUMENTS-plan.md`
   - Include the issue name and link: `https://github.com/REPO/issues/$ARGUMENTS`
   - Document all findings, tasks, and implementation approach
