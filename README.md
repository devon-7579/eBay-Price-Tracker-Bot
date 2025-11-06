# eBay Price Tracker Bot

> Track, compare, and alert on eBay listings automatically — across real Android devices and emulators. This eBay Price Tracker Bot eliminates manual refreshing and price hunting, sending timely notifications when prices drop or listings match your target criteria. Expect consistent, human-like interactions with the eBay app and reliable reports that accelerate decision-making.

<p align="center">
  <a href="https://Appilot.app" target="_blank"><img src="media/appilot-baner.png" alt="Appilot Banner" width="100%"></a>
</p>
<p align="center">
 <a href="https://t.me/devpilot1" target="_blank"><img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
 <a href="mailto:support@appilot.app" target="_blank"><img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"></a>
 <a href="https://appilot.app" target="_blank"><img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website"></a>
 <a href="https://discord.gg/r5sJ5vhf" target="_blank"><img src="https://img.shields.io/badge/Join-Appilot_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Appilot Discord"></a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom eBay Price Tracker Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
This system automates price tracking on eBay by navigating the Android app (or mobile web) to watchlist items, saved searches, and specific keywords/sellers.  
It removes the repetitive work of checking current prices, recent sales, and shipping totals, and notifies you when a target threshold, discount, or NEW condition is met.  
Businesses and power buyers gain faster deal discovery, consistent monitoring, and scalable coverage across many SKUs.

### Automating eBay Deal Discovery & Alerts
- Monitors watchlists, saved searches, and seller stores with human-like app interactions.
- Detects price drops, new listings, and best-offer eligible items, then pushes alerts via webhook, email, or Telegram.
- Aggregates current price, shipping, taxes, and historical sold data to compute “effective price”.
- Schedules runs and parallelizes across devices to cover hundreds of keywords with low failure rates.
- Built for growth teams: proxy support, multi-account isolation, and anti-pattern randomization.

## Core Features
- **Real Devices and Emulators:** Run on physical Android phones/tablets and emulator stacks (Bluestacks/Nox) for high compatibility with the eBay app UX.
- **No-ADB Wireless Automation:** Operate without tethered USB using ADB-less/Appilot wireless control, reducing setup friction and improving fleet mobility.
- **Mimicking Human Behavior:** Randomized delays, swipe/scroll curves, tap jitter, and viewport variance to avoid robotic patterns.
- **Multiple Accounts Support:** Isolated sessions, per-account cookies, and separate watchlists/saved searches for agency or team use.
- **Multi-Device Integration:** Horizontal scaling via device farms; distribute tasks by keyword, store, or category with centralized queueing.
- **Exponential Growth for Your Account:** Faster deal capture, increased purchase velocity, and improved seller negotiations through timely alerts.
- **Premium Support:** SLA-backed onboarding, custom workflows, and priority debugging for production environments.
- **Smart Price Rules:** Define thresholds by absolute value, % drop, shipping-inclusive total, or delta vs. historical sold median.
- **Sold-History Snapshotting:** Periodically captures recent SOLD listings to gauge realistic market price bands.
- **Notifications Hub:** Webhooks, REST callbacks, email/Telegram/Slack messages with deep links to listings.

## Additional Feature Set

| Feature | Description |
|---|---|
| Rate Limiter & Backoff | Adaptive pacing per device/account to respect app limits and reduce captcha triggers. |
| Proxy & Fingerprint Manager | Rotating mobile/HTTP proxies and device fingerprint variance for safer large-scale runs. |
| Task Scheduler & Queue | Cron-like schedules with priority queues and retries for failed tasks. |
| OCR & Text Normalization | Extracts price/shipping text from dynamic UI when elements are non-standard. |
| Audit Logs & Replay | Structured logs with screen-record snippets for debugging and compliance. |
| Export Pipelines | CSV/JSON exports and optional Google Sheets sync for ops teams. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/ebay-price-tracker-bot-banner.png" alt="ebay-price-tracker-bot-architecture" width="95%">
  </a>
</p>

## How It Works
1. **Input or Trigger** — The automation is triggered through the Appilot dashboard, where the user initiates the process by setting up desired tasks such as app interactions, notifications, or scheduled actions on the Android device or emulator.
2. **Core Logic** — Appilot controls the Android device or emulator through UI Automator or ADB (Android Debug Bridge), performing actions like app navigation, form submissions, data entry, or automated clicks/taps.
3. **Output or Action** — As a result, the automation performs the designated tasks (e.g., sending messages, making app updates, posting content, etc.) and outputs the desired results to the user or triggers further actions within the connected system.
4. **Other functionalities** — Additional features like retry logic, error handling, logging, or parallel processing can be configured within the Appilot dashboard to ensure smooth execution and troubleshooting in case of failures.

## Tech Stack
- **Language:** Kotlin, Java, JavaScript, Python  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, MonkeyRunner, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm.

## Directory Structure
```
ebay-price-tracker-bot/
│
├── src/
│ ├── main.py
│ ├── automation/
│ │ ├── tasks.py
│ │ ├── scheduler.py
│ │ ├── detectors/
│ │ │ ├── price_rules.py
│ │ │ └── sold_history.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── proxy_manager.py
│ │ ├── device_controller.py
│ │ ├── notifier.py
│ │ └── config_loader.py
│ ├── drivers/
│ │ ├── appium_caps.json
│ │ └── uiautomator_helpers.kt
│ └── integrations/
│ ├── webhooks.py
│ ├── telegram_bot.py
│ └── sheets_sync.py
│
├── config/
│ ├── settings.yaml
│ ├── accounts.yaml
│ └── credentials.env
│
├── dashboards/
│ └── appilot-flows.json
│
├── media/
│ ├── ebay-price-tracker-bot-banner.png
│ └── screenshots/
│ └── listing-alert.png
│
├── logs/
│ ├── device-001.log
│ └── task-runner.log
│
├── output/
│ ├── alerts.json
│ ├── report.csv
│ └── exports/
│ └── latest_listings.csv
│
├── tests/
│ ├── test_price_rules.py
│ └── test_notifier.py
│
├── docker/
│ ├── Dockerfile
│ └── compose.yaml
│
├── requirements.txt
└── README.md
```


## Use Cases
- **Deal hunters** use it to track price drops on watchlisted items, so they can buy at the right moment without constant checking.  
- **Resellers** use it to monitor new listings in target categories, so they can source inventory faster than competitors.  
- **Ops/Analytics teams** use it to export effective-price data to Sheets/BI tools, so they can benchmark and forecast acquisition costs.  
- **Agencies** use it to manage multiple buyer accounts across verticals, so they can scale searches with isolation and reporting.  

## FAQs
**How do I configure this automation for multiple accounts?**  
Define each account in `config/accounts.yaml` with individual cookies/proxies; the scheduler assigns tasks by account, ensuring isolation and staggered runs.

**Does it support proxy rotation or anti-detection?**  
Yes — enable rotating mobile/HTTP proxies in `config/settings.yaml`. The controller randomizes gestures, timings, and viewport scrolls to avoid fixed patterns.

**Can I schedule it to run periodically?**  
Use `automation/scheduler.py` to set cron-like intervals per keyword or search. Tasks queue automatically and distribute across devices.

**Will it include shipping and taxes in alerts?**  
You can enable “effective price” mode, which parses shipping/tax lines and computes a total before applying your thresholds.

**What happens if eBay updates its UI?**  
UI selectors are abstracted in `drivers/uiautomator_helpers.kt` and `src/automation/utils/device_controller.py` for quick patches; fallback OCR can bridge minor changes.

## Performance & Reliability Benchmarks
- **Execution Speed:** Scans 30–60 listings per device-minute (UI-dependent), with near-real-time alerts for new matches.  
- **Success Rate:** ~**95%** end-to-end task completion in stable network conditions with proper proxy hygiene.  
- **Scalability:** Proven horizontal scaling from **300 up to 1,000** concurrent Android sessions via containerized device farms and task queues.  
- **Resource Efficiency:** Lightweight workers (≤300MB RAM baseline per emulator) and adaptive throttling to maintain device responsiveness.  
- **Error Handling:** Exponential backoff, circuit breakers, auto-retry on transient failures, structured logging, and optional alerting to Slack/Telegram.

##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>
