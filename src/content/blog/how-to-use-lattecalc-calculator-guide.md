---
title: "How to Use the LatteCalc Opportunity Cost Calculator: A Complete Walkthrough"
description: "A field-by-field walkthrough of the LatteCalc calculator — what each input does, how the math works behind the scenes, and how to read every number in your results."
pubDate: 2026-11-11
---

## What This Calculator Actually Answers

The [LatteCalc calculator](/) answers one specific question: if you took a recurring expense and converted it into Bitcoin instead, how much BTC would you have accumulated, and what might that position be worth at a future date under a given growth assumption? It is not a price predictor, a trading signal, or a guarantee — it's a structured way to see the scale of an opportunity cost that's normally too spread out across small purchases to notice.

## Section 1: The Spend

**Habit name (optional).** A free-text label — "Daily Coffee," "Lunch Out," whatever you're evaluating. This only affects the wording of your results and share text; it has no effect on the math.

**Amount per purchase.** The fiat amount of a single instance of the habit — $5 for a coffee, $15 for a lunch, whatever applies. The currency selector next to this field supports USD, KRW, JPY, EUR, GBP, CAD, AUD, SGD, HKD, AED, and INR; switching currencies automatically converts your entered amount using live exchange rates so the underlying dollar value stays consistent.

**Frequency.** Choose Daily, Weekly, Bi-Weekly, Monthly, or Once. This determines the multiplier applied to your amount: Daily uses 365 purchases/year, Weekly uses 52, Bi-Weekly uses 26, Monthly uses 12, and Once treats your entered amount as a single, non-recurring purchase rather than a scheduled habit.

## Section 2: The Future

**How far ahead? (1–40 years).** A slider controlling your projection horizon. The target year updates live as you move the slider, so you can see exactly which calendar year your projection lands on.

**Current BTC Price.** This field auto-populates from a live CoinGecko API price feed, refreshed automatically every 60 seconds, with a manual refresh button (↻) if you want to force an update. You can also type in your own value — useful if you want to test a hypothetical entry price rather than today's actual price. Once you manually edit this field, the calculator stops auto-overwriting it, so your custom value sticks until you reload the page.

**Expected Annual Return (CAGR).** This is the single most important assumption in the entire calculator, and it's presented as four selectable scenarios rather than one number, specifically to avoid implying false precision:

| Scenario | CAGR | What It Represents |
|---|---|---|
| Bear | 15% | A conservative, below-historical-average growth assumption |
| Base | 21% | A moderate assumption, roughly in line with many diversified-asset long-run benchmarks |
| Bull | 35% | An optimistic assumption closer to some of Bitcoin's own longer-run historical averages |
| Hyperbull | 55% | An aggressive assumption reflecting Bitcoin's most favorable historical multi-year stretches |

You can also drag the underlying slider (5% to 60%) to any custom value between these presets — selecting a preset button snaps the slider to that exact value, while manually dragging the slider shows you which named range you're closest to.

A full explanation of how these four tiers were chosen, and how to pick one that matches your own assumptions, is covered in [Bear, Base, Bull, Hyperbull: Understanding the Four Growth Scenarios](/bear-base-bull-hyperbull-scenarios-explained).

## Section 3: Reading Your Results

After clicking **Calculate the Cost**, the results section expands with several distinct blocks:

**The Verdict Card** gives you the headline number — your total projected portfolio value by the target year — alongside your total amount spent and the return percentage compared to what you put in.

**The Breakdown List** gives you the components behind that headline number:
- *Total [Currency] Out* — your actual cumulative spend over the chosen horizon.
- *BTC Accumulated* — the actual amount of Bitcoin your spend would have purchased, shown in both BTC and satoshis (sats), based on the BTC price you entered.
- *BTC Price in [target year]* — the projected future price implied by compounding today's entered price at your selected CAGR.
- *Portfolio Value* — your accumulated BTC multiplied by that projected future price.
- *Return on Spend* — the percentage gain or loss of the projected portfolio value versus your total cash spent.
- *Sats per [Currency] Spent* — a reference figure showing how many satoshis your money buys at the current price, useful for comparing purchasing power across different entry points.

**The Share Section** generates ready-to-post text summarizing your result, with a direct "Post to X" button and a copy-to-clipboard option.

## A Worked Example

Enter "Daily Coffee," $5, Daily frequency, a 10-year horizon, and select the Base scenario. The calculator will show your total spend (~$18,250), the BTC that amount would purchase at the current live price, and the projected portfolio value 10 years out at a 21% CAGR. Switch to Bear and then Bull without changing anything else, and compare how much the projected outcome range shifts — that comparison is more informative than any single scenario's number in isolation.

## Understanding the "Once" Frequency Option

Most of the frequency options (Daily, Weekly, Bi-Weekly, Monthly) model a recurring habit multiplied across your chosen time horizon. The "Once" option behaves differently — it treats your entered amount as a single, one-time purchase rather than a recurring schedule, which makes it the right choice for modeling a lump-sum decision (like "what if I put a $5,000 bonus into Bitcoin instead of spending it") rather than a habitual, repeated expense. Switching between a recurring frequency and "Once" is a useful way to compare "small amounts repeated often" against "one larger amount invested a single time," since both scenarios use the same underlying CAGR projection math, just applied to a different spending pattern.

## Why the BTC Price Field Matters More Than It Looks

It's easy to skip past the BTC Price field since it auto-fills with a live price, but it quietly controls a meaningful part of your result. Because the calculator computes "BTC Accumulated" as your total spend divided by this price, a higher entered price produces less accumulated BTC for the same dollar amount, and a lower entered price produces more. This is worth testing deliberately: try entering a historically low price (say, a price from a past bear-market low) versus the current live price, holding everything else constant, to see how dramatically the BTC Accumulated figure shifts. This isn't a flaw in the tool — it's an accurate reflection of how much a given dollar amount actually buys at different points in Bitcoin's price history, and it's exactly the dynamic that makes buying consistently through both high and low prices (dollar-cost averaging) different from a single lump-sum purchase at one specific price point.

## Using the Share Feature Responsibly

The generated share text includes your specific inputs and projected outcome, formatted for posting on social media. Because the projection depends entirely on your selected CAGR scenario — which is an assumption, not a fact — sharing a Hyperbull-scenario result without that context can create a misleading impression for anyone who sees the post without understanding how the number was generated. If you do share a result, including which scenario you selected (Bear, Base, Bull, or Hyperbull) gives the number appropriate context for anyone reading it.

## Where to Go Next

If you want to compare a recurring-purchase strategy (DCA) against a single lump-sum investment using real historical price data instead of a projected CAGR, use the [DCA vs Lump Sum tool](/dca-vs-lumpsum). For a longer-range financial-independence view built around milestone tracking, see the [Freedom Planner](/freedom).

---

*Not financial advice. All projections are hypothetical and for educational purposes; actual results will differ from any scenario shown. — Hyunsu Park (Crypto SOO)*
