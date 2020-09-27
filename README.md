# Analyse Document

## Probleem stelling
### Analyse
#### Abstract
![Abstract Design](img/Abstract_Design.jpg)
#### Smart Object (Hardware Analyse)
![Blokdiagram](img/HW_Blokdiagram.jpg)
##### Specificatie tabel
| Blok                   | Specificatie | Min   | Nominaal    | Max   |
|------------------------|--------------|-------|-------------|-------|
| Lithium-batterij 18650 | Werkspanning | 3V    | 3,6V        | 4,2V  |
|                        | Capaciteit   |       | 2850mAh     |       |
|                        | Stroom       |       | 28,50A(10C) |       |
| ATSAMD21               | Werkspanning | 1,62V |             | 3,63V |
|                        | FCPU         |       |             | 48MHz |
| SDS011                 | Werkspanning | 4,7V  | 5V          | 5,3V  |
|                        | Stroom       | <4mA  |             | 80mA  |
| Zonnepaneel            | Werkspanning |       |             |       |
|                        | Stroom       |       |             |       |
##### Argumentatie en alternatieven tabel

| Part                                                                  | Pro's en contra's                                                                                                                        |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Adafruit Feather M0                                                   | <ul><li>Usb programmeerbaar</li> <li>Genoeg CPU-kracht</li> <li>Zuinig</li></ul>                                                                                           |
| BME680 Breakout - Air Quality, Temperature, Pressure, Humidity Sensor | <ul><li>Compact</li>  <li>Grote input-voltage range</li> <li>I2C (0x76 \| 0x77)</li>  <li>4 in 1</li>  <li>Nadeel: lange settle-time</li></ul>                                                    |
| Li-Ion Batterij - 18650 - 3,7V 2900mAh                                | <ul><li>Grote capaciteit</li> <li>Snelladen</li> <li>Lage self-discharge</li> <li>Gebruikstemperatuur -20 <==> 60 graden Celcius</li> <li>oplaadtemperatuur 4 <==> 45 graden Celsius</li> |
| Batterijhouder voor 18650 batterijen                                  | <ul><li>Geen soldeerwerk op de batterijen</li> <li>Makkelijk accu te vervangen</li> <li>Makkelijk extern op te laden</li></ul>                                               |
#### Software Analyse
##### Data In- en Outputs
| Blok     | Data In            | Data Out                                            |
|----------|--------------------|-----------------------------------------------------|
| ATSAMD21 | Sensor data (alle) | Sensor data (alle)                                  |
| SDS011   | N.V.T.             | Sensor data (fijnstof)                              |
| DHT22    | N.V.T              | <ul><li>Sensor data (temperatuur)</li> <li>Sensor data (vochtigheid)</li></ul> |
| RFM95W   | Sensor data (alle) | Sensor data (alle                                   |
##### State diagram
##### Flowchart
![Flowchart](img/Flowchart.jpg)
##### Mockup
## Bronnen
