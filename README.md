AI Employee - Advanced Autonomous System 🤖
Your 24/7 Digital Business Assistant
This isn't your typical chatbot - it's a sophisticated autonomous agent built to manage business operations around the clock. Powered by Python backend logic and a sleek Next.js interface, this system acts as your digital workforce.
✨ Core Capabilities
1. 🔄 Dual-Mode Operation
The system intelligently operates across two environments for optimal security and automation:

☁️ Remote Mode: Continuous operation in cloud environment

Functions: Email monitoring, messaging platform oversight, social media management, financial tracking
Safety First: View-only access to sensitive data - requires explicit approval for any critical actions


💻 On-Premise Mode: Runs on your trusted local machine

Functions: Executes verified actions, handles authenticated operations, processes approved transactions



2. 🖥️ Modern Control Interface
Built with cutting-edge web technologies including Next.js, Framer Motion, and Shadcn UI:

Modular Control Panel: Granular management of monitoring services

Individual Toggles: Enable or disable specific monitoring modules independently
Use Case: Need a break? Disable WhatsApp monitoring while keeping email active


Real-Time Dashboard: Live status updates and system health monitoring
Adaptive Theming: Seamless light and dark mode experience
Fluid Interactions: Polished animations and intuitive user experience

3. 🏪 Business System Integration

ERP Connection: Direct integration with Odoo for comprehensive business management
Automated Reporting: Scheduled financial reviews and executive summaries delivered weekly


🛠️ Getting Started
What You'll Need

Node.js (version 18 or higher)
Python 3.10+
Docker (recommended for cloud deployment)
PM2 process manager (npm install -g pm2)

Setup Method 1: Local Installation
Perfect for development and full control over all components.

Configure Environment:
Duplicate .env.example as .env and add your API credentials.
Launch Backend Services:

powershell    # For Windows PowerShell users
    cd AI_Employee
    $env:AGENT_MODE="local"
    $env:HEADLESS="false" 
    pm2 start ecosystem.config.js
*Tip: Setting `HEADLESS="false"` opens browser windows for initial authentication (like WhatsApp QR scanning)*
3.  Start Web Interface:
bash    cd AI_Employee/web-ui
    npm install
    npm run dev
Open your browser to: `http://localhost:3000`
Setup Method 2: Cloud Deployment
Deploy to cloud infrastructure for uninterrupted operation.

Deploy with Docker:

bash    docker-compose up --build -d
The system automatically enters cloud mode with headless operation for stability.

🎯 Using the Control Center
Access the Services section in your dashboard to manage all monitoring components:
ComponentPurposeActionCore AgentMain processing engineStart/StopEmail MonitorScans inbox for priority messagesEnable/DisableMessaging MonitorWatches for urgent chat notificationsEnable/DisableSocial MonitorTracks professional network activityEnable/DisableTask CoordinatorHandles approval workflowsAlways Active
Pro Tip: Customize your monitoring based on availability - pause the core agent while keeping data collection active during off-hours.

📁 Architecture Overview
AI_Employee/
├── autonomous_agent.py   # Core processing logic
├── ecosystem.config.js   # Process management configuration
├── watchers/            # Monitoring modules (Email, Chat, Social)
├── mcp_servers/         # Integration layer (ERP, Email, Browser)
├── web-ui/              # Next.js dashboard
│   ├── app/             # Application pages
│   └── components/      # Reusable UI elements
└── Dockerfile           # Container configuration

🔐 Security & Permissions
All sensitive operations require manual approval. The system follows a zero-trust model where:

Read operations run automatically
Write operations queue for review
Financial actions need explicit authorization


💡 Quick Tips

Start with email monitoring only to familiarize yourself with the system
Review the approval queue regularly during initial setup
Customize notification thresholds based on your business needs
Use local mode for testing before deploying to cloud
