# The Legend of Kalyani — the prompts

Every generation prompt that made a 13-minute AI film, with what each one cost
and what went wrong.

**Watch the film first, it is the only thing here that matters:**
https://youtu.be/jvqy4QWOT5I

Thirteen vertical episodes assembled into one film. A Bengali legend about how a
city got its name, loosely after Dr B C Roy. Fictionalised: the city is real,
the people in it are invented.

## What is in here

**`RULES.md`** is the one to read. It is the working document the project used,
not a guide written afterwards. Every rule in it came from a clip that failed,
and the costs are left in, because "this cost 12 credits to learn" is what makes
a rule worth obeying.

A few things in it that took real money to find out:

- An unspecified person is drawn from the model's default, and that default is
  white. The fix that holds is not a sentence about where people are from, it is
  naming a garment only an Indian man wears.
- Naming a cuff *button* on a kurta made the model build a shirt and flip the
  garment mid-shot. Never name a thing you want absent, and check every clothing
  noun against what that garment actually has.
- A reference frame holding a person, attached to a shot of an object, plays the
  person first and then hard-cuts.
- Two character references in one clip can split a single line between two
  voices.
- A still costs nothing and a video does, so a composition gets tested free
  before it is paid for. But a still cannot show you motion, so write down what
  the test is blind to before you run it.

**`prompts/`** is the evidence: 132 prompts, one file per episode, each paired
with its length, its cost, how many takes it took, and a note on what actually
happened when it rendered.

## Why the failures are in here

Most published prompt collections are the ones that worked. The useful
information was in the ones that did not, and in the arguments about why. Both
are left in, including the places where the reasoning was confidently wrong and
had to be reversed later.

The honest summary of what the model got wrong most often: nothing. It did what
it was told. Almost every expensive failure in this project was something left
unsaid rather than something said wrong.

## What is not in here

The scripts, the Bengali dialogue, the edit and the assembly pipeline. This is
the generation craft only.

## Stack

Google Flow for generation and music, Gemini for dramatisation and prompt
drafting, ElevenLabs for narration and monologue, VN for the edit, Claude Code
for the pipeline and the record keeping.

Every creative decision was a human one.

## Licence

MIT. Take them, use them, change them. Attribution is appreciated and not
required.

The licence covers the prompts and the notes in this repository. The film is a
separate work and is not licensed here.
