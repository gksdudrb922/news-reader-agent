# News Reader Agent

An intelligent AI-powered news aggregation and analysis system built with CrewAI that automatically discovers, summarizes, and curates news articles on any given topic. The system uses multiple specialized AI agents working in collaboration to deliver comprehensive, multi-tier news briefings.

## 🚀 Features

- **Automated News Discovery**: Searches and collects recent news articles from credible sources
- **Intelligent Content Filtering**: Removes low-quality content, duplicates, and non-article pages
- **Multi-Tier Summarization**: Creates tweet-length, executive, and comprehensive summaries
- **Professional Curation**: Assembles publication-ready news briefings with editorial analysis
- **Source Credibility Scoring**: Evaluates and ranks news sources for reliability
- **Content Classification**: Categorizes articles by topic and relevance

## 🏗️ Architecture

The system employs a three-agent CrewAI architecture:

### 1. News Hunter Agent

- **Role**: Senior News Intelligence Specialist
- **Responsibilities**:
  - Discovers and collects relevant news articles
  - Filters out misinformation and low-quality content
  - Identifies credible sources and cross-references information
  - Applies intelligent filtering (removes articles <200 words, older than 48 hours)

### 2. Summarizer Agent

- **Role**: Expert News Analyst and Content Synthesizer
- **Responsibilities**:
  - Creates multi-tier summaries (tweet-length, executive, comprehensive)
  - Maintains journalistic objectivity and clarity
  - Provides context and implications analysis
  - Identifies patterns across multiple stories

### 3. Curator Agent

- **Role**: Senior News Editor and Editorial Curator
- **Responsibilities**:
  - Curates content into cohesive narratives
  - Creates publication-ready news briefings
  - Provides editorial analysis and context
  - Identifies key themes and future outlook

## 🛠️ Tools & Technologies

- **CrewAI**: Multi-agent orchestration framework
- **SerperDev**: News search and discovery
- **Playwright**: Web scraping with headless browser automation
- **BeautifulSoup**: HTML parsing and content extraction
- **OpenAI GPT-4**: Language model for analysis and summarization

## 📁 Project Structure

```text
news-reader-agent/
├── main.py                 # Main application entry point
├── tools.py               # Custom tools (search, scraping)
├── config/
│   ├── agents.yaml        # Agent configurations and roles
│   └── tasks.yaml         # Task definitions and workflows
├── output/                # Generated reports
│   ├── content_harvest.md # Raw article collection
│   ├── summary.md         # Multi-tier summaries
│   └── final_report.md    # Publication-ready briefing
├── pyproject.toml         # Project dependencies
└── README.md             # This file
```

## 🚀 Quick Start

### Prerequisites

- Python 3.13+
- OpenAI API key
- SerperDev API key

### Installation

- Clone the repository:

```bash
git clone <repository-url>
cd news-reader-agent
```

- Install dependencies using uv:

```bash
uv sync
```

- Set up environment variables:

```bash
# Create .env file
echo "OPENAI_API_KEY=your_openai_api_key" >> .env
echo "SERPER_API_KEY=your_serper_api_key" >> .env
```

### Usage

Run the news reader agent with a topic:

```bash
python main.py
```

The system will:

1. Search for recent news articles about the specified topic
2. Filter and collect credible articles
3. Generate multi-tier summaries
4. Create a professional news briefing
5. Save outputs to the `output/` directory

## 📊 Output Format

The system generates three types of reports:

### 1. Content Harvest (`content_harvest.md`)

- Raw collection of discovered articles
- Source metadata and credibility scores
- Filtering statistics and search queries used

### 2. Summary Report (`summary.md`)

- Multi-tier summaries for each article:
  - **Tweet-length** (≤280 characters)
  - **Executive Summary** (150-200 words)
  - **Comprehensive Summary** (500-700 words)
- Quality metrics and audience recommendations

### 3. Final Report (`final_report.md`)

- Publication-ready news briefing
- Editorial analysis and key themes
- Professional formatting with sections:
  - Executive Summary
  - Lead Story
  - Breaking News & Developments
  - Technology & Innovation
  - Editor's Analysis
  - Additional Reading

## ⚙️ Configuration

### Agent Configuration (`config/agents.yaml`)

- Define agent roles, goals, and backstories
- Configure LLM models and parameters
- Set verbose output and date injection

### Task Configuration (`config/tasks.yaml`)

- Define workflow steps and expected outputs
- Configure output file paths and formats
- Set task dependencies and agent assignments

## 🔧 Customization

### Adding New Tools

Extend the system by adding custom tools in `tools.py`:

```python
@tool
def custom_tool(parameter: str):
    """
    Tool description for the AI agent.
    """
    # Implementation here
    return result
```

### Modifying Agent Behavior

Update agent configurations in `config/agents.yaml` to change:

- Agent roles and expertise areas
- LLM models and parameters
- Tool assignments

### Customizing Output Format

Modify task configurations in `config/tasks.yaml` to:

- Change output file formats
- Adjust summary lengths and styles
- Add new analysis categories

## 📈 Example Output

The system successfully processes topics like "Cambodia Thailand War" and produces:

- **4 articles** collected from Reuters, NDTV, South China Morning Post, BBC News
- **Multi-tier summaries** with tweet-length, executive, and comprehensive formats
- **Professional briefing** with editorial analysis and future outlook
- **Source attribution** and credibility scoring

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

License information not specified. Please check with the project maintainers for licensing details.

## 🙏 Acknowledgments

- Built with [CrewAI](https://crewai.com/) for multi-agent orchestration
- Powered by [OpenAI](https://openai.com/) for language processing
- Uses [SerperDev](https://serper.dev/) for news search
- Web scraping with [Playwright](https://playwright.dev/)

## 📞 Support

For questions, issues, or contributions, please open an issue on the repository or contact the maintainers.
