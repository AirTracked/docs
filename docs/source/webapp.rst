Webapp
=======

Mapview
--------

The Mapview is intended to be a simple, easy to use, and easy to understand web interface for viewing, planing, assigning and exporting routes.

It is based on Node.js and uses the `Mapbox GL JS <https://docs.mapbox.com/mapbox-gl-js/guides/>`_ library for rendering the map and the `Mapbox Optimization v2 API <https://docs.mapbox.com/api/navigation/optimization/>`_ for route calculation.
The routes can be exported as a ICS file for import into a calendar application. With this way you can use the calendar application of your choice for navigation. Cars (like Tesla) with a calendar integration can also use the calendar for navigation.


Mapbox
^^^^^^^

Why Mapbox?
''''''''''''

For short: Mapbox has a lot of free requests per month and it has more features than Google Maps.

The longer version: Google Maps is the most used map service and it is very good. But it has some disadvantages. A Google Maps object itself (just the map without any id) is free no mather how many loads the map has. But thats where the fun is only starting.
Everything else is billed via the Google Maps Platform. You can try to calculate how much you would pay via the `calculator <https://mapsplatform.google.com/pricing/>`_. There you can see that you "only" have $200 free monthly usage.
For a student project this is a sufficient contingent of free requests. But think a little bit bigger: 28.500 loads only for one SDK is not enough if you want to sell the product. And you also have to calculate the other features like the Geocoding API or the Route API.
So things can get very expensive very fast.

This is where Mapbox comes in. After Google raised the prices for Maps companies switched to Mapbox. And Mapbox has a few advantages over Google Maps. The biggest one is that you get 50.000 free loads per month on the JavaScript SDK alone.
Every API is billed separately and the amount of free requests is significantly higher than Google Maps.
For AirTrack we are also using the `Mapbox Optimization v2 API <https://docs.mapbox.com/api/navigation/optimization/>`_ witch is currently in public beta and therefore free to use. This API is used for calculating routes with a (theoretically) 1000 given waypoints.
It solves the so called "Traveling Salesman Problem" (TSP). Google Maps does not have a similar API. You can find more about the TSP `here <https://en.wikipedia.org/wiki/Travelling_salesman_problem>`_.


Mapbox vs. Google Maps Platform
''''''''''''''''''''''''''''''''

This comparison is based on what we need for AirTrack. Based on this we decided to use Mapbox.




+------------------------------------------------+----------------------------------------+----------------------+
| Features                                       | Mapbox                                 | Google Maps Platform |
+================================================+========================================+======================+
| JavaScript SDK free loads per month            | 50.000                                 | 28,500               |
+------------------------------------------------+----------------------------------------+----------------------+
|| JavaScript SDK $ per 1000 loads per month     || $5 (50.001-100.000 loads per month)   || $7                  |
||                                               || $4 (100.001-200.000 loads per month)  ||                     |
||                                               || $3(200.001-1.000.000 loads per month) ||                     |
+------------------------------------------------+----------------------------------------+----------------------+
| Geocoding API free requests per month          | 100.000                                | 28,500               |
+------------------------------------------------+----------------------------------------+----------------------+
| Route Optimization API free requests per month | Unlimited (because of public beta)     | No API               |
+------------------------------------------------+----------------------------------------+----------------------+
| API & SDK requests billed separately           | Yes                                    | No                   |
+------------------------------------------------+----------------------------------------+----------------------+
| Detailed documentation                         | Yes                                    | Yes                  |
+------------------------------------------------+----------------------------------------+----------------------+
| Support                                        | Only in paid version                   | Only in paid version |
+------------------------------------------------+----------------------------------------+----------------------+
| Custom map styles                              | Yes                                    | Yes                  |
+------------------------------------------------+----------------------------------------+----------------------+
| Offline maps                                   | Yes                                    | No                   |
+------------------------------------------------+----------------------------------------+----------------------+
| Possibility for self-hosting                   | Yes (Mapbox Atlas)                     | No                   |
+------------------------------------------------+----------------------------------------+----------------------+
| Street view                                    | No                                     | Yes                  |
+------------------------------------------------+----------------------------------------+----------------------+
| Easy implementation of dynamic map changes     | Yes                                    | No                   |
+------------------------------------------------+----------------------------------------+----------------------+
| Turf.js integration                            | Yes                                    | No                   |
+------------------------------------------------+----------------------------------------+----------------------+
| **Open Source**                                | **Yes**                                | No                   |
+------------------------------------------------+----------------------------------------+----------------------+





.. End