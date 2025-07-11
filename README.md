# 🚢 Captain AI Bot

A comprehensive Telegram AI bot designed to help users achieve their goals, build positive habits, make better decisions, and maintain a healthy lifestyle through intelligent conversation and advanced tracking features.

## 🌟 Features

### 🎯 Advanced Goal Tracking
- **Smart Goal Management**: Create, track, and update goals with detailed attributes
- **Progress Logging**: Log progress updates with descriptions and percentages
- **AI-Powered Planning**: Get personalized action plans for your goals
- **Category Organization**: Organize goals by personal, professional, health, education, financial, social
- **Completion Tracking**: Track goal completion rates and success metrics

### 🏃 Habit Tracker
- **Daily Habit Tracking**: Mark habits as completed with notes and mood tracking
- **Streak Monitoring**: Track current and longest streaks for motivation
- **Weekly Progress**: View habit completion rates and trends
- **Category Support**: Organize habits by health, productivity, learning, social, mindfulness
- **Frequency Options**: Set habits as daily, weekly, or monthly

### 📝 Intelligent Journaling
- **Daily Journal Entries**: Add journal entries with mood tracking (1-5 scale)
- **AI Analysis**: Get insights and patterns from your journal entries
- **Tag System**: Organize entries with custom tags
- **Mood Trends**: Track emotional patterns over time
- **Weekly Summaries**: AI-generated weekly journal summaries

### 🤔 Decision Analysis
- **AI-Powered Analysis**: Get comprehensive decision analysis using Gemini AI
- **Option Comparison**: Compare different options with pros and cons
- **Risk Assessment**: Understand potential risks and benefits
- **Personalized Recommendations**: Get advice tailored to your situation
- **Decision History**: Track all your past decisions and outcomes

### 💪 Self-Assessment System
- **Weekly Assessments**: Rate mental state, productivity, and satisfaction
- **AI Feedback**: Get personalized feedback and improvement suggestions
- **Progress Tracking**: Monitor improvement over time
- **Trend Analysis**: Identify patterns in your well-being

### 💬 Natural Language Processing
- **Conversational AI**: Chat naturally without strict commands
- **Intent Recognition**: Understand user intentions automatically
- **Context Awareness**: Maintain conversation context per user
- **Life Coach Style**: Get personalized coaching and advice

### 📊 Smart Reporting
- **Weekly Reports**: Comprehensive weekly summaries of all activities
- **Monthly Analytics**: Detailed monthly progress reports
- **AI-Generated Insights**: Get intelligent analysis of your patterns
- **Progress Visualization**: See trends and improvements over time

### 🌐 Web Dashboard
- **Modern Interface**: Beautiful, responsive web dashboard
- **Real-time Data**: View all your data in one place
- **Quick Actions**: Perform common tasks directly from dashboard
- **Analytics**: Comprehensive charts and statistics
- **Mobile Friendly**: Works perfectly on all devices

### 🔔 Smart Notifications
- **Daily Reminders**: Get reminded of daily habits and goals
- **Weekly Reports**: Receive weekly progress summaries
- **Goal Reminders**: Stay on track with goal deadlines
- **Motivational Messages**: Get personalized motivation

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- MongoDB
- Telegram Bot Token
- Google Gemini API Key

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd captain
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp env.example .env
   ```
   
   Edit `.env` file with your configuration:
   ```env
   TELEGRAM_BOT_TOKEN=your_telegram_bot_token
   MONGODB_URI=mongodb://localhost:27017/captain
   GEMINI_API_KEY=your_gemini_api_key
   PORT=3000
   BASE_URL=http://localhost:3000
   ```

4. **Start the application**
   ```bash
   npm start
   ```

5. **Access the dashboard**
   - Web Dashboard: http://localhost:3000/dashboard
   - Health Check: http://localhost:3000/health

## 📱 Bot Commands

### 🎯 Goal Commands
- `/add_goal` - Add a new goal
- `/goal_status` - View all your goals
- `/update_goal` - Update goal details
- `/log_progress` - Log goal progress
- `/complete_goal` - Mark goal as completed

### 🏃 Habit Commands
- `/add_habit` - Add a new habit
- `/habit_status` - View today's habits
- `/mark_habit` - Mark habit as completed
- `/habit_progress` - View habit progress

### 📝 Journal Commands
- `/journal` - Add a journal entry
- `/journal_status` - View recent entries
- `/journal_search` - Search journal entries

### 🤔 Decision Commands
- `/decision_analysis` - Analyze a decision
- `/decisions` - View all decisions
- `/decision_status` - View decision details

### 💪 Assessment Commands
- `/assessment` - Take a self-assessment
- `/assessment_history` - View assessment history
- `/weekly_assessment` - Get weekly assessment

### 📊 Report Commands
- `/weekly_report` - Generate weekly report
- `/monthly_report` - Generate monthly report
- `/dashboard` - View web dashboard

### 💬 Conversation Commands
- `/motivation` - Get motivational support
- `/chat` - Start a conversation
- `/clear_context` - Clear conversation context

### ⚙️ Settings Commands
- `/settings` - View your settings
- `/help` - Show all commands

## 🗂️ Project Structure

```
captain/
├── src/
│   ├── models/           # MongoDB schemas
│   │   ├── User.js
│   │   ├── Goal.js
│   │   ├── Habit.js
│   │   ├── Journal.js
│   │   └── Decision.js
│   ├── services/         # Business logic
│   │   ├── geminiService.js
│   │   ├── goalService.js
│   │   ├── habitService.js
│   │   ├── journalService.js
│   │   ├── decisionService.js
│   │   ├── assessmentService.js
│   │   ├── reportService.js
│   │   ├── conversationService.js
│   │   ├── telegramBot.js
│   │   ├── database.js
│   │   ├── logger.js
│   │   └── cronJobs.js
│   ├── handlers/         # Message handlers
│   │   ├── commandHandler.js
│   │   └── messageHandler.js
│   ├── routes/           # API routes
│   │   └── dashboard.js
│   ├── public/           # Static files
│   │   └── dashboard.html
│   └── index.js          # Main application
├── package.json
├── README.md
└── .env
```

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `TELEGRAM_BOT_TOKEN` | Your Telegram bot token | Yes |
| `MONGODB_URI` | MongoDB connection string | Yes |
| `GEMINI_API_KEY` | Google Gemini API key | Yes |
| `PORT` | Server port (default: 3000) | No |
| `BASE_URL` | Base URL for dashboard links | No |
| `NODE_ENV` | Environment (development/production) | No |

### MongoDB Collections

The application creates the following collections:
- `users` - User profiles and preferences
- `goals` - Goal tracking data
- `habits` - Habit tracking data
- `journalentries` - Journal entries
- `decisions` - Decision analysis data
- `assessments` - Self-assessment data

## 🎨 Dashboard Features

### Overview Tab
- Quick statistics and progress summary
- Recent activities and achievements
- Quick action buttons

### Goals Tab
- List all goals with progress bars
- Add new goals
- Update goal progress
- View goal statistics

### Habits Tab
- Today's habits with completion status
- Mark habits as completed
- View habit streaks and trends
- Add new habits

### Journal Tab
- Recent journal entries
- Mood tracking visualization
- Add new entries
- Search and filter entries

### Decisions Tab
- Decision analysis history
- View past decisions and outcomes
- Add new decision analysis

### Analytics Tab
- Comprehensive charts and graphs
- Progress trends over time
- Performance metrics
- AI-generated insights

## 🤖 AI Integration

### Google Gemini AI
- **Goal Planning**: Generate personalized action plans
- **Decision Analysis**: Provide comprehensive decision analysis
- **Motivational Messages**: Create personalized motivation
- **Journal Insights**: Analyze patterns and provide insights
- **Conversation**: Natural language processing and responses
- **Weekly Reports**: Generate intelligent weekly summaries

### Natural Language Processing
- **Intent Recognition**: Understand user intentions
- **Context Awareness**: Maintain conversation context
- **Smart Responses**: Provide relevant and helpful responses
- **Command Extraction**: Extract information from natural language

## 📈 Analytics & Insights

### Goal Analytics
- Completion rates and trends
- Progress tracking over time
- Category-wise performance
- Success rate analysis

### Habit Analytics
- Streak tracking and visualization
- Completion rate trends
- Category performance
- Consistency metrics

### Journal Analytics
- Mood trend analysis
- Entry frequency patterns
- Tag usage statistics
- Emotional pattern recognition

### Decision Analytics
- Decision outcome tracking
- Analysis accuracy metrics
- Option comparison statistics
- Risk assessment accuracy

## 🔒 Security & Privacy

### Data Protection
- All data stored locally in MongoDB
- No sensitive data sent to external services
- User data isolation and privacy
- Secure API key management

### Authentication
- Telegram user authentication
- User session management
- Secure dashboard access
- API endpoint protection

## 🚀 Deployment

### Local Development
```bash
npm run dev
```

### Production Deployment
```bash
npm start
```

### Docker Deployment
```dockerfile
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue on GitHub
- Check the [FAQ](FAQ.md)
- Review the [documentation](DEPLOYMENT.md)

## 🔄 Changelog

See [CHANGELOG.md](CHANGELOG.md) for a complete list of changes and updates.

---

**Captain AI Bot** - Always Keep You on the Right Course! 🚢 
