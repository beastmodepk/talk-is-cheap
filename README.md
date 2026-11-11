# 💸 Talk Is Cheap

**Stock tips are free. Track records aren't.**

Talk Is Cheap watches the stock calls made in Instagram reels and posts, writes every
single one down, and then — this is the part the gurus hate — *checks what happened next.*

A creator can delete a bad reel. They cannot delete it from here.

> 🚧 **Status: design phase.** This repo currently holds the design and a front-end
> mock with sample data. No live ratings yet. Scores shown anywhere in this repo
> are illustrative until the tracker is switched on.

---

## 🏆 The Leaderboard

One board to rule the finfluencers:

- **Creators** — every suggester ranked by a rolling score built from their actual,
  tracked picks: hit rate, and how their calls did **against the S&P 500 (VOO)**
  at 1, 5 and 20 days. Tiers: **Follow closely** · **Watch** · **Ignore** · **Unrated**
- **Stocks** — every suggested name, with *who* suggested it, *why*, and how those
  calls are tracking. One stock, seven suggesters? You see all seven — and what each
  of them is worth
- **Today** — new calls logged, picks reaching a checkpoint, tier promotions & demotions
- **Posts** — every post fact-checked and scored for honesty and specificity.
  Said "983%" when it was really 941%? There's a badge for that, and it's not a nice one

Rotating titles keep it spicy: **Leader of the Month**, **Biggest Riser**,
**Most Honest**, **Best Newcomer**. Earned, never bought. There is no sponsored rank,
no pay-to-rank, and no deleting your losers. That is the whole point.

## 🔍 How scoring works

Three levels, all published, no secret sauce:

1. **Post score** (when a call is logged) — fact-check verdict, claim honesty,
   specificity. Named a price level and a reason? Points. Pure hype? Fewer points
2. **Pick score** (automatic, over time) — every pick is measured at fixed checkpoints
   (1 / 5 / 20 days) against VOO. Winners *and* losers. Forever
3. **Creator score** (rolling) — built only from tracked picks, recency-weighted.
   Under ~5 tracked picks you're **Unrated** — one viral call proves nothing

Ratings are **earned forward**: your tier comes from what happens *after* we log
your call, not from a highlight reel of your greatest hits.

On top of that, suggested stocks also get scored by two independent financial
lenses — a catalyst score out of 30 and a street-consensus conviction out of 10 —
so a suggestion is only strong when the *stock* and the *people pushing it* both hold up.

Full methodology lives in the design doc (and will get its own page before launch).

## 🗂️ What's in this repo — and what isn't

This is the **public** repo: the front-end, the leaderboard UI, and the code that
renders it. People are welcome to read every line.

The **data lives in a separate, private repo** — the database of creators, posts,
picks and scores, plus the machinery that collects and scores them. This front-end
reads a published, read-only export from that data repo. The receipts are public;
the kitchen is not.

```
┌────────────────────────┐        read-only export        ┌──────────────────────┐
│  talk-is-cheap-data    │ ─────────────────────────────▶ │  talk-is-cheap       │
│  (private)             │   boards · sheets · scores     │  (public, this repo) │
│  database + scoring    │                                │  front-end + UI      │
└────────────────────────┘                                └──────────────────────┘
```

## 🎯 Want a leadership spot?

Post your calls in public, with specifics — a name, a reason, a level, a timeframe —
and let them be tracked. That's it. That's the application form.
Specific beats loud, honest beats hyped, and a long memory beats a deleted post.

Think we logged one of your calls wrong? There's a dispute route — corrections are
reviewed against the original post and shown openly, never quietly edited.
Don't want to be listed at all? There's an opt-out, too. (Your tier will miss you.)

## ⚠️ Disclaimer

Talk Is Cheap tracks **public statements** and compares them with **public market
data**. Scores describe past calls against a benchmark; they are **not financial
advice**, not an endorsement of any creator as an advisor, and not a recommendation
to buy or sell anything. Do your own research — ideally better than a 30-second reel.

## 🛣️ Roadmap

- [x] Design + leaderboard mock (sample data)
- [ ] Tracker live: calls logged and checkpoint scoring switched on
- [ ] GitHub Pages: public leaderboard, a page per creator and per stock
- [ ] Shareable rank cards — post your receipt
- [ ] Claim your handle (verify it's really you, get the badge)
- [ ] Later, if it earns it: accounts, saved boards, rank-change alerts

---

*Talk is cheap. Proof is not. 💸*
