# leaflet-challenge
<br>

A project that uses JavaScript with Leaflet and HTML to visualize earthquake data.
<br>
<br>
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
This JavaScript with Leaflet project reads in JSON earthquake data from a URL and creates a layered earthquake data vizualization. The visualization allows users to switch map layers and click on markers to get earthquake data for diffrent locations.


#### Features
- Read in JSON earthquake data from a URL.

- Create interactive vizualizations which include options for toggling between map layers and clicking markers for earthquake information. 

<br>

#### Requirements & Dependencies
This project does not use external dependencies managed through npm or yarn. Instead, all the necessary JavaScript libraries, including Leaflet, are included directly in the accompanying HTML file using `<script>` tags. These libraries are either hosted via Content Delivery Networks (CDNs) or included locally.
<br>

---
## Project Structure
<br>

#### HTML Setup
The HTML file (`index.html`) in this project is structured as follows:

1. **Document Type Declaration** `<!DOCTYPE html>` defines the document type and version of HTML being used.

2. **Head Section** `<head>` contains meta information about the document, such as character encoding, viewport settings, and the page title.

3. **Leaflet CSS Styling** `<link rel="stylesheet">` is linked in the `<head>` section to provide styling for the map vizulaization.

4. **Body Section** `<body>` contains the main content of the webpage, including the map elements.

5. **Map Structure**: The interactive maps are structured within the `<body>`using `<script>` tags for Javacript and Leaflet.

6. **JavaScript File** A JavaScript file is included at the end of the `<body>` to handle interactivity and data visualization, followed by a link to the `logic.js` file that contain custom code for the map vizualization.

Please refer to the accompanying `index.html` file for the complete code.
<br>

#### JavaScript Setup 
The `logic.js` file is used to create a map vizualization with markers. Here's an overview of its key functionalities:

1. **Define the URL for JSON Data**: The `const url` and `const url2` variables are used to store the URLs of the JSON earthquake and tectonic plates data. 

2. **Create and add a Legend to the Map**: The `L.control`, `onAdd`, and `legend.addTo` methods are used to create a custom legend for the map. The legend uses a graduation of colors from bright red, for the earthquakes nearest to Earth's surface, to light green, for the deepest earthquakes.

3. **Create Circle Markers** `L.circleMarker` is used to create circle markers for each earthquake location. The `getColor` function is used to style the markers based on the magnitude of the earthquake, and the `bindPopup`method adds a popup with earthquake data for each marker.    

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