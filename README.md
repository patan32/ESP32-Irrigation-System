I am using Open-Meteo for weather. Entity is "weather.home". Make sure in states you have entity called: "home_rain_forecast_0d" or else it won't work. I had to use Meteorologisk institutt (Met.no) for humdity reading since Open-Meteo doesn't provide that entity. 

Change your weather entity name from HA for weather to work properly. Look for weather.forecast_home entity and change it to what you have in HA for weather. 
automation.yaml - updates the NZ holiday days. 
sensors.yaml - All sensors are defined and needs the entity changed to match yours in HA. 
