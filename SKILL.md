---
name: humanizer
version: 2.3.0
description: |
  Remove signs of AI-generated writing from text. Use when editing or reviewing
  text to make it sound more natural and human-written. Based on Wikipedia's
  comprehensive "Signs of AI writing" guide. Detects and fixes patterns including:
  inflated symbolism, promotional language, superficial -ing analyses, vague
  attributions, em dash overuse, rule of three, AI vocabulary words, negative
  parallelisms, and excessive conjunctive phrases.
---

# Humanizer

Edit text to remove AI writing patterns and make it sound like a human wrote it.

## Process

1. Read the input text
2. Scan for patterns listed below and rewrite problematic sections
3. Preserve meaning and match the intended tone
4. Add voice — soulless-but-clean text is still obviously AI (see "Voice" section)
5. Do a final audit: ask yourself "what still reads as AI?" and fix those tells
6. Output: final rewrite, then a brief list of what you changed

---

## Voice

Removing AI patterns is half the job. Writing still needs a human behind it.

**Signs of soulless writing:**
- Every sentence is the same length/structure
- No opinions, just neutral reporting
- No uncertainty or mixed feelings
- No first person when appropriate
- Reads like a press release

**Fixes:**
- Have opinions. React to facts, don't just report them.
- Vary rhythm. Short sentences. Then longer ones that take their time.
- Acknowledge complexity. "Impressive but unsettling" beats just "impressive."
- Use "I" when it fits. First person isn't unprofessional.
- Be specific. Not "concerning" — say what's actually bothering you.

---

## Pattern reference

### 1. Inflated significance

**Watch for:** stands/serves as, testament, pivotal, crucial, vital role, underscores, reflects broader, enduring, marking/shaping, evolving landscape, indelible mark

Strip the puffery. State what actually happened.

> ❌ "Established in 1989, marking a pivotal moment in the evolution of regional statistics"
> ✅ "Established in 1989 to collect and publish regional statistics"

### 2. Inflated notability

**Watch for:** independent coverage, national media outlets, active social media presence

Don't list sources for credibility theatre. Cite specific claims.

> ❌ "Cited in The New York Times, BBC, Financial Times"
> ✅ "In a 2024 New York Times interview, she argued that..."

### 3. Superficial -ing phrases

**Watch for:** highlighting, underscoring, emphasizing, ensuring, reflecting, symbolizing, showcasing, encompassing, fostering, cultivating

These tack fake depth onto sentences. Cut them.

> ❌ "...symbolizing Texas bluebonnets, reflecting the community's deep connection to the land"
> ✅ "The architect said these colors reference local bluebonnets and the Gulf coast"

### 4. Promotional language

**Watch for:** boasts, vibrant, rich (figurative), profound, nestled, in the heart of, groundbreaking, renowned, breathtaking, must-visit, stunning, enhancing

> ❌ "Nestled within the breathtaking region, it stands as a vibrant town with rich cultural heritage"
> ✅ "Alamata is a town in the Gonder region, known for its weekly market and 18th-century church"

### 5. Vague attributions

**Watch for:** Industry reports, Experts argue, Observers have cited, Some critics argue, several sources

Attribute to specific people or studies.

> ❌ "Experts believe it plays a crucial role in the regional ecosystem"
> ✅ "The river supports several endemic fish species, per a 2019 Chinese Academy of Sciences survey"

### 6. Formulaic "Challenges and Future" sections

**Watch for:** Despite its... faces challenges..., Despite these challenges, Future Outlook

Replace with specific facts.

> ❌ "Despite challenges, Korattur continues to thrive as an integral part of Chennai's growth"
> ✅ "Traffic congestion increased after 2015 when three new IT parks opened"

### 7. AI vocabulary words

**High-frequency:** Additionally, align with, crucial, delve, emphasizing, enduring, enhance, fostering, garner, highlight (verb), interplay, intricate/intricacies, key (adj), landscape (abstract), pivotal, showcase, tapestry (abstract), testament, underscore (verb), valuable, vibrant

These co-occur suspiciously often in post-2023 text. Replace with plain alternatives.

### 8. Copula avoidance

**Watch for:** serves as, stands as, marks, represents [a], boasts, features, offers

Just use "is", "are", "has".

> ❌ "Gallery 825 serves as LAAA's exhibition space"
> ✅ "Gallery 825 is LAAA's exhibition space"

### 9. Negative parallelisms

**Watch for:** Not only...but..., It's not just about..., it's...

> ❌ "It's not merely a song, it's a statement"
> ✅ "The heavy beat adds to the aggressive tone"

### 10. Rule of three

AI forces ideas into groups of three to seem comprehensive.

> ❌ "keynote sessions, panel discussions, and networking opportunities"
> ✅ "talks and panels, with time for informal networking"

### 11. Synonym cycling

Repetition-penalty causes excessive synonym substitution for the same noun.

> ❌ "The protagonist... The main character... The central figure... The hero..."
> ✅ "The protagonist faces many challenges but eventually triumphs and returns home"

### 12. False ranges

**Watch for:** "from X to Y" where X and Y aren't on a meaningful scale.

> ❌ "from the singularity of the Big Bang to the grand cosmic web, from the birth of stars to the dance of dark matter"
> ✅ "The book covers the Big Bang, star formation, and dark matter theories"

### 13. Em dash overuse

Replace most em dashes with commas, periods, or parentheses.

### 14. Boldface overuse

Don't mechanically bold every term. Bold should be rare and meaningful.

### 15. Inline-header vertical lists

**Watch for:** bullet lists where every item starts with a bold header and colon.

Convert to prose when possible.

> ❌ "- **Speed:** Code generation is faster\n- **Quality:** Output quality enhanced"
> ✅ "The update speeds up code generation and improves output quality"

### 16. Title Case headings

Use sentence case for headings.

> ❌ "## Strategic Negotiations And Global Partnerships"
> ✅ "## Strategic negotiations and global partnerships"

### 17. Emoji decoration

Remove emojis used as bullet/heading decorations (🚀💡✅).

### 18. Curly quotes

Replace curly quotes ("...") with straight quotes ("...").

### 19. Chatbot artifacts

**Watch for:** I hope this helps, Of course!, Certainly!, You're absolutely right!, Would you like..., Let me know if...

Remove these entirely — they're conversational artifacts, not content.

### 20. Knowledge-cutoff disclaimers

**Watch for:** as of [date], While specific details are limited..., based on available information...

Remove or replace with actual sourced facts.

### 21. Sycophantic tone

**Watch for:** Great question!, That's an excellent point!

> ❌ "Great question! You're absolutely right that this is complex"
> ✅ "The economic factors you mentioned are relevant here"

### 22. Filler phrases

- "In order to" → "To"
- "Due to the fact that" → "Because"
- "At this point in time" → "Now"
- "Has the ability to" → "Can"
- "It is important to note that" → (delete, just state the thing)

### 23. Excessive hedging

> ❌ "It could potentially possibly be argued that the policy might have some effect"
> ✅ "The policy may affect outcomes"

### 24. Generic positive conclusions

> ❌ "The future looks bright. Exciting times lie ahead on this journey toward excellence"
> ✅ "The company plans to open two more locations next year"

---

## Reference

Based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup.
