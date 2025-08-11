# Product Launch Tracker - n8n Workflow

An simple product/campaign discovery automation that monitors trending launches across ProductHunt, Indiegogo, and Kickstarter, delivering curated summaries directly to your Slack workspace.

## 🎯 Overview

This n8n workflow creates a simple product monitoring system that:

- **Multi-Platform Monitoring**: Tracks trending products across ProductHunt, Indiegogo, and Kickstarter
- **Smart Keyword Targeting**: Searches for specific product categories and technologies
- **Automated Scheduling**: Runs daily or on-demand for consistent market intelligence
- **Data Aggregation**: Merges results from multiple platforms into unified reports
- **Instant Notifications**: Delivers formatted summaries to designated Slack channels
- **Competitive Intelligence**: Identifies emerging trends and market opportunities

## 🏗️ Architecture

### Workflow Components

#### 1. Trigger System
- **Schedule Trigger**: Daily automated execution at configurable times
- **Manual Trigger**: On-demand workflow execution for immediate updates

#### 2. Keyword Search Engine
- **Target Keywords**: Configurable search terms (e.g., "AI agent", "Smart AI", custom terms)

#### 3. Data Extraction Pipeline
- **Airtop.ai**: Using Airtop node to scrape the contents from the provided URLs

#### 4. Aggregation & Processing
- **Result Merging**: Combines data from all platforms

#### 5. Notification System
- **Slack Integration**: Formatted messages to specified channels


## 🚀 Getting Started

### Prerequisites
- n8n installed and running
- API access and credentials for:
  - Airtop
  - Slack Bot Token
- Slack workspace with appropriate permissions

### Required Credentials
1. **Airtop API**:
   - Client ID and Client Secret
   - Access Token for API requests

2. **Slack Bot Token**:
   - Bot User OAuth Token
   - Channel permissions for posting messages


### Installation

1. **Import the Workflow**:
   ```bash
   # In n8n interface
   Workflows > Import from File > Select product-launch-tracker.json
   ```

2. **Configure Credentials**:
   - Add Product Hunt API credentials
   - Set up Slack Bot Token (Refer: https://youtu.be/qk5JH6ImK0I?si=aHAc0JEDQ1QujcRm to connect Slack to n8n)
   - Configure web scraping parameters

3. **Set Target Keywords**:
   ```json
   {
     "keywords": [
       "AI agent",
       "Smart AI",
       "automation tool",
       "productivity app"
     ]
   }
   ```

## 🤝 Contributing

Ways to enhance this workflow:
- **Duplicate Detection**: Removes redundant entries especially between Indiegogo and Kickstarter
- **Relevance Scoring**: Ranks products by keyword match and engagement
- **Summary Generation**: Open the URLs and creates a brief about the product or campaign including price
- **Slack blocks**: Use blocks to format the output in Slack 

## 📄 License

This workflow is provided under MIT License for commercial and personal use.

## 🆘 Support

- **Setup Issues**: Check n8n community forums for configuration help
- **API Problems**: Refer to platform-specific API documentation
- **Slack Integration**: Consult Slack API guides and bot setup
- **Feature Requests**: Submit via GitHub issues

---

**Ready to discover the next big thing?** 🚀 Import this workflow and never miss trending product launches again!