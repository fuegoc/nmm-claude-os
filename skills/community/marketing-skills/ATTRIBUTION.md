# Marketing Skills — Attribution and License

These skills are forked from the [Marketing Skills](https://github.com/coreyhaines31/marketingskills) collection by **Corey Haines**, built originally for Claude Code and other Agent Skills-compatible coding agents.

- **Original author:** Corey Haines — https://corey.co
- **Original repo:** https://github.com/coreyhaines31/marketingskills
- **Related:** [Conversion Factory](https://conversionfactory.co), [Swipe Files](https://swipefiles.com), [Magister](https://magistermarketing.com)

## Why these are forked into `claude-os`

The No More Mondays Claude OS distributes these skills alongside the custom NMM skills so team members can install them in a single flow without needing to manage a separate plugin marketplace. When an update in upstream Marketing Skills changes something relevant, we pull the fix manually and bump our own CHANGELOG.

## Which skills are forked

Only the subset directly relevant to student feedback on UGC and creator work:

- `cold-email` — B2B cold email sequences (the single most relevant skill for NMM pitch feedback work)
- `copywriting` — write and improve marketing copy across any page
- `copy-editing` — review and improve existing copy
- `ad-creative` — generate and iterate ad creative, headlines, primary text
- `marketing-psychology` — psychological principles and persuasion
- `customer-research` — audience understanding and ICP work
- `product-marketing-context` — foundation skill that the others build on

The other ~33 skills in the upstream repo (SEO, analytics, pricing, CRO for forms/popups/paywalls, etc.) are excellent but not directly relevant to what NMM students work on day to day. Install them separately if needed via the upstream plugin.

## Used by

- `skills/student-feedback/SKILL.md` — calls into these as a library when reviewing student submissions

## License

The original Marketing Skills repo is distributed under its own license (see upstream). Attribution is preserved. Any customizations we make to these files should be clearly marked with a `// NMM customization:` comment so they can be traced.
