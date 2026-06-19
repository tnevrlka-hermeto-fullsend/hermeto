## Upstream issue context

Issues in this repository mirror upstream issues from hermetoproject/hermeto.
The upstream issue number is embedded as an HTML comment in the issue body:

    <!-- upstream-issue: NUMBER -->

### Steps

1. Extract NUMBER from the `<!-- upstream-issue: NUMBER -->` HTML comment
   in the issue body.
2. Fetch the full upstream issue including all comments:

       gh issue view NUMBER --repo hermetoproject/hermeto \
         --json title,body,comments,labels,state

3. Use the fetched title, body, and comments as your primary context for
   understanding the problem. The snapshot in the mirror issue body is a
   fallback only — prefer the live upstream data.

### Constraints

- NEVER interact with the upstream repository — no comments, no PRs,
  no reactions, no references of any kind.
- NEVER use the format `hermetoproject/hermeto#NUMBER` or any GitHub
  auto-linkable reference in commits, PR descriptions, or comments.
  Use `upstream issue NUMBER` in plain text if you need to reference it.
- All your work targets this fork only.
