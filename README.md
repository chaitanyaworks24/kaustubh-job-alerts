# Kaustubh's Job Alerts

Checks every 2 hours for **Product Manager / APM, Product Analyst, Business Analyst, Category, Growth/CRM and Business Operations** roles, and sends new ones to Telegram (@JobFindet_bot), newest first.

**Locations:** Bengaluru, Mumbai, Pune, Delhi NCR, Hyderabad, and remote jobs open to India. Edit `locations` in `config.json` to change these.

**Level:** skips Director/VP/Head, Senior PM and non-product roles (engineering, design, HR, finance, sales).

## Where it looks

- **Indian startups:** Razorpay, Paytm, Meesho, CRED, Groww, Zeta, FamPay, Fi, slice, Clear, Porter, Glance, InMobi, BlueStone, Navi, Atlan, Mindtickle, Hevo Data
- **Big companies' career portals in India (Workday):** PayPal, Target, Adobe, Salesforce, Mastercard, Citi, Barclays, Philips, Nike, NVIDIA, Thomson Reuters, Wolters Kluwer, Workday, Zendesk, Gartner, Lowe's, Equifax
- **Job sites (via [JobSpy](https://github.com/speedyapply/JobSpy)):** LinkedIn, Naukri and Indeed (logged out, jobs posted in the last 24 hours). Glassdoor is set up but off: it blocks GitHub's servers. The same job showing up on several sites is only sent once.
- **Indian job boards:** iimjobs and Hirist (same backend; searched with a 10-second gap between requests, as their robots.txt asks). Hirist hides some of its newest jobs from logged-out visitors, so a few Hirist roles arrive a few days late.
- **Remote:** Himalayas (jobs open to India)

## Alerts

Jobs go to Kaustubh's chat. After each check's jobs, one more message lists all their apply links as full URLs, one per line, ready to copy and forward (split into several messages if it's too long for one). Problem reports (daily check-in, ⚠️ source failures, 🚨 crashes) go to `TELEGRAM_ADMIN_CHAT_ID` (Chaitanya).

## Run locally

Needs Python 3.10+ for the JobSpy sites:

```sh
pip install -r requirements.txt
python3 job_watcher.py --dry-run   # show matching jobs, send nothing
python3 job_watcher.py             # send alerts
```

## Not covered automatically

Instahyre, Cutshort, Wellfound, and most PM roles at Flipkart, Swiggy, Zomato and PhonePe (they use their own portals or block bots). Use those sites' email job alerts.
