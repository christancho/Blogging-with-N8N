# Blogging with N8N

A comprehensive AI-powered blogging automation system built with N8N that creates, optimizes, and publishes high-quality blog content automatically.

## Project Objective

This project demonstrates a complete automated blogging workflow that transforms a simple topic request into a fully published, SEO-optimized blog post. The system uses multiple specialized AI agents working in sequence to handle every aspect of content creation, from initial research to final publication on your Ghost CMS website.

## ⚠️ Important: Model Selection

**Use high token per minute (TPM) models for optimal performance.** The interactions between multiple AI agents will quickly surpass the 30k TPM limit of most standard models. We recommend starting with **ChatGPT 5-mini** which offers a 200k TPM limit, or other high-TPM models to ensure smooth workflow execution without rate limiting interruptions.

### Model Comparison Table

| Model | Token limits | Request and other limits | Batch queue limits |
|-------|--------------|-------------------------|-------------------|
| gpt-5 | 30,000 TPM | 500 RPM | 900,000 TPD |
| gpt-5-mini | 200,000 TPM | 500 RPM | 2,000,000 TPD |
| gpt-5-nano | 200,000 TPM | 500 RPM | 2,000,000 TPD |
| gpt-4.1 | 30,000 TPM | 500 RPM | 900,000 TPD |
| gpt-4.1-mini | 200,000 TPM | 500 RPM | 2,000,000 TPD |
| gpt-4.1-nano | 200,000 TPM | 500 RPM | 2,000,000 TPD |
| o3 | 30,000 TPM | 500 RPM | 90,000 TPD |
| o4-mini | 200,000 TPM | 500 RPM | 2,000,000 TPD |
| gpt-4o | 30,000 TPM | 500 RPM | 90,000 TPD |

**Key Abbreviations:**
- **TPM**: Tokens Per Minute
- **RPM**: Requests Per Minute  
- **TPD**: Tokens Per Day

### Anthropic Claude Models (Tier 1)

| Model | Maximum requests per minute (RPM) | Maximum input tokens per minute (ITPM) | Maximum output tokens per minute (OTPM) |
|-------|-----------------------------------|----------------------------------------|------------------------------------------|
| Claude Opus 4.x* | 50 | 30,000 | 8,000 |
| Claude Sonnet 4 | 50 | 30,000 | 8,000 |
| Claude Sonnet 3.7 | 50 | 20,000 | 8,000 |
| Claude Sonnet 3.5<br>2024-10-22 (deprecated) | 50 | 40,000† | 8,000 |
| Claude Sonnet 3.5<br>2024-06-20 (deprecated) | 50 | 40,000† | 8,000 |
| Claude Haiku 3.5 | 50 | 50,000† | 10,000 |
| Claude Opus 3 (deprecated) | 50 | 20,000† | 4,000 |
| Claude Haiku 3 | 50 | 50,000† | 10,000 |

**Notes:**
- *Claude Opus 4.x models are currently in limited access
- †These models have higher input token limits but are deprecated

## How It Works

The workflow orchestrates a team of AI agents, each specializing in a specific aspect of content creation. Starting with a user's topic request, the system automatically:
1. **Researches** the topic comprehensively
2. **Creates** a structured table of contents
3. **Generates** engaging, well-researched content
4. **Optimizes** for SEO and search visibility
5. **Edits** and polishes the content
6. **Publishes** directly to your Ghost CMS website

## Agent Roles & Responsibilities

### 🤖 Blog Content Orchestrator Agent
**The Project Manager** - Coordinates the entire workflow, manages data flow between agents, and ensures quality control at each stage. This agent handles user interactions, validates data, and manages approval gates before proceeding to publication.

### 🔍 Research Agent
**The Information Specialist** - Conducts comprehensive research using multiple sources including Brave Search, Brave News, and your existing blog content. Creates compelling table of contents, identifies content gaps, and provides research insights for content generation.

### ✍️ Content Generator Agent
**The Master Writer** - Transforms research insights and approved TOC into engaging, well-cited blog content. Researches each section individually, includes proper citations, and maintains consistent style throughout the article.

### 🎯 SEO Optimizer Agent
**The Search Expert** - Performs comprehensive SEO optimization including keyword research, on-page optimization, meta tag generation, and content enhancement recommendations. Ensures maximum search visibility and ranking potential.

### ✂️ Content Editor Agent
**The Quality Assurance Specialist** - Enhances content readability, verifies citations, improves flow, and ensures all links are functional. Creates professional HTML-formatted content ready for publication.

### 🚀 Blog HTML Publisher Agent
**The Publication Specialist** - Generates complete HTML documents with SEO meta tags, schema markup, and social media optimization. Automatically publishes content to your Ghost CMS website using the Ghost Publisher Tool.

## Agent Files

Each agent has its own configuration file with detailed system messages and prompts:

### Original Versions (Verbose)
- [Blog Orchestrator](Blog%20Orchestrator.md) - Main workflow coordinator
- [Researcher](Researcher.md) - Research and TOC creation agent
- [Content Generator](Content%20Generator.md) - Content creation agent
- [SEO Optimizer](SEO%20Optimizer.md) - SEO optimization agent
- [Content Editor](Content%20Editor.md) - Content editing and polishing agent
- [Publisher](Publisher.md) - Publication and Ghost CMS integration agent

### Simplified Versions (Recommended for Production)
- [Blog Orchestrator Simplified](Blog_Orchestrator_Simplified.md) - 61.8% size reduction (249→95 lines)
- [Researcher Simplified](Researcher_Simplified.md) - 59.1% size reduction (232→95 lines)
- [Content Generator Simplified](Content_Generator_Simplified.md) - 68.0% size reduction (297→95 lines)
- [SEO Optimizer Simplified](SEO_Optimizer_Simplified.md) - 73.5% size reduction (358→95 lines)
- [Content Editor Simplified](Content_Editor_Simplified.md) - 67.4% size reduction (291→95 lines)
- [Publisher Simplified](Publisher_Simplified.md) - 78.5% size reduction (442→95 lines)

**Note**: The simplified versions maintain 100% functionality while being significantly more efficient to read and process by AI agents. Each includes practical examples and clear workflow steps.

## Key Features

- **Fully Automated**: From topic to published post with minimal human intervention
- **AI-Powered**: Multiple specialized AI agents working in sequence
- **SEO Optimized**: Comprehensive search engine optimization at every stage
- **Ghost CMS Integration**: Direct publishing to your website
- **Quality Control**: Multiple approval gates and validation steps
- **Research-Driven**: Comprehensive research using multiple sources
- **Citation Management**: Proper source attribution and internal linking
- **Content Consistency**: Maintains brand voice and style throughout
- **Optimized Agent Performance**: Simplified agent configurations for faster processing

## Workflow Benefits

- **Time Savings**: Reduce content creation time from hours to minutes
- **Quality Consistency**: Maintain high standards across all content
- **SEO Performance**: Built-in optimization for better search rankings
- **Scalability**: Create multiple high-quality posts efficiently
- **Research Depth**: Comprehensive research using multiple sources
- **Professional Output**: Publication-ready content with proper formatting
- **Efficient Processing**: Simplified agents reduce processing time and token usage

## Getting Started

### 🚀 Quick Start with N8N Creator

**Ready to try it immediately?** Use the pre-built workflow on the N8N Creator platform:

**[Full Blog Content Automation with GPT-4, Claude & Ghost CMS Publisher](https://n8n.io/workflows/7920-full-blog-content-automation-with-gpt-4-claude-and-ghost-cms-publisher/)**

This ready-to-use template includes all the necessary nodes and configurations. Simply:
1. Click "Use for free" on the N8N Creator page
2. Configure your API credentials
3. Start creating automated blog content immediately!

### 📋 Manual Setup

For custom implementation or local N8N setup:

1. **Install N8N** on your system
2. **Import the workflow** from the JSON file
3. **Configure API credentials** for OpenAI, Anthropic, Brave Search, and Ghost CMS
4. **Set up your agents** with the provided system messages (recommend using simplified versions)
5. **Start the workflow** by requesting a blog topic

### Agent Setup Recommendation
For optimal performance, use the **simplified agent versions** which offer:
- 59-78% size reduction compared to original versions
- Faster processing and reduced token usage
- Maintained 100% functionality
- Clear examples and streamlined workflows
- Complete agent suite optimization (all 6 agents simplified)

## Requirements

- N8N instance
- OpenAI API key (for GPT models)
- Anthropic API key (for Claude models)
- Brave Search API key
- Ghost CMS admin API access
- Existing blog content for reference (optional but recommended)



## Workflow Structure

The system follows a 7-phase workflow:
1. **Topic Planning** - User input and requirements gathering
2. **Research & TOC** - Comprehensive research and outline creation
3. **Content Generation** - AI-powered content creation
4. **SEO Optimization** - Search engine optimization
5. **Content Editing** - Quality enhancement and polishing
6. **User Review** - Final approval before publication
7. **Publication** - Automatic posting to Ghost CMS

## License

MIT License - Feel free to use, modify, and distribute this project.

## Contributing

This project demonstrates advanced N8N workflow automation and AI agent orchestration. Contributions and improvements are welcome!
