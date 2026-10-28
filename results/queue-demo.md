# Weekly ops runbook - 2026-W44
Queue items: 4   Programs: 2   Skills matched: 31 of 50   Plan steps: 24

Thin coverage (no matched skill in these phases): portfolio

## program

duplicate-policy-review  (match 2)
  Understand how a program treats duplicates, race conditions and partial findings before you hunt, because duplicate rules decide whether popular surfaces are worth your hours at all
   1. Locate the duplicate rule in the policy and platform page, quoting it verbatim in your notes.
   2. Determine whether first-submitted or first-confirmed wins, because the two reward entirely different working styles.
   3. Check what partial credit exists for unique variants, such as a different root cause reaching the same impact.
   4. Estimate crowd density from the program's public bounty count versus its scope size and popularity.
   5. Decide whether to race on popular surfaces or to pursue angles where fewer hunters can arrive first.
   6. Log the rule and your strategy choice together so later results can be attributed to the decision, not to luck alone.

program-fit-scoring  (match 2)
  Score every candidate program against your real skills, access and payout expectations before spending a research hour, so limited capacity flows to programs you can actually win in
   1. List every program under consideration with its scope size, asset types, payout range and published response times.
   2. Score your own fit per program: matching expertise, tooling you already own, and whether the assets are reachable from your position.
   3. Weight payout against effort using your historical data, not the program's advertised maximum bounty.
   4. Record the score with one sentence of reasoning so a later review can challenge the judgment instead of re-deriving it.
   5. Rank programs and cut anything below your fit threshold, keeping the cut list with reasons rather than deleting it.
   6. Re-score whenever a program changes scope, payout bands or response commitments, because fit is a moving property.

reward-structure-analysis  (match 2)
  Decode how a program actually pays, from bounty tables and duplicate rules to hidden multipliers, so expected value is computed from published terms instead of hoped-for maximums
   1. Extract the full bounty table: severity bands, payout ranges, and which bands the program has actually paid historically.
   2. Identify multipliers and modifiers such as quality bonuses, first-reporter rules and duplicate handling.
   3. Model duplicate loss using the program's published duplicate rule and your own acceptance history, not optimism.
   4. Compute expected value per severity band as payout times acceptance probability minus duplicate discount.
   5. Compare programs on expected value per research hour, using effort estimates you recorded from past engagements.
   6. Revisit the model when the program edits its table, since reward structures change more often than scope does.

program-health-and-signal-check  (match 1)
  Vet a program's operational health from public signals before investing research time, because a broken triage pipeline turns valid findings into unpaid, unanswered tickets
   1. Read recent public disclosure threads for the program and note time-to-first-response and time-to-fix distributions.
   2. Check whether the program answers scope questions at all, since silence during pre-sales predicts silence during triage.
   3. Look for signs of churn: repeated triage contacts, policy rewrites, or bounty table changes within a few months.
   4. Verify that accepted reports actually result in fixes, by matching disclosures to released patch notes or version bumps.
   5. Weigh positive signals such as published statistics and researcher testimonials against the negative evidence you found.
   6. Record a health verdict with the two or three observations that drove it, so a later recheck compares like with like.

safe-harbor-position-review  (match 1)
  Establish in writing what protection the program actually grants researchers before testing begins, so authorization, liability and exit terms are known rather than assumed
   1. Locate the program's safe harbor statement, terms of service and any separate testing addendum, and archive dated copies.
   2. Record exactly which actions are protected: scanning, exploitation, data access, social engineering and physical testing.
   3. Note the exclusions, because a safe harbor clause that omits data access protects far less than its headline suggests.
   4. Check the withdrawal clause and what event ends your authorization, such as a policy edit or a reported dispute.
   5. Write a one-paragraph position summary stating what you may do, what you may not, and who confirmed it.
   6. Re-read the archived copies whenever the program updates its policy, since protection can be narrowed without notice.

scope-clause-interpretation  (match 1)
  Read a program's scope clauses as a contract rather than a mood, resolving each ambiguous in-scope claim into a testable asset list before you send a single request
   1. Copy every scope sentence verbatim into an interpretation worksheet so paraphrase never becomes the working definition.
   2. Split each clause into the asset it names, the qualifier attached to it, and the conditions that void it.
   3. Mark each clause as explicit, inferred or disputed, and treat only explicit entries as authorized without confirmation.
   4. Write the narrowest reasonable reading and the widest plausible reading side by side for every ambiguous clause.
   5. Send the narrow reading to the program as a confirmation question and wait for the answer before testing the gap.
   6. Version the worksheet so a later scope edit shows exactly which interpretation changed and when.

## queue

dead-hypothesis-pruning  (match 1)
  Remove hypotheses whose assumptions no longer hold, with the falsification evidence recorded, so the queue reflects what is still testable rather than what was once plausible
   1. For each queue item, state the assumption it depends on and the evidence that would falsify that assumption.
   2. Test cheaply whether the assumption still holds, using a single request or a public changelog rather than a full session.
   3. Mark falsified items as dead immediately instead of letting them occupy ranked positions.
   4. Record what killed the item, with the observation, so future rounds do not resurrect the same idea.
   5. Re-check near-miss items whose assumption is weakened but not yet dead, and set a re-evaluation condition.
   6. Keep the queue pruned at each triage so dead weight never competes with live work for attention.

hypothesis-backlog-triage  (match 1)
  Run a recurring triage over your idea backlog so hypotheses are ranked, merged, split or killed on evidence rather than surviving indefinitely on the hope that they are promising
   1. Dump every backlog item with its creation date, current score and the last evidence attached to it.
   2. Merge items that describe the same underlying weakness from different angles, keeping the strongest framing.
   3. Split items that bundle several independent tests, because a compound item can neither be started nor finished.
   4. Kill items whose assumption has been falsified or whose target no longer exists, recording why each died.
   5. Re-score survivors against fresh information such as new scope, new tooling or newly observed behavior.
   6. Archive killed items instead of deleting them so future rounds do not resubmit the same dead idea.

signal-promotion-gating  (match 1)
  Promote a lead from observation to active queue item only when it clears declared evidence gates, so curiosity does not silently convert into committed research hours
   1. Define promotion gates in advance: in-scope confirmation, a testable hypothesis, an observable outcome and an effort band.
   2. Log every raw lead at observation time with the evidence that produced it, before judging its merits.
   3. Apply the gates mechanically at triage, promoting only leads that satisfy every gate on written evidence.
   4. Route ungated leads to a holding area with the specific missing gate named for each.
   5. Promote only as many leads as the week's capacity admits, ranking gated leads by expected value per hour.
   6. Audit promotions afterward to see which gates best predicted productive work, and tighten the ones that did not.

weekly-queue-construction  (match 1)
  Build the week's queue from a ranked hypothesis backlog with explicit entry criteria, so Monday starts with decided work instead of an open browser and a vague plan
   1. Collect every open hypothesis, target idea and pending follow-up into one candidate list without ranking yet.
   2. Score each candidate on expected value, effort estimate and confidence, using numbers you have used before.
   3. Drop anything that cannot be tested this week for reasons you write down, so the drop is a decision, not drift.
   4. Order the survivors by expected value per hour, then cut the list at your measured weekly capacity.
   5. Attach a session-sized first action to each queued item, because vague entries get skipped under time pressure.
   6. Carry unstarted items forward explicitly at the Friday review rather than letting them vanish by default.

## reproduce

cross-account-reproduction  (match 1)
  Prove a finding across distinct accounts and tenants so ownership and isolation claims rest on two independent identities rather than on one session's confused state
   1. Create two independent identities with no shared state, groups, teams or administrative links.
   2. Establish distinct owned data in each identity so ownership boundaries have something real to cross.
   3. Perform the triggering action as one identity and observe its effect on data owned by the other.
   4. Reverse the roles and repeat, confirming the boundary is consistently crossed rather than one-directional.
   5. Record identifiers for both sides of every crossing so the evidence shows exactly whose object moved.
   6. State in the report which direction worked, because asymmetric crossing often indicates a different root cause.

environment-matrix-reproduction  (match 1)
  Reproduce across a deliberate matrix of clients, accounts and configurations so the defect's blast radius is known before you describe it, not discovered during triage
   1. Define the matrix dimensions that could plausibly matter: browser, device, account role, plan tier and region.
   2. Select a minimal set of cells that separates the dimensions without exploding into full combinatorics.
   3. Run the reproduction procedure identically in each cell, changing only the dimension under test.
   4. Record a cell-by-cell result table with pass, fail or not-applicable for every combination tried.
   5. Identify the boundary: which dimension flips the behavior and which dimensions have no effect.
   6. Report the boundary as part of the finding, since the affected-surface claim depends on it.

flake-rate-measurement  (match 1)
  Measure how often a non-deterministic defect actually fires before reporting it, because an unquantified intermittent bug is the fastest way to lose triage credibility
   1. Define the trial: identical procedure, clean reset between attempts, fixed inputs and environment.
   2. Run a meaningful number of attempts, enough that the observed rate means something rather than one in three.
   3. Record every attempt with its outcome, timestamp and any variation you noticed, not only the successes.
   4. Compute the observed rate and a simple range so the claim is quantified instead of described as intermittent.
   5. Vary one suspected factor at a time to see which condition raises or lowers the rate.
   6. Report the rate, the trial size and the conditions, so triage knows exactly how hard reproduction will be.

minimal-repro-reduction  (match 1)
  Reduce a working reproduction to the smallest set of steps, fields and state that still triggers the defect, because triage trusts short repros and abandons long ones
   1. Start from the full working reproduction and identify each step, field and precondition it contains.
   2. Remove one element at a time, retesting after each removal, and keep the removal only if the defect still triggers.
   3. Record what each removed element actually contributed, since some elements affect severity rather than reproducibility.
   4. Repeat until no further removal keeps the defect alive, producing the minimal failing sequence.
   5. Verify the minimal version reproduces twice from clean state before adopting it as the canonical repro.
   6. Attach both versions when reporting: minimal for triage speed, full for context on how it was found.

prerequisite-chain-documentation  (match 1)
  Document every precondition a defect depends on, in order, so triage can rebuild your exact starting position instead of guessing at what state the test assumed
   1. List every precondition: account roles, feature flags, prior actions, data rows and entitlement states.
   2. Order the prerequisites so the chain can be executed top to bottom without improvisation.
   3. Mark which prerequisites are default, obtainable through the product, or requiring privileged access.
   4. State the time dependence: how long a precondition takes to establish and how long it remains true.
   5. Verify the chain by following it literally from a fresh environment and noting where the instructions were ambiguous.
   6. Attach the ordered chain to the report as its own section, separate from the trigger steps.

reproduction-consistency-reruns  (match 1)
  Re-run a finished reproduction on a separate day, session and vantage point to catch day-one luck before triage does it for you and files it as not-reproducible
   1. Set the finding aside for a defined interval so accumulated state and assumptions lose their grip.
   2. Re-run the full documented procedure from clean state, following only what is written, not what you remember.
   3. Note every point where the written procedure was ambiguous, then fix the procedure rather than your memory.
   4. Run the procedure from a second vantage point, different network or machine, to expose environment dependence.
   5. Compare outcomes across runs and record consistency explicitly in the report.
   6. If a run fails, treat the procedure as the suspect first and the defect as the second suspect.

## report

impact-quantification-framing  (match 2)
  Translate a technical observation into concrete business and user impact with numbers where honest numbers exist, because severity negotiations are won on impact, not on request cleverness
   1. State the primary harm concretely: what data, what action or what money is affected, and for whom.
   2. Quantify with observed facts: row counts visible, records per response, accounts affected by the boundary.
   3. Bound the claim honestly, naming what you did not test and what an attacker would still need.
   4. Distinguish demonstrated impact from plausible-but-untested impact and label each part of the report accordingly.
   5. Map the framed impact onto the program's severity scale with one line of reasoning per criterion.
   6. Keep a copy of the numbers you asserted so a later re-test can confirm they still hold after fixes.

report-structure-authoring  (match 2)
  Lay out a report so a tired triage engineer gets summary, impact, reproduction and evidence in that order, without hunting through prose for the four facts they need
   1. Open with a two-sentence summary: what is wrong, on which asset, and what an attacker gains.
   2. Follow with impact stated in the product's terms: data exposed, action performed, or money affected.
   3. Place the reproduction as numbered steps with preconditions separated into their own short section.
   4. Attach evidence inline next to the claim it supports rather than collecting everything at the end.
   5. Close with severity rationale and any remediation direction you can justify from the evidence.
   6. Cut every sentence that does not serve comprehension, because length costs triage time and your credibility.

severity-justification-drafting  (match 2)
  Derive severity from the program's published criteria with an explicit written rationale per factor, so the number arrives argued rather than asserted and survives the first challenge
   1. Read the program's severity definitions verbatim and note the factors each band actually keys on.
   2. Score each factor separately from your evidence: attack vector, prerequisites, impact, scope and user interaction.
   3. State the reasoning for every factor, including factors you could not test and how you treated them.
   4. Compute the band from the factors rather than starting from a gut number and justifying backward.
   5. Pre-write the counterargument a skeptic would raise, and answer it inside the rationale.
   6. Keep the factor notes with the report so a post-fix re-rating can reuse the same reasoning structure.

remediation-guidance-drafting  (match 1)
  Offer remediation direction grounded in the root cause you actually observed, framed as guidance rather than instruction, so triage gets a useful starting point without you overstepping
   1. Name the observed defect separately from your hypothesis about the underlying cause, keeping the two distinct.
   2. Ground the hypothesis in evidence: which response, which code path signature, which behavior pattern suggested it.
   3. Describe the class of fix, such as enforcing an ownership check at a query boundary, without prescribing implementation.
   4. Note where else the same class likely appears, since one observed instance usually marks a pattern.
   5. Flag anything you tested that suggests a fix would be incomplete, such as a second path with the same behavior.
   6. Keep the tone advisory so the owning team can translate guidance into their architecture without contortion.

## followup

bounty-amount-verification  (match 3)
  Verify the awarded bounty against the program's published table and your argued severity, so a misapplied band is caught within the payout window rather than accepted silently
   1. Pull the current published bounty table and note the band boundaries that applied at submission time.
   2. Confirm the severity that was actually assigned, which may differ from the severity you argued.
   3. Compute the expected amount from band and any modifiers such as quality bonuses or first-reporter rules.
   4. Compare expectation against the offer, checking band, currency and any platform fee deductions.
   5. Raise a discrepancy within the program's stated window with the table, band and calculation attached.
   6. Log the final amount and any correction so your reward model uses settled numbers rather than offers.

triage-response-handling  (match 3)
  Process a triage reply as a decision point rather than an email, classifying it into accept, clarify, duplicate or dispute with the next concrete action already named
   1. Read the reply fully before acting, since partial reads turn clarifications into premature defenses.
   2. Classify it into one of accept, clarify, duplicate, downgrade or reject, and record the classification.
   3. Identify the specific question or decision the reply contains, which is usually narrower than its tone.
   4. Prepare a response that answers only what was asked, with evidence attached rather than restated.
   5. Set the response deadline from the program's stated timeline and put it in your queue, not your memory.
   6. Log the outcome against the program so your health and payout models absorb the real signal.

clarification-loop-management  (match 2)
  Keep clarification rounds short and bounded by answering the whole question each round, tracking open asks on both sides, and escalating when a loop stops converging
   1. Track every open question on both sides in one list, so nothing is answered twice or dropped.
   2. Answer all of a round's questions in a single reply rather than dribbling responses across days.
   3. For each answer, attach the evidence directly instead of referencing an attachment from an earlier round.
   4. Detect when answers are being requested repeatedly in different words, which means your last answer did not land.
   5. Summarize the state after each round in two lines so both sides share one picture of where the loop stands.
   6. Declare the loop stalled after a set number of rounds with no progress, and name the escalation path.

duplicate-claim-negotiation  (match 2)
  Respond to a duplicate verdict by testing whether it is truly the same root cause, and by arguing the narrower case where your finding proves something the original did not
   1. Obtain the original report's stated root cause and impact, or the platform's summary, before arguing anything.
   2. Compare root causes first, since shared symptoms with distinct causes are usually not true duplicates.
   3. Compare impact, asset and prerequisite differences item by item and write down which differences are real.
   4. If overlap is genuine, concede the duplicate plainly and ask what partial credit or acknowledgment applies.
   5. If overlap is partial, present the specific difference: different path, different prerequisite or different impact.
   6. Record the verdict and the program's duplicate rule interpretation for future expectations.
