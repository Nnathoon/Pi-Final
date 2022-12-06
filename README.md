# Pi-FinalThe following instructions listed below are for creating a two player reaction based game. Included below are the materials needed as well as the code that will be needed to make the game function. The goal of the game is to see which player can press their button the fastest after the LED in the middle goes off.

![IMG_5907](https://user-images.githubusercontent.com/116108477/206002504-6e8db2b2-1d4c-414b-b67c-76e2cefd1a1a.jpg)

Materials needed for this project.
-  Raspberry Pi
-  Breadboard
- LED
- Resistor 
- 2 push buttons
- 4 male to female jumper wires
- 2 male to male jumper wires

The diagram below depicts how the project is configured. (The first bread board represents the Raspberry Pi and the corresponding GPIO pins)

![[tinkercad project.png]]

Remember to remove any power from the raspberry pi when moving wires to and from different GPIO pins.

Step 1

Take your bread board and two buttons, place one button on G1 and G3 and J1 and J3. on the opposite side of the board place the second button on G28 and G30 and J28 and J30.

Adding the LED to column C 15 and 16 (long end of the LED into slot C16) and adding a resistor to A15 and -10 allowing safe voltage to the LED to not burn it out.

![[IMG_5908 1.jpg]]
Step 2

Using the two male to male jumper wires attach one wire to -1 and F1 and the other wire to -30 and F30

![[IMG_5910.jpg]]
Take one of the remaining male to female jumper wires and plug the male end into F3 and the female end into the raspberry pi onto GPIO14. 

Connect another jumper wire to F28 and GPIO15.

For the LED connect a jumper wire from A16 to GPIO4

With the last jumper wire connect it from-19 to GPIO9 (Ground pin)

![[IMG_5911.jpg]]
Step 3 

Adding the code for the reaction game requires you to use a Linux based machine creating a python file that is executable through the terminal.  to create a new file through the nano editor in the terminal type
"nano projectnamehere.py" the file extension ".py" indicates that this is a python file and is executable through python. Be sure to note your project name so you can make edits or changes at a later date and to run the script for the game.

![[IMG_5912 1.jpg]]
After the project python file has been created you and can start typing in the necessary code. You can copy the code from the screenshots below.

![[IMG_5904.jpg]]

Lines 1 and 2 are importing rules to make the LED and button function according to different rules. importing the sleep function enables time specified increments to have the LED on or off.

Lines 5-7 specify which component is attached to which GPIO in so the script can identify the correct hardware.

Lines 9 and ten enable player names to be asked and typed in to indicate who wins the game.

The value of line 12 can be changed based on preference, I found that three seconds is a good value for a pause between when the players type there names to get their fingers on the buttons. other wise the game would start immediately after player 2 types their name in.

The values of line 15 can be changed based on your personal preference, this line indicates the parameters of the minimum and maximum time the light will go off. Line 3 command allows the light to go off at a random interval anywhere from your line 15 values.

Step 4 

Now that you have the script and the understanding for the game it is recommended that you  run the file to ensure everything works properly, or to adjust the values of a few of the lines to your personal preference. type in the terminal "filename.py" to execute the file for testing.

Conclusion

After adjusting values and preforming a verification that the program is working to your liking the reaction game is complete. If for any reason something is not working please refer to the steps and pictures above.
