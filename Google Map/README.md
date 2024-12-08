# GMap App

This is a simple Google Maps application built using HTML, CSS, and JavaScript. The app allows users to log in and view their current location on a Google Map after successful authentication.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Integration](#api-integration)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Simple login mechanism with predefined credentials.
- **Geolocation**: Retrieves the user's current location using the browser's Geolocation API.
- **Interactive Map**: Displays the user's location on a Google Map with a marker.
- **Responsive Design**: Adaptable layout for both desktop and mobile devices.

## Technologies Used

- **HTML**: For the structure of the application.
- **CSS**: For styling and layout.
- **JavaScript**: For interactivity and handling API calls.
- **Google Maps JavaScript API**: To display maps and markers based on user location.

## Installation

To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/gmap-app.git
   ```

2. Navigate to the project directory:
   ```bash
   cd gmap-app
   ```

3. Open `index.html` in your web browser.

## Usage

1. Launch the application in your web browser.
2. Enter your username and password (e.g., `admin` / `password`).
3. Click the "Login" button to authenticate.
4. Upon successful login, your current location will be displayed on the map.

## API Integration

This application uses the [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript/overview) to fetch and display map data. Make sure to replace `AIzaSyAPQTpD3wN7zpV_Atn3RP7uMmozj9yTkLY` in the script tag with your own Google Maps API key.

### Example of Google Maps Integration

The following code snippet initializes the map at the user's current location:

```javascript
function showPosition(position) {
    var lat = position.coords.latitude;
    var lng = position.coords.longitude;
    var mapDiv = document.getElementById('map');
    mapDiv.style.display = 'block';

    var map = new google.maps.Map(mapDiv, {
        center: {lat: lat, lng: lng},
        zoom: 15
    });

    var marker = new google.maps.Marker({
        position: {lat: lat, lng: lng},
        map: map,
        title: 'You are here!'
    });
}
```

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please fork the repository and submit a pull request.

1. Fork the repository.
2. Create your feature branch:
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


