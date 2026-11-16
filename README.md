# Kaustubh's Job Alerts

Checks every 3 hours for **Product Manager / APM, Product Analyst, Business Analyst, Category, Growth/CRM and Business Operations** roles, and sends new ones to Telegram (@JobFindet_bot), newest first.

**Locations:** Bengaluru, Mumbai, Pune, Delhi NCR, Hyderabad, and remote jobs open to India. Edit `locations` in `config.json` to change these.

**Level:** skips Director/VP/Head, Senior PM and non-product roles (engineering, design, HR, finance, sales).

## Where it looks

- **Indian startups:** Razorpay, Paytm, Meesho, CRED, Groww, Zeta, FamPay, Fi, slice, Clear, Porter, Glance, InMobi, BlueStone, Navi, Atlan, Mindtickle, Hevo Data
- **Big companies' career portals in India (Workday):** PayPal, Target, Adobe, Salesforce, Mastercard, Citi, Barclays, Philips, Nike, NVIDIA, Thomson Reuters, Wolters Kluwer, Workday, Zendesk, Gartner, Lowe's, Equifax
- **Remote:** Himalayas (jobs open to India)

## Alerts

Jobs go to Kaustubh's chat. Problem reports (daily check-in, ⚠️ source failures, 🚨 crashes) go to `TELEGRAM_ADMIN_CHAT_ID` (Chaitanya).

## Run locally

```sh
python3 job_watcher.py --dry-run   # show matching jobs, send nothing
python3 job_watcher.py             # send alerts
```

## Not covered automatically

LinkedIn, Naukri, Instahyre, Cutshort, Wellfound, and most PM roles at Flipkart, Swiggy, Zomato and PhonePe (they use their own portals or block bots). Use those sites' email job alerts.
