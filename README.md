# rank-cat-visual-harmony

A sophisticated ObjectiveAI Vector Function that evaluates and ranks cat photographs based on visual harmony, balance, and compositional excellence.

## Overview

`rank-cat-visual-harmony` transforms the subjective art of evaluating photographic quality into a measurable, reproducible assessment framework. This function employs an ensemble of language models to evaluate which cat photographs best demonstrate visual harmony—that elusive quality where every compositional element works together intentionally to create a unified, compelling image.

## Input

The function accepts an array of cat photo objects:

```json
[
  {
    "url": "https://example.com/photo1.jpg",
    "title": "Sleeping Black Cat",
    "photographer": "Jane Smith"
  },
  {
    "url": "https://example.com/photo2.jpg"
  }
]
```

**Required:**
- `url` (string): The URL or file path to the cat photograph image

**Optional:**
- `title` (string): A descriptive title or label for the photograph
- `photographer` (string): Credit or attribution to the photographer

**Constraints:** Minimum 2 photos, maximum 100 photos per request.

## Output

An array of probability scores (one per input photo) representing how strongly each photo demonstrates visual harmony. Scores normalize to approximately 1.0, enabling direct comparison and ranking.

```json
[0.35, 0.28, 0.22, 0.15]
```

## Four Dimensions of Evaluation

### 1. Visual Balance and Spatial Distribution
Evaluates whether visual weight is distributed evenly and intentionally. Assesses symmetrical vs. asymmetrical balance, negative space usage, and the spatial relationship between subject and surroundings.

### 2. Color and Tone Unity
Analyzes the photograph's color palette and tonal range. Evaluates color harmony, whether colors complement the cat's natural coloring, and the overall emotional coherence of the image.

### 3. Compositional Flow and Visual Rhythm
Examines how the viewer's eye naturally moves through the image. Looks for leading lines, repeating shapes, visual hierarchy, and whether the eye follows a logical journey rather than bouncing randomly.

### 4. Overall Coherence and Unified Vision
Assesses whether all elements work together as a cohesive whole reflecting a singular artistic vision, where each compositional choice serves the overall image intentionally.

## Use Cases

**Photography Curation:** Museums, galleries, and publications can identify visually harmonious photos for cohesive collections.

**Social Media:** Platforms can surface the most visually striking cat content to improve user engagement.

**Photography Education:** Students and educators can learn which images achieve visual harmony and why.

**Photographer Development:** Individual photographers can evaluate their work and identify compositionally excellent images for their portfolios.

**Commercial Applications:** Pet businesses, e-commerce sites, and adoption agencies can select compelling photos for marketing materials.

## How It Works

The function employs Vector Completion with four specialized evaluation tasks:

1. Each task prompts an ensemble of language models with the same set of cat photographs
2. The task asks which photo best demonstrates a specific dimension of visual harmony
3. Models assess photographs independently and their evaluations are aggregated
4. Probability scores are generated for each photo across each dimension
5. Final rankings combine results from all four evaluations

This ensemble approach leverages collective aesthetic judgment, reducing individual bias and producing robust, reproducible rankings.

## Philosophy

The rank-cat-visual-harmony function is founded on the principle that photographic excellence emerges from measurable compositional principles. When colors harmonize, balance creates stability, the viewer's eye flows naturally, and all elements serve a coherent vision—the result is a photograph that genuinely resonates.

This function celebrates those moments where technique, vision, and subject align perfectly, enabling photographers, curators, and enthusiasts to discover, learn from, and appreciate the finest examples of cat photography.

## Technical Details

- **Function Type:** Vector Completion
- **Evaluation Tasks:** 4 specialized compositional assessments
- **Input Format:** JSON array of photo objects
- **Output Format:** Array of probability scores (sum ≈ 1.0)
- **Assessment Method:** Ensemble LLM evaluation across visual harmony dimensions