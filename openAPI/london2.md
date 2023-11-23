Source from https://tfl.gov.uk/info-for/open-data-users/api-documentation

Our Unified API
Our unified API brings together data across all modes of transport into a single RESTful API. This API provides access to the most highly requested realtime and status information across all the modes of transport, in a single and consistent way.
Example Unified API calls
Our data downloads
General
Tube
Bus, Coach and River
Roads
Santander Cycles
Oyster
Accessibility
Network statistics
Cycle Hire usage data 2012 - 2020
Oyster card data
 
Example Unified API calls
Access to the developer documentation is available at https://api.tfl.gov.uk

Example API requests (PDF 42KB)
Our data downloads
All the data feeds below are available for download. Using our data is subject to our terms and conditions. For a full description of each data feed, along with schema and sample data, please see our open data page on the TfL website.

General
Journey Planner API Beta
This API allows you to make requests to TfL's Journey Planner and receive responses as XML. The JP API is IP locked. When we've reviewed your registration information we'll send you an email to let you know if access is granted to the IP address you have provided.

Journey Planner timetables
The Journey Planner timetable feed contains up to date standard timetables for London Underground, bus, DLR and river services.

Station locations
Our station location feed is a geo-coded KML feed of most London Underground, DLR and London Overground stations.

Station facilities
Our station facilities feed is a Geo-coded KML feed of most London Underground, DLR and London Overground stations. It has station facilities and access information for each station.

Tube
Tube departure boards, line status and station status
This feed provides access to live Tube data, including a summary train prediction service, a detailed train prediction service, station and line status

Tube - this weekend v2
The 'Tube this weekend' feed contains information on planned line and station closures for the coming weekend. It also has details of planned works affecting station access - such as those involving lifts and escalators.

Bus, Coach and River
Live bus and river bus arrivals API (instant)
This API provides live bus and river bus arrival information across all TfL bus stops and piers. Instant requests are responded to with the live bus and river bus arrival information valid at that point in time.

Live bus and river bus arrivals API (stream)
This API provides live bus and river bus arrival information across all TfL bus stops and piers. Stream requests are responded to with a continuous supply of live bus and river bus arrival information. Access to the streamed API is password restricted. Once your details have been verified a username and password will be issued by email.

Bus stop locations
This dataset contains information about the location and identifiers for each bus stop served by the London bus network.

Bus routes
This dataset describes the London Buses standard network information. The network information includes the location of all bus stops in London and the sequence of bus stops that every bus route in London stops at.

Bus stop localities
This dataset contains additional location information (road name, locality and borough) for each bus stop served by the London bus network. The locality information contained within is based on a range of sources from the GLA - the locality data is not a definitive record of London's socio-geographical structure but an aid to help understand London's localities at a glance.

Coach parking sites/locations
London has a number of coach parking sites that are provided to enable operators to safely park vehicles in areas that will not impede other road users. The file provides geo-coded locations of all coach parking sites along with details such as hours of operation and charging information.

Roads
Live Traffic Disruptions - TIMS
This feed was built to replace the Live Traffic Disruptions (LTIS) feed, which was decommissioned on 1 April 2013. The new feed has been changed to capture a richer range of information about road disruptions, including improved spatial information, details of closures and more in-depth categorisation of the cause of a disruption.

Road disruptions
The Roads disruption API includes additional data on road disruptions (events and planned works) up to 12 months ahead. However, the additional data does not include polygons and affected roads. The location in the additional data may not include borough and postcode information.

Live Roadside Message Signs v2
The live roadside message signs XML feed comes direct from TfL's traffic control centre system and contains the location and live message on every sign currently displaying information in London.

Santander Cycles
Santander Cycles availability
The Santander Cycles XML feed contains the name, location, coordinates and maximum number of docking points for all operational Santander Cycles docking stations. It also contains the number of available bikes (excluding locked or faulty bikes), and number of available docking points.

Oyster
Oyster Ticket Stop locations
Our Oyster Ticket Stop locations is a geo-coded KML feed of the 3,700 outlets across London where customers can top up their Oyster card and renew a Travelcard or Bus & Tram Pass.

Accessibility
Step-Free Tube Guide Data - lrad-v2
The data contained in this xml file provides information about step-free access to platforms and trains at London Underground, London Overground, DLR and TfL Rail stations. It also contains information about toilet locations and access conditions at these stations.

Network statistics
WebCat
PTAL is a measure of Public Transport Access Level. We allow users to download the same PTAL data that is used in our Web-based Connectivity Assessment Toolkit (WebCAT). (Any data that was previously available is superseded by the data provided currently, and should no longer be used.) The use of this data, either through WebCAT or when downloaded from here, is subject to the WebCAT terms of use.

Information about the PTAL measure and the way it should be used is available from the Planning with WebCAT page. Download the 'Transport connectivity assessment guide' on that page for additional background, examples and other useful measures of connectivity to complement the work with PTAL.

PTAL values are provided for a grid of points at 100 meter intervals, covering the whole of London. The concept of presenting PTAL values for grid points is explained in detail in the guide on the Planning with WebCAT page. The available PTAL data is provided in three files, one for a recent base year and two others for future scenarios in 2021 and 2031.

Each of the files is in CSV format, containing the following data fields:

A unique identifier for each grid point
The X (Easting) coordinate, based on the British National Grid
The Y (Northing) coordinate, based on the British National Grid
The Access Index (AI) for the point (a calculated value from which we derive PTAL)
The Public Transport Access Level (PTAL)
The data can be imported into any standard GIS package using the X and Y coordinates.

Base PTAL Grid Values
2021 PTAL Grid Values
2031 PTAL Grid Values
Rolling Origin & Destination Survey (RODS)
The Rolling O&D survey is an ongoing programme to capture information about journeys on the Tube network.

London Underground passenger counts data
Passenger counts collects information about passenger numbers entering and exiting London Underground stations, largely based on the Underground ticketing system gate data.

Dial-a-Ride statistics
This quarterly report details usage, by London borough, for the specified quarter, as well as the same quarter of the previous year to allow for comparison.

Cycle Hire usage data 2012 - 2020
Cycle Hire statistics
Oyster card data
Oyster card journey information
This dataset provides a 5% sample of all Oyster card journeys performed in a week during November 2009 on bus, Tube, DLR and London Overground.
