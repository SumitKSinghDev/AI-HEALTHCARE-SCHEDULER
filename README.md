# 🏥 AI Healthcare Scheduler - India

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/SumitKSinghDev/AI-HEALTHCARE-SCHEDULER)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg)](https://nodejs.org/)

> A comprehensive AI-powered healthcare appointment scheduling system designed specifically for Indian healthcare providers with multi-language support, intelligent features, and seamless payment integration.

## 🌟 Overview

The AI Healthcare Scheduler is a complete healthcare appointment management solution that combines artificial intelligence with modern web technologies to streamline the patient booking experience. Built with Indian healthcare needs in mind, it supports multiple languages, Indian payment systems, and local hospital networks.

### 🎯 Key Highlights
- **AI-Powered**: Intelligent symptom analysis, doctor recommendations, and smart scheduling
- **Indian Localized**: Hindi, Marathi, Tamil, Telugu, and 8+ Indian languages support
- **Payment Ready**: Razorpay integration for seamless Indian payments (₹)
- **Voice Enabled**: ElevenLabs voice synthesis for accessibility
- **Enterprise Features**: 2FA, encryption, analytics, and smart home integration
- **Mobile Optimized**: Responsive design for all devices

---

## 🚀 Features

### 📅 **Core Scheduling Features**
- **Smart Slot Suggestion** - AI recommends optimal appointment times based on doctor availability, patient history, and urgency
- **Real-Time Availability** - Live updates from multiple doctors, clinics, and departments
- **Multi-Doctor & Multi-Location Support** - Book across specialties and clinics in one place
- **Recurring Appointments** - Perfect for physiotherapy, dialysis, or regular check-ups
- **Group Appointments** - Family visits or multi-specialist consultations
- **Appointment Queue Management** - Digital queue system with wait-time predictions

### 🤖 **AI & Personalization**
- **AI Symptom Checker** - Enter symptoms, get doctor recommendations and urgency assessment
- **Smart Urgency Prioritization** - Emergency cases automatically get earlier slots
- **Predictive No-Show Prevention** - AI detects patterns and sends targeted reminders
- **Doctor Recommendation Engine** - Based on past visits, preferences, and ratings
- **Language Preference Matching** - Matches patients with doctors who speak their language
- **Intelligent Slot Scoring** - Advanced algorithms for optimal appointment scheduling

### 👥 **Patient Experience**
- **Voice & Chatbot Booking** - Book appointments using natural language
- **Auto Reminders** - SMS, WhatsApp, and email notifications with prep instructions
- **Pre-Visit Questionnaires** - Collect medical history before appointments
- **Digital Check-In** - QR code scanning to avoid queues
- **Wait-Time Prediction** - Real-time updates on expected delays
- **Online Payment Integration** - Razorpay support for advance payments and insurance
- **Mobile & Email Integration** - Complete contact management system
- **Appointment Slip Generation** - Professional medical documentation

### 🏥 **Doctor & Clinic Tools**
- **AI-Powered Calendar Management** - Auto-blocks time for surgeries, breaks, and follow-ups
- **Smart Rescheduling** - Automatic alternate slot suggestions for affected patients
- **Appointment Completion Workflow** - Add diagnosis, prescriptions, and follow-up dates
- **Integrated Telemedicine** - Video consultation links generated automatically
- **Analytics Dashboard** - Track appointment trends, cancellations, and demographics
- **Patient Profile Management** - Comprehensive medical history tracking
- **Reward Points System** - Patient loyalty program with attendance rewards

### 🔒 **Enterprise & Security Features**
- **Two-Factor Authentication (2FA)** - Secure access for doctors and patients
- **Encrypted Communication** - End-to-end secure messages and file sharing
- **Low-Bandwidth Mode** - Optimized for areas with poor internet connectivity
- **Smart Home Integration** - Alexa/Google Home appointment notifications
- **Attendance Rewards** - Points system for punctual patients
- **Advanced Analytics** - Comprehensive reporting and insights
- **Multi-Language Support** - English, Hindi, Marathi, Gujarati, Tamil, Telugu, Kannada, Malayalam, Bengali, Punjabi

### 🌐 **Indian Healthcare Integration**
- **Indian Hospital Network** - Apollo, Fortis, Max Healthcare, and more
- **Indian Insurance Support** - Star Health, HDFC ERGO, ICICI Lombard integration
- **Razorpay Payment Gateway** - Secure Indian payment processing
- **Indian Phone Number Format** - +91 mobile number validation
- **Regional Language Support** - Native language interfaces
- **Indian Currency (₹)** - All pricing in Indian Rupees

---

## 🛠 Technology Stack

| Component | Technology |
|-----------|------------|
| **Backend** | Node.js + Express.js |
| **Frontend** | HTML5, CSS3, JavaScript (Vanilla) |
| **AI Services** | OpenAI API, ElevenLabs |
| **Payment** | Razorpay SDK |
| **Database** | In-Memory (Production: MongoDB/PostgreSQL) |
| **Deployment** | Vercel, Heroku, Docker |
| **Security** | JWT, 2FA, AES Encryption |

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm or yarn
- API Keys (OpenAI, ElevenLabs, Razorpay)

### Installation

```bash
# Clone the repository
git clone https://github.com/SumitKSinghDev/AI-HEALTHCARE-SCHEDULER.git
cd AI-HEALTHCARE-SCHEDULER

# Install dependencies
npm install

# Set up environment variables
cp env.example .env
# Edit .env with your API keys

# Start the server
npm start
```

### Environment Variables

```env
OPENAI_API_KEY=your_openai_api_key
ELEVENLABS_API_KEY=your_elevenlabs_api_key
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_secret
NODE_ENV=production
PORT=3000
```

---

## 📱 Usage

### For Patients
1. **Book Appointment** - Select doctor, date, and time
2. **AI Symptom Check** - Get intelligent doctor recommendations
3. **Digital Check-in** - Scan QR code on arrival
4. **Receive Reminders** - SMS, WhatsApp, or email notifications
5. **Make Payments** - Secure online payments with Razorpay
6. **Earn Rewards** - Get points for attendance and punctuality

### For Doctors
1. **Manage Calendar** - AI-optimized scheduling
2. **Complete Appointments** - Add diagnosis and prescriptions
3. **Generate Slips** - Professional appointment documentation
4. **View Analytics** - Patient trends and clinic performance
5. **Smart Rescheduling** - Automatic patient notifications

### For Administrators
1. **Dashboard Analytics** - Comprehensive reporting
2. **User Management** - Doctor and patient profiles
3. **System Configuration** - Multi-language and clinic settings
4. **Payment Monitoring** - Transaction tracking and reports

---

## 🌍 Deployment

### Vercel (Recommended)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/SumitKSinghDev/AI-HEALTHCARE-SCHEDULER)

### Heroku
```bash
git push heroku main
```

### Docker
```bash
docker-compose up -d
```

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment instructions.

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **OpenAI** for intelligent AI capabilities
- **ElevenLabs** for natural voice synthesis
- **Razorpay** for secure payment processing
- **Indian Healthcare Community** for feedback and requirements

---

## 📞 Support

For support, email [sumitksingh243@gmail.com](mailto:sumitksingh243@gmail.com) or create an issue in this repository.

---

<div align="center">

### 🏥 Built with ❤️ for Indian Healthcare

**[Live Demo](https://your-app-name.vercel.app)** | **[Documentation](DEPLOYMENT.md)** | **[Issues](https://github.com/SumitKSinghDev/AI-HEALTHCARE-SCHEDULER/issues)**

</div>
