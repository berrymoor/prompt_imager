# Prompt Imager

## Overview

**Prompt Imager** is a powerful utility that transforms complex JSON prompts into structured, visually optimized images. This tool is designed for content creators, video producers, and AI model operators who need to convert detailed text-based instructions into portable reference images suitable for use with modern generative AI systems.

## Purpose

When working with advanced generative models like **Nano Banana**, **GPT Image**, **Veo 3.1**, **Seedance 2**, and **Grok Imagine**, long and complex prompts often lose clarity or exceed token limits. Prompt Imager solves this by:

- **Structuring** complex JSON data into human-readable hierarchical text format
- **Visualizing** the structured content as high-resolution images
- **Optimizing** font sizing and layout to ensure all content is clearly readable
- **Exporting** as portable PNG files for seamless integration with AI systems

## Key Features

### JSON to Structured Text Conversion
- Automatic JSON parsing with intelligent formatting
- Hierarchical structure visualization with consistent indentation
- Graceful handling of arrays, nested objects, and primitive values
- Fallback to plain text mode if input is not valid JSON

### Intelligent Canvas Rendering
- **Dynamic font scaling**: Automatically adjusts font size to fit all content within the canvas
- **Vertical centering**: Content is centered for optimal visual presentation
- **Responsive padding**: Scales relative to canvas dimensions
- **Binary search optimization**: Finds the largest readable font size efficiently

### Flexible Export Options
- Multiple aspect ratio presets:
  - **9:16** (Portrait/Mobile)
  - **1:1** (Square/Social Media)
  - **16:9** (Landscape/Widescreen)
- High-resolution output at 1920px base dimension
- One-click PNG download
- Metadata display (compression ratio, input type, font metrics)

## Usage Example

### Basic Workflow

1. **Prepare Your Prompt**
   - Structure your instructions as JSON for maximum clarity:
   ```json
   {
     "subject": "futuristic cityscape",
     "style": {
       "art_direction": "cyberpunk aesthetic",
       "color_palette": ["neon blue", "electric pink", "deep purple"],
       "lighting": "dramatic backlighting"
     },
     "technical_specs": {
       "resolution": "4K",
       "aspect_ratio": "16:9",
       "motion": "subtle camera pan"
     },
     "reference_instruction": "Use text from reference image as guide for generation"
   }
   ```

2. **Paste into Prompt Imager**
   - Open the web interface
   - Paste your JSON into the textarea
   - Select desired aspect ratio

3. **Generate**
   - Click "Generate Image"
   - Review the structured output
   - Verify readability at target display size

4. **Download & Use**
   - Click "Download PNG"
   - Attach the image to your AI model input
   - Use the reference instruction: *"Use text from reference image as guide for generation"*

### Reference Integration Pattern

When submitting to generative models, combine the downloaded image with clear instructions:

```
Reference Image: [Attach PNG from Prompt Imager]
Instruction: "Use text from reference image as guide for generation. Prioritize all structural and stylistic specifications shown in the image."
```

This approach ensures consistent adherence to detailed specifications across multiple generation runs.

## Technical Specifications

### Canvas Rendering Engine
- **Resolution**: Up to 1920px × 1920px (scales with aspect ratio)
- **Font**: System monospace fonts (SF Mono, Cascadia Code, Fira Code, Consolas)
- **Font Weight**: 600 (Semi-bold for enhanced readability)
- **Line Height**: 1.2x font size
- **Color Scheme**: Black text (#1a1a1a) on white background (#ffffff)

### Performance
- Real-time font size optimization using binary search algorithm
- Intelligent line wrapping while preserving indentation structure
- Responsive UI with minimal latency

## Browser Compatibility

- Modern browsers with HTML5 Canvas support
- Desktop and mobile-optimized interface
- Graceful fallback for environments with disabled download attributes

## File Structure

```
├── index.html          # Single-file web application
├── README.md          # This documentation
└── .git/              # Version control
```

## Getting Started

1. Clone or download the repository
2. Open `index.html` directly in a web browser (no server required)
3. Paste your JSON prompt
4. Select output format
5. Generate and download

## Use Cases

✓ **AI Video Generation**: Prepare detailed motion and cinematography briefs  
✓ **Image Synthesis**: Document complex visual requirements with metadata  
✓ **Model Fine-tuning**: Create structured reference assets  
✓ **Prompt Documentation**: Archive and version control instruction sets  
✓ **Team Collaboration**: Share visual specifications across production teams  

## Advantages Over Plain Text

| Aspect | Plain Text | Prompt Imager |
|--------|-----------|-----------------|
| Clarity | Ambiguous indentation | Structurally explicit |
| Portability | Requires copy-paste | Single portable image |
| Model Integration | Direct input | Reference-guided generation |
| Visual Hierarchy | Limited | Clear visual structure |
| File Sharing | Text format | Standard PNG format |

## Future Enhancements

- [ ] Multi-color syntax highlighting for different data types
- [ ] Custom theme/branding options
- [ ] Batch processing for multiple prompts
- [ ] Integration with popular AI platforms
- [ ] Prompt template library

## License

Open source. Feel free to use, modify, and distribute.

## Support

For issues, suggestions, or contributions, please open an issue in the repository.