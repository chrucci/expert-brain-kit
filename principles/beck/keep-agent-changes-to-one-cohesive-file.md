# Keep agent changes to one cohesive file

Verified: 2 verbatim quotes from 1 source

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Compare the agent's first-attempt success rate on single-file changes against changes that span several files or touch very large files.

Agents do worse when a file grows too long and when a change spans several files. Structure code into cohesive files so each change touches one file, even if that means temporarily merging files before splitting them again.

## Quotes

> If I have a single file and it gets too long, then the genie doesn't get the right context to make changes.
>
> [Genie Sessions: Optionality at 00:51:07](https://newsletter.kentbeck.com/p/genie-sessions-optionality?t=3067s)

> the genie only has to operate on a single file at a time, then it seems to operate much better. If I break it out into two files and now the genie has to make some change that spans two files, then it gets stupid again.
>
> [Genie Sessions: Optionality at 00:52:00](https://newsletter.kentbeck.com/p/genie-sessions-optionality?t=3120s)

## Support

Candidate: one source supports this principle so far.

Expert: Kent Beck

Topics: techniques

## Related principles

- [Kent Beck: Watch for the coordination tax of agent swarms](watch-for-the-coordination-tax-of-agent-swarms.md)
