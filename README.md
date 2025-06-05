# Alert Lead Hunter - Production Ready

A comprehensive weather-based lead generation system that monitors weather alerts and automatically generates targeted leads for restoration and emergency services companies.

## 🌟 Features

### Weather Monitoring
- **Real-time weather alerts** from National Weather Service (NWS)
- **Multiple weather APIs** including OpenWeatherMap and WeatherAPI.com
- **Intelligent alert filtering** based on service areas and severity
- **Automated monitoring** with configurable intervals

### Lead Generation
- **Demographic-based targeting** using US Census data
- **Property data integration** for accurate lead qualification
- **Geographic targeting** within defined service areas
- **Lead scoring** based on weather impact and property characteristics

### Communication Campaigns
- **Email campaigns** via SendGrid integration
- **SMS campaigns** via Twilio integration
- **Automated follow-up** sequences
- **Campaign performance tracking**

### Desktop Application
- **Modern React interface** with real-time updates
- **Campaign management** dashboard
- **Lead tracking** and status management
- **Service area mapping** and configuration
- **Data export/import** capabilities

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Python 3.8+
- API keys for weather and communication services (see Configuration)

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd alert-lead-hunter-main
```

2. **Install frontend dependencies**
```bash
npm install
```

3. **Install Python dependencies**
```bash
cd python_scripts
pip install -r requirements.txt
```

4. **Configure API keys** (see Configuration section)

5. **Start the application**
```bash
# Start frontend development server
npm run dev

# In another terminal, start the Python backend
cd python_scripts
python alert_lead_hunter.py
```

## ⚙️ Configuration

### Required API Keys

#### Required APIs
- **OpenWeatherMap**: Get API key at [openweathermap.org](https://openweathermap.org/api)
- **WeatherAPI.com**: Get API key at [weatherapi.com](https://www.weatherapi.com/)
- **Google Geocoding**: Get API key at [Google Cloud Console](https://console.cloud.google.com/)
- **RapidAPI**: Get API key at [rapidapi.com](https://rapidapi.com/) for property data
- **SendGrid**: Get API key at [sendgrid.com](https://sendgrid.com/)
- **Twilio**: Get credentials at [twilio.com](https://www.twilio.com/)

#### Note on API Requirements
All API keys are required for full functionality. The application is designed for production use and requires valid API keys to operate properly.

### Environment Variables

Create a `.env` file in the `python_scripts` directory:

```env
# Weather APIs
OPENWEATHER_API_KEY=your_openweather_key
WEATHERAPI_KEY=your_weatherapi_key

# Lead Generation
GOOGLE_API_KEY=your_google_key
RAPIDAPI_KEY=your_rapidapi_key

# Communication
SENDGRID_API_KEY=your_sendgrid_key
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_token
TWILIO_PHONE_NUMBER=your_twilio_phone
```

## 🏗️ Building for Production

### Desktop Application (Electron)

1. **Build the React application**
```bash
npm run build
```

2. **Build Electron executable**
```bash
npm run build:electron
npm run dist
```

3. **Alternative: Use PowerShell script**
```powershell
.\build-exe.ps1
```

The executable will be created in the `dist-electron` directory.

### Python Backend

The Python backend can be deployed as:
- **Standalone script** on a server
- **Docker container** (Dockerfile included)
- **Cloud function** (AWS Lambda, Google Cloud Functions)
- **Scheduled service** (cron job, Windows Task Scheduler)

## 📊 Usage

### Setting Up Service Areas
1. Open the application
2. Navigate to "Service Areas"
3. Add your target geographic areas with radius
4. Configure weather alert types to monitor

### Configuring Campaigns
1. Go to "Campaign Manager"
2. Create campaigns for different weather events
3. Set target audience and messaging
4. Configure budget and duration

### Monitoring and Leads
1. The system automatically monitors weather alerts
2. Leads are generated based on weather events in service areas
3. View and manage leads in the "Leads" section
4. Track campaign performance in real-time

## 🔧 Development

### Frontend Development
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run test         # Run tests
npm run test:watch   # Run tests in watch mode
```

### Backend Development
```bash
cd python_scripts
python setup_and_test.py  # Test all APIs and configuration
python alert_lead_hunter.py  # Run the main orchestrator
```

### Technologies Used

#### Frontend
- **React 18** with TypeScript
- **Vite** for build tooling
- **Tailwind CSS** for styling
- **shadcn/ui** for components
- **Electron** for desktop packaging

#### Backend
- **Python 3.8+** with asyncio
- **Requests** for API calls
- **Pandas** for data processing
- **SendGrid** for email
- **Twilio** for SMS

## 📈 Performance

- **Real-time monitoring** with configurable intervals
- **Efficient API usage** with caching and rate limiting
- **Scalable architecture** supporting multiple service areas
- **Optimized lead scoring** algorithms

## 🔒 Security

- **API key encryption** and secure storage
- **Rate limiting** to prevent API abuse
- **Data validation** and sanitization
- **Secure communication** with HTTPS/TLS

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Support

For support, feature requests, or bug reports, please create an issue in the repository.

## 🚀 Deployment Options

### Option 1: Desktop Application
- Build Electron executable for Windows/Mac/Linux
- Distribute to end users for local installation
- Ideal for individual contractors or small businesses

### Option 2: Cloud Deployment
- Deploy Python backend to cloud services
- Host React frontend on CDN
- Ideal for SaaS offerings or enterprise deployments

### Option 3: Hybrid Deployment
- Desktop app for user interface
- Cloud backend for processing and data storage
- Best of both worlds for scalability and user experience
