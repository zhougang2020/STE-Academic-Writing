# Abstract Template B (Challenge → Insight → Contribution)

## Skeleton

1. [Task sentence]
2. [Challenge sentence]
3. To solve this, our key idea is [insight].
4. To this end, we propose [contribution].
5. [Benefit sentence]
6. Experiments show [main result].

## Example (Depth-aware diffusion)

1. In recent years, generative models have undergone significant advancement due to the success of diffusion models.
2. The success of these models is often attributed to their use of guidance techniques. However, these methods cannot guide a generated image to be aware of its geometric configuration, such as depth, which hinders application to areas that require depth awareness.
3. To address this limitation, we propose a novel guidance approach for diffusion models that uses estimated depth information derived from the rich intermediate representations of diffusion models.
4. We first present a label-efficient depth estimation framework using the internal representations of diffusion models. At the sampling phase, we utilize two guidance techniques to self-condition the generated image using the estimated depth map.
5. This approach enables depth-aware image generation without requiring explicit depth supervision.
6. Experiments show that our method achieves state-of-the-art performance on depth-conditioned image generation benchmarks.
