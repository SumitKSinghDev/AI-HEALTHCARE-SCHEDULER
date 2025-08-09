# 🚀 AI Healthcare Scheduler - Deployment Guide

## 🏥 Overview
This comprehensive guide covers deploying the AI Healthcare Scheduler across multiple platforms including Docker, Heroku, Vercel, and cloud providers.

## 📋 Prerequisites

### Required API Keys
- **OpenAI API Key**: For AI symptom analysis and medical recommendations
- **ElevenLabs API Key**: For voice synthesis features
- **Razorpay Keys** (Optional): For payment processing in India

### System Requirements
- Node.js 18+ 
- npm or yarn
- Docker (for containerized deployment)
- Git

## 🐳 Docker Deployment (Recommended)

### Quick Start
```bash
# Clone the repository
git clone <your-repo-url>
cd ai-healthcare-scheduler

# Create environment file
cp env.example .env
# Edit .env with your API keys

# Build and run with Docker Compose
docker-compose up -d

# Access at http://localhost:3000
```

### Manual Docker Build
```bash
# Build the image
docker build -t ai-healthcare-scheduler .

# Run the container
docker run -d \
  -p 3000:3000 \
  -e OPENAI_API_KEY=your_openai_key \
  -e ELEVENLABS_API_KEY=your_elevenlabs_key \
  -e RAZORPAY_KEY_ID=your_razorpay_key \
  -e RAZORPAY_KEY_SECRET=your_razorpay_secret \
  --name healthcare-scheduler \
  ai-healthcare-scheduler
```

## 🔴 Heroku Deployment

### One-Click Deploy
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

### Manual Deployment
```bash
# Install Heroku CLI
# Login to Heroku
heroku login

# Create new app
heroku create your-app-name

# Set environment variables
heroku config:set OPENAI_API_KEY=your_key
heroku config:set ELEVENLABS_API_KEY=your_key
heroku config:set RAZORPAY_KEY_ID=your_key
heroku config:set RAZORPAY_KEY_SECRET=your_secret

# Deploy
git push heroku main

# Open the app
heroku open
```

## ⚡ Vercel Deployment

### Quick Deploy
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Set environment variables in Vercel dashboard
# Or use CLI:
vercel env add OPENAI_API_KEY
vercel env add ELEVENLABS_API_KEY
vercel env add RAZORPAY_KEY_ID
vercel env add RAZORPAY_KEY_SECRET
```

### GitHub Integration
1. Push code to GitHub
2. Connect repository to Vercel
3. Add environment variables in dashboard
4. Deploy automatically on push

## ☁️ Cloud Platform Deployment

### AWS EC2
```bash
# Launch EC2 instance (Ubuntu 22.04)
# Install Node.js and Docker
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

# Clone and deploy
git clone <your-repo>
cd ai-healthcare-scheduler
sudo docker-compose up -d

# Configure security group for port 3000
```

### Google Cloud Platform
```bash
# Using Cloud Run
gcloud run deploy healthcare-scheduler \
  --source . \
  --platform managed \
  --region asia-south1 \
  --allow-unauthenticated \
  --set-env-vars OPENAI_API_KEY=your_key
```

### Azure Container Instances
```bash
# Create resource group
az group create --name healthcare-rg --location eastasia

# Deploy container
az container create \
  --resource-group healthcare-rg \
  --name healthcare-scheduler \
  --image your-registry/ai-healthcare-scheduler \
  --ports 3000 \
  --environment-variables OPENAI_API_KEY=your_key
```

## 🔧 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `OPENAI_API_KEY` | ✅ Yes | OpenAI API key for AI features |
| `ELEVENLABS_API_KEY` | ✅ Yes | ElevenLabs API key for voice |
| `RAZORPAY_KEY_ID` | ❌ No | Razorpay key for payments |
| `RAZORPAY_KEY_SECRET` | ❌ No | Razorpay secret for payments |
| `NODE_ENV` | ❌ No | Set to 'production' |
| `PORT` | ❌ No | Server port (default: 3000) |

## 🏥 Indian Healthcare Compliance

### Data Localization
- Deploy in Indian data centers (Mumbai, Chennai)
- Use AWS Asia Pacific (Mumbai) region
- Ensure data residency compliance

### Payment Integration
- Razorpay is integrated for Indian payments
- Supports UPI, Cards, Net Banking
- INR currency support

### Language Support
- Hindi, Marathi, Gujarati, Tamil, Telugu
- Regional hospital data included
- Indian phone number formats

## 🔒 Security Considerations

### Production Checklist
- [ ] Use HTTPS/SSL certificates
- [ ] Set secure environment variables
- [ ] Enable CORS for specific domains
- [ ] Implement rate limiting
- [ ] Add authentication for admin features
- [ ] Regular security updates

### API Key Security
```bash
# Never commit API keys to git
echo ".env" >> .gitignore
echo "*.key" >> .gitignore

# Use secret management services
# AWS Secrets Manager, Azure Key Vault, etc.
```

## 📊 Monitoring & Logging

### Health Checks
- Endpoint: `/health`
- Returns system status and API connectivity
- Use for load balancer health checks

### Logging
```javascript
// Application logs available at:
// - Console output
// - /logs directory (if mounted)
// - Cloud platform logging services
```

## 🚀 Performance Optimization

### Production Settings
```bash
# Set NODE_ENV to production
NODE_ENV=production

# Enable gzip compression
# Configure CDN for static assets
# Use Redis for session storage (future)
```

### Scaling
- Use container orchestration (Kubernetes)
- Implement horizontal pod autoscaling
- Add Redis for shared state
- Use PostgreSQL for persistent data

## 🔧 Troubleshooting

### Common Issues
1. **Port already in use**: Change PORT environment variable
2. **API key errors**: Verify keys are correctly set
3. **CORS errors**: Check allowed origins
4. **Memory issues**: Increase container memory limits

### Debug Commands
```bash
# Check container logs
docker logs healthcare-scheduler

# Check environment variables
docker exec healthcare-scheduler env

# Test API endpoints
curl http://localhost:3000/health
```

## 📱 Mobile & PWA

### Progressive Web App
- Service worker enabled
- Offline functionality
- App-like experience on mobile
- Push notifications ready

## 🌐 Multi-Region Deployment

### Global Load Balancing
```bash
# Deploy to multiple regions
# Use CloudFlare or AWS CloudFront
# Implement geo-routing for Indian users
```

## 📞 Support & Maintenance

### Updates
```bash
# Pull latest changes
git pull origin main

# Rebuild and redeploy
docker-compose down
docker-compose up -d --build
```

### Backup Strategy
- Export appointment data regularly
- Backup environment configurations
- Document custom modifications

---

## 🎉 Quick Deploy Commands

### Docker (Fastest)
```bash
git clone <repo> && cd ai-healthcare-scheduler
cp env.example .env  # Add your API keys
docker-compose up -d
```

### Heroku (Easiest)
```bash
git clone <repo> && cd ai-healthcare-scheduler
heroku create your-app-name
git push heroku main
```

### Vercel (Serverless)
```bash
git clone <repo> && cd ai-healthcare-scheduler
vercel --prod
```

---

🏥 **Your AI Healthcare Scheduler is now ready for production!**

For support, create an issue in the repository or contact the development team.
