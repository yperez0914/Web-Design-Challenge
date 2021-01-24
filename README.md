# Web-Design-Challenge
<br>
For this project, I created a visualization dashboard website to showoff the visualizatiions generated from my What's the Weather Like project that plotted weather conditions for cities around the world. Several pages were created to include each visualization, an explanation of the results, and the data used to build them.Multiple components were used to create the website including a navbar, cards, and grids from Bootsrap (with customizations of course!) Pandas was used to generate the html for the data table. Finally., formatting and media queries were added using CSS. A few of them will be highlighted below.
<br>

# Check out my website!
[Whats the Weather Like?](https://yperez0914.github.io/Web-Design-Challenge/)
<br>

# Navbar 
<br>
Each page has a navbar to navigate easily from one page to another and get back to this landing page easily. It also includes a dropdown to navigate to each plot. This was created using Boostrap's Navbar component.
<br>

## Example:
```
<div class = "row ">
        <div class = "col-3 mynav">
            <nav class="navbar  navbar-expand-lg navbar-light ">
                <a class="navbar-brand" href="index.html">Home</a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
                </button>
            </nav>
        </div>
        <div class = "col-9 mynav">
            <nav class="navbar  navbar-expand-lg navbar-light  ml-auto">
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item active">
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            Plot
                        </a>
                        <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
                            <a class="dropdown-item" href="viz1.html">NH: Max Temp vs. Latitude</a>
                            <a class="dropdown-item" href="viz2.html">NH: Cloudiness vs. Latitude </a>
                            <a class="dropdown-item" href="viz3.html">NH: Humidity vs. Latitude </a>
                            <a class="dropdown-item" href="viz4.html">NH: Wind Speed vs. Latitude </a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item" href="#">Southern Hemisphere Plots Coming Soon!</a>
                        </div>
                    </li>
                        <li class="nav-item">
                        <a class="nav-link" href="comparisons.html">Comparisons</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="data.html">Data</a>
                        </li>
                </ul>
                </div>
            </nav>
        </div>   
    </div>
```

<br>

# Cards

<br>
The Landing page, Comparisons page, and each Visualization page includes a sidebar with previews of the visualizations that will lead you to the their detailed explanations in a new tab with one click. This sidebar was created using Boostrap's Cards component. The visualization sidebar and Comparisons page also required the use of Bootsrap's grid for proper layout.
<br>

## Example: 

```
<div class = "col-md-4 viz">
        <div class="card">
            <div class="card-body">
                <h4 class="card-title">Visualizations</h4>
                <p class="card-text"> Click on the images below to learn more.</p>
            </div>
        <div class = "row">
            <div class = "col-md-6">
                <div class="card">
                    <div class="card-body image">
                        <a  target="_blank" href="viz1.html">
                            <img src = "Resources\assets\images\Northern Hemisphere-Max Temp vs. Latitude.png"class ="img-fluid" >
                        </a>
                            
                    </div>
                </div>
            </div>
            <div class = "col-md-6">
                <div class="card">
                    <div class="card-body image">
                        <a target="__blank" href = "viz2.html">
                            <img src = "Resources\assets\images\Northern Hemisphere-Cloudiness vs. Latitude.png" class = "img-fluid">
                    </a>
                    </div>
                </div>
            </div>
        </div>
        <div class = "row">
            <div class = "col-md-6">
                <div class="card">
                    <div class="card-body image">
                        <a target = "_blank" href = "viz3.html">
                            <img src = "Resources\assets\images\Northern Hemisphere-Humidity vs. Latitude.png" class = "img-fluid">
                    </a>
                    </div>
                </div>
            </div>
            <div class = "col-md-6">
                <div class="card">
                    <div class="card-body image">
                        <a target="_blank" href= "viz4.html">
                            <img src = "Resources\assets\images\Northern Hemisphere-Wind Speed vs. Latitude.png" class = "img-fluid">
                    </a>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </div>
    </div>
````

<br>

# Pandas Conversion from CSV to HTML
<br>
To create the Data page the CSV data was read in and converted to HTML using Pandas.
<br>

## Example 
```
cities = pd.read_csv(r"Resources\cities.csv", index_col = "City_ID")

html = cities.to_html()
print(html)
```
<br>

# CSS Formatting and Media Queries
<br>
To make the pages more visually appealing, a CSS stylesheet was created to format text-alignment, font-weight, background-color, etc. For optimal viewing, media queries were created for a background color change and for the Navbar to collapse and a toggle button to appear when viewing on small screens. 

## Example
```
/* Body formatting */
body {
    background-color: lightcoral;
}
/* Navbar formatting */
.mynav{
    font-weight: bold;
    background-color: rgb(230, 200, 30);
    /* padding:0% */
/* Media Queries */
@media only screen and (max-width: 767.98px) {
    body {
        background-color: white;
}
@media only screen and (max-width: 767.98px) {
    .mynav {
        font-weight: bold;
        background-color: white;
}
```
<br>
<br>
<br>
Find the full codes for each page here: <br>
[Landing Page full code](https://github.com/yperez0914/Web-Design-Challenge/blob/main/index.html) 
<br>
[Max Temp vs. Latitude Visualization Page]https://github.com/yperez0914/Web-Design-Challenge/blob/main/viz1.html)
<br>
[Humidity vs. Latitude Visualization Page](https://github.com/yperez0914/Web-Design-Challenge/blob/main/viz2.html) 
<br>
[Cloudiness vs. Latitude Visualization Page](https://github.com/yperez0914/Web-Design-Challenge/blob/main/viz3.html)
<br>
[Wind Speed vs. Latitude Visualization Page](https://github.com/yperez0914/Web-Design-Challenge/blob/main/viz4.html)
<br>
[Comparisons Page](https://github.com/yperez0914/Web-Design-Challenge/blob/main/comparisons.html)
<br>
[Data Page] https://github.com/yperez0914/Web-Design-Challenge/blob/main/data.html)
<br>
[CSS Stylesheet]https://github.com/yperez0914/Web-Design-Challenge/blob/main/style.css)
<br>