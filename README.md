# Belfast's Housing Crisis by Area
A data visualisation page demonstrating homelessness and public housing provision statistics across East, North, South and West Belfast.

## Overview

### What is this application for?
In the north of Ireland, decisions about new build public housing programmes are supposed to be made following the assessment of housing need in different areas. This includes the numbers of people experiencing homelessness and housing need, the availability of current public housing and any forthcoming plans to build new housing (additional stock).

Official statistics are a necessary component of this decision making process and are critical in enabling the public to hold politicians and public officials to account.

"Belfast's Housing Crisis by Area" is a response to the Northern Ireland Housing Executive's 2016 decision to cease periodic publications of key statistics relating to homelessness and public housing provision. "Belfast's Housing Crisis by Area" is an attempt to generate the crowd-sourcing and sharing of statistics and information among community organisations and NGOs active on housing rights issues which, in turn, will assist in public housing campaigns and advocacy.  

### What does it do?
Users can view 5 separate datasets, disaggregated by area (north, south, east and west), by visiting "Belfast's Housing Crisis by Area":
* number of households in 'Housing Stress' (i.e. >30 points on the General Housing Waiting List) - 2015
* number of households in critical need of housing (i.e. >150 points on the General Housing Waiting List) - 2015
* number of housing units allocated to individuals/families - 2015
* number of new units of public housing built - 2010-15
* total amount of public money paid to private landlords due to the shortage of public housing

The datasets are visualised through interactive charts which can be filtered to compare statsitics between areas.

Users can send email messages from the site to pass on information or make contact with the Equality Can't Wait campaign.

### How does it work
The "Belfast's Housing Crisis by Area" data is stored in the **static/data/housingdata.csv** file. The **Javascript** library **d3.js** is used to parse the data from the housingData.csv file and works with **dc.js** (including **crossfilter**) to plot and render charts constructed in the ```charts.js``` and ```calc.js``` file.

The programme is written in **Javascript**, the site is styled with a **Bootswatch** (**Bootstrap**) theme and **JQuery** code. The Bootstrap grid layout is used to make the application responsive across mobile, tablet and desktop devices. The site is designed using **mobile-first** design principles.

Users can contact the Equality Can't Wait campaign by sending an email directly from the site using **EmailJS** service.

**AWS Cloud9** has been used as the IDE for deployment of site on github pages. 

## Technology Used

### Code
- **HTML**, **CSS**, and **JavaScript (inc JQuery)**
    - Base languages used to create website
- [Jasmine](https://jasmine.github.io/) 
    - Javascript code was tested in the Jasmine framework test suite
- [d3.js](https://d3js.org/)
    - this Javascript library manipulates the DOM based on interactions with the datasets
- [dc.js](https://dc-js.github.io/dc.js/) and  [crossfilter](https://crossfilter.github.io/crossfilter/)
    - constructs the charts and enables interaction/responsiveness between the charts based on user interactions
- [EmailJS](http://www.emailjs.com/)
    - Allows users to send emails to the Equality Can't Wait email using client side technologies and EmailJS's Javascript library
- [Bootstrap](http://getbootstrap.com/)
    - **Bootstrap 4.0.0** is used to render a responsive layout
- [Bootswatch](https://bootswatch.com/)
    - the **Bootswatch** 'Sketchy' theme was used on elements of the site
- [JQuery](https://jquery.com)
    - **JQuery** adds animation styling to the site to enhance user experience. [jquery.simple-text-rotator](https://www.npmjs.com/package/jquery.simple-text-rotator) rotates the the total amount of public monies paid to private landlords across the city by area
- [Sass](https://sass-lang.com/)
    - **Sass/scss** CSS extension is used to code and organise CSS stylesheets

## Testing 
The back and front end features were tested manually. The manual testing methodology and tests are found [here](spec/MANUALTESTS.md) 

The **Jasmine Testing Framework** was used to test the callback function made to the d3.csv() method in [calc.js](js/calc.js). To test the function outside of the asynchronous request made to the .csv file, the function was abstracted in calc.js and an array of objects created to test the function (getTotalStress). The test suite can be found [here](spec/calcSpec.js).

## Contributing
"Belfast's Housing Crisis by Area" is an evolving project. The Equality Can't Wait campaign intend on periodically updating the site with statistics collected through freedom of information request or via user submissions/contact via the site. We welcome pull requests concerning the following planned features (or any other suggestions you may have):
* archive of datasets for download
* different pages displaying thematic issues around housing in Belfast
* data visulation using Google Maps Platform APIs to display comprehensive area based statistics

### Getting the code up and running
1. Clone this repository by opening your Terminal, change the current working directory to the location where you want the cloned directory to be made.  
2. Type `$git clone https://github.com/Deasun/housing-crisis.git`  and hit Enter. Your repository will be ready.
3. Run the index.html, open in a broswer and the page will display
4. We welcome all contributions to improving our code, so make changes you think are needed/desired and submit a pull request

## Credits

### Statistics
The statistics presented are compiled from a range of different datasets requested from the [Northern Ireland Housing Executive](https://www.nihe.gov.uk/) through Freedom of Information request in 2016.

### Developer
Dessie Donnelly (email: des_donn@mailbox.org)

### Partners
Equality Can't Wait & #BuildHomesNow campaign C/O PPR, Ground Floor, Community House, Citylink Business Park
6A Albert Street, Belfast, BT12 4HQ (tel: 028 90313315)
Contact: Elfie Seymour (email: elfie@pprproject.org)