# MyUiPathJournal
Repository chronicling my 7-year UiPath RPA career: real-world automations, industry-standard workflows, design docs, and quantified impact. Perfect learning resource for UiPath beginners and a portfolio for clients assessing my automation expertise.

---

Hi, I’m **MasterOfLogic**, an **Intelligent Automation Evangelist**.
If you’re reading this journal, you’re probably looking for more than a dry résumé—you want to see the synergy between my passion for intelligent automation and a glimpse of my personal journey.

### From Newcomer to Change-Maker

I joined **Access Bank** in 2018 as a **Process Automation Engineer** with only a rough idea of what the role entailed. Seven years later, I’m proud of the measurable impact I’ve had: building dozens of automations, optimising countless processes, and dramatically improving key metrics such as speed, reliability, and cost.

In this document I’ll highlight a few signature projects and explain why they matter.

---

## 1. Indiana Overhead Adjustment

**Type of process:** Unattended

**Type of automation:** Desktop Ui-Automation automation

**Applications involved:** Matrixcare Desktop app

**MatrixCare** is a desktop electronic health-record (EHR) and operations platform designed for post-acute and long-term-care providers (skilled-nursing facilities, senior-living communities, home-health and hospice agencies, life-plan/CCRC campuses, and private-duty nursing). Its modular suite spans point-of-care charting, medication & e-MAR, admissions, revenue cycle, analytics, and data exchange with hospitals and HIEs.
[https://www.matrixcare.com/](https://www.matrixcare.com/)
![image](https://github.com/user-attachments/assets/d7896ff4-aff4-4bbc-b7d5-19e3c4026ad8)

**Link to project:** [https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process](https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process)

**Process steps:** [https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process?tab=readme-ov-file#readme](https://github.com/MasterOfLogic1/IndianaOverheadAdjustment.RPA.Uipath.Process?tab=readme-ov-file#readme)




### The manual process

Here  Billing officers receive CSV files with **over two million invoice lines**. Each officer must:

1. Open each invoice in MatrixCare
2. Search for the invoice on matrix care which appears with multiple transactions on the desktop app
3. for each transaction see , Edit the posting amount (The rule: *If the total balance is negative **and** any component balance is divisible by \$34.50, adjust the posting amount—for PA Indiana Medicaid payees only.*
4. The traditional process takes 2 dayys or more to complete as entry specilist get tired and make mistakes.



### Our automation

Using UiPath, built a **desktop automation** that performs these steps in the most optimal way in 1hr

* Csv is sent through a uipath app and is loaded into a storage bucket
* The app also triggers the robot which reads the csv, refines the records and loads the data into a queue
* queue triggers are set to kick start 4 robots running the performer process which handles adjustment of the overhead balances.

### Impact

| Metric                     | Before automation | After automation     |
| -------------------------- | ----------------- | -------------------- |
| Employees involved         | 30                | 0 (fully unattended) |
| Hours per employee per day | 6                 | 0                    |
| Hourly cost                | \$45              | \$0                  |
| **Daily labour cost**      | **\$8,100**       | **\$0**              |

*(30 employees × 6 hours × \$45 = \$8,100 per day)* at \$45 /hour – **\$2.1 million** a year.

Beyond the direct \$8 k-per-day savings, the bot eliminates manual errors and slashes turnaround time from days to hours.
⏱️ Processing time: 180 human‑hours → **1 unattended hours**
💰 Labour spend: **\$2,106,000 saved** yearly

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

