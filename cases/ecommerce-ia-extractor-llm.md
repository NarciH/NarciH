# A small fine-tuned model that turns emails and invoices into clean data

**Status: training now.** Built and tested; once the first training run finishes it goes live and is compared with Gemini.

## The problem

Return requests arrive as messy emails ("hi, the trainers from last Monday's order are too small…") and invoices as free text. Someone has to copy the order number, dates, amounts and reasons into a system. A large hosted model can do it, but at a cost per document and with your data leaving your control. The question this project answers: **can a small open model, trained for the job and running on an ordinary server without a GPU, match it?**

## What it does

- Reads a **return request** and fills in customer, order, delivery date (also from "last Monday"), product, reason, condition, amount, a one-line summary and urgency.
- Reads an **invoice** and fills in number, seller and tax id, every line with quantity and discount, base, VAT and total.
- Always returns a complete, valid record or a clear error, never a half-filled one. Missing data stays empty instead of being invented.

## How it is measured

- **Same task, three models**: the fine-tuned small model, the same model without training, and Gemini, all with the same instructions.
- **An honest test**: 40 texts written by hand, plus a test set that is locked before training so the model never sees it.
- **What gets reported**: accuracy per field (dates and amounts compared by value, not by spelling), invoice lines found, valid records, full matches, response time and cost per 1,000 documents.

## Results

Accuracy, response time and cost against Gemini will be published here once the comparison has run. This page only publishes measured numbers.

**Built with** an open 4-billion-parameter model fine-tuned with QLoRA, compared with Gemini.

*The source code is private. Happy to show it working in a call.*
