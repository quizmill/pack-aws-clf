# Notices

## Original questions

Every question in this pack has `source: "original"` (ids
`aws-clf-<tier>-d<domain>-<n>`). They were written for this pack and are
not derived from any community question bank, from AWS's official practice
questions or Official Pretest, or from any third-party practice exam or
"dump". Each one is grounded in the public AWS documentation page named in
its `sourceRef`; the AWS docs are cited, not reproduced.

Community study posts were read only to see which topics and traps
candidates report (shared responsibility edge cases, support plans, the
Well-Architected pillars, analytics services); no item's wording comes from
them.

## Exam blueprint

The manifest's `exam` block and category weights come from the official
exam guide and certification page, checked on 2026-10-26:

- **AWS Certified Cloud Practitioner (CLF-C02) exam guide**
  <https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html>
  - "The exam includes 50 questions that affect your score." and "The exam
    includes 15 unscored questions that do not affect your score." —
    65 questions in total (`exam.questionCount: 65`).
  - "Your results for the exam are reported as a scaled score of
    100–1,000." and "The minimum passing score is 700." — `exam.passPct: 70`
    with `exam.scaled: true` (the raw-to-scaled mapping is not public, so
    the app's readiness estimate is a raw-accuracy target, not a scaled
    score).
  - Content domains, used as this pack's categories with their weights:
    Domain 1 Cloud Concepts (24% of scored content), Domain 2 Security and
    Compliance (30%), Domain 3 Cloud Technology and Services (34%),
    Domain 4 Billing, Pricing, and Support (12%).
  - Each question's `task-N.N` tag is the guide's task statement it
    exercises (Task 1.1 "Define the benefits of the AWS Cloud" through
    Task 4.3 "Identify AWS technical resources and AWS Support options").
- **AWS Certified Cloud Practitioner certification page**
  <https://aws.amazon.com/certification/certified-cloud-practitioner/>
  - "Exam duration 90 minutes" (`exam.durationMinutes: 90`; the exam guide
    itself does not state a duration) and "65 questions; either multiple
    choice or multiple response".
- **AWS Support plans** <https://aws.amazon.com/premiumsupport/plans/>,
  checked on 2026-10-26, for the current plan names (Basic Support,
  Business Support+, Enterprise Support, Unified Operations) used in
  Domain 4 questions.

## Not included

No AWS-copyrighted material is included in this pack. AWS Skill Builder's
official practice questions, the Official Pretest, and any commercial
question banks are proprietary and are **not** redistributed here. Study
those directly on AWS Skill Builder — they are the authoritative source.

AWS and the AWS certification names are trademarks of Amazon.com, Inc. or
its affiliates. This pack is unofficial and not affiliated with or endorsed
by AWS.
