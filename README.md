<img src="img/banner.png" alt="Waseem Ahmad Ansari - Senior Software Engineer, AI &amp; LLM Quality Evaluator, Search Evaluator" width="100%">

<p align="center">
  <a href="https://waseemwdd0165-jpg.github.io"><img src="https://img.shields.io/badge/Portfolio-0d1117?style=for-the-badge&logo=googlechrome&logoColor=2dd4bf" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/waseem-ahmad-ansari-bba5771ab/"><img src="https://img.shields.io/badge/LinkedIn-0d1117?style=for-the-badge&logo=linkedin&logoColor=2dd4bf" alt="LinkedIn"></a>
  <a href="mailto:Waseemwdd0165@gmail.com"><img src="https://img.shields.io/badge/Email-0d1117?style=for-the-badge&logo=gmail&logoColor=2dd4bf" alt="Email"></a>
</p>

<p align="center">
  Computer Engineer (B.E.) with nine years building software, web, and mobile applications,<br>
  and seven years evaluating the search and AI systems that shape what people find online.
</p>

<p align="center">
  <sub>Based in Malegaon, Maharashtra, India (IST) &nbsp;·&nbsp; Remote &nbsp;·&nbsp; +91 92703 04741</sub>
</p>

---

## What I do

I build software and I evaluate it. Knowing how a search stack or a language
model pipeline is put together makes for sharper judgement of what it produces —
and years of assessing that output against detailed guidelines make for more
careful engineering.

> **Engineering** — application development across desktop, web, and mobile;
> front-end and back-end integration; functional and non-functional QA; Agile
> delivery; mentoring and coding standards.

> **AI &amp; search evaluation** — RLHF response ranking and preference data; red
> teaming for unsafe and policy-violating output; hallucination and factuality
> checking; prompt engineering and SFT data authoring; search and ads relevance
> rating; multilingual evaluation and localization.

---

## Multiplayer games

Real-time games that run in a browser. No install, no account, no app store —
open a link, share the code, and play. All three are server-authoritative on
Cloudflare Workers with Durable Objects, so every player sees the same world and
a modified browser cannot cheat.

| Game | What it is | Built with |
|---|---|---|
| **[Chalk Runner](https://chalk-runner.waseemwdd0165.workers.dev/)** | Two players on a blackboard. One draws the ground, the other runs on it and never stops. Chalk runs out and only works near the runner, so the drawer is always one line behind. Walls, low roofs and no-chalk gaps force ramps and jumps, and everyone gets the same level each day. | Canvas · Web Audio · WebSockets · Durable Objects |
| **[Pitch Black](https://pitch-black.waseemwdd0165.workers.dev/)** | A stealth game played in the dark. One hunter, everyone else runs for the exit, and the caught join the hunt. Every device renders the same maze from its own torch, and the server sends each player only what their torch reaches — so the console gives nothing away. | Canvas · Raycasting · WebSockets · Durable Objects |
| **[Sunday Park](https://sunday-park.waseemwdd0165.workers.dev/)** | A voxel amusement park everybody shares. No room code: open the link and you are at the gate with whoever else is online. Ride the big wheel, the carousel and the swings, or get lost in the mirror maze. Rides are seat-synced from the server. | Three.js · WebSockets · Durable Objects |
| **[Human or Machine?](https://waseemwdd0165-jpg.github.io/human-or-machine.html)** | A room-code party game for 3 to 8. Everyone reads the same response and votes on whether a person or a model wrote it, then the reveal explains what gave it away. My day job, turned into a party game. | WebRTC, peer to peer — no server at all |

---

## Evaluation tools

Tools built out of seven years of rating work. Each one is a loop I actually
run, turned into something anyone can use.

### [inter-annotator-agreement](https://github.com/waseemwdd0165-jpg/inter-annotator-agreement) &nbsp;<sub>Python</sub>

The useful question about two raters is never *how much did they agree*. It is
*which boundary did they disagree on*. So this reports percent agreement,
Cohen's and Fleiss' kappa, and then points at the pair of labels they keep
mixing up and names every item they split on.

In the sample run, one rater sits at 75 to 80 percent on three labels and
**16.7 percent on the fourth** — she calls it by the neighbouring name almost
every time. That is not a careless rater, it is one sentence in the guideline.

No dependencies, standard library only, 30 tests with the kappa arithmetic
worked out by hand in the comments rather than computed by the code under test.

### [eval-sampler](https://github.com/waseemwdd0165-jpg/eval-sampler) &nbsp;<sub>Java</sub>

Forty thousand responses, budget to rate five hundred. Which five hundred? And
then the budget goes up and the obvious fix, redrawing, throws away every rating
already done.

Nothing here is shuffled. Each row gets a sort key from the seed and its own id,
and the sample is the lowest keys in each stratum, so the same seed picks the
same rows on any machine, and asking for 1,200 after rating 500 returns a set
that contains those 500. The quota maths is largest-remainder with a floor, so
the quotas add up to exactly n, no stratum is over-drawn, and the one percent
language still gets looked at.

No build tool and no dependencies: a JDK is the whole toolchain. 28 tests.

### Four browser tools

All run in the browser on sample data — no API key, no server.

| Project | What it demonstrates |
|---|---|
| **[LLM Response Evaluator](https://waseemwdd0165-jpg.github.io/llm-evaluator.html)** | Side-by-side rubric scoring, forced preference choice, gold-label agreement, JSONL export — the RLHF preference-data loop |
| **[Search Relevance Rater](https://waseemwdd0165-jpg.github.io/search-rater.html)** | Needs Met and Page Quality rating against written guidelines, keyboard-driven, CSV export |
| **[Prompt Testing Workbench](https://waseemwdd0165-jpg.github.io/prompt-workbench.html)** | Prompt versions run against a fixed test set with automated checks, including a prompt-injection case |
| **[Text Annotation Tool](https://waseemwdd0165-jpg.github.io/annotation-tool.html)** | Span labelling for NER data with live inter-annotator agreement against a gold standard |

---

## From the banking years

Nine years on the nationwide Cheque Truncation System rollout, written out as
code rather than left on a CV.

### [cheque-batch-validator](https://github.com/waseemwdd0165-jpg/cheque-batch-validator) &nbsp;<sub>.NET 8</sub>

A presentment batch either agrees with its own trailer or it does not settle.
The rule that matters is which records you count: the control total is compared
against every record the file claimed to contain, including the ones validation
threw out and the ones nobody could parse. Compare it against the survivors
instead and a file can drop a record in transit and still balance, which is the
one failure a control total exists to catch.

Four sample batches ship with it, two that settle and two that do not, plus an
xUnit suite over the field rules, both kinds of duplicate, and every way the
control check can fail.

### [plsql-reconciliation](https://github.com/waseemwdd0165-jpg/plsql-reconciliation) &nbsp;<sub>Oracle PL/SQL</sub>

The nightly reconciliation, written twice: the row-by-row cursor it used to be
and the single set-based statement it became. The old one is kept in the
repository on purpose, because a rewrite cannot be judged without the thing it
replaced, and because the worst line in it was not the per-row lookup but the
`COMMIT` inside the loop, which leaves a failed run half reconciled.

The centrepiece is the assertion script. It runs both over the same 200,000 row
batch and fails unless they decide every line identically, down to the wording
of the reason and the ledger id attached, and unless all six verdicts actually
occurred, because an equivalence test over data that never reaches a branch has
not tested it.

Written out from the work and not run since; the README says so plainly and
carries no timings for the same reason.

---

## Writing

Three bugs from Chalk Runner, each one a thing I got wrong and the check that
would have caught it sooner.

| | |
|---|---|
| **[The QR code that round-tripped and still could not be scanned](https://waseemwdd0165-jpg.github.io/writing/qr-code-that-round-tripped.html)** | I wrote the encoder and the decoder, and they agreed perfectly. Both were wrong, because the generator polynomial was built backwards. On testing against the world rather than against yourself. |
| **[Two tabs, one seat](https://waseemwdd0165-jpg.github.io/writing/two-tabs-one-seat.html)** | Reconnect worked on every device I tried, then two tabs on one laptop turned out to be one player. localStorage is scoped to the origin, and my test double was more isolated than the browser. |
| **[Every room had its own global leaderboard](https://waseemwdd0165-jpg.github.io/writing/every-room-had-its-own-global-board.html)** | Each room wrote the record of the day into its own Durable Object, so the board looked right everywhere and was wrong everywhere. With one room, local and global are the same object. |

---

## Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-0d1117?style=flat&logo=python&logoColor=3776ab)
![C#](https://img.shields.io/badge/C%23-0d1117?style=flat&logo=csharp&logoColor=a371f7)
![Java](https://img.shields.io/badge/Java-0d1117?style=flat&logo=openjdk&logoColor=e76f00)
![C](https://img.shields.io/badge/C-0d1117?style=flat&logo=c&logoColor=00599c)
![C++](https://img.shields.io/badge/C%2B%2B-0d1117?style=flat&logo=cplusplus&logoColor=00599c)
![JavaScript](https://img.shields.io/badge/JavaScript-0d1117?style=flat&logo=javascript&logoColor=f7df1e)
![SQL](https://img.shields.io/badge/SQL-0d1117?style=flat)
![PL/SQL](https://img.shields.io/badge/PL%2FSQL-0d1117?style=flat&logo=oracle&logoColor=f80000)

**Web &amp; frameworks**

![.NET](https://img.shields.io/badge/.NET%20%2F%20.NET%20Core-0d1117?style=flat&logo=dotnet&logoColor=a371f7)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-0d1117?style=flat&logo=dotnet&logoColor=a371f7)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-0d1117?style=flat)
![MVC](https://img.shields.io/badge/MVC-0d1117?style=flat)
![HTML5](https://img.shields.io/badge/HTML-0d1117?style=flat&logo=html5&logoColor=e34f26)
![CSS3](https://img.shields.io/badge/CSS-0d1117?style=flat&logo=css3&logoColor=1572b6)
![Three.js](https://img.shields.io/badge/Three.js-0d1117?style=flat&logo=threedotjs&logoColor=ffffff)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-0d1117?style=flat&logo=cloudflare&logoColor=f38020)

**Databases**

![Oracle](https://img.shields.io/badge/Oracle%20(DBA%20%26%20PL%2FSQL)-0d1117?style=flat&logo=oracle&logoColor=f80000)
![MySQL](https://img.shields.io/badge/MySQL-0d1117?style=flat&logo=mysql&logoColor=4479a1)
![MariaDB](https://img.shields.io/badge/MariaDB-0d1117?style=flat&logo=mariadb&logoColor=7d8b9e)
![Stored procedures](https://img.shields.io/badge/Stored%20procedures-0d1117?style=flat)

**Tools**

![Git](https://img.shields.io/badge/Git-0d1117?style=flat&logo=git&logoColor=f05032)
![Docker](https://img.shields.io/badge/Docker-0d1117?style=flat&logo=docker&logoColor=2496ed)

---

## Experience

<table>
<tr><td width="230" valign="top">

**Senior Software Engineer**

Net Tech Services India Pvt. Ltd, Mumbai

<sub>*Jan 2017 – Mar 2025*</sub>

</td><td valign="top">

- Contributed to the nationwide Cheque Truncation System (CTS) rollout for core banking — a regulated, high-availability environment where a failed deployment stops branch operations
- Designed, built, and shipped applications, websites, and mobile apps for clients, from architecture through deployment
- Led front-end and back-end integration; ran functional and non-functional QA
- Mentored junior developers and helped set coding standards across the team

</td></tr>
<tr><td width="230" valign="top">

**AI &amp; LLM Quality Evaluator · Search Evaluator · Localization Analyst**

Freelance

<sub>*2018 – Present*</sub>

</td><td valign="top">

- Rank competing model responses to produce preference data behind RLHF, applying written rubrics consistently at volume
- Red-team models for unsafe, biased, and policy-violating output
- Check model claims against sources to catch hallucinations and fabricated citations
- Evaluate output across multiple languages; test chatbots and voice assistants
- Rate search results and digital ads against quality guidelines

</td></tr>
<tr><td width="230" valign="top">

**Support Executive Officer**

Net Tech Services India Pvt. Ltd

<sub>*2016*</sub>

</td><td valign="top">

- Tested core software products, functionally and for performance and reliability
- Supported application rollouts and contributed to UI development

</td></tr>
</table>

---

## Education

**B.E. Computer Engineering** — University of Mumbai, Rizvi College of Engineering
<br><sub>Examination May 2015 · Convocation January 2017</sub>

---

<p align="center">
  <sub>Open to remote contract and freelance work.<br>
  Reach me at <a href="mailto:Waseemwdd0165@gmail.com">Waseemwdd0165@gmail.com</a></sub>
</p>
