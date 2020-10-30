# A forked work of KMB & LWB combined headway ETA

## Features from orginal works (Direct clone from Michael's wordings)

* ETA automatically refreshes every 15 seconds.

* Direct bookmark and load a specified combination of routes at a certain stop.

* The existing combination is preserved when a route serving the same stop is entered.

  For example, if routes 258D and 259D at Tuen Mun Road Interchange is already chosen,
  typing 61X into the route selection box will add 61X into the chosen combination
  with the correct direction automatically selected.

  Limitation: if the newly-added route serves the stop in both directions (e.g. 64K @ Kam Sheung Road Station),
  or passing through the same stop in the same direction twice (e.g. 54 @ Kam Sheung Road Station),
  only one of the stop will be automatically added. You can choose the alternatives manually.

* The existing combination is preserved when another stop with the same combination in the same direction is chosen.

  For example, if you have selected routes 61X, 258, 259D at Beacon Heights,
  choosing Wong Tai Sin Station from the stop list now will still load the combination of 61X, 258D, 259D,
  choosing Millennium City from the stop list will load 258D, 259D because 61X do not serve the stop.

  Limitation: if the newly-chosen stop serves the same route in the same direction twice at the exact same pole,
  e.g. choosing 71S at Kwong Fuk Playground, then choose Tai Po Market Station (TA10-T-1250-0),
  both stopping of 71S at that same pole will be selected automatically.

## Features extended in my addon works

* Change the page layout

* Using the local storage in browser to store bookmarks of your previous check.


## Installation
No installation is needed. Clone the repository and open `index.xhtml`.
It runs fully within the browser.

## Usage
1. Enter the route number.
2. Change the direction and the variant.
3. Select a stop which you want to get the ETA.
4. A list of routes appear in the box below which serve the select stop.
Select the other routes you want to see at the same time as well.
Alternatively you may type in the other routes directly into the box as well.
5. The ETA appears at the stop, which automatically reloads after 15 seconds.
6. The URL is appended with a query string. You can bookmark that link such that the ETA
of the desired combination is shown directly without selecting again.

## Demo
<<<<<<< HEAD
[A demo instance is set up.](https://j35tor.github.io/webtools/kmb_eta.xhtml)

=======
[A demo instance is set up.](https://miklcct.com/kmb_eta/)
>>>>>>> upstream/master

## Issues
* A proxy server is required to bypass the CORS restriction.
The proxy URL is defined in `scripts/Common.js`.
The address provided in the repository is a private proxy server which can only be used to
query the KMB mobile API.

## Acknowledgement
Thanks for the foundation work done by Michael Tsang and please refer to the Acknowledgement section of his orginal works
(https://github.com/miklcct/kmb-lwb-combined-headway-eta)
