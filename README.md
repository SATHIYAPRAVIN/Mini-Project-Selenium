# Mini-Project-Selenium
Automates flight search on IRCTC Air using Selenium. Selects HYD to PNQ for today's date, captures available flights, validates results, and takes a screenshot. Supports Chrome &amp; Firefox, handles dropdowns, auto-suggestions, and form inputs with robust error handling and validations.

---

# IRCTC Flight Search Automation

## Description

This project automates the flight search functionality on the official IRCTC Air website ([https://www.air.irctc.co.in/](https://www.air.irctc.co.in/)) using Selenium WebDriver.

The automation script performs the following tasks:

* Launches the IRCTC Air flight search page and verifies the correct site is opened.
* Maximizes the browser window.
* Selects "HYDERABAD (HYD)" as the departure city and "PUNE (PNQ)" as the destination city using auto-suggest dropdowns.
* Picks today's date for the journey using the date picker.
* Chooses "Business" class from the traveler class dropdown.
* Clicks the "Search" button to retrieve available flights.
* Validates that the search results correspond to the selected cities and date.
* Extracts and displays the names and flight numbers of all available flights in the console.
* Captures a screenshot of the results page and saves it to the project folder.
* Supports multi-browser execution on both Chrome and Firefox.
* Handles dynamic and bootstrap dropdown elements.
* Manages form filling, error messages, and validations.

## Key Features

* Cross-browser automation (Chrome, Firefox)
* Extraction and storage of multiple flight details in collections
* Robust form handling and interaction with auto-suggest and dropdown UI components
* Validation of results to ensure data accuracy
* Screenshot capture for reporting and debugging
* Clean and maintainable Selenium WebDriver test scripts
