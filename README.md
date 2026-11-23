# Blog Writing Crew

A multi-agent AI system built with CrewAI and Google Gemini. Four agents work in sequence to produce a polished blog post and social media content on any topic.

## Agents
- **Senior Research Analyst**: searches the web (Serper) and writes a structured research brief
- **Blog Content Writer**: drafts a markdown blog post from the brief
- **Blog Editor**: polishes the draft for clarity, grammar and flow
- **Social Media Content Strategist**: turns the final post into a Twitter/X thread and a LinkedIn post

## Setup
1. Install dependencies: `crewai install`
2. Create a `.env` file with:
   - `GEMINI_API_KEY=your_key`
   - `SERPER_API_KEY=your_key`
   - `MODEL=gemini/gemini-3.5-flash`
3. Create the output folder: `mkdir output`
4. Run: `crewai run` and enter a topic when prompted

## Output
- `output/blog_post.md`: the final blog post
- `output/social_posts.md`: Twitter/X thread and LinkedIn post

## Notes
- Agents and tasks are defined in `agents/*.jsonc` and `crew.jsonc`.
- The free Gemini tier has a daily request limit per model, so a full run may need a fresh model or no search tools.
- Built following the NextWork "Build a Blog Writing Crew with CrewAI" project.
