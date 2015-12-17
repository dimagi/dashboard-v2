# Development Environment

<table>
  <tr>
    <td>Item</td>
    <td>Name</td>
    <td>Version</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>IDE</td>
    <td>RStudio</td>
    <td>0.98.1091</td>
    <td>--</td>
  </tr>
  <tr>
    <td>Language</td>
    <td>R</td>
    <td>3.1.2</td>
    <td>--</td>
  </tr>
  <tr>
    <td>Web Framework</td>
    <td>Shiny</td>
    <td>0.12.1</td>
    <td>Framework that allows you to create web applications is R.</td>
  </tr>
  <tr>
    <td>Specific packages</td>
    <td>Shinydashboard</td>
    <td>0.3.0</td>
    <td>CSS framework that allows you to create dashboard looking layouts.</td>
  </tr>
  <tr>
    <td></td>
    <td>Shinyapps</td>
    <td>0.3.63</td>
    <td>Library that allows you to deploy applications to shinyapps.io directly from RStudio.</td>
  </tr>
  <tr>
    <td></td>
    <td>Leaftlet</td>
    <td>1.0.0.9999</td>
    <td>Create interactive maps with the JavaScript ‘Leaflet’ Library</td>
  </tr>
  <tr>
    <td></td>
    <td>GoogleVis</td>
    <td>0.5.8</td>
    <td>R interface to Google Charts</td>
  </tr>
  <tr>
    <td></td>
    <td>Lubridate</td>
    <td>1.3.3</td>
    <td>Makes dealing with dates easier</td>
  </tr>
  <tr>
    <td>Hosting service</td>
    <td>Shinyapps.io</td>
    <td>--</td>
    <td>Platform as a Service on which you can deploy Shiny applications.</td>
  </tr>
  <tr>
    <td>Github Repository</td>
    <td>https://github.com/ieda-project/dashboard-v2</td>
    <td></td>
    <td></td>
  </tr>
</table>


# Run The Application Locally

1. Clone the repository

2. Open RStudio

3. Set the working directory to the repository

4. Install all the above mentioned specific packages

5. Execute the [Data Update Procedure](#heading=h.amimpgt6afn5) (see below)

6. Open one of the main Shiny App files: server.R, ui.R, global.R

7. Click on the ‘Run App’ button

8. *Optionally install other missing packages and re-run the application*

# Data Update Procedure

Download the following exports from CommCareHQ and copy them to the ‘data’ directory located at the root of the repository (create it if non existent).

<table>
  <tr>
    <td>Name</td>
    <td>Action</td>
  </tr>
  <tr>
    <td>Case Exports</td>
    <td></td>
  </tr>
  <tr>
    <td>tablet_user (IeDA Dashboard, PBF Migration)</td>
    <td>Rename to: tablet-users.csv</td>
  </tr>
  <tr>
    <td>Form Exports</td>
    <td></td>
  </tr>
  <tr>
    <td>Child Treatment - Meta Data (IeDA Dashboard)</td>
    <td>Rename to: child-treatment.csv</td>
  </tr>
  <tr>
    <td>Child Visit - Meta Data (IeDA Dashboard)</td>
    <td>Rename to: child-visit.csv</td>
  </tr>
  <tr>
    <td>Enroll Child - Meta Data (IeDA Dashboard)</td>
    <td>Rename to: enroll-child.csv</td>
  </tr>
  <tr>
    <td>Other Exports</td>
    <td></td>
  </tr>
  <tr>
    <td>List of mobile users</td>
    <td>Rename column: "data: csps_site_code" to “site_code”
Rename column: “data: district” to “district”
Keep only columns: username, site_code, district
Delete sheet: groups
Save as: mobile-users.csv</td>
  </tr>
  <tr>
    <td>Locations</td>
    <td>Keeps only sheet: CSPS
Keep only columns: site_code, name, parent_site_code, latitude, longitude
Save as: locations.csv</td>
  </tr>
</table>


# Deploy procedure

The Shiny deployment toolchain is directly integrated with RStudio. Everything can be done through the RStudio UI.

## 1. Create a shinyapp.io account (only ones)

* Go to [https://www.shinyapps.io/admin/#/signup](https://www.shinyapps.io/admin/#/signup)

## 2. Connect your Shinyapps.io account to RStudio (only ones)

* Go to *Tools > ShinyApps > Manage Accounts*

* Click on *Connect*

* Follow instructions

## 3.Publish Application

* Open one of the main Shiny App files: server.R, ui.R, global.R

* Go to *Tools > Shiny App > Publish App...*

* Select account

* Select application (create new if first time)

