# content/

Written by the paper, not by hand.

When an editor locks an issue, the publishing system commits it here through
the GitHub Contents API. The commit *is* the publication event: its timestamp
is when the issue became final, and its diff is the only way an issue's text
ever changes.

```
issues/       one JSON file per published issue, exactly as it went out
crosswords/   the weekly mini, committed at the same lock
```

Two rules hold this together:

1. **Issues are append-only in spirit.** A correction is a new commit that
   states what was wrong. We do not silently edit a published claim, and
   `git log` is the receipt.
2. **Sources travel with the story.** Each issue file carries the citations
   behind each of its stories, so verifying us never requires trusting us.

Directories are kept by `.gitkeep` until the first issue lands.
