# MyUiPathJournal
Repository chronicling my 7-year UiPath RPA career: real-world automations, industry-standard workflows, design docs, and quantified impact. Perfect learning resource for UiPath beginners and a portfolio for clients assessing my automation expertise.

https://www.matrixcare.com/
![image](https://github.com/user-attachments/assets/d7896ff4-aff4-4bbc-b7d5-19e3c4026ad8)

# 🦾 Automating Stories That Matter

![hero](docs/images/hero.gif)

## Preface – *“There has to be a better way…”*

Seven years ago I was the rookie in a Medicaid billing office, staring at an avalanche of invoices and spreadsheets.  Manual copy‑paste ruled the day, error rates were **5 %**, and overtime pizza was a line‑item in the budget.  When I discovered **UiPath** those long nights turned into my playground – and eventually into the portfolio you’re reading now.

Below are the three flagship adventures that taught me how to make robots pay their own salaries (and then some).  Every link opens the actual source so you can peel back the curtain and reuse anything you like.

---

## 1. *The Indiana Overhead Odyssey*

### The Scene

Thirty clerks, six hours each day, chipping away at a stubborn pile of **Indiana Medicaid** invoices.  Their mission: find any invoice whose **total was negative** *and* whose individual lines were perfectly divisible by **\$34.50**.  Mundane, brittle, and – at \$45 /hour – **\$2.1 million** a year.

### My Hero’s Toolkit

* Desktop robot built with razor‑sharp selectors and multithreaded queues
* Batch adjustment logic scripted in pure activities (no code fancy footwork)
* Real‑time audit emails + a Power BI feed for finance leadership

### Happily Ever After

⏱️ Processing time: 180 human‑hours → **3 unattended hours**
💰 Labour spend: **\$2,106,000 saved** yearly
🔗 [Source](https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process)

![Overhead diagram](docs/images/overhead_adjustment_flow.png)

---

## 2. *The Sandata EVV Double‑Act*

*(Dispatcher & Performer)*

### The Scene

Across the state, **50 full‑time agents** wrestled with the Sandata Manager portal, updating Electronic Visit Verification (EVV) records.  Compliance deadlines loomed; morale wilted.

### My Hero’s Toolkit

* **Dispatcher** robot scrapes *On‑Hold* or *Pending* records and drops them into an Orchestrator queue
* **Performer** robot, queue‑triggered, logs in, releases each hold, leaves a compliant comment, and updates status to *Confirmed*
* Resilience baked in: retry scopes, API failover, and ServiceNow exception routing

### Happily Ever After

⏱️ Turnaround: 3 days → **45 minutes**
💰 Labour spend: **\$4,655,000 saved** yearly
🔗 [Dispatcher Repo](https://github.com/MasterOfLogic1/SandataEvvReportDispatcher.RPA.Uipath.Process) · [Performer Repo](https://github.com/MasterOfLogic1/SandataEvvReportPerformer.RPA.Uipath.Process)

![EVV gif](docs/images/sandata_evv.gif)

---

## 3. *The MESA Waiver Whisperer* – *(Coming Soon!)*

Link: [https://github.com/MasterOfLogic1/MESA.ED.Waiver.RPA.Uipath.Process](https://github.com/MasterOfLogic1/MESA.ED.Waiver.RPA.Uipath.Process)
While the final metrics are still being audited, early pilots hint at another six‑figure saving.  Stay tuned – the saga continues.

![MESA flow](docs/images/mesa_waiver.png)

---

## 📚 Side‑Quests: Reusable Libraries

I never reinvent a wheel.  Everything generic ends up in [`/UipathLibraries`](https://github.com/MasterOfLogic1/UipathLibraries):

* **QueueHelpers** – JSON‑safe serializers with poison‑pill handling
* **OutlookMailer** – Markdown‑to‑HTML templated emails with inline images
* **ErrorShield** – Plug‑and‑play retry/timeout/catch framework

---

## The Scoreboard

> **Total annual payroll replaced:** *≈ \$6.8 million*
> **Total bot OPEX (licences + VM):** *< \$40 k*
> **ROI in Year 1:** *1 700 %*

---

## Ready for Your Quest?

If these stories spark ideas – or if you have a mountain of copy‑paste with your name on it – let’s talk.

* 💌 **Email:** [automation@masteroflogic.io](mailto:automation@masteroflogic.io)
* 💼 **LinkedIn:** [linkedin.com/in/masteroflogic](https://www.linkedin.com/in/masteroflogic)
* 🚀 **Hire me:** open to freelance & full‑time opportunities

> “Automation is cost‑cutting by tightening the corners *and not* cutting them.” – **Haresh Sippy**

---

### How to Run the Bots Locally

```bash
# Install UiPath Studio 23.10+ and clone any repo:
 git clone https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process
# Open Main.xaml and hit Run (or publish to Orchestrator for unattended magic)
```

MIT License – take, tweak, and prosper 🎉

