# pack-aws-clf — a quizmill learning pack

Practice for the **AWS Certified Cloud Practitioner (CLF-C02)** exam
(65 questions, 90 min, pass 700/1000, scaled). This pack is a
**30-question sample** of the full bank, `aws-clf-full`: cloud concepts,
security and compliance, core AWS services, and billing, pricing and
support, across the Easy, Hard and Very hard tiers.

Live at <https://aws-clf.quizmill.dev>.

The app's upgrade card (on Home, and in Settings → Packs) links to the full
bank, and the manifest names it (`upgrade.packId`, with `upgrade.unlockUrl`
as the service), so a licence key for `aws-clf-full` unlocks it **in place**
next to the sample, with progress kept per pack.

> **Unofficial.** Not affiliated with or endorsed by AWS. This is community
> study material — every question is `reviewStatus: "draft"`; cross-check
> against the AWS docs and the official practice set.

## Where the questions come from

Every question is **original** (`source: "original"`), written for the full
bank from the public AWS documentation and the official exam guide — no
community banks, official practice questions or dumps. Each one's
`sourceRef` is the AWS doc page it rests on, and its explanation ends with a
"Read more" link to it. See [`NOTICE.md`](NOTICE.md).

The 30 here are copied **verbatim, by id**, from the full bank, with the 22
concept cards they link to. Ids are the full bank's own
(`aws-clf-<tier>-d<domain>-<n>`), so every id in the sample exists in the
full bank and progress carries over.

## Categories & tiers

The categories are the exam guide's four content domains, with its weights.
The sample is drawn in proportion to them:

| Domain | Weight | Sample (Easy / Hard / Very hard) |
| --- | --- | --- |
| 1 · Cloud Concepts | 24% | 7 (3 / 3 / 1) |
| 2 · Security and Compliance | 30% | 9 (3 / 4 / 2) |
| 3 · Cloud Technology and Services | 34% | 10 (3 / 5 / 2) |
| 4 · Billing, Pricing, and Support | 12% | 4 (1 / 2 / 1) |
| **Total** | | **30 (10 / 14 / 6)** |

### How the sample was chosen

- **Every task statement.** All 15 of the guide's tasks (1.1 – 4.3) have at
  least one question.
- **Every tier**, in roughly the full bank's mix: 10 Easy, 14 Hard, 6 Very
  hard.
- **Both answer formats.** Four of the 30 are "Select TWO".
- **One concept per question**: no two of the 30 share a key.

The sample is frozen: a fix to one of these 30 lands in both repos, but new
questions go to the full bank only.

## Use it

```
npx quizmill run quizmill/pack-aws-clf   # straight from GitHub
npx quizmill run .        # http://localhost:3000
npx quizmill validate .   # schema + cross-reference checks
```

To deploy as its own app, `.github/workflows/deploy.yml` builds it onto the
quizmill engine (static app in `aws-clf-app/`, named after the manifest id)
and publishes to Cloudflare Pages (project `aws-clf`, custom domain
`aws-clf.quizmill.dev`) once the repo's `CLOUDFLARE_*` secrets are set.
`.github/workflows/ci.yml` validates every PR.
