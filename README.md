# rank-cat-expressiveness

Ranks a collection of cat pictures by the expressive character visible in each image. Not by photographic quality, not by cuteness, not by breed — by how much a single picture reveals about who a particular cat is in a particular moment.

A blurry snapshot of a cat mid-sneeze, caught in outraged bewilderment, outranks a studio-lit portrait of a cat sitting politely on a cushion. The key distinction is **specificity versus generality**: an image that communicates something particular about a cat's inner life ranks above an image that merely confirms a cat was present.

## Input

An array of **2 or more cat images**. Each image should contain at least one cat. The images can come from any source — personal photo libraries, social media feeds, shelter adoption galleries, or any other collection that needs sorting by expressiveness.

```
[image, image, image, ...]
```

## Output

A **normalized vector of scores** (one per input image, summing to 1) representing each image's relative expressive character. Higher scores indicate images with more expressive, characterful cats; lower scores indicate generic or neutral poses.

```
[0.45, 0.35, 0.12, 0.08]
```

## What It Evaluates

The function decomposes expressive character into three qualities, each handled by a dedicated sub-function:

### 1. Facial Expressiveness
**[cat-face-expressiveness-ranker](https://github.com/ObjectiveAI-claude-code-1/cat-face-expressiveness-ranker)**

Reads the cat's face for signs of active emotional expression. Examines the eyes for states like relaxation, focus, excitement, or affection — from slow half-lidded blinks to wide dilated stares. Reads the ears for signals: forward-pricked curiosity, sideways-flattened irritation ("airplane ears"), or fully pinned-back alarm. Notes whether the mouth and whiskers add expressiveness — a mid-yawn, a mid-meow, or whiskers fanned forward in engagement. The central question: is the face actively transmitting an inner state, or is it simply present?

**Ranks high:** A cat with pupils dilated in excitement, ears pinned back in annoyance, or eyes squeezed shut in blissful contentment.
**Ranks low:** A cat with a neutral, closed expression — the generic resting face of a cat that is neither engaged nor bothered.

### 2. Body Posture and Physical Tension
**[cat-body-language-intensity](https://github.com/ObjectiveAI-claude-code-1/cat-body-language-intensity)**

Reads the cat's body for the physical story it tells. Assesses the degree of tension or relaxation visible in the posture — from the rigid arch and puffed tail of a startled cat, to the boneless sprawl of one draped across furniture in complete surrender, to the coiled crouch of a cat about to pounce. Evaluates whether the posture is dynamic and communicative, or static and default.

**Ranks high:** A cat caught mid-leap, theatrically flopped in a doorway, or loafing with the deliberate composure of a cat who has chosen serenity.
**Ranks low:** A cat sitting upright in a generic position that any cat might hold at any time without particular intention.

### 3. Specificity of Individual Character
**[cat-idiosyncrasy-score](https://github.com/ObjectiveAI-claude-code-1/cat-idiosyncrasy-score)**

Assesses whether the image captures something particular to *this* cat in *this* moment. Looks for idiosyncrasy — a pose so peculiar, an expression so loaded with apparent intention, that a viewer would instinctively narrate it: *"This cat is judging me,"* or *"This cat has never been more offended."* This is the quality that separates a memorable cat picture from a merely competent one.

**Scores high:** A cat wedged impossibly into a box far too small, one paw extended in defiance of physics — an image that could not belong to just any cat.
**Scores low:** A pleasant but anonymous image that tells you nothing about who that particular cat is.

## Use Cases

- **Social media platforms** — Select the most engaging thumbnail from a gallery of pet photos
- **Animal shelters** — Choose adoption profile pictures that best showcase each cat's personality, because a photo of a cat gazing imperiously from a high shelf tells a potential adopter far more than a photo of a cat curled in a generic ball
- **Personal photo libraries** — Surface highlight images from thousands of near-identical shots
- **Content curation** — Filter large volumes of cat content to find the images with the most character and personality
- **Pet photography** — Identify the strongest shots from a session based on expressive impact rather than technical quality

## Philosophy

The best pictures of animals are the ones that make us feel, however briefly, as though we understand what the animal is experiencing. This function reads the visual language of posture, expression, and individuality, and ranks images by how much of that language is present. The images that say the most, rank the highest.