# TakeMeter

> ### 👋 Start here
>
> **New to this repo? Read [RUNNING.md](RUNNING.md) first** — setup, the
> notebook, the baseline, and what to do when something breaks.
>
> Once `python test.py` passes:
>
> ```bash
> head -5 data/practice_labels.csv     # the shape your labels.csv needs
> ```
>
> Then open `takemeter.ipynb` **in this folder** — in VS Code, or with
> `jupyter notebook` if you prefer. Pick the kernel: the `.venv` inside this
> project. Run section 1, which reports the hardware you'll be training on.
> Everything else waits until you have data.
>
> Nothing to upload, nothing to connect, no accounts and no keys. The notebook
> runs on your machine and writes next to your code.
>
> **The rest of this file is your submission.** Fill it in as you go.

---

<!-- ─────────────────────────────────────────────────────────────────────────
     HOW TO USE THIS FILE

     Unit 5 asks for the first five sections. Unit 6 adds the five below them.

     Everything is pasted as TEXT. No screenshots, no images.

     ⚠️ The confusion matrix especially. The notebook prints one as a markdown
     table, ready to copy. A screenshot of a matrix earns nothing. Paste the
     table.
     ───────────────────────────────────────────────────────────────────────── -->

<!-- ═══════════════════════ UNIT 5 — THE BUILD ═══════════════════════ -->

## What This Does

<!-- Your community, and what your classifier sorts posts into. Three or four
     sentences. -->



---

## Label Taxonomy

<!-- Each label: a one-sentence definition and two real examples from your
     reading. Then your decision rule for the hardest boundary.

     The decision rule is worth a point on its own and it's the thing most
     people leave out. Every taxonomy has a hardest boundary. Name yours. -->

### `Personal Narrative`

**Definition:** Posts about personal stories, past memories, or personal experience, the focus of the story will mention what the person feels and experienced.

**Example 1:** Is the album really dead?
> Like actually. I've spent the last two years making what I think is my life's greatest work, only to realise the world in which I live values this craft less and less. I mean I'm guilty of it too, listening to records just isn't what it used to be, but I try. Yet here we all are making them as though nothing has changed. How depressing! I don't mean to be dramatic, I know the fire will always burn, but it flickers now in the winds of time.

**Example 2:** Kind folks of reddit, what do you think of Streetlight Manifesto?
> The first track i heard was around the time i quit weed for good. It's also the first artist that made me like brass instruments.
I love Toh Kays songwriting yet i tend to forget about them ever so often. I feel my main problem is that the lyrics are often way to fast to sing along but they are so bloody good and interesting compared to other 3rd wave ska bands like Less Than Jake or Mad Caddys. Kinda feel like they are so underraded. It's not really Ska nor is it Skapunk. They are kinda unique and have such a bloody good brass section.
And now roast me :)

### `Deep Analysis`

**Definition:** Posts that focus heavily on music production, historical evolution of artist or music.

**Example 1:**The long instrumental outro on “People Make the World Go Round” might be the real heart of the song
> The long version of “People Make the World Go Round” has a whole second half, and I think it’s the best part

https://youtu.be/2owZXPyeilc?si=pq2Q5CoSjFxLEqN-

Most people probably know “People Make the World Go Round” from the single, which is around 3:30.

That version is already great. Thom Bell’s arrangement, Linda Creed’s lyrics, Russell Thompkins Jr. singing in that ridiculous falsetto.

But the album version on The Stylistics’ first record is over six minutes long, and right around the point where the single fades out, it just keeps going.

And honestly, that’s the part I like the most.

The vocals slowly disappear and the whole thing opens up. Bass, drums, congas, all those strange Bell percussion sounds, then guitar and flute drifting in and out.

It doesn’t really feel like it’s trying to get anywhere anymore. It just sits in the groove.

That part hits me more physically than the first half. It’s hard to explain without sounding slightly ridiculous, but it feels like the song starts breathing differently.

The lyrics are actually pretty bleak. Strikes, garbage piling up, pollution, Wall Street losing money. The whole world is dysfunctional.

Then the words disappear and the music just keeps going.

To me it almost feels like the song is saying: yeah, the world is a mess, but it keeps turning anyway.

That’s obviously just my interpretation, but once I started hearing it like that I couldn’t really unhear it.

I also found something interesting about the rhythm.

I assumed the long instrumental part felt more relaxed because it probably settled into a simple 4/4 groove. Apparently not. The ending vamp has been analysed as alternating between 4/4 and 5/4.

Which is kind of funny, because it feels more relaxed even though the meter is actually less regular.

Maybe that extra beat is part of why it feels so loose, like the music is constantly hanging around a little longer than you expect.

The song also seems to have really appealed to jazz and soul-jazz musicians. Milt Jackson did an eight-minute version, Cleveland Eaton covered it, O’Donel Levy did a great guitar version, and it kept resurfacing later in hip hop and sample culture.

I don’t want to claim all those musicians were specifically obsessed with the long Stylistics outro, because there’s no way to know that. But it does feel like there was something in the composition that musicians wanted to stretch out and live inside.

Does the long outro change the meaning of the song for you, or does it just feel like an extended groove?

And for anyone here who understands the meter better than I do, why does that 4/4 and 5/4 vamp feel so relaxed when the rhythm is actually becoming less regular?

If you only know the short version, let the album version keep running past the point where the single would have faded out.

That’s where the song really starts for me.

**Example 2:** What new technology will create new genres in the next 10 years?
> The home DAW made it so anyone could produce a decent enough sounding record in their bedroom. Indie, folk, hip-hop, ambient, and of course EDM all evolved to survive in this new landscape?

What technology will revolutionize music production?

Will we see electronic remixes of machine learning compositions?

Will telepathic midi control become a staple of EDM?

### `Philosophical Discussion`

**Definition:** Posts about broad culture, or artistic questions about music.

**Example 1:**Why did major American bands like the Grateful Dead, Dave Matthews Band, Tom Petty and the Heartbreakers, Journey and Van Halen fail to break through in Europe?
> Van Halen could sell out stadiums in the US, yet in Europe they had to open for Bon Jovi. That would never happen in the States.

DMB could easily sell out the biggest arena in my country (Portugal), but I doubt they have much of a fanbase in the rest of Europe. My dad is a huge fan of 70s rock, and he tells me Van Halen and Journey were never particularly big over here. And FUNNILY ENOUGH, he'd never even heard of Tom Petty...

**Example 2:** Why didn't people hate trap in the 2010s as much as they hated disco in the 70s?
> Trap music was essentially as dominant in the 2010s as disco was in the 70s. Yet people didn't walk around chanting "TRAP MUSIC SUCKS". There was no "trap music demolition night" because of its massive popularity. Yes, disco was huge in its time... but so was trap music. What was with the weird ass hatred disco inspired back in the 70s where people felt the need to destroy it and making it a personality trait?

Was the last time open, public hatred of popular music was socially acceptable the Justin Bieber hate of the early 2010s?

### The hardest boundary

**Which two labels:** Deep Analysis and Philosophical Discussion posts

**The post:** Is the musical bridge an overused function in pop songwriting?
> Just a thought that popped into my head. I guess it's cultural how I never really noticed how much bridges are used in traditional song structures in the West.

I understand their function, I think. They provide a nice contrast from the verse and chorus, and the key change generally resolves nicely back into the original key. You can contrast this to songs where there is no bridge, but the second to last chorus is in a different key.

I won't argue that putting a bridge in every song is too formulaic because pop music in general is formulaic, just as most catchy and easy listening music is. However I'm wondering if it hampers the goal of a pop song. It doesn't really add anything new that's catchy, and it doesn't add more to the song than if one of the choruses was in a different key.

Of course there are plenty of songs where the bridge is fantastic and is almost like a second chorus. But many times this isn't the case.

For example I just heard "This Love" by Maroon 5 on the radio. I really like that song and I think it's every definition of what a good pop song should be. But the bridge just feels forced, you know? Like the producers/songwriter is like "oh yeah we need a bridge" and throw something in.

I guess what I'm getting at is that too many bridges feel like they only exist because that's what's expected in a usual song. I think this hurts a song more than it helps

**The decision rule I used every time:**
If the post's primary focus is on analyzing the instruments, chord progression, key changes, then the post is for Deep Analysis. If it mainly focuses on song trends, industry habits without a detailed breakdown of the musical mechanics, the post will be categorized as Philosophical Discussion.



---

## The Dataset

<!-- Where you collected from, how you labelled, your counts, and three hard
     cases. -->

**Where the posts came from:** The post came from reddit subpost called LetsTalkMusic. Here is the link: https://www.reddit.com/r/LetsTalkMusic/

**How I labelled them:** <!-- Cold first? Pre-labelled with AI and corrected?
Say so plainly — the disclosure is required, not penalised. -->

**Counts per label:**

| Label | Count | Share |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |
| **Total** |  | 100% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**2.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**3.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

---

## The Training Run

<!-- Your starting model, your settings, and anything you changed and why. -->

**Base model:**

**Settings:** <!-- epochs, learning rate, batch size, seed -->

**Anything I changed from the defaults, and why:**

**Split sizes:** <!-- train / val / test, and per-label counts in the test
split. If a label had fewer than about 8 in test, say so — it explains a lot
of next unit's variance. -->



---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Moment 2**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Pre-labelling disclosure:**

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy |  |  |  |
| Macro F1 |  |  |  |
| F1 — `label_one` |  |  |  |
| F1 — `label_two` |  |  |  |

**What I predicted before I looked:**
<!-- Milestone 1 asks you to write this BEFORE seeing the trained numbers. A
     prediction made afterwards isn't one. -->

**What the gap actually means:**
<!-- If the baseline matched your trained model, your fine-tuning added
     nothing — and that is a real finding, not a failure. Say it plainly. -->



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

| true \ predicted |  |  |  |
|---|---|---|---|
| **** |  |  |  |
| **** |  |  |  |
| **** |  |  |  |

**My biggest off-diagonal number, and what it means:**
<!-- Not "the model made mistakes" — WHICH boundary it didn't learn, and which
     direction. "7 real analysis posts were called hot_take and only 3 went the
     other way" is a direction, not just an error rate. -->



---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |

**Diagnoses**

<!-- For each miss: the cause, and how you know. The four common causes are:
     too few examples for a label, a boundary you applied inconsistently, a
     genuinely hard label pair, and a task the model can't reach from this
     much data.

     ⚠️ Use your agreement report as evidence. It is the only instrument you
     have that can tell a LABELLING problem from a MODEL problem, and this
     section is graded on whether you used it that way. -->



---

## Agreement Report

<!-- Your rate against the staff set, and every disagreement adjudicated.

     Remember you labelled these 30 under the STAFF taxonomy in
     data/staff_taxonomy.md, not your own — so every argument below is made
     from those definitions and those decision rules. -->

**Agreement rate:** ___ / 30 = ___%

<!-- Nobody grades this number. A 60% who argues every disagreement from the
     stated rules beats a 95% who wrote "staff was right" nine times. Several
     of the 30 were chosen because they're genuinely ambiguous — you should be
     winning some of these. -->

**Disagreements**

<!-- Three lines each: the post, both labels, and who you think is right and
     why — grounded in the staff definitions you were both applying.

     Then sort each into one of three piles:
       (a) the rule covered it and I applied it loosely → a consistency problem
       (b) the rule genuinely doesn't say               → a gap in the definitions
       (c) the rule is ambiguous here and my reading is defensible → argue it.
           This is a legitimate win.

     Pile (a) is the one that matters most for your diagnosis: if you applied a
     written rule two different ways on 30 posts, that is direct evidence about
     what you did across your own 200. -->

**1.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**2.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**What the pattern in my disagreements tells me:**



---

## The Improvement

**What I changed:**

**Which diagnosis pointed at it:**

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->



---

## What's Still Broken

<!-- For each criterion still missed: what you'd do, and why you stopped. -->



**The gap between what I meant my labels to capture and what the model
learned:**
<!-- Two sentences. Your confusion matrix is the evidence. -->



<!-- ═════════════════════════════════════════════════════════════════════

     SUBMISSION CHECKLIST — unit 5

       [ ] criteria.md has five numbered criteria, each naming a NUMBER
       [ ] Each has a reason underneath tied to your data or taxonomy
       [ ] labels.csv: at least 150 rows, text/label/note, ONE file not split
       [ ] No label above 70%
       [ ] All five unit 5 sections have real content
       [ ] Label Taxonomy includes the decision rule for your hardest boundary
       [ ] The Dataset includes three hard cases
       [ ] results.json and test_split.csv committed (the notebook does this)
       [ ] At least four new commits
       [ ] Repository URL submitted — WRITE IT DOWN

     SUBMISSION CHECKLIST — unit 6

       [ ] Baseline vs. Trained table, with your prediction written beforehand
       [ ] Run Log — Before, five criteria across three seeds
       [ ] Confusion matrix TYPED AS A MARKDOWN TABLE
       [ ] A verdict on every criterion
       [ ] A diagnosis for every miss, using the agreement report as evidence
       [ ] Agreement Report with every disagreement adjudicated
       [ ] One improvement, with Run Log — After
       [ ] What's Still Broken
       [ ] results_three_seeds_before.json, results_three_seeds_after.json,
           baseline_results.json and
           agreement_results.json committed
       [ ] At least four new commits
       [ ] The SAME repository URL as last unit

     Do not delete and recreate this repository.
     ═════════════════════════════════════════════════════════════════════ -->

---

📖 **How to run this project: [RUNNING.md](RUNNING.md)**
