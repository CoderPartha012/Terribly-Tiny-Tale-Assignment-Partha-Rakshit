# Terribly-Tiny-Tale-Assignment-Partha-Rakshit
Terribly Tiny Tale Assignment

The above React.js component that displays a histogram of the top 20 most frequently occurring words in a given text file.

The component defines a state variable "histogramData" using the useState hook, which stores an array of sorted word frequencies. When the user clicks the "Submit" button, the component makes an HTTP GET request to the URL 'https://www.terriblytinytales.com/test.txt' using the axios library to fetch the text data. The text data is split into individual words, and their frequencies are computed and sorted to create an array of the top 20 most frequently occurring words, which is then stored in the histogramData state variable.

The component also defines a handleExportData function that is called when the user clicks the "Export" button. This function generates a CSV file containing the data in histogramData and saves it to the user's local file system using the file-saver library.

The component uses the useEffect hook to create and render a histogram using the d3.js library when the histogramData state variable is updated. The histogram is rendered within an SVG element, with the axes and bars created using d3.scaleBand, d3.scaleLinear, d3.axisBottom, d3.axisLeft, and d3.selectAll. The svgRef variable is used to reference the SVG element within the component.

Finally, the component renders a "Submit" button that triggers the handleFetchData function, and displays the histogram and "Export" button only when histogramData has a length greater than 0.
