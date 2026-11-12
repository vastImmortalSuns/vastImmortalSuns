# Ben Jenkins

Full-stack software engineer in Seattle. Seven years of production work: four at Liberty Mutual Insurance (2019–2023, full-stack and then data engineering), and since 2023 running [Ben Jenkins Design](https://benjenkinsdesign.org), where I build and run client platforms end to end.

[benjenkinsdesign.org](https://benjenkinsdesign.org) · [LinkedIn](https://www.linkedin.com/in/benjamin-jenkins) · benjenkinswebdesign@gmail.com

**What I work in:** TypeScript and JavaScript, React and Next.js, Node, Python, C# and .NET, Java. Postgres, MySQL, SQL Server, DynamoDB. AWS and Supabase. The OpenAI and Anthropic APIs, retrieval-augmented generation, and evaluation harnesses for LLM features. Payment, accounting and shipping integrations.

## Work you can open

### Preachly — [platform.preachlyai.com](https://platform.preachlyai.com/)

Principal Software Engineer, 2026 – present. A research and sermon-preparation platform for pastors: an AI research assistant grounded in a large theological corpus, a "librarian" over each pastor's own sermons, generated study materials, and an atlas of churches, sermons and podcasts. Subscription SaaS with billing and an admin back office.

- **How it works:** answers come from retrieved sources, not from a model's memory. Hybrid search runs over a corpus of hundreds of thousands of sermon transcripts and tens of thousands of other works; several models from two providers each take the job they measured best at for the cost; and every quotation is checked against its source text on the server before it reaches the reader.
- **Evaluation:** a four-layer harness run against production (retrieval, tool selection, end to end, faithfulness), about 600 checks, with a per-claim faithfulness judge and a CI gate that fails on regression.
- **Size:** about 198,000 lines, 79 edge functions, 79 Playwright suites.
- Source is private (business code).

### SRF Orders — [srforders.com](https://srforders.com)

B2B wholesale ordering platform for Silk Road Fibers (JL Canvas Co.), live since August 2026. A solo build. Retailers browse the catalog, order, and pay by card on file or on terms; staff run fulfilment, inventory, billing and accounts; the accounting system stays the system of record, synced both ways.

- **Integrations:** QuickBooks Online (OAuth, two-way sync of customers, products and pricing, invoice and payment push, inventory adjustments), Square (card on file, ACH, refunds, a nightly settlement check), ShippingEasy (signed requests, labels, costs read back into the invoice), transactional email.
- **Quality:** 618 tests run against a real database and the accounting vendor's sandbox. Mutation testing gates every inventory-touching push. 43 production deploys in the first 103 days.
- **Size:** about 42,000 lines of application code.
- Source is private (client code).

### benjenkinsphotos.com — [benjenkinsphotos.com](https://benjenkinsphotos.com)

My photography portfolio: a landing page and three generated gallery pages holding 273 photos from Istanbul, Edinburgh and France. Static, no framework, no build step, no third-party JavaScript.

- Vanilla JS, about 870 lines: View Transitions API for the click-to-enlarge morph, IntersectionObserver reveals, pointer-event swipe. CSS container queries, CSS trig for the hero wheel, 3D transforms for the project shelf.
- Three WebP tiers per photo with Display P3 to sRGB conversion. The Istanbul gallery went from about 49 MB loaded eagerly to about 1.5 MB to first paint. Landing-page JS went from about 65 KB (jQuery, AOS, GSAP) to 7.1 KB with no dependencies.
- Python and Pillow generate the images and pages; Hostinger deploys from `main` on every push.

### Client websites

[silkroadfiber.com](https://silkroadfiber.com) · [happystitchingco.com](https://happystitchingco.com) · [ridingsresidential.com](https://ridingsresidential.com) · [lb-nurseries.com](https://lb-nurseries.com) · [dischbuilt.com](https://dischbuilt.com) · [skagithandyman.com](https://skagithandyman.com) · [touchstoneelectrical.com](https://touchstoneelectrical.com) · [dclivepro.com](https://dclivepro.com) · [cliff4ld1.com](https://cliff4ld1.com) · [iramcbee.com](https://iramcbee.com)

The last two are Washington State legislative campaign sites, built in 2026.

I've also run SEO for three of them for more than a year each: each reached the first page of Google within a month, then grew traffic by roughly 10–15% month over month.

## Working with AI models

I've put more than 1,000 hours into building with OpenAI's and Anthropic's models, GitHub Copilot and Lovable. Preachly is where that shows: models chosen by measurement rather than by default (a cheaper model lost its judging job after agreeing with the baseline on under a third of verdicts), structural fixes where a better model would only make a failure rarer, and an evaluation harness so every prompt and model change is compared run against run. The photography site above was built and shipped with Claude Opus 5 and 5.5.

## Before 2023

**Liberty Mutual Insurance, Seattle (2019 – 2023).** Full-Stack Software Engineer, then Data Engineer. Built employee-facing applications on the company's global database, used by roughly half its employees, and data pipelines (Python, AWS Lambda, Step Functions, DynamoDB, SQL Server) that moved protected insurance data across the business 250% faster than the previous process. A six-person Seattle team paired with a team in Ireland.

**B.A. in Computer Science, Seattle Pacific University, 2020.** I've mentored about ten SPU computer science students since.

## About the repositories below

The public repositories on this profile are student projects from my time at SPU. Everything above is private because it's client or business code; the contribution graph is where that work shows.
