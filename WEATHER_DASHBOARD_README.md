# Weather Dashboard

A beautiful, responsive weather dashboard that fetches real-time weather data from the OpenWeatherMap API.

## Features

✨ **Real-Time Weather Data**
- Current weather conditions for any city
- Temperature, humidity, wind speed, pressure, and visibility
- Weather description and icons

📊 **5-Day Forecast**
- Hourly forecast data visualization
- Temperature trends and weather conditions
- Min/Max temperature display

📍 **Location Services**
- Search by city name
- Use geolocation to get weather for your current location
- Recent searches history stored in browser

🎨 **Beautiful UI**
- Responsive design for all devices
- Glassmorphism effects
- Smooth animations and transitions
- Dark mode friendly

## Setup Instructions

### 1. Get API Key
1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Get your API key from the dashboard
4. Free tier includes current weather and forecast data

### 2. Configure the Dashboard
Open `app.js` and replace the API_KEY:

```javascript
const API_KEY = 'your_api_key_here'; // Replace with your OpenWeatherMap API key
```

### 3. Run the Dashboard
- Open `index.html` in your web browser
- Or use a local server:
  ```bash
  python -m http.server 8000
  # or
  npx http-server
  ```
- Visit `http://localhost:8000`

## Files

- **index.html** - Main HTML structure
- **styles.css** - Styling and responsive design
- **app.js** - JavaScript for API calls and DOM manipulation
- **WEATHER_DASHBOARD_README.md** - Documentation

## Usage

### Search by City
1. Enter a city name in the search box
2. Press Enter or click the Search button
3. View current weather and 5-day forecast

### Use Your Location
1. Click "📍 Use My Location" button
2. Allow browser access to your location
3. Weather for your location loads automatically

### Recent Searches
- Click any recent search to reload that city's weather
- Last 5 searches are stored in browser local storage

## API Endpoints Used

- **Current Weather**: `/weather?q={city}&appid={API_KEY}&units=metric`
- **Forecast**: `/forecast?q={city}&appid={API_KEY}&units=metric`
- **By Coordinates**: `/weather?lat={lat}&lon={lon}&appid={API_KEY}`

## Weather Icons

```
01d/01n - Clear sky ☀️/🌙
02d/02n - Cloudy ⛅/☁️
09d/09n - Rainy 🌧️
11d/11n - Thunderstorm ⛈️
13d/13n - Snow ❄️
50d/50n - Fog 🌫️
```

## Customization

### Change Temperature Units
Modify the `units` parameter in API calls:
- `units=metric` - Celsius (default)
- `units=imperial` - Fahrenheit

### Modify Color Scheme
Edit the gradient in `styles.css`:
```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Adjust Forecast Days
In `displayForecast()` function, change the slice value:
```javascript
Object.entries(dailyForecasts).slice(0, 5) // Change 5 to desired days
```

## Browser Compatibility

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Geolocation requires HTTPS on production

## Troubleshooting

### "City not found" Error
- Check spelling of city name
- Use English city names
- Try full name with country code

### No Weather Data Showing
- Verify API key is correct
- Check API key has weather access
- Check browser console for errors (F12)

### Geolocation Not Working
- Ensure website is HTTPS (localhost works)
- Check browser permissions
- Allow location access when prompted

## Free Tier Limitations

OpenWeatherMap free tier includes:
- Current weather
- 5-day forecast
- Call limit: 60 calls/minute
- Up to 1,000 calls/day

## Inspiration & Motivation

Start your day with [good morning quotes](https://www.inspiringshortquotes.com/good-morning-quotes/) to set a positive tone. Explore [deep quotes](https://www.inspiringshortquotes.com/deep-quotes/) for meaningful insights and reflection. Discover [short quotes](https://www.inspiringshortquotes.com/short-quotes/) that pack powerful messages in just a few words.

Whether you're checking the weather or seeking daily motivation, visit [Inspiring Short Quotes](https://www.inspiringshortquotes.com/) for your daily dose of inspiration with our collection of [motivational quotes](https://www.inspiringshortquotes.com/short-quotes/).

## Future Enhancements

- [ ] Multiple city comparison
- [ ] Weather alerts
- [ ] Historical weather data
- [ ] Weather maps integration
- [ ] Air quality index
- [ ] Severe weather warnings
- [ ] UV index data
- [ ] Sunrise/sunset times

## License

Free to use and modify for personal or commercial projects.

## Support

For issues with OpenWeatherMap API:
- Check [API Documentation](https://openweathermap.org/api)
- Visit [Support Forum](https://openweathermap.org/questions)

For daily inspiration, check out [good morning quotes](https://www.inspiringshortquotes.com/good-morning-quotes/), [deep quotes](https://www.inspiringshortquotes.com/deep-quotes/), and [short quotes](https://www.inspiringshortquotes.com/short-quotes/).

Enjoy your weather dashboard! 🌤️
