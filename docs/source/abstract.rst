AirTrack
========

Welcome to the documentation of AirTrack!

What is AirTrack?
-----------------

AirTrack is not a single application, instead it stands for a whole ecosystem.

It is a set of tools that is designed to reduce the administrative resources needed to coordinate asset inspections. They are tailored to the needs of the telecommunications industry, but can be adapted to other industries as well.

What is part of AirTrack?
'''''''''''''''''''''''''''''''''''

Currently, AirTrack consists of the following components:
* AirTrack Web (Browser based)
* AirTrack Companion (Android)

For more information about the individual components, please refer to the respective documentation.

What is the motivation behind AirTrack?
---------------------------------------

The user story of the client that requested AirTrack is as follows:

|  "As a member of FBG, I want a central tool to plan and visualize our drone inspections of telecommunication towers on a map. 
|  Previously, we were using Excel and Google Maps to keep track of our projects, but we need a more efficient and streamlined solution. 
|  The tool should allow us to easily schedule and assign inspections, track progress, and generate reports. 
|  We also need the ability to export all the stops in an ICS file for easy integration with our calendar system. 
|  This will help us save time and resources, improve our workflow, and ensure that we are meeting our clients' needs.""
|
|  -- FBG Member


According to this user story, the following requirements were defined:

* The flight data on the Android system must be automatically sent to the server.
* Each pilot must have their own account.
* The flight data is automatically converted and stored in a database.
* The assigned sites are listed in the web app. For each site there is a detailed view and a description of the location.
* Admin users can assign the sites to the pilots via the webapp.
* The web app and database must be able to scale as needed in the AWS cloud.
* The user can see his assigned sites in the Android app and can also get a detailed description of the location.
* The route to the site can be exported in the webapp as an ICS file.

We achieved these requirements by developing, configuring and using the following components:

* AirTrack Web (Browser based)
* AirTrack Companion (Android)
* AWS API Gateway
* AWS Lambda
* MongoDB Atlas
* DatCon

What are the requirements for running AirTrack?
-----------------------------------------------

AirTrack Web
''''''''''''

AirTrack Web is a web application that can be accessed from any device with a modern, up-to-date web browser.

AirTrack Companion
''''''''''''''''''

AirTrack Companion is an Android application that requires at least Android 11 (API level 30).




Installation
------------

You don't need to install anything to use AirTrack. It is a web application that can be accessed from any device with a web browser.

If you are using AirTrack Companion, you can download it from the Google Play Store or via the APK file provided in the respective repository.





.. End