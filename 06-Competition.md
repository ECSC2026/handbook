The event features three separate competition days played on-site. The first competition day (Tuesday) is a Jeopardy-style CTF competition. On Wednesday, there will be a new format: CTF-Unplugged. It is not included in the main score. The final competition day (Thursday) contains the Attack/Defense CTF competition.

## 6.1. Setup

The CTF infrastructure will be hosted in the cloud. The participants will connect to the cloud using infrastructure prepared by the organizers on-premises.

Each team has its own table in the game arena. Each table has a switch, which has at least 12 Ethernet ports available (i.e., excluding ports already used by the organizers). ==Each table has at least 12 power sockets available== (“Schuko” / Type F) for a total of at least 3.5 kW power capacity per table. Some of that power will be used for other hardware (e.g., the switch); expect there to be roughly 3 kW available for players.

Team tables may include additional hardware or network devices provided by the organizers for challenges or infrastructural support. This equipment, sourced from the venue, sponsors, or the organizers themselves, must be left on the table at the end of the competition, unless otherwise specified.

Teams can connect to the Internet through Ethernet cables to their switches. Players are expected to bring their own computer, ethernet cables (and adapters, if required). The wired infrastructure has a dedicated uplink of 9 Gbps. Teams have 1 Gbps access to the network per table, but keep in mind that the overall capacity can vary depending on the type of traffic and the routes used, making it difficult to provide an exact estimate. Players must avoid generating excessive traffic; team-specific rate limits can be imposed to limit infrastructure disruptions.

There will be a backup over Wi-Fi.

## 6.2. Day 2: Jeopardy

Day 2 of ECSC 2026 (Tuesday, October 13, 2026) is the Jeopardy competition.

While the competition will follow a typical, modern jeopardy-style CTF with dynamic scoring, the following subsections explore certain aspects of the competition in more detail.

We strongly encourage players, captains, and coaches to carefully read the sections below, but also to familiarize themselves with other jeopardy-style CTF competitions to better understand this format.

### 6.2.1. Schedule

The Jeopardy competition lasts 12 hours. Writeups can be submitted during and up to 10 minutes after the competition.

| Time (CEST) | Event |
|-------------|-------|
| 9:00        | Setup and testing |
| 10:00       | Jeopardy competition starts. Challenges become accessible, flags and writeups can be submitted. |
| 22:00       | Jeopardy competition ends. |
| 22:10       | Writeup submission deadline. |

In case of unforeseen circumstances the schedule can be altered. In such a case, the organizers will inform all teams. Where it would affect the competition length, the exact details of any possible schedule change will be decided by the Jury.

### 6.2.2. Challenges

The approximate number of challenges for the Jeopardy competition will be announced later on. A challenge is considered solved when a player successfully acquires a flag and submits it on the Jeopardy Platform during the competition without breaking any rules.

Unless a challenge's description states otherwise, the flag format matches the following regular expression: `^ECSC\{.*\}$`

Additionally, players are required to upload a writeup for each solved challenge before the writeup submission deadline. A working solver script or exploit is considered a writeup equivalent (must be delivered in a form that can be easily analyzed if needed). Writeups can be minimal (e.g. a copy of the solve script). The purpose is solely to be able to see how the challenge was solved. In some cases, the team handing in the writeup may be asked follow-up questions.


:::warning
Failure to submit a valid writeup before the deadline may result in penalties for the team, as determined by the Jury.

:::

A set of challenges will be published at the beginning of the CTF. Additional challenges will be published during the CTF when the number of unsolved challenges in a category gets low or after some time has passed without a release in the category. The decision will be made by the organizers of the jeopardy CTF in accordance with the mentioned criteria. Some prepared challenges might not be released.

There will be no challenges published after 20:00.

If, during the competition, a challenge is found to have issues, one of the following actions will be taken:

* In case a challenge is deemed fixable, it will be promptly repaired and re-deployed.
* In case a challenge is deemed unfixable, the Jury shall decide whether to remove the challenge or, if feasible, replace it.
* In case a challenge has unintended solution(s), the organizers can prepare a new version without the unintended solution(s) and the Jury can decide to add this challenge to the competition's challenge set.

Given the above, it is possible for the competition to effectively end with fewer or more challenges than initially announced.

### 6.2.3. Challenge hints

While unlikely, challenge hints may be released during the competition. The Jury will make the final decision on whether a hint is issued and on its exact wording.

### 6.2.4. Network setup

No special network setup will be required. There are, however, other network considerations to discuss.

Most importantly, both the Jeopardy platform and all Jeopardy CTF challenges will only be accessible from the local competition network (ethernet link). This means that challenges with server-side components will not accept inbound connections from hosts external to the local competition network unless otherwise specified.

At the same time, selected challenges with server-side components will have internet access and will be able to connect to external hosts. As is typical for CTF competitions, at times players can be expected to operate external servers, be able to set up external domains (DNS), be able to acquire HTTPS certificates, and take similar actions. It may be possible or required to access open ports on your own laptop from a challenge. Whether or not a challenge has internet access will be visible on the platform.

## 6.3. Day 3: Fun Day!

Day 3 of ECSC 2026 (Wednesday, October 14, 2026) is **not** part of the main competition. It will host a smaller experimental game mode: CTF-Unplugged. It will feature a more race-focused style with a separate scoreboard and prize pool. Exact details will follow as soon as the format designs are finalized.

### 6.3.1: CTF-Unplugged

CTF Unplugged will be a multi-round competition. Teams will compete to solve challenges the fastest, in an offline environment on organiser provided laptops. This event does not influence the final winners of ECSC, but will instead have it's own scoreboard and own mention at the awards ceremony. This competition will focus on the ability to solve complex cybersecurity related challenges in a constrained environment, under time pressure.

Note: This is the first time this format is being run, rules are subject to clarification or change in the coming weeks. Some exact numbers are still under discussion based on venue constraints and similar, and will be clarified closer to the event.

* The event is planned to run over 6 rounds. Four qualifying rounds, a Semi-Final, and a Final.
* Each round is planned to last \~50 minutes
* Challenges will be solved from within an environment with no internet access, with tools/software/resources provided by the organisers.
* Teams will be granted access to this environment before ECSC, to familiarise themselves with the available tools.
* Teams will receive points based on how quickly they solve challenges.
* A top cut of teams from the four qualifying rounds will compete in the Semi-Final, and the top overall teams after the Semi-Final will compete in the Final.
* The final placements will be determined solely by performance in the final.

### 6.3.2 Qualifying rounds

There will be 4 qualifying rounds, one for each of Reversing, Pwn, Crypto and Web.

* All ECSC and Guest teams may participate, (up to 40 teams.)
* Each team may select up to two members to collaborate in each round
* Each team will have access to one shared laptop
* A round is planned to last \~50 minutes.
* A round will have 2+ challenges within the niche category of that round. (Pwn/web/rev/crypto).
* A team is finished once all challenges have been solved, or the time expires
* Points are awarded based on challenges solved and time-to-solve

### 6.3.3 Semi Final

Based on the scores from the four qualifying rounds, a top cut of teams will qualify onwards to the Semi Final

* Top [X] teams by points after the four qualifying rounds may participate in the semi final
* The semi final is expected to last \~50 minutes
* Teams will have access to four laptops to share
* Teams may each send up to [X] players to compete
* There will be multiple challenges across a range of categories.
* Teams will be scored based on challenges solved and time-to-solve

### 6.3.4 Finals

Based on overall scores from qualifiers combined with Semi Finals (with higher weighting to semi-final scores), the top [X] teams will qualify for the final.

## 6.4. Day 4: Attack-Defense

The Attack-Defense CTF will take place on October 15, starting at 10:00 with a one-hour setup and testing slot. The CTF itself will start at 11:00 and last for 8 hours, until 19:00.

Attack-Defense CTFs are a type of cybersecurity competition in which participating teams host services and attempt to exploit each other over a shared, private network. The goal of the game is to earn points by stealing secrets stored in your opponents' service instances, and to avoid losing points by preventing your own secrets from being stolen and submitted, all the while keeping the services available and functioning. The team with the most points by the end wins.


:::warning
We will only provide minimal information here. The rest of the information can be found in the Attack-Defense Wiki ([https://wiki.ad.ecsc2026.de](https://wiki.ad.ecsc2025.de)), which takes precedence over this Handbook. This applies to sections 6.4 and 7.2.

:::

### 6.4.1. Schedule

The schedule for the day of the Attack-Defense CTF:

| Time (CEST) | Event |
|-------------|-------|
| 10:00       | Setup Testing Slot starts |
| 11:00       | The Attack-Defense CTF officially begins |
| 12:00       | Network opens and teams can communicate with other vulnboxes |
| 18:00       | Scoreboard freeze |
| 19:00       | The Attack-Defense CTF officially ends |

### 6.4.2. Game Overview

Each team is given root access to one cloud-hosted Linux-based virtual machine that exposes vulnerable services to other teams over a private virtual network.

Over the course of every round, lasting 60 seconds, so-called checkers store text snippets called flags in the services on each team's vulnbox and test their functionality to make sure they are working as intended. Extracting these flags from other teams' services and submitting them to a central flag submission service each round to earn ATK-points is the primary goal of the game.


:::info
**Flag stores**: A checker may store multiple unique flags each round in distinct areas of a service, and there may be more than one intended vulnerability to reach each one.

:::

To incentivize teams to keep their services available to other teams to exploit, a series of checks is performed each round against every service of every team by the organizers' checkers. These tests define the so-called Service-Level Agreement (SLA): the functionality required for a team to earn SLA-points each round.


:::info
**Attack info**: Checkers may provide hints for successfully stored flags to help guide exploits (e.g., the checker’s username). In some cases, this info is crucial to exploiting the vulnerability at all. It can be retrieved via the attack API.

:::

Each round a team receives DEF-points for every service. The number of points earned is highest when the service is unexploited and decreases with the number of other teams exploiting it.

These points combine to calculate the team score using the scoring formula (see section 7.2).

## 6.5. Team Composition

Each team is composed of a maximum of ten and a minimum of five players. Each participant must belong to one of the following groups:

* **Senior**, born from January 1st, 2001, to December 31st, 2005,
* **Junior**, born from January 1st, 2006, to October 12th, 2012.

People who do not fall within this age range are not allowed to participate in the ECSC 2026. Each team can contain up to five senior players; no limitations exist on the number of junior participants.

Reserve players and player substitutions are not allowed.

## 6.6. Communication


:::success
You can join the ECSC 2026 Discord server at <https://discord.gg/mFGwuwp4cg>

This link does not expire. In case of issues, please contact staff by mail at `general@ecsc2026.de`.

:::

As in previous years, ECSC will use the Discord chat platform. Most communication on the competition days is expected to take place on the designated Discord server.


:::warning
Use of the provided Discord server is strongly recommended and is required for certain actions, such as filing formal complaints during the competition.

:::

The Discord server setup, the authentication, and the ticketing system are outlined in section 9 of this document.

Please note that this Handbook is published prior to the competition. As such, changes may still be introduced.

### 6.6.1. Discord Account

To use the Discord platform, it is required to have or create a Discord account. The platform can be accessed using one of the following methods:

* using a modern web browser through <https://discord.com/> (Discord accounts can also be created here),
* using a desktop client available at <https://discord.com/download>,
* or using a mobile client available at <https://discord.com/download>.

Important documents:

* <https://discord.com/privacy> - Discord Privacy Policy
* <https://discord.com/terms> - Discord's Terms of Service

### 6.6.2. Communication Rules

Effective communication between players, coaches and the organization is crucial for the smooth functioning of the competition and the overall event. To ensure clarity and efficiency, it is essential to distinguish between three main communication categories:

* **competition-related communication**, which pertains to the gameplay and technical aspects (e.g., game rules and format, technical issues affecting gameplay, formal complaints or disputes regarding scoring and rankings, reporting possible disruptive behavior from other players within the game, strategic play, ...).
* **event-related communication**, which covers logistics and any other non-competition matters (e.g., issues with meal schedules and dietary needs, health and safety concerns, general inquiries about event logistics).
* **emergencies**, which can cover health and safety issues, but also inappropriate behavior, bullying, discrimination, illegal activities and every other scenario described in the Technical and Human Behavior section (see 6.7).

For all **competition-related communications**, teams can always choose between one of the following options:

* A formal complaint. Every formal complaint must be initially reported through the dedicated ticket bot button to be considered by the jury. Other communication means are not considered valid.
* A proper ticket on the Discord server explaining the issue (e.g., a challenge seems to be not responding, or they need a clarification about the rules), by clicking on the corresponding ticket bot button in the Discord server.
* The team captain requests a meeting with a team coach or vice versa, by writing a message in the dedicated channel on the Discord server, pinging the role watchdog-manager.
  * Meetings must be held in one of the predefined spots (which will be clearly indicated in the game arena); after a meeting is requested, a watchdog handles the meeting request and accompanies the player to the predefined spot.
  * The meeting must always be supervised by at least one watchdog and must be conducted in English.
  * Communication must be limited to non-technical topics. Some examples are:
    * Suggesting priorities
    * Reporting challenge status (but not technical details or hints)
    * Game strategy
    * Raising complaints about unfair behavior from other teams
  * Each team can request up to 8 meetings during each competition day.
  * The maximum duration of a meeting is 3 minutes.
* The team captain speaks directly with a watchdog inside the game arena; in this case, it will be the watchdog's job to decide whether the request should be handled via a ticket through the Discord server or whether it needs to be addressed urgently and immediately. Watchdogs can report urgent or serious issues directly to watchdog managers and/or organizers. Particularly serious situations will be handled case by case.

For all **event-related communications**, people can always choose between one of the following options:

* A participant opens a proper ticket on the Discord server explaining the issue (e.g., a logistical issue in the venue), by clicking on the corresponding ticket bot button in the Discord server.
* The team captain writes a message on the coaches - captains Discord channel (`#captain-coaches-comms`), explaining what they need (e.g., they would like some more snacks).
* A player speaks directly with a watchdog inside the game arena; in this case, it will be the watchdog's job to decide whether the request should be handled via the Discord channel or whether it needs to be addressed urgently and immediately (e.g. a player is not feeling well and needs medical assistance).

In **emergencies**, people should always feel free to communicate any serious issue in whatever way may work best for them. Some examples could be:

* Speak with a watchdog in the game arena or someone from the staff around the venue.
* Open an emergency ticket on the Discord server.
* Directly write on the emergencies dedicated Discord channel.

Generally, follow the communication guidelines described in the Technical and Human Behavior section (see 6.7).

## 6.7. Technical and Human Behavior

Be nice to each other. ECSC is a competitive event, but also an opportunity for teams to learn from each other and have fun. Players should help foster that environment.

### 6.7.1. Fairness and Sportsmanship

It is vital that everyone enjoys the event and leaves with a satisfying experience. Therefore, in addition to anything ruled out by law (and common sense), the following are disallowed, up to the penalty of a ban from the event and venue:

* Any communication about the CTF challenges (e.g. sharing flags, challenge details or solutions) with people outside of the player's own team (players and captain) during the competition itself.
* Giving or accepting assistance from anyone outside the own team and organizers for issues related to the competition is strictly prohibited.
* Interfering with other teams' efforts, e.g. by DoSing, vandalizing public resources (like Wikipedia articles) related to a challenge solution, or similar actions.
* Flag hoarding: refraining from submitting flags after solves, and then submitting them at once near the end of the competition.
* Gathering and/or taking advantage of insider information relating to the competition is prohibited.
* Attacking the infrastructure, other teams or any other third parties is strictly prohibited. This includes any physical infrastructure present at the event locations and also applies outside of the competition hours. All of the targets will be hosted under challenge specific domains, unless otherwise specified in the challenge description.
* Attempting to elicit unintended behavior in any devices or services not designated as challenges for the competition running in the game network is strictly forbidden.
* Physically interacting or digitally tampering with the physical infrastructure provided by the organizers without permission is prohibited.
* Any action with the effect of creating excessive load for the contest or team infrastructure is prohibited, even if such actions are in the interest of the competition.
* Any action with the effect of intentionally making another team’s service unavailable or non-functioning when interacted with by players or the checkers is prohibited.
* The deployment of fake flags is prohibited.
* As stated in Section 6.11, we prohibit LLM usage during the competition. Refer to Section 6.11 for details.

Any unfair behavior with respect to the competition or the other players is forbidden, even if not explicitly described in the rules above; the organizers, the jury and any other relevant authority reserve the right to evaluate each case independently.

When in doubt, please ask (file a Discord ticket).

If you encounter any infrastructure or platform issues, please report them via a ticket on the Discord server and refrain from disclosing them publicly.

### 6.7.2. 0-day Policy

The organizers may disclose any vulnerabilities (including 0-days) used during the competition to the relevant upstream vendor, but they will use their best effort to credit the original finder and coordinate the disclosure process.

## 6.8. Data recording and retention

Please note that various activities, including Discord messages across all channels, competition network traffic, Jeopardy platform usage, and entire Attack-Defense network traffic are recorded and logged. It will be accessed in case of a suspected rule violation.

Any data we record will be deleted within 30 days after the conclusion of ECSC 2026, except for data fragments that may need to be retained for ongoing investigations, if any. Such data will be removed when no longer needed.

## 6.9. Allowed/necessary tools and hardware equipment

### 6.9.1. Software equipment

Every challenge will be solvable using only open source or freely available software. Participants are free to use any software tool they want, including commercial ones, but the organizers will try to ensure they will not give any significant advantage to discourage their use.

### 6.9.2. Hardware equipment

Players are allowed to bring a basic hardware setup: one laptop each, mice, keyboards, power/ethernet/data cables, adapters, external drives, phones, headphones/headsets. The team is allowed to bring up to:

* 1 additional computer (max 300 W total output power as indicated on the charger, e.g., laptop, mini-PC, Raspberry Pi) for hosting internal services. It may not be used as the primary computer to solve challenges.
* 1 externally powered monitor, in total.
* 10 self-contained monitors (without an external power source, e.g., USB monitors) or tablets in total.

No power extenders are allowed except for the ones provided by the organizers.

Cloud resources are not considered "hardware equipment"; therefore, there is no limitation on them. If something is not mentioned in the list above, then teams must request it. This applies to electronics as well as bulky objects that may impede or annoy other teams in the arena. If teams are unsure about something, they should formally request permission in advance.

Each team is required to bring their own ethernet cables to connect their devices to the access switch they have on their table. Teams must also make sure they have all the adapters they need (e.g., in case no ethernet port is present on a laptop).

Each team is required to bring all the power adapters they need. Each table has at least 12 sockets available (type F compatible).

The hardware equipment necessary to solve the hardware challenges is provided by the organizers; players are not allowed to use any additional tool to solve the hardware challenges apart from their laptops and phones or tablets.

Additional equipment must be submitted in advance for approval by the organizers and venue staff.

In case of players' hardware failure, teams can request to substitute a device. The request must be reported to a watchdog and will then be raised to the jury. If the request is accepted, the team coaches can bring a new device to the players and bring the old device outside of the arena.

## 6.10. Penalties and complaints

Individuals or teams breaking one or more rules can receive a warning or a penalty, depending on the seriousness of the situation. Possible penalties apply to rule infringements both during the final event (from the time a team arrives until they depart) and online, at any time.

Penalties will be decided by the jury in the form of:

* Time or point penalties for the team in one or both the competition days, or in the aggregated scoreboard.
* Locking out a team from one or more challenges if the team is performing disruptive actions towards them.
* Temporary or permanent exclusion of one or more team members from the competition.
* In extreme cases, complete disqualification of the team from the competition.

## 6.11. LLM Usage Ban

Usage of LLMs is restricted during the competition. The following section describes which kind of LLM usage is allowed and which is prohibited.

Sometimes it is not clear when a service uses an LLM or it is not easy to turn it off. We still want to provide as much freedom as possible so for there spirit of the competition here is a non exhaustive list of things where we have a clear stance: 

What is prohibited:

* Agentic AI such as Codex or Claude
* LLM-based chats such as ChatGPT
* LLM-based code completion (such as copilot) 
* Expanding (or interacting with) the AI summary of search engines like Google
  * We suggest you may use an extension to disable it
* AI Search (e.g. Google Search in AI mode)

What is allowed for its intended purpose only:

* Translation software such as DeepL
* OCR software

If you are unsure whether a service you want to use is allowed or prohibited, you can always ask the organizers!

## 6.12. Screen Recordings

As an enforcement measure for the LLM ban we aim to create screen recordings during the Jeopardy and A/D CTF competitions. Participants should therefore take care to not expose any private information during the competitions and prepare accordingly. Details about the concrete implementation will follow later on.

Screen recordings will be accessible only to a strictly limited group of people (consisting of the jury and selected members of the watchdog and core organization team) and will be handled with utmost care.

All screen recordings will be kept onsite and will not be uploaded anywhere.