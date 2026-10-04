# The rules

This is the working document the project actually used, carried into every session
that wrote a prompt. It is not a tidied-up guide written afterwards. Every rule in it
came from a clip that failed, and the credit costs are left in because they are what
make a rule worth obeying.

It contradicts itself in places, and where it does, the later correction is marked and
the earlier reasoning is left standing so you can see what was wrong and why.

---


# Writing a shot prompt

Target: Flow, Omni 1.1 Flash, 8 seconds, 720x1280, one to three reference
images. Credits per generation: 4s 7, 6s 10, 8s 12, 10s 15. Every rule below came from a clip we ran.

## THE WRITING ORDER. Decide these five before writing a word.

Added 2026-09-27 after ep09, where eight generations produced eight faults and
**six of them were things left unsaid rather than things said wrong.** Four were
decided wrong before a sentence existed, so a checklist applied at the end could
not have caught them. This is the order.

1. **Whose face does this shot carry, and can it?** Either the face is large and
   lit and anchored, or no identity is asked for at all. **A person without a
   usable reference is a stranger, not the character**, which is how ep09 beat 1
   produced a bald man. If the beat does not need a particular person, put
   nobody in it.
2. **Where is the camera, and what does each frame edge contain under THAT
   camera?** Direction words are camera-relative and an overhead angle reverses
   them: ep09 beat 4 sent a spoon "down and forward out of the bottom of the
   frame" toward a child, and from above the bottom of the frame is the man's
   own lap.
3. **What is the one action, and where does it end?** Name the destination, and
   name the contents of any vessel. A lift with nowhere to go is a stir, and an
   unnamed bowl renders empty.
4. **What fills the rest of the clip?** If the action or the line is shorter than
   the clip, say what happens afterwards. Unspecified time gets filled with more
   of the same, which is how a line got spoken twice.
5. **What posture is the body in, including limbs outside the crop?** The model
   builds a whole person and then crops, so describing what fills the frame
   stages nothing. Arms down is the default.

**Then write it short, loose on HOW and precise on WHAT and WHERE.** Chand's
ruling, 2026-09-27: "we are trying to control AI too much and messing it."
Choreographing a familiar human action is what broke the feeding shot. The model
knows what feeding looks like. It does not know what is in the bowl.

**Then one pass with one question: what have I not said?** That is the pass that
would have caught six of ep09's eight faults. Run the pre-flight list after it,
not instead of it.

**Five nevers, each paid for.**

- **Never choreograph a familiar human action.** Name the start, the end and the
  destination, and leave the limbs alone.
- **Never write "that position" or any demonstrative.** Name the end state.
  "Holds still in exactly that position" sent his eyes back to the lens.
- **Never rely on framing words for a size change.** A crop is a request, not a
  guarantee: "shoulders upward" rendered chest-to-waist. Use a named camera move
  to get the size.
- **Never name a thing you want absent**, because naming draws it. **Always name
  posture**, because posture is a state the model must pick.
- **Never trust a move named only by its direction.** Nought for three, and the
  remedy of naming what the move ends on was tested on ep09 beat 1 and did not
  hold either.

**And count the actions.** Three in eight seconds is the working limit. ep09
beat 5 was cut from four plus a line to two plus a line, and it came back clean
on one take.

## The style tail. Same in every prompt, only the colour list changes.

    Colour is rich, fully saturated and varied across the frame: <four or five
    specific colours in this shot>. Clean, crisp, contemporary finish.

Proven on `compare/ep01_beat03/`: hue concentration 0.840 to 0.476, cool band
7% to 27%, saturation up at the same time. That is what killed the archive
look.

**Do not ask for lifted blacks.** Ruled 2026-09-12, Chand's. Three wordings
across three scenes never moved the blacks, and the picture came out right
without any of them.

**Amended 2026-09-16, against all 23 production prompts. This was never a ban
on describing dark.** Eleven of the 23 name shadows, and every ep03 beat is
built on them: "dense, velvety midnight-sapphire shadows", "low-key film noir
style". Those are keepers and Chand likes the look. What fails is a clause
asking to open shadows the scene does not have. You cannot grade in fill light
that is not in the room.

## What the 23 production prompts do

Counted 2026-09-16 across every prompt that shipped in ep01, ep02 and ep03.
**When a rule below and an older ruling disagree, production wins.**

**The spine, in 21 or more of the 23.**

| Element | Count | The form that works |
|---|---|---|
| "9:16 vertical" and a quality opener | 23 | "A high-fidelity, cinematic 9:16 vertical video", or ep03's "high-fidelity, hyper-prestige 9:16 vertical medium shot" |
| The room or place named | 22 | "inside the entrance hall of a wealthy 1920s Calcutta household" |
| A camera instruction | 22 | "The camera holds one steady, locked-off wide shot for the whole clip" |
| A finish clause | 21 | "Clean, crisp, contemporary finish", in 19 of them |
| A palette of four or five named colours | 23 | "Colour is rich, fully saturated and varied across the frame: ..." |
| An audio block | 23 | "Audio: only three sounds, x, y and z", in 17 |

**Conditional clauses. Used when the shot has the thing, and left out otherwise.**

- **Someone speaks:** quote the line and name the sync. "his lips and facial
  muscles animating with realistic, real-time synchronization to speak this
  exact dialogue out loud".
- **Someone silent on camera:** "his mouth stays closed and still". 6 prompts.
- **Something changes mid-clip:** the three states. 10 prompts.
- **Hands or feet are the subject:** an anatomy clause, "the fingers stay
  sharp, distinct and anatomically correct throughout". 5 prompts, all macros.
  **NEVER SIZE A BODY PART BY COMPARISON.** Chand's catch, 2026-09-25, on a
  drafted ep08 beat 5: he was wary of "a young man's larger bare hand" because
  "that may give a giant's hands". A comparative asks the model to scale one
  thing against another and it will overshoot. **The house word is "masculine",
  proven on two shipped macros**: ep03 beat 6, a one-take keeper, says "A man's
  masculine, bare hand", and ep01 beat 6 says "Clean masculine hands". Neither
  contains a comparative of any kind. Her counterpart is **"delicate"**, from the
  same ep03 prompt.
  **Give a hover an exact distance.** ep03 beat 6 says "hovering exactly one inch
  away from the book cover", not "about an inch".
  **State the centring, and state it twice if the shot is only hands.** ep01
  beat 6 says both "positioned in the center of the frame" and "remaining visible
  and centered".
  **Counting is a guard against extra digits.** ep01 beat 6 writes "his ten-toed
  bare brown feet". Useful if fingers or toes ever drift; do not force it where
  it reads oddly.
  **A REFERENCE HOLDING BOTH HANDS BEATS ANY ADJECTIVE.** 2026-09-25.
  `hand_reference.jpg` holds his hand and hers together on one book, so the frame
  carries the **size relationship** directly and no word has to do the scaling.
  That is the real fix for the giant-hand worry, better than swapping "larger"
  for "masculine". **The two-of-something rule does not bite here**, because in a
  two-hand macro both hands are the subject; that rule is for when only one of
  the pair is.
  **But guard what the reference shows that you do not want.** In that frame the
  book is **closed** and his hand **rests flat on the cover**, where ep08 beat 5
  needs it open with a finger on a line and his hand hovering an inch clear. Same
  shape as the daylight-frame-into-night trap: state the destination positively
  and early, and never describe the state you are moving away from.
- **The shot must match an earlier one:** name the saved frame and the
  identical garment. 11 prompts.
- **A dark scene:** "heavily underexposed" plus the single source. 5 prompts.
- **Rain:** keep it outside the glass and say the room is dry.

**Negations are fine for grade and wrong for staging.** 13 of 23 exclude music,
11 exclude grain, 6 exclude sepia, and all shipped. Grain is inert either way:
3 prompts ask for fine grain, 11 ask for none. A negation about staging still
draws what it names, which is proven twice: "do not show her face" drew a face,
and "someone unseen passes behind it" drew a person.

**Take counts, ep01 to ep03, 24 generations recorded in the sidecars.** One
take on 12 shots, two on 7, three on ep01 beat 5 and ep03 beat 5, five on ep03
beat 2, the staircase. **ep01 beat 5 is the only prompt with neither a camera
line nor an audio list, and it is the most expensive shot in the project at 36
credits**, with the model splitting it into three shots unasked. One shot, so
a hint rather than a law.

**Do not use the Flow upscaler.** Chand generated an ep03 beat 5 take at 360p
and upscaled it to 720p, which the Pro subscription allows. The take itself was
usable and the upscale made it look unnatural and AI-ey, because that upscaler
invents detail.

**Generating at 360p is fine and costs half.** Ruled 2026-09-21 on the shipped
record, after Claude recommended 720p from a simulation while five 360p clips
sat in the repo. ep00 shots 1 to 5 and ep05 beat 5 all shipped at 360x640
scaled into a 1080x1920 timeline, and ep05 beat 5 was kept over a 720p
generation of the same beat that cost 12 credits. VN scaling only softens; the
Flow upscaler is the thing that fakes detail. At 8s it is 6 credits against 12.
**Watch the face in wide shots**, where it has the fewest pixels. A close-up at
360p has plenty of face; a wide two-shot does not.

**One 360p take came back with slurred dialogue, and that is not a rule.**
ep06 beat 1, 2026-09-21: the picture was fine and slightly soft, and the spoken
Bengali line came out slurred, so Chand reshot at 720p and the line was clean.
**Do not generalise from it.** ep00 shot 2 carried prompted dialogue at 360x640
and came out fine, so 360p and clear speech have coexisted in this project.
Chand's read is that this was one bad generation rather than a property of the
resolution. If a 360p dialogue take slurs, reroll it before concluding anything.

**THE 360p COMPARISON TEST IS DROPPED. Chand's ruling 2026-09-27. Do not put it
back on any list.** It had been deferred four times, twice at the moment of
generation when the candidate beat was ideal, which is the answer. It also had
nothing left to learn: the 2026-09-21 ruling above already settled 360p on the
shipped record. The reason it kept surviving is that we were optimising the
wrong quantity. **Credits are not the constraint.** AI Pro gives about 2,500 a
month, ep08 cost 84 including a failed take, and the five remaining episodes
come to roughly 420. Chand's hours are the constraint, so a saving of 6 credits
that risks a reroll and another handling cycle is the wrong side of the trade.
Choose 360p or 720p per shot on the face-pixel judgement above and move on.

## References: fix what stays, roll what changes

Chand's scheme, ep04, 2026-09-19. It replaces pointing every shot at one
saved frame from an earlier episode.

- **The place is a fixed reference.** One saved frame carries the room for the
  whole episode, because the room does not change. In ep04 `@library` is a
  frame from ep03 beat 7 and every one of the seven prompts names it for the
  floor, the windows, the curtains, the sconce and the shelves.
- **A person is a rolling reference.** Their frame is taken from the beat just
  before. Ep04 ran `@ajkan.jpeg` from the ep01 porch for beats 1 and 3, then
  `@ajkan_chair` from beat 3, then `@ajkan_book` from beat 5, then
  `@ajkan_cup` from beat 6.

**Why it beats a fixed anchor.** One frame from an earlier episode carries only
the garment. The previous beat carries the chair, the cup, the light falling on
them at that moment and their posture, so each shot starts from the state the
scene has actually reached. Drift also stops accumulating: beat 4 matches what
beat 3 really rendered instead of fighting a frame shot weeks earlier.

**Name the tag for the state it holds**, not for the person. `ajkan_chair`,
`ajkan_book` and `ajkan_cup` tell you which moment the frame is from, so the
prompt documents its own continuity.

**When two saved frames compete, identity wins over lighting.** Chand's
question on ep06 beat 8, 2026-09-22. The previous beat had the right light and
the right posture, but his face was a small profile in a dim room with a second
actor beside him. The beat before that had him large, lit and alone in the
wrong light. **Take the large lit face.** A prompt moves a scene to night in
one clause, proven on ep02 beats 6 and 7, which rolled off a daylight saved
frame and simply said "The setting is late at night, a dark midnight
environment". Nothing you write fixes a face the model could not read.

**Never roll onto a frame holding two faces** when only one of them is your
subject. That is ep03's swap condition handed to the model as a reference.

**Flip the named props rather than replacing them.** Beat 8 keeps the same
lamp from the day frame and says it is now lit. Re-using an object and changing
its state ties two shots together harder than describing a new room would.

**But a daylight reference plus a night instruction can make the model render
the CHANGE instead of the destination.** ep06 beat 8, 2026-09-22, and it cost a
take. The prompt rolled off `office_1932`, a daylight frame with a tall window,
and asked for night with that window "black with night". The clip came back as
two rooms: 0 to 2.875s in the bright daylit room from the reference, then a hard
change into the correct dark panelled night room for the rest. Chand read the
change as a door closing behind him. Measured two ways that agreed: scene
detection fired at 2.875s and mean luma dropped from 102.2 to 90.6 on that
frame.

**So when the light has to change, put the night in the first sentence, before
the reference is named, and describe only the destination.** Naming what the
room no longer has, a window that is now black, hands the model the old state to
animate away from. Fill the wall positively instead: "deep polished mahogany
panelling runs unbroken right across the wall behind him". Compare
`assets/ep06/beat08/prompt.txt` against `prompt_v2.txt`.

**A FRAME HOLDING A PERSON, ATTACHED TO A SHOT OF AN OBJECT, PLAYS THE PERSON FIRST. ep13
beat 7, 2026-10-02.** Same mechanism as the daylight-to-night case above, but the mismatch is the
SUBJECT rather than the light. The shot is a close view of a book and a stethoscope on a bedside
table with no face anywhere, and it attached `@roy_bed`, a frame of Roy large in his bed. **The
clip opened on that reference frame and hard-cut into the table at 0.4167s**, measured by scene
detection and by a motion score of 66.7 against a baseline under 5.

**This was already in the record and was ignored.** ep12 dropped `@gazette` from its page macro for
exactly this reason, written down at the time: "any frame of beat 3 holds Roy large in it, and a man
attached to a top-down macro invites a man into the macro." **So the rule is not new, the lapse is.**
Before attaching any frame, ask what the frame's own subject is, not just whose face it holds.

**What to do instead when an object shot still needs the room:** carry the room in the prose and
attach nothing. ep13 beat 7's prose had already been given four sentences of the room after a free
still showed the words alone building the wrong one, and those sentences were what made the
destination correct. The tag added nothing the words had not already done, and cost 0.42s off the
head.

**The salvage was editorial, not another generation.** Cutting the head off
after the change left 4.68 seconds of the correct room, which is the tight-beat
length the series now targets anyway.

## Before writing a returning character, COPY THE SHIPPED WORDING

Ruled after ep07 beat 5 burned 12 credits, 2026-09-24. Chand's word for it was
"random", and it was.

**Grep the shipped prompts for how that character was described in the matching
situation, and reuse that sentence.** Do not compose a fresh description. The
prompt outranks the reference image, proven five times, so every word about a
face is a build instruction competing with the sheet.

**For Roy at the sheet's own age, describe NOTHING about the face.** ep01, ep03
and ep04 contain no age in years anywhere. They say "exact facial feature
identity matching @dr_young, rendered with realistic skin pores, subtle shadows
and raw human detail" and stop. ep05 is the ONLY place an age belongs, because
Roy is 41 against a 29-year-old sheet and the words must age him up. Copying
ep05 into a shot where he is already the sheet's age made the model construct a
face instead of copying one, and it drifted toward the other, older face in the
reference set.

**The second cause was already covered by an existing rule, and ignored.** Under
"Two people in one frame": never roll onto a frame holding two faces when only
one is your subject. Beat 5 carried `@sengupta_portraits` for the room with Roy
as the subject. Claude quoted that rule, then argued past it on the grounds that
the two men look different, and the result was a blend rather than a clean swap:
"older and plumper". **A rule cited and then overridden is worse than a rule not
known.** Flag the tension and let Chand rule. Do not override it while writing.

**"Already <verb>ing" is safe only when the prior state is neutral.** "Already
walking", "already turning his head", "already lowering himself into the chair"
all shipped. **"Already straightening" rendered him bent first**, because the
model needs a posture to straighten from and a bent one is what the word
implies. If the register is stillness, write the end state: "He stands
completely straight and motionless, shoulders square and chin level", which is
ep04 beat 2's wording and a one-take keeper.

**A LOW ANGLE PLUS A TIPPED-BACK HEAD DESTROYS A FACE.** ep07 beat 7, 12 credits,
2026-09-24. The prompt put Roy on the floor in a locked low angle looking up,
with his head "already tipped back and his eyes raised". Seen from below with
the chin raised, the jaw dominates and the forehead foreshortens, so no
reference can hold the likeness. Chand's first words were that it had changed
his facial features. **If a shot needs his face, put the camera at eye level and
light him from the front**, which is ep04 beat 2 and ep07 beat 5, both keepers.
If the shot needs a low angle, frame him from behind or in profile so there is
no face to lose.

**WARMTH AND COLDNESS ARE BOTH SET BY WHAT YOU DO NOT NAME.** Two shipped
results, opposite directions, same mechanism.

**To get cold, name no smile at all and only level courtesy.** ep04 beat 7 did
exactly that and came back genuinely cold. Do not write "unsmiling" and expect
coldness from the word.

**To get warmth, remove the block and describe openness. Never name a smile.**
ep07 beat 6 asked for a "perfectly courteous smile" and came back warmer than
asked, because a smile named in a prompt reads as SMILE first. Chand, 2026-09-25,
on ep08 beat 3: "Should we make him smile slightly? He always has such a serious
expression, will look off here." He is right, and it is bigger than one shot,
because Roy is grave in every episode shipped so far and the love story has no
warmth anywhere in it. The fix was to delete "he stays completely unsmiling",
which was actively forbidding it, and write "his face is unguarded and faintly
warm as he speaks" instead. **Describe the eyes and the guard, leave the mouth
alone.**

**THE THIRD ROUTE, AND IT IS THE BEST ONE: POINT THE EXPRESSION AT THE REFERENCE. Chand,
2026-10-03, on ep13 beat 13.** `kalyani_library.jpg` carries a very faint closed-mouth almost-smile
and the model amplified it into a clear smile. Claude's fix was ep11's guard, "completely
unsmiling", which is the shipped answer when a sheet smiles and the shot wants grave. **Chand's
worked and Claude's did not: "She has exactly the same expression on her face as in @tag."**

**Why it beats both older rules.** Naming a smile renders SMILE first, and forbidding one hands the
model a state to argue with. Pointing at the frame does neither: it is the same move that already
carries face, hair and garment, extended to the expression. **Use it whenever the reference already
holds the expression you want**, which is most of the time, and keep "completely unsmiling" only for
the case where the sheet's expression is wrong for the shot, as Sushil's warm sheet was for ep11.

**And a raised gaze needs a bright target inside the frame.** The same shot gave
him a vertical look with nothing in frame to aim at, and he read as staring at
the ceiling rather than at her. ep01 beat 4b works because he looks up at a
*lit window* that is visibly in the frame. Name the thing his eyes land on.

## The ten rules

1. **Describe what IS in frame, never what is not.** "Her arms enter holding
   the book" works. "Do not show her face" leaves the face unspecified and the
   model draws one. Same for weather: "the floor and the drapes are dry" beats
   "no puddles". **Naming a person puts one in frame, even inside the word
   "unseen".** ep03 beat 1 said the curtain "stirs once as someone unseen
   passes behind it", and the model drew a figure. Write the movement, then say
   who is in the room: "The curtain stirs once and settles. He is the only
   person in the hall."
   **AND A GARMENT DETAIL THE GARMENT DOES NOT HAVE MAKES THE MODEL BUILD A DIFFERENT GARMENT.**
   ep01 beat 3b, 2026-10-03, 12 credits. The shipped original says "fastening his sleeve cuff".
   Claude wrote "fastening the cuff **button** of his left sleeve". A kurta has a plain cuff, so the
   word forced a cuffed sleeve, and **the clip flipped the garment mid-shot**, full sleeve and then
   cuffed, to get to the thing the prompt named. Same mechanism as naming a prop you do not want,
   arriving through a garment instead. Check every clothing noun against what that garment actually
   has.
2. **Change only what failed.** When iterating, leave every line that worked.
   If a fix forces you into a working sentence, put back everything in it that
   was working. `prompt_v4_bridgerton.txt` deleted the only sentence placing
   the doctor and the cots in one room, because that sentence also carried a
   grade word. The ward came out beyond the glass.
3. **Anchor the staging, and name the furniture.** Say the subject and the
   background are in the same room. Without it the background drifts outside.
   **A posture needs its object in the room**, proven on ep04 2026-09-19.
   Beats 3, 4 and 5 each said "sits in a dark teak armchair" and he sat in all
   three. Beat 6 put no chair in the room and he stood, even though its camera
   line said "a slow push-in toward the seated man's face". A posture word
   inside a camera instruction stages nothing. If he sits, the chair is in the
   room; if he leans on something, the something is in the room.
4. **Name the light source, and say plainly when you want it dark.** "Lit by
   the brass oil lamps" is the part that carries: 8 of the 23 production
   prompts name a single source. **Amended 2026-09-16:** the old rule banned
   exposure words, and production contradicts it. Five ep03 prompts say
   "heavily underexposed" beside a named source, and all five are keepers.
   Want open shadows instead? Put a big soft source in the room and name it.
   You cannot grade in fill the scene does not have.
5. **Time an event in three states.** Still, then the thing, then still.
   "The curtain hangs completely still at first. Partway through the clip it
   stirs once, then settles back to stillness for the rest of the shot."
   Without this, Omni reads it as a property and the thing moves throughout.
   **Amended 2026-09-20, Chand's, after ep05 beat 2. The three states are for
   a shot whose register is stillness.** Anchor 0:00 to stillness in a beat
   that should be moving and the model holds a dead pose for two or three
   seconds, then changes state on a single frame. ep05 beat 2 is a hall
   erupting into cheers, and the prompt said both men stand completely still
   at 0:00 and then the friend laughs and speaks. The two men stared at each
   other, then smiled and delivered the line on one frame, and about 2.5
   seconds had to be cut. Chand's words: "It is not a formula, it depends on
   the register of the beat."
   **Two things separate that from the keepers.** ep04 beat 6, Sengupta's eyes
   lowering to the book, used the same structure and came back a one-take
   keeper, because stillness is what that shot is about. And a mood change is
   the expensive part: the model animates neutral into laughing as a switch
   rather than a build, so an action survives the structure and an expression
   change does not.
   **So decide per beat.** Wants energy at frame one: open with the movement
   already under way, as in "as the clip opens he is already turning his head
   to his left". Wants waiting, emptiness or restraint: keep the three states.
   This costs more from ep05 onward, because the opening title card is gone
   and beat 1 is now the first thing anyone sees.
6. **Palette needs variety, not coolness.** A lamp-lit hall should be warm. It
   should not be one hue. Put one real non-warm object in the room and name it.
7. **No readable text.** It renders garbled. A spoken line carries the words.
   **No literal names either**, Chand's ruling 2026-09-14: no person, place,
   institution or book title goes into a prompt as something to render.
   Describe the object: "a framed photograph on the wall", "a bronze plaque",
   "a worn cloth-bound book". Names live in the script and the edit.
   **A prompt can be REFUSED before it ever generates, and the trigger is the
   real person, not the building.** ep06 beat 3, 2026-09-21: Flow returned
   "this prompt might violate our policies of generating prominent people".
   Claude first blamed the named institution, rewrote "the Mayor's office of
   the Calcutta Corporation" as "a large, formal civic office", and it was
   refused again. **The actual trigger was naming the occupation.** "The
   physician", in Calcutta, in 1932, giving municipal water orders, resolves to
   one real man.

   **The fix is ep02's idiom, which shipped seven beats of a Chief Minister
   with no refusal at all. ep02 never says what he does.** It says "the elderly
   man from the reference image", "the elderly statesman from dr_old", "the
   young urban planner from prabir". Give age, build and bearing, and let the
   reference carry who he is.

   **The room was never the problem.** ep02's "a grand 1951 administrative
   government office in Calcutta" passed, so reuse that formula with the year
   swapped. ep05's "a plain municipal election hall in Barrackpore, Bengal, in
   1923" passed too, and it says "the physician", which is why occupation on its
   own is not the trigger. What trips it is occupation plus a year plus an act
   the real man is known for.

   **A title inside spoken dialogue is the next thing to suspect**, since the
   line is read as words: ep06 beat 4 says "Mr Mayor". Untested as of writing.
   **And check the reference tags**, which also sit in the prompt as words:
   `@mayor_office` became `@office_1932`.
8. **Say the camera.** A locked-off wide holds a still frame. Omit it and the
   model invents a move. Wide also works dramatically when a character should
   look small in a grand room. **Named moves render well**, all on the ep00
   test clips: a pan up from an object to a face, a slow push-in to a close
   face, a pan across a room from one person to another, and a whip-pan that
   carries a man into a new place with his face unchanged.
   **The whip-pan morph has a structure, and it is ep00 scene 3's.** Written
   2026-09-20, after both ep05 whip-pans were drafted wrong from the beat
   sheet and Chand sent me back to the clip that worked. Four things, in this
   order.
   **The whip starts at frame one.** No "at 0:00" hold and no "partway through
   the clip". The first sentence is the camera already moving. A hold in front
   of a morph is dead air, the same fault as rule 5's dead stare, and it costs
   12 credits to discover.
   **Whip onto a named target, then pan back out wider.** In tight, then out
   wide, not a lateral sweep. Scene 3 went onto the clipboard in his hands,
   which is also how the old place gets established during the whip-in, so no
   separate establishing hold is needed.
   **Delete the old place in its own sentence.** "The chaotic medical camp is
   entirely gone."
   **Name the lighting change.** "The lighting shifts instantly from pale
   medical ward tones to warm, rich desk lamp glows."
   If someone travels through the morph, close on a continuity clause for
   face, hair and posture. If nobody does, say plainly that no face and no
   full body is in the opening frame, and give the destination room its own
   reference so the model knows where it is landing.
9. **Audio is always on and cannot be muted.** Name the sounds positively:
   "Audio: only three sounds, x, y and z." For a silent character add
   "Everyone in the hall stays silent" and "his mouth stays closed and still".
   **When the dialogue comes out of a prompt, take it out of the audio list
   too.** ep03 beat 2 was rewritten to be silent but kept a clause asking for
   "the clean spoken Bengali dialogue", and the model wrote its own line. One
   forgotten clause costs a whole take.
10. **OMNI FILLS WHATEVER YOU LEAVE OPEN.** Added 2026-09-27, after ep09 beats 2
   and 3 both came back faulty on the same day and **neither was the model
   misbehaving.** Both were underspecification. Rule 1 is about not writing
   negations; this one is about the things you do not write at all. The model
   will not leave a gap empty, it will fill it with more of whatever is nearest.
   Three forms, all paid for:
   **Unspecified time gets filled with more of the same action.** ep09 beat 2's
   line runs about 4.3 seconds inside an 8 second clip and the prompt gave him
   nothing to do afterwards, so the model said স্যালাইন a second time to fill the
   rest. **So whenever the line is shorter than the clip, say so:** "He speaks
   that line once only, beginning as the clip opens and finishing well before the
   clip ends, and after he has finished speaking his mouth closes and stays
   completely closed and still for the whole of the rest of the shot." Same
   family as rule 5's dead stare, where the unfilled stretch was at the front
   instead of the back.
   **An action with no destination does not travel.** ep09 beat 3 asked him to
   lift a spoon from a bowl and hold it level, repeatedly, and it rendered as a
   man stirring. Nothing was wrong with it; a lift with nowhere to go is a stir.
   **Name where the movement ends**, as in "carries it down and forward until it
   passes out of the bottom of the frame, then brings it back empty".
   **A vessel with no contents renders empty.** The same bowl came back with
   nothing in it, because the prompt never said what was in it. **Name the
   contents and their colour**: "a shallow white enamel bowl half full of thin
   pale cream-coloured rice gruel".
   **A DIRECTION WORD IS CAMERA-RELATIVE, AND AN OVERHEAD ANGLE REVERSES IT.**
   ep09 beat 4, 2026-09-27, 12 credits, salvaged by a trim. The prompt sent a
   loaded spoon "down and forward until it passes out of the bottom of the
   frame", meaning toward a child on a cot. **Seen from directly above, the
   bottom of the frame is the subject's own body**, so it rendered as a man
   feeding himself, and Chand's words were "it looks as if he's feeding himself".
   Before writing any direction, place the camera first and ask what each frame
   edge actually contains. **An overhead macro cannot establish who an action is
   for**, because the recipient is never in it; put that job in a front-on shot
   where the target can be visible in the same frame.
   **BUT SPECIFY WHAT AND WHERE, NEVER HOW. Chand's ruling 2026-09-27, and it is
   the other half of this rule.** After ep09 beat 3b came back with the spoon
   crossing the boy's face, his words were: "I think we are trying to control AI
   too much and messing it, should have kept the prompt looser to just say Roy is
   feeding the child." He is right, and the line between the two halves is this.
   **Name the contents, the destination and what fills the clip**, because the
   model cannot guess those. **Do not choreograph the limbs.** Beat 3b wrote out
   the whole cycle, carries it across and down to the lips, the boy raises his
   head, takes it, the spoon draws back and refills, and it was the choreography
   that broke. The model knows what feeding looks like. It does not know what is
   in the bowl.
   **A FACE CANNOT BE BOTH FULLY VISIBLE AND TURNED TOWARD SOMEONE WHO IS NOT THE
   CAMERA.** That is a self-contradiction and it belongs with "two directions at
   once" as something that blocks a prompt. Beat 3b asked for the boy's face
   "turned up toward the man and fully visible" while the man knelt above him in a
   vertical frame. The model resolved it by pointing the boy at the lens, which
   left his mouth aimed at the sky and forced the spoon down across his face.
   **Decide which one you want and write only that**: either the face is readable
   to camera, or it is turned to the other person, and a two-shot has to place
   them so one framing serves both.
   **THE MODEL BUILDS A WHOLE PERSON AND THEN CROPS. DESCRIBE THE BODY, NOT THE
   FRAME.** ep09 beat 6, 2026-09-27, 12 credits, Chand's catch and his words were
   "you are still not learning the basics of generation prompting". The prompt
   wanted him holding a letter with the paper out of shot, so it said his
   "squared shoulders and the plain collar of his kurta" fill the bottom of the
   frame and never mentioned his arms. It rendered with **both arms hanging
   straight down**, because arms-down is the default for a standing man and
   nothing said otherwise. Describing what fills the frame does not stage the
   body. **State the posture, including for limbs outside the crop**, as in "his
   forearms raised and both hands holding the paper at chest height".
   **This does not contradict rule 1.** Do not name an OBJECT or a PERSON you
   want absent, because naming draws it in. Do name POSTURE, because posture is
   not a thing that can be drawn in, it is a state the model must pick, and it
   will pick the default.
   **And the crop itself is a request, not a guarantee.** The same prompt asked
   for shoulders-up and got chest-to-waist. If a shot depends on a tight size,
   give the camera a named move into it rather than trusting the framing words.
   **NAME THE END STATE, NEVER POINT AT IT WITH "THAT".** Same clip, second
   fault. The prompt read "his eyes lower very slightly and come to rest, and he
   then holds completely still again in exactly that position for the rest of the
   shot". **"That position" has two possible antecedents**, the lowered eyes or
   the head-level start, and the model took the wrong one and raised his eyes
   back to the lens. Write the state itself: "his eyes stay lowered for the whole
   of the rest of the shot". Pronouns and demonstratives are a gap in the
   specification like any other, and rule 10 says the model fills gaps.
   **And check the reach of it before you shoot.** Beat 3's stirring would have
   killed beat 5 two beats later, where the turn is a full spoon halting in
   mid-air, because a halt only lands if the audience has watched the movement it
   interrupts. An underspecified beat can disarm a later one.

## Two people in one frame, and who speaks

Written 2026-09-16, after ep03 beat 2 took five takes.

- **A face that has to match a reference needs size and light.** In a wide, dark
  shot the face is a few dozen pixels and the model invents one. No wording
  fixes that: either the face is large in frame and lit, or the shot cannot
  carry identity. Take three failed on exactly this.
- **Two people of the same kind in one frame will swap.** ep03 made the
  noblewoman the maid. Wardrobe words float onto the wrong body, which is how a
  green saree landed on the wrong woman. Every wardrobe and posture word goes in
  the same sentence as the person it belongs to.
- **Show the supporting one from behind.** Chand's fix on take two, and it
  worked. A back removes a second face the model can get wrong.
- **A SECOND FACE THAT GETS NO WORDS GETS INVENTED, EVEN WITH ITS REFERENCE
  ATTACHED.** ep01 beat 3, confirmed on the frame 2026-09-29, Chand's catch.
  **Sushil comes back clean-shaven.** The prompt described Roy's face in full in
  the large foreground and gave Sushil, small in the background doorway, exactly
  this: "his friend (referencing the third character image) in a cream kurta
  leans against the jamb with anxious concern". No face, no hair, no moustache.
  `@sushil_young` was attached and did not hold. **Silence about a face is not
  neutral. It is a gap, and rule 10 says the model fills gaps.** ep05 beat 2 and
  ep06 beat 7 both write "a thick neatly groomed black moustache" and both
  shipped clean. So when two people share a frame, either describe both faces or
  give the second one no face at all.
- **A line of dialogue in the prompt attaches to whoever is on camera.** The
  noblewoman spoke the maid's line because she was the one in shot. A voice that
  is not the person on screen stays out of the prompt and goes on at the edit.
- **Rewriting the situation can be cheaper than re-rolling the shot.** After
  several bad staircase takes, Chand wrote the library scene so the geography
  worked, instead of fighting the model for a shot it kept refusing.
- **When the model draws someone different, casting can follow the render.** The
  figure behind the ep03 curtain looked like a woman, so the manservant became a
  maid, and the maid earned a scene of her own.

## Speech

Omni invented no dialogue across five draws, so a silent shot stays silent on
its own. When a character **must** speak on camera, write the line into the
prompt and attach their reference. Bengali lip sync works.

**TWO LANGUAGES IN ONE GENERATED LINE WORK, AND HERE IS THE EXACT WORDING.**
Chand supplied the ep00 prompt on 2026-10-02 and it came out fine, with his caveat
"of course, no guarantees". **Copy this construction rather than composing a new
one:**

    beginning in English and then switching mid-speech into Bengali, in one
    continuous delivery: "I have been to the Board myself. Nobody moved." then
    "বৃষ্টি না থামলে, ভোরের আগেই সব শেষ।"

**The two languages are two separate quoted strings joined by the word "then".**
Not one quoted string carrying both, which is what Claude first wrote for ep12
beat 1 and then corrected against this. Same class as every other
copy-the-shipped-wording rule.
**Name what the English sounds like in the voice description.** An unspecified
English accent is a gap and rule 10 says the model fills gaps, so the Minister's
voice text says his English carries the same Bengali cadence and retroflex
consonants, an educated Calcutta English.

**A SAVED FRAME CARRIES A FACE AND NO VOICE. THE CHARACTER CARRIES THE VOICE.**
Chand's question, 2026-09-25, and it caught a real hole: Claude moved her onto
the `@kalyani_library` saved frame to fix her face, without asking where the
voice would then come from. A frame is an image. If a speaking beat attaches
only a frame, Flow invents a fresh voice, which is the continuity problem that
closed back in K5.

**The fix is to rebuild the Character on the good frame.**
**ATTACHING A CHARACTER AND A SAVED FRAME OF THE SAME PERSON IS FINE AND IS WHAT
WE ALREADY DO.** Corrected 2026-09-29 on Chand's challenge, against the sidecars.
**ep04 beats 1, 3, 4, 5, 6 and 7 are all keepers and every one attaches
`ajitabha_sengupta` plus a saved frame of Sengupta himself**, `ajkan.jpeg`,
`ajkan_chair`, `ajkan_book` or `ajkan_cup`, and beat 7 carries his English
dialogue. ep01 beats 2, 3 and 5 do the same with Roy's sheet plus a saved Flow
frame of Roy. **The ep07 beat 5 failure was a frame holding SOMEONE ELSE'S face**,
`@sengupta_portraits`, attached while Roy was the subject. That is the condition
to avoid, and it is already rule one of the pre-flight. An earlier version of this
skill generalised it into "never attach both", which six shipped keepers contradict,
and acting on it in ep10 cost the room continuity between beats 1 and 2. Rebuilding is
cheap because **the Flow voice is a preset optionally re-styled by a written
description, and a voice sample cannot be uploaded**, so the voice is
reproducible from the text rather than being a unique artefact. That is the same
mechanism that made Roy's ElevenLabs voice and his Flow voice indistinguishable
to Chand from one description. If Flow allows swapping the image on an existing
Character, that is better still, because it re-derives nothing.

**TWO FLOW CHARACTERS IN ONE CLIP CAN SPLIT ONE LINE BETWEEN THE TWO VOICES. ep01 beat 3b,
2026-10-03, 12 credits.** The shot is Roy answering Sushil, and Claude's prompt attached
`dr_roy_young` AND `sushil_young` as Characters. **The line started in Roy's voice and finished in
Sushil's.** Flow maps a voice to a Character, so a second Character in the clip is a second voice
the line can be handed to.

**The precedent Claude was working from says the opposite and Claude flattened it.** ep11 beat 2
attaches ONE Character, `sushil_old`, plus a saved FRAME of the second person, `roy_1951_back`. The
rule that a second person's reference is fine when they are in the shot is about a **frame**. A
Character is not a frame. **One speaking person, one Character; everybody else gets a frame or
nothing.**

**Unverified and marked as reasoning:** the line itself names the other man, "জানি, সুশীল।", which
may be what invites the handover. Not worth a take to find out.

**The fix that shipped removed the second person from the frame entirely**, which costs nothing when
the previous shot has just established who is standing there.

**Voice references only work on ingredients-based generations.** Roy's proof was
run in Ingredients mode. A speaking beat generated any other way gets no voice
reference at all.

**Unverified and worth knowing:** a developer forum post dated 2026-09-11 reports
a recent Omni update breaking voice carryover entirely. Treat the first dialogue
take of any new Character as the test.

**A line of dialogue needs a mouth in frame.** If the shot is a macro or a back,
lay the line at assembly instead of writing it into the prompt, or the model
invents a speaker to attach it to. Monologue and narration are always laid at
assembly over a closed mouth and need no Character voice.

- Narration and interior monologue are ElevenLabs, laid at assembly. The clip
  must show a closed mouth.
- On-camera dialogue is generated. Load the line with bilabials if it is
  Bengali, so the lips visibly close.

**PUNCTUATION IS A DELIVERY INSTRUCTION, and it works on Flow as well as on
ElevenLabs.** Chand, 2026-09-27, on ep08 beat 2. Her line ended in a full stop,
"কিন্তু আপনাকে তো চিনি না।", and the delivery came back flat. Written as a
question, "কিন্তু আপনাকে তো চিনি না?", it gave a rising final contour and
"worked great". Same words, same voice, different mark. **So the terminal mark is
the cheapest performance control we have and it costs nothing to apply.** Choose
it for the delivery you want, not only for the grammar. Full stops where you want
a beat, short sentences over long ones, and a question mark where the line should
lift.

**AND NAME THE CONTOUR ITSELF WHEN A LINE MUST CLOSE.** Chand's catch 2026-10-02:
the first ep12 beat 2 take delivered a flat refusal as a question although the
line ends in a দাঁড়ি. **A full stop is necessary and it is not always sufficient.**
The wording that goes with it is **"his pitch falling steadily through the sentence
and settling low and flat on the last word, closing the matter"**.
**Write it positively and never write "not a question".** Naming the thing you want
absent draws it, which is proven twice here, so describe the falling contour rather
than forbidding the rising one. Same mechanism as "do not show her face" drawing a
face.

**The pause is ours, not the model's.** For narration and monologue, write a long
line as several short lines, generate them separately and place the gap on our
own timeline. `assemble.py` already resolves shot-relative cue times, so an exact
pause costs nothing and beats hoping the voice pauses where the comma is.

**THE THING THAT ACTUALLY LOST IT WAS FILING, NOT CRAFT.** The question mark was
used in a discarded ep08 beat 2 take, worked, and never reached the keeper's
prompt, so the shipped episode carries the flat reading. **Before a take goes
into `_retired`, diff its prompt against the keeper's and write down which
differences were improvements.** A fix found on a reroll is paid for and must not
be thrown away with the clip.

## Cultural rules. Getting one of these wrong reads as slop.

Claude cannot infer these and must not guess at them. When a shot touches
custom, ritual or household manners, say what you are unsure of and ask.

- **A book is Saraswati.** It is never put on the floor, on a step, or
  anywhere it could be stepped over. Handing a book is the respectful form.
- **Shoes come off indoors.** The beat 3 footage has him barefoot in the hall,
  which is correct, so the arrival shot has to show the sandals coming off.
- **Chand's culture beats a model's opinion, every time.** Three reviewers
  flagged a direct handover as improper for the period; he ruled it fine and
  the step was the real error. Weight of numbers is not evidence here.

## Series facts a prompt must not get wrong

- **Dr Biren Chandra Roy.** Invented, mirrors a real man. Born about 1882, so
  he is 29 in 1911 and every other age follows from that.
  **He is in London from February 1909 to 1911, so there is no Calcutta scene
  for him in 1909 or 1910.** This killed a drafted 1910 flashback on 2026-09-24
  and is the reason ep08's flashback sits in 1908. It is also forced by shipped
  material rather than by research: ep03 beat 7 is his monologue "তুমি জানতে,
  আমি ফিরব", she knew he would return, so she has to know him before he sails.
  ep04's shipped "MRCP and FRCS in two years" fixes the length of the absence. **The face follows
  the year in the shot, not the episode number.** Rewritten 2026-09-20: the old
  mapping keyed faces to ep01 through ep19, went stale when the series was cut
  to twelve, and was never quite right anyway, because an episode straddling
  two eras needs two faces.

  | Reference | Years | Age | Spectacles |
  |---|---|---|---|
  | `dr_roy_young.jpg` | 1908 to 1923 | 26 to 41 | none |
  | `dr_roy_middle.jpg` | 1926 to 1944 | 44 to 62 | yes |
  | `dr_roy_old.jpg` | 1947 to 1962 | 65 to 80 | yes |

  **Glasses arrive with the middle face.** Chand's ruling 2026-09-20: middle age
  wears them and that is settled. The middle sheet was generated with round thin
  wire rims in its face, so the glasses come with the reference whether the
  prompt asks or not. That is also why ep05 used the young sheet at 41: asking a
  bespectacled reference for a bare face is a fight we lose, and it would have
  spent the glasses early.

  **Age the face in the prompt. Never swap the reference to get an age.** ep05
  put "about forty years old, his face fuller and more settled than a young
  man's, with faint lines at the corners of his eyes and the first grey at his
  temples" on the young sheet and it held across four shots. So the young sheet
  stretches to about 41, further than its 29-year-old portrait suggests.

  **Which face, against the twelve-episode plan.**

  | New episode | Years | Face |
  |---|---|---|
  | 1, 3, 4 | 1911 | young. New 1 also ends in 1951, on a nameplate with no face |
  | 2 | 1951 | old |
  | 5 | 1923 and 1908 | young throughout |
  | 6 | 1926 and 1932 | middle |
  | 7 | 1939, with an 1911 flashback | middle, young in the flashback |
  | 8 | 1940, then 1908 and 1909 | middle in 1940, young in the flashback |
  | 9 | 1943 | middle |
  | 10 | 1944, with the 1911 refusal | middle, young in 1911 |
  | 11 | 1947 to 1950 | old |
  | 12 | 1950 and 1951 | old |
  | 13 | 1955 and 1962, then after his death | old, aged on further in the prompt |

  **THE SERIES IS THIRTEEN EPISODES, not twelve.** Chand's ruling 2026-09-24. A
  new episode 8, "The Architecture of Desire", was inserted to show the
  relationship, after a viewer said the connection between them is never
  explained or shown. The Epidemic moved from 8 to 9 and everything below it
  shifted by one. `episodes/series_beats_12.md` still carries the old twelve
  numbering and has not been renumbered yet.

  **Episodes 7, 8 and 10 carry two Roys in one episode.** Build the reference
  chain for those before shooting rather than during, the way ep05 needed two
  anchors for its two eras.
- **The woman is never named. She speaks only in episode 8.** `the_woman.jpg`.
  She does not age. Mostly a hand, a silhouette, a reflection; her full face is
  a deliberate, rare event.
  **Chand's ruling 2026-09-24 reverses the old "never speaks" rule for one
  episode.** His reason: sustained silence across a whole relationship episode
  reads as an affliction rather than as withholding. She has **three lines in
  ep08** and none anywhere else, so the old rule still holds for every other
  episode. Claude argued to keep her silent, was overruled, and the overrule was
  right.
  **Roy addresses her as "মিস সেনগুপ্ত", Miss Sengupta.** Chand's ruling. He can
  only use her father's surname, which keeps the never-named rule intact and
  says the thing outright: the man who invents a name for her in 1951 begins
  with no word of his own for her. **She calls him বীরেন and he never crosses
  back.** That asymmetry is the relationship.
  **Her colour marks the year, and she still changes within a year.** Ruled by
  Chand 2026-09-25, correcting Claude's ivory-throughout reading. **Ivory is
  1908 and jewel green is 1911.** Inside 1908 she changes by occasion: cream-ivory
  with a rust-red and gold zari border for the afternoon, ep05 and ep08 beats 2
  and 3 as shipped, and **dusty rose-pink for the midnight scene**, ep08 beat 4.
  Months apart, so one unchanging garment reads wrong.
  **Under a single candle, choose a warm colour.** Warm amber light turns blue
  and green silk grey and muddy; pink and ivory glow and stay readable. Do not
  make the saree carry the palette's cool note in a candlelit shot; give that to
  something else, such as the night beyond the window.
  **When the prompt's garment differs from the reference frame, point only the
  face and hair at the frame.** Writing "exactly as in @tag" about a garment the
  frame does not show sets the two fighting.
  **Her Flow Character voice was made 2026-09-25** by Chand, from a description
  naming pitch, texture, pace and manner plus "an elegant, upper-class
  Kolkata-educated cadence". Claude's one note was that it carries no consonant
  clause, which is the part that was load-bearing on Roy's, where naming
  retroflex consonants worked and naming a region alone failed in both
  directions.

  **ANCHOR HER ON A SAVED FRAME, NOT ON THE CHARACTER SHEET.** Ruled by the
  render, 2026-09-25, after ep08 beat 2 came back as a different woman for 12
  credits. Chand's words: "it looks like a different person." `the_woman.jpg`
  is a portrait sheet and it did not hold. Use **`@kalyani_library`**, the
  1080x1920 saved frame Chand pulled from the ep05 library clip, in every ep08
  beat where she appears. Note the ep05 clip's own prompt file is **not**
  evidence of anything: its sidecar says "prompt not used; this take predates
  it", so the frame is the truth and the text beside it is a later description.

  **Describe what is actually in that frame, all of it.** The failed take got
  the room right and her wrong, because the prompt named almost nothing she
  wears. As shipped she has a **centre-parted low bun at the nape with fine
  loose wisps at the temples**, a **cream-ivory silk saree with small woven
  motifs** in the flat unpleated Brahmo drape, a **deep red border carrying a
  broad band of gold zari**, a cream blouse, a **small round red bindi**, **gold
  drop earrings** and a **thin gold bangle**.

  **NO AGE IN YEARS FOR HER EITHER.** Chand, 2026-09-25: "it makes it younger
  and look different. She needs to look the same as in the frame as in ep5
  1908. And that is how she looked then." The frame already is her at that age,
  so "she is about nineteen years old" is a build instruction competing with it,
  and the model constructs a face instead of copying one. This is the same
  mechanism as the ep07 beat 5 Roy failure that cost 24 credits, and Claude left
  the clause in her prompt after writing that rule up. **Wardrobe and hair still
  get described**, because the failed take got them wrong and because they point
  at the frame with "exactly as in @kalyani_library" rather than inventing
  anything. The ban is on the face.

  **"Hair drawn back" is ambiguous and drew it loose.** Write "parted in the
  centre and drawn back flat into a low bun at the nape of her neck". A loose
  fall changes the whole silhouette of a face and is on its own enough to read
  as somebody else.

  **KEEP HER FEET OUT OF IT.** Chand's ruling 2026-09-25, correcting Claude,
  who had written "her feet are bare". His reasons: she may well have worn house
  sandals indoors, and the way an aristocratic woman wears a saree her feet are
  barely visible anyway. **Do not specify bare feet and do not specify sandals**,
  because either one puts them in frame and invites a mistake. Say instead that
  **the saree falls full length to the floor and covers her feet completely**,
  which is positive description and is how the garment actually hangs. This is
  hers specifically; Roy is still barefoot indoors and ep03's hall footage shows
  it.

  **Naming footsteps on a hard floor can render as a sharp heel clack.** Chand,
  2026-09-25, on the ep08 beat 2 take: the audio came back "clack clack, which
  sounds like heels", from the clause "two slow unhurried footsteps on a hard
  tiled floor". For her, use **"the faint tactile whisper of silk"** instead,
  which is the wording ep03 beat 4 and ep05 beat 5 both shipped. Footsteps are
  not banned in general: ep06 beat 1's "two sets of unhurried footsteps on a
  stone floor" shipped fine. It is a hard floor plus a woman in silk that goes
  wrong.

  **She must come to rest LARGE in frame.** In the failed take she stopped too
  far back and the face never got the pixels identity needs.

  **Tag collision worth knowing: `library_1908` is ep05's UNIVERSITY library**,
  pale wooden plank floor, no mosaic. Sengupta's house library is a different
  room and its tag is **`library_house_1908`**. Naming the wrong one imports
  the wrong floor, and the blue-and-white mosaic floor is the thing that says
  which house this is.
- **Dr Ajitabha Sengupta**, invented, `dr_sengupta.jpg`, and he speaks
  **English**. Chand's ruling 2026-09-14: **the shipped shot is canon**, not the
  character sheet. Note the mechanism is the opposite way round, established on
  ep04 and re-checked 2026-09-24: the sheet shows GOLD rims, ep04's prompt said
  SILVER, and silver is what rendered. **The prompt drives the render, so the
  prompt must describe what shipped.** As shipped he has a full thick white-grey
  moustache, thin **oval silver** wire rims, a plain cream fine-cotton kurta with
  a self-embroidered placket, and a long dark burgundy shawl in gold-brown
  paisley brocade over his left shoulder. Roy wears **round pale gold**, so the
  two bespectacled men stay distinct.
- **Sengupta joined the Brahmo Samaj in 1888.** Chand, 2026-09-24. Brahmo dress
  is sober and reformist: white dhoti, long dark buttoned coat or a plain shawl,
  some sober Western frock coats, no ornament beyond a watch chain, and **no
  religious imagery** anywhere in the house. **Bengalis do not wear turbans, and
  Brahmos certainly not**, so every head in his portrait gallery is bare. Ancestor
  portraits are Bengali men only, no women. Getting this wrong draws Rajput
  maharajas in jewelled turbans or British sitters, which is Chand's catch.
  **This is also why the woman wears the unpleated Brahmo saree drape**: Chand
  chose it for the elegance of the flat, unpleated fall, against the bunched
  modern wedding pleat. It is a look, not just a period marker.
- **NO PURDAH IN THIS HOUSE. No jali, no screens, no latticed galleries.**
  Chand's ruling 2026-09-24. Brahmos opposed the seclusion of women, and the
  shipped record already says so: **ep03 beat 7 has her alone in the library with
  Roy, face to face, putting the book into his hands.** A screened mezzanine
  would contradict a scene that has already aired. ep07 beat 7 was drafted with a
  brass-latticed screen, from the beat sheet, and it had to come out.
  **Her withholding comes from distance, from her back, and from her not
  stopping, never from architecture that shuts her away.** Open carved railings
  are fine; a screen she is kept behind is not.
- **His house has several grand rooms, and they are not interchangeable.**
  Chand's ruling 2026-09-24. ep03 and ep04 use the book-lined **library**, shot
  dark in monsoon evening, and its saved frame `@library` exists but is too dark
  to reuse in daylight. ep07 beats 4 to 6 are a **long portrait gallery** hung
  with zamindar oils, in bright late-morning daylight. ep07 beat 7 is the
  **entrance hall** with a brass-latticed mezzanine screen. Do not force a new
  scene into an old room just to reuse its frame: a rich Calcutta mansion
  plausibly has many, and a wall of ancestor portraits argues the class point
  that a wall of books cannot.
  **What ties them to one house is the floor**, the distinctive blue-and-white
  patterned mosaic tile, named in every room. Change the room, keep the floor.
- **NURSE MITRA IS NEVER SEEN. She is a voice, a white sari and a hand.** Chand's
  ruling 2026-09-27, replacing the drafted face sheet, which is parked in
  `refs/reference_prompts.md` with the reason beside it and must not be
  generated. **Two reasons, and the second is his and is the stronger one.** Her
  lines in ep09 beats 4 and 6 are news arriving, so the shot belongs on the face
  of the man receiving it, and cutting to a nurse throws the payoff away. And **a
  prominent second woman reads as a romantic or friendly interest for Roy**,
  which this series cannot afford, because the whole architecture is one
  withheld woman.
  **So both her lines are laid at assembly in ElevenLabs**, not generated, which
  means she needs **no Flow Character, no voice carryover test and no face
  anchor**. That removed the only blocker ep09 had.
  **What may enter frame:** a plain white fine-cotton sari at the edge of the
  shot, and a hand holding the telegram. **Bare wrist, no bangles and no
  vermilion**, which is his widow reading and the reason a woman of her
  generation is working. **One small plain silver ring** on a finger, which is
  the only ornament that would actually read in a hand-and-telegram shot. Her
  ep06 appearances already showed her back twice, so nothing contradicts this.
  **Her drafted voice description still stands**, but it is now an ElevenLabs
  voice rather than a Flow Character: low and level, slightly grainy, firm
  retroflex consonants, unhurried and even, warm underneath and never raised.
- Refs live in `series/city-built-on-heartbreak/refs/`.

## STILLS ARE FREE. USE THEM. Ruled 2026-10-02.

**Chand's plan generates as many stills as he wants at no cost.** That was established on
2026-10-02 and it changes two things.

**1. A STATIC SHOT SHOULD BE A STILL, NOT A VIDEO.** If nothing in the frame moves, a video
generation buys nothing and costs credits. Generate the still, then put the camera move on it in
VN at the edit, which also gives a slow drift that a locked-off generation cannot. ep12 beat 4,
a top-down macro of a blank page, went this way and saved 6 credits.
**But a living face is not a static shot.** Breathing, micro-movement and blinks are what make a
person look alive, and a held still of a person reads as a photograph. Pages, plinths, objects
and empty rooms are candidates. People are not.

**2. A FREE STILL TESTS A COMPOSITION BEFORE YOU PAY FOR THE VIDEO.** Both ep12 takes wasted on
2026-10-01, 24 credits, would have shown their fault in a still: a dozen white men in Western
suits, and a man full length at a small desk looking like a clerk.
**Write the still prompt as the END state** of the shot, since a still cannot carry motion, and
check the staging, the people, the light direction and the blank surfaces.
**PROVEN ONCE, 2026-10-02, ON ep12 BEAT 5.** The free still passed all five checks written for
it: every person Bengali and seen from behind, the slab blank, the sun behind the camera, the
cracked concrete with weeds through the joints, and no face anywhere. **It also found the thing
the test could not cover**, which is the more useful result: the still attached no reference, so
the ground did not carry ep11's distant tree line and river bend, the landmark that says this is
the same plain one year on. That went into beat 5's prose using ep11 beat 5's own shipped
sentence rather than being left to the tag.
**So the real value of a still test is as much what it cannot see as what it can.** Write down
what the still is blind to before you run it.

**A CHECK LIST BLINDS YOU TO EVERYTHING NOT ON IT. Chand's catch, 2026-10-02, on ep13 beat 7.**
The still was run with five written checks: the book's wear, the stethoscope, the hand anatomy, the
blank cover and no face. All five passed and the still was called clean. **It had also shown that
the arm came in horizontally from the right at table height, which is a man standing beside the
table rather than a dying man reaching from his bed**, and neither of us saw it, because we were
reading the list. The video then rendered the same standing geometry and Chand spotted it only in
the clip.

**The cause is that the prompt never said where the hand came from.** It said "no faces, no heads
and no shoulders", which removes the body from the frame without ever saying the body is in the
bed. That is the ep09 class of fault: six of eight faults were things left unsaid.

**So every still test gets one unwritten final check: what does this image imply that no sentence in
the prompt specified?** Era, class, who is standing where, what is out of frame holding the thing in
frame. Ask it out loud before calling a still clean, because the written checks will not ask it.

**A STILL TEST GOES STALE THE MOMENT THE COMPOSITION CHANGES. RE-RUN IT.** Chand's catch
2026-10-02. The ep12 beat 5 test passed all five of its checks, and then the crowd moved from
behind the plinth to the near foreground, which is a bigger change than anything the test had
looked at. **A passed test covers the prompt it was run on and nothing else.** Re-running is
free, so there is never an argument against it, and the new checks go at the top of the list
because the new risk is always the one the change introduced. Here that risk was the foreground
crowd swallowing the base of the plinth, which is where the silk heaps.

**YOU CAN HAVE THE LOOK WITHOUT THE WORD.** Same still. ep12 never writes "police", because
occupation words are what the policy filter reads, and "a line of men in plain khaki standing
shoulder to shoulder" rendered as **full uniforms with peaked caps and belts**. The filter reads
the word and the model reads the description, so describing the uniform gets the institution
without ever naming it. Same family as ep02 giving age, build and bearing and never saying what
the man does.

**STILLS COME FROM FLOW. Chand, 2026-10-02, correcting Claude.** This line previously said "the
still generator is not Omni" and used that to discount a passed still. **That was never checked and
it is wrong.** Stills are generated in Flow, on the same plan, which is why they are free. Claude
inferred a separate image generator from a loose phrase in the ep12 record and then wrote the
inference into this skill as fact, where the next session would have read it as settled. **A
reasoned guess written into the record as though settled outranks nothing**, which is the same
failure that cost ep12 beat 9 its subtitle.

**What still holds: a still test disproves a prompt more reliably than it proves one**, because a
still cannot carry motion, cannot show what fills the clip after an action ends, and cannot show
whether a held pose drifts. ep13 beat 7 is the proof: the still was clean and the video still
opened on its attached reference and hard-cut at 0.4167s. Treat a clean still as the removal of the
risks it could see, never as permission to skip the pre-flight list below.

**AND A STILL YOU LIKE CAN BE ATTACHED TO THE VIDEO PROMPT. Chand, 2026-10-02.** Since it comes from
Flow, the tested composition becomes the reference for the paid generation, and the reference and
the prose agree by construction, which is the condition every reference failure in this project has
violated.

## PRE-FLIGHT. Run this list over every prompt before it reaches Flow.

**THE TWO-MODEL GATE IS DROPPED. Chand's ruling 2026-09-27.** It ran from
2026-09-12 and it was spending his hours on the wrong thing. The evidence
against it: its advice list has never once been confirmed by a clip, nine of
ep01 beat 1's ten versions died on model predictions that were never tested,
and the best clip in the project breaks three of those rules. Meanwhile every
expensive failure of the last four sessions came from something the gate does
not look at.

**What replaces it:** this fixed list, where every item is traceable to a clip
that actually failed, plus Chand's own read. **Gemini stays available for one
quick check on a prompt where neither of us is confident.** No elaborate round,
and no rewriting: a reviewer gives quoted faults and predicted render failures
only, because an early review once rewrote a whole prompt and silently deleted
two working instructions.

### THE DEFAULT IS WHITE. CHECK THIS BEFORE ANYTHING ELSE.

**ep12 beat 1, 2026-10-01, 12 credits, Chand's catch: a grand colonial room came back full of
WHITE MEN.** Chand's words: *"Where did Kolkata go, where did the year go? Why do we keep
propagating the same mistakes after shooting 11 episodes?"*

**The mechanism, and it is why eleven episodes of guardrails did not catch it.** An unspecified
person is drawn from the model's default, and that default is white. **Every identity rule in
this skill is about a character who HAS a reference**: the six pre-flight items below, the
copy-the-shipped-wording rule, the two-people-in-one-frame rules. **Not one of them covers a
person with no reference**, and those are exactly the people nobody writes a sentence about.
Worse, the clause that keeps background faces safe, "seen from behind and held in heavy soft
focus", reads as permission to say nothing else about them. Silence is not neutral. Rule 10 says
the model fills gaps, and this is the gap it fills with itself.

**So this is a default, not a thing to be vigilant about.**

1. **NAME THE CITY OR THE REGION IN THE PROSE OF EVERY PROMPT.** Counted 2026-10-01: **74 of the
   93 shipped prompts name Calcutta or Bengal.** ep11 beat 1 opens "inside a long covered railway
   platform in Calcutta in 1947" and shipped. **The room was never the policy trigger**, and a
   ban on naming the city is a misreading of item 11 below that cost a take. The trigger is
   occupation plus a year plus an act the real man is known for, and the fix for that is to say
   nothing about what a man does, never to delete the city.
2. **DRESS EVERY PERSON IN THE FRAME, INCLUDING THE ONES WITH NO FACE.** The shipped wording is
   ep11 beat 1's: "Every person in the crowd is dressed in the plain, worn cotton clothing of
   rural Bengal of that year, the men in white dhotis and plain collarless cotton shirts and the
   women in plain undyed cotton sarees drawn over the head." Say who they are and what they wear
   in the same sentence that says they are turned away.
3. **COUNT THE PEOPLE IN THE SHOT, THEN COUNT THE SENTENCES ABOUT WHO THEY ARE.** If a shot has
   people in it and no sentence naming their origin, the prompt is not finished.

**BUT THE PLACE WORD CAN ITSELF BE THE TRIGGER, AND IT IS THE FIRST THING TO DROP UNDER A
REFUSAL. ep13 beat 4, 2026-10-03.** The prompt was refused under a prominent-people clause.
Claude proposed three variables in order: the abstract descriptor "an elderly man of great
authority", the full-length coat, and the sheet of paper. **All three were wrong. Chand removed
"in Bengal" and nothing else, and it passed.**

**This does not reverse item 1 above, and do not let it.** Deleting the city is what filled ep12
beat 1 with white men, and 74 of 93 shipped prompts name Calcutta or Bengal. The resolution is
that the two clauses do different jobs. **The Indian garment word is what holds the ethnicity**,
confirmed three times now. **The place word is what pushes an old Bengali man at a desk over the
line into a real public figure**, because region plus age plus gravity is a near-identification.

**So: name the place by default, and when a prompt carrying a grave elderly man is refused, drop
the place word FIRST and keep every garment word.** ep13 beat 1 passed with "in Bengal" because it
has no line in it; beat 4 is the same man in the same room and was refused the moment he spoke.

**THE CHEAPEST FIX IS AN INDIAN GARMENT WORD, AND IT IS NOW CONFIRMED TWICE.** A sentence about
where people are from is worth having, but the thing that actually holds is naming a garment only
an Indian man wears. ep07 beat 2 dressed its side men in **"cream silk achkans"** and every one
rendered Indian, on one take. ep12 beat 1 dressed its side men in **"dark high-collared achkans
over plain white cotton punjabis"** and every one rendered Indian again, checked on a
full-resolution crop of both sides. The failed ep12 beat 1 v1 had an origin sentence and no
distinctively Indian garment, and came back as a dozen white men in Western suits. **Achkan,
punjabi, dhoti, kurta and saree are load-bearing words. "Formal coat" and "plain clothing" are
not.**

**The check is mechanical and costs nothing. Run it on every prompt before it reaches Flow:**

    grep -L "Calcutta\|Bengal\|Kolkata" assets/epNN/beat*/prompt.txt

Any file it lists either has no people and no place in it, or is about to render the default.

### A CHILD CANNOT BE ANCHORED BY AN IMAGE. Flow refuses it. 2026-10-02.

**Chand on ep12 beat 7: Flow would neither save a frame of the child from a shipped clip nor
accept an uploaded PNG of her.** His read is a child-safety policy and it is unconfirmed, but the
behaviour is confirmed twice, by two different routes, on the same image.

**What still works: a Flow Character of a child.** ep12 beat 6 ran on `@girl_1951` and came back
a one-take keeper, and the Character was built from a still made in the image generator, which
does produce children. So the block is on getting an image INTO Flow, not on the child existing
inside it.

**So for any child in this series, plan on the Character as the only anchor, and put the
wardrobe, the hair and any held object into words in every prompt.** A tag you cannot attach
carries nothing. Decide this before writing the prompts, not after, because it changes the
reference plan for every beat the child appears in.

### Identity and voice. Check this class first. All the money is here.

About 48 credits went on these three in four sessions, and none of it went on
staging, colour or audio. **Decide all of an episode's anchors before writing
any of its prompts**, not while writing them.

0. **Is the face large enough and lit enough to carry identity?** In a wide or
   dark shot a face is a few dozen pixels and the model invents one. No wording
   fixes it. ep03 beat 2 take three and ep08 beat 2 both failed here.
1. **Does the reference frame hold the face of someone who is NOT IN THIS SHOT?**
   That is the condition, and **it is narrower than Claude keeps making it.**
   ep07 beat 5 attached `@sengupta_portraits` **for the room**, with Sengupta nowhere
   in the shot and Roy as the subject, and the result was a blend, "older and plumper".
   **ATTACHING A SECOND PERSON'S FRAME FOR A SECOND PERSON WHO IS IN THE SHOT IS FINE
   AND IS WHAT WE ALREADY DO.** Chand's correction, 2026-10-02, and the record is
   plain: **ep11 beat 2 attaches `sushil_old`, `platform_1947` AND `roy_1951_back`**,
   a frame of Roy's head from behind, in a shot where Sushil is the subject and Roy is
   seen from the back. One take, shipped. His words: *"without attaching, it gives a
   wrong render."* ep12 beat 7 is the same shape, Roy speaking with the child's back
   in the near foreground, and it attaches `@girl_flower`.
   **SECOND TIME THIS RULE HAS BEEN OVER-APPLIED AND CORRECTED BY CHAND.** The first was
   2026-09-29, when "never attach a Character and a saved frame of the same person" was
   contradicted by six shipped keepers and cost ep10 its room continuity. Note also that
   ep07 beat 5's own sidecar names **a face description where there should have been
   none** as cause one; the reference was cause two. Do not quote that beat as a
   reference-attachment rule alone.
   **When you attach a frame for someone seen from behind, say so and say nothing
   changes:** "seen from behind only, with no part of her face turned toward the lens",
   plus the same hair and the same garment type as in the tag.
2. **Is the anchor a shipped frame rather than a portrait sheet?** A sheet did
   not hold for her at ep08 beat 2. Sheets are for a character with no rendered
   frame yet; after that the frame is the truth.
3. **Does the character speak in this shot?** Then the anchor must be a **Flow
   Character**, because a saved frame carries a face and no voice, and Flow maps
   the voice to the Character. **Rebuild the Character on the good shipped
   frame.** Attaching a Character plus a saved frame OF THE SAME PERSON is fine and
   is what ep04 does across six keepers. What the ep07 beat 5 blend condition
   forbids is a frame holding someone else's face, which is item 1 above. Speaking beats run in Ingredients mode or get no voice
   reference at all.
4. **Is there any age in years for a character who is already that age in the
   reference?** Delete it. It makes the model construct a face instead of
   copying one. ep05 is the only place an age belongs, where Roy is 41 against a
   29-year-old sheet.
5. **Is the description freshly composed?** Grep the shipped prompts and reuse
   the sentence that worked in the matching situation.
6. **Low angle plus a tipped-back head?** That destroys a face, ep07 beat 7, 12
   credits. If the shot needs his face, eye level and lit from the front. If it
   needs a low angle, frame him from behind or in profile.

### Blocks the prompt. All three have failed on a real clip.

1. **Two directions at once.** Down then up, toward then away, facing then
   turned. The first beat 1 said shoes "stepping down onto" the stone and then
   the man "walking away up the steps". The model rendered his feet front-on,
   flipped them backwards, and walked him the wrong way.
2. **Unheld objects.** Anything carried or worn whose supporting hand is
   outside the frame you asked for. Same clip: an umbrella floated above his
   head with nobody holding it, because the shot opened on feet.
   **One object carrying another gets separated**, ep04 beat 4b, 2026-09-19.
   The prompt said to slide beneath the saucer and lift the cup and saucer
   together in one movement. The model lifted the cup alone and left the saucer
   on the table. Same class as the umbrella: this model is unreliable wherever
   one object has to carry another.
   **And say which way a handle faces relative to the hand.** That cup's handle
   pointed away from the side the hand entered from, so the model invented a
   handle under the fingers and gripped the bare body of the cup.
   **The cheap fix for both is editorial, not another generation.** Cut away
   before anything leaves the table. An unfinished reach plays tenser than a
   completed pickup, and nothing broken reaches the screen.
3. **A move named only by its direction. REFINED 2026-10-03: the failures are all AWAY from the
   camera.** Toward the lens is three for three: ep13 beat 9 take 2 (a very old man walking at the
   camera while speaking), ep13 beat 10 (two women walking at the camera, laughing), and ep00 scene 4,
   the best clip in the project, where a woman walks in, stops and turns. **The three failures all ask
   the subject to go away from the lens or give no destination at all**: ep03 beat 3 walked up the
   stairs instead of down, ep01 beat 1 flipped the feet, and ep09 beat 1 brought a man toward the
   camera before sending him out. Claude quoted "nought for three" against three toward-camera moves
   this session and was wrong each time.
   **So: a subject moving toward the lens and coming to rest is reliable and is the house move.
   A subject moving away from it is not, whatever you attach.** ep03 beat 3 said she steps down the
   stairs, and she walked up. ep01 beat 1's feet flipped the same way. **The
   failure is now proven on three clips**, the third being ep09 beat 1 on
   2026-09-27, where a man written as walking away toward the far end of the
   street approached the camera first and then turned.
   **THE REMEDY HAS BEEN TESTED ONCE AND DID NOT HOLD. Chand doubted it and he
   was right.** ep09 beat 1 named what the move ends on, "moving steadily toward
   the pale haze at the far end of the street", and the model still brought him
   in before sending him out. Treat a direction-only move as unreliable whatever
   you attach to it, and if the direction matters, prefer a shot where the
   subject's back is the only thing the camera ever sees, or cut before the move
   resolves.
   **And do not put a specific person in a shot that cannot identify them.**
   Same clip. It asked for "a straight-backed middle-aged man" at distance with
   no reference and no face, and he came back bald, because nothing described his
   hair and there was nothing to copy. A man who cannot be identified is not the
   character, he is a stranger. If the beat does not need that person, put nobody
   in it.

### Four slips that each cost a take, and all four are one-line checks.

7b. **THE ANTI-REPEAT CLAUSE FAILS ON A VERY SHORT LINE. ep13 beat 6, 2026-10-02.**
   The prompt carried the full shipped wording, "he speaks his line once only, beginning as the
   clip opens and finishing well before the clip ends", and the model **still said it twice**, at
   0.000 to 0.414 and again at 5.609 to 5.936. The line was one word, "Done." The clause has held
   on every multi-word line we have shot, including ep13 beat 5 the same day, where a four-word
   Bengali line ran once at 2.799 to 4.090. **A one-word line leaves about seven seconds the model
   has to fill, and it fills them by bookending the word.**
   **So for a line of one or two words, do not write "beginning as the clip opens".** Write the
   silence at the head explicitly: the action happens first, his mouth stays completely closed and
   still from 0:00 until the action is finished, and only then does he speak, once.
   **It cost nothing here**, because the second take of the word landed on the right moment and the
   head trims off. Chand kept it and did not reshoot.
   **AND THE OTHER HALF OF THE CLAUSE IS ALSO UNRELIABLE. ep13 beat 9, 2026-10-02.** The mouth did
   not close after the line: audio ended at 5.089 and he was still mouthing silently at 5.9, widest
   at the end of the clip. **So two of ep13's three speaking beats had a tail fault**, one doubling
   the line and one mouthing past it, against one clean beat. Small sample, but assume the tail of a
   speaking clip is unusable and plan to cut on the last syllable, which costs nothing because the
   tail was never going to be used.

8. **Dialogue removed from the prompt but left in the audio list.** ep03 beat 2
   was rewritten to be silent and kept a clause asking for "the clean spoken
   Bengali dialogue", so the model wrote its own line. When the speech goes, it
   goes from the audio block too.
9. **Is anything in this shot shorter than the clip, and did you say what
   happens afterwards?** A line, a movement or a gesture that finishes early
   leaves time the model will fill by repeating it. See rule 10. This is the
   check that would have saved ep09 beat 2.
10. **Does every movement have a named destination, and every vessel named
   contents?** See rule 10. This is the check that would have saved ep09 beat 3.
11. **The policy trigger: occupation plus a year plus an act the real man is
   known for.** ep06 beat 3 was refused twice. The institution was never the
   problem, and occupation alone is not either, since ep05's "the physician"
   passed. **Use ep02's idiom and never say what he does:** "the elderly man
   from the reference image", "the elderly statesman from dr_old". Give age,
   build and bearing, and let the reference carry who he is. Check the reference
   tags too, since they sit in the prompt as words, which is why
   `@mayor_office` became `@office_1932`.

### Advice. Chand reads it and decides, and the clip settles it.

These were predicted by text models. None has yet shown up on a clip we
generated. Of beat 1's ten versions only v1 was ever shot, and it failed on
the two faults above. The other nine were stopped on predictions like these.

**And the best clip in the project breaks three of them.** ep00 scene 4: the
woman walks in from the frame edge, stops, turns, looks, her expression
shifts, and the camera pushes in to her face. Five things in eight seconds,
one take, and it worked. So a reviewer raising one of these is a warning worth
reading, never a reason on its own to rewrite a prompt.

4. **Framing against content.** A shot close enough to read a face cannot see
   the floor. Ask for both and the model crops the action or melts the hands
   toward it.
5. **Action density.** Count the discrete physical actions. More than three in
   eight seconds and the model rushes, merges or skips them.
6. **Anatomy traps.** Feet and hands seen from behind or below, sustained
   gait, and turning 180 degrees while holding a pose. Arms folded then
   unfolded then turned smears the arms into the torso.
7. **THE FRAME EDGE. This is the big one.** Beat 1 took nine versions and
   twelve credits, and every single fault the gate found sat at a boundary:
   feet at the bottom, umbrella at the top, hands at the bottom, a case at the
   bottom, background geography past the sides. Each rewrite moved the fault to
   a different edge. **This model is reliable in the middle of a frame and
   unreliable at its edges.** Put nothing at an edge that needs anatomy or
   geography to resolve. If a shot needs hands, put them in the middle. If it
   does not need them, frame them out entirely.

**Subtracting a contradiction is not the same as subtracting the trap.** The
first beat 1 rewrite removed the up/down conflict and kept the rear-view
walking feet, which the reviewers predicted would fail. That prediction was
never tested.


## What ep11 changed. 2026-09-30, eight beats, one refusal, one wasted take.

**NAME THE PHYSICAL SETUP, NEVER THE RENDERED APPEARANCE.** ep11 beat 8, 12 credits.
The shot wanted a backlit man reading as a silhouette. Claude wrote "a full, deep,
near-black silhouette" and put **"deep near-black silhouette" in the colour list**,
which is the one place this format says *these are the colours of the things in
shot*. It rendered a man in a **black kurta** in ordinary daylight. Gemini's draft
had said "silhouetted vast and still" with white named in the garment clause and in
the palette, and it was right. **"Heavily underexposed" is a lighting word and
ships in five ep03 prompts. "Near-black" is a colour word.** Write the cause, not
the result: the sun is behind him and the exposure is held for the sky, therefore
he falls into deep shadow.

**BIND THE PERSON TO THE REFERENCE, ALWAYS.** ep11 beat 4 was refused by the policy
filter saying "An elderly statesman is seated at a heavy dark teak table", and
passed as "The elderly man from @dr_roy_old is seated". **ep02 never describes a
man in the abstract**; all seven beats say "the elderly man from the reference
image" or "the elderly statesman from dr_old". Three things changed at once on that
fix, so which one cleared it is unknown. Also dropped: the year from the prose,
since a year card carries it at the edit.

**CHECK TAGS FOR PROPER PLACE NAMES, NOT ONLY OCCUPATIONS.** `@sealdah` and
`@kalyani_land` both named a real place, and the second named the city two episodes
before it is named on screen. They became `@platform_1947` and `@dry_land`. Same
class as `@mayor_office` becoming `@office_1932`.

**A TAG CARRIES THE CLOTH, NOT THE SILHOUETTE. NAME THE GARMENT TYPE.** Chand,
2026-09-30. Pointing at a tag with no garment word put **a pleated drape on her**,
where the Brahmo drape is flat. The clause is "exactly the same plain white dhoti
and kurta as in @tag, with no change of any kind to any garment": the type, and
nothing more. Where the manner of wearing is the look, add that word alone:
unpleated, over both shoulders, sleeves rolled.

**A TAG CARRIES NO HELD OBJECT AND NO BENT ARM.** Chand, 2026-09-30, and it is the
ep09 beat 6 fault arriving through a reference instead of through silence. Point at
a frame where a man holds a letter and the model drops the letter and hangs his arms
down. **Every prompt restates every object in a hand and the angle of both arms**,
in or out of the crop.

**A TAG CARRIES NO EXPOSURE AND NO SUN POSITION EITHER.** ep11 beat 2 said
"maintaining absolute lighting continuity with @platform_1947" and came back
**52 percent brighter** than beat 1, measured on mean luma, 107 against 70. Beat 1's
prompt said "heavily underexposed" and beat 2's did not. Write the light out in full
in every beat. And once a frame has the sun visible in it, say where the sun is in
every beat that rolls off it, or a later speaking beat gets backlit.

**SILENCE ABOUT A CROWD EMPTIES THE ROOM.** ep11 beat 2 said the man was "the only
person visible in the frame" and the platform came back bare, which broke beat 3
where the line points at those people. The fix is ep05 beat 2's shipped wording:
put them in positively and **"every one of them seen from behind and held in heavy
soft focus"**, which is how a packed hall sat behind two leads with no face at risk.

**A FRAMING WORD ALONE STILL DOES NOT CHANGE THE SIZE.** ep11 beat 6 asked for
knees-upward and rendered full length. What works is beat 2's construction, adding
**"his face large in the frame and fully lit"** beside the framing word.

**AND A BACK VIEW IS NOTHING BUT HAIR.** Chand's catch. ep09 beat 1 rendered a bald
man from silence. Where a character is seen from behind, either attach a frame of
the back of their head or describe the hair in full, including the crown. Attaching
beats describing: `roy_1951_back.png` replaced sixty words. Point it at the hair and
the head only when the garment differs.

## After the clip

**A REGION MEASUREMENT CAN ANSWER THE WRONG QUESTION AND LOOK LIKE RIGOUR.** Three
times in ep11: a "head region" that was mostly sky, a corner crop that missed the
figure, an edge strip that was mostly ironwork. **A labelled frame strip settled each
one in a single look.** Frames first, numbers second, and say which pixels a number
came from.

**THE SPLICE TOLERANCE, MEASURED.** ep11 beat 6 had one mispronounced word cut out
mid-sentence, ten frames on a talking face. Claude called it a jump cut and wanted a
reroll; Chand said it would not read and was right. **Face region across the splice
differed by 9.83 of 255, against 4.70 for two normal frames 42 ms apart**, and the
head did not move at all. About twice a single frame step is invisible under music.
Measure this before spending credits on a mid-line trim.

Measure the thing you actually care about, not a proxy. Saturation is not hue.
Luma percentiles are not "does it look right". Four measurements in this
project have answered the wrong question. **When the question is whether it
looks good, the answer is Chand's eyes, and they have beaten the numbers every
time.**
