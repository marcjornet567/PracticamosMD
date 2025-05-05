# ESTO ES UN DOCUMENTO DE PRACTICA
## Proyecto:
Hemos encontrado una API publica, llamada meteo[https://open-meteo.com/] , que nos da informacion meteorologica a tiempo real con un archivo con formato JSON.

## Sitios
### Yo he escojido
- **Barcelona**
- **Madrid**
- **Asturias**

## Codigo en python
Con esto ya planteado, hemos hecho los codigos con cada localizacion.


## Ejemplo de Codigo:
``` python
import urllib.request, json 


url_tiempo = (
    "https://api.open-meteo.com/v1/forecast?"
    "latitude=43.3619&longitude=-5.8494&current_weather=true&"
    "hourly=relativehumidity_2m"
)




with urllib.request.urlopen(url_tiempo) as datos:
	parseado = json.load(datos)

print("Temperatura en Asturias: ", parseado["current_weather"]["temperature"])
print("Viento en Asturias: ", parseado["current_weather"]["windspeed"])
print("Humedad: ", parseado["hourly"]["relativehumidity_2m"])

```
