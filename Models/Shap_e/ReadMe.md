
```markdown
# Shap-E: Generating Conditional 3D Implicit Functions

This repository provides the official code and model release for **Shap-E**, a model for generating 3D objects conditioned on text or images.

**Original Repository**: [https://github.com/openai/shap-e](https://github.com/openai/shap-e)

## Overview

Shap-E allows for the generation of 3D objects based on text prompts or image inputs, enabling the creation of various creative 3D shapes like:
- A chair that looks like an avocado
- An airplane that looks like a banana
- A birthday cupcake
- Ube ice cream cone
- A penguin

These are just examples of what the model can create based on given prompts.

## Installation

To install Shap-E, clone the repository and install it in editable mode with pip:

```bash
git clone https://github.com/openai/shap-e.git
cd shap-e
pip install -e .
```

### Requirements

- Python 3.x
- Blender (version 3.3.1 or higher) - Required only if using the `encode_model.ipynb` notebook

Set the `BLENDER_PATH` environment variable to the path of the Blender executable if using the encoding functionality.

## Usage

The repository includes several Jupyter Notebooks to get you started:

1. **Text-to-3D Model** (`sample_text_to_3d.ipynb`): Sample a 3D model conditioned on a text prompt.

2. **Image-to-3D Model** (`sample_image_to_3d.ipynb`): Sample a 3D model conditioned on a synthetic view image. For optimal results, it's recommended to remove the background from the input image.

3. **Encode Model** (`encode_model.ipynb`): Load a 3D model or a mesh (trimesh), generate multiview renders and a point cloud, encode them into a latent, and render it back. This notebook requires Blender, and the `BLENDER_PATH` environment variable should be set.

## Resources

- **Repository**: [OpenAI Shap-E on GitHub](https://github.com/openai/shap-e)
- **License**: MIT License

## Contributors

The project has been contributed to by the following users:
- @unixpickle
- @heewooj
- @bitsnaps
- @chand1012
- @mattdeitke
- @onpix
- @mertyyanik
- @ahmadmustafaanis

## License

Shap-E is released under the MIT License.

---

For additional information, refer to the [README](https://github.com/openai/shap-e) on the official GitHub repository.
