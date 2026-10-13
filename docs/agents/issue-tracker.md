# Issue tracker: GitHub

Issues and specs live in GitHub Issues for `11rex11/Tw-homepage`.
Use the `gh` CLI from the repository checkout.

## Conventions

- Create: `gh issue create --title "..." --body-file <file>`
- Read: `gh issue view <number> --json number,title,body,labels,comments`
- List: `gh issue list --state open --json number,title,body,labels`
- Comment: `gh issue comment <number> --body-file <file>`
- Label: `gh issue edit <number> --add-label "..." --remove-label "..."`
- Close: `gh issue close <number> --comment "..."`

Use appropriate state and label filters when listing issues.
Write multiline content to a file and pass it with `--body-file`.

When a skill says "publish to the issue tracker", create a GitHub issue.
When it says "fetch the relevant ticket", read the GitHub issue.

## Pull requests as a triage surface

**PRs as a request surface: no.**

## Related work

Use native sub-issues and dependencies when supported.
Otherwise, put `Part of #<parent>` and `Blocked by: #<number>` in
child issue bodies, and maintain a task list in the parent issue.
A ticket is unblocked when every blocker is closed.
