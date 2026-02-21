# rank-cat-expressiveness

Ranks cat pictures by the expressive character visible in each image — surfacing the portraits that reveal personality and inner life, and ranking down the snapshots where a cat is merely present.

## How It Works

`rank-cat-expressiveness` is a **vector function**. Given an array of two or more cat images, it produces a probability distribution (a vector of values summing to 1) that ranks the images from most to least expressive. Higher values indicate images where the cat's face, body, and moment communicate something vivid and specific; lower values indicate images that are generic, neutral, or unrevealing.

The function decomposes expressiveness into three independent dimensions, each evaluated by a dedicated sub-function. The final ranking is a weighted combination of all three evaluations.

## Input

An array of cat images (minimum 2):

```json
{
  "type": "array",
  "minItems": 2,
  "items": {
    "type": "image",
    "description": "A cat picture to evaluate for expressive character."
  }
}
```

Images can come from any source — phone cameras, social media, shelter listings, professional photography. Technical quality does not matter; what matters is what the cat's face, body, and behavior communicate within the frame.

## Output

A vector of floating-point values, one per input image, summing to 1. Each value represents the image's relative expressiveness compared to the others in the set. For example, given 4 images, an output of `[0.45, 0.30, 0.15, 0.10]` means the first image is the most expressive and the last is the least.

## What It Evaluates

The function breaks expressive character into three qualities, each handled by its own sub-function:

### 1. Facial Expressiveness
**Sub-function:** [rank-cat-facial-expressiveness](https://github.com/ObjectiveAI-claude-code-1/rank-cat-facial-expressiveness)

Ranks images by the emotional and psychological information visible in the cat's face. Reads the eyes (wide-open alarm, half-lidded contentment, dilated pupils of excitement), ears (pricked forward in curiosity, flattened in annoyance, rotated backward in tracking), mouth (open mid-yawn, closed in regal indifference), and whiskers (fanned forward in engagement, pulled back flat). The key question: *could you confidently name what this cat is feeling just by looking at its face?* Images with legible, specific expressions rank high; images with blank, neutral, or hidden faces rank low.

### 2. Body Posture and Physical Tension
**Sub-function:** [cat-posture-expressiveness](https://github.com/ObjectiveAI-claude-code-1/cat-posture-expressiveness)

Scores each image individually for how much the cat's body communicates. Examines limb geometry, weight distribution, and the degree of tension or relaxation throughout the frame. Distinctive postures — the hunting crouch, the boneless furniture-drape, the startled Halloween arch, the perfectly tucked loaf, the belly-up sprawl of total vulnerability — score high because the body itself tells a story. Neutral, unremarkable sitting or standing positions score low because they could belong to any cat at any time.

### 3. Specificity of Moment
**Sub-function:** [rank-cat-moment-specificity](https://github.com/ObjectiveAI-claude-code-1/rank-cat-moment-specificity)

Ranks images by whether they capture a *particular* instant or a *generic* snapshot. Looks for narrative tension — a sense that something just happened or is about to happen. A cat mid-leap, a cat knocking something off a table with deliberate eye contact, a cat frozen in the act of stealing food — these are specific, unrepeatable moments that reveal an individual personality. Images where the cat could be anywhere, doing nothing in particular, at any point in time rank lowest.

## Use Cases

- **Photo curation**: Find the 10 best images out of hundreds on your camera roll — the ones with the most personality and character.
- **Shelter and adoption listings**: Select the most compelling, personality-rich photos to represent animals waiting for homes.
- **Social media and content**: Surface the cat pictures most likely to stop someone mid-scroll — the ones that communicate something vivid.
- **Content recommendation**: Prioritize expressive, character-rich images over generic ones when serving animal content in feeds or galleries.
- **Understanding resonance**: Use the three-dimensional breakdown to study *why* certain cat pictures resonate — which qualities (face, body, moment) contribute most to a picture's impact.

## Philosophy

The best cat pictures are portraits, not snapshots. They make you feel like you know the cat. They capture individuality, not mere presence. This function operationalizes that intuition by evaluating three concrete dimensions of expressiveness and combining them into a single ranking. It does not judge beauty, breed, or photographic technique. It asks only: *Is this cat telling us something?*