# GeoLocation API

The Geolocation API is a service that accepts an HTTPS request with the cell tower and WiFi access points that a mobile client can detect. 
It returns latitude/longitude coordinates and a radius indicating the accuracy of the result for each valid input.

## How the Geolocation API works

The Geolocation API uses cellular device data fields, cell tower data, and WiFi access point array data to return latitude/longitude coordinates and an accuracy radius. 
It accepts an HTTPS POST request and a JSON structured request body to its endpoint. The following example shows the request URL and an example request body:
```bash

https://www.googleapis.com/geolocation/v1/geolocate?key=YOUR_API_KEY" 
"Content-Type: application/json" 
{ "homeMobileCountryCode":310,
   "homeMobileNetworkCode":410,
   "radioType":"gsm",
   "carrier":"Vodafone",
   "considerIp":true
}

```


## Usage

[Geolocation](Geolocation):
The main class of this API — contains methods to retrieve the user's current position, watch for changes in their position, and clear a previously set watch.

[GeolocationPosition](GeolocationPosition):
Represents the position of a user. A GeolocationPosition instance is returned by a successful call to one of the methods contained inside Geolocation, 
inside a success callback, and contains a timestamp plus a GeolocationCoordinates object instance.

[GeolocationCoordinates](GeolocationCoordinates):
Represents the coordinates of a user's position; a Geolocation Coordinates instance contains latitude, longitude, and other important related information.

[GeolocationPositionError](GeolocationPositionError):
A GeolocationPositionError is returned by an unsuccessful call to one of the methods contained inside Geolocation, inside an error callback, and contains an error code and message.

[Navigator.geolocation](Navigator.geolocation):
The entry point into the API. Returns a Geolocation object instance, from which all other functionality can be accessed.

## Contributing

If you would like to contribute to my project, please follow these steps:

1. Fork the repository.
2. Make your changes.
3. Submit a pull request. 

## License

[MIT](https://choosealicense.com/licenses/mit/)
