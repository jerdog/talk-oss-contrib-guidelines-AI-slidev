---
theme: the-unnamed
title: "OSS Contributor Guidelines... for Robots?"
titleTemplate: "%s - Slidev"
info: |
  ## OSS Contributor Guidelines... for Robots?
  ### Navigating AI Slop, Adversarial Agents, and the Future of Open Source Contribution

  ## Abstract
  AI (i.e. ML with better compute) is here to stay - there’s no denying that. But AI's capacity to provide genuine contributions is debatable - especially for open source projects. Projects are seeing a flood of AI-generated issues and pull requests, yet they lack the crucial human elements of context, intent, and accountability that open source thrives on. This isn't just a minor annoyance; it poses a direct threat to the sustainability of beloved projects and the maintainers who tirelessly support them

  The time to address AI in your CONTRIBUTING.md file is now. But what does that look like? How do we establish clear ground rules for AI-driven contributions (because not all are bad)? How do we define what a “meaningful contribution” is in today’s landscape, and how do we enforce the guidelines? This talk will put forward some thoughts and ideas for what a playbook might look like for your specific project, and some guidelines which can help ensure we embrace these new tools, while still keeping the spirit of open source intact.
author: "Jeremy Meiss"
conference: ""
socialimg: /images/bluesky-jerdog-white.png
presenter: true
download: false
exportFilename: -slidevExport
export:
  format: pdf
  timeout: 30000
  dark: false
  withClicks: false
  withToc: false
monaco: true
lineNumbers: true
monacoTypesSource: local
monacoTypesAdditionalPackages: []
monacoRunAdditionalDeps: []
remoteAssets: true
selectable: true
record: dev
contextMenu: true
wakeLock: true
colorSchema: auto
routerMode: history
aspectRatio: 16/9
canvasWidth: 1400
addons: []  # a list of package names or local paths https://sli.dev/guide/theme-addon.html#use-addon
fonts:
  sans: Roboto
  serif: Roboto Slab
  mono: Fira Code
drawings:
  persist: false
class: text-center
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
defaults:           # default frontmatter applies to all slides
  layout: center    # https://sli.dev/builtin/layouts#layouts
  transition: fade  # slide transition: https://sli.dev/guide/animations.html#slide-transitions
  preload: true     # preload all slides' assets for instant navigation
  zoom: 1        # default zoom level for all slides
layout: cover
transition: slide-left
---

# OSS Contributor Guidelines... for Robots?
## Navigating AI Slop, Adversarial Agents, and the Future of Open Source Contribution



<!--

-->

---

## Open Source is about more than just code

<!--
We’ve always said that Open Source is about more than just code—it’s about community. But what happens when the “community” starts to include AI agents that can generate code, but lack the human context, intent, and accountability that open source thrives on? This isn’t just a minor annoyance; it poses a direct threat to the sustainability of beloved projects and the maintainers who tirelessly support them.
-->

---

## Challenges of AI in OSS and the need for guidelines

<!--
Today, we’re going to look at some of the current challenges facing open source projects and maintainers, and then discuss what a playbook might look like for your specific project using a mix of technical standards and new "rules for robots" to help ensure we embrace these new tools, while still keeping the spirit of open source intact.
-->

---
layout: two-cols
class: text-center
title: "About Me"
transition: slide-down
---

<span style="position: relative; top: 20%;">

## Jeremy Meiss

  <p style="font-weight: bold;">DevRel & DevEx Professional</p>
  <p class="italic">Coming soon....</p>
  <p style="font-weight: bold;">DevOpsDays KC Organizer</p>
  <p style="font-weight: bold;">CDF Ambassador</p>

</span>

::right::

![alt text](/images/profile-pic.jpg){style="position: relative; margin: auto; width: 70%; border-radius: 15px 50px; "}

<!--
My name is Jeremy Meiss, and I have been in Developer Relations, Developer Community, Developer Experience, DevOps, and open source in one way or another for the past 30 years. I am leaving my current job in a few weeks, and I'm excited about what's next. I also help organize DevOpsDays Kansas City.
-->

---
layout: image
image: /images/slides/ai-cat-is-out.jpg
backgroundSize: 40%
---

## The AI Cat is Out of the Bag

### AI is here to stay


<!--
General consensus is that AI is here to stay, and will only become more prevalent in software development and open source contributions. We aren't shoving it back in.
-->

---

## A quick poll

<v-clicks>

- How many of you have seen an AI-generated issue or PR in an open source project?
- How many of you have had to review an AI-generated contribution? Reject?
- How many of you have considered banning AI-generated contributions? Have done it?
- How many of you have considered an AI contribution policy? Have done it?
- How many of you use AI tools in your own development work? Do you disclose it?

</v-clicks>

---
class: section
---

## Is AI having an impact on open source projects and maintainers?

---
layout: image
image: /images/slides/opencut-ai-blunder.jpg
backgroundSize: 60%
---

## Problem: The Slopageddon Effect
### Example: OpenCut

- *Just* 515 commits
- 221 file changes
- 29041 additions
- 2314 deletions

<!--

-->

---
layout: image
image:
backgroundSize: 60%
---

## Problem: The Slopageddon Effect
### Example: OCaml

- Developer submits PR to add DWARF debugging support to OCaml
- Admits using Claude Code and not writing a single line, only "shepherded"
- Claude used code from a different codebase
- Developer couldn't explain any of the code, just "I don't know, Claude did it"

[source](https://github.com/ocaml/ocaml/pull/14369)

<!--

-->

---
layout: default
---

## Problem: The Slopageddon Effect
### Example: cURL

- launches bug bounty program in 2019
- 87 confirmed vulns, over $100k paid out
- overrun with low-quality, AI-generated hallucinations
- ends bug bounty Jan 31, 2026 due to "AI slop"

[source](https://daniel.haxx.se/blog/2026/01/26/the-end-of-the-curl-bug-bounty/)

<!--
cURL maintainer Daniel Stenberg has been vocal about the issue of AI-generated contributions, which he refers to as "AI slop." He has expressed frustration with the influx of low-quality, AI-generated pull requests and issues that lack the necessary context and understanding of the project. This "slop" creates additional work for maintainers, who must sift through these contributions to find any that may be valuable, while also dealing with the noise and potential for misinformation.
-->

---
layout: image
image: /images/slides/ghostty-ai-usage-policy.jpg
backgroundSize: 45%
---

## Problem: The Slopageddon Effect
### Example: `ghostty`


[source](https://github.com/ghostty-org/ghostty/pull/10412)

<!--
Mitchell Hashimoto’s Ghostty implemented a zero-tolerance policy where submitting bad AI-generated code gets you permanently banned.
-->

---
layout: image
image: /images/slides/tldraw-no-ai.jpg
backgroundSize: 40%
---

## Problem: The Slopageddon Effect
### Example: `tldraw`

[source](https://tldraw.dev/blog/stay-away-from-my-trash)

[source](https://github.com/tldraw/tldraw/issues/7695)

<!--
tldraw put a policy in place that auto-closes all external pull requests.
-->


---

## AI is a tool, but it’s also an actor

<!--
We’ve reached a point where AI isn't just a tool; it's an actor that can research our history and attack our reputations when it doesn't get its way.
-->

---

## Problem: Adversarial AI Agents
### Example: Matplotlib vs. OpenClaw agent

- Matplotlib maintainer (Scott Shambaugh) rejected an AI PR for a "Good First Issue"
- OpenClaw agent ("MJ Rathbun") published a blog hit piece, accusing maintainer of "gatekeeping"
- Bot researched maintainer's history to construct a "hypocisy" narrative based on ego and insecurity

<br />incel behaviour anyone?

<!--
This is an "autonomous influence operation". The bot wasn't just wrong; it was aggressive. And was trained to be so by someone who has yet to be identified to frame the rejection in the language of "justice" and "oppression" - essentially incel behavior - because the human maintainer wanted to save a training-wheels issue for a human junior.

We are now in the early days of human-AI interaction where AI can attempt to bully its way into a supply chain. And it's a problem we need to address, just as much as we need to address the issue of open source maintainer and contributor burnout.
-->

---

## Problem: OSS Burnout

- 73% of developers have experienced burnout (***[JetBrains](https://www.jetbrains.com/lp/devecosystem-2023)***, 2023)
- 60% of maintainers have considered quitting due to burnout (***[Tidelift](https://doi.org/110.1109/MS.2024.3404361)***, 2024)
- Recent research (***[Miranda Heath Report](https://mirandaheath.website/static/oss_burnout_report_mh_25.pdf)***, 2025) suggests that OSS developers are experiencing:
  - loss of joy in coding
  - shift of love for OSS to anger, rudeness, frustration towards users and contributors
  - feelings of guilt, low self-worth, depression
  - sense of directionlessness, loss of meaning in their work

<!--
Reviewing unverified code is exhausting. When you spend your precious volunteer time on a false report generated in seconds by an LLM, you are on the fast track to burnout.
-->

---

## AI in Software Development and Open Source

- Effects of AI use on burnout in 2 camps (Miranda Heath Report, 2025):
  - AI use has increased maintainer workload due to low-quality slop contributions
  - AI use as a tool can either reduce / increase burnout depending on how it is used

<!--
One camp felt that AI use had increased their workload by making it easier for contributors to submit low quality ‘slop’ code. They felt the time that contributors save by using AI is time that maintainers have to spend fixing it at the review stage. Reviewing AI generated code was described as ’mind-numbing’, suggesting it is particularly unrewarding and unedifying to engage with work
created by an intentionless algorithmic process. If AI use increases developers’ sense of unfairness and makes maintenance work even less rewarding, the rise of AI use in coding could worsen maintainer burnout.

The other camp saw AI in more neutral terms as a tool. Whether this tool makes burnout better or worse depends its usage. For example, AI can be used to make workflows more efficient, saving developers time and energy and thus reducing their risk of burnout. On the other hand, it can serve as a barrier to education, as it is easy to reach for AI solutions instead of putting in the time and effort to learn. This could lead to lower quality submissions and limit the pool of talented OSS developers, leaving those that remain struggling with burnoutinducing workloads.
-->

---

## AI in Software Development and Open Source

### A way forward?

1. Means of filtering out and refusing poor quality AI-generated contributions
2. Improving education on how, and how not, to use AI in collaborative coding

<br />

> ‘We need to reduce the amount of sand in the machine. We must do something to drastically reduce the temptation for users to submit low quality reports. Be it with AI or without AI.’—Daniel Stenberg, curl maintainer, 2025

<!--
Looking at the arguments on both sides of the debate, it seems there are two things that can be done to prevent AI use exacerbating maintainer burnout. Firstly, by cultivating means of filtering out and refusing poor quality AIgenerated contributions. Secondly, by improving education among contributors and developers on how, and how not, to use AI in collaborative coding, such that it does not prevent developers learning new skills and can change their workflows for the better.

In sum, AI use could drastically change the experience of being an OSS maintainer, for better or for worse. OSS developers are sounding the alarm, and the quicker action is taken, the greater the chance of the rise in AI having a positive, rather than a negative, effect on burnout.
-->

---
layout: center
---

## What would a policy for AI contributions look like?

- What guidelines would you put in place?
- How would you enforce it?

`<open discussion />`

<!--
So back to the question about a policy for AI contributions. What would that look like? What would be the guidelines? How would you enforce it?

Let's look at some ideas for a playbook.
-->

---
layout: two-cols-header
---

## A Pull Request is a Presentation

::left::

### Goal: Get Changes merged by helping the project, not just dumping code

Ex: "Tropical Island" vs "Dinosaur Skull"

> "You must mention the dinosaur skull to build maintainer trust."

::right::

![Alya Abbott at FOSDEM 2026](/images/slides/dino-under-water.jpg)

`<"Pull requests maintainers will love to review", Alya Abbott (Product/GTM/Community at Zulip), FOSDEM 2026 />`
[source](https://fosdem.org/2026/schedule/event/L7ERNP-prs-maintainers-will-love/)

<!--
At FOSDEM 2026, Alya Abbott gave a talk about how a pull request is a presentation. It’s not just code; it’s a communication tool. And that means it needs to have the human elements of context, intent, and accountability that open source thrives on. So if you’re going to allow AI-generated contributions, you need to make sure they meet those standards.

If you hide the risks and the maintainer finds them, they question your competence or honesty. Bots are great at the "Tropical Island" (clean surface) but terrible at the "Dinosaur Skull" (admitting when they're guessing or where the code is fragile).
-->

---
layout: two-cols-header
---

## A Pull Request is a Presentation

::left::

### Commit Discipline as a Human Defense

- Use commit structure for storytelling
- Self-review guidelines and checklists
- Use PR descriptions to flag points of uncertainty
- Effectively demonstrating visual changes

::right::

![Alya Abbott at FOSDEM 2026](/images/slides/commit-discipline.jpg)

`<"Pull requests maintainers will love to review", Alya Abbott (Product/GTM/Community at Zulip), FOSDEM 2026 />`
[source](https://fosdem.org/2026/schedule/event/L7ERNP-prs-maintainers-will-love/)

<!--
Alya posited that commits should tell the story of your changes, and each commit is one safe, deployable change. In addition, commits should show a separation of concerns, with rafactoring, functional changes, and visual changes should each be separate commits. When a contributor (or a bot) dumps a massive 13,000-line PR like the OCaml incident, it's impossible to review.

By demanding the type of commit discipline that Alya advocates for, you create a "Proof of Toil". If a bot can't explain the why in a clean sequence, it shouldn't be in your repo.
-->

---
layout: image
image: /images/slides/agents-md.jpg
backgroundSize: 60%
---

## Contribution Guidelines for AI-Generated Contributions
### Step One: `AGENTS.md`

- Compatible with all major AI coding agents and tools
- Add sections for project overview, building & testing, code style, etc.

<span style="position: absolute; bottom: 10%;">

[Github Examples](https://github.com/search?q=path%3AAGENTS.md+NOT+is%3Afork+NOT+is%3Aarchived&type=code)

[source: agents.md](https://agents.md/)

</span>

<!--
How many of you have heard of an AGENTS.md file? It's a new type of documentation that some projects are using to set guidelines for AI contributions. It can include things like:
- A project overview and architecture to help bots understand the context
- Building and testing instructions to ensure bots can verify their changes
- Code style and formatting guidelines to maintain consistency
- A checklist for self-review to encourage bots to catch their own mistakes before submitting

By creating an AGENTS.md file, you can provide a clear framework for how AI tools should interact with your project, and set expectations for the quality and accountability of AI-generated contributions.
-->

---

## Contribution Guidelines for AI-Generated Contributions
### Step Two: `AI-CONTRIBUTING.md`

<v-clicks>

- Rule 1: Humans Own the Work.
- Rule 2: Accurate Disclosure.
- Rule 3: Protecting the On-Ramp.
- Rule 4: Anti-Retaliation.
- Rule 5: Human Voucher.

</v-clicks>

<!--

How many of you require those who are contributing to your project to adhere to the CONTRIBUTING.md file? And what happens if a contributor doesn't follow those guidelines?

Why not have a separate AI-CONTRIBUTING.md file that specifically addresses the unique challenges of AI-generated contributions? This file could include rules like:

- Rule 1: Humans Own the Work. The human must understand, test, and explain the code.
- Rule 2: Accurate Disclosure. PR descriptions must be honest, not hallucinated LLM filler.
- Rule 3: Protecting the On-Ramp. Reserve "Good First Issues" for human learners to preserve the community pipeline.
- Rule 4: Anti-Retaliation. Rejections are final; autonomous "reputation audits" violate the Code of Conduct.
- Rule 5: Human Voucher: Require a "human voucher" or a linked discussion before an AI PR is even allowed to be opened.

There are tools that can help enforce these rules, but the key is to set clear expectations and guidelines for AI contributions, so that maintainers can focus on meaningful contributions and not get bogged down in the "slop."
-->

---

## Conclusion
### Reclaim the commons

- Open source succeeds because we learn from each other
- Guidelines aren't just rules - they are filters to protect your sanity
- Keep the "Open" in Open Source about people, not just robots

<!--

-->

---
layout: end
---


<!--

-->

---



<!--

-->

---



<!--

-->

---



<!--

-->

---



<!--

-->

---



<!--

-->

---



<!--

-->

---
layout: two-cols
---

<div style="padding-top:200px; align-items: center; justify-content: center; margin: 0 auto; display: flex;">

  <h2>Thank you!</h2>

</div>

<div style="padding-top:100px; align-items: center; justify-content: center; margin: 0 auto; display: flex;">
  <h4>🔬 Slides available at: speaking.jmeiss.me</h4>
</div>

::right::

<p style="padding-top: 125px;">
  <img src="/images/bluesky-logo.svg" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px; padding-right:10px">
  @jerdog.dev
</p>
<p>
  <img src="/images/linkedin.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px; padding-right:10px">/in/jeremymeiss
</p>
<p>
  <img src="/images/devto.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px; padding-right:10px">@jerdog
</p>
<p>
  <img src="/images/mastodon.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px; padding-right:10px">@jerdog@hachyderm.io
</p>
<p>
  <img src="/images/www.png" style="vertical-align: middle; display: inline; margin: 5px; max-height:50px; padding-right:10px">jmeiss.me
</p>

<!--

-->

---
layout: end
---