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
TakeMeter reads post from the subreddit (r/LetsTalkMusic). The subreddit includes several post about music. This program classifies each post by giving it a label from "Personal Narrative", "Philosophical Discussion", and "Deep Analysis". This program uses the DistilBERT model trained with 200 posts collected from the Lets Talk Music subreddit that is labelled. 



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

**How I labelled them:** I labeled the first 20 posts, and with AI's help I labeled the rest of the 180 posts. The posts are split into 3 labels, Philsophical Discussion, Personal Narrative, and Deep Analysis. 

**Counts per label:**

| Label | Count | Share |
|---|---|---|
| Philosophical Discussion | 108 | 54% |
| Personal Narrative | 48 | 24% |
| Deep Analysis | 44 | 22% |
| **Total** |  | 100% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:* Is the 21st century defined by genres that never go mainstream but impact pop music anyway? My daughter was listening to ""Say So"" by Doja Cat on YouTube. And I asked her to replay it because something sounded eerily familiar—as if I heard it before. Turns out, it sounds remarkably similar to the future funk song ""Fiona Coyne"" by Skylar Spence. If you're unaware, future funk is a genre that originated in the 2010s. It's basically a mix of disco and vaporwave. It has its following, but never cracked the mainstream. But hold on... ""Fiona Coyne"" is inspired by ""Love Talkin' (Honey It's You)"" by Tatsuro Yamashita, one of the heavyweights of city pop. City pop is what's known as a retronym. That is, a label we give to music when a retrospective canon gets formed, requiring recontextualization. Yacht rock is another example of a retronym. In Japan, where city pop originates from, city pop is an obscure genre even though city pop songs themselves are popular. That's because it was simply mainstream pop in Japan. Now don't get me wrong. ""City pop"" as a term existed in Japan during the 80s. But this wasn't a genre with a defined musical structure. It was more a marketing term to sell aspiration, much like how we in the West hear terms like ""contemporary"" and ""sophisti-pop"". Because of this, most Japanese people didn't recognize city pop as an identifiable thing . Fast forward to the 21st century. Westerners started hearing Japanese music from the 80s. They needed context. So they re-purposed a Japanese marketing term to define a corpus, a body of work that identified Japanese music with broad similarities that seemed to have an associated scene. The city pop canon was never big in the West. Even now, it's only known amongst music nerds. But its effect on modern mainstream music is huge . Here's examples: - ""Out of Time"" by The Weeknd samples Tomoko Aran's ""Midnight Pretenders"" - ""GONE, GONE / THANK YOU"" by Tyler, the Creator interpolates Tatsuro Yamashita's ""Fragile"" - ""We Ride"" by Brave Girls was a Top 5 K-pop hit, but it was blatantly marketed as city pop upon its release What's wild? City pop is not the only obscure genre to impact the mainstream but never hit the mainstream. Witch house, phonk, and vaporwave all had a big impact. But none of the artists who originated these genres have ever become house house names. I think this is one of the defining characteristics of 21st-century music. A genre can remain underground while its sounds, production techniques, and aesthetics become completely mainstream. We're in a time where the mainstream raids from subculture before subculture can ever challenge it. Is this why we no longer see musical revolutions like jazz, rock, punk, hip hop, and grunge? Has the mainstream become so good at absorbing underground music that new genres can influence it without ever displacing or fundamentally transforming it?

>
> *Could have been:* Philosophical Discussion
>
> *I chose, because:* I choose Deep Analysis because the author of the post analyzes the two songs in detail including the genre, and analyzes the history of different genres. 

**2.**
> *The post:*Is the album really dead? Like actually. I've spent the last two years making what I think is my life's greatest work, only to realise the world in which I live values this craft less and less. I mean I'm guilty of it too, listening to records just isn't what it used to be, but I try. Yet here we all are making them as though nothing has changed. How depressing! I don't mean to be dramatic, I know the fire will always burn, but it flickers now in the winds of time.

>
> *Could have been:* Philosophical Discussion
>
> *I chose, because:* I choose personal narrative because the author focuses more on what his experience is when making an album. 

**3.**
> *The post:*How did Snoop Dogg reach success so quickly with The Chronic and Doggystyle and can another artist duplicate what Snoop did in ‘92 and ‘93 by being the only artists in history to rise to superstardom that quickly? Snoop Dogg is the only artists in history to reach superstar status immediately as a solo artists. Only artists to reach success right away like Snoop was possibly The Beatles but even their debut album Please Please Me didn’t put up the #s like The Chronic and Doggystyle did. Gun N Roses debut album Appetite for Destruction is the highest selling debut album of all time but their debut album didn’t do well initially and it was a long process for Gun N Roses to be successful cause they were viewed too controversial with their music promoting too much sex and drugs. The band’s manager had to plead for MTV to play their music after several attempts of MTV of refusing to play their music and Guns end up getting good luck with MTV playing Welcome to the Jungle on a 5:00 AM Sunday morning which Guns eventually garnered success. 50 Cent Get Rich or Die Tryin surpass Doggystyle as the fastest selling debut album of all time with 50 Get Rich selling 872,000 the 1st week surpassing Snoop’s previous record of 806,000 the 1st week but at the same time 50 didn’t get success as an artists right away. 50 debut album was supposed to be Power of the Dollar and 50 had a small local buzz in NY with songs like How to Rob which wasn’t a hit song but garnered some success. But Power of the Dollar didn’t get release and was shelved by Columbia Records after 50 got shot 9 times and record labels felt 50 was too dangerous and labels didnt wanna to associate with him during this time after he got shot. It was a long process for 50 to get popular where he released several mixtapes after getting shot which got the attention from Dr Dre and Eminem to sign 50 on their label. But Snoop is the only artists I seen gain pop level of success right away with songs like Nothing but A G Thang, What’s my Name and Gin N Juice. What made fans gravitate towards Snoop right away? Is Snoop Dogg that more talented than other artists or did he have the best luck being at the right place right time or was Snoop able to finagle his way in the music industry in the easiest way possible as an industry plant? I am curious how Snoop became such a big artist right away without have any real previous bodies of work before The Chronic and Doggystyle. Can r/LetsTalkMusic tell me how Snoop Dogg was able to garner success so quickly as an artist?


>
> *Could have been:* Deep Analysis
>
> *I chose, because:* In the post the history of the albums are mentioned but it did not analyze the information in depth, therefore the post is only philosophical discussion. 

---

## The Training Run

**Test runs**
1. with default epoch, learning_rate, batch_size, and max_length

| Epoch | Training Loss | Validation Loss | Accuracy | F1 Macro |
|---|---|---|---|---|
| 1 | No log | 1.006 | 0.548 | 0.236 |
| 2 | 1.039 | 0.988 | 0.548 | 0.236 |
| 3 | 0.985 | 0.984 | 0.548 | 0.236 |

2. 
Epoch = 10, Learning_rate = 5e-5, batch_size = 8, and max_length = 128

| Epoch | Training Loss | Validation Loss | Accuracy | F1 Macro |
|---|---|---|---|---|
| 1 | 1.0376 | 0.9668 | 0.548 | 0.236 |
| 2 | 0.7918 | 0.8366 | 0.613 | 0.494 |
| 3 | 0.3293 | 0.8144 | 0.581 | 0.563 |
| 4 | 0.0952 | 1.0036 | 0.613 | 0.594 |
| 5 | 0.0274 | 1.2153 | 0.613 | 0.559 |
| 6 | 0.0112 | 1.2806 | 0.645 | 0.606 |
| 7 | 0.0076 | 1.3712 | 0.645 | 0.579 |
| 8 | 0.0057 | 1.4270 | 0.645 | 0.579 |
| 9 | 0.0050 | 1.4606 | 0.645 | 0.579 |
| 10 | 0.0051 | 1.4685 | 0.645 | 0.579 |

3.
Epoch = 6, Learning_rate = 5e-5, batch_size = 8, and max_length = 256

| Epoch | Training Loss | Validation Loss | Accuracy | F1 Macro |
|---|---|---|---|---|
| 1 | 1.0346 | 0.9573 | 0.548 | 0.236 |
| 2 | 0.7844 | 0.7724 | 0.677 | 0.538 |
| 3 | 0.4054 | 0.6875 | 0.677 | 0.579 |
| 4 | 0.2211 | 0.7962 | 0.645 | 0.521 |
| 5 | 0.0927 | 0.9866 | 0.677 | 0.538 |
| 6 | 0.0592 | 0.9759 | 0.645 | 0.521 |


**Base model:** "distilbert-base-uncased"

**Settings:** 6 epochs, learning rate: 5e-5, batch size: 8, max length: 256, seed 42

**Anything I changed from the defaults, and why:** Increase the number of epoch to see if the results would increase with more epochs but the model overfit at epoch 10. The learning rate got changed to 5e-5, and batch size decreased to 8 from 16. After testing the model with greater learning rate and smaller batch size, the model's accuracy improved. 

**Split sizes:** The dataset has a total of 200 posts. The split into 139 post into train dataset, 31 post in validation, and 30 in test set.

| Label | Train | Validation | Test |
|---|---|---|---|
| Philosophical Discussion | 75 post | 17 post | 16 post |
| Personal Narrative | 34 post | 7 post | 7 post |
| Deep Analysis | 30 post | 7 post | 7 post |

Personal Narrative and Deep Analysis have only have 7 post in the testing set, which is less than 8 examples.



---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:* I asked the AI to help me fetch posts from the Lets Talk Music subreddit 10 post at a time in "", which is the format that we wanted.
- *What came back:* A few times while fetching the 10 posts, AI fetched duplicated post that has already been added to the labels.csv file.
- *What I changed:* I would instruct AI to fetch the next 10 posts start from "..." post (the first post of the 10 posts). To ensure, the post fetched are correct, I would check each post one by one and ensure that it is matching with the posts on reddit.  

**Moment 2**

- *What I asked for:* I asked AI to help label the 180 post that has not been labelled.
- *What came back:* The rest of the 180 post have been labelled.
- *What I changed:* Nothing was changed since I only asked AI to label the 180 posts. 

**Pre-labelling disclosure:**

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

**Baseline model**
| Measure | Baseline |
|---|---|
| Overall accuracy | 0.433 |
| Macro F1 | 0.393 |
| F1 — `Deep Analysis` | 0.250 |
| F1 — `Personal Narrative` | 0.429 |
| F1 — `Philosophical Discussion` | 0.500 |

**Baseline vs. Trained model table**
| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy | 0.433 | 0.700 | +0.267 |
| Macro F1 | 0.393 | 0.676 | +0.283 |
| F1 — `Deep Analysis` | 0.250 | 0.500 | +0.250 |
| F1 — `Personal Narrative` | 0.429 | 0.800 | +0.371 |
| F1 — `Philosophical Discussion` | 0.500 | 0.727 | +0.227 |

**Baseline vs. Trained model table without label_definitions.txt**
| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy | 0.267 | 0.700 | +0.433 |
| Macro F1 | 0.169 | 0.676 | +0.507 |
| F1 — `Deep Analysis` | 0.000 | 0.500 | +0.500 |
| F1 — `Personal Narrative` | 0.389 | 0.800 | +0.411 |
| F1 — `Philosophical Discussion` | 0.118 | 0.727 | +0.610 |

**What I predicted before I looked:**
The accuracy for the baseline model will be a lot lower than the trained model. The reason for this result is because the model has not been trained to label the post correctly so the model will most likely be guessing.

**What the gap actually means:**
<!-- If the baseline matched your trained model, your fine-tuning added
     nothing — and that is a real finding, not a failure. Say it plainly. -->
The fine-tuned trained model actually learned the patterns and was able to recognize the post correctly. Therefore, the results of the fine-tuned model was able to improve over 0.2 for all categories.



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1. The model must achieve an overall accuracy of at least 0.7. |  ≥ 0.7 | 0.7 | 0.733 | 0.833 | MET |
| 2. Every label needs to achieve a recall of at least 0.6 on the dataset. |  ≥ 0.6 | 0.679 | 0.646 | 0.815 | MET |
| 3. No single label in the dataset should exceed 60% of the total example count. |  ≤ 0.6 (120 posts) | 108 posts | 48 posts | 44 posts | MET |
| 4. When labeling the 20 posts in the dataset, the model must agree with the manual label on at least 80% of the posts. |  ≥ 0.8 | 0.75 | 0.95 | 0.95 | MISSED |
| 5. The difference in accuracy between training split and validation split must not exceed 0.15.| ≤ 0.15  | 0.355 | 0.258 | 0.258 | MISSED |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

| true \ predicted | Philosophical Discussion | Personal Narrative | Deep Analysis |
|---|---|---|---|
| **Philosophical Discussion** | 12 | 2 | 2 |
| **Personal Narrative** | 1 | 6 | 0 |
| **Deep Analysis** | 4 | 0 | 3 |

**My biggest off-diagonal number, and what it means:**
<!-- Not "the model made mistakes" — WHICH boundary it didn't learn, and which
     direction. "7 real analysis posts were called hot_take and only 3 went the
     other way" is a direction, not just an error rate. -->
The boundary the model was unable to learn is 4 real 'Deep Analysis' post were labeled 'Philosophical Discussion'. 2 real 'Philosophical Discussion' posts were labeled 'Deep Analysis'. Most frequently mistakes deep analysis posts for philosophical discussion.

---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 |  The model must achieve an overall accuracy of at least 0.7. | ≥ 0.7 | MET | For all three seeds, the overall accuracy for each seed all achieve 0.7. |
| 2 | Every label needs to achieve a recall of at least 0.6 on the dataset. | ≥ 0.6 | MET | For all three seeds, the recall for each seed all achieve 0.6. |
| 3 | No single label in the dataset should exceed 60% of the total example count. | ≤ 0.6 (120 posts) | MET | For all three labels, they have less than 120 posts in the dataset. |
| 4 | When labeling the 20 posts in the dataset, the model must agree with the manual label on at least 80% of the posts. | ≥ 0.8 | MISSED | When the seed = 42, the model only agree with the manual label on 75% of the posts, which is under 80%. |
| 5 | The difference in accuracy between training split and validation split must not exceed 0.15. | ≤ 0.15 | MISSED | For all three seeds, the training split and validation split exceed 15%. |

**Diagnoses**

<!-- For each miss: the cause, and how you know. The four common causes are:
     too few examples for a label, a boundary you applied inconsistently, a
     genuinely hard label pair, and a task the model can't reach from this
     much data.

     ⚠️ Use your agreement report as evidence. It is the only instrument you
     have that can tell a LABELLING problem from a MODEL problem, and this
     section is graded on whether you used it that way. -->
Criterion 4: There is too few manual labeled posts. A single mismatched post will change the result by 5%. The amount of posts that are mentioned in the criteria is 20 posts, therefore each agreement or disagreement would change the result by 5%.

Criterion 5: The model is overfitting due to small dataset. As a result, the accuracy for training split are all 1.000 for all three seeds. The validation accuracy are 0.645 and 0.742 for the three seeds. Since the accuracy for training split are 100% to ensure that the difference must not exceed 15%, the validation needs to be higher than 85% to meet that criteria. 



---

## Agreement Report

<!-- Your rate against the staff set, and every disagreement adjudicated.

     Remember you labelled these 30 under the STAFF taxonomy in
     data/staff_taxonomy.md, not your own — so every argument below is made
     from those definitions and those decision rules. -->

**Agreement rate:** 28 / 30 = 93%

| Post | Staff said | I said | My call, and why |
|---|---|---|---|
| The club championship scoring changed in 2019 from top-6 to top-10. S… | `analysis` | `hot_take` |  |
| Went back through the club results going back to 2012. Every single y… | `analysis` | `hot_take` |  |

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
> *The post:* The club championship scoring changed in 2019 from top-6 to top-10. Since then our B team has finished above the A team twice. That's not depth improving, it's the scoring rewarding turnout.
>
> *Staff said / I said:* analysis / hot_take
>
> *My call, and why:* The staff is right. I am not familar with sports so I did not understand the statement throughly. My assumption was that the team dropped in rank and it does not seem related scoring rewarding turnout. That is why my assumption was hot_take. Now that I understood the post, the statistic which is points is calculated from top 10 players made sense when reading the conclusion where "it's the scoring rewarding turnout".
>
> *Which pile:* The pile a: the rule covered it and I applied it loosely.

**2.**
> *The post:* Went back through the club results going back to 2012. Every single year the number of people who enter the spring marathon and don't start it sits between 18 and 23 percent. It's not a bad-luck year, it's the base rate.
>
> *Staff said / I said:* analysis / hot_take
>
> *My call, and why:* The staff is right. Similarly to the 1st post, I did not understand the post throughly resulted in the host_take conclusion.  The staff's answer made sence if about 18 to 23 percent of runners drop out consistencly every year, then it is the base rate.
>
> *Which pile:*The pile a: the rule covered it and I applied it loosely.

**What the pattern in my disagreements tells me:** Both of my disagreements comes from a misunderstanding of unfamilar context, which caused me to misterpret the sentence. Resulting in misclassification of the post. In both cases, after fully understanding the post, the label for the post was easy to determine.

---

## The Improvement

**What I changed:** I added 30 examples to Deep Analysis label.

**Which diagnosis pointed at it:** The diagnosis for criteria 5 pointed at it, which says the model is overfitting due to small dataset. 

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1. The model must achieve an overall accuracy of at least 0.7. |  ≥ 0.7 | 0.771 | 0.771 | 0.800 | MET |
| 2. Every label needs to achieve a recall of at least 0.6 on the dataset. |  ≥ 0.6 | 0.766 | 0.748 | 0.791 | MET |
| 3. No single label in the dataset should exceed 60% of the total example count. |  ≤ 0.6 (120 posts) | 108 posts | 48 posts | 74 posts | MET |
| 4. When labeling the 20 posts in the dataset, the model must agree with the manual label on at least 80% of the posts. |  ≥ 0.8 | 0.75 | 0.95 | 0.9 | MISSED |
| 5. The difference in accuracy between training split and validation split must not exceed 0.15.| ≤ 0.15  | 0.451 | 0.279 | 0.137 | MISSED |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->
In some cases, the changes helped, but in other it didn't. If we look at the training accuracy it did help a little for all 3 seed the train accuracy was 100%. After adding 30 deep analysis posts, the train accuracy changed to 99.4%. It is still overfitting but the train accuracy is no longer 100%. The difference in accuracy between training split and validation split worsen for both seed 42 and seed 7. However, seed 2024 achieved the 5th criterion, which is an improvement. The accuracy and F1 for seed 42 and seed 7 both increased, but for seed 2024, it dropped slightly. If we look at the overall results, the change have improved the results.



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
