
<div align = 'center'>

[![Logo]][Website]

#### A ESP8266 Weather Station

</div>


**Development**   [![Badge Master]][Actions] <br>
**Master**    [![Badge Master]][Actions]

---

<div align = 'center'>

**⸢ [Install] ⸥**  **⸢ [Modules] ⸥**  

</div>

---





This code works best with the **NodeMCU V2 ESP8266** module and an `0.96"` **OLED** display.
To get you up and running in no time we created a kit which contains all the necessary parts:
[Kit]

By buying this and [other kits][Shop] from us you are funding maintenance and  development of this library. Thank you!

[![Kit Preview]][Kit]


## Service level promise

<table><tr><td><img src="https://thingpulse.com/assets/ThingPulse-open-source-prime.png" width="150">
</td><td>This is a ThingPulse <em>prime</em> project. See our [open-source commitment declaration][Commitment] for what this means.</td></tr></table>





## Why Weather Station as a library?

I realized that more and more the Weather Station was becoming a general framework for displaying data over WiFi to one of these pretty displays. But everyone would have different ways or sources for data and having the important part of the library would rather be the classes which fetch the data then the main class.
So if you write data fetchers which might be of interest to others please contact me to integrate them here or offer your code as extension library yourself and call it something like esp8266-weather-station-<yourservice>.
We will gladly list it here as third party library...

## Upgrade Notes

**Version 2, January 2020, removes WU support, see below**

**Replace Wunderground with OpenWeatherMap as weather data provider**

The weather information provider we used so far (Wunderground) [recently stopped their free tier][No Free] without previous notice on May 15, 2018. This release adds support for a new provider with a free tier for weather information: OpenWeatherMap.com. The basic demo (WeatherStationDemo) has been adapted to use this new API through the OpenWeatherMapCurrent and OpenWeatherMapForecast REST clients.

Sadly OpenWeatherMap provides less information than Wunderground did (or still does). If you are missing attributes in the response documents then please [contact the OpenWeatherMap team][OpenWeatherMap].

**ESP8266 OLED Library upgrade**

The ESP8266 OLED Library changed a lot with the latest release of version 3.0.0. We fixed many bugs and improved performance and changed the API a little bit. This means that you might have to adapt your Weather Station Code if you created it using the older 2.x.x version of the library. Either compare your code to the updated WeatherStationDemo or read through the [upgrade guide][Upgrade]

## Deprecation notes

| Announcement  | Module  | Removal  |
|---------------|---------|----------|
| 2018-06-13    | all **Wunderground** related code, see [our blog][Bye Wunderground] for details  | January 2020, version 2.0.0  |

<!----------------------------------------------------------------------------->

[Badge Development]: https://github.com/ThingPulse/esp8266-weather-station/actions/workflows/main.yml/badge.svg?branch=development
[Badge Master]: https://github.com/ThingPulse/esp8266-weather-station/actions/workflows/main.yml/badge.svg

[Install]: Documentation/Install.md
[Modules]: Documentation/Modules.md

[Upgrade]: https://github.com/ThingPulse/esp8266-oled-ssd1306/blob/master/UPGRADE-3.0.md
[Actions]: https://github.com/ThingPulse/esp8266-weather-station/actions
[Logo]: https://thingpulse.com/assets/ThingPulse-w300.svg

[Tutorial]: https://docs.thingpulse.com/how-tos/Arduino-IDE-for-ESP8266/
[API Key]: https://docs.thingpulse.com/how-tos/openweathermap-key/

[Commitment]: https://thingpulse.com/about/open-source-commitment/
[Website]: https://thingpulse.com
[Shop]: https://thingpulse.com/shop/

[Kit Preview]: resources/ThingPulse-ESP8266-Weather-Station.jpeg
[Kit]: https://thingpulse.com/product/esp8266-iot-electronics-starter-kit-weatherstation-planespotter-worldclock/

[Example]: examples/WeatherStationDemo/WeatherStationDemo.ino

[OpenWeatherMap]: https://openweathermap.desk.com/customer/portal/emails/new
[No Free]: https://thingpulse.com/weather-underground-no-longer-providing-free-api-keys/
[Alonso]: http://conga.oan.es/~alonso/doku.php?id=blog:sun_moon_position
[Bye Wunderground]: https://thingpulse.com/hello-openweathermap-bye-bye-wunderground/

