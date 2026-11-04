# Creative

## Overview

Creatives are the first (and often only) impression an advertiser makes. In Sponsored Content, the creative is the ad. Strong creatives drive CTR, which directly impacts CPA. This file covers Sponsored Content ads, display ads, Gen AI AdMaker, landing pages, creative review, and creative testing.

> **Attribution note:** When reporting creative-level CPA or CVR, always specify the attribution model (e.g., `CPA (CT only)`, `CVR (Total CT+VT)`).

> **Where the Display item MCP payload lives:** This file covers Display creative *strategy and review*. The **payload shape** for Display items via the MCP — `ad_tag` (3P JS tag) vs `asset_url` + `dimensions` (1P-hosted) — is documented in [`targeting.md`](targeting.md) under "Native vs Display creative type", because the lock-in interacts with campaign-type selection at create time.

---

## Sponsored Content Ads

### Campaign Setup

- For each campaign, **4 to 6 ads** are recommended (never more than 10).
- Include **two meaningfully different titles and two different images** per campaign.
- Include **one description or one CTA** per campaign to set post-click expectations.
- Create **separate campaigns for distinct customer groups.** Example for insurance: "Car Insurance: Drivers under 30…" and "Home Insurance: Protect Your Home…"

### Title Best Practices

| Element | Best Practice |
|---|---|
| **Length** | 60 characters, front-loaded value proposition. |
| **Localisation** | Use Dynamic Keyword Insertion (DKI) for localisation. |
| **Grammar** | Grammatically tight — no errors. |
| **Style** | Clear post-click expectations. Clarity. Trust. Avoid misleading or sensational titles. |

**Messaging angles to consider:**

- Listicles: "Top 5 Ways…"
- Testimonial style: first-person experiences.
- Expert quotes or FOMO messaging.
- Questions: "Are You Overpaying for Insurance?"
- Data or urgency: "Rates Dropped 12%."
- Audience callout: "Busy Parents," "Small Business Owners."
- Dynamic Keyword Insertion (DKI) for localisation.

### Image Best Practices

| Do | Don't |
|---|---|
| High contrast, sharp focus | Low resolution or blurry images |
| Faces drive engagement | Generic stock images |
| Simple focus, product-centric | Branding in image |
| Bold colours, proper cropping | Overcrowded visuals |

### Motion Ads

- Motion ads can drive **up to 20% higher CVR** and can be auto-generated from static assets using AI tools — no design expertise needed.
- Consider A/B testing static vs. motion.
- Specs: short (< 15 seconds), proper video specs, subtle movement only.
- Video: short, with subtitles, easy to watch muted, CTAs included.

### Ad Optimisation

- Keep the default **Ad Optimisation mode enabled** — it prioritises top-performing creative combinations automatically.
- If testing creatives manually, isolate clear differences across angles and track performance using consistent naming.
- Aim for **three distinct titles and three unique images** per campaign for enough variety.
- **Ensure ads avoid** mature themes, distasteful imagery, aggressive promises, or close-ups of body parts — these can limit access to premium inventory.

---

## Display Ads

### Ad Sizes

Multiple ad sizes can be uploaded in a single campaign (no need for a different campaign per ad size).

**For maximum reach, upload these IAB standard dimensions:**

| Platform | Sizes |
|---|---|
| **Mobile** | 300×250, 300×600, 320×50, 720×1280 |
| **Desktop** | 300×250, 300×600, 970×250, 728×90, 160×600 |

If you can't upload every size, prioritise: 300×250 and 300×600.

### Top Spending Ad Sizes

| Platform | Top Size | Supply Type |
|---|---|---|
| Mobile | 300×600 | Mostly non-bidded (Feature Placement) |
| Mobile | 300×250 | Even mix of bidded and non-bidded |
| Desktop | 300×600 | Mostly bidded (Right Rail) |
| Desktop | 300×250 | Even mix of bidded and non-bidded |

### Social Importer

Import 300×250 and 300×600 sizes directly from the Meta Ads Library. Can also repurpose ads from other channels (Creative Shop can help resize).

### Display Creative Strategy

| Do | Why |
|---|---|
| Use high-quality, CTA-driven creatives | Display supply is more expensive than Sponsored Content due to limited inventory. |
| Visual simplicity and brand consistency | Clarity drives engagement. |
| Include a clear CTA within the creative | Users need direction. |
| Include a brand logo | Recognition and trust. |
| Use subtle motion to encourage interaction | Higher engagement. |
| Value-based messaging: price drops and urgency | Drives action. |

### Display Landing Pages

- Default: drive directly to the **product page** (users know they clicked an ad and are typically closer to converting).
- Advertorial pages work when the product / service requires additional education, storytelling, or context before conversion.

---

## Gen AI AdMaker

### Capabilities

| Feature | How to Use |
|---|---|
| **Titles and descriptions** | Generate from scratch using prompts (target audience + product details). Rephrase existing content. Produce alternative versions of high-performing titles while maintaining core value proposition. |
| **Ad creatives** | Create static images from scratch (prompt or reference image). Modify backgrounds for seasonality / promotions. Convert static images into motion ads. |

### Key Benefit

Using Gen AI AdMaker significantly improves **creative approval rate by approximately 50%**. The model has built-in policies that reduce time to launch.

---

## Landing Pages

### Landing Page Guidelines

- Provide a positive user experience on landing pages.
- Disclose all promotional content as promotional content.
- Ensure all advertisements and third-party content comply with Realize Advertising Policies.

### Image Guidelines

| Requirement | Details |
|---|---|
| Resolution | Not blurry or pixelated; highest resolution possible. |
| Size | Minimum width 400px, minimum length 350px, no more than 5MB. |
| Relevance | Only images relevant to product, offering, and landing page. |
| Prohibited | No pornographic, defamatory, unlawful, or sexually suggestive content. No "before and after" images. No celebrities or politicians without permission. |

### Landing Page Checklist

| Element | Requirement |
|---|---|
| **Length** | 400-600 words. |
| **Design** | Clean and simple: simple black font on white background. |
| **Images** | Add a picture at the beginning or midway to make the page inviting. |
| **Readability** | Bold subheaders, big fonts, short paragraphs. |
| **CTA placement** | Place the same CTA button multiple times across the page to remain visible throughout scroll — simpler to implement and track as a single conversion. |

### Title and Text Guidelines

- Branding text must accurately reflect the source of the content.
- Thumbnails must not show before / after photos.
- Thumbnails must not be poor quality or very low resolution.
- Titles must not be misleading — must accurately reflect the landing-page subject.
- Titles must not be in all capital letters or contain excessive punctuation.

---

## Creative Review Process

### Content Review Policy

Every campaign item submitted to the network is reviewed and labelled to ensure it meets Advertiser Policy.

### Prohibited Content

- Do not promote anything offensive, threatening, or inappropriate.
- Do not promote anything dangerous or that promotes dangerous behaviour.
- Do not promote anything with false promises, scams, or illegal activity.

### Restricted Content

All restricted content, products, and services must comply with additional restrictions **and** applicable laws and regulations of every targeted location.

### Best Practices for Faster Approval

- Follow all advertiser policy guidelines before submission.
- Use **Gen AI AdMaker** — improves approval rate by approximately 50% due to built-in policies.
- Ensure ads avoid mature themes, distasteful imagery, aggressive promises, or close-ups of body parts.

### Reading why something was rejected

`get_campaign`, `list_campaigns`, `get_item` and `list_items` each return a read-only
**`policy_review`** object next to `approval_state`. It is normally present on a rejected object; when
it is not, say the reason was not returned rather than supplying one.

**A campaign and an item do not carry the same fields.**

| Field | Campaign | Item | Carries |
|---|---|---|---|
| `reject_reason` | yes | yes | The policy code. **Internal — never show it to the user.** |
| `reject_reason_description` | yes | yes | The reason in readable form. This is the line to show the user. |
| `reviewer_notes` | always null | yes | A reviewer's written explanation when one exists — often names the exact fix |
| `policy_review.status_reason` | no | yes | The **Need To Edit** reason when the item is in that state (`DUPLICATE`, `NO_TITLE`, `NO_THUMBNAIL`, `NO_URL`, `TIMEOUT`, `IMAGE_WITHOUT_LICENSE`); null otherwise |

**Reviewer notes are only ever populated on items** (verified against the platform source 2026-11-03: the campaign serializer sets the two reason fields and nothing else). A campaign-level rejection gives you a reason and no note — if the user needs the detail, it is on the items, via `list_items`. Note an item also has a **top-level** `status_reason` that is a different field with a different set of values; the one above is the one inside `policy_review`.

**Never report a rejection without its reason.** "This item is rejected" alone leaves the user to
guess, and the answer is already in the payload in hand — there is no second call to make.

**And a rejection is not the end of the ad.** Editing a rejected ad resubmits it for review, so the
reason is something to act on, not just to report. Offer the fix. The ad will not go live on that
write — it goes back into review — and some accounts limit how many times one ad can be resubmitted,
so a replacement is the fallback once that limit is reached.

- **`reviewer_notes` is null on most rejected objects, and is the user's own text to act on when it is not** — quote it, never compress it. Report what carries a value; say the reviewer left no note rather than reading one out of the
  code name. If `policy_review` is absent on something that reads `REJECTED`, or present with every
  field null, say the reason was not returned — there is no second call that fetches it, and the
  status is not a reason.
- **The description is canned text for the code, not a report on this campaign.** It is looked up
  from a table, one fixed sentence per code, so quote it as given but **never read it as a list of
  this campaign's actual faults**. `CAMPAIGN_SUBMISSION_ERROR`, for instance, carries a stock sentence naming two
  possible causes — "Broken landing page URL; No items in campaign" — and telling the user they have
  both is asserting defects the platform never recorded. Say what the code means and let them check
  which applies.
- **A code with no description of its own falls back to the platform's default text**, which may be
  a stock sentence or may be nothing at all. Either way it does not describe this rejection, so say
  the reason was not given rather than reading the fallback out as the finding.

A campaign payload usually also carries **`inventory_summary`** (`number_of_items`,
`number_of_approved_items`, `number_of_reject_items`). Useful, with four limits worth knowing:

- **Approved is not running.** An approved-but-paused ad counts as approved. To say a campaign is
  partly live rather than merely partly approved, read item `status` from `list_items`.
- **There is no pending count.** Pending is total minus approved minus rejected.
- **It can be missing entirely** on credentials without the inventory-summary permission.
- **`0 / 0 / 0` does not mean "no ads", and `list_items` will not settle it.** The count covers the campaign's own
  attached ad rows once they are fully registered — an ad awaiting approval *is* counted, a deleted one is not — and the
  zeros are *substituted* when there are none, so the field is present and reads zero rather than going absent. Three
  kinds of campaign read zero while perfectly healthy:
  - a **catalog** campaign, whose products are not ad rows at all, reads zero for its whole life;
  - a campaign whose ads are **still being crawled**: a newly added ad is not counted until its crawl resolves, so a
    campaign set up minutes ago reads zero. (On accounts with the creative library switched on a new ad is registered
    immediately, so that gap does not arise there.)
  - an **RSS** campaign reads zero until its feed is first read; after that its generated ads are counted.

  An ad placed from the **creative library** is an ordinary attached ad, counted from the start, so a library campaign
  reading zero really is empty. **No field on the campaign payload separates any of these from a genuinely empty
  campaign** — `campaign_item_type` looks like it should, but it is a one-way latch set on the first ad and never reset,
  so all of them sit on one of the `HAS_NO_ITEMS*` values (there is one per ad format, so test the prefix, not the bare
  `HAS_NO_ITEMS`). `list_items` does not resolve it either: it returns nothing at all for a catalog campaign, and on an
  RSS campaign it lists the feed while hiding the generated ads, so `number_of_items` there can far exceed the rows
  `list_items` returns — that gap is by design, not a bug. So never call a campaign empty on a `0 / 0 / 0`: say it has no
  counted ads, and ask whether it runs on a product catalog or an RSS feed, or was only just set up. The user knows;
  nothing in the payload does. A **non-zero** total with `number_of_approved_items: 0` is the trustworthy case — there,
  nothing really is approved. (Counting query, crawl path and the library and RSS paths verified against platform source
  2026-11-04; the catalog case is inferred from catalog ads living outside the counted table, not from a line that
  states it.)

---

## Creative Testing & Refresh

### Testing Strategy

| Rule | Details |
|---|---|
| **Always-on testing** | Include different ad messaging variations and formats (static, motion, carousel). |
| **LP testing** | Pair creative messaging with tailored landing pages and monitor performance. |
| **Format experiments** | Test different ad formats and measure performance. |

### Creative Fatigue

Creative fatigue is one of the most common reasons for performance plateaus. Creatives experience fatigue when the ad is shown to the same user many times. The algorithm adapts to the CTR decline and uses it to predict future performance.

**When noticing fatigue:**

- Add creative variations across formats (static, motion, carousel).
- Experiment with new messaging angles.
- Consider adding Display if it's not part of the current mix.
- Make the refresh **significant** — not just a word or two. The goal is to present a different angle the audience hasn't seen.

### Narrow Targeting + Fatigue

Narrow-targeted campaigns suffer **more** from audience and creative fatigue. Refresh creatives more often on narrow campaigns.

---

## Guardrails

- Never launch a campaign with fewer than 4 creatives (recommend 4-6, max 10).
- Never use misleading or sensational titles — they get rejected and waste budget.
- Never use "before and after" images.
- Never feature celebrities or politicians without explicit permission.
- Never use AI-generated creatives without human review (despite higher approval rate).
- Always ensure the landing-page message matches the ad creative.
- Always include motion ads in the creative mix — up to 20% higher CVR.
- Always place CTA buttons multiple times across the landing page.
- Always refresh creatives significantly — a word change isn't enough.

## Common Mistakes

1. **Too few creatives.** Algorithm has nothing to test. 4-6 per campaign, 3 distinct titles + 3 unique images.
2. **Misleading titles.** Creative rejection + high bounce. Write compelling but honest titles.
3. **Same messaging for all audiences.** Low relevance. Create separate campaigns for distinct customer groups.
4. **Missing display sizes.** Reduced reach. Prioritise at least 300×250 and 300×600.
5. **Never refreshing creatives.** Fatigue kills performance. Significant refresh, not just minor word changes.
6. **Display driving to generic homepage.** Lower CVR. Drive to product page (or advertorial if education is needed).

## Pro Tips

- Motion ads can be auto-generated from static assets using AI tools — no design expertise needed. Always include at least one motion creative.
- Gen AI AdMaker improves creative approval by approximately 50% — use it as a starting point for faster launches.
- Keep Ad Optimisation mode enabled — it automatically prioritises top-performing creative combinations.
- For display, the default is to drive directly to the product page. Use advertorial pages only when the product needs additional education.
- Social Importer is a fast-start: import Meta ads (300×250 and 300×600), see which formats work, then expand.
- Narrow-targeted campaigns need **more frequent** creative refresh — fatigue hits faster with smaller audiences.
