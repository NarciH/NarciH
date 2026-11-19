# Fraud and return-abuse detection that explains every decision

**Live demo: coming soon.**

## The problem

An online store loses money twice: to stolen cards and fraud rings at checkout, and to return abuse afterwards (wearing a dress for the weekend and returning it, or claiming a parcel "never arrived"). Blocking too much loses good customers; reviewing everything by hand is too expensive. The team needs a score they can act on, and a reason they can trust.

**Mercado Aurora** is a fictional online store (electronics, home, fashion). The project simulates a year of realistic activity, about 80,000 orders plus a Black Friday month, with documented fraud and abuse patterns.

## What it does

- Scores every **payment** and every **return**, and gives the **three reasons that pushed the score the most**. Example: a 1,899 EUR electronics order from an account opened yesterday, shipping to an address four other accounts used this month, scores 0.99, and the first reason shown is "accounts at the same address".
- Sets the line between "let it through" and "send to review" from **money, not accuracy**: the cost of a manual review against the cost of a missed case.
- Learns again with new data and **only replaces the current model when the new one is better**.

## Results (measured on the simulated data; test set = the last ~7 weeks)

| | Payments | Returns |
|---|---|---|
| Events in the test set | 12,000 (1.15 % fraud) | 1,556 (4.8 % abuse) |
| Share sent to manual review | 1.7 % | 14 % |
| Fraud or abuse caught | 64 % | 88 % |
| Expected cost per 1,000 events | 1,725 → **676 EUR** | 2,853 → **775 EUR** |

On payments the model ties a simple baseline overall but is better where reviewers work, at the top of the list (63 % vs 57 % of fraud caught at 80 % precision). On returns it gains the most (0.529 vs 0.438 on the standard ranking metric), because abuse depends on combinations of signals that a simple model cannot see. Return abuse is never caught at 80 % precision, so returns stay a review queue, not an automatic block.

**Built with** gradient-boosted trees and per-decision explanations, on Google Cloud.

*The source code is private. Happy to show it working in a call.*
