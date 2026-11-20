<p align="center">
  <a href="https://ecvision-frontend-4y6shrzafa-uc.a.run.app">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="../assets/cases/ecommerce-ia-vision-dark.png">
    <img alt="In-store video analytics that answers questions about the day" src="../assets/cases/ecommerce-ia-vision-light.png" width="100%">
  </picture>
  </a>
</p>

# In-store video analytics that answers questions about the day

**[▶ Try the live demo](https://ecvision-frontend-4y6shrzafa-uc.a.run.app)** · no sign-up; the first request after a quiet period can take up to ~30 s while the service wakes up.

## The problem

A physical store already has cameras, but nobody watches the footage. The questions a manager actually has go unanswered: how many people came in today, which areas hold their attention, when does the checkout line get too long, and did staffing match the busy hours.

## What it does

- **Counts people coming in and going out**, hour by hour, from ordinary store video.
- **Measures how long visitors stay in each zone** (entrance, aisles, checkout).
- **Flags checkout queues** when they pass a threshold.
- **Answers questions in plain Spanish**, and every number in the answer comes from the recorded events; it never makes figures up.
- **Private by design**: faces are blurred, uploads are deleted after a day, and it never guesses age, gender or any other personal trait.
- **No special hardware**: it processes video on ordinary servers, without GPUs.

## What your business gets

| Without it | With the video analytics |
|---|---|
| Footage nobody watches | Entries, exits, dwell time and queue alerts from the same cameras |
| Staffing by gut feeling | Busy hours and queue peaks, per day |
| Worries about filming customers | Blurred faces, short retention, no personal traits inferred |

## Try it in the demo

1. In **Ver resultados**, pick the `entrada-01` clip, then `cajas-01` for the queue chart.
2. In **Pregúntale al analista**, ask "¿A qué hora hubo más fila en el día simulado?"
3. Ask "¿Cuántas mujeres entraron?" and see it decline.

## Results

Counting error, detection accuracy, processing speed and the share of questions answered correctly are being measured on labeled sample footage. This page only publishes measured numbers.

## Where it fits

Retail stores and supermarkets, banks and service counters, malls, museums and events: visitor flow and waiting times without identifying anyone.

**Built with** open computer-vision models and an assistant on Google's Agent Development Kit (ADK) and Gemini, on Google Cloud.

---

*The source code is private. Happy to show it working on a call.* · [David Hincapié](https://github.com/NarciH), AI engineer · [← All projects](../README.md)
