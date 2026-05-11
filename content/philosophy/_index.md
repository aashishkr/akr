---
draft: true
title: "Engineering Philosophy"
description: "How I think about building software — strategy, scale, and developer empowerment."
summary: "Strategy-first thinking, predictable scaling, and empowering the org through great developer experience."
showToc: true
---

Building software at scale isn't just about writing code — it's about making decisions that compound. These are the principles I return to, whether I'm sketching an architecture on a whiteboard or debugging a production incident at 2 AM.

---

## Strategy-First

The most expensive bug is building the wrong thing.

Before any system design begins, I start by mapping user journeys end-to-end. This isn't a product manager's job alone — as engineers, we hold context about technical constraints that fundamentally shape what's feasible and what's elegant.

At Coinbase, this meant studying how new users moved through onboarding across different regulatory regimes. By identifying shared patterns in these journeys, we consolidated what would have been a dozen country-specific flows into a single, configurable platform — cutting the project timeline significantly and reducing the surface area for bugs.

**The principle:** Invest time upfront to understand *why* a system exists before deciding *how* to build it.

---

## Scaling Predictably

The goal isn't to handle the next 10x — it's to make the next 10x boring.

I've spent years migrating systems from legacy monoliths to modern, event-driven architectures. At Google, this meant transitioning mission-critical user-facing services to Go and Java-based event streams backed by Kafka and Cloud Spanner. The measure of success wasn't the migration itself — it was that downstream teams barely noticed it happened.

Zero-error performance isn't aspirational; it's a design constraint. Every system I build starts with a failure budget, clear SLOs, and automated observability that surfaces problems before users feel them.

**The principle:** Reliable systems are designed, not debugged into existence.

---

## Empowering the Org

The best infrastructure is invisible. Engineers should be building products, not fighting their tools.

I treat Developer Experience as a first-class product. At every company I've worked at, I've invested in building SDKs, no-code configuration tools, and self-service platforms that let product engineers move fast without deep infrastructure knowledge.

At Google, this looked like building privacy compliance SDKs that abstracted away the complexity of EU DMA requirements — turning a months-long compliance process into a few lines of configuration. At Coinbase, it meant designing A/B testing platforms that product teams could operate independently, without requiring infrastructure team involvement for every experiment.

**The principle:** If other engineers need to read your system's source code to use it, you haven't finished building it.

---

*These aren't abstract principles — they're the lens I use to evaluate every technical decision. If you think about building software the same way, [let's talk](/contact/).*
