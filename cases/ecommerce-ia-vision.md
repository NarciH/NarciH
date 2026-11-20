<a id="top"></a>
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:071A20,55:0B4A57,100:2FB3B8&height=190&section=header&text=Store%20Video%20Analytics&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Counts%2C%20dwell%20time%20and%20queues%2C%20then%20answers%20about%20the%20day&descAlignY=60&descSize=17&animation=fadeIn" alt="Store Video Analytics: Counts, dwell time and queues, then answers about the day" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=19&duration=3000&pause=900&color=2FB3B8&center=true&vCenter=true&width=720&lines=Visitors+in+and+out%2C+hour+by+hour;Minutes+spent+in+each+zone;Checkout+queue+alerts;Faces+blurred%2C+no+personal+traits+inferred" alt="Visitors in and out, hour by hour" />

<p>
  <img src="https://img.shields.io/badge/status-live-2FB3B8?style=flat-square" alt="Live" />
  <img src="https://img.shields.io/badge/industry-physical_retail-0B4A57?style=flat-square" alt="Physical retail" />
  <img src="https://img.shields.io/badge/demo_UI-Spanish-557079?style=flat-square" alt="Demo in Spanish" />
  <img src="https://img.shields.io/badge/hardware-no_GPU_needed-557079?style=flat-square" alt="No GPU needed" />
</p>

<a href="https://ecvision-frontend-4y6shrzafa-uc.a.run.app"><img src="https://img.shields.io/badge/%E2%96%B6_Try_the_live_demo-no_sign--up-0B4A57?style=for-the-badge" alt="Try the live demo" /></a>
<a href="#-try-it-in-60-seconds"><img src="https://img.shields.io/badge/What_to_try-60_s-2FB3B8?style=for-the-badge" alt="What to try" /></a>

</div>

## 😣 The problem

A physical store already has cameras, but **nobody watches the footage**. The questions a manager actually has go unanswered:

> *How many people came in today? · Which areas hold their attention? · When does the checkout line get too long? · Did staffing match the busy hours?*

## 🧭 From cameras to answers

<p align="center"><img src="../assets/cases/ecommerce-ia-vision-journey.svg" alt="Store cameras, faces blurred, people counted and timed per zone, and a manager asks questions in plain language." width="100%" /></p>

> [!TIP]
> The demo sleeps when nobody uses it, so the first request after a quiet period can take up to ~30 s. Everything after that is fast.

## 🧩 What's inside

<table>
  <tr>
    <td valign="top" width="33%"><h3>🚪 People counting</h3>Entries and exits, hour by hour, from ordinary store video.</td>
    <td valign="top" width="33%"><h3>⏱️ Dwell time per zone</h3>How long visitors stay at the entrance, in each aisle and at checkout.</td>
    <td valign="top" width="33%"><h3>🚨 Queue alerts</h3>Flags the checkout line when it passes a threshold you choose.</td>
  </tr>
  <tr>
    <td valign="top" width="33%"><h3>💬 Ask the analyst</h3>Questions in plain Spanish; every number in the answer comes from the recorded events, never made up.</td>
    <td valign="top" width="33%"><h3>🙈 Private by design</h3>Faces blurred, uploads deleted after a day, and it never guesses age, gender or any personal trait.</td>
    <td valign="top" width="33%"><h3>🖥️ No special hardware</h3>Processes video on ordinary servers, without GPUs.</td>
  </tr>
</table>

## 🔀 A conversation with the analyst

```mermaid
%%{init: {"theme": "base", "themeVariables": {"primaryColor": "#E4F0F1", "primaryTextColor": "#071A20", "primaryBorderColor": "#0B4A57", "lineColor": "#2FB3B8", "secondaryColor": "#FFFFFF", "tertiaryColor": "#F6FAFA", "fontFamily": "Inter, Segoe UI, sans-serif"}}}%%
sequenceDiagram
    actor G as 🧑‍💼 Store manager
    participant A as 💬 Video analyst
    G->>A: ¿A qué hora hubo más fila en el día simulado?
    A-->>G: The peak hour and queue length, taken from the recorded events
    G->>A: ¿Cuántas mujeres entraron?
    A-->>G: Declines: it never infers gender or any personal trait
```

## 💼 What your business gets

| | Without it | With the video analytics |
|:-:|---|---|
| 📼 | Footage nobody watches | Entries, exits, dwell time and queue alerts from the same cameras |
| 🎲 | Staffing by gut feeling | Busy hours and queue peaks, per day |
| 😟 | Worries about filming customers | Blurred faces, short retention, no personal traits inferred |
| 📊 | Reports someone has to build | Ask a question, get the number and where it came from |

## 🧪 Try it in 60 seconds

1. Open the **[live demo](https://ecvision-frontend-4y6shrzafa-uc.a.run.app)**.
2. In **Ver resultados**, pick the `entrada-01` clip, then `cajas-01` for the queue chart.
3. In **Pregúntale al analista**, try the questions below.

| Ask this | What to look for |
|---|---|
| ¿A qué hora hubo más fila en el día simulado? | The peak hour, with the figure behind it |
| The `cajas-01` clip | The checkout queue over time, and when it crossed the alert line |
| ¿Cuántas mujeres entraron? | A polite refusal: it never infers gender |

## 📊 Results

> [!NOTE]
> Counting error, detection accuracy, processing speed and the share of questions answered correctly are being measured on labeled sample footage. They will appear here, dated, once measured. This page only publishes measured numbers.

## 🌍 Where it fits

<table>
  <tr>
    <td valign="top" width="33%"><h3>🛍️ Stores and supermarkets</h3>Traffic, dwell time and checkout staffing.</td>
    <td valign="top" width="33%"><h3>🏦 Banks and service counters</h3>Waiting times and peak hours at each counter.</td>
    <td valign="top" width="33%"><h3>🏛️ Malls, museums, events</h3>Visitor flow without identifying anyone.</td>
  </tr>
</table>

## 🧰 Built with

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white" alt="ONNX" />
  <img src="https://img.shields.io/badge/Google_ADK-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google ADK" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini" />
  <img src="https://img.shields.io/badge/Google_Cloud-0B4A57?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Google Cloud" />
</p>

<details>
<summary><b>📖 Key ideas in plain words</b></summary>

- **Computer vision:** software that finds and follows people in video frames, so they can be counted and timed.
- **Zones:** areas you draw on the camera image (entrance, aisle, checkout) to measure where time is spent.
- **Grounded answers:** the assistant reads only the recorded events, so every number it gives can be traced.
- **Privacy by design:** blurring, short retention and a hard "no" to personal traits are built in, not optional.

</details>

<details>
<summary><b>❓ Questions a client usually asks</b></summary>

- **Do I need new cameras?** No; it works on ordinary store video.
- **Does it recognise people?** No. It counts and times anonymous visitors and blurs faces.
- **Can it run on my premises?** It runs on ordinary servers without GPUs, in the cloud or on-site.

</details>

## 🧭 What's next

- [x] Live demo with counting, dwell time, queues and the analyst
- [ ] Publish counting error, accuracy and speed on labeled footage
- [ ] Short walkthrough video with sample clips

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
    <td align="center" width="25%"><a href="ecommerce-ia-fraude-mlops.md"><b>🛡️<br/>Fraud & return-abuse detection</b></a><br/><sub>Scores, explains, reviews less</sub></td>
    <td align="center" width="25%"><a href="ecommerce-ia-agentes.md"><b>🤖<br/>Returns agents</b></a><br/><sub>Closes simple returns, asks on risky ones</sub></td>
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
