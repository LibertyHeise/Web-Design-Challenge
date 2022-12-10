# Web-Design-Challenge
Module 11

Introduction

Through this process I worked in Visual Code to create my html pages (inde and data) which were used as a landing page and a data page, respectfully.  

Index
<!DOCTYPE html>
<html lang="en-us">

<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">

  <title>Bootstrap Visualization Dashboard</title>

  <!-- Boostrap Stylesheet -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous">

  <!-- Our own CSS stylesheet -->
  <link rel="stylesheet" href="assets/css/styles.css" media="screen">

</head>

<body>
  <!-- Start of navbar -->
  <nav class="navbar navbar-expand-lg navbar-custom">
    <div class="container-fluid">
      <div class="col-xs-9 phone-nav">
        <a class="navbar-brand" href="#" id="logo">Latitude</a>
      </div>

      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div>
        <ul class="nav navbar-nav justify-content-end">

          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false"
              aria-haspopup="true">
              Plots<span class="caret"></span>
            </a>
            <!-- <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true"
                aria-expanded="false">Plots <span class="caret"></span></a> -->
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="visualization/temp.html">Max Temperature</a></li>
              <li><a class="dropdown-item" href="visualization/humidity.html">Humidity</a></li>
              <li><a class="dropdown-item" href="visualization/cloudiness.html">Cloudiness</a></li>
              <li><a class="dropdown-item" href="visualization/wind.html">Wind Speed</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="comparison.html">Comparison</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="data.html">Data</a>
          </li>

        </ul>
      </div>
    </div>
  </nav>

  <!-- End of navbar -->

  <!-- Start of container -->
  <div class="container">
    <section class="row">
      <div class="col-md-8">
        <article class="description-content">
          <h1 class="description-header">Summary: Latitude vs. X</h1>
          <hr class="description-hr" />
          <img src="assets/images/Fig1.png" alt="" id="description-image" />
          <p>This data project was completed in order to analyze how weather changes as you get closer to the equator. To
            determine specifics in each data set, data was pulled from the OpenWeatherMap API and assembled on over 500
            cities.</p>
          <p>Once the dataset was compiled, Matplotlib was used to plot various specifics of the weather vs. latitude.
            The specifics included: temperature, cloudiness, wind speed, and humidity. This data is provided through data and visualizations created as part of the analysis.</p>
        </article>
      </div>
      <div class="col-md-4">
        <!-- Start of Visualizations imageNav Area -->
        <section id="imageNav-area">
          <div class="imageNav-content">
            <h2 class="imageNav-header">Visualizations</h2>
            <hr />
            <div id="images">
              <a href="visualization/temp.html"><img src="assets/images/Fig1.png" alt="Latitude vs. Max Temperature"
                  class="imageNav-photo"></a>
              <a href="visualization/humidity.html"><img src="assets/images/Fig2.png" alt="Latitude vs. Humidity"
                  class="imageNav-photo"></a>
              <a href="visualization/cloudiness.html"><img src="assets/images/Fig3.png" alt="Latitude vs. Cloudiness"
                  class="imageNav-photo"></a>
              <a href="visualization/wind.html"><img src="assets/images/Fig4.png" alt="Latitude vs. Wind Speed"
                  class="imageNav-photo"></a>
            </div>
          </div>
        </section>
        <!-- End of the Visualizations imageNav Area -->

      </div>
    </section>
  </div>

  <!-- Start of Visualizations imageNav Area -->

  <!-- End of the Visualizations imageNav Area -->
  <!-- End of container -->

  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"
    integrity="sha384-oBqDVmMz9ATKxIep9tiCxS/Z9fNfEXiDAYTujMAeBAsjFuCZSmKbSSUnQlmh/jp3"
    crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.min.js"
    integrity="sha384-IDwe1+LCz02ROU9k972gdyvl+AESN10+x7tBKgc9I5HFtuNz0wWnPclzo6p9vxnk"
    crossorigin="anonymous"></script>

</body>

</html>

Data
import pandas as pd

cities_csv_df = pd.read_csv('Resources/cities.csv')

cities_csv_df.to_html('data.html', index=False, classes=['table', 'table-striped', 'table-hover'])

I then created all of the further analysis pages for the different weather points including cloudiness, humidity, temperature and wind.  I also used the bootstrap css to create my styles for the web page so it looked similar/the same as the one exampled in the challenge.

