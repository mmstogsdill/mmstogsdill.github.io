---
title: Senior Design Fall 2021
date: 2022-01-10 00:00:00
tags:
---

This semester, I successfully completed the first course of Senior Design at the University of Iowa. Throughout the course, we were divided into teams, affording my team and me the opportunity to apply the knowledge we had accumulated over the past three years with our degree. The course entailed three distinct Electrical/Computer Engineering projects, each culminating in the creation of a final product.

# Project 1 - Digital Thermometer with Web Interface

The initial project, which I personally found most fulfilling, involved the development of a digital thermometer capable of displaying the current temperature on both a screen and an online interface. The thermometer enclosure houses a Raspberry Pi, serving as the main processing unit, along with a temperature probe that has been ingeniously repurposed with XLR connections, allowing for convenient plug-and-play functionality within the enclosure. Additionally, the enclosure features an LCD screen to display temperature readings, an on/off switch, and a button to activate the screen and view current temperature data. Remarkably, the entire device is powered by a 20,100 mAh portable charger.

![Thermometer Enclosure](images/ThermoFinalPrototype.jpeg)

Operating on boot-up, the thermometer utilizes a Raspberry Pi to execute two Python scripts. The first script primarily checks the device's on/off state, while the second script establishes and operates a server. The Raspberry Pi continuously monitors user inputs, client connections, messages, and sends temperature data at one-second intervals.

![Thermometer GUI](images/ThermometerGUI.jpeg)

On the receiving end, our computer runs a script that connects to the server created by the Raspberry Pi. This client script receives temperature data and presents it through a graphical interface. The interface offers options for Celsius and Fahrenheit display, text messaging for threshold alerts, and a visual graph to observe temperature changes over time.

By the end of the project, my team and I had not only learned valuable skills in electrical hardware and software but also developed a fully functional digital thermometer that showcased our knowledge and studying in Electrical/Computer Engineering.

If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Thermometer with Web Interface Final Report](docs/ThermometerWithWebInterface.pdf)

# Project 2 - Electric Eye Safety System

The second project of the semester involved the creation of an Electric Eye Safety System, designed to simulate an emergency stop scenario often encountered in industrial settings, such as factories with conveyor belts or heavy equipment. The system's goal was to prevent injuries by triggering a shutdown if a foreign object disrupted the connection between a laser emitter and receiver.

![Electric Eye Safety System Receiver](images/ElectricEyeFinalPrototype.jpeg)

Our team's specific task was to develop a receiver capable of capturing an infrared signal transmitted by the professors and T.A.'s custom-made transmitter. This project presented a significant challenge, as it demanded the application of circuit design knowledge acquired in previous courses. To successfully complete this undertaking, I had to draw upon my expertise in hardware signal filtering, AC to DC conversion, electrical signal amplification, unity gain amplifiers, and voltage reading using an analog converter on an Arduino.

![Electric Eye Safety System Schematic](images/ElectricEyeDiagram.jpeg)

The receiver we created efficiently captures the infrared signal from the transmitter and converts it into a compact electrical waveform. To ensure utmost accuracy, the signal is carefully passed through a buffer, protecting it from any external component influence and preserving its precise calculated nature. During the project, we found the website [Filter Wizard](https://tools.analog.com/en/filterwizard/) to be an invaluable resource for creating hardware filters, and I highly recommend it to anyone in need of such assistance for their projects.

The circuit we designed effectively filters out ambient light noise, producing a clean waveform that allows for seamless processing. Following the filtering stage, the signal is directed through an amplifier and an AC to DC converter, making it readable by the Arduino. Whenever the infrared signal between the transmitter and receiver is interrupted, a LED located at the end of the breadboard illuminates, signaling the imperative need to shut down the system.

Throughout this project, I gained invaluable experience and honed my skills in tackling complex engineering challenges, reaffirming my passion for Electrical/Computer Engineering.

If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Electric Eye Safety System Final Report](docs/ElectricEyeSafetySystem.pdf)

# Project 3 - Polling Website [UI/UX Design]

The final project for the course proved to be the most challenging and rewarding endeavor, as it required creating a polling website with enhanced features to rival the functionality of doodlepoll.com. This scheduling tool allows users to efficiently set up meetings and appointments for large groups, and our aim was to take this concept even further by incorporating more user-friendly and intuitive elements.

The website demanded multiple pages, each serving a distinct purpose: the home page, admin page, create poll page, modify page, poll page, and login page. Notably, the login and admin pages featured a hardcoded username and password, granting exclusive access to a single admin for making necessary poll changes.

To achieve the desired UI/UX design, we leveraged the gatsby framework, harnessing its wealth of helpful plugins. Each page was skillfully crafted using HTML, and we adorned the website with stylized components like buttons and fonts sourced from various libraries.

![Polling Website Storyboard](images/UIUXStoryboard.jpeg)

This project proved particularly challenging for me, as my background lay primarily in electrical engineering with extensive experience in hardware and hardware-focused programming. However, I was fortunate to collaborate with talented teammates majoring in computer science and engineering, who brought considerable expertise in web development to the table. With their support, I dedicated myself to mastering the gatsby framework and undertook the responsibility of programming the login page for the site.

![Creating a Poll](images/UIUXHomeScreen.jpeg)

In the end, this collaborative effort allowed me to broaden my skillset and venture into the realm of web development, highlighting the invaluable learning experiences that come from interdisciplinary teamwork.

The entire website can obviously not be shown in a few screenshots but there is a report of the entire project included below.
If you want to check out a more detailed report of the project you can see it here. This is our final report my team and I wrote to be submitted with our project.
[Broken Engineers Polling Website UI/UX Design Final Report](docs/PollingWebsiteUIUXDesign.pdf)