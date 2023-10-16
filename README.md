# leaflet-challenge
<br>

A project that uses JavaScript with Leaflet and HTML to visualize earthquake and tectonic plates data.
<br>
<br>
Click for deployment: https://terrysimbar.github.io/leaflet-challenge/
<br> 
<img src="Images/earthquake_layer.png" width="1000">   

## Table of Contents
#### Introduction
#### Features
#### Requirements & Dependencies
#### Project Structure
#### Usage
#### Contributing
#### License
<br>

#### Introduction
This JavaScript with Leaflet project reads in JSON earthquake and tectonic plates data from two URLs to create a layered map visualization. The visualization allows users to switch map layers and click on markers to get earthquake data for different locations.


#### Features
- Use D3 to read in JSON data from URLs.

- Create interactive visualizations which include options for toggling between map layers and clicking markers to get earthquake information. 

<br>

#### Requirements & Dependencies
This project does not use external dependencies managed through npm or yarn. Instead, all the necessary JavaScript libraries, including D3 and Leaflet, are included directly in the accompanying HTML file using `<script>` tags. These libraries are either hosted via Content Delivery Networks (CDNs) or included locally.
<br>

---
## Project Structure
<br>

#### HTML Setup
The HTML file (`index.html`) in this project is structured as follows:

1. **Document Type Declaration** `<!DOCTYPE html>` defines the document type and version of HTML being used.

2. **Head Section** `<head>` contains meta information about the document, such as character encoding, viewport settings, and the page title.

3. **Leaflet CSS Styling** `<link rel="stylesheet">` is linked in the `<head>` section to provide styling for the map visulaization.

4. **Body Section** `<body>` contains the main content of the webpage, including the map elements.

5. **Map Structure**: The interactive map is structured within the `<body>`using `<script>` tags for Javacript, D3 and Leaflet.

6. **JavaScript File** A JavaScript file is included at the end of the `<body>` to handle interactivity and a link to the `logic.js` file that contains custom code for the map visualization.

Please refer to the accompanying `index.html` file for the complete code.
<br>

#### JavaScript Setup 
The `logic.js` file is used to create a map visualization with layer and markers. Here's an overview of its key functionalities:

1. **Define the URLs for JSON Data**: The `const url` and `const url2` variables are used to store the URLs of the JSON earthquake and tectonic plates data. The earthquake data in this project uses records from the past 7 days, while the tectonic plates data is static.  Developers have flexibility to choose earthquake data for various time frames using this link: https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php

2. **Fetch JSON Data**: The `async` and `await` methods are used with D3 to fetch the JSON data from the URLs and store them in the `earthquakeData` and `boundariesData` variables.

3. **Format the interactive Map**: The `L.map`, `L.tileLayer`, `L.LayerGroup`, `.forEach`, `L.control`, amd other methods are used to setup the map and legend. The legend uses a graduation of colors from light green for the earthquakes nearest to Earth's surface, to red for the deepest earthquakes.

4. **Format Circle Markers** `L.circleMarker` is used to create circle markers for each earthquake location. The `getColor` function is used to style the markers based on the magnitude of the earthquake, and the `bindPopup`method adds a popup with earthquake data for each marker.   

5. **Setup Toggling and Selecting Layers**: An event listener uses methods such as `querySelectorAll`, `querySelector`, `addEventListener`, `addTo`, and `forEach` to toggle between the different map layers. 

For the complete code and detailed implementation, please refer to the `logic.js` files in this project.
<br>

---
#### Usage
1. Ensure that you have all the necessary files/links/scripts. 
2. Load the project files in an appropriate code editor such as Jupyter Notebook. 
3. Copy the HTML File path and paste it in your browser to view the dashboard.

#### Contributions
Contributions to this project are highly encouraged! If you wish to contribute, please follow these guidelines:

- Fork the leaflet-challenge repository and clone it locally.
- Create a new branch for your feature or bug fix.
- Commit your changes with descriptive commit messages.
- Push your branch to your forked repository.
- Submit a pull request to the original repository.
- Please ensure that your code adheres to the project's coding style and conventions.


If you encounter any issues or have suggestions for improvements, please open an issue on the GitHub repository.

### License
These projects are licensed under the MIT License. Feel free to use, modify, and distribute the code as per the terms of the license. 