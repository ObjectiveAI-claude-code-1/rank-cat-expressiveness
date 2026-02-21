# Rank Cat Expressiveness: Reading the Inner Life of Cats Through Pictures

## Purpose

The internet is saturated with cat pictures. They fill our feeds, our group chats, our saved folders. But not all cat pictures are created equal, and anyone who has ever scrolled past a hundred of them knows this intuitively. Some images stop you mid-scroll. A cat caught in the middle of an enormous yawn, its whole face contorted into a pink cavern of melodrama. A cat perched on a windowsill with its ears rotated backward, radiating an unmistakable irritation at something only it can perceive. A cat sprawled across a keyboard in a posture so thoroughly boneless that you can almost feel the weight of its contentment. These images communicate something. They have character. They reveal, in a single frozen moment, a glimpse of who this particular animal is and what it appears to be feeling right now.

Then there are the other pictures — the ones where a cat is simply present. It sits on a couch. It faces a wall. It exists in the frame the way a lamp exists in the frame. The cat is there, and that is all you can say about it.

The purpose of `rank-cat-expressiveness` is to distinguish between these two categories, and to do so with nuance across the entire spectrum between them. Given a cat picture, the function evaluates how much expressive character is visible in the image — how vividly the cat's pose, face, and body communicate something specific about its inner life in that moment. The function does not judge whether a cat is beautiful, whether the photograph is well-composed, or whether the breed is exotic. It asks a simpler and stranger question: *Is this cat telling us something?*

## Inputs

The function takes a single input: an image of a cat. This image might come from anywhere — a phone camera roll, a social media feed, a shelter adoption listing, a photographer's portfolio. The image might be high-resolution or blurry, carefully staged or hastily captured. What matters is not the technical quality of the photograph but what is visible within it: a cat, doing something, in some posture, with some expression.

The function's job is to look at that image and produce a score — a vector of values — that captures how expressively rich the picture is. This score is not a single thumbs-up or thumbs-down. It is a multi-dimensional reading that breaks expressiveness down into its constituent parts, so that the ranking it produces is grounded in specific, legible reasoning rather than a vague sense of "good" or "bad."

## Use Cases

The applications for this function are broader than they might first appear. The most obvious use is curation: given a large collection of cat pictures, surface the ones with the most character. This is valuable for social media accounts dedicated to cats, for shelter organizations trying to select the most compelling adoption photos, for anyone who has three hundred pictures of their cat on their phone and wants to find the ten worth sharing.

But the function also has a role in understanding what makes animal photography resonate with people. By breaking expressiveness into concrete dimensions, it offers a vocabulary for talking about why certain images land and others don't. It becomes a tool not just for sorting, but for seeing — for training our attention on the specific details that transform a picture of a cat into a portrait of a cat.

There is also a deeply practical use in content recommendation. Platforms that serve animal content could use expressiveness as a signal, prioritizing images that communicate something vivid over images that are merely competent. The result would be a feed that feels more alive, more particular, more worth looking at.

## The Three Qualities

To rank cat pictures by expressive character, the function must evaluate three fundamental qualities. Each represents a different dimension of what makes a cat picture feel alive and specific rather than generic and forgettable.

### 1. Facial Expressiveness

The face is where we look first, and it is where the most concentrated emotional information lives. A cat's face is a remarkably communicative instrument. The eyes alone carry enormous range: the slow blink of trust, the wide-open stare of alarm, the half-lidded squint of drowsy satisfaction, pupils blown wide with excitement or narrowed to slits in bright irritation. The ears are equally eloquent — pricked forward in curiosity, flattened sideways in annoyance, rotated backward to track a sound behind them, or relaxed into a soft neutral that signals calm. The mouth and whiskers complete the picture: whiskers fanned forward in engagement or pulled back against the cheeks, a mouth slightly open in a chirp or tightly closed in regal indifference.

This quality measures how much emotional or psychological information is legible in the cat's face. A cat with wide eyes, pinned ears, and forward whiskers is broadcasting on every channel at once. A cat whose face is turned away from the camera, obscured by shadow, or frozen in a perfectly neutral expression is giving us almost nothing to read. The highest-scoring images in this dimension are those where you could describe what the cat appears to be feeling just by looking at its face — surprise, annoyance, bliss, suspicion, absolute boredom — and the lowest-scoring are those where the face is either invisible or blank.

### 2. Body Posture and Physical Tension

A cat's body tells a story that the face alone cannot. The way a cat holds itself — the degree of tension or relaxation in its frame, the geometry of its limbs, the distribution of its weight — communicates an enormous amount about its state of being. Consider the difference between a cat sitting upright with its paws tucked neatly beneath it and a cat draped over the arm of a sofa like a piece of melting cheese. Both are at rest, but one is composed and the other has surrendered entirely to gravity. Consider the taut crouch of a cat about to pounce, every muscle coiled and ready, versus the stiff upright posture of a cat that has just been startled, its back arched and its tail puffed to twice its normal size.

This quality evaluates how much the cat's body contributes to the overall expressiveness of the image. A cat in a distinctive posture — the classic loaf, the full stretch, the belly-up sprawl of total vulnerability, the Halloween-cat arch of fear or play — scores high because the body itself is communicating. A cat sitting in a neutral, upright, unremarkable position scores low, because the posture tells us nothing about what is happening inside the animal. The key is whether the body looks like it belongs to this moment and this cat, or whether it could be a stock photo of any cat in any context.

### 3. Specificity of Moment

This is the quality that ties everything together and elevates it beyond a simple checklist of physical features. Specificity of moment asks: *Does this image capture something particular, or something generic?* It is the difference between a cat that happens to be sitting on a table and a cat that is clearly, unmistakably in the middle of something — knocking a glass off that table with deliberate eye contact, or crouched at the edge of it watching a bird with laser focus, or sitting on it with one paw raised mid-swat as though it has just been personally offended by an object.

A picture with high specificity of moment feels like it has a before and an after. You can imagine what just happened or what is about to happen. The cat is not merely existing in space; it is caught in the middle of an experience. You look at the image and you feel that you are seeing a specific instant in the life of a specific animal, not a generic representative of the species. This is what gives a cat picture its sense of personality — the feeling that this cat is an individual with its own particular way of being in the world, and that the photograph has captured a sliver of that individuality.

Images that score low on this dimension are the ones where the cat could be anywhere, doing anything, at any time. There is no narrative tension, no emotional specificity, no sense that something is happening. The cat is present but not revealed. Images that score high are the ones that make you laugh, or lean in, or say "that is exactly what my cat does" — because they have captured not just a cat, but a *moment*, and in that moment, a personality.

## Conclusion

The philosophy underlying `rank-cat-expressiveness` is that the best cat pictures are the ones that make you feel like you know the cat. They are portraits, not snapshots. They capture individuality, not mere presence. By evaluating facial expressiveness, body posture, and specificity of moment as three independent but interlocking dimensions, the function builds a rich, grounded understanding of what makes a cat picture resonate. It looks for the images where the cat is not just seen, but understood — where the photograph becomes a window into the small, vivid, deeply particular inner life of an animal that has no idea it is being watched, and is all the more itself because of it.