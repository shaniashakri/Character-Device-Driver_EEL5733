# Character-Device-Driver_EEL5733

This is an assignment for course EEL5733 UF
--------------------------------------------------------------------------------------------------------------------------------
In this assignment, you’ll change the Linux USB Keyboard driver to change the way the CAPSLOCK led is
turned on.
In the original driver, the CAPSLOCK led is turned on when the CAPSLOCK key is pressed the first
time and is turned off when it is pressed again, and is on again when it is pressed the next time,
and so on. You’ll change the code to introduce two modes into the driver: MODE1 and MODE2.
When the driver starts functioning, it is in MODE1, in which CAPSLOCK will be handled as usual.
MODE2 will be activated when NUMLOCK is pressed, CAPSLOCK is not pressed, and CAPSLOCK
is not on. When transitioning to MODE2, the CAPSLOCK led will be turned on automatically.
MODE2 will be active until NUMLOCK is pressed again.
However, when in MODE2, CAPSLOCK led will turn off when CAPSLOCK is pressed the first time
after transitioning to MODE2 and will turn on when it is pressed the next time, and so on. In
MODE2, your driver should leave the CAPSLOCK led status in a way that will be compatible with
MODE1, e.g, whether the input layer thinks the CAPSLOCK is on or not. As a result, in MODE2,
when the CAPSLOCK led is off (on) you will see that the characters that are typed on the
keyboard will be displayed in upper (lower) case mode.
Please note that this assignment requires a demo. You should schedule a time with the
TA/grader to show your code. During the demo, be prepared to answer questions about your
implementation. You can test your driver on a virtual machine, e.g., Virtual Box, and by
checking the status of your led keys and the characters you type on the terminal. Make sure to
write a message to the kernel log when mode changes happen to facilitate testing of your
driver.
You will submit your driver code, a Makefile, and a README file on CANVAS.
