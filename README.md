# verdantfinpulse

**Verdant FinPulse** (`verdantfinpulse.com`) is a fast, mobile-friendly, 10-page client-side financial calculator SaaS web portal built with vanilla HTML5, CSS3, and modern ES6 JavaScript. Designed with an editorial fintech aesthetic inspired by Northline and Fernwood, every calculator executes 100% locally inside the user's browser with zero server round-trips, zero database tracking, persistent dark and light themes, multi-currency support, 50 reserved advertisement placements, and comprehensive long-form SEO guides.

## Live Demo & Deployment URLs

* **GitHub Pages URL:** `https://<your-github-username>.github.io/verdantfinpulse/`
* **Recommended Custom `.com` Domains:** `verdantfinpulse.com` · `usefinpulse.com` · `finpulsehq.com` · `verdantmoney.com`

## Complete 10-Page Sitemap

| Page Path | Workspace Name | Core Mathematical Formula | Primary Financial Use Case |
| :--- | :--- | :--- | :--- |
| `index.html` | Main SaaS Directory & Dashboard | Live Search + Category Filter | Browse, search, and launch all 9 financial workspaces |
| `tools/discount-calculator.html` | Discount Calculator | `Final = Price × (1 - d₁) × (1 - d₂)` | Compute net sale prices, stacked coupons, and optional sales tax |
| `tools/hourly-to-salary.html` | Hourly Wage to Salary Calculator | `Annual = (Rate × Hrs + 1.5 × Rate × OT) × Wks` | Convert hourly wages and overtime into annual, monthly, and net pay |
| `tools/budget-splitter.html` | 50/30/20 Budget Splitter | `50% Needs · 30% Wants · 20% Savings` | Allocate after-tax income across essential needs, lifestyle, and wealth |
| `tools/tip-splitter.html` | Tip & Bill Splitter | `Per Guest = (Bill + Tax + Bill × Tip%) ÷ Guests` | Split group dining checks and gratuity evenly across any party size |
| `tools/savings-goal.html` | Savings Goal Calculator | `PMT = [FV - PV(1+r)ⁿ] × r ÷ [(1+r)ⁿ - 1]` | Calculate required monthly and weekly deposits with compound APY |
| `tools/loan-calculator.html` | Simple Loan Calculator | `M = P · r(1+r)ⁿ ÷ [(1+r)ⁿ - 1]` | Estimate monthly amortized payments, total interest, and extra payoff savings |
| `tools/emergency-fund.html` | Emergency Fund Calculator | `Target = Monthly Core Burn × 3 or 6` | Benchmark 3-month starter and 6-month full liquid cash safety nets |
| `tools/sales-tax-calculator.html` | Sales Tax Calculator | `Gross = Net × (1 + r)` · `Net = Gross ÷ (1 + r)` | Add forward sales tax or reverse-extract pre-tax net revenue from receipts |
| `tools/margin-calculator.html` | Profit Margin & Markup Calculator | `Margin = (P - C) ÷ P` · `Markup = (P - C) ÷ C` | Model unit gross profit, margin vs. markup ratios, and batch volume profit |

## Design & Technical Highlights

* **Northline × Fernwood Visual System:** Combines Midnight Black (`#0B0B0C`), Deep Forest Green (`#1F3D2B` / `#142A20`), Sand Beige (`#E8DCC4`), Warm Cream (`#F7F5EF`), Lime Green (`#C6F432`), and Electric Purple (`#8B5CF6`) with editorial serif display headings (`Georgia, "Times New Roman", serif`) and tabular numeric readouts.
* **Real-Time Keystroke & Slider Telemetry:** Every calculator updates primary metrics, proportional stacked bars, and itemized ledgers on `input` events without form submission buttons or page reloads.
* **Mobile-First Touch Ergonomics:** Features a collapsible mobile navigation drawer (`☰`), 44px minimum touch targets, 16px mobile input font sizing (preventing iOS Safari auto-zoom), responsive stacked layouts for narrow screens, and a floating `↑ Top` quick-jump button.
* **Persistent Dark/Light Mode & Multi-Currency:** Saves user preferences for Dark/Light theme and currency symbol (`$ USD`, `€ EUR`, `£ GBP`, `₹ INR`, `¥ JPY`) in local storage.
* **50 CLS-Safe Advertisement Placements:** Includes 5 reserved `.ad-slot` containers per page (50 total across all 10 pages) with unique page-scoped IDs, reserved minimum heights to prevent cumulative layout shift (CLS), and `data-ad-lazy="true"` attributes on below-the-fold slots.
* **Comprehensive On-Page SEO:** Every page includes an original 750–1,200 word educational guide, worked mathematical examples, expandable `<details>`/`<summary>` FAQs, contextual internal links, Open Graph tags, and `WebApplication`/`WebSite` JSON-LD structured data.

## Repository Structure

```text
verdantfinpulse/
├── index.html                        # Main SaaS Directory, Hero Preview & Homepage SEO Guide
├── tools/
│   ├── discount-calculator.html      # Discount & Stacked Coupon Calculator
│   ├── hourly-to-salary.html         # Hourly Wage to Annual Salary Converter
│   ├── budget-splitter.html          # 50/30/20 Proportional Budget Calculator
│   ├── tip-splitter.html             # Restaurant Tip & Group Bill Splitter
│   ├── savings-goal.html             # Compound APY Savings Goal Planner
│   ├── loan-calculator.html          # Amortizing Loan & Extra Payment Calculator
│   ├── emergency-fund.html           # 3-Month & 6-Month Emergency Runway Calculator
│   ├── sales-tax-calculator.html     # Forward & Reverse Sales Tax Calculator
│   └── margin-calculator.html        # Gross Profit Margin & Cost Markup Calculator
├── .github/
│   └── workflows/
│       └── deploy-pages.yml          # Automated GitHub Actions deployment to GitHub Pages
├── .nojekyll                         # Bypasses Jekyll processing for instant static serving
├── sitemap.xml                       # Search engine XML sitemap
├── robots.txt                        # Crawler indexing rules
└── README.md                         # Project documentation
```

## How to Deploy on GitHub Pages

1. Open your **`verdantfinpulse`** repository on GitHub and click **Add file → Upload files**.
2. Extract `verdantfinpulse-github-pages.zip` on your computer and drag `index.html`, the `tools/` folder, `.nojekyll`, `.github/`, `sitemap.xml`, and `robots.txt` into the upload area.
3. Click **Commit changes** to push the files to your `main` branch.
4. Go to **Settings → Pages** in your repository, set **Build and deployment → Source** to **GitHub Actions** (or **Deploy from a branch → `main` / `/ (root)`**), and save.
5. To connect a custom `.com` domain (such as `verdantfinpulse.com`), enter your domain under **Settings → Pages → Custom domain**, enable **Enforce HTTPS**, and point your DNS `A` records to GitHub Pages (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`) with a `CNAME` record for `www` pointing to `<your-github-username>.github.io`.

## Adding Your Ad Network Code

Each page contains 5 clearly commented `.ad-slot` containers:

* **Homepage (`index.html`):** `home-ad-slot-1` through `home-ad-slot-5`
* **Calculator Pages (`tools/*.html`):** `<tool>-ad-slot-1` through `<tool>-ad-slot-5`

Search for `<!-- PASTE AD NETWORK TAG / SCRIPT` in any HTML file and paste your ad network `<ins>` tag or script inside the `.ad-placeholder-inner` container.

## License

Copyright © Verdant FinPulse. All rights reserved.
