# Kolibri Improvement Proposals (KIPs)

The Kolibri Improvement Proposals repo is a place to submit, consider, and discuss gov proposals for the Kolibri Protocol. By no means is it the only way to have these discussions, but in general the pull request/software review cycle lends nicely to writing proposals and iterating on them.

This sort of proposal system has been used to great effect by other projects (like [Django](https://github.com/django/deps), [Debian](https://dep-team.pages.debian.net/), [Curve Finance](https://resources.curve.fi/guides/voting/creating-a-dao-proposal#creating-your-proposal), and countless others), and should work well for Kolibri as well. It's very useful to drive consensus off-chain about changes, refining them, and having proposals 

Not all KIPs need to be gov proposals that end up on-chain - they can outline various other changes (e.g. adding or removing a specific mod to the Kolibri Discord). 

## Process

To propose a new KIP, you should copy the `kips/_template.md` file to a new file named something like `kips/KIP01 - Some Proposal Title.md`, fill out the relevant parts, and then open a new pull request against the master branch. From there you should post in the Kolibri Discord (and possibly tweet about it using the #kolibri tag), and folks can show their support via 👍/👎 emojis on the PR itself, as well as ask whatever questions they have.

Note that not all KIPs will be complete at submission time and may have open action items.

## Adoption

Once things have had deliberation period of at least 3 days, the PR will be merged, which should coincide with whatever actions need to be carried out (a proposal being submitted to the DAO - linking to the proposal, or any other things necessary by whomever can do it).

## Helpful Formatting Tips

KIPs are [Markdown](https://www.markdownguide.org/basic-syntax/) files and you can apply some formatting. Common uses patterns below:

### Subheadings

Use:
```
# Main Heading
## Sub Heading
### Sub Sub Heading
````

Renders as:
> # Main Heading
> ## Sub Heading
> ### Sub Sub Heading

### Bold and Italics

Use:
```
*italic*
**bold**
```

Renders as:

> *italic*
> 
>**bold**

### TODOs

If you have an item to discuss, use:
```
🗒️ ⬜ <!-- ✅ --> TODO(your_github_name): Discuss with community \<thing to discuss\>
```

Renders as: 

> 🗒️ ⬜ <!-- ✅ --> **TODO(your_github_name): Discuss with community \<thing to discuss\>**

When resolved, you can either remove the line, or keep it for historical purposes by ammending to:
```
🗒️ ✅ Discussed with community \<thing to discuss\>. See comments in [pull request](https://github.com/hover-labs/kolibri-improvement-proposals/pulls/<PR #>)
```

Which renders as:
> 🗒️ ✅ Discussed with community \<thing to discuss\>. See comments in [pull request](https://github.com/hover-labs/kolibri-improvement-proposals/pulls/<PR #>)
