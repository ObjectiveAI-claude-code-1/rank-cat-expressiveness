# rank-cat-expressiveness

A vector function that ranks cat pictures by the expressive character visible in each image. Given a collection of cat photographs, it determines which images reveal the most about the cat's personality, inner state, and individual character — and which merely confirm that a cat was present.

## How It Works

`rank-cat-expressiveness` takes an array of cat images and produces a probability distribution over those images, assigning higher weight to pictures where the cat's expression, posture, and presence communicate something specific and alive. The function evaluates three independent dimensions of expressiveness, then combines them into a single ranking.

### Input

The function accepts an array of cat images (minimum 2). Each image should contain at least one cat. The images can be any breed, color, age, setting, or photographic quality — the function evaluates only what the cat's face and body are doing in the frame.

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

### Output

A probability distribution (array of numbers summing to 1) with one value per input image. Higher values indicate greater expressive character. The output can be used directly for ranking, sorting, or selection.

## What It Evaluates

The function decomposes expressive character into three qualities, each handled by a dedicated sub-function:

### 1. Facial Legibility — [`{{ .Task0 }}`](https://github.com/{{ .Owner }}/{{ .Task0 }})

Ranks images by how clearly the cat's face communicates an emotional or mental state. Examines eyes (wide with surprise, narrowed with suspicion, locked in focus, squeezed shut in bliss), ears (pricked forward in curiosity, flattened in annoyance, rotated back in alarm), mouth (open mid-meow, tongue visible), and whisker position. A face caught mid-expression ranks high. A face that is neutral, blank, or turned away ranks low. The key question: *looking only at this cat's face, could you describe what it appears to be feeling?*

### 2. Bodily Intention — [`{{ .Task1 }}`](https://github.com/{{ .Owner }}/{{ .Task1 }})

Ranks images by how much the cat's body posture communicates a specific action, state, or intention. Looks for postures with visible purpose: the rigid crouch before a pounce, the boneless sprawl of deep sleep, the puffed-up arch of alarm, the extended stretch of a mid-leap, the rhythmic kneading of paws. A body telling a clear story ranks high. A body sitting quietly in a standard, symmetrical pose ranks low. The key question: *looking only at this cat's body, could you describe what it is doing or about to do?*

### 3. Particularity — [`{{ .Task2 }}`](https://github.com/{{ .Owner }}/{{ .Task2 }})

Scores each image individually for how singular and unrepeatable the captured moment is. Evaluates whether the combination of expression, posture, and gesture belongs only to this specific cat in this specific instant, or whether any similar cat could be swapped in without anyone noticing. An image that resists substitution scores high. A generic, interchangeable snapshot scores low. The key question: *could only this cat have made this picture?*

## Use Cases

- **Social media curation**: Surface cat photos most likely to stop a viewer mid-scroll — not because the cat is beautiful or rare, but because its expression demands a reaction.
- **Pet adoption profiles**: Select the photo most likely to convey an animal's personality to a prospective owner, choosing the image where the cat looks like *someone* rather than *something*.
- **Photo culling**: Help photographers sifting through hundreds of shots from a session find the frames where the animal's character broke through.
- **Content ranking**: Prioritize cat images in any feed, gallery, or collection by the strength of personality visible in each frame.

## Philosophy

The function's guiding principle is **specificity over generality**. The best cat pictures refuse to be generic. They insist — through expression, posture, and individual character — that this is not just *a* cat but *this* cat, not just *a* moment but *this* moment. The function ranks images by how loudly and clearly the cat's own personality speaks through the frame.