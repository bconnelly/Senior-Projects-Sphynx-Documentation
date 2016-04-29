Front End
=========

Our front end consists of an application demonstrating CEAN (Cassandra, Express, Angular, and Node) Integration with FusionCharts. Application allows users to view analysis pertaining to Democratic and Republican party candidate nominations. Data sources used were Twitter, GDELT, and the Huffington Post API. Each source was tracked by counts and all candidates were compared on a single FusionChart. Then, with all counts discovered on a certain time frame, analysis was done to try and find a correlation between multiple sources.  

**Technologies used:**

FusionCharts is a comprehensive JavaScript charting library that allowed us to create charts relative to candidate Tweet, GDELT, and Poll Percentage counts.

AngularJS was used to implement dynamic views for individual candidates running for presidential hopefuls. This allowed us to extend our HTML code into a more simplified and easily readable environment. It helped alleviate issues with data binding, which AngularJS is well known to simplify.

HTML and CSS were used within our Angular application for beautification, page views, and container structures for each individual application page.

JSON files were created by running the jsonize.py file that contained the FusionCharts specific graph structure and data associated with said graph. Inquire within .json files in the FrontEnd/NGC-FrontEnd/public folder if you would like a visual model. 
 
Type in either below when the Front End server has been started:
| **Machine 1:** 128.138.202.110:3000
| **Machine 2:** 128.138.202.117:3000


Type in either below when the Front End server has been started:

| **Machine 1:** 128.138.202.110:3000
| **Machine 2:** 128.138.202.117:3000

(if neither connect to the Front End, the server is down or has not been initialized for Front End purposes)

**Instructions to run locally**

1) Clone repository and download npm packages


    ``git clone https://github.com/phugiadang/CSCI-4308-Open-Sources-Data-Analytics.git``

    ``npm install``

    ``bower install``

2) Go into directory FrontEnd/NGC-FrontEnd/


Run ``npm start`` or ``sudo npm start``



3) Open browser http://localhost:3000/


**Questions**

For questions, contact Team OSAM (through GitHub is fine for now)
