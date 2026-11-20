<a id="top"></a>
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:071A20,55:0B4A57,100:2FB3B8&height=190&section=header&text=Fraud%20Detector&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Scores%20every%20payment%20and%20return%2C%20and%20says%20why&descAlignY=60&descSize=17&animation=fadeIn" alt="Fraud Detector: Scores every payment and return, and says why" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=19&duration=3000&pause=900&color=2FB3B8&center=true&vCenter=true&width=720&lines=64%25+of+payment+fraud+caught%2C+1.7%25+reviewed;Every+score+comes+with+its+top+3+reasons;Review+line+set+by+money%2C+not+accuracy;A+new+model+ships+only+if+it+beats+the+old+one" alt="64% of payment fraud caught, 1.7% reviewed" />

<p>
  <img src="https://img.shields.io/badge/status-live-2FB3B8?style=flat-square" alt="Live" />
  <img src="https://img.shields.io/badge/industry-e--commerce_%C2%B7_payments-0B4A57?style=flat-square" alt="E-commerce payments" />
  <img src="https://img.shields.io/badge/demo_UI-Spanish-557079?style=flat-square" alt="Demo in Spanish" />
  <img src="https://img.shields.io/badge/figures-measured_2026--11--20-0B4A57?style=flat-square" alt="Measured 2026-11-20" />
</p>

<a href="https://ecfraud-api-4y6shrzafa-uc.a.run.app"><img src="https://img.shields.io/badge/%E2%96%B6_Try_the_live_demo-no_sign--up-0B4A57?style=for-the-badge" alt="Try the live demo" /></a>
<a href="#-try-it-in-60-seconds"><img src="https://img.shields.io/badge/What_to_try-60_s-2FB3B8?style=for-the-badge" alt="What to try" /></a>

</div>

## 😣 The problem

An online store loses money twice:

- 💳 **At checkout:** stolen cards and rings of new accounts.
- 📦 **After delivery:** return abuse, like a dress worn for the weekend and sent back, or a parcel that "never arrived".

Blocking too much loses good customers; reviewing everything by hand costs too much. The team needs **a score it can act on, and a reason it can trust**.

## 🧭 What happens to every order

<p align="center"><img src="../assets/cases/ecommerce-ia-fraude-mlops-journey.svg" alt="A payment or return gets a risk score, the score names its top reasons, and only cases worth it go to a person." width="100%" /></p>

> [!TIP]
> The demo sleeps when nobody uses it, so the first request after a quiet period can take up to ~30 s. Everything after that is fast.

## 🧩 What's inside

<table>
  <tr>
    <td valign="top" width="33%"><h3>🎯 One score per event</h3>Every <b>payment</b> and every <b>return</b> gets a risk score from 0 to 1 the moment it arrives.</td>
    <td valign="top" width="33%"><h3>💬 The three reasons why</h3>Each score names what pushed it most, e.g. <i>"accounts at the same address"</i>. Analysts stop guessing.</td>
    <td valign="top" width="33%"><h3>💶 A line drawn by money</h3>The cut-off between <i>let it through</i> and <i>review</i> comes from the cost of a review versus the cost of a missed case, not from accuracy.</td>
  </tr>
  <tr>
    <td valign="top" width="33%"><h3>🔁 Learns, carefully</h3>It retrains on new data and <b>only replaces the current model when the new one is better</b>.</td>
    <td valign="top" width="33%"><h3>🕵️ Two kinds of abuse</h3>Separate scoring for checkout fraud and for return abuse, because they behave differently.</td>
    <td valign="top" width="33%"><h3>📈 Ready for peaks</h3>Tested on a year of activity that includes a Black Friday month.</td>
  </tr>
</table>

## 🔀 How a decision is made

```mermaid
%%{init: {"theme": "base", "themeVariables": {"primaryColor": "#E4F0F1", "primaryTextColor": "#071A20", "primaryBorderColor": "#0B4A57", "lineColor": "#2FB3B8", "secondaryColor": "#FFFFFF", "tertiaryColor": "#F6FAFA", "fontFamily": "Inter, Segoe UI, sans-serif"}}}%%
flowchart LR
    E(["💳 Payment or 📦 return"]) --> S["🎯 Risk score<br/>+ top 3 reasons"]
    S --> D{"Expected loss<br/>more than a review costs?"}
    D -- "no" --> P["✅ Let it through"]
    D -- "yes" --> R["🧑‍💼 Analyst reviews,<br/>reasons in view"]
```

**Example from the demo:** a 1,899 EUR electronics order from an account opened yesterday, shipping to an address four other accounts used this month, scores **0.99**. The first reason: *accounts at the same address*.

## 💼 What your business gets

| | Without it | With the fraud detector |
|:-:|---|---|
| 🚧 | Rules of thumb that block good customers or let rings through | A score per payment and return, tuned to what each mistake costs |
| ❓ | Analysts guess why an order looks odd | Every score names its top three reasons |
| ⚖️ | Reviewing everything, or nothing | Only the cases worth a review reach a person |
| 🧪 | A new model goes live on hope | A new model replaces the old one only when it measures better |

## 🧪 Try it in 60 seconds

1. Open the **[live demo](https://ecfraud-api-4y6shrzafa-uc.a.run.app)**.
2. Choose **Pago** (payment) or **Devolución** (return).
3. Click an example, press **Evaluar** and read the **Por qué** (why) panel.

| Example | What to look for |
|---|---|
| *Red de cuentas nuevas* (a ring of new accounts) | A score near 1 and "same address" among the reasons |
| *Vestido tras el fin de semana* (dress returned after the weekend) | Return abuse flagged, with the reasons behind it |

## 📊 Results

<p align="center"><sub><b>Measured on 2026-11-20 on ~7 weeks of activity the model never saw</b></sub></p>

<table>
  <tr>
    <td align="center" width="25%"><h2>64%</h2><sub>of payment fraud caught</sub></td>
    <td align="center" width="25%"><h2>1.7%</h2><sub>of payments sent to review</sub></td>
    <td align="center" width="25%"><h2>88%</h2><sub>of return abuse caught</sub></td>
    <td align="center" width="25%"><h2>-73%</h2><sub>expected cost per 1,000 returns</sub></td>
  </tr>
</table>


```mermaid
%%{init: {"theme": "base", "themeVariables": {"xyChart": {"plotColorPalette": "#0B4A57", "backgroundColor": "transparent"}}}}%%
xychart-beta
    title "Expected cost per 1,000 events (EUR)"
    x-axis ["Payments, no model", "Payments, with model", "Returns, no model", "Returns, with model"]
    y-axis "EUR" 0 --> 3000
    bar [1725, 676, 2853, 775]
```

| | 💳 Payments | 📦 Returns |
|---|--:|--:|
| Events in the test set | 12,000 (1.15% fraud) | 1,556 (4.8% abuse) |
| Share sent to manual review | **1.7%** | **14%** |
| Fraud or abuse caught | **64%** | **88%** |
| Expected cost per 1,000 events (no model → model) | 1,725 → **676 EUR** | 2,853 → **775 EUR** |

Data: a year of simulated activity (about 80,000 orders plus a Black Friday month). Return abuse is never caught at 80% precision, so returns stay **a review queue, not an automatic block**.

## 🌍 Where it fits

<table>
  <tr>
    <td valign="top" width="33%"><h3>🛒 E-commerce & marketplaces</h3>Checkout fraud, promo abuse and return abuse.</td>
    <td valign="top" width="33%"><h3>🏦 Insurance & lending</h3>Claims and applications that need a ranked review queue.</td>
    <td valign="top" width="33%"><h3>🧑‍💼 Any review team</h3>Wherever people must decide where their review hours go.</td>
  </tr>
</table>

## 🧰 Built with

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/XGBoost-0B4A57?style=for-the-badge" alt="XGBoost" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/BigQuery-669DF6?style=for-the-badge&logo=googlebigquery&logoColor=white" alt="BigQuery" />
  <img src="https://img.shields.io/badge/Google_Cloud-0B4A57?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Google Cloud" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
</p>

<details>
<summary><b>📖 Key ideas in plain words</b></summary>

- **Risk score:** a number from 0 to 1 that says how likely an event is to be fraud or abuse.
- **Explanations per decision:** for each score, the factors that pushed it up or down the most, in plain words.
- **Cost-based threshold:** instead of chasing accuracy, the line is set where the money lost to missed fraud and the money spent on reviews add up to the least.
- **MLOps:** the routine that retrains, compares and promotes models safely, so the system keeps up with new fraud patterns.

</details>

<details>
<summary><b>❓ Questions a client usually asks</b></summary>

- **Does it block customers automatically?** It doesn't have to. You decide what happens above the line: block, hold or review. Returns, in particular, stay a review queue.
- **Can it use my own data?** Yes; the demo uses synthetic data from a fictional store, and the same process trains on your history.
- **What if fraud patterns change?** It retrains on new data and only promotes a model that measures better.

</details>

## 🧭 What's next

- [x] Live demo with payment and return scoring
- [x] Cost-based thresholds measured on unseen weeks
- [ ] Monitoring dashboard for drift over time
- [ ] Short walkthrough video

## 🤝 Want this on your own data?

I build this kind of system for real businesses, on your documents, your orders and your cloud. The source code is private; **I'm happy to show it working on a call** and talk about what it would take for your team.

<p align="center">
  <a href="https://linkedin.com/in/odavidhg"><img src="https://img.shields.io/badge/Let%27s_talk_on-LinkedIn-0B4A57?style=for-the-badge&logo=linkedin&logoColor=white" alt="Let's talk on LinkedIn" /></a>
  <a href="../README.md"><img src="https://img.shields.io/badge/All_projects-NarciH-2FB3B8?style=for-the-badge&logo=github&logoColor=071A20" alt="All projects" /></a>
</p>

### More from the portfolio

<table>
  <tr>
    <td align="center" width="25%"><a href="ecommerce-ia-rag.md"><b>📚<br/>Policy assistant</b></a><br/><sub>Answers with the exact clause</sub></td>
    <td align="center" width="25%"><a href="ecommerce-ia-agentes.md"><b>🤖<br/>Returns agents</b></a><br/><sub>Closes simple returns, asks on risky ones</sub></td>
    <td align="center" width="25%"><a href="ecommerce-ia-vision.md"><b>🎥<br/>In-store video analytics</b></a><br/><sub>Counts, dwell time, queues, answers</sub></td>
    <td align="center" width="25%"><a href="ecommerce-ia-extractor-llm.md"><b>🧾<br/>Document extractor</b></a><br/><sub>Messy text to clean records</sub></td>
  </tr>
</table>

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="../assets/brand/logo-horizontal-dark.svg" />
  <img src="../assets/brand/logo-horizontal.svg" alt="David Hincapié, AI Engineer" width="260" />
</picture>

<sub><b>Mercado Aurora</b> is a fictional store with synthetic data, created for these demos. · <a href="#top">Back to top ↑</a></sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2FB3B8,45:0B4A57,100:071A20&height=110&section=footer" alt="" width="100%" />

</div>
