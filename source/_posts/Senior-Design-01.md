---
title: Senior Design Fall 2021
date: 2022-01-10 00:00:00
tags:
---

This semester I completed the first course of Senior Design at the University of Iowa. The course split us into teams where my team and I were able to put into practice everything we've learned the last three years with our degree. The course assigns three different Electrical/Computer Engineering projects that end with each team producing a final product.

# Project 1 - Digital Thermometer with Web Interface

The first project, and in my opinion the most satisfying to finsih, my team and I were given was to create a digital thermometer that was able to display the current temperature on a screen as well as on an online display.

The thermometer enclosure includes a raspberry pi for the main processing unit, a temperture probe that has been repurposed with XLR connections so that it may plugged and unplugged to and from the enclosure. In addition, there is an LCD screen to display temperature, an on/off swtich, and a button to turn on the screen and see current temperature data. The entire device is powered by a 20,100 mAh portable charger.

![Thermometer Enclosure](images/ThermoFinalPrototype.jpeg)

The thermometer uses a Raspberrry pi to run two python scripts on boot up. The first script is primarily for checking the on/off state of the device. The second script creates and runs a server and the pi then continuosly checks for user inputs, client connection and messages, and sends temperature data once a second.

![Thermometer GUI](images/ThermometerGUI.jpeg)

On the other side our computer is running a script which connects to the server the raspberry pi has created. The client receives temperature data and displays it on the graphical interface. The interface allows for Celcius and Farenheit, text messaging for threshold alerts, and visual graph to see temperature changes over time.


If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Thermometer with Web Interface Final Report](docs/ThermometerWithWebInterface.pdf)

# Project 2 - Electric Eye Safety System

The second project of the semester was to create an Electric Eye Safety System. Our team was told this was to simulate an emergency stop that you might see in a factory. If you had a conveyer belt or heavy equipment and a foreign object were to break the connections made between a laser emitter and receiver the entire process would shutdown to prevent injury.

![Electric Eye Safety System Receiver](images/ElectricEyeFinalPrototype.jpeg)

Our project was to create a receiver capable of receiving an infrared signal from a transmitter made by the professors and T.A.'s. This project was a great challenge as it made use of the circuit design knowledge I had gained in my previous courses. In order to complete this project I needed to use what I knew about hardware filtering signals, AC to DC conversion, amplification of electrical signals, unity gain amplifiers, and reading voltages using the analog converter on an Arduino.

![Electric Eye Safety System Schematic](images/ElectricEyeDiagram.jpeg)

The receiver my team and I created receives the infrared signal from the transmitter and creates a small electrical waveform. The signal passes through a buffer so there is no influence from components outside the filter portion making sure the signal comes out exactly as calculated. This project made great use of the website [Filter Wizard](https://tools.analog.com/en/filterwizard/) check it out if you ever need help creating hardware filters for your projects.The circuit the filters out the noise from ambient light so that we have a clean waveform to work with. After filtering the signal passes through an amplifier and AC to DC converter so that the signal may be read by the Arduino. If the infrared signal between Tx and Rx is broken the LED at the end of the breadboard is lit up signaling that the system must be shut down.

If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Electric Eye Safety System Final Report](docs/ElectricEyeSafetySystem.pdf)

# Project 3 - Polling Website [UI/UX Design]

The final project for the course and the most challenging for myself was to create a polling website. The website to be made had to be a polling website similar to doodlepoll.com which is a scheduling tool that allows the user to set up meetings and appointments for a large group of people. Our goal was to build on this concept and add more user intuitive and helpful features.

The website was required to have multiple pages including a home page, admin page, create poll page, modify page, poll page, and login page. In addition to login and admin page there is a harcoded username and password that allows for a single admin to sign in and make changes to polls as needed.

The website makes use of the gatsby framework which has a number of helpful plugins to make the most of the UI/UX design portion of the project. Each page was written using HTML and a majority of the stylized components like buttons and font were downloaded from libraries.

![Polling Website Storyboard](images/UIUXStoryboard.jpeg)

This project turned out to be the most challenging for me as I was an electrical engineer with a lot of experience in hardware and hardware focused programming. Luckily, my teammates who are computer science and engineering majors have a had a lot of experience in web development. This being the case my main focus and contribution was to fimiliarize myself with the gatsby framework and programming the login page for the site.


![Creating a Poll](images/UIUXHomeScreen.jpeg)

The entire website can obviously not be shown in a few screenshots but there is a report of the entire project included below.

If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Polling Website UI/UX Design Final Report](docs/PollingWebsiteUIUXDesign.pdf)