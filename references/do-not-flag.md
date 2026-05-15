# Do Not Flag: Restraint Reference

Read this during Pass 3 (self-audit). Its job is to stop the single most
damaging failure of any humanizer: over-editing that strips the fingerprints
of a real writer and replaces them with smooth, average prose. Smooth average
prose is itself an AI tell. When this file and tell-patterns.md disagree about
a span, this file wins.

## Part 1: Not tells on their own

These are weak signals. Treat each as a tell ONLY when it recurs across the
piece or co-occurs with several others. In isolation, leave them alone.

- **Perfect grammar.** Plenty of humans write clean prose. Correctness is not
  a confession. Never introduce errors to "look human."
- **A single em dash.** One or two in a whole piece is ordinary punctuation.
  Only dash *frequency and monotony* is a tell.
- **Curly quotes / smart apostrophes.** Word processors and CMSs insert these
  for millions of human writers. Normalize only for consistency with the
  surrounding document, never as evidence of AI.
- **Formal or elevated vocabulary.** Academics, lawyers, and careful essayists
  write formally. Register is not origin.
- **Common transitions.** "However," "therefore," "in addition," "for
  example" are normal connective tissue. The tell is mechanical *overuse* of
  the showy ones (moreover, furthermore) in a fixed rhythm, not their
  existence.
- **One passive sentence.** Passive is correct constantly (unknown agent,
  object is the topic, scientific register). Only systematic agent-hiding is
  a tell.
- **One tricolon.** A single well-earned three-part list is good rhetoric.
  Only the *pattern* of compulsive threes is a tell.
- **A topic sentence.** Stating the point before supporting it is good
  exposition, not a machine artifact.

Rule of escalation: a lone weak signal stays. Two or more, clustered and
rhythmic, is the actual signature. When unsure, do not cut.

## Part 2: Human-writing markers to PRESERVE

These are the affirmative evidence that a person wrote something. They are
fragile and easy to "clean up" by accident. Removing one is the worst mistake
this skill can make. If a tell-pattern fix would erase any of these, do not
apply the fix.

- **Specific concrete details and numbers.** "the 4:15 from Reading,"
  "$1,840," "the second cubicle from the window." Specificity is the densest
  human signal there is. Never trade a real detail for a smoother sentence.
- **Mixed or contradictory feelings.** "I loved it and I never want to do it
  again." Models resolve to one clean valence; humans hold two. Keep the
  contradiction.
- **Time-bound and dated references.** "back when Twitter was still Twitter,"
  "before the 2021 rule change." These anchor the writer in lived time.
- **Idiosyncratic sentence-length swings.** A six-word sentence next to a
  fifty-word one. Do not regularize this. It is the rhythm of a mind, not a
  defect. Increasing this variance is a goal, not a problem to fix.
- **Self-corrective asides.** "well, actually," "or rather," "scratch that,"
  "I had this backwards." Models rarely self-interrupt. Humans do.
- **Unresolved tangents and mild digressions.** A parenthetical that wanders
  and does not perfectly close. Real thought is not always tidy.
- **Mild repetition for emphasis.** "It was wrong. Just wrong." Deliberate
  repetition is a rhetorical choice, not elegant-variation failure.
- **Regional, generational, or trade idiolect.** "that dog won't hunt,"
  "proper job," "send it," shop-floor or subculture vocabulary. This is voice.
- **Strong, unhedged opinion.** "This framework is a mistake." A flat claim a
  model would soften is a human marker. Do not add a hedge to "balance" it.
- **Profanity, slang, and informal contractions** where the register invites
  them. Do not launder voice into corporate neutral.

If you find yourself about to remove something because it is "a little rough,"
stop. Roughness that carries information or personality is the target state,
not the problem.

## Part 3: LLM idiolects (know the source, calibrate the fix)

Different model families cluster differently. Recognizing the dialect lets you
predict which tells will co-occur, so you diagnose faster and avoid
over-flagging neutral prose that merely resembles one trait.

- **ChatGPT / GPT family:** verbose; heavy hedging ("it is important to
  note"); collaborative artifacts ("Certainly! Let me know if..."); tidy
  rule-of-three; "In conclusion" / "Overall" wrap-ups; frequent em dashes;
  bolded key terms.
- **Claude family:** more concise but strongly parallel; clean tricolons;
  "Here's the thing" / "The key insight is" framing; balanced
  "on one hand / on the other"; measured, slightly diplomatic stance; section
  scaffolding.
- **Gemini family:** list-forward; many headers and inline-header bullets;
  boldface-heavy; compact declarative sentences; sometimes abrupt section
  transitions.
- **Grok family:** verbose with chatty asides and informal interjections,
  while still carrying classic artifacts (hedges, wrap-ups, signposting).

Use this to your advantage: if you see one ChatGPT trait, the cluster is
likely present, so audit for the rest. But do not flag, for example, ordinary
human conciseness just because conciseness is also a Claude trait. The dialect
is the *combination*, not any single feature.

## Part 4: Stop conditions (hard limits on every pass)

Do not apply a change if any of these is true:

1. **It changes meaning.** Any alteration to a fact, number, name, claim,
   causal relationship, hedge that carries real epistemic weight, or the
   author's evident intent. This includes *adding*: a fact, number, date,
   name, or example that was not in the source and was not supplied by the
   user is a fabrication even when it is plausible, and it is worse than the
   vagueness it replaced because it reads more human. If you concretized a
   thin sentence with a detail you do not actually know, remove the detail
   (shorten the sentence) or, if it might be true and matters, surface it as a
   question in the "Meaning check" section instead of asserting it. When any
   fix is ambiguous, ask there rather than guessing.
2. **It erases a specific detail.** A vaguer sentence is never an acceptable
   trade for a smoother one. Keep the detail; fix the sentence around it.
3. **It flattens a genuine quirk.** If removing a "tell" would also remove the
   thing that makes the prose sound like a particular person, leave it and
   note the tradeoff in "Deliberately left alone."
4. **It would introduce your own uniform rhythm.** If your edits are making
   every sentence resolve the same way (every fragment for punch, every fix a
   short-then-long pair), you are installing a humanizer signature. Stop and
   vary how you vary.
5. **The text is already human.** If a near-miss paragraph is just a person
   writing formally with a couple of dashes and a tricolon, the correct output
   is minimal or no edits plus an explicit "Deliberately left alone"
   explanation. A heavy rewrite of genuine human prose is a failure, not a
   success.

Restraint is not the absence of work. Naming what you correctly did not touch,
and why, is part of the deliverable and the strongest evidence the skill
worked.
