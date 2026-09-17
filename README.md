# RefNet

## What and why?

RefNet is a mobile web application that gives UAE students verified peer reviews and trust-scored referrals for internships, so that landing one depends on merit instead of "wasta" (personal connections).

Two problems compound on each other in the UAE internship market. The first is an access gap: internships are overwhelmingly filled through personal connections rather than open applications, and students without an existing local network are largely shut out regardless of qualification. The second is an information gap: no platform serving the UAE combines verified peer reviews, real salary data, and honest day-to-day accounts of what an internship is actually like — Glassdoor's UAE intern coverage is negligible and its reviewers are never verified as students at all, and dedicated portals like Bayt.com or InternsME are pure listing boards with no review layer whatsoever.

I ran two surveys in June 2026 to check whether these gaps are actually felt rather than assumed. Among 71 UAE university students, 85.9% said they didn't feel they had enough information going in (pay, day-to-day work, culture), and 83.1% said someone less qualified had gotten an opportunity over them because of a connection they lacked. A separate survey of 25 UAE high school students found 84% found the internship search process confusing, and of those who did find something, more went through family or school connections than independent search — meaning without an adult's help, a 15–17-year-old has essentially no real path in.

RefNet closes both gaps with one mechanic: a verified review. Submission is locked behind university email verification, so a review can't be posted without proof of enrollment — the same review then supplies the honest information the access gap hides, and the social proof that powers a credible referral. This matters because internships are frequently the deciding factor in a student's first job offer, and the current process for finding a good one is opaque in a way that disproportionately hurts students without pre-existing professional networks.

## For whom?

RefNet's initial users are NYU Abu Dhabi students actively searching for internships — over 2,000 students, and a deliberate pilot choice rather than a default one. NYUAD is unusually international, so its students are unusually likely to lack the local family network wasta rewards, and it's academically selective, so they're unusually motivated to want a merit-based alternative. I also have direct access to this community and can realistically recruit early reviewers to test the product throughout the semester, rather than designing for an audience I can't reach or validate assumptions with.

A representative persona: an international student a few years into a science or engineering major, with no established professional network in the UAE, who wants a fair shot at competing for the same internships as everyone else. Cold LinkedIn messages rarely get a reply, there's no way to tell upfront which companies even hire international students, and unclear timelines have already cost this kind of student a deadline or two. RefNet helps by surfacing which companies have hired international interns before, giving real timelines and interview accounts from past interns' reviews, and replacing the cold message with a referral that carries an actual track record behind it.

University students are deliberately the only side opened in this pilot: they're the only ones who can write the reviews and give the referrals that make the platform worth anything to anyone else. A second, no-code-required "HS Welcome" filter for high-school-age interns is designed into the data model from the start, but stays switched off in the app until a deep enough review base exists to make it worth opening.

## How?

From a student's perspective, RefNet works as follows:

- **Sign up and verify.** Students create an account with a university email address, establishing verified identity from the start — no review or referral request can be submitted without it.
- **Search or browse companies.** A home screen surfaces companies with the most existing reviews and an industry filter (Finance, Technology, Marketing, Consulting, Energy, Real Estate), with a free-text search bar for company name or role type. Every company tile shows its review count up front.
- **Read verified, anonymous-by-default reviews.** A company page shows an overall rating, tags like "Paid internship" and "HS Welcome," and individual reviews: exact monthly salary, a 1–5 culture rating, a recommend/don't-recommend flag, and the application/interview timeline. Reviews display the reviewer's class year and university for context but not their name, unless they actively opt into attribution — protecting students from the real social risk of a named negative review in a small, tightly networked market, while still keeping every review tied to a verified student.
- **Check a referral trust score.** Referrals carry a trust score built from three inputs: review quality and completeness, referral success rate, and response rate to incoming requests — a transparent, earned alternative to the social credibility wasta hands out for free.
- **Request a referral.** A "Request a Referral" button opens the referring student's profile (trust score, verified review count, referrals given, response rate) with a pre-filled, editable message field, turning a cold ask into something that already carries context and credibility.
- **Build a reviewer profile.** A five-tier reputation system (Explorer through Career Leader) awards points for reviews, tips, and referrals, giving students who've already landed a role a reason to come back and contribute rather than disappearing from the app.

## Scope

RefNet is scoped appropriately for a team of 4–6 programmers over one semester. The core functionality — university email verification, company/review browsing with filtering, an anonymous-by-default review system, trust scoring, and a referral request flow — is substantial enough to require real design and engineering work across frontend, backend, and data modeling, but doesn't require novel algorithmic research or infrastructure at scale. The screens themselves (search, company review profile, referral request flow) are straightforward to scope and build incrementally, which leaves the team's semester effort free to focus on the harder problems: backend verification logic, the referral and trust-score system, and the anonymity/attribution model.
