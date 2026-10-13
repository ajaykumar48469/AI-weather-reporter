# AI Voice Weather Reporter

Ask for the weather by typing, speaking, or tapping "Current Location", and get the forecast read back to you.

**[Live demo](https://aiweatherreporter.vercel.app)**

## Features

- **Three ways to search:** type a city, say it out loud, or use your device location.
- **Spoken forecasts:** the app reads the current conditions, the next 24 hours, and any safety advice.
- **Safety tips:** warnings for heat, freezing temperatures, strong wind, rain and snow, shown on screen and spoken.
- **°C / °F toggle:** switch units and the report refreshes.
- **Live details:** wind speed and direction, humidity, pressure and visibility.
- **Adaptive background:** the page colors change with the weather (clear, cloudy, rain, storm, snow).
- **Responsive and keyboard friendly:** works on phones, with `Alt+V` for voice and `Alt+L` for location.

## How it works

1. The city name goes to the OpenWeatherMap Geocoding API to get coordinates.
2. Coordinates go to the Current Weather and 5-day Forecast endpoints.
3. The app builds an on-screen report and a spoken summary from the response.

Voice input uses the browser's Speech Recognition API and spoken output uses Speech Synthesis, so there are no extra voice dependencies. Voice input works in Chromium-based browsers and Safari.

## Tech stack

- HTML5, CSS3, vanilla JavaScript (single page, no build step)
- OpenWeatherMap API (geocoding, current weather, forecast)
- Web Speech API (recognition and synthesis), Geolocation API
- Font Awesome icons
- Deployed on Vercel

## Run locally

```bash
git clone https://github.com/Joenikson/aiweatherreporter.git
cd aiweatherreporter
```

Open `index.html` in a browser, or serve it with any static server:

```bash
npx serve .
```

Add your own OpenWeatherMap key (free tier works) where the app defines `API_KEY`.

## Roadmap

- Move the API key behind a small serverless proxy
- City autocomplete
- Multi-language voice support
- 5-day forecast cards

## License

Released under the [Unlicense](LICENSE).

## Author

**Joe Nikson**: [GitHub](https://github.com/Joenikson) · [Portfolio](https://simpleportfolioim.netlify.app)
