# Turbidity_sensor
A mini project with Arduino Uno for a turbidity sensor.
The turbidity sensor works in 3 stages

Stage 1:
The sensor initially calibrates with whatever clean liquid the user wants to measure
The calibration works by using the first 5 measurements from the LED-PHOTORESISTOR system and finding their mean value
That mean value is considered as the ideal clean state of the liquid

Stage 2:
The sensor measures during certain intervals 
Using the algorithm below it calculates how clean is the original liquid as a percentage
per = 100 - (float(base) - float(measurement));

Stage 3:
The data are sent to a connected LCD screen
