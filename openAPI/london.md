Unified API
Our open data spans a large spectrum of quality, accuracy and data formats. We are simplifying your access to this data with a new front-end for our unified API.
Benefits of a unified API
Available datasets
Using the unified API
How it works
Existing data sources
 
Our improved unified API has a number of benefits over our older processes:

Benefits of a unified API
Unification of the data for modes of transport into a common format and structure (common canonical data model).

The majority of the transport data provided by each mode of transport is semantically similar. Historically, the data for each mode has been shared with you in different formats and structures. This makes the development of multi-mode applications difficult as you will need to write code for each mode of transport.

The unified API presents all the data that is semantically similar for each mode of transport in the same format and consistent structures. This enables you to write once, and access all of the same types of data across all the modes of transport quickly, making multi-mode application development easier.

The core identifiers for all stations and platforms have been normalised to the national Naptan standard. This standard is an identification scheme that is supported by the DfT nationally, allowing the API to integrate data from transport authorities outside of London. The complexity of mapping between multiple identification systems used within TfL has been hidden from consumers of the API.

Live and web scale

The unified API is designed for applications to use in realtime and at high volume.

Previously the data has been provided in a variety of ways from flat file to streams. In particular the flat files encourage an approach where you create applications with copies of the data, meaning the local copy quickly becomes outdated. The new API is designed to allow you to query in realtime and on demand, so that end customers always have the latest information.

Low latency

Some data sets are time-sensitive; in particular bus and rail arrivals can be out of date within 30s. The unified API supports the latest technologies to deliver this information at the lowest possible latencies (websockets) in ways that scale to meet high volumes. This capability is delivered for rail and buses even though the source data systems use differing paradigms behind the scenes (bus Countdown uses streams, Trakernet uses polling).

Minimise structural and operational complexity

Much of TfL's source data is provided from back-office operational systems. The data is rich, but in many places it is over-complicated for most consumer applications. The unified API is designed with customer-facing applications in mind and the data that is output is designed to be easily understandable, and supportive of common customer-facing application use cases.

Support of common web and data formats

The unified API supports output in both XML and JSON format.

JSON is quickly becoming the de facto data format for web and mobile applications, due to its ease of integration into browser technologies and server technologies that support Javascript. XML is also widely used as the data interchange format for data rich applications.

JSON also allows easier integration with web-based mapping technologies such as Google Maps and Open Street map.

Supportive of future change whilst minimising user impact

The unified API acts as a mediator and façade between the users of the API and changes to the core source systems that provide the data. This shields users of the API from changes to those source systems as the API can implement logic to maintain the structures and methods that applications have been developed against.

JSON is a schema-less standard which is particularly suited to allowing new data to be incorporated without impacting previously developed solutions.

Available datasets
The API supports all the data requirements of the TfL website. Every data-driven aspect of the website (including maps) is powered by the unified API.

Some of the multi-modal core datasets included and available to developers are:

Journey Planning (current and future)
Status (current and future)
Disruptions (current) and Planned works (future)
Arrival/departure predictions (instant and websockets)
Timetables
Embarkation points and facilities
Routes and lines (topology and geographical)
Fares
Additionally, the API supports an extensive places capability for looking up and matching locations by name, postcode etc. It also includes cycle hire data.

Other datasets are also available for Cabwise, providing locations of registered taxi firms and WebCAT, which includes modelling information on transport, such as travel times between locations.
