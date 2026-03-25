Automated Client Hunting Agent (Zero Budget)
I developed this n8n automation to act as a tireless, 24/7 scout for developers and digital agencies. This agent is specifically designed to hunt for high-value projects across global freelance platforms and local business listings, all while staying within the "Zero Budget" or free tiers of the tools used.

🔍 How It Works
This agent doesn't just scrape data; it qualifies leads and initiates contact. It runs automatically every 6 hours, scanning three distinct "hunting grounds" for opportunities.

1. Multi-Platform Lead Sourcing
I’ve integrated three major sources to ensure a steady stream of diverse projects:

Upwork: The agent fetches an RSS feed of the latest jobs based on specific keywords like WordPress, WooCommerce, and automation.

Fiverr: It scrapes public search results for high-demand services without requiring a paid API.

Google Maps (via Apify): I use this to find local businesses that either lack a website or have a weak digital presence, such as low ratings or few reviews.

2. Intelligent Qualification & Deduping
To prevent spamming and wasted effort, I built a custom processing layer:

Service Matching: A JavaScript engine analyzes job descriptions to match them against core service categories like UI/UX Design, AI Automation, or SEO.

Priority Scoring: Leads are ranked as High, Medium, or Low based on the detected budget and the density of relevant keywords.

Anti-Duplicate System: Before moving forward, the agent checks a Google Sheet to ensure the specific lead hasn't already been discovered or contacted.

3. AI-Powered Outreach
For every fresh lead found, the agent uses Gemini 2.5 Flash-Lite to write a personalized, human-sounding cold email.

It references the specific platform and project title.

It highlights the exact service that fits the client's need.

It maintains a strict "Max 5 sentences" rule to keep the outreach concise and professional.

4. Automated CRM & Alerts
Lead Logging: Every lead is automatically appended to a Google Sheet, including the platform, budget, matched service, and the generated outreach message.

Automatic Contact: If a lead has a contactable email, the agent sends the outreach immediately via Gmail.

Team Notifications: For High Priority leads, I’ve set up an alert system that sends a detailed HTML email to the team for instant follow-up.

🛠️ Tech Stack
Automation: n8n

AI (LLM): Gemini 2.5 Flash-Lite (Free Tier)

Scraping: Apify (Google Maps Scraper) & RSS

Database/CRM: Google Sheets

Communication: Gmail

📂 Setup & Configuration
Import the Workflow: Download the JSON file and import it into your n8n instance.

The Config Node: I’ve centralized all settings in a single Config node. You’ll need to input your:

Apify API Token.

Google Sheet ID.

Gemini API Key.

Target location/query for Google Maps.

Credentials: Connect your Google account for Sheets and Gmail using OAuth2 within n8n.

Google Sheet Setup: Create a sheet with a tab named Leads and include headers for tracking details like Lead ID, Platform, Title, Link, and Status.

💡 Why I Built This
Scaling a service-based business requires consistent lead generation, but manual hunting is a massive time sink. I built this to automate the "top of the funnel" tasks—searching, filtering, and initial outreach—allowing me to focus entirely on closing deals and delivering high-quality work.

Developed by Huzaifa Tariq – AI Engineer.
