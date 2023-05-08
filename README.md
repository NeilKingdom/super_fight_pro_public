# Purpose Statement

_"A smart phone application and martial arts body armour equipment are designed, programmed, 
assembled, and tested on the basis of cost, sustainability, durability, and manufacturability 
for the purpose of enhancing martial artist’s training regiments within the boundaries of the 
Android platform, closed source software, and client requirements."_

# Client Requirements

- At least one "training mode" (a time-selectable round)
- At least one "game mode" (a mode which has pre-defined limitations, and which focuses one area of discipline)
- Records force measurements to some degree of accuracy and repeatability (real-world units were not a requirement)
- No wearables aside from the body armour equipment that was provided to us 
- Strikes only needed to be recorded at the center of the armour, where the internal fiberglass shielding was located 
- The software would not be available to the public i.e., closed-source

# Project Goals

The project team had a few internal goals for the mobile application:

- __Simple (KISS):__ The application would target a wide age-range, thus, a simple user experience was a key indicator of success
- __Visually appealing:__ The previous project team's application failed (in our opinion) at creating
a UI design that was visually appealing. We wanted to remedy this.
- __Doing things the "proper" way:__ Proper code is subjective. We defined "proper" code to
mean closely following Android's own guidelines and documentation. Cobbled together hacks were a no-go.
This also meant using well-established libraries where possible. The hope was to make our code as
readable and future-proof as possible!

# Challenges

- __Choosing the right sensor:__ We looked into everything, from sonar to infrared to hydraulic pressure, etc.
The most cost-effective option were Force Sensing Resistors (FSR). FSRs are flexible, light-weight,
and have substantial tollerances to pressure.
- __Budget__: We were given a budget of $300 CAD. Tekscan's FlexiForce A502 FSRs cost (at the time) 
~$190 for a pack of 4. Fortunately, we were able to save cost since the previous project team had 
purchased 8 of the same sensor, which we were able to reuse.
- __Learning new technologies:__ Amongst the 3 developers (including myself) on the project team, 
none had ever used Kotlin, or developed for Android. Here are just a few of the things that we had
to learn as we developed the application: 
    - The tools provided by Android Studio
    - The idioms and syntax of Kotlin 
    - The Bluetooth protocol
    - The APIs provided by Android
    - The APIs provided by esp-idf for the ESP-32 microcontroller
- __Cooperation:__ There were many disagreements within the project team for both the hardware and
software portions of the project. We had to learn how to overcome those disagreements and how to
collaborate effectively as a team.

# Results (Software)

<div>
    <img src="./img/homepage_light_1.jpg" width="24%" alt="Home Page (Light Theme)">
    <img src="./img/homepage_light_2.jpg" width="24%" alt="Home Page (Light Theme)">
    <img src="./img/homepage_dark_1.jpg" width="24%" alt="Home Page (Dark Theme)">
    <img src="./img/homepage_dark_2.jpg" width="24%" alt="Home Page (Dark Theme)">
</div>

### Dashboard/Home Page

<br />
<br />

<div>
    <img src="./img/modespage_light_1.jpg" width="24%" alt="Modes Page (Light Theme)">
    <img src="./img/modespage_dark_1.jpg" width="24%" alt="Modes Page (Light Theme)">
    <img src="./img/modespage_light_2.jpg" width="24%" alt="Modes Page (Dark Theme)">
    <img src="./img/modespage_dark_2.jpg" width="24%" alt="Modes Page (Dark Theme)">
</div>

### Modes Selection Page and Training Mode

<br />
<br />

<div>
    <img src="./img/speedmode_light_1.jpg" width="24%" alt="Speed Mode (Light Theme)">
    <img src="./img/speedmode_dark_1.jpg" width="24%" alt="Speed Mode (Dark Theme)">
    <img src="./img/speedmode_light_2.jpg" width="24%" alt="Strength Mode (Light Theme)">
    <img src="./img/speedmode_dark_2.jpg" width="24%" alt="Strength Mode (Dark Theme)">
</div>

### Speed Mode and Strength Mode

<br />
<br />

<div>
    <img src="./img/settings_light_1.jpg" width="24%" alt="Settings (Light Theme)">
    <img src="./img/settings_dark_1.jpg" width="24%" alt="Settings (Dark Theme)">
    <img src="./img/settings_light_2.jpg" width="24%" alt="Bluetooth Settings (Light Theme)">
    <img src="./img/settings_dark_2.jpg" width="24%" alt="Bluetooth Settings (Dark Theme)">
</div>

### Settings Page and Bluetooth Connection Page

<br />
<br />

<div>
    <img src="./img/userspage_light_1.jpg" width="24%" alt="Users Page (Light Theme)">
    <img src="./img/userspage_dark_1.jpg" width="24%" alt="Users Page (Dark Theme)">
    <img src="./img/userspage_light_2.jpg" width="24%" alt="User Creation Page (Light Theme)">
    <img src="./img/userspage_dark_2.jpg" width="24%" alt="User Creation Page (Dark Theme)">
</div>

### User Select Page and User Creation Page

# Results (Hardware)

# Conclusion

We were able to meet all of the client's expectations and even exceed them in regard to the mobile
application. User profiles were included into the final build so that data displayed on the dashboard
would be coupled to the active user. A dark theme and light theme option were added, as well as the
option to select between metric and imperial units for weight. We created the required training mode,
which would display strike data on a line chart in real-time, as well as a few other stats. We also
created two game modes: speed and strength. The speed mode would record the number of hits that a 
user could land within a minute, whereas the strength mode would provide an unlimited amount of time
for the user to prepare and land their most fatal blow. 
