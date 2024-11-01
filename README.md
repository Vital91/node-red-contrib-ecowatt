# node-red-contrib-ecowatt
Nodered Node to get RTE ecowatt forcast 

## Description
Make API call to French RTE Site  ("Réseau de Transport d'Electricité") in order to retrieve "ecowatt" forcast.

API documentation here : https://data.rte-france.com/catalog/-/api/doc/user-guide/Ecowatt/5.0

## Installation
npm i node-red-contrib-ecowatt

## Setup

0) Drag and drop "echowatt" Node into your Nodered project.
1) Go to RTE digital site : https://data.rte-france.com/create_account and create new account.
2) Login and Search for "ecowatt" application.
3) Select "Discover the API"
4) Select "Subscribe to API" --> Window "Create an application will open"
5)  Provide a Name for the application (eg. "NodeRed")
    Select Type "Web/Server"
    Click Validate
6) Goto "My Applications"
7) Select the newly created application
8) Press "Copy to base 64" button.
9) past the copied string into  "Oauth STR" properties of the "ecowatt" Node.

## Usage

- It is allowed only one call every 15mn to the API, subsequent calls are blocked until time out occure.
- Option "Use RTE Sandbox URL" allow unlimited calls but the structure returned is always the same (usefull to understand the format).
- Don't forget to subscribe to the new V5 API Version on the RTE site when you upgrade the Node !









