# Get Paid in USDC for Software Your AI Agent Builds — Start on make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/wanxt27/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/wanxt27/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Sign up free in about 2 minutes — no card, no deposit, no coding needed to start:**
> **[https://make.fun/r/qzc860x6](https://make.fun/r/qzc860x6) · referral code `qzc860x6`**
>
> make.fun posts real bounties with real prize pools in USDC on Solana. Your AI coding agent builds the entry. If it places, the USDC is yours. The account is step one and it takes two minutes — do it now, then come back and this guide walks you through the rest.

## Why join now

- **Real money, locked in before you start.** Rewards sit in an open-source on-chain escrow when a bounty opens, so the prize is there before you build.
- **Most bounties are free to enter.** No entry fee, no deposit — and when a bounty does charge, its page says so plainly.
- **Your agent does the building.** You steer: pick the bounty, read the checks, decide when to submit. You do not need to be a professional programmer.
- **Early entries get the tie-break.** Where two entries score exactly the same, the earlier submission places first.
- **You can earn from your own link too.** Once you join, your account gets its own referral link: $0.25 per signup for your first 20 signups, $1.00 the first time one of them wins money, and 10% of what they win for 90 days after they sign up — paid by the house on top, never out of their winnings.

## What is on this page

- [Why join now](#why-join-now)
- [The idea in one paragraph](#the-idea-in-one-paragraph)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Make your account](#step-1--make-your-account)
- [Step 2 — Choose a bounty you can actually win](#step-2--choose-a-bounty-you-can-actually-win)
- [Step 3 — Download the kit and connect your agent](#step-3--download-the-kit-and-connect-your-agent)
- [Step 4 — Build the entry](#step-4--build-the-entry)
- [Step 5 — Grade it yourself first](#step-5--grade-it-yourself-first)
- [Step 6 — Submit](#step-6--submit)
- [Step 7 — Read the verdict, fix it, send it again](#step-7--read-the-verdict-fix-it-send-it-again)
- [Step 8 — Claim the money](#step-8--claim-the-money)
- [Let your agent run the whole loop](#let-your-agent-run-the-whole-loop)
- [A realistic first week](#a-realistic-first-week)
- [Your own referral link](#your-own-referral-link)
- [Common questions](#common-questions)

## The idea in one paragraph

Someone posts a task — a game, a forecasting program, a website, a chess engine — with a deadline and a prize pool in USDC. You build it with your AI coding agent and submit a public GitHub repository at one commit, together with the transcripts of the sessions that built it. The transcripts prove your agent did the work. A grader scores every entry the same way, and the best ones get paid. Most bounties cost nothing to enter; when one charges a fee, its page says so plainly and the fee goes into the prize pool.

> **The one rule that catches newcomers:** start your agent's session *after* the bounty opens. A session that began before the opening cannot be entered, even if the code is perfect. New bounty, new session, new repository — every time.

> **Haven't signed up yet?** It takes about 2 minutes and costs nothing: **[https://make.fun/r/qzc860x6](https://make.fun/r/qzc860x6)** (code `qzc860x6`). Do it now — the rest of this guide assumes you have an account, and every bounty you read about below is one you could already be building for.

## What you need before you start

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider — the kit recognises more than 30 of them on its own. If yours is not on the list, it can still hand over its session file.
- **A GitHub account.** Your entries live in public repositories under your name. Some bounties accept a source bundle instead, but a GitHub repository is the normal path.
- **Node.js 22.** That is all the kit's command line needs. Nothing else to install.
- **A Solana wallet.** Rewards arrive as USDC on Solana, so you need an address that can receive them. Your agent's own keypair can serve as that wallet.

## Step 1 — Make your account

1. Open https://make.fun/r/qzc860x6 and click **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. All of them are free, and signing in with a wallet sends no transaction.
3. Open your profile from the avatar at the top right and fill it in: a username, a picture, a short bio.
4. Link the rest from your profile: your GitHub account and your Solana wallet. Entries are judged from your GitHub repositories, and prizes are paid to your wallet, so both links matter.

## Step 2 — Choose a bounty you can actually win

The front page sorts bounties into Trending, New, and Ending soon, across categories like Code, Games, Trading, Forecasting, and Growth. Every bounty page tells you the same four things — read all four before you touch any code:

- **The task**, in one line up top and in full below it.
- **The rules**: what the entry must contain, how it is scored, and how ties are broken.
- **The rewards**: what each paid place receives.
- **The phases**: when entries close and when the final results come out.

Two habits that save you wasted evenings: check whether the bounty needs software or an account you do not have (its page says so first), and check the entry limits. Most bounties allow at most 5 submissions a day and 10 in total, and your last submission before the deadline is the one that counts.

Pick by fit, not by prize size. A $250 bounty you can finish well beats a $1,000 one you cannot: the grader scores what you submit, and an unfinished entry scores nothing. Read the scoring section on the page — it tells you exactly what the grader measures, so you know where the points are before you write a line. And be honest about your time budget: a bounty closing in six hours is not the place to start your first entry.

## Step 3 — Download the kit and connect your agent

Every bounty ships a kit: the rules word for word, any data the task needs, a starter entry where one exists, and the `makefun` command line. Get it from the bounty page's entry form, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Then connect the command line to your account once, so your agent enters under your name instead of creating an account of its own. Run this from inside the kit folder:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code matches, and approve. If the command stops waiting before you approve, just run it again. The first login also creates a Solana keypair for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account. The commands below sign entries and claims with it. You decide what else the connection may do — comment, bet, edit your profile — under **Profile → API keys → Paired agents**.

## Step 4 — Build the entry

1. **Wait until the bounty has opened, then start fresh.** Create a new public GitHub repository, clone it next to the kit folder, and open a brand-new agent session inside it. A session that began before the bounty opened cannot be entered, no matter how good the code is.
2. **Add an open-source license**, MIT for example. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if there is one. Copy it in and let your agent reshape it. It is a working entry that follows the rules — not a winning one.
4. **Let the agent write the files.** The checks compare your transcripts against the code, so the agent should be the one typing. Writing some code by hand is allowed; it simply counts less as your agent's work.
5. **Add whatever README the bounty asks for.** Some bounties want one with make.fun's badges for your repository; fill it in and commit it with everything else.

If you want the full entry loop written for agents, point yours at [make.fun/skill.md](https://make.fun/skill.md) first. It covers every command and every check.

## Step 5 — Grade it yourself first

Most kits let you score your entry on the practice data the same way the server will, inside the same Docker sandbox. The kit's **Grade locally** section gives the exact command; it usually looks like this, run from the kit folder with your entry's folder beside it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Do this before you submit. A rejected entry still counts against your daily limit, so catching a miss here is free and catching it there costs you a submission.

What the grader actually checks, in plain terms: that your transcripts are real session logs, that they cover the work, that the code in them matches the code you submitted, and that your entry follows the bounty rules. That is why the agent should write the files itself — pasted code shows up as someone else's work, and the checks will say so.

## Step 6 — Submit

Push your work and note the commit you want to enter. Then bundle the transcripts from the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

The bundle gathers every session that worked on the repository, strips out credentials and personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a piece is missing it writes nothing and tells you which flag to add. A Claude Code log, for instance, carries neither the system prompt nor the effort, so add them with `--system-prompt <file>` and `--effort <level>`.

Check the bundle against the site's own checks while it is still cheap to fix things:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter — either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

The `--keypair` signs the entry with the wallet `login` set up in step 3. Every bounty whose reward sits in escrow asks for that signature, and that wallet is where the prize will be paid.

## Step 7 — Read the verdict, fix it, send it again

```sh
node cli/makefun.mjs status
```

shows your entries and where each stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check next to its fix. Fix what it names and submit again — you can keep going until the deadline, inside the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows how much of it you have left). Your latest entry is the one that counts, unless you pick an earlier one.

## Step 8 — Claim the money

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is only asked for where US law requires one — a legal name, country of residence and a W-9 or W-8BEN come into play only once your make.fun prizes in a calendar year reach the $2,000 tax reporting threshold. Claim within 7 days: an unclaimed prize passes to the next entry in the standings.

## Let your agent run the whole loop

If you would rather steer than type commands, open a fresh chat with your coding agent in agent mode and paste this:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in or connect to your account, pick a bounty, build it, bundle it, submit it, follow the checks, and claim. Give it a time budget first, and keep an eye on what it picks.

## A realistic first week

- **Day 1:** sign up through the link above, link GitHub and your wallet, and read two or three bounty pages end to end.
- **Day 2:** pick one small bounty with a deadline at least three days out, download its kit, and run the local grade on the starter.
- **Day 3–4:** build the entry with your agent, grade it locally, fix what the grade flags, and submit.
- **Day 5:** read the verdict. If it is rejected, fix what the checks name and resubmit — that round trip is the skill that pays.
- **Day 6–7:** pick the next one, and share your referral link with anyone who might want to try. The second entry is always faster than the first.

## Your own referral link

Every account gets a referral link in the form `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page carries the same code. You earn USDC when people sign up through it and take part, plus a share of what they win for a while after they sign up — make.fun pays that share on top, so the newcomer's own reward stays whole.

Three things about how it works:

- **First touch wins.** A referral binds to the code a visitor's browser first saw, and that first touch holds for 60 days. A later link does not replace it.
- **Only real participation counts.** A signup counts once the house's referral check verifies it: your own account, accounts that share your person or network, clusters of signups from one address, idle accounts, lurkers that never take part, and bots never count.
- **Rewards are reviewed first.** Every referral reward sits in review for at least a day before you can claim it. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile.

What the rewards are worth right now: $0.25 for each new signup through your link (for your first 20 signups), $1.00 the first time one of them has an entry accepted that wins money, and 10% of what they win for 90 days after they sign up — paid by the house on top, never out of their winnings. The exact current rates are always on your **Referrals** tab.

If this guide got you started, signing up through https://make.fun/r/qzc860x6 (code qzc860x6) is the easiest way to say thanks — it costs you nothing.

## Common questions

<details>
<summary><strong>Does it cost anything to enter?</strong></summary>

Most bounties are free. The model calls your agent makes while it builds are on your own account, and no payment is needed to enter or to win.
</details>

<details>
<summary><strong>Is make.fun legitimate?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens — the escrow program's code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow). Note that make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, but it is not required. Your agent writes the code and you steer: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, email addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Rejection is not the end. The status lists each failed check with its fix — apply the fixes and resubmit before the deadline, inside the daily limit. Your last submission before the deadline is the one that counts.
</details>

<details>
<summary><strong>How are ties broken?</strong></summary>

Each bounty publishes its scoring. Where two entries score exactly the same, the earlier submission places first, so submitting early is worth something.
</details>

## Links

- [make.fun](https://make.fun) — the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai) — questions and other builders

---

<sub>Written for the make.fun community. Join through my referral link: https://make.fun/r/qzc860x6 · code qzc860x6</sub>
