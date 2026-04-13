---
name: feedback-patterns
description: A library of common feedback patterns used when reviewing student work at the No More Mondays accelerator. Called by the student-feedback skill as a dependency. Not typically invoked directly. Contains pattern names, triggers, and standard remediation guidance that gets rewritten in the user's voice by student-feedback.
---

# Feedback Patterns Library

This skill is a library, not a standalone tool. It is called by `student-feedback` to supply the raw patterns that show up repeatedly when reviewing student work. The `student-feedback` skill is responsible for rewriting these patterns in the user's voice.

When this skill is invoked directly by a user, respond once with:

> This is a library skill used by Student Feedback. You probably want to invoke `student feedback` instead and paste the student submission you want reviewed.

## When to reference patterns

The `student-feedback` skill calls this library to check student work against common failure modes. Match each pattern below against the submission being reviewed. Any pattern that fires becomes a feedback point.

## The patterns

### Hook patterns

**weak-hook**
- **Triggers when:** the first 2 seconds have no pattern interrupt, the opening is a slow ramp, or the hook is a question the viewer already knows the answer to
- **Core feedback:** the viewer decides whether to keep watching in the first 2 seconds. The current opening gives them no reason to stay. Replace it with a pattern interrupt (unexpected statement, visual contradiction, or contrarian claim).
- **Reference:** NMM Module 2 — Hooks

**generic-hook**
- **Triggers when:** the hook could work for any creator in any niche ("Let me tell you about...", "Today we're going to...", "Here's how to...")
- **Core feedback:** the hook is not specific enough to your offer or audience. Rewrite it so that it only makes sense to someone who is already a potential fit for your product.
- **Reference:** NMM Module 2 — Hooks

**hook-payoff-mismatch**
- **Triggers when:** the hook promises one thing and the rest of the content delivers something else
- **Core feedback:** your hook sets up expectation X but your content pays off Y. Either rewrite the hook to match the content or rewrite the content to match the hook. Do not let the viewer feel lied to.

### CTA patterns

**weak-cta**
- **Triggers when:** the CTA is vague ("Check it out", "Link in bio"), buried, or missing entirely
- **Core feedback:** the viewer needs a clear, specific next action within the first 80% of the content. What exactly should they do, and why now?

**cta-friction**
- **Triggers when:** the CTA asks for too much too fast ("Sign up for my 12-week program") without earning it first
- **Core feedback:** match the CTA weight to the trust the content has earned. Cold viewer = small ask (follow, save, comment). Warm viewer = medium ask (free resource, email). Hot viewer = big ask (purchase, call).

### Positioning patterns

**unclear-audience**
- **Triggers when:** you cannot tell who the content is for after watching the first 10 seconds
- **Core feedback:** the piece is trying to speak to everyone and therefore lands with no one. Pick one specific person in your audience and speak directly to them. Their name, their situation, their objection.

**off-brand-voice**
- **Triggers when:** the tone or language shifts between "you the creator" and "polished marketing" in a way that breaks trust
- **Core feedback:** the voice in this piece is inconsistent with how you usually sound. Viewers notice this instantly. Rewrite in your real voice, not a performed version.

### Structure patterns

**no-retention-hook**
- **Triggers when:** the middle of the content has no re-hook or tension point, and retention drops off
- **Core feedback:** long-form content needs a second hook around the 30-50% mark. A promise, a contradiction, a question you have not answered yet. Keep the viewer leaning forward.

**weak-payoff**
- **Triggers when:** the main insight or moment of value is buried or rushed
- **Core feedback:** the actual value in this piece happens at [timestamp], but it is delivered in 3 seconds and then you move on. Slow down on the payoff. That is what the viewer came for.

**over-explaining**
- **Triggers when:** the creator explains context or background that viewers already have or do not need
- **Core feedback:** you are setting up too much before you deliver. Trust the viewer. Cut the first 20% and start at the point.

### Voice and craft patterns

**filler-words**
- **Triggers when:** "um", "like", "you know", "so yeah" dominate the first 30 seconds
- **Core feedback:** fillers are a symptom of unclear thinking about what you want to say next. Write your first 10 seconds word for word, rehearse it, and land it clean. The rest can be looser.

**monotone-energy**
- **Triggers when:** the performance energy is flat and does not vary between sentences
- **Core feedback:** energy variation is what makes content feel alive. Pick 3 moments in the content where the energy should spike or drop, mark them, and re-record with those variations in mind.

### Missing patterns

**no-proof**
- **Triggers when:** the creator makes a claim ("this works", "I grew to X") with no evidence
- **Core feedback:** unsupported claims are the biggest trust killer. Add one specific piece of proof: a number, a screenshot, a quote, a demo.

**no-stakes**
- **Triggers when:** the content has no consequence — nothing bad happens if the viewer ignores it
- **Core feedback:** why should the viewer care right now? What breaks if they do nothing? The piece is missing a stakes statement.

## How patterns get rewritten

The `student-feedback` skill reads these patterns, identifies which ones fire on a given submission, and then rewrites the `core feedback` line in the user's voice (from section 6 of the Role Project). The pattern name and reference are used internally but may appear in the source block of the final feedback.

## Extending this library

When a new feedback pattern shows up repeatedly, add it here with the same structure: name, triggers, core feedback, reference. Push the update via the repo. All skills that reference this library will pick up the new pattern on next re-install.
