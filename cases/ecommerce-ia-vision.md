# In-store video analytics that answers questions about the day

**[▶ Try the live demo](https://ecvision-frontend-4y6shrzafa-uc.a.run.app)** · the first request after a quiet period can take up to ~30 s while the service wakes up.

## The problem

A physical store already has cameras, but nobody watches the footage. The questions a store manager actually has go unanswered: how many people came in today, which areas hold their attention, when does the checkout line get too long, and did staffing match the busy hours. Hiring someone to count by hand is expensive; buying a closed analytics product locks the data away.

## What it does

- **Counts people coming in and going out**, hour by hour, from ordinary store video.
- **Measures how long visitors stay in each zone** (entrance, aisles, checkout), so the team sees which displays work.
- **Flags queues** at the checkout when they pass a threshold, so someone can open another till.
- **Answers questions in plain language**: "what was the busiest hour?", "how long did people wait at checkout this afternoon?". Every number in the answer comes from the recorded events; the assistant never makes figures up.
- **Respects privacy by design**: faces are blurred, and the system never guesses age, gender or any other personal trait. It counts movement, not identities.
- **Runs without special hardware**: it processes video on ordinary servers, so a small store does not need to buy GPUs.

## Results

Counting error, detection accuracy, processing speed and the share of questions answered correctly are being measured on labeled sample footage. This page only publishes measured numbers.

**Built with** computer vision with open models and an assistant on Google's Agent Development Kit (ADK) and Gemini, on Google Cloud.

*The source code is private. Happy to show it working in a call.*
