# Earthlytics - US Earth Data Visualization

A comprehensive web application for exploring US environmental data using NASA satellite imagery and AI-powered analysis. Built with Next.js, TypeScript, and CesiumJS.

## 🌍 Features

- **Interactive 3D Globe**: Realistic Earth viewer using NASA satellite imagery
- **Real-time Data Visualization**: Weather, climate, vegetation, water, pollution, land use, and socioeconomic data
- **AI-Powered Analysis**: Generate eco-focused, urban, and balanced development scenarios
- **Data Export**: Download datasets as CSV or GeoJSON
- **Search & History**: Find locations by city name or coordinates with search history
- **Responsive Design**: Works on desktop and mobile devices

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Cesium Ion account (free)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd earthlytics
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp env.example .env.local
   ```

4. **Configure your API keys in `.env.local`**
   ```env
   # Required: Get your free token from https://cesium.com/ion/
   NEXT_PUBLIC_CESIUM_ION_TOKEN=your_cesium_ion_token_here
   
   # Optional: For enhanced data (get from NASA Earthdata)
   NASA_API_KEY=your_nasa_api_key_here
   NASA_EARTHDATA_TOKEN=your_nasa_earthdata_token_here
   
   # Optional: For AI analysis (get from OpenAI)
   OPENAI_API_KEY=your_openai_api_key_here
   ```

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🛠️ Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **TypeScript** - Type-safe JavaScript
- **TailwindCSS** - Utility-first CSS framework
- **CesiumJS** - 3D globe and mapping library
- **Recharts** - Data visualization components
- **Lucide React** - Icon library

### Backend
- **Next.js API Routes** - Serverless API endpoints
- **OpenStreetMap Nominatim** - Geocoding service
- **US Census Geocoder** - Fallback geocoding
- **NASA APIs** - Satellite and environmental data

### Data Sources
- **NASA GIBS/Earthdata** - Satellite imagery and environmental data
- **NASA Giovanni** - Climate and atmosphere data
- **NASA SEDAC** - Socioeconomic data
- **OpenStreetMap** - Geographic data

## 📁 Project Structure

```
earthlytics/
├── app/                    # Next.js App Router
│   ├── api/               # API routes
│   │   ├── geocode/       # Location search
│   │   ├── nasaProxy/     # NASA data proxy
│   │   ├── ai/            # AI analysis
│   │   └── export/        # Data export
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Root layout
│   └── page.tsx           # Main page
├── components/            # React components
│   ├── charts/           # Data visualization components
│   ├── Header.tsx        # Top navigation
│   ├── Sidebar.tsx       # Data category sidebar
│   ├── GlobeViewer.tsx   # 3D globe component
│   ├── HistoryPanel.tsx  # Search history
│   ├── AIAssistant.tsx   # AI analysis panel
│   └── DataVisualization.tsx # Main data display
├── types/                # TypeScript type definitions
├── public/               # Static assets
├── package.json          # Dependencies
├── tailwind.config.js    # Tailwind configuration
├── next.config.js        # Next.js configuration
└── README.md            # This file
```

## 🎯 Usage

### Basic Navigation
1. **Search for a location** using the search bar (city name or coordinates)
2. **Click on the globe** to select any US location
3. **Choose a data category** from the left sidebar
4. **View visualizations** and data tables
5. **Get AI analysis** using the right panel
6. **Export data** as CSV or GeoJSON

### Data Categories
- **Weather**: Current conditions, temperature, humidity, wind
- **Climate**: Historical patterns, seasonal data
- **Vegetation**: NDVI, coverage, health indicators
- **Water**: Water bodies, quality, coverage
- **Pollution**: Air quality, pollutant levels
- **Land Use**: Urban, agricultural, forest coverage
- **Socioeconomic**: Population, income, employment

### AI Scenarios
The AI assistant generates three development scenarios:
- **Eco-Focused**: Prioritizes environmental sustainability
- **High-Density Urban**: Maximizes urban development
- **Balanced Growth**: Combines sustainability with economic growth

## 🔧 Configuration

### Cesium Ion Setup
1. Visit [cesium.com/ion](https://cesium.com/ion)
2. Create a free account
3. Get your access token
4. Add it to your `.env.local` file

### NASA API Keys (Optional)
1. Visit [NASA Earthdata](https://earthdata.nasa.gov/)
2. Create an account and get API keys
3. Add keys to your `.env.local` file

### OpenAI API (Optional)
1. Visit [OpenAI Platform](https://platform.openai.com/)
2. Get an API key
3. Add it to your `.env.local` file

## 🚀 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically

### Other Platforms
The app can be deployed to any platform that supports Next.js:
- Netlify
- Railway
- Render
- AWS Amplify

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **NASA** for providing satellite imagery and environmental data
- **Cesium** for the 3D globe technology
- **OpenStreetMap** for geocoding services
- **Recharts** for data visualization components

## 🐛 Troubleshooting

### Common Issues

**Globe not loading**
- Check your Cesium Ion token
- Ensure you have a stable internet connection
- Check browser console for errors

**Data not loading**
- Verify your NASA API keys
- Check network connectivity
- Some data may be simulated for demo purposes

**Build errors**
- Clear `.next` folder and reinstall dependencies
- Check Node.js version (18+ required)
- Verify all environment variables are set

### Getting Help

- Check the [Issues](https://github.com/your-repo/earthlytics/issues) page
- Create a new issue with detailed description
- Include browser console errors if applicable

## 🔮 Future Enhancements

- Real-time data integration with NASA APIs
- Historical data comparison
- Custom data layer creation
- Advanced AI analysis with machine learning
- Mobile app version
- Collaborative features
- Real-time collaboration
- Advanced filtering and search
- Custom visualization tools

---

Built with ❤️ for environmental awareness and data-driven decision making.
