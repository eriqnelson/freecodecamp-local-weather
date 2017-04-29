# Objective: Build a CodePen.io app that is functionally similar to this:
http://codepen.io/FreeCodeCamp/full/bELRjV

1. User Story: I can see the weather in my current location.
https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/Using_geolocation

* Query location on load
navigator.geolocation.getCurrentPosition(success[, error[, options]])
* Display weather plaintext with alt ids for screen readers
* Display temp

2. User Story: I can see a different icon or background image (e.g. snowy mountain, hot desert) depending on the weather.
Display an icon
https://erikflowers.github.io/weather-icons/
https://openweathermap.org/weather-conditions
Map {“id”:num} to icon lookup table


3. User Story: I can push a button to toggle between Fahrenheit and Celsius.
Stateful indicator of the metric determines which function to process

`function toFahrenheit(num){return (num-32)*5/9};`
`function toCelsius(num){return num*9/5+32};`

## Weather API
https://openweathermap.org/current

Sample response:

`{"coord":{"lon":139.01,"lat":35.02},"weather":[{"id":800,"main":"Clear","description":"clear sky","icon":"01n"}],"base":"stations","main":{"temp":285.514,"pressure":1013.75,"humidity":100,"temp_min":285.514,"temp_max":285.514,"sea_level":1023.22,"grnd_level":1013.75},"wind":{"speed":5.52,"deg":311},"clouds":{"all":0},"dt":1485792967,"sys":{"message":0.0025,"country":"JP","sunrise":1485726240,"sunset":1485763863},"id":1907296,"name":"Tawarano","cod":200}`
