# AI Content Pipeline

An autonomous content creation and editing pipeline that routes human-created drafts through specialized AI agents for editing, fact-checking, and optimization while preserving the author's unique voice.

## Overview

This system acts as a "newsroom coordinator" that manages content through multiple editorial stages with quality gates and autonomous progression. Perfect for marketing teams, content creators, or anyone who wants to systematically improve their writing while maintaining their personal style.

## Key Features

- **Voice Preservation**: Maintains your individual writing style while applying brand guidelines
- **Autonomous Workflow**: Progresses through editing stages without manual intervention when quality gates are met
- **Multiple Content Types**: Supports blogs, whitepapers, case studies, social media, emails, and more
- **Quality Scoring**: Uses a comprehensive rubric to ensure content meets standards
- **Fact Verification**: Optional fact-checking stage with real source verification
- **Flexible Configuration**: Easily customizable for different industries and brands

## How It Works

1. **Coordinator**: Orchestrates the entire pipeline and tracks progress
2. **Editor**: Improves structure, clarity, and audience targeting
3. **Copy Editor**: Fixes grammar, style, and adds metadata
4. **SEO Specialist**: Optimizes for search while preserving voice
5. **Fact Checker**: Verifies claims with real, accessible sources (optional)

The system automatically advances between stages when quality thresholds are met, only stopping for user input when issues require human decision-making.

## Quick Start

### 1. Setup Your Configuration

Copy and customize these core files for your needs:

- `style_guide.md` - Your brand voice and writing guidelines
- `voice_guide.md` - Do's and don'ts for your content
- `rubric.yaml` - Quality scoring criteria
- `briefs/brief.json` - Content brief template

### 2. Create a Content Brief

```json
{
  "id": "my-article-2025",
  "content_type": "blog",
  "title_working": "Your Article Title",
  "audience": {
    "primary": "Your target readers",
    "stage": "Awareness/Consideration/Decision"
  },
  "angle": "Your unique perspective or hook",
  "wordcount_target": 1200,
  "keywords": {
    "primary": "main SEO keyword",
    "secondary": ["supporting", "keywords"]
  }
}
```

### 3. Run the Pipeline

The coordinator AI agent will:
1. Read your brief and style guides
2. Route your content through the appropriate agents
3. Score against the rubric at each stage
4. Provide autonomous progression or stop with specific feedback
5. Deliver polished, publish-ready content

## File Structure

```
src/
├── CLAUDE.md              # Main coordinator prompt
├── style_guide.md         # Brand writing guidelines
├── voice_guide.md         # Writing do's and don'ts  
├── rubric.yaml           # Quality scoring criteria
├── agents/               # Individual agent prompts
│   ├── editor.md
│   ├── copy.md
│   └── seo.md
├── briefs/              # Content brief templates
├── contracts/           # Task tracking templates
├── drafts/             # Work-in-progress files
├── reviews/            # Agent output files
└── final/              # Published content
```

## Content Types Supported

- **Blog Posts**: Full editorial pipeline with SEO optimization
- **Whitepapers**: Structure, citations, executive summaries
- **Case Studies**: Challenge/solution/results format
- **Social Media**: Character limits, hashtag optimization  
- **Email Campaigns**: Subject lines, preview text, CTAs
- **And more**: Easily configurable for new content types

## Customization Guide

### For Your Industry

1. **Update `style_guide.md`** with industry-specific terminology and guidelines
2. **Modify agent prompts** in the `agents/` folder for domain expertise
3. **Adjust `rubric.yaml`** scoring criteria for your content quality standards
4. **Create content type templates** in the brief format

### For Your Brand

1. **Brand Language**: Add your product names, company voice, and messaging guidelines to `style_guide.md`
2. **Voice Guidelines**: Customize `voice_guide.md` with your specific do's and don'ts
3. **Quality Standards**: Modify `rubric.yaml` thresholds and criteria for your standards
4. **Templates**: Create brief templates for your common content types

## Advanced Features

### Quality Gates
- Automatic scoring against 6 criteria (audience fit, thesis clarity, evidence, structure, SEO, style)
- Configurable passing thresholds
- Risk flag detection for security, legal, and accuracy issues

### Autonomous Progression  
- Advances automatically when quality standards are met
- Stops only when human input is required
- Tracks retry attempts to prevent infinite loops

### Voice Preservation
- Primary goal is maintaining the author's individual style
- Applies brand guidelines without sanitizing personal voice
- Rejects corporate-speak replacements of authentic language

## License

MIT License - feel free to customize and use for your content operations.

## Contributing

This is designed to be a starting point. Customize the agents, rubrics, and workflows for your specific needs. The system is most powerful when adapted to your unique content requirements and brand voice. This project was built with Claude Code in mind but should be adaptable for other systems.