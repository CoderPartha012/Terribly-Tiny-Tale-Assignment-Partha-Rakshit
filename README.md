# Terribly Tiny Tales Histogram

This React application fetches data from the Terribly Tiny Tales API, processes the text data to create a histogram of the top 20 most frequent words, and visualizes the histogram using D3.js. The user can also export the histogram data as a CSV file.

## Table of Contents

- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Code Explanation](#code-explanation)

## Dependencies

The following dependencies are used in this application:

- React: A JavaScript library for building user interfaces.
- Axios: A popular HTTP client for making API requests.
- D3.js: A powerful library for creating data visualizations.
- FileSaver: A library for saving files on the client-side.

## Installation

1. Make sure you have Node.js and npm installed on your system.
2. Clone the repository.
3. Navigate to the project directory and run `npm install` to install the required dependencies.

## Usage

1. Run `npm start` to start the development server.
2. Open your browser and navigate to `http://localhost:3000`.
3. Click the "Submit" button to fetch the data and display the histogram.
4. The top 20 most frequent words will be displayed in a histogram.
5. Click the "Export" button to download the histogram data as a CSV file.

## Code Explanation

The main component of the application is `App`. It has the following state variables and functions:

- `histogramData`: An array that stores the processed histogram data.
- `handleFetchData`: An asynchronous function that fetches the text data from the API, processes it to calculate word frequencies, and updates the `histogramData` state.
- `handleExportData`: A function that exports the histogram data as a CSV file using the `file-saver` library.
- `svgRef`: A React ref that is used to reference the SVG element for the histogram visualization.

The `React.useEffect` hook is used to create the histogram visualization using D3.js whenever the `histogramData` state is updated.

The component renders a "Submit" button, which, when clicked, calls the `handleFetchData` function to fetch and process the data. If the `histogramData` array is not empty, the component also renders the histogram visualization and an "Export" button, which, when clicked, calls the `handleExportData` function to export the data as a CSV file.
