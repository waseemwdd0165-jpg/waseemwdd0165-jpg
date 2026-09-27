<h1 align="center">Waseem Ahmad Ansari</h1>

<p align="center">
  <b>Senior Software Engineer</b> &nbsp;·&nbsp; <b>AI &amp; LLM Quality Evaluator</b> &nbsp;·&nbsp; <b>Search Evaluator</b>
</p>

<p align="center">
  I build software and I judge software.<br>
  Nine years shipping applications, seven years evaluating the search and AI systems that decide what people find.
</p>

<p align="center">
  <a href="https://waseemwdd0165-jpg.github.io"><img src="https://img.shields.io/badge/Portfolio-waseemwdd0165--jpg.github.io-0b7285?style=for-the-badge" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/waseem-ahmad-ansari-bba5771ab/"><img src="https://img.shields.io/badge/LinkedIn-Waseem%20Ahmad%20Ansari-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:waseemwdd0165@gmail.com"><img src="https://img.shields.io/badge/Email-waseemwdd0165%40gmail.com-c92a2a?style=for-the-badge" alt="Email"></a>
</p>

<p align="center">
  <i>Mumbai, India (IST) &nbsp;·&nbsp; working remotely</i>
</p>

---

## Play something right now

No install, no account, no sign-up. Open a link, send the code to a friend, and you are playing.

### [Chalk Runner](https://chalk-runner.waseemwdd0165.workers.dev/) &nbsp;<sub>one step ahead</sub>

Two players on a blackboard. **One draws the ground, the other runs on it and never stops.** Chalk runs out and only works near the runner, so the drawer is always one line behind. Walls, low roofs and no-chalk gaps force ramps and jumps.

The server owns the runner and every line, thirty times a second, so both screens show the same run and a modified browser cannot draw itself a shortcut. A dropped connection freezes the round and holds the seat for twenty five seconds. Everyone in the world gets the same level each day, from one seed.

<sub>Canvas · Web Audio · WebSockets · Cloudflare Durable Objects · 220 server checks, 54 browser checks, and a harness that plays sixty rounds by itself</sub>
&nbsp;·&nbsp; [source](https://github.com/waseemwdd0165-jpg/waseemwdd0165-jpg.github.io/tree/main/chalk-runner)

### [Pitch Black](https://pitch-black.waseemwdd0165.workers.dev/) &nbsp;<sub>a stealth game played in the dark</sub>

One hunter, everyone else runs for the exit, and whoever is caught joins the hunt. **Every device renders the same maze from its own player's torch**, so two people sitting in one room see almost nothing in common.

A browser cannot be trusted to keep a secret, so the server holds the map and works out per player exactly what their torch reaches, and sends only that. Opening the console gives nothing away. Line of sight is DDA grid traversal, after an earlier fixed-step raycast was caught leaking players through diagonal wall corners.

<sub>Canvas · Raycasting · WebSockets · Cloudflare Durable Objects</sub>

### [Sunday Park](https://sunday-park.waseemwdd0165.workers.dev/) &nbsp;<sub>a shared voxel amusement park</sub>

No room code and no lobby. **Open the link and you are standing at the gate with whoever else is online.** Ride the big wheel, the carousel and the swings, pop balloons for tickets, or get lost in the mirror maze.

The server publishes each ride's angle and assigns riders to seats, so a rider is always in a car rather than floating beside it. Terrain and trees are instanced meshes and textures are 16 pixel canvases, so the whole world arrives as code rather than assets.

<sub>Three.js · WebSockets · Cloudflare Durable Objects</sub>

### [Human or Machine?](https://waseemwdd0165-jpg.github.io/human-or-machine.html) &nbsp;<sub>a party game about spotting AI writing</sub>

Three to eight players read the same response and vote on whether a person or a model wrote it, then the reveal explains what gave it away. My day job turned into something a group can play in ten minutes. Peer to peer over WebRTC, so there is no server behind it at all.

---

## Evaluating AI, day to day

Seven years of this, for TELUS Digital, DataAnnotation, Mindrift, Alignerr and Handshake AI.

**Project Boson** — Handshake AI, current. Blind comparisons of agentic coding models: the same task run through a terminal agent under two arms, judged without knowing which model produced which. Backend and ML/data domains. The job is reading what the agent actually did, not whether the final answer looks right.

**Project Dynamo** — Handshake AI, 97 tasks. Authoring the terminal tasks these agents are tested against: original scenarios with their own environment, a verifiable solution, quality rules and calibrated difficulty. Writing one that a strong model fails *for the right reason* is the hard part.

Alongside that: RLHF response ranking and preference data, red teaming for unsafe and policy-violating output, hallucination and factuality checking, prompt engineering and SFT data authoring, search and ads relevance rating, and multilingual evaluation across English, Hindi, Urdu and Marathi.

---

## Tools built out of that work

Four browser tools, each one a loop I actually run, on sample data. No API key, no server, no build step.

| Tool | What it demonstrates |
| --- | --- |
| [LLM Response Evaluator](https://waseemwdd0165-jpg.github.io/llm-evaluator.html) | Side by side rubric scoring, forced preference choice, agreement against gold labels, JSONL export — the RLHF preference-data loop |
| [Search Relevance Rater](https://waseemwdd0165-jpg.github.io/search-rater.html) | Needs Met and Page Quality against written guidelines, keyboard driven, CSV export, including a YMYL query |
| [Prompt Testing Workbench](https://waseemwdd0165-jpg.github.io/prompt-workbench.html) | Three prompt versions against a fixed test set, scored by automatic checks, including a prompt-injection case |
| [Text Annotation Tool](https://waseemwdd0165-jpg.github.io/annotation-tool.html) | Span labelling for NER data with live inter-annotator agreement against a gold standard |

---

## Stack

![Python](https://img.shields.io/badge/Python-3776ab?style=flat-square&logo=python&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512bd4?style=flat-square&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET%20Core-512bd4?style=flat-square&logo=dotnet&logoColor=white)
![Java](https://img.shields.io/badge/Java-e76f00?style=flat-square&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599c?style=flat-square&logo=cplusplus&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=flat-square&logo=css3&logoColor=white)

![Oracle](https://img.shields.io/badge/Oracle-f80000?style=flat-square&logo=oracle&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479a1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQL](https://img.shields.io/badge/PL%2FSQL-336791?style=flat-square)

![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-f38020?style=flat-square&logo=cloudflare&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ed?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-f05032?style=flat-square&logo=git&logoColor=white)

---

## Experience

**AI &amp; LLM Quality Evaluator · Search Evaluator · Localization Analyst** — Freelance &amp; Contract · *Jan 2018 – present · remote*

**Senior Software Engineer** — Net Tech Services India Pvt. Ltd, Mumbai · *Jan 2017 – Mar 2025*

Contributed to the nationwide **Cheque Truncation System (CTS)** rollout for core banking, a regulated, high-availability environment where a failed deployment stops branch operations. Designed, built and shipped applications, websites and mobile apps for clients from architecture through deployment. Led front-end and back-end integration, ran functional and non-functional testing that cut the defect rate reaching production, and mentored junior developers on coding standards.

**Support Executive Officer** — Net Tech Services India Pvt. Ltd · *Jan 2016 – Dec 2016*

---

## Education

**B.E. Computer Engineering** — University of Mumbai, Rizvi College of Engineering
<sub>Examination May 2015 · Convocation January 2017</sub>

---

<p align="center">
  <sub>Open to remote full-time, contract and freelance work.<br>
  <a href="mailto:waseemwdd0165@gmail.com">waseemwdd0165@gmail.com</a> &nbsp;·&nbsp; +91 92703 04741</sub>
</p>
